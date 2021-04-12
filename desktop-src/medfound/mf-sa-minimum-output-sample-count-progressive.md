---
description: Indique le nombre minimal d’échantillons progressifs que la Microsoft Media Foundation transformation (MFT) doit autoriser à être nombre à un moment donné.
ms.assetid: C1F27F39-FADA-4644-ACD6-B02EAD9CFFE7
title: Attribut MF_SA_MINIMUM_OUTPUT_SAMPLE_COUNT_PROGRESSIVE (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b452f9fa4016705ed90a7f5b07abcaa6ff11983
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203715"
---
# <a name="mf_sa_minimum_output_sample_count_progressive-attribute"></a>\_ \_ \_ \_ \_ \_ Attribut progressif du nombre minimal d’échantillons de sortie MF sa

Indique le nombre minimal d’échantillons progressifs que la Microsoft Media Foundation transformation (MFT) doit autoriser à être nombre à un moment donné.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Notes

Cet attribut s’applique uniquement à MFTs qui utilisent une mémoire tampon circulaire pour allouer leurs propres exemples de sortie. Les autres MFTs ignorent cet attribut.

Pour définir cet attribut :

1.  Appelez [**IMFTransform :: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) sur le décodeur pour recevoir un pointeur [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .
2.  Appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) pour ajouter l’attribut.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications Windows 8 \[ Desktop Apps \| UWP\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ \| apps UWP\]<br/>                              |
| En-tête<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




