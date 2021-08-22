---
title: Méthode StartService de la classe MicrosoftDNS_Server
description: La méthode StartService démarre le serveur DNS.
ms.assetid: f6343a34-9d1b-4f82-897e-289650af6be9
keywords:
- Méthode StartService DNS
- Méthode StartService DNS, classe MicrosoftDNS_Server
- MicrosoftDNS_Server de la classe DNS, StartService, méthode
topic_type:
- apiref
api_name:
- MicrosoftDNS_Server.StartService
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5e74de96ad24ff16ea2c2effaef78003011f5d6bd5d421336084ac5c7701f79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119432639"
---
# <a name="startservice-method-of-the-microsoftdns_server-class"></a>Méthode StartService de la \_ classe de serveur MicrosoftDNS

La méthode **StartService** démarre le serveur DNS.

## <a name="syntax"></a>Syntaxe


```mof
uint32 StartService();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

ERREUR \_ : la réussite indique que le service a été correctement démarré. Toute autre valeur est un code d’erreur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| Espace de noms<br/>                | \\MicrosoftDNS racine<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. mof</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Serveur MicrosoftDNS**](microsoftdns-server.md)
</dt> <dt>

[**Méthode StopService de la \_ classe de serveur MicrosoftDNS**](microsoftdns-server-stopservice.md)
</dt> <dt>

[**Méthode StartScavenging de la \_ classe de serveur MicrosoftDNS**](microsoftdns-server-startscavenging.md)
</dt> <dt>

[**Méthode GetDistinguishedName de la \_ classe de serveur MicrosoftDNS**](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





