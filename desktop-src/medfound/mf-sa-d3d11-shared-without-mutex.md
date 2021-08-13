---
description: Indique à l’allocateur d’échantillon vidéo de créer des textures partageables à l’aide du mécanisme hérité.
ms.assetid: A9F4D4AF-BB47-48E2-B40A-D0245FD61FAF
title: Attribut MF_SA_D3D11_SHARED_WITHOUT_MUTEX (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8495d0c2033f6ffbc1a212c9768af3157697eb588c968cb3fbd62959fa3515f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118740301"
---
# <a name="mf_sa_d3d11_shared_without_mutex-attribute"></a>MF \_ sa \_ d3d11 \_ partagée \_ sans \_ attribut MUTEX

Indique à l’allocateur d’échantillon vidéo de créer des textures partageables à l’aide du mécanisme hérité.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Remarques

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
</dt> <dt>

[**IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex)
</dt> <dt>

[MF \_ sa \_ d3d11 \_ partagée](mf-sa-d3d11-shared.md)
</dt> </dl>

 

 




