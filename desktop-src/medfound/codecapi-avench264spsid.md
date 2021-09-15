---
description: Définit l’identificateur de l’ensemble de paramètres de séquence (SPS) dans l’unité de couche d’abstraction de réseau (NAL) SPS du flux de bits H. 264.
ms.assetid: 583DD539-6EE8-4DD4-A0FE-D2BBE1A4302F
title: CODECAPI_AVEncH264SPSID, propriété (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e06fb78fc128b2eec5db2c61faf70ee10a5eba5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127296335"
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

## <a name="requirements"></a>Spécifications



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

 

