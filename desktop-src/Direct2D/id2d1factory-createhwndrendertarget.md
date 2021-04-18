---
title: Méthodes ID2D1Factory CreateHwndRenderTarget (D2d1. h)
description: Crée un ID2D1HwndRenderTarget, une cible de rendu qui est rendue dans une fenêtre.
ms.assetid: 3b55b1b0-a423-40dc-9581-c1fbe8134ca5
keywords:
- Méthodes CreateHwndRenderTarget Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 984de8aea923c5b90d05fb79bc0c9edc319fb4bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526342"
---
# <a name="id2d1factorycreatehwndrendertarget-methods"></a><span data-ttu-id="c5ce5-104">ID2D1Factory :: CreateHwndRenderTarget, méthodes</span><span class="sxs-lookup"><span data-stu-id="c5ce5-104">ID2D1Factory::CreateHwndRenderTarget methods</span></span>

<span data-ttu-id="c5ce5-105">Crée un [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)), une cible de rendu qui est rendue dans une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="c5ce5-105">Creates an [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)), a render target that renders to a window.</span></span>

### <a name="overload-list"></a><span data-ttu-id="c5ce5-106">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="c5ce5-106">Overload list</span></span>



| <span data-ttu-id="c5ce5-107">Méthode</span><span class="sxs-lookup"><span data-stu-id="c5ce5-107">Method</span></span>                                                                                                                                                                                                                                                                              | <span data-ttu-id="c5ce5-108">Description</span><span class="sxs-lookup"><span data-stu-id="c5ce5-108">Description</span></span>                                                                                                             |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5ce5-109">[**CreateHwndRenderTarget (propriétés de la \_ cible de rendu d2d1, propriétés de la cible de \_ \_ \* \_ rendu HWND d2d1 \_ \_ \_ \* , ID2D1HwndRenderTarget \* \* )**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c5ce5-109">[**CreateHwndRenderTarget(D2D1\_RENDER\_TARGET\_PROPERTIES\*,D2D1\_HWND\_RENDER\_TARGET\_PROPERTIES\*,ID2D1HwndRenderTarget\*\*)**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))</span></span> | <span data-ttu-id="c5ce5-110">Crée un [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)), une cible de rendu qui est rendue dans une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="c5ce5-110">Creates an [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)), a render target that renders to a window.</span></span><br/> |
| <span data-ttu-id="c5ce5-111">[**CreateHwndRenderTarget (propriétés de la \_ cible de rendu D2D1 \_ \_&, propriétés de la cible de \_ rendu HWND d2d1 \_ \_ \_&, ID2D1HwndRenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createhwndrendertarget(constd2d1_render_target_properties__constd2d1_hwnd_render_target_properties__id2d1hwndrendertarget))</span><span class="sxs-lookup"><span data-stu-id="c5ce5-111">[**CreateHwndRenderTarget(D2D1\_RENDER\_TARGET\_PROPERTIES&,D2D1\_HWND\_RENDER\_TARGET\_PROPERTIES&,ID2D1HwndRenderTarget\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createhwndrendertarget(constd2d1_render_target_properties__constd2d1_hwnd_render_target_properties__id2d1hwndrendertarget))</span></span>   | <span data-ttu-id="c5ce5-112">Crée un [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)), une cible de rendu qui est rendue dans une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="c5ce5-112">Creates an [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)), a render target that renders to a window.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c5ce5-113">Notes</span><span class="sxs-lookup"><span data-stu-id="c5ce5-113">Remarks</span></span>

<span data-ttu-id="c5ce5-114">Lorsque vous créez une cible de rendu et que l’accélération matérielle est disponible, vous allouez des ressources sur le GPU de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c5ce5-114">When you create a render target and hardware acceleration is available, you allocate resources on the computer's GPU.</span></span> <span data-ttu-id="c5ce5-115">En créant une cible de rendu une fois et en la conservant le plus longtemps possible, vous obtenez des avantages en matière de performances.</span><span class="sxs-lookup"><span data-stu-id="c5ce5-115">By creating a render target once and retaining it as long as possible, you gain performance benefits.</span></span> <span data-ttu-id="c5ce5-116">Votre application doit créer des cibles de rendu une seule fois et les conserver pendant toute la durée de vie de l’application ou jusqu’à ce que l’erreur de [**\_ recréation de la \_ cible D2DERR**](direct2d-error-codes.md) soit reçue.</span><span class="sxs-lookup"><span data-stu-id="c5ce5-116">Your application should create render targets once and hold onto them for the life of the application or until the [**D2DERR\_RECREATE\_TARGET**](direct2d-error-codes.md) error is received.</span></span> <span data-ttu-id="c5ce5-117">Lorsque vous recevez cette erreur, vous devez recréer la cible de rendu (et toutes les ressources qu’elle a créées).</span><span class="sxs-lookup"><span data-stu-id="c5ce5-117">When you receive this error, you need to recreate the render target (and any resources it created).</span></span>

## <a name="examples"></a><span data-ttu-id="c5ce5-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="c5ce5-118">Examples</span></span>

<span data-ttu-id="c5ce5-119">L’exemple suivant crée un [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c5ce5-119">The following example creates an [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)).</span></span>


```C++
RECT rc;
GetClientRect(m_hwnd, &rc);

D2D1_SIZE_U size = D2D1::SizeU(
    rc.right - rc.left,
    rc.bottom - rc.top
    );

// Create a Direct2D render target.
hr = m_pD2DFactory->CreateHwndRenderTarget(
    D2D1::RenderTargetProperties(),
    D2D1::HwndRenderTargetProperties(m_hwnd, size),
    &m_pRenderTarget
    );
```



## <a name="requirements"></a><span data-ttu-id="c5ce5-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c5ce5-120">Requirements</span></span>



| <span data-ttu-id="c5ce5-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c5ce5-121">Requirement</span></span> | <span data-ttu-id="c5ce5-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5ce5-122">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c5ce5-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="c5ce5-123">Header</span></span><br/>  | <dl> <span data-ttu-id="c5ce5-124"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5ce5-124"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="c5ce5-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c5ce5-125">Library</span></span><br/> | <dl> <span data-ttu-id="c5ce5-126"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c5ce5-126"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="c5ce5-127">DLL</span><span class="sxs-lookup"><span data-stu-id="c5ce5-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="c5ce5-128"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5ce5-128"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5ce5-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5ce5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5ce5-130">**ID2D1Factory**</span><span class="sxs-lookup"><span data-stu-id="c5ce5-130">**ID2D1Factory**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
</dt> </dl>
