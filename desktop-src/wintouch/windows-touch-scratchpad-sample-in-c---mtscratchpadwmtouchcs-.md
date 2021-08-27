---
title: Windows Exemple Touch du bloc-notes en C (MTScratchpadWMTouchCS)
description: l’exemple Windows touch du bloc-notes en C# montre comment utiliser des messages tactiles Windows pour dessiner des traces des points tactiles dans une fenêtre.
ms.assetid: 652124be-01a8-4df4-b590-e5c2ca3f012c
keywords:
- Windows Touch, exemples de code
- Windows Toucher, exemple de code
- Windows Exemples tactiles, de bloc-notes
- Exemples de bloc-notes
ms.topic: article
ms.date: 10/28/2019
ms.openlocfilehash: 112f8446af4b845bfd36e4262a11da807535c93baaf6257a10a9a8d2b03374e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089843"
---
# <a name="windows-touch-scratchpad-sample-c"></a>Windows Touch bloc-notes, exemple (C#)

l' [exemple Windows touch du bloc-notes en C#](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/CS) montre comment utiliser des messages tactiles Windows pour dessiner des traces des points tactiles dans une fenêtre. Le suivi du doigt principal, celui qui a été placé en premier dans le digitaliseur, est dessiné en noir. Les doigts secondaires sont dessinés dans six autres couleurs : rouge, vert, bleu, cyan, magenta et jaune. L’illustration suivante montre comment l’application peut se présenter lors de son exécution.

![capture d’écran montrant l’exemple de bloc-notes tactile Windows en c Sharp, avec des tildes noirs, verts, bleus et rouges sur l’écran](images/mtscratchpadwmtouchcs.png)

Pour cet exemple, un formulaire touchable est créé pour gérer les messages [**WM_TOUCH**](wm-touchdown.md) . ce formulaire est hérité pour permettre Windows Touch sur l’application du bloc-notes. Lorsque les messages de **WM_TOUCH** sont envoyés au formulaire, ils sont interprétés en points et ajoutés à la collection de traits. La collection de traits est rendue dans l’objet Graphics. Le code suivant montre comment le formulaire touchable s’inscrit pour la gestion des messages **WM_TOUCH** et comment il gère les messages **WM_TOUCH** .

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

le code suivant montre comment l’Windows message tactile est interprété et les données sont ajoutées aux collections stroke.

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

Le code suivant illustre l’affichage d’une collection Stroke.

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

Le code suivant montre comment les objets Stroke individuels s’affichent avec un objet Graphics.

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

## <a name="related-topics"></a>Rubriques connexes

[exemple de Windows touch de bloc-notes (C++)](windows-touch-scratchpad-sample--mtscratchpadwmtouch-.md), [application multipoint de bloc-notes (WM_TOUCH/c #)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/CS), [application de bloc-notes multipoint (WM_TOUCH/c + +)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/cpp), exemples d’applications [tactiles Windows](windows-touch-samples.md)

