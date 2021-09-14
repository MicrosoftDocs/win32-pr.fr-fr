---
description: depuis Windows Vista, la technologie tablet pc prend en charge l’entrée tactile sur les tablet pc avec des digitaliseurs compatibles avec les fonctions tactiles. cette prise en charge comprend une interface utilisateur améliorée qui facilite le ciblage et l’utilisation des commandes Windows lors de l’utilisation d’un doigt pour l’entrée.
ms.assetid: 63f1d71f-03d8-4d83-a174-e3dc7c57bad0
title: prise en charge des entrées tactiles dans Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b623630c93c33b846ab1bb491fc56fe46dfe825
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127296022"
---
# <a name="touch-input-support-in-windows-vista"></a>prise en charge des entrées tactiles dans Windows Vista

depuis Windows Vista, la technologie tablet pc prend en charge l’entrée tactile sur les tablet pc avec des digitaliseurs compatibles avec les fonctions tactiles. cette prise en charge comprend une interface utilisateur améliorée qui facilite le ciblage et l’utilisation des commandes Windows lors de l’utilisation d’un doigt pour l’entrée.

## <a name="touch-digitizer-support"></a>Prise en charge du digitaliseur tactile

### <a name="pen-and-touch-input-not-exclusive"></a>Entrée Pen et Touch non exclusive

Ne supposez pas que les entrées de stylet et de toucher s’excluent mutuellement dans les applications [**InkCollector**](inkcollector-class.md), [**InkOverlay**](inkoverlay-class.md)et [**RealTimeStylus**](realtimestylus-class.md) .

dans Windows Vista, lorsque le système reconnaît un stylet, il ignore l’entrée tactile. Autrement dit, le trait tactile se termine et le trait du stylet commence. Étant donné que cela peut changer à l’avenir, votre code ne doit pas supposer que les entrées de stylet et de toucher s’excluent mutuellement.

### <a name="other-mouse-message-sources"></a>Autres sources de message de souris

Il y a d’autres sources de messages de souris, même lorsque l’utilisateur interagit uniquement à l’aide d’un doigt ou d’un stylet. Les sources incluent des pavés tactiles, ainsi que le mouvement destiné à permettre à une application derrière une fenêtre superposée de savoir que la souris se déplace au-dessus de l’application.

### <a name="enabling-and-disabling-the-touch-input-user-interface"></a>Activation et désactivation de l’interface utilisateur d’entrée tactile

Vous pouvez activer ou désactiver l’interface utilisateur d’entrée tactile en fonction des exigences de votre application. pour ce faire, interceptez les messages de fenêtre du système d’exploitation dans une procédure de fenêtre et modifiez le message de Windows. Remplacez [WndProc](/dotnet/api/system.windows.forms.control.wndproc?view=netcore-3.1) dans votre application pour intercepter ces messages. Le \# Pseudo-code C suivant illustre l’activation et la désactivation de l’interface utilisateur d’entrée tactile. Le code illustre également l’utilisation de la même technique pour désactiver le mouvement de pression et de blocage. Cette méthode fonctionne également pour désactiver le stylet.


```C++
const int WM_TABLET_QUERY_SYSTEM_GESTURE_STATUS = 716;

const uint SYSTEM_GESTURE_STATUS_NOHOLD           = 0x00000001;
const uint SYSTEM_GESTURE_STATUS_TOUCHUI_FORCEON  = 0x00000100;
const uint SYSTEM_GESTURE_STATUS_TOUCHUI_FORCEOFF = 0x00000200;

protected override void WndProc(ref Message msg)
{
    switch (msg.Msg)
    {
        case WM_TABLET_QUERY_SYSTEM_GESTURE_STATUS:
        {
            uint result = 0;
            if (...)
            {
                result |= SYSTEM_GESTURE_STATUS_NOHOLD;
            }

            if (...)
            {
                result |= SYSTEM_GESTURE_STATUS_TOUCHUI_FORCEON;
            }

            if (...)
            {
                result |= SYSTEM_GESTURE_STATUS_TOUCHUI_FORCEOFF;
            }

            msg.Result = (IntPtr)result;
        }
        break;

        default:
            base.WndProc(ref msg);
            break;
    }
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Interface](../wintouch/windows-touch-portal.md)
</dt> </dl>

 

 
