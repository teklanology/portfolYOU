In this guide we explain how to iterate through model and drawing objects in the current model or drawing.

For models, use the class ModelObjectEnumerator and for drawings, DrawingObjectEnumerator.

Enumerate model objects
The ModelObjectEnumerator class provides the means to iterate through model object instances in the current model.

This example shows how to enumerate all selected objects of Beam type and get the solid information of the beams.

```csharp
ModelObjectEnumerator Enum = myModel.GetModelObjectSelector().GetAllObjects();

while (Enum.MoveNext())
{
    Beam B = Enum.Current as Beam;
    if (B != null)
    {
        Solid Solid = B.GetSolid();
    }
}
```