---
description: Spécifie les indicateurs de liaison à utiliser lors de l’allocation des surfaces Microsoft Direct3D 11 pour les exemples de supports.
ms.assetid: C3B475B1-9A44-47EA-BCE7-D3D0FB56DDAC
title: Attribut MF_SA_D3D11_BINDFLAGS (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bb5ae4161a6782a3ea7a69b471044e43c5ee7a4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414129"
---
# <a name="mf_sa_d3d11_bindflags-attribute"></a>\_ \_ Attribut BINDFLAGS d3d11 MF sa \_

Spécifie les indicateurs de liaison à utiliser lors de l’allocation des surfaces Microsoft Direct3D 11 pour les exemples de supports.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Notes

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

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau \| UWP apps\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau \| UWP apps\]<br/>                              |
| En-tête<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
