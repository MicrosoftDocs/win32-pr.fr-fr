---
description: Ces méthodes doivent être remplacées par des classes dérivées.
ms.assetid: 68402cff-effd-4a2b-b9f9-f13f233b1555
title: CMSPAddress des méthodes virtuelles pures
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a93c9b2a995554dd2f7412c8fa5bf153ea8871e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518712"
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

 

 



