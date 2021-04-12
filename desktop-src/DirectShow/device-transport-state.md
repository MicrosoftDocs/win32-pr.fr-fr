---
description: État du transport de l’appareil
ms.assetid: 15edded0-207c-41e8-81fe-deb6335045eb
title: État du transport de l’appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05f52ea846c79be6cb2d011b635da358f7ecd0a2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392895"
---
# <a name="device-transport-state"></a>État du transport de l’appareil

Pour récupérer l’état actuel de l’appareil, par exemple lire, suspendre ou arrêter, appelez la méthode [**IAMExtTransport :: obtenir le \_ mode**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-get_mode) . La méthode récupère une constante qui indique l’état de l’appareil :



| Valeur                    | État de l’appareil |
|--------------------------|--------------|
| \_lecture en mode Ed \_           | Lire         |
| \_arrêt en mode Ed \_           | Arrêter         |
| \_gel en mode Ed \_         | Suspendre        |
| \_mode Ed \_ FF             | Avance rapide |
| \_rembob en mode Ed \_            | Rembobiner       |
| \_enregistrement en mode Ed \_         | Enregistrement       |
| \_blocage d' \_ enregistrement en mode Ed \_ | Enregistrement-pause |



 

Le code suivant vérifie l’état de l’appareil :


```C++
LONG State;
hr = MyDevCap.pTransport->get_Mode(&State);
if (SUCCEEDED(hr))
{
    switch (State)
    {
        case ED_MODE_PLAY:
        // ... 
    }
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Contrôle d’un caméscope DV](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



