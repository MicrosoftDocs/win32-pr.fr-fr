---
title: Windows Touch bloc-notes utilisant l’exemple Real-Time Stylus (C#)
description: consultez un exemple C# Windows touch du bloc-notes (MTScratchpadRTStylus), qui montre comment utiliser des messages tactiles Windows pour dessiner des traces des points tactiles dans une fenêtre.
ms.assetid: 8e80672f-0780-4dec-a9b4-afec0f7782ad
keywords:
- Windows Touch, exemples de code
- Windows Toucher, exemple de code
- Windows Exemples tactiles, de bloc-notes
- Exemples de bloc-notes
- Windows Touch, objet de stylet (RTS) en temps réel
ms.topic: article
ms.date: 10/28/2019
ms.openlocfilehash: a76f7a66f8bc26b7e1cad8f1fa71d9703f0c0da1ad1452a078b374a0f1603238
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055843"
---
# <a name="windows-touch-scratchpad-using-the-real-time-stylus-sample-c"></a>Windows Touch bloc-notes utilisant l’exemple Real-Time Stylus (C#)

l’exemple Windows touch du bloc-notes ([MTScratchpadRTStylus](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS)) montre comment utiliser des messages tactiles Windows pour dessiner des traces des points tactiles dans une fenêtre. Le suivi du doigt principal, celui qui a été placé en premier dans le digitaliseur, est dessiné en noir. Les doigts secondaires sont dessinés dans six autres couleurs : rouge, vert, bleu, cyan, magenta et jaune. La capture d’écran suivante montre comment l’application peut se présenter lors de son exécution.

![capture d’écran montrant l’exemple de bloc-notes tactile Windows utilisant le stylet en temps réel en c Sharp, avec des tildes noirs et rouges sur l’écran](images/mtscratchpadrtstyluscs.png)

Pour cet exemple, l’objet Real-Time Stylus (RTS) est créé et la prise en charge de plusieurs points de contact est activée. Un plug-in DynamicRenderer est ajouté au RTS pour afficher le contenu. Un plug-in, EventHandlerPlugIn, est implémenté pour effectuer le suivi du nombre de doigts et pour modifier la couleur de dessin du convertisseur dynamique. avec les deux plug-ins dans la pile de plug-in RTS, l’application Windows Touch du bloc-notes affiche le contact principal en noir et le reste des contacts dans les différentes couleurs.

Le code suivant montre comment l’EventHandlerPlugIn incrémente et décrémente le nombre de contacts et définit la couleur du convertisseur dynamique.

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

Le code suivant montre comment la RTS est créée avec la prise en charge de plusieurs points de contact.

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

Une fois la couleur de l’objet DynamicRenderer modifiée et les traits dessinés, un appel à DynamicRenderer :: Refresh entraîne l’affichage des nouveaux traits. Le code suivant montre comment effectuer cette opération dans la méthode OnPaintHandler.

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

## <a name="related-topics"></a>Rubriques connexes

[application multipoint de bloc-notes (rts/C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS), [application de bloc-notes multipoint (rts/C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp), [exemples de touches tactiles Windows](windows-touch-samples.md)
