---
description: La propriété ConfigurableItems en lecture seule de l’objet Merge retourne une collection ConfigurableItem objets, chacun représentant une ligne unique de la table ModuleConfiguration.
ms.assetid: 4d1a64f7-fbd0-4358-8911-112e43f1be4a
title: Merge.Configpropriété urableItems (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.ConfigurableItems
- IMsmMerge.get_ConfigurableItems
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 179594ba7fe7691edb9abe1f72d104742fe9bc9e3a4a23b728ad8607b94c444a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013037"
---
# <a name="mergeconfigurableitems-property"></a>Merge.Configpropriété urableItems

La propriété **ConfigurableItems** en lecture seule de l’objet [**Merge**](merge-object.md) retourne une collection [**ConfigurableItem**](configurableitem-object.md) objets, chacun représentant une ligne unique de la [table ModuleConfiguration](moduleconfiguration-table.md). Sémantiquement, chaque interface de l’énumérateur représente un élément qui peut être configuré par le consommateur de module. La collection est une collection en lecture seule et implémente les interfaces de collection en lecture seule standard de Item (), Count () et \_ NewEnum (). L’énumérateur **IEnumMsmConfigItems** implémente Next (), Skip (), Reset () et Clone () avec la sémantique standard.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Merge.ConfigurableItems
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="c"></a>C++

Consultez la fonction [**obtenir \_ ConfigurableItems**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-get_configurableitems) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 2,0 ou version ultérieure<br/>                                                    |
| En-tête<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




