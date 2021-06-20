---
title: Bloc-notes Windows Touch utilisant l’exemple Real-Time Stylus (C#)
description: Consultez l’exemple C# de bloc-notes Windows Touch (MTScratchpadRTStylus), qui montre comment utiliser des messages tactiles Windows pour dessiner des traces des points tactiles dans une fenêtre.
ms.assetid: 8e80672f-0780-4dec-a9b4-afec0f7782ad
keywords:
- Windows Touch, exemples de code
- Tactile Windows, exemple de code
- Exemples tactiles Windows, bloc-notes
- Exemples de bloc-notes
- Interface tactile Windows, objet de stylet (RTS) en temps réel
ms.topic: article
ms.date: 10/28/2019
ms.openlocfilehash: 3c30d3543024a48394ddd7b9b2b06a05b61f5025
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406312"
---
# <a name="windows-touch-scratchpad-using-the-real-time-stylus-sample-c"></a><span data-ttu-id="7a5c2-108">Bloc-notes Windows Touch utilisant l’exemple Real-Time Stylus (C#)</span><span class="sxs-lookup"><span data-stu-id="7a5c2-108">Windows Touch Scratchpad using the Real-Time Stylus Sample (C#)</span></span>

<span data-ttu-id="7a5c2-109">L’exemple du bloc-notes Windows Touch ([MTScratchpadRTStylus](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS)) montre comment utiliser des messages tactiles Windows pour dessiner les traces des points tactiles dans une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="7a5c2-109">The Windows Touch Scratchpad sample ([MTScratchpadRTStylus](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS)) shows how to use Windows Touch messages to draw traces of the touch points to a window.</span></span> <span data-ttu-id="7a5c2-110">Le suivi du doigt principal, celui qui a été placé en premier dans le digitaliseur, est dessiné en noir.</span><span class="sxs-lookup"><span data-stu-id="7a5c2-110">The trace of the primary finger, the one that was put on the digitizer first, is drawn in black.</span></span> <span data-ttu-id="7a5c2-111">Les doigts secondaires sont dessinés dans six autres couleurs : rouge, vert, bleu, cyan, magenta et jaune.</span><span class="sxs-lookup"><span data-stu-id="7a5c2-111">Secondary fingers are drawn in six other colors: red, green, blue, cyan, magenta and yellow.</span></span> <span data-ttu-id="7a5c2-112">La capture d’écran suivante montre comment l’application peut se présenter lors de son exécution.</span><span class="sxs-lookup"><span data-stu-id="7a5c2-112">The following screen shot shows how the application could look while running.</span></span>

![capture d’écran montrant l’exemple de bloc-notes tactile Windows utilisant le stylet en temps réel en c Sharp, avec des tildes noirs et rouges sur l’écran](images/mtscratchpadrtstyluscs.png)

<span data-ttu-id="7a5c2-114">Pour cet exemple, l’objet Real-Time Stylus (RTS) est créé et la prise en charge de plusieurs points de contact est activée.</span><span class="sxs-lookup"><span data-stu-id="7a5c2-114">For this sample, the Real-Time Stylus (RTS) object is created and support for multiple contact points is enabled.</span></span> <span data-ttu-id="7a5c2-115">Un plug-in DynamicRenderer est ajouté au RTS pour afficher le contenu.</span><span class="sxs-lookup"><span data-stu-id="7a5c2-115">A DynamicRenderer plug-in is added to the RTS to render content.</span></span> <span data-ttu-id="7a5c2-116">Un plug-in, EventHandlerPlugIn, est implémenté pour effectuer le suivi du nombre de doigts et pour modifier la couleur de dessin du convertisseur dynamique.</span><span class="sxs-lookup"><span data-stu-id="7a5c2-116">A plug-in, EventHandlerPlugIn, is implemented to track down the number of fingers and to change the color that the dynamic renderer is drawing.</span></span> <span data-ttu-id="7a5c2-117">Avec les deux plug-ins dans la pile de plug-in RTS, l’application Windows Touch du bloc-notes affiche le contact principal en noir et le reste des contacts dans les différentes couleurs.</span><span class="sxs-lookup"><span data-stu-id="7a5c2-117">With both plug-ins in the RTS plug-in stack, the Windows Touch Scratchpad application will render the primary contact in black and the rest of the contacts in the various colors.</span></span>

<span data-ttu-id="7a5c2-118">Le code suivant montre comment l’EventHandlerPlugIn incrémente et décrémente le nombre de contacts et définit la couleur du convertisseur dynamique.</span><span class="sxs-lookup"><span data-stu-id="7a5c2-118">The following code shows how the EventHandlerPlugIn increments and decrements a count of the number of contacts and sets the color of the dynamic renderer.</span></span>

```CSharp
        public void StylusDown(RealTimeStylus sender, StylusDownData data)
        {
            // Set new stroke color to the DrawingAttributes of the DynamicRenderer
            // If there are no fingers down, this is a primary contact
            dynamicRenderer.DrawingAttributes.Color = touchColor.GetColor(cntContacts == 0);

            ++cntContacts;  // Increment finger-down counter
        }

        public void StylusUp(RealTimeStylus sender, StylusUpData data)
        {
            --cntContacts;  // Decrement finger-down counter
        }
```

<span data-ttu-id="7a5c2-119">Le code suivant montre comment la RTS est créée avec la prise en charge de plusieurs points de contact.</span><span class="sxs-lookup"><span data-stu-id="7a5c2-119">The following code shows how the RTS is created with multiple contact point support.</span></span>

```CSharp
        private void OnLoadHandler(Object sender, EventArgs e)
        {
            // Create RealTimeStylus object and enable it for multi-touch
            realTimeStylus = new RealTimeStylus(this);
            realTimeStylus.MultiTouchEnabled = true;

            // Create DynamicRenderer and event handler, and add them to the RTS object as synchronous plugins
            dynamicRenderer = new DynamicRenderer(this);
            eventHandler = new EventHandlerPlugIn(this.CreateGraphics(), dynamicRenderer);
            realTimeStylus.SyncPluginCollection.Add(eventHandler);
            realTimeStylus.SyncPluginCollection.Add(dynamicRenderer);

            // Enable RTS and DynamicRenderer object, and enable auto-redraw of the DynamicRenderer
            realTimeStylus.Enabled = true;
            dynamicRenderer.Enabled = true;
            dynamicRenderer.EnableDataCache = true;
        }
```

<span data-ttu-id="7a5c2-120">Une fois la couleur de l’objet DynamicRenderer modifiée et les traits dessinés, un appel à DynamicRenderer :: Refresh entraîne l’affichage des nouveaux traits.</span><span class="sxs-lookup"><span data-stu-id="7a5c2-120">After the DynamicRenderer object's color has changed and strokes have been drawn, a call to DynamicRenderer::Refresh will cause the new strokes to appear.</span></span> <span data-ttu-id="7a5c2-121">Le code suivant montre comment effectuer cette opération dans la méthode OnPaintHandler.</span><span class="sxs-lookup"><span data-stu-id="7a5c2-121">The following code shows how this is performed in the OnPaintHandler method.</span></span>

```CSharp
        private void OnPaintHandler(object sender, PaintEventArgs e)
        {
            // Erase the background
            Brush brush = new SolidBrush(SystemColors.Window);
            e.Graphics.FillRectangle(brush, ClientRectangle);

            // Ask DynamicRenderer to redraw itself
            dynamicRenderer.Refresh();
        }
```

## <a name="related-topics"></a><span data-ttu-id="7a5c2-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7a5c2-122">Related topics</span></span>

<span data-ttu-id="7a5c2-123">[Application multipoint de bloc-notes (RTS/C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS), [application de bloc-notes multipoint (RTS/C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp), [exemples de fonctions tactiles Windows](windows-touch-samples.md)</span><span class="sxs-lookup"><span data-stu-id="7a5c2-123">[Multi-touch Scratchpad Application (RTS/C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS), [Multi-touch Scratchpad Application (RTS/C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp), [Windows Touch Samples](windows-touch-samples.md)</span></span>
