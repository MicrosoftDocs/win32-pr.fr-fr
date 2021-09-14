---
description: Indique à l’allocateur d’échantillon vidéo de créer des textures partageables à l’aide du mécanisme hérité.
ms.assetid: A9F4D4AF-BB47-48E2-B40A-D0245FD61FAF
title: Attribut MF_SA_D3D11_SHARED_WITHOUT_MUTEX (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9139328c9d272007be6e5cd9434614cb1de8c9fc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414125"
---
# <a name="mf_sa_d3d11_shared_without_mutex-attribute"></a>MF \_ sa \_ d3d11 \_ partagée \_ sans \_ attribut MUTEX

Indique à l’allocateur d’échantillon vidéo de créer des textures partageables à l’aide du mécanisme hérité.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Notes

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
</dt> <dt>

[**IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex)
</dt> <dt>

[MF \_ sa \_ d3d11 \_ partagée](mf-sa-d3d11-shared.md)
</dt> </dl>

 

 




