Before you can access any of the Tekla Open API objects, you will need to initialize the connection between Tekla Structures and your application.

Because applications are not started together with Tekla Structures they cannot expect to have Tekla Structures running upon execution.

In this guide we go trough two ways of checking if the Tekla Structures is running and a model is open.

For drawings, the following creates a new instance to the drawings object:

```csharp
DrawingHandler CurrentDrawingHandler = new DrawingHandler();
```