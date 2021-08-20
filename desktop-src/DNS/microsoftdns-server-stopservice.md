---
title: Méthode StopService de la classe MicrosoftDNS_Server
description: La méthode StopService arrête le serveur DNS.
ms.assetid: 80637d5b-e43a-4710-b3ab-eec246587788
keywords:
- Méthode StopService DNS
- Méthode StopService DNS, classe MicrosoftDNS_Server
- Classe MicrosoftDNS_Server DNS, méthode StopService
topic_type:
- apiref
api_name:
- MicrosoftDNS_Server.StopService
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d42a443e22d382dd6e7f6ec9d528d0a1f57c6062ba0e03742033c494b75cd8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076743"
---
# <a name="stopservice-method-of-the-microsoftdns_server-class"></a>Méthode StopService de la \_ classe de serveur MicrosoftDNS

La méthode **StopService** arrête le serveur DNS.

## <a name="syntax"></a>Syntaxe


```mof
uint32 StopService();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

ERREUR \_ : la réussite indique que le service a été arrêté avec succès. Toute autre valeur est un code d’erreur.

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

[**Méthode StartService de la \_ classe de serveur MicrosoftDNS**](microsoftdns-server-startservice.md)
</dt> <dt>

[**Méthode StartScavenging de la \_ classe de serveur MicrosoftDNS**](microsoftdns-server-startscavenging.md)
</dt> <dt>

[**Méthode GetDistinguishedName de la \_ classe de serveur MicrosoftDNS**](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





