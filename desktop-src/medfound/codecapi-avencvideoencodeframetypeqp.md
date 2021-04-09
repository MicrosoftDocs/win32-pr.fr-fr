---
description: Spécifie les types de frames (I, P ou B) auxquels le paramètre de quantification (QP) est appliqué.
ms.assetid: 6331033F-7EEB-41B3-B166-29686D4AADB6
title: CODECAPI_AVEncVideoEncodeFrameTypeQP, propriété (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76e68e0cb6cbdc076dbf523f3ae9dfd7b5870f47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111859"
---
# <a name="codecapi_avencvideoencodeframetypeqp-property"></a>CODECAPI \_ propriété AVEncVideoEncodeFrameTypeQP

Spécifie les types de frames (I, P ou B) auxquels le paramètre de quantification (QP) est appliqué.

## <a name="data-type"></a>Type de données

**ULONGULONG** (VT \_ UI8)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncVideoEncodeFrameTypeQP**

## <a name="remarks"></a>Notes

Pour les encodeurs qui prennent en charge la définition d’un paramètre de quantification (QP) pour différents types de trames (I, P, B), ils exposent cette API en plus de [CODECAPI \_ AVEncVideoEncodeQP](codecapi-avencvideoencodeqp.md). Si un encodeur ne prend en charge qu’un seul QP pour tous les types de frame, ils prennent en charge uniquement CODECAPI \_ AVEncVideoEncodeQP.

Il s’agit d’une propriété d’encodage dynamique qui signifie qu’une nouvelle valeur peut être définie à tout moment pendant la session d’encodage.

**Encodeurs H. 264/AVC :**

L’encodeur doit prendre en charge [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)et [**GetParameterRange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).

Un ensemble de champs 4 16 bits est utilisé pour spécifier le cadre RPS dans l’encodage Fixed-QP. Les champs sont les suivants :

-   **Bits 0-15 :** QP utilisé pour les trames I, plage valide \[ 0, 51 \] .
-   **Bits 16-31 :** QP utilisé pour les frames P, plage valide \[ 0, 51 \] .
-   **Bits 32-47 :** QP utilisé pour les frames B, plage valide \[ 0, 51\]
-   **Bits 48-63 :** réservé

Quand ce CodecAPI est pris en charge, les encodeurs prennent en charge le paramètre QP sur le type de trame I, P et B.

La valeur par défaut est 0x0000001a001a001a. QP égal à 26 pour I, P et B.

Quand [CODECAPI \_ AVEncVideoSelectLayer](codecapi-avencvideoselectlayer.md) sélectionne une couche temporelle spécifique, [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue) de CODECAPI \_ AVEncVideoEncodeFrameTypeQP doit définir QP pour les images I, P et B sur cette couche temporelle. Par défaut, il définit QP pour les images I, P et B sur la couche temporelle de base de la couche temporelle 0.

[CODECAPI \_ AVEncVideoMaxQP](codecapi-avencvideomaxqp.md) et [CODECAPI \_ AVEncVideoMinQP](codecapi-avencvideominqp.md) doivent être utilisés pour définir et limiter la plage de QP pour RPS de tous les types d’images, I, P et B.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | \[Applications Windows 8.1 Desktop Apps \| UWP\]<br/>                                   |
| Serveur minimal pris en charge<br/> | Applications Windows Server 2012 R2 \[ Desktop Apps \| UWP\]<br/>                        |
| En-tête<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

