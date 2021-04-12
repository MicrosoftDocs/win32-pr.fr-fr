---
description: Spécifie la plage utilisée dans les recherches de mouvement.
ms.assetid: b2026f47-ac39-4276-8359-c939b202f00c
title: MFPKEY_MOTIONSEARCHRANGE, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c557ea1a462192434222e425dccb8b9a0e291986
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202347"
---
# <a name="mfpkey_motionsearchrange-property"></a>MFPKEY \_ propriété MOTIONSEARCHRANGE

Spécifie la plage utilisée dans les recherches de mouvement.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMVCMotionSearchRange g

## <a name="data-type"></a>Type de données

VT \_

## <a name="default-value"></a>Valeur par défaut

0

## <a name="remarks"></a>Notes

Cette propriété peut être définie sur l’une des valeurs suivantes. H indique une plage horizontale et une plage verticale. Toutes les plages sont indiquées en pixels.



| Valeur | Plage                                |
|-------|--------------------------------------|
| 0     | + 63.75/-64 H, + 31.75/-32.0 V       |
| 1     | + 127.75/-128.0 H, + 63.75/-64 V     |
| 2     | +511,75/-512,0 H, +127,75/-128,0 V   |
| 3     | + 1023.75/-1024.0 H, + 255.75/-256.0 V |
| -1    | Bloc macro-adaptative (automatique)      |



 

Cette propriété contrôle la taille de la zone Frame dans laquelle le codec recherchera un élément pouvant avoir un mouvement entre les frames. Une plus grande fenêtre de recherche permet de trouver un mouvement plus rapide, mais elle nécessite plus de temps processeur. Les exigences de l’UC sont approximativement doublées à chaque niveau.

Le mode automatique (-1) sélectionne dynamiquement le mode le plus efficace.

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

 

 




