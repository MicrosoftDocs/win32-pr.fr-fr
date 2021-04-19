---
description: PNRP utilise la structure WSAQUERYSET conjointement avec diverses fonctions pour faciliter la résolution des noms et l’énumération des noms et des clouds.
ms.assetid: 0ccf20c1-4c95-4caf-a8f3-82a9e0a9907b
title: PNRP et WSAQUERYSET (P2P. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d09d135d57af0922feb5a143c41696d85dac083
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518783"
---
# <a name="pnrp-and-wsaqueryset"></a>PNRP et WSAQUERYSET

PNRP utilise la structure [**WSAQUERYSET**](winsock-nsp-reference-links.md) conjointement avec diverses fonctions pour faciliter la résolution des noms et l’énumération des noms et des clouds.

Pour obtenir la définition complète des fonctions [**WSAQUERYSET**](winsock-nsp-reference-links.md) ou Windows Sockets, consultez leurs définitions respectives dans la documentation de l’API Windows Sockets 2 dans le kit de développement Platform SDK.

## <a name="wsaqueryset-and-wsasetservice"></a>WSAQUERYSET et WSASetService

La fonction [**WSASetService**](winsock-nsp-reference-links.md) utilise la structure **WSAQUERYSET** pour inscrire ou supprimer des noms d’homologue. La page [PNRP et WSASetService](pnrp-and-wsasetservice.md) explique comment utiliser la structure **WSAQUERYSET** avec cette fonction.

## <a name="wsaqueryset-and-wsalookupservicebegin"></a>WSAQUERYSET et WSALookupServiceBegin

La structure [**WSAQUERYSET**](winsock-nsp-reference-links.md) est largement utilisée avec les fonctions **WSALookupServiceBegin**, **WSALookupServiceNext** et **WSALookupServiceEnd** . Les détails sur la façon dont ces fonctions utilisent la structure **WSAQUERYSET** sont détaillés dans les pages de référence suivantes :

-   [PNRP et WSALookupServiceBegin](pnrp-and-wsalookupservicebegin.md)
-   [PNRP et WSALookupServiceNext](pnrp-and-wsalookupservicenext.md)
-   [PNRP et WSALookupServiceEnd](pnrp-and-wsalookupserviceend.md)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/>                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                             |
| Version<br/>                  | Windows XP avec SP1 avec le Pack de mise en réseau avancée pour Windows XP<br/>  |
| En-tête<br/>                   | <dl> <dt>P2P. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[PNRP et objet BLOB](pnrp-and-blob.md)
</dt> <dt>

[PNRP et WSASetService](pnrp-and-wsasetservice.md)
</dt> </dl>

 

 




