---
title: D3D12_RECT (D3D12. h)
description: D3D12 \_ Rect est déclaré en tant que Rect.
ms.assetid: 39511ACE-7AC5-42A2-896D-7E0977A346C6
keywords:
- D3D12_RECT
topic_type:
- apiref
api_name:
- D3D12_RECT
api_location:
- D3D12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 951c0de8468b0384ae1a474740f9b46c2aa68dfc23c3394f8dae6a8064d9319e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751729"
---
# <a name="d3d12_rect"></a>D3D12 \_ Rect

D3D12 \_ Rect est déclaré en tant que Rect. Pour plus d’informations sur cette structure de rectangles GDI, consultez [**Rect**](/previous-versions//dd162897(v=vs.85)).

``` syntax
typedef RECT D3D12_RECT;
```

## <a name="remarks"></a>Remarques

Cette structure est utilisée par les méthodes suivantes :

-   [**RSSetScissorRects**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetscissorrects)
-   [**ClearDepthStencilView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-cleardepthstencilview)
-   [**ClearRenderTargetView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearrendertargetview)
-   [**ClearUnorderedAccessViewUint**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
-   [**ClearUnorderedAccessViewFloat**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)

Cette structure est un membre de la structure de la [**\_ \_ région ignorée D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_discard_region) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D12. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures principales](direct3d-12-structures.md)
</dt> <dt>

[**CD3DX12 \_ Rect**](cd3dx12-rect.md)
</dt> </dl>

 

