---
description: Spécifie la méthode utilisée pour encoder les informations de vecteur de mouvement.
ms.assetid: 22ffdb77-9266-42e5-be41-fc7457141bba
title: MFPKEY_DELTAMVRANGEINDEX, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c72d923659e64c9a0dcab40811e31d7752924700
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528677"
---
# <a name="mfpkey_deltamvrangeindex-property"></a>MFPKEY \_ propriété DELTAMVRANGEINDEX

Spécifie la méthode utilisée pour encoder les informations de vecteur de mouvement.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMVCDeltaMVRangeIndex g

## <a name="data-type"></a>Type de données

VT \_

## <a name="default-value"></a>Valeur par défaut

0

## <a name="remarks"></a>Notes

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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




