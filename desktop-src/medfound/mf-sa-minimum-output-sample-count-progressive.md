---
description: Indique le nombre minimal d’échantillons progressifs que la Microsoft Media Foundation transformation (MFT) doit autoriser à être nombre à un moment donné.
ms.assetid: C1F27F39-FADA-4644-ACD6-B02EAD9CFFE7
title: Attribut MF_SA_MINIMUM_OUTPUT_SAMPLE_COUNT_PROGRESSIVE (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48df5262e225b8768d3251f9768cf2156ee2acacb19ca70752ae5bf989b682ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955429"
---
# <a name="mf_sa_minimum_output_sample_count_progressive-attribute"></a>\_ \_ \_ \_ \_ \_ Attribut progressif du nombre minimal d’échantillons de sortie MF sa

Indique le nombre minimal d’échantillons progressifs que la Microsoft Media Foundation transformation (MFT) doit autoriser à être nombre à un moment donné.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Remarques

Cet attribut s’applique uniquement à MFTs qui utilisent une mémoire tampon circulaire pour allouer leurs propres exemples de sortie. Les autres MFTs ignorent cet attribut.

Pour définir cet attribut :

1.  Appelez [**IMFTransform :: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) sur le décodeur pour recevoir un pointeur [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .
2.  Appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) pour ajouter l’attribut.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau \| UWP apps\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau \| UWP apps\]<br/>                              |
| En-tête<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




