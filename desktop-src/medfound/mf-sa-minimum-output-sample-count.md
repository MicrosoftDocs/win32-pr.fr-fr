---
description: Spécifie le nombre maximal d’échantillons de sortie qu’une Microsoft Media Foundation transformation (MFT) aura en suspens dans le pipeline à tout moment.
ms.assetid: 53D393B4-BFF1-430F-9CD1-5071336E6F04
title: Attribut MF_SA_MINIMUM_OUTPUT_SAMPLE_COUNT (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cf168158fd6a5f9a173d4d5d25dda3fa5b16d2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201722"
---
# <a name="mf_sa_minimum_output_sample_count-attribute"></a>\_Attribut de \_ nombre minimal d' \_ échantillons de sortie MF \_ sa \_

Spécifie le nombre maximal d’échantillons de sortie qu’une Microsoft Media Foundation transformation (MFT) aura en suspens dans le pipeline à tout moment.

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
</dt> <dt>

[Attributs de transformation](transform-attributes.md)
</dt> </dl>

 

 




