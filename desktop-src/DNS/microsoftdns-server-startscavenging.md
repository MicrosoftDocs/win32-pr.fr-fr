---
title: Méthode StartScavenging de la classe MicrosoftDNS_Server
description: La méthode StartScavenging démarre le nettoyage des enregistrements obsolètes dans les zones soumises au nettoyage.
ms.assetid: ee1bc0e0-9334-4971-a524-4bb8a9015b5b
keywords:
- Méthode StartScavenging DNS
- Méthode StartScavenging DNS, classe MicrosoftDNS_Server
- MicrosoftDNS_Server de la classe DNS, méthode StartScavenging
topic_type:
- apiref
api_name:
- MicrosoftDNS_Server.StartScavenging
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6173021ca49dc73b7ec89f60b097b2179078a774c9a40c26fda2c41b2ad25f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874769"
---
# <a name="startscavenging-method-of-the-microsoftdns_server-class"></a>Méthode StartScavenging de la \_ classe de serveur MicrosoftDNS

La méthode **StartScavenging** démarre le nettoyage des enregistrements obsolètes dans les zones soumises au nettoyage.

## <a name="syntax"></a>Syntaxe


```mof
uint32 StartScavenging();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

ERREUR \_ : la réussite indique que le nettoyage a été correctement démarré. Toute autre valeur est un code d’erreur.

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

[**Méthode StopService de la \_ classe de serveur MicrosoftDNS**](microsoftdns-server-stopservice.md)
</dt> <dt>

[**Méthode GetDistinguishedName de la \_ classe de serveur MicrosoftDNS**](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





