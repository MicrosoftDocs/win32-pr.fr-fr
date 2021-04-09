---
title: CounterItem. Width, propriété
description: Récupère ou définit la largeur de ligne utilisée pour représenter sous forme de graphique la valeur de compteur.
ms.assetid: 1f5c1e74-18d4-4005-b83f-bf7265d356cb
keywords:
- Propriété Width SysMon
- Propriété Width SysMon, classe CounterItem
- Classe CounterItem SysMon, propriété Width
topic_type:
- apiref
api_name:
- CounterItem.Width
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e67892f9e4cf6799f1b9311bb2cd47ec02744cb6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741788"
---
# <a name="counteritemwidth-property"></a>CounterItem. Width, propriété

Récupère ou définit la largeur de ligne utilisée pour représenter sous forme de graphique la valeur de compteur.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
Property Width As Long
```



## <a name="property-value"></a>Valeur de la propriété

Largeur de ligne utilisée dans un graphique linéaire. Les valeurs valides sont comprises entre 1 et 3, où 1 (la valeur par défaut) est la largeur la plus étroite.

**Avant Windows Vista :** Les valeurs valides sont comprises entre 1 et 9. N’utilisez pas une valeur de largeur supérieure à 3 Si votre application est exécutée sur Windows Vista.

## <a name="exceptions"></a>Exceptions



| Type d'exception               | Condition                              |
|------------------------------|----------------------------------------|
| **System.ArgumentException** | La largeur de ligne spécifiée n’est pas valide. |



 

## <a name="remarks"></a>Notes

La largeur de ligne par défaut pour les seize premiers compteurs que vous ajoutez est 1. La largeur de ligne par défaut pour les seize compteurs suivants (compteurs 17-32) que vous ajoutez est 2. La largeur de ligne par défaut pour les seize compteurs suivants (compteurs 33-48) que vous ajoutez est 3. Après cela, SYSMON choisit de façon aléatoire la largeur de ligne. Pour plus d’informations, consultez [**CounterItem. Color**](counteritem-color.md).

Pour spécifier un [**style de ligne**](counteritem-linestyle.md) autre que Solid, la largeur doit être 1. Si vous spécifiez une valeur supérieure à 1 et spécifiez un style de ligne non plein, SYSMON ignore la largeur de ligne spécifiée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                            |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CounterItem**](counteritem.md)
</dt> </dl>

 

 





