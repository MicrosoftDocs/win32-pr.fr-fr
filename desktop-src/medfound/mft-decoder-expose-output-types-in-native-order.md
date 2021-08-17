---
description: Spécifie si un décodeur expose des types de sortie IYUV/I420 (convenant au transcodage) avant d’autres formats.
ms.assetid: 8505CFA1-210A-4DA8-B92A-FCE62F0310E5
title: Attribut MFT_DECODER_EXPOSE_OUTPUT_TYPES_IN_NATIVE_ORDER (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46b91492054215aee5a63dbcf0adf300d74933a0859a2d71256e7e4352deba9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117872338"
---
# <a name="mft_decoder_expose_output_types_in_native_order-attribute"></a>Le \_ DÉcodeur MFT \_ expose les \_ \_ types \_ de sortie dans l' \_ \_ attribut order natif

Spécifie si un décodeur expose des types de sortie IYUV/I420 (convenant au transcodage) avant d’autres formats.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Remarques

Cet attribut est une indication pour le décodeur de réorganiser sa liste de types de sortie dans un ordre particulier, en fonction de l’utilisation prévue, de lecture ou de transcodage.

Pour la plupart des formats d’encodage (H. 264, MPEG-2, WMV), les décodeurs vidéo dans Microsoft Media Foundation prennent en charge plusieurs sorties YUV courantes, notamment NV12, YV12, YUY2, IYUV et I420. Le décodeur offre une liste triée des types de sortie par le biais de sa méthode [**IMFTransform :: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) .

Pour la lecture, NV12 est le format le plus efficace et le plus largement pris en charge. Par conséquent, par défaut, les décodeurs offrent généralement NV12 comme premier type de sortie dans la liste. Cela réduit le temps nécessaire pour résoudre le type de média lors de la génération d’une topologie de lecture. Toutefois, pour le transcodage, les IYUV ou les I420 sont plus efficaces pour le processeur et sont généralement préférés par des encodeurs.

Si un décodeur prend en charge cet attribut, l’attribut a le comportement suivant :

-   Si l’attribut a une valeur différente de zéro, IYUV et I420 apparaissent en premier dans la liste des types de médias de sortie. Ce paramètre est plus efficace pour le transcodage.
-   Si l’attribut est égal à zéro, NV12 apparaît en premier dans la liste des types de médias de sortie. Ce paramètre est plus efficace pour la lecture et est la valeur par défaut.

Pour définir cet attribut :

1.  Appelez [**IMFTransform :: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) sur le décodeur pour recevoir un pointeur [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .
2.  Appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) pour ajouter l’attribut.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau \| UWP apps\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                |
| En-tête<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




