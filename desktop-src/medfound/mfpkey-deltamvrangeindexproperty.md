---
description: Spécifie la méthode utilisée pour encoder les informations de vecteur de mouvement.
ms.assetid: 22ffdb77-9266-42e5-be41-fc7457141bba
title: MFPKEY_DELTAMVRANGEINDEX, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7a21ac1a0bdaf859c93bca800d72f5e9ed155919bb07a24f5287b2436e57f94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113339"
---
# <a name="mfpkey_deltamvrangeindex-property"></a>MFPKEY \_ propriété DELTAMVRANGEINDEX

Spécifie la méthode utilisée pour encoder les informations de vecteur de mouvement.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMVCDeltaMVRangeIndex g

## <a name="data-type"></a>Type de données

VT \_

## <a name="default-value"></a>Valeur par défaut

0

## <a name="remarks"></a>Remarques

Si cette propriété est définie, l’encodeur augmente la plage du vecteur de mouvement Delta dans les champs. Les informations de vecteur de mouvement ne sont valides que pour les champs entrelacés.

Cette propriété peut être définie sur l’une des valeurs suivantes :



| Valeur | Description                                                                          |
|-------|--------------------------------------------------------------------------------------|
| 0     | Utilisez la plage de vecteurs de mouvement Delta existante.                                          |
| 1     | Doublez la plage du vecteur de mouvement Delta dans le sens horizontal.                    |
| 2     | Doublez la plage du vecteur de mouvement Delta dans le sens vertical.                      |
| 3     | Doublez la plage du vecteur de mouvement Delta dans les directions horizontale et verticale. |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




