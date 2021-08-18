---
description: PNRP utilise la structure WSAQUERYSET conjointement avec diverses fonctions pour faciliter la résolution des noms et l’énumération des noms et des clouds.
ms.assetid: 0ccf20c1-4c95-4caf-a8f3-82a9e0a9907b
title: PNRP et WSAQUERYSET (P2P. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bbc635b0c1ca19cfaeeeb7f8b013aefad1e49e2141dd9715a36c0238e7be6f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061356"
---
# <a name="pnrp-and-wsaqueryset"></a>PNRP et WSAQUERYSET

PNRP utilise la structure [**WSAQUERYSET**](winsock-nsp-reference-links.md) conjointement avec diverses fonctions pour faciliter la résolution des noms et l’énumération des noms et des clouds.

pour obtenir la définition complète des fonctions de sockets [**WSAQUERYSET**](winsock-nsp-reference-links.md) ou Windows, consultez leurs définitions respectives dans la documentation de l’API Windows sockets 2 dans le kit de développement platform SDK.

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
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                             |
| Version<br/>                  | Windows xp avec SP1 avec le Pack de mise en réseau avancée pour Windows XP<br/>  |
| En-tête<br/>                   | <dl> <dt>P2P. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[PNRP et objet BLOB](pnrp-and-blob.md)
</dt> <dt>

[PNRP et WSASetService](pnrp-and-wsasetservice.md)
</dt> </dl>

 

 




