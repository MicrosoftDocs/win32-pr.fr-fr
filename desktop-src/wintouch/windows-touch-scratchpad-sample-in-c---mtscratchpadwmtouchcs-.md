---
title: Exemple de bloc-notes Windows Touch en C (MTScratchpadWMTouchCS)
description: L’exemple de bloc-notes Windows Touch en C# montre comment utiliser des messages tactiles Windows pour dessiner des traces des points tactiles dans une fenêtre.
ms.assetid: 652124be-01a8-4df4-b590-e5c2ca3f012c
keywords:
- Windows Touch, exemples de code
- Tactile Windows, exemple de code
- Exemples tactiles Windows, bloc-notes
- Exemples de bloc-notes
ms.topic: article
ms.date: 10/28/2019
ms.openlocfilehash: 2d91c08c55f0d5b29a170a3a01c6ee882fad765f
ms.sourcegitcommit: c7fa8fc137714433c8d18b1bf71e9cf0b5bf5e80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/25/2020
ms.locfileid: "104031975"
---
# <a name="windows-touch-scratchpad-sample-c"></a><span data-ttu-id="dba76-107">Exemple de bloc-notes Windows Touch (C#)</span><span class="sxs-lookup"><span data-stu-id="dba76-107">Windows Touch Scratchpad Sample (C#)</span></span>

<span data-ttu-id="dba76-108">L' [exemple de bloc-notes Windows Touch en C#](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/CS) montre comment utiliser des messages tactiles Windows pour dessiner des traces des points tactiles dans une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="dba76-108">The [Windows Touch Scratchpad sample in C#](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/CS) shows how to use Windows Touch messages to draw traces of the touch points to a window.</span></span> <span data-ttu-id="dba76-109">Le suivi du doigt principal, celui qui a été placé en premier dans le digitaliseur, est dessiné en noir.</span><span class="sxs-lookup"><span data-stu-id="dba76-109">The trace of the primary finger, the one that was put on the digitizer first, is drawn in black.</span></span> <span data-ttu-id="dba76-110">Les doigts secondaires sont dessinés dans six autres couleurs : rouge, vert, bleu, cyan, magenta et jaune.</span><span class="sxs-lookup"><span data-stu-id="dba76-110">Secondary fingers are drawn in six other colors: red, green, blue, cyan, magenta, and yellow.</span></span> <span data-ttu-id="dba76-111">L’illustration suivante montre comment l’application peut se présenter lors de son exécution.</span><span class="sxs-lookup"><span data-stu-id="dba76-111">The following image shows how the application could look when it runs.</span></span>

![capture d’écran montrant l’exemple de bloc-notes tactile Windows en c Sharp, avec des tildes noirs, verts, bleus et rouges sur l’écran](images/mtscratchpadwmtouchcs.png)

<span data-ttu-id="dba76-113">Pour cet exemple, un formulaire touchable est créé pour gérer les messages [**WM_TOUCH**](wm-touchdown.md) .</span><span class="sxs-lookup"><span data-stu-id="dba76-113">For this sample, a touchable form is created to handle [**WM_TOUCH**](wm-touchdown.md) messages.</span></span> <span data-ttu-id="dba76-114">Ce formulaire est hérité pour activer la fonction tactile Windows sur l’application du bloc-notes.</span><span class="sxs-lookup"><span data-stu-id="dba76-114">This form is inherited to enable Windows Touch on the scratchpad application.</span></span> <span data-ttu-id="dba76-115">Lorsque les messages de **WM_TOUCH** sont envoyés au formulaire, ils sont interprétés en points et ajoutés à la collection de traits.</span><span class="sxs-lookup"><span data-stu-id="dba76-115">When the **WM_TOUCH** messages come to the form, they are interpreted into points and are added to the collection of strokes.</span></span> <span data-ttu-id="dba76-116">La collection de traits est rendue dans l’objet Graphics.</span><span class="sxs-lookup"><span data-stu-id="dba76-116">The strokes collection is rendered to the Graphics object.</span></span> <span data-ttu-id="dba76-117">Le code suivant montre comment le formulaire touchable s’inscrit pour la gestion des messages **WM_TOUCH** et comment il gère les messages **WM_TOUCH** .</span><span class="sxs-lookup"><span data-stu-id="dba76-117">The following code shows how the touchable form registers itself for handling **WM_TOUCH** messages, and how it handles **WM_TOUCH** messages.</span></span>

```CSharp
        private void OnLoadHandler(Object sender, EventArgs e)
        {
            try
            {
                // Registering the window for multi-touch, using the default settings.
                // p/invoking into user32.dll
                if (!RegisterTouchWindow(this.Handle, 0))
                {
                    Debug.Print("ERROR: Could not register window for multi-touch");
                }
            }
            catch (Exception exception)
            {
                Debug.Print("ERROR: RegisterTouchWindow API not available");
                Debug.Print(exception.ToString());
                MessageBox.Show("RegisterTouchWindow API not available", "MTScratchpadWMTouch ERROR",
                    MessageBoxButtons.OK, MessageBoxIcon.Error, MessageBoxDefaultButton.Button1, 0);
            }
        }
(...)
        [PermissionSet(SecurityAction.Demand, Name = "FullTrust")]
        protected override void WndProc(ref Message m)
        {
            // Decode and handle WM_TOUCH message.
            bool handled;
            switch (m.Msg)
            {
                case WM_TOUCH:
                    handled = DecodeTouch(ref m);
                    break;
                default:
                    handled = false;
                    break;
            }

            // Call parent WndProc for default message processing.
            base.WndProc(ref m);

            if (handled)
            {
                // Acknowledge event if handled.
                m.Result = new System.IntPtr(1);
            }
        }
```

<span data-ttu-id="dba76-118">Le code suivant montre comment le message tactile Windows est interprété et les données sont ajoutées aux collections Stroke.</span><span class="sxs-lookup"><span data-stu-id="dba76-118">The following code shows how the Windows Touch message is interpreted and the data is added to stroke collections.</span></span>

```CSharp
        private bool DecodeTouch(ref Message m)
        {
            // More than one touchinput may be associated with a touch message,
            // so an array is needed to get all event information.
            int inputCount = LoWord(m.WParam.ToInt32()); // Number of touch inputs, actual per-contact messages

            TOUCHINPUT[] inputs; // Array of TOUCHINPUT structures
            inputs = new TOUCHINPUT[inputCount]; // Allocate the storage for the parameters of the per-contact messages

            // Unpack message parameters into the array of TOUCHINPUT structures, each
            // representing a message for one single contact.
            if (!GetTouchInputInfo(m.LParam, inputCount, inputs, touchInputSize))
            {
                // Get touch info failed.
                return false;
            }

            // For each contact, dispatch the message to the appropriate message
            // handler.
            bool handled = false; // Boolean, is message handled
            for (int i = 0; i < inputCount; i++)
            {
                TOUCHINPUT ti = inputs[i];

                // Assign a handler to this message.
                EventHandler<WMTouchEventArgs> handler = null;     // Touch event handler
                if ((ti.dwFlags & TOUCHEVENTF_DOWN) != 0)
                {
                    handler = Touchdown;
                }
                else if ((ti.dwFlags & TOUCHEVENTF_UP) != 0)
                {
                    handler = Touchup;
                }
                else if ((ti.dwFlags & TOUCHEVENTF_MOVE) != 0)
                {
                    handler = TouchMove;
                }

                // Convert message parameters into touch event arguments and handle the event.
                if (handler != null)
                {
                    // Convert the raw touchinput message into a touchevent.
                    WMTouchEventArgs te = new WMTouchEventArgs(); // Touch event arguments

                    // TOUCHINFO point coordinates and contact size is in 1/100 of a pixel; convert it to pixels.
                    // Also convert screen to client coordinates.
                    te.ContactY = ti.cyContact/100;
                    te.ContactX = ti.cxContact/100;
                    te.Id = ti.dwID;
                    {
                        Point pt = PointToClient(new Point(ti.x/100, ti.y/100));
                        te.LocationX = pt.X;
                        te.LocationY = pt.Y;
                    }
                    te.Time = ti.dwTime;
                    te.Mask = ti.dwMask;
                    te.Flags = ti.dwFlags;

                    // Invoke the event handler.
                    handler(this, te);

                    // Mark this event as handled.
                    handled = true;
                }
            }

            CloseTouchInputHandle(m.LParam);

            return handled;
        }
    }
```

<span data-ttu-id="dba76-119">Le code suivant illustre l’affichage d’une collection Stroke.</span><span class="sxs-lookup"><span data-stu-id="dba76-119">The following code shows how a stroke collection is displayed.</span></span>

```CSharp
        public void Draw(Graphics graphics)
        {
            if ((points.Count < 2) || (graphics == null))
            {
                return;
            }

            Pen pen = new Pen(color, penWidth);
            graphics.DrawLines(pen, (Point[]) points.ToArray(typeof(Point)));
        }
```

<span data-ttu-id="dba76-120">Le code suivant montre comment les objets Stroke individuels s’affichent avec un objet Graphics.</span><span class="sxs-lookup"><span data-stu-id="dba76-120">The following code shows how the individual stroke objects display themselves with a Graphics object.</span></span>

```CSharp
        public void Draw(Graphics graphics)
        {
            if(points.Count < 2 || graphics == null)
            {
                return;
            }

            Pen pen = new Pen(color, penWidth);
            graphics.DrawLines(pen, (Point[]) points.ToArray(typeof(Point)));
        }
```

## <a name="related-topics"></a><span data-ttu-id="dba76-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dba76-121">Related topics</span></span>

<span data-ttu-id="dba76-122">[Exemple de bloc-notes Windows Touch (C++)](windows-touch-scratchpad-sample--mtscratchpadwmtouch-.md), [application multipoint de bloc-notes (WM_TOUCH/c #)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/CS), [application de bloc-notes multipoint (WM_TOUCH/C + +)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/cpp), [exemples de fonctions tactiles Windows](windows-touch-samples.md)</span><span class="sxs-lookup"><span data-stu-id="dba76-122">[Windows Touch Scratchpad Sample (C++)](windows-touch-scratchpad-sample--mtscratchpadwmtouch-.md), [Multi-touch Scratchpad Application (WM_TOUCH/C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/CS), [Multi-touch Scratchpad Application (WM_TOUCH/C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/cpp), [Windows Touch Samples](windows-touch-samples.md)</span></span>

