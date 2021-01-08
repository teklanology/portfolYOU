Interaction with the model open in Tekla Structures requires creating a Model instance.

```cs
// Create a new instance of Model class. 
Model model = new Model();
```

Once the Model instance has been created, the following methods can be implemented

## CommitChanges()

Commits changes made to the model.

```cs
Model model = new Model();

// write code here

model.CommitChanges();
```

## FetchModelObjects

Returns a list of model objects from a GUID list.

```cs
Model model = new Model();

TSMUI.ModelObjectSelector modelObjectSelector = new TSMUI.ModelObjectSelector();
ModelObjectEnumerator modelObjectEnum = modelObjectSelector.GetSelectedObjects();
var guids = new List<string>();
// ...
var modelObjects = model.FetchModelObjects(guidList, true);
```

## GetClashCheckHandler

Returns a new clash check handler.

```cs
Model model = new Model();

ClashCheckHandler clashCheckHandler = model.GetClashCheckHandler();
clashCheckHandler.RunClashCheck();
clashCheckHandler.StopClashCheck();
```

## GetConnectionStatus

Returns true if a connection to Tekla Structures has succeeded.

```cs
Model model = new Model();

// check if connection has succeeded?
if (model.GetConnectionStatus())
{ 
    Console.WriteLine("Connection succeeded!");
}
```

## GetGUIDByIdentifier

Returns the GUID of the given identifier instance.

```cs
Model model = new Model();
var guid = model.GetGUIDByIdentifier(new Identifier(12345678)); 
```

## GetIdentifierByGUID

Returns an identifier instance that has the given GUID in the model.

```cs
Model model = new Model();
Identifier identifier = model.GetIdentifierByGUID("...");
```

## GetInfo

Returns a ModelInfo object containing information about the current model.

```cs
Model model = new Model();
ModelInfo modelInfo = model.GetInfo();
Console.WriteLine(modelInfo.ModelName);
```

## GetModelObjectSelector

Returns an instance of the ModelObjectSelector object from which different selections can be made.

```cs
Model model = new Model();
model.GetModelObjectSelector().GetAllObjects();
```

## GetPhases

Returns a PhaseCollection object containing information about the phases in the current model.

```cs
Model model = new Model();
PhaseCollection phaseCollection = model.GetPhases();
foreach (Phase phase in phaseCollection)
{
    Console.WriteLine(phase.PhaseNumber);
}
```

## GetProjectInfo

Returns a ProjectInfo object containing information about the project properties in the current model.

```cs
Model model = new Model();
ProjectInfo projectInfo = model.GetProjectInfo();
Console.WriteLine(projectInfo.ProjectNumber);
```

## GetWorkPlaneHandler

Returns a work plane handler for the current model, which is used to manipulate the work plane in the model.

```cs
Model model = new Model();
WorkPlaneHandler workPlaneHandler = model.GetWorkPlaneHandler();
workPlaneHandler.GetCurrentTransformationPlane();
```

## SelectModelObject

Using an identifier to an object, it checks its type, instantiates and selects it before returning it.

```cs
Model model = new Model();
ModelObject modelObject = model.SelectModelObject(new Identifier(12345678));
```