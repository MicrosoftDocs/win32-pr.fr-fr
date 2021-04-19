---
description: Codes d’État qui peuvent être retournés par les fonctions DXGI.
ms.assetid: dd7480b4-8218-4716-ab9f-74a9955b8aa7
title: DXGI_STATUS (DXGI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b39c402880ccdcbda009402d56127e70a61543d0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523818"
---
# <a name="dxgi_status"></a><span data-ttu-id="c187e-103">État de DXGI \_</span><span class="sxs-lookup"><span data-stu-id="c187e-103">DXGI\_STATUS</span></span>

<span data-ttu-id="c187e-104">Codes d’État qui peuvent être retournés par les fonctions DXGI.</span><span class="sxs-lookup"><span data-stu-id="c187e-104">Status codes that can be returned by DXGI functions.</span></span>



| <span data-ttu-id="c187e-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="c187e-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                      | <span data-ttu-id="c187e-106">Description</span><span class="sxs-lookup"><span data-stu-id="c187e-106">Description</span></span>                                                                                                                                                                                                                                                                                              |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_STATUS_OCCLUDED"></span><span id="dxgi_status_occluded"></span><dl> <span data-ttu-id="c187e-107"><dt>**Dxgi \_ ÉTAT \_ bloqués**</dt> <dt>0x087A0001</dt></span><span class="sxs-lookup"><span data-stu-id="c187e-107"><dt>**DXGI\_STATUS\_OCCLUDED**</dt> <dt>0x087A0001</dt></span></span> </dl>                                                 | <span data-ttu-id="c187e-108">Le contenu de la fenêtre n’est pas visible.</span><span class="sxs-lookup"><span data-stu-id="c187e-108">The window content is not visible.</span></span> <span data-ttu-id="c187e-109">Lors de la réception de cet État, une application peut arrêter le rendu et utiliser le \_ test dxgi présente \_ pour déterminer quand reprendre le rendu.</span><span class="sxs-lookup"><span data-stu-id="c187e-109">When receiving this status, an application can stop rendering and use DXGI\_PRESENT\_TEST to determine when to resume rendering.</span></span> <span data-ttu-id="c187e-110">Vous ne recevrez pas \_ d’État dxgi \_ bloqués si vous utilisez une chaîne de permutation de modèle.</span><span class="sxs-lookup"><span data-stu-id="c187e-110">You will not receive DXGI\_STATUS\_OCCLUDED if you're using a flip model swap chain.</span></span><br/>                                                                                                                           |
| <span id="DXGI_STATUS_MODE_CHANGED"></span><span id="dxgi_status_mode_changed"></span><dl> <span data-ttu-id="c187e-111"><dt>**Dxgi \_ MODE d’état \_ \_ modifié**</dt> <dt>0x087A0007</dt></span><span class="sxs-lookup"><span data-stu-id="c187e-111"><dt>**DXGI\_STATUS\_MODE\_CHANGED**</dt> <dt>0x087A0007</dt></span></span> </dl>                                    | <span data-ttu-id="c187e-112">Le mode d’affichage du Bureau a été modifié, il peut y avoir une conversion/étirement de couleurs.</span><span class="sxs-lookup"><span data-stu-id="c187e-112">The desktop display mode has been changed, there might be color conversion/stretching.</span></span> <span data-ttu-id="c187e-113">L’application doit appeler [**IDXGISwapChain :: ResizeBuffers**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) pour qu’elle corresponde au nouveau mode d’affichage.</span><span class="sxs-lookup"><span data-stu-id="c187e-113">The application should call [**IDXGISwapChain::ResizeBuffers**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) to match the new display mode.</span></span><br/>                                                                       |
| <span id="DXGI_STATUS_MODE_CHANGE_IN_PROGRESS"></span><span id="dxgi_status_mode_change_in_progress"></span><dl> <span data-ttu-id="c187e-114"><dt>**Dxgi \_ \_ \_ Changement du mode \_ d’État en \_ cours**</dt> <dt>0x087A0008</dt></span><span class="sxs-lookup"><span data-stu-id="c187e-114"><dt>**DXGI\_STATUS\_MODE\_CHANGE\_IN\_PROGRESS**</dt> <dt>0x087A0008</dt></span></span> </dl> | <span data-ttu-id="c187e-115">[**IDXGISwapChain :: ResizeTarget**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizetarget) et [**IDXGISwapChain :: SetFullscreenState**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate) retournent \_ \_ \_ la modification du mode d’État dxgi \_ en \_ cours si une transition de mode plein écran/avec fenêtre se produit lorsque l’une des API est appelée.</span><span class="sxs-lookup"><span data-stu-id="c187e-115">[**IDXGISwapChain::ResizeTarget**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizetarget) and [**IDXGISwapChain::SetFullscreenState**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate) will return DXGI\_STATUS\_MODE\_CHANGE\_IN\_PROGRESS if a fullscreen/windowed mode transition is occurring when either API is called.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c187e-116">Notes</span><span class="sxs-lookup"><span data-stu-id="c187e-116">Remarks</span></span>

<span data-ttu-id="c187e-117">La valeur **HRESULT** pour chaque valeur d' **\_ État dxgi** est déterminée à partir de cette macro qui est définie dans DXGItype. h :</span><span class="sxs-lookup"><span data-stu-id="c187e-117">The **HRESULT** value for each **DXGI\_STATUS** value is determined from this macro that is defined in DXGItype.h:</span></span>


```
#define _FACDXGI    0x87a
#define MAKE_DXGI_STATUS(code)  MAKE_HRESULT(0, _FACDXGI, code)
```



<span data-ttu-id="c187e-118">Par exemple, **dxgi \_ Status \_ bloqués** est défini comme **0x087A0001**:</span><span class="sxs-lookup"><span data-stu-id="c187e-118">For example, **DXGI\_STATUS\_OCCLUDED** is defined as **0x087A0001**:</span></span>


```
#define DXGI_STATUS_OCCLUDED                    MAKE_DXGI_STATUS(1)
```



## <a name="requirements"></a><span data-ttu-id="c187e-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c187e-119">Requirements</span></span>



| <span data-ttu-id="c187e-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c187e-120">Requirement</span></span> | <span data-ttu-id="c187e-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="c187e-121">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="c187e-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="c187e-122">Header</span></span><br/> | <dl> <span data-ttu-id="c187e-123"><dt>DXGI. h</dt></span><span class="sxs-lookup"><span data-stu-id="c187e-123"><dt>DXGI.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c187e-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c187e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c187e-125">Constantes DXGI</span><span class="sxs-lookup"><span data-stu-id="c187e-125">DXGI Constants</span></span>](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 




