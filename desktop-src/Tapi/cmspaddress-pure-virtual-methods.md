---
description: Méthodes virtuelles pures CMSPAddress-ces méthodes doivent être substituées par des classes dérivées.
ms.assetid: 68402cff-effd-4a2b-b9f9-f13f233b1555
title: CMSPAddress des méthodes virtuelles pures
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c9d9b9494e4ee42972d97433927fd587034af81
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084207"
---
# <a name="cmspaddress-pure-virtual-methods"></a>CMSPAddress des méthodes virtuelles pures

Ces méthodes doivent être remplacées par des classes dérivées.



| CMSPAddress des méthodes virtuelles pures                           | Description                                                                                                                                                                            |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MSPAddressAddRef**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressaddref)   | La méthode private AddRef pour l’adresse.                                                                                                                                                 |
| [**MSPAddressRelease**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressrelease) | Méthode de mise en sortie privée pour l’adresse.                                                                                                                                                |
| [**CreateMSPCall**](/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall)        | Appelé par l’interface TAPI pour créer un objet d’appel. L’implémentation dans la classe dérivée doit simplement appeler la fonction [**CreateMSPCallHelper**](/windows/desktop/api/Mspaddr/nf-mspaddr-createmspcallhelper) .        |
| [**ShutdownMSPCall**](/windows/desktop/api/msp/nf-msp-itmspaddress-shutdownmspcall)    | Appelé par l’interface TAPI pour arrêter un objet d’appel. L’implémentation dans la classe dérivée doit simplement appeler la fonction [**ShutdownMSPCallHelper**](/windows/desktop/api/Mspaddr/nf-mspaddr-shutdownmspcallhelper) . |
| [**GetCallMediaTypes**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getcallmediatypes) | Obtient les types de médias pris en charge par le MSP.                                                                                                                                                 |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**CMSPAddress**](/windows/desktop/api/Mspaddr/nl-mspaddr-cmspaddress)
</dt> </dl>

 

 



