---
description: Contrôle le cache lorsqu’un fournisseur de propriétés est déchargé.
ms.assetid: 8fc7de7a-889c-4d53-97ea-a676879de1d3
ms.tgt_platform: multiple
title: Classe __PropertyProviderCacheControl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __PropertyProviderCacheControl
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 1d153049a9635b4b77a1ad09ca0ee64835b9bcfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203162"
---
# <a name="__propertyprovidercachecontrol-class"></a>\_\_PropertyProviderCacheControl, classe

La classe **\_ \_ PropertyProviderCacheControl** contrôle le cache lorsqu’un fournisseur de propriétés est déchargé. Cette classe existe uniquement dans l' \\ espace de noms racine.

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class __PropertyProviderCacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a>Membres

La classe **\_ \_ PropertyProviderCacheControl** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **\_ \_ PropertyProviderCacheControl** possède les propriétés suivantes.

<dl> <dt>

**ClearAfter**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Intervalle de temps après la libération par WMI d’un fournisseur de propriétés. L’heure est au format intervalle.

</dd> </dl>

## <a name="remarks"></a>Notes

La classe **\_ \_ PropertyProviderCacheControl** est dérivée de [**\_ \_ CacheControl**](--cachecontrol.md). Pour plus d’informations, consultez [déchargement d’un fournisseur](unloading-a-provider.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |
| Espace de noms<br/>                | Tous les espaces de noms WMI<br/>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Classes système WMI](wmi-system-classes.md)
</dt> </dl>

 

 




