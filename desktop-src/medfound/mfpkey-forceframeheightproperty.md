---
description: Spécifie une hauteur de frame intermédiaire pour la vidéo encodée.
ms.assetid: 7382ec31-6d59-4e8c-94eb-804786074038
title: MFPKEY_FORCEFRAMEHEIGHT, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8e4662ce56ea4c20d44abdd05641219bc6b94ee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127227478"
---
# <a name="mfpkey_forceframeheight-property"></a>MFPKEY \_ propriété FORCEFRAMEHEIGHT

Spécifie une hauteur de frame intermédiaire pour la vidéo encodée.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMVCForceFrameHeight g

## <a name="data-type"></a>Type de données

VT \_

## <a name="remarks"></a>Notes

Vous pouvez définir cette valeur et la propriété [MFPKEY \_ FORCEFRAMEWIDTH](mfpkey-forceframewidthproperty.md) pour forcer l’encodeur à encoder le flux vidéo avec une taille de frame inférieure aux tailles d’entrée ou de sortie. En cas de décodage, la vidéo est redimensionnée à sa résolution d’entrée d’origine.

Les dimensions de frame valides sur l’un des axes sont commodes de 2 à 8192 pixels. Les dimensions du frame doivent être divisibles par 2.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




