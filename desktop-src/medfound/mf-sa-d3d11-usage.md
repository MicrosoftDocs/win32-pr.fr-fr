---
description: Spécifie comment allouer des surfaces Microsoft Direct3D 11 pour des exemples de supports.
ms.assetid: E9A415FA-74BF-4822-BB0E-D8AAA7D73664
title: Attribut MF_SA_D3D11_USAGE (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e0609435cf42134f28e8464fd3173412836c8d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201723"
---
# <a name="mf_sa_d3d11_usage-attribute"></a>\_Attribut d' \_ utilisation d3d11 MF sa \_

Spécifie comment allouer des surfaces Microsoft Direct3D 11 pour des exemples de supports. L’utilisation de indique directement si un échantillon est accessible par le processeur ou le GPU.

## <a name="data-type"></a>Type de données

**D3d11 \_ UTILISATION** stockée en tant que **UInt32**

## <a name="remarks"></a>Notes

La valeur de cet attribut est une valeur d' [**\_ utilisation d3d11**](/windows/win32/api/d3d11/ne-d3d11-d3d11_usage) .

### <a name="microsoft-media-foundation-transforms"></a>Transformations de Microsoft Media Foundation

Dans ce contexte, l’attribut s’applique uniquement lorsque la Microsoft Media Foundation transformation (MFT) renvoie la **valeur true** pour l’attribut [prenant en \_ \_ \_ charge d3d11 MF](mf-sa-d3d11-aware.md) .

Si une table MFT prend en charge Direct3D 11, cet attribut fournit un indicateur à la MFT lors de l’allocation des surfaces Microsoft Direct3D pour la sortie. Définissez l’attribut comme suit :

1.  Appelez [**IMFTransform :: GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) pour accéder au magasin d’attributs MFT.
2.  Appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

Le pipeline Media Foundation définit l’attribut avant le démarrage de la diffusion en continu. La table MFT doit tenter d’honorer le paramètre lorsqu’il alloue des surfaces. Si ce n’est pas possible, la table MFT peut ignorer l’attribut, au lieu d’échouer à l’allocation.

En outre, si la table MFT requiert des surfaces Direct3D pour l’entrée, elle peut exposer cet attribut comme un indicateur pour la façon dont les surfaces d’entrée doivent être allouées. Interrogez l’attribut comme suit :

1.  Appelez [**IMFTransform :: GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) pour accéder aux attributs du flux d’entrée.
2.  Appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

### <a name="sample-allocator"></a>Allocateur d’échantillon

Cet attribut peut être défini sur l’allocateur d’échantillon vidéo, dans la méthode [**IMFVideoSampleAllocatorEx :: InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) .

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

 

 
