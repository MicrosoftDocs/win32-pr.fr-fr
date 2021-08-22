---
description: Contrôle quand une classe ou un fournisseur d’instance est déchargé.
ms.assetid: 4cbeb820-8a65-4fab-97f1-2a973b2a4310
ms.tgt_platform: multiple
title: Classe __ObjectProviderCacheControl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ObjectProviderCacheControl
- Root.__ObjectProviderCacheControl.ClearAfter
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: a4711f13afde50d512c3a7e210a0853ef9cc7606be096d95f86b144684a5add6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118820689"
---
# <a name="__objectprovidercachecontrol-class"></a>\_\_ObjectProviderCacheControl, classe

La classe système **\_ \_ ObjectProviderCacheControl** contrôle quand une classe ou un fournisseur d’instance est déchargé. Il se trouve uniquement dans l' \\ espace de noms racine.

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[singleton]
class __ObjectProviderCacheControl : __CacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a>Membres

La classe **\_ \_ ObjectProviderCacheControl** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **\_ \_ ObjectProviderCacheControl** possède les propriétés suivantes.

<dl> <dt>

**ClearAfter**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Intervalle de temps après lequel WMI libère une instance, une classe ou un fournisseur de méthode. L’heure est au [format d’intervalle](interval-format.md).

</dd> </dl>

## <a name="remarks"></a>Remarques

La classe **\_ \_ ObjectProviderCacheControl** est dérivée de [**\_ \_ CacheControl**](--cachecontrol.md). Pour plus d’informations sur l’utilisation de cette classe, consultez [déchargement d’un fournisseur](unloading-a-provider.md).

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |
| Espace de noms<br/>                | Root<br/>                |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_\_CacheControl**](/windows/desktop/WmiSdk/--cachecontrol)
</dt> <dt>

[Classes système WMI](wmi-system-classes.md)
</dt> <dt>

[Réception d’événements à tout moment](receiving-events-at-all-times.md)
</dt> </dl>

 

