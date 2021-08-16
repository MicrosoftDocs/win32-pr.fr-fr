---
description: Spécifie les indicateurs de liaison à utiliser lors de l’allocation des surfaces Microsoft Direct3D 11 pour les exemples de supports.
ms.assetid: C3B475B1-9A44-47EA-BCE7-D3D0FB56DDAC
title: Attribut MF_SA_D3D11_BINDFLAGS (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65f0fbc607ccdc8f878e25109fcadfdf8956007d99909d9a21c0e668951106d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119102462"
---
# <a name="mf_sa_d3d11_bindflags-attribute"></a>\_ \_ Attribut BINDFLAGS d3d11 MF sa \_

Spécifie les indicateurs de liaison à utiliser lors de l’allocation des surfaces Microsoft Direct3D 11 pour les exemples de supports.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Remarques

La **valeur de cet** attribut est une opération or au niveau du bit des indicateurs d' [**\_ \_ indicateur de liaison d3d11**](/windows/win32/api/d3d11/ne-d3d11-d3d11_bind_flag) .

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
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau \| UWP apps\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau \| UWP apps\]<br/>                              |
| En-tête<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
