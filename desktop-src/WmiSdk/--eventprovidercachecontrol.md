---
description: Contrôle le moment où un fournisseur d’événements est déchargé.
ms.assetid: 7f11e521-d0f6-4c3c-8bfe-ceed2d106ed3
ms.tgt_platform: multiple
title: Classe __EventProviderCacheControl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventProviderCacheControl
- Root.__EventProviderCacheControl.ClearAfter
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: c54ec47b1f67d96816cf24a6b6e0108ee0b1de70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203742"
---
# <a name="__eventprovidercachecontrol-class"></a>\_\_EventProviderCacheControl, classe

La classe système **\_ \_ EventProviderCacheControl** contrôle le moment où un fournisseur d’événements est déchargé. Il se trouve uniquement dans l' \\ espace de noms racine.

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[singleton]
class __EventProviderCacheControl : __CacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a>Membres

La classe **\_ \_ EventProviderCacheControl** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **\_ \_ EventProviderCacheControl** possède les propriétés suivantes.

<dl> <dt>

**ClearAfter**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Intervalle de temps après lequel Windows Management Instrumentation (WMI) libère un fournisseur d’événements. L’heure est au [format d’intervalle](interval-format.md). Le déchargement du fournisseur peut prendre jusqu’à deux fois l’intervalle spécifié.

</dd> </dl>

## <a name="remarks"></a>Notes

La classe **\_ \_ EventProviderCacheControl** est dérivée de [**\_ \_ CacheControl**](--cachecontrol.md).

Pour plus d’informations sur l’utilisation de cette classe, consultez [déchargement d’un fournisseur](unloading-a-provider.md).

## <a name="requirements"></a>Configuration requise



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
</dt> </dl>

 

