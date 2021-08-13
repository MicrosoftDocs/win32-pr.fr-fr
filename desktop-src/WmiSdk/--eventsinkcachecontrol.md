---
description: Utilisé pour déterminer à quel moment WMI libère un pointeur IWbemUnboundObjectSink des fournisseurs de consommateur d’événements.
ms.assetid: f7b14efc-a2f7-4e99-8ec8-5b5af0743139
ms.tgt_platform: multiple
title: Classe __EventSinkCacheControl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventSinkCacheControl
- Root.__EventSinkCacheControl.ClearAfter
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: dc73e2cb740486ad08172c10233f4865709a87d9f1122f399002133687744094
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118557913"
---
# <a name="__eventsinkcachecontrol-class"></a>\_\_EventSinkCacheControl, classe

La classe système **\_ \_ EventSinkCacheControl** permet de déterminer à quel moment WMI libère le pointeur [**IWbemUnboundObjectSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) d’un fournisseur de consommateur d’événements. La classe **\_ \_ EventSinkCacheControl** est une classe singleton. Il se trouve uniquement dans l' \\ espace de noms racine.

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[singleton]
class __EventSinkCacheControl : CacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a>Membres

La classe **\_ \_ EventSinkCacheControl** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **\_ \_ EventSinkCacheControl** possède les propriétés suivantes.

<dl> <dt>

**ClearAfter**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Intervalle de temps après lequel WMI libère un fournisseur d’événements. Le déchargement du fournisseur peut prendre jusqu’à deux fois l’intervalle spécifié. L’heure est au [format d’intervalle](interval-format.md).

</dd> </dl>

## <a name="remarks"></a>Remarques

La classe **\_ \_ EventSinkCacheControl** est dérivée de [**\_ \_ CacheControl**](--cachecontrol.md). Pour plus d’informations sur l’utilisation de cette classe, consultez [déchargement d’un fournisseur](unloading-a-provider.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |
| Espace de noms<br/>                | Root<br/>                |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Classes système WMI](wmi-system-classes.md)
</dt> </dl>

 

 




