---
description: Méthodes virtuelles pures CMSPCallBase-ces méthodes doivent être substituées par des classes dérivées.
ms.assetid: 2ea9d35a-c87e-44f4-8dc6-618251c81fe4
title: CMSPCallBase des méthodes virtuelles pures
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8da8530ab3dae737bf1407f00d5d4a415a1437e3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094457"
---
# <a name="cmspcallbase-pure-virtual-methods"></a>CMSPCallBase des méthodes virtuelles pures

Ces méthodes doivent être remplacées par des classes dérivées.



| CMSPCallBase des méthodes virtuelles pures                                 | Description                                                                                                                             |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**MSPCallAddRef**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-mspcalladdref)               | Méthode de AddRef privée pour l’objet d’appel.                                                                                              |
| [**MSPCallRelease**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-mspcallrelease)             | Méthode de mise en sortie privée pour l’objet d’appel.                                                                                             |
| [**Rein**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-init)                                 | Appelée par l’objet d’adresse MSP (dans la méthode [**CreateMSPCall**](/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall)) pour initialiser l’objet d’appel MSP. |
| [**Correct**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-shutdown)                         | Appelé par l’objet d’adresse MSP pour arrêter l’appel..                                                                                |
| [**InternalCreateStream**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-internalcreatestream) | Appelée par [**CreateStream,**](/windows/win32/api/tapi3if/nf-tapi3if-itstreamcontrol-createstream) pour créer un objet de flux.                                               |
| [**CreateStreamObject**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-createstreamobject)     | Appelée par [**InternalCreateStream**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-internalcreatestream) pour créer un objet de flux.                                  |
| [**RemoveStream**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-removestream)                 | Appelé par l’application pour supprimer un flux de l’appel                                                                              |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**CMSPCallBase**](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallbase)
</dt> </dl>

 

 
