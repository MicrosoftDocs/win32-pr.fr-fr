---
description: La liste suivante contient les méthodes internes d’adresse CMSP.
ms.assetid: 2016a776-1464-46b5-96b9-b045834f9e38
title: Méthodes d’assistance interne CMSPAddress
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec703a6f01052675cfa8f086364b56b38d5c34010107d92866bb8409454c362a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117947556"
---
# <a name="cmspaddress-internal-helper-methods"></a>Méthodes d’assistance interne CMSPAddress



| Méthodes d’assistance interne CMSPAddress                                        | Description                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetStaticTerminals**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getstaticterminals)               | Appelée par [**\_ StaticTerminals**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_staticterminals) et [**EnumerateStaticTerminals**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratestaticterminals) pour récupérer un tableau de terminaux statiques qui peuvent être utilisés sur cette adresse.                                     |
| [**GetDynamicTerminalClasses**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getdynamicterminalclasses) | Appelée par [**\_ DynamicTerminalClasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_dynamicterminalclasses) et [**EnumerateDynamicTerminalClasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratedynamicterminalclasses) pour récupérer un tableau de classes de terminaux dynamiques qui peuvent être utilisées sur cette adresse. |
| [**UpdateTerminalList**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-updateterminallist)               | Remplit la liste des terminaux statiques du MSP.                                                                                                                                                                                                                                |
| [**ReceiveTSPAddressData**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-receivetspaddressdata)         | Appelé lorsqu’un message de données TSP est destiné à être traité par l’adresse plutôt que par un appel spécifique.                                                                                                                                                                    |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**CMSPAddress**](/windows/desktop/api/Mspaddr/nl-mspaddr-cmspaddress)
</dt> </dl>

 

 
