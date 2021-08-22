---
description: La classe est la classe de base abstraite pour les classes utilisées pour déterminer quand WMI doit libérer un objet COM (Component Object Model).
ms.assetid: 32631610-8c0e-4f04-b0b2-62e5f8e23ef4
ms.tgt_platform: multiple
title: Classe __CacheControl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __CacheControl
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 429e973d83e1f213b011998c75dfbfabd81fb7bb4921f0f8b9f61bcedd6080c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051097"
---
# <a name="__cachecontrol-class"></a>\_\_CacheControl, classe

La classe système **\_ \_ CacheControl** est la classe de base abstraite pour les classes utilisées pour déterminer quand WMI doit libérer un objet COM (Component Object Model). Les instances de cette classe ne sont jamais créées. La classe **\_ \_ CacheControl** se trouve uniquement dans l’espace de noms racine. Pour plus d’informations sur l’utilisation de cette classe, consultez [déchargement d’un fournisseur](unloading-a-provider.md).

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[abstract]
class __CacheControl : __SystemClass
{
};
```

## <a name="members"></a>Membres

La classe **\_ \_ CacheControl** ne définit aucun membre.

## <a name="remarks"></a>Remarques

La classe **\_ \_ CacheControl** est dérivée de [**\_ \_ SystemClass**](--systemclass.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |
| Espace de noms<br/>                | Tous les espaces de noms WMI<br/>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_\_SystemClass**](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[Classes système WMI](wmi-system-classes.md)
</dt> <dt>

[**\_\_EventConsumerProviderCacheControl**](--eventconsumerprovidercachecontrol.md)
</dt> <dt>

[**\_\_EventProviderCacheControl**](--eventprovidercachecontrol.md)
</dt> <dt>

[**\_\_EventSinkCacheControl**](--eventsinkcachecontrol.md)
</dt> <dt>

[**\_\_ObjectProviderCacheControl**](--objectprovidercachecontrol.md)
</dt> <dt>

[\_\_PropertyProviderCacheControl](--propertyprovidercachecontrol.md)
</dt> <dt>

[Déchargement d’un fournisseur](unloading-a-provider.md)
</dt> </dl>

 

