---
title: Exemple de bloc-notes Windows Touch (C++)
description: L’exemple Windows Touch du bloc-notes montre comment utiliser des messages tactiles Windows pour dessiner les traces des points tactiles dans une fenêtre.
ms.assetid: 6c4b4595-1e95-499c-b045-b5ae01aa5a6e
keywords:
- Windows Touch, exemples de code
- Tactile Windows, exemple de code
- Exemples tactiles Windows, bloc-notes
- Exemples de bloc-notes
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: afdd39e886d97671942b4ff67a74c0da75924fbb
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104032058"
---
# <a name="windows-touch-scratchpad-sample-c"></a>Exemple de bloc-notes Windows Touch (C++)

L' [exemple Windows Touch du bloc-notes](https://github.com/MicrosoftDocs/win32-pr/blob/master/desktop-src/wintouch/windows-touch-scratchpad-sample--mtscratchpadwmtouch-.md) montre comment utiliser des messages tactiles Windows pour dessiner les traces des points tactiles dans une fenêtre. Le suivi du doigt principal, celui qui a été placé en premier dans le digitaliseur, est dessiné en noir. Les doigts secondaires sont dessinés dans six autres couleurs : rouge, vert, bleu, cyan, magenta et jaune. L’illustration suivante montre comment l’application peut se présenter lors de son exécution.

![capture d’écran montrant le bloc-notes tactile Windows, avec des tildes rouges et noirs à l’écran](images/mtscratchpadwmtouch.png)

Pour cette application, la fenêtre est inscrite en tant que fenêtre tactile, les messages tactiles sont interprétés pour ajouter des points tactiles aux objets Stroke et les traits d’encre sont rendus à l’écran dans le gestionnaire de messages **WM_PAINT** .

Le code suivant montre comment la fenêtre est inscrite en tant que fenêtre tactile.

```C++
    // Register application window for receiving multitouch input. Use default settings.
    if(!RegisterTouchWindow(hWnd, 0))
    {
        MessageBox(hWnd, L"Cannot register application window for multitouch input", L"Error", MB_OK);
        return FALSE;
    }
```

Le code suivant montre comment les messages tactiles sont utilisés pour ajouter des points tactiles aux traits d’encre.

```C++
        // WM_TOUCH message handlers
        case WM_TOUCH:
            {
                // WM_TOUCH message can contain several messages from different contacts
                // packed together.
                // Message parameters need to be decoded:
                unsigned int numInputs = (unsigned int) wParam; // Number of actual per-contact messages
                TOUCHINPUT* ti = new TOUCHINPUT[numInputs]; // Allocate the storage for the parameters of the per-contact messages
                if(ti == NULL)
                {
                    break;
                }
                // Unpack message parameters into the array of TOUCHINPUT structures, each
                // representing a message for one single contact.
                if(GetTouchInputInfo((HTOUCHINPUT)lParam, numInputs, ti, sizeof(TOUCHINPUT)))
                {
                    // For each contact, dispatch the message to the appropriate message
                    // handler.
                    for(unsigned int i=0; i<numInputs; ++i)
                    {
                        if(ti[i].dwFlags & TOUCHEVENTF_DOWN)
                        {
                            OnTouchDownHandler(hWnd, ti[i]);
                        }
                        else if(ti[i].dwFlags & TOUCHEVENTF_MOVE)
                        {
                            OnTouchMoveHandler(hWnd, ti[i]);
                        }
                        else if(ti[i].dwFlags & TOUCHEVENTF_UP)
                        {
                            OnTouchUpHandler(hWnd, ti[i]);
                        }
                    }
                }
                CloseTouchInputHandle((HTOUCHINPUT)lParam);
                delete [] ti;
            }
            break;
```

Le code suivant montre comment les traits d’encre sont dessinés à l’écran dans le gestionnaire de messages **WM_PAINT** .

```C++
        case WM_PAINT:
            hdc = BeginPaint(hWnd, &ps);
            // Full redraw: draw complete collection of finished strokes and
            // also all the strokes that are currently in drawing.
            g_StrkColFinished.Draw(hdc);
            g_StrkColDrawing.Draw(hdc);
            EndPaint(hWnd, &ps);
            break;
```

Le code suivant montre comment l’objet Stroke affiche les traits à l’écran.

```C++
void CStroke::Draw(HDC hDC) const
{
    if(m_nCount < 2)
    {
        return;
    }

    HPEN hPen = CreatePen(PS_SOLID, 3, m_clr);
    HGDIOBJ hOldPen = SelectObject(hDC, hPen);
    Polyline(hDC, m_arrData, m_nCount);
    SelectObject(hDC, hOldPen);
    DeleteObject(hPen);
}
```

## <a name="related-topics"></a>Rubriques connexes

[Exemple de bloc-notes Windows Touch (C#)](windows-touch-scratchpad-sample-in-c---mtscratchpadwmtouchcs-.md), [application de bloc-notes multipoint (WM_TOUCH/c #)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/CS), [application de bloc-notes multipoint (WM_TOUCH/C + +)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/cpp), [exemples de fonctions tactiles Windows](windows-touch-samples.md)
