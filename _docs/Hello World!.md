Hello World!

This is a basic example of a Tekla Structures macro that displays a message box saying "Hello World!".

Refer to https://teklanology.github.io/blog/csharp-basics for a breakdown.

```csharp
using System.Windows.Forms;

namespace Tekla.Technology.Akit.UserScript
{
    // A version of the classic "Hello, World! program
    static class Script
    {
        public static void Run(Tekla.Technology.Akit.IScript RunMe)
        {
            MessageBox.Show("Hello, World!");
        }
    }
}
```