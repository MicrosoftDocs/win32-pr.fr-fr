---
title: Classe MicrosoftDNS_Cache
description: La \_ classe de cache MicrosoftDNS décrit un cache existant sur un serveur DNS.
ms.assetid: 139406eb-70f2-4614-9662-703ada032298
keywords:
- MicrosoftDNS_Cache de la classe DNS
- MicrosoftDNS_Cache de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_Cache
- MicrosoftDNS_Cache.ClearCache
- MicrosoftDNS_Cache.GetDistinguishedName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03728a82f7668e38e43c92e3edacff1717333c6b073ee3491389723fb63b5f7f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077069"
---
# <a name="microsoftdns_cache-class"></a>\_Classe de cache MicrosoftDNS

La classe de **\_ cache MicrosoftDNS** décrit un cache existant sur un serveur DNS. Cette classe simplifie la visualisation de la relation contenant-contenu des objets DNS, plutôt que la représentation d’un objet réel. La classe de **\_ cache MicrosoftDNS** est un conteneur pour les enregistrements de ressource mis en cache par le serveur DNS. Ne confondez pas cela avec un fichier cache qui contient des indications de racine.

Chaque instance du **\_ cache** de la classe MicrosoftDNS doit être affectée à un seul serveur DNS. Il peut être associé à plusieurs instances de classes [**MicrosoftDNS \_ Domain**](microsoftdns-domain.md) ou [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) .

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class MicrosoftDNS_Cache : MicrosoftDNS_Domain
{
};
```

## <a name="members"></a>Membres

La classe de **\_ cache MicrosoftDNS** possède les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

La classe de **\_ cache MicrosoftDNS** possède ces méthodes.



| Méthode                   | Description                                                                                     |
|:-------------------------|:------------------------------------------------------------------------------------------------|
| **ClearCache**           | Efface le cache du serveur DNS des enregistrements de ressources. <br/> Qualificateurs : implémentés<br/> |
| **GetDistinguishedName** | Récupère le nom unique de la zone. <br/> Qualificateurs : implémentés<br/>   |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| Espace de noms<br/>                | \\MicrosoftDNS racine<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. mof</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Domaine MicrosoftDNS**](microsoftdns-domain.md)
</dt> <dt>

[**Méthode ClearCache de la \_ classe de cache MicrosoftDNS**](microsoftdns-cache-clearcache.md)
</dt> <dt>

[**Méthode GetDistinguishedName de la \_ classe de cache MicrosoftDNS**](microsoftdns-cache-getdistinguishedname.md)
</dt> </dl>

 

 





