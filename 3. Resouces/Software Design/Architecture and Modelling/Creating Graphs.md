# Mermaid Graphs
## Creating graphs from code

 [Mermaid ](https://mermaid-js.github.io/mermaid/#/) is a Javascript  package that enables the rendering of graphs from text based descriptions. The [web page](https://mermaid-js.github.io/mermaid/#/README) contains a number of really good examples of how to create various diagram types.  The section on [flowcharts](https://mermaid-js.github.io/mermaid/#/flowchart) is particularly good. 

Here is an example of a Mermaid graph created using mark down

```mermaid
graph TD;

subgraph Unsupported Files;
    Extract(Extract Unsupported Files)-->SaveFiles(Save Files)-->
    DetermineFileType(Determine FileType)-->WhichFile{File Type};
    WhichFile--D0150-->150header(Change D0150 header to V1);
    WhichFile--D0268-->268Destination{File destination}
	268Destination--MARS-->268header(Convert D0268 header to V1);
	268Destination--AMS-->268structure(Convert D0268 Structure to V1);
	WhichFile--D0313-->313Structure(Update D0313 structure);
    150header & 313Structure & 268header & 268structure -->Export(Export Files);
    Export-->LoadDTNFiles(Load files to DTNIN);
end;

subgraph Failed D0268 Files from MARS
    LoadDTNFiles(Load files to DTNIN)-->ExtractFailed;
    ExtractFailed(Extract Failed D0268 Files from MARS)-->SaveFailedFiles(Save Files)-->IdentifyDestination{Identify Destination}
    IdentifyDestination--AMS-->ConvertAMS(Change Structure to V001)-->MoveAMS(Move to AMSOUT)
    IdentifyDestination--DTN-->Change268Header(Change D0268 Header to  V002)-->MoveDTN(Move to DTNOUT)
    IdentifyDestination--Galvani-->Change268Header-->MoveGalvani(Move to GalvaniOUT)
    MoveAMS-->LoadFiles
    MoveDTN-->LoadFiles
    MoveGalvani-->LoadFiles
end;
subgraph Re-process Sidelined Files 
    LoadFiles(Load files)-->Sidelined;
    Sidelined(Extract Sidelined Files)-->SaveSidelinedFiles(Save Ver 1 D0313 and D0150  Files)-->ConvertSidelined(Convert to Version 2)-->
    MovetoDTNOut(Move to DTNOUT)-->LoadtoDTNOUT(Load to DTNTOUT)
end;
```