---
description: Spécifie comment les informations de couleur sont utilisées dans les opérations de recherche de mouvement.
ms.assetid: a625b103-0a55-4268-a01a-6a464a56fec2
title: MFPKEY_MOTIONSEARCHLEVEL, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b53c6bf8f94b2b9817249d96cffbfa0da251dbbcb0545c141230de90f80485af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555409"
---
# <a name="mfpkey_motionsearchlevel-property"></a>MFPKEY \_ propriété MOTIONSEARCHLEVEL

Spécifie comment les informations de couleur sont utilisées dans les opérations de recherche de mouvement.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMVCMotionSearchLevel g

## <a name="data-type"></a>Type de données

VT \_

## <a name="default-value"></a>Valeur par défaut

0

## <a name="remarks"></a>Remarques

Cette propriété peut être définie sur l’une des valeurs suivantes.



| Valeur | Informations vidéo utilisées                           |
|-------|--------------------------------------------------|
| 0     | Luminance uniquement.                                       |
| 1     | Luminance avec Chroma entier le plus proche.                |
| 2     | Luminance avec chroma vrai.                           |
| -1    | Bloc macro-adaptative avec vrai Chroma.            |
| -2    | Bloc macro-adaptative avec Chroma d’entier le plus proche. |



 

Par défaut, le codec effectue une recherche de mouvement uniquement dans le canal de luminance. L’inclusion d’informations Chroma dans l’estimation de mouvement peut améliorer considérablement la qualité de la vidéo encodée. La recherche de mouvement avec la luminance et la chrominance réelle produira la meilleure qualité vidéo, mais à un coût de performances optimal. Les deux modes dynamiques (-1 et-2) et la luminance avec le mode Chroma entier le plus proche fournissent des compromis raisonnables entre qualité et performances.

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

 

 




