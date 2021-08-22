---
description: Définit l’identificateur de l’ensemble de paramètres de séquence (SPS) dans l’unité de couche d’abstraction de réseau (NAL) SPS du flux de bits H. 264.
ms.assetid: 583DD539-6EE8-4DD4-A0FE-D2BBE1A4302F
title: CODECAPI_AVEncH264SPSID, propriété (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da06e431a3747e676e3934ac9a261e1d0e1ec37e18bacf01f8a3e623c4257488
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664659"
---
# <a name="codecapi_avench264spsid-property"></a>CODECAPI \_ propriété AVEncH264SPSID

Définit l’identificateur de l’ensemble de paramètres de séquence (SPS) dans l’unité de couche d’abstraction de réseau (NAL) SPS du flux de bits H. 264.

## <a name="data-type"></a>Type de données

**ULong** (VT \_ UI4)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncH264SPSID**

## <a name="property-value"></a>Valeur de la propriété

Spécifie la valeur de l' **\_ ID du \_ jeu \_ de paramètres SEQ** dans l’unité de SPS nal. L’élément de syntaxe de l’ID de l' **\_ ensemble de paramètres \_ \_ Seq** identifie le jeu de paramètres de séquence. Le flux de bits résultant peut être concaténé avec d’autres flux de bits, afin de produire un flux de bits plus long qui contient plusieurs jeux de paramètres de séquence avec différents identificateurs SPS.

La plage valide est 0 31, comme indiqué dans la spécification H. 264/AVC.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau \| UWP apps\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau \| UWP apps\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

