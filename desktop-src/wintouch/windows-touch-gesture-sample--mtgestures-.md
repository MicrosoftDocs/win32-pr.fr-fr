---
title: Windows Exemple de mouvement tactile (MTGestures)
description: cette section décrit l’exemple de mouvement tactile Windows.
ms.assetid: 04166c9c-5de7-409e-9d5e-dd210a3a3f11
keywords:
- Windows Touch, exemples de code
- Windows Toucher, exemple de code
- Windows Toucher, mouvements
- Windows Toucher, exemples de geste
- Exemples de mouvements
- gestes, exemple de code
- mouvements, exemples de code
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: 656b269eae779cd999680e165ba071d983d18526c2e9b873c5a916d61ccdb9f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110582"
---
# <a name="windows-touch-gesture-sample-mtgestures"></a>Windows Exemple de mouvement tactile (MTGestures)

cette section décrit l’exemple de mouvement tactile Windows.

l’exemple de mouvement tactile Windows montre comment utiliser des messages de mouvement pour translater, faire pivoter et mettre à l’échelle une zone rendue par le Graphics Device Interface (GDI) en gérant le message d' [**WM_GESTURE**](wm-gesture.md) . La capture d’écran suivante montre comment l’exemple apparaît lorsqu’il est en cours d’exécution.

![capture d’écran montrant l’exemple de mouvement tactile Windows lorsqu’il est en cours d’exécution, avec un rectangle blanc pivoté et entouré d’un noir à l’écran](images/mtgestures.png)

Pour cet exemple, les messages de mouvement sont passés à un moteur de mouvement, qui appelle ensuite des méthodes sur des objets de dessin pour translater, faire pivoter et mettre à l’échelle un objet qui a des méthodes pour gérer ces commandes. Pour vous aider à voir comment fonctionne l’exemple, examinez les étapes d’utilisation de la commande TAP à deux doigts pour activer ou désactiver les lignes diagonales dans la zone rendue. Un utilisateur effectue le mouvement TAP à deux doigts, ce qui génère un message géré par le programme. Lorsque le message est géré, il bascule une valeur booléenne pour le rendu des diagonales sur l’objet de dessin, et l’objet restitue ensuite les lignes diagonales.

Le code suivant montre comment les messages de mouvement sont passés au moteur de mouvement à partir de la méthode WndProc.

```C++
    case WM_GESTURE:
        // The gesture-processing code is implemented in the CGestureEngine
        // class.
        return g_cGestureEngine.WndProc(hWnd,wParam,lParam);
        break;
```

Le code suivant montre comment le moteur de mouvement gère la commande TAP à deux doigts.

```C++
// Two-finger tap command
void CMyGestureEngine::ProcessTwoFingerTap(void)
{
    if(_pcRect)
    {
        _pcRect->ToggleDrawDiagonals();
    }
}
```

Le code suivant montre comment l’objet Drawing bascule ses diagonales.

```C++
void ToggleDrawDiagonals(void){_bDrawDiagonals = !_bDrawDiagonals;}
```

Le code suivant montre comment l’objet restitue des lignes diagonales dans sa méthode Draw.

```C++
    if(_bDrawDiagonals)
    {
        // draw diagonals
        MoveToEx(hdc,ptRect[0].x,ptRect[0].y,NULL);
        LineTo(hdc,ptRect[2].x,ptRect[2].y);
        MoveToEx(hdc,ptRect[1].x,ptRect[1].y,NULL);
        LineTo(hdc,ptRect[3].x,ptRect[3].y);
    }
```

## <a name="related-topics"></a>Rubriques connexes

[application de mouvements tactiles multiples (C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/CS), [application de gestes multipoint (C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/cpp), exemples de [touches tactiles Windows](windows-touch-samples.md)
