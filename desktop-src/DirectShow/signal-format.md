---
description: Format de signal
ms.assetid: 8684972c-3233-49bf-8c34-ca644aca432a
title: Format de signal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb6983328729e0dc72d93c0e00a74e7e65a7f237
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127324904"
---
# <a name="signal-format"></a>Format de signal

Le format de signal d’un caméscope DV peut être NTSC ou PAL, standard ou long Play.

**Pilote MSDV**

Pour récupérer le format du signal d’entrée à partir du pilote MSDV, appelez la méthode [**IAMExtTransport :: GetTransportBasicParameters**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-gettransportbasicparameters) et transmettez l' \_ indicateur de \_ signal d’entrée de base Ed \_ . La méthode retourne une constante définie, indiquant le format.

Le code suivant vérifie le format de signal et utilise cette valeur pour calculer le temps moyen par frame. Le mode variable reçoit la constante de format de signal.


```C++
LONG Mode, AvgTimePerFrame;
hr = MyDevCap.pTransport->GetTransportBasicParameters(
        ED_TRANSBASIC_INPUT_SIGNAL, &Mode, NULL);
if (SUCCEEDED(hr))
{
    switch (Mode)
    {
    case ED_TRANSBASIC_SIGNAL_525_60_SD: // NTSC SD
        AvgTimePerFrame = 33;  // 33 msec (29.97 FPS)
        break;
    case ED_TRANSBASIC_SIGNAL_525_60_SDL: // NTSC SDL
        AvgTimePerFrame = 33;  
        break;
    case ED_TRANSBASIC_SIGNAL_625_50_SD: // PAL SD
        AvgTimePerFrame = 40;  // 40 msec (25 FPS)
        break;
    case ED_TRANSBASIC_SIGNAL_625_50_SDL: // PAL SDL
        AvgTimePerFrame = 40;  
        break;
    default: 
        // Unknown type
        AvgTimePerFrame = 33; // Default
        break;
    }
}
```



Pour connaître le format de signal de sortie, appelez la même méthode avec l' \_ indicateur de signal de sortie de base Ed \_ \_ .

**Pilote UVC**

Pour récupérer le format du signal d’entrée ou de sortie à partir du pilote UVC, appelez [**IAMStreamConfig :: GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) sur le code confidentiel et examinez le bloc de format vidéo. (Pour les appareils UVC, le code affiché dans l’exemple précédent retourne généralement ED \_ \_Signal de transbasic \_ inconnu. il n’est donc pas fiable.)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Contrôle d’un caméscope DV](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



