---
description: Spécifie une largeur de frame intermédiaire pour la vidéo encodée.
ms.assetid: 805bd587-31af-49b8-b5ab-2dcf2a3f81c5
title: MFPKEY_FORCEFRAMEWIDTH, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8d04e30f5fd5d2ecc7055553e17eaf86199b62be8d3dd861b9f82246947212f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939833"
---
# <a name="mfpkey_forceframewidth-property"></a>MFPKEY \_ propriété FORCEFRAMEWIDTH

Spécifie une largeur de frame intermédiaire pour la vidéo encodée.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMVCForceFrameWidth g

## <a name="data-type"></a>Type de données

VT \_

## <a name="remarks"></a>Remarques

Vous pouvez définir cette valeur et la propriété [MFPKEY \_ FORCEFRAMEHEIGHT](mfpkey-forceframeheightproperty.md) pour forcer l’encodeur à encoder le flux vidéo avec une taille de frame inférieure aux tailles d’entrée ou de sortie. En cas de décodage, la vidéo est redimensionnée à sa résolution d’entrée d’origine.

Les dimensions de frame valides sur l’un des axes sont commodes de 2 à 8192 pixels. Les dimensions du frame doivent être divisibles par 2.

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

 

 




