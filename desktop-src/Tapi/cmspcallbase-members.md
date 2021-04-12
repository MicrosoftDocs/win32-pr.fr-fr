---
description: La liste suivante contient les membres CMSPCAllBase.
ms.assetid: a3193639-e0c4-4851-a879-551eca8023f9
title: Membres CMSPCallBase
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8ddae67d85a64a5a443727b3950054957c7f24f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203022"
---
# <a name="cmspcallbase-members"></a>Membres CMSPCallBase



| Type de membre                   | Nom             | Description                                                                                                                                                                                                                                                                                                                                       |
|-------------------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IUnknown                      | \*m \_ pFTM        | Pointeur vers le marshaleur libre de threads.                                                                                                                                                                                                                                                                                                          |
| CMSPAddress\*                 | \*m \_ pMSPAddress | Pointeur vers l’objet d’adresse MSP. Il est utilisé pour récupérer les terminaux par défaut si l’application ne la sélectionne pas. Il comporte également un refcount (via [**MSPAddressAddRef**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressaddref), et non AddRef) afin que l’adresse agrégée ne disparaissent pas pendant que l’appel est toujours actif, mais que l’adresse de l’interface TAPI 3 n’est pas AddRef’ed. |
| \_handle MSP                   | \*m \_ htCall      | Handle de l’appel de TAPI3's. Utilisé pour déclencher des événements d’appel.                                                                                                                                                                                                                                                                                             |
| DWORD                         | m \_ dwMediaType   | Masque de rébinaire des types de média sur cet appel.                                                                                                                                                                                                                                                                                                          |
| CMSPArray <ITStream \*> | \_flux m       | Liste des objets de flux dans l’appel.                                                                                                                                                                                                                                                                                                           |
| CMSPCritSection               | \_verrou m          | Verrou qui protège les listes de flux.                                                                                                                                                                                                                                                                                                          |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**CMSPCallBase**](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallbase)
</dt> </dl>

 

 



