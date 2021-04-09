---
title: D2D1_SIZE_U (D2DBaseTypes. h)
description: Stocke une paire ordonnée d'entiers, représentant généralement la largeur et la hauteur d'un rectangle.
ms.assetid: e28da5ee-7d68-4ec5-b477-c6ead0c725e6
keywords:
- D2D1_SIZE_U
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c78b5c317a98169957402dd125c054b8f6e0bc69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103205"
---
# <a name="d2d1_size_u"></a><span data-ttu-id="4e3df-104">Taille de D2D1 \_ \_ U</span><span class="sxs-lookup"><span data-stu-id="4e3df-104">D2D1\_SIZE\_U</span></span>

<span data-ttu-id="4e3df-105">Stocke une paire ordonnée d'entiers, représentant généralement la largeur et la hauteur d'un rectangle.</span><span class="sxs-lookup"><span data-stu-id="4e3df-105">Stores an ordered pair of integers, typically the width and height of a rectangle.</span></span>


```C++
typedef D2D_SIZE_U D2D1_SIZE_U;
```



## <a name="remarks"></a><span data-ttu-id="4e3df-106">Notes</span><span class="sxs-lookup"><span data-stu-id="4e3df-106">Remarks</span></span>

<span data-ttu-id="4e3df-107">Comme les points, les tailles sont un autre concept graphique important.</span><span class="sxs-lookup"><span data-stu-id="4e3df-107">Like points, sizes are another important graphics concept.</span></span> <span data-ttu-id="4e3df-108">Dans Direct2D, les tailles sont représentées par les structures **d2d1 \_ size \_ U** ou [**d2d1 \_ size \_ F**](d2d1-size-f.md) .</span><span class="sxs-lookup"><span data-stu-id="4e3df-108">In Direct2D, sizes are represented by the **D2D1\_SIZE\_U** or [**D2D1\_SIZE\_F**](d2d1-size-f.md) structures.</span></span> <span data-ttu-id="4e3df-109">Elles contiennent toutes deux une paire ordonnée de nombres.</span><span class="sxs-lookup"><span data-stu-id="4e3df-109">They both contain an ordered pair of numbers.</span></span> <span data-ttu-id="4e3df-110">La **structure \_ \_ U de taille d2d1** contient une paire ordonnée de valeurs **UInt32** et la **structure \_ d2d1 taille \_ F** contient une paire ordonnée de valeurs **float** .</span><span class="sxs-lookup"><span data-stu-id="4e3df-110">The **D2D1\_SIZE\_U** structure contains an ordered pair of **UINT32** values, and the **D2D1\_SIZE\_F** structure contains an ordered pair of **FLOAT** values.</span></span>

<span data-ttu-id="4e3df-111">La **structure \_ \_ U de taille d2d1** offre un moyen pratique de stocker une paire ordonnée de nombres, tels que la largeur et la hauteur d’un rectangle.</span><span class="sxs-lookup"><span data-stu-id="4e3df-111">The **D2D1\_SIZE\_U** structure provides a convenient way for you to store an ordered pair of numbers, such as the width and height of a rectangle.</span></span>

<span data-ttu-id="4e3df-112">**D2d1 \_ TAILLE \_ u** est un nouveau nom pour un type déjà défini **de \_ taille \_ D2D (u**).</span><span class="sxs-lookup"><span data-stu-id="4e3df-112">**D2D1\_SIZE\_U** is a new name for an already defined type **D2D\_SIZE\_U**.</span></span> <span data-ttu-id="4e3df-113">Vous pouvez utiliser la fonction **d2d1 :: Resize** pour créer une structure **de \_ taille \_ d2d1** .</span><span class="sxs-lookup"><span data-stu-id="4e3df-113">You can use the **D2D1::SizeU** function to create a **D2D1\_SIZE\_U** structure.</span></span> <span data-ttu-id="4e3df-114">Cette structure est couramment utilisée pour spécifier la taille en pixels d’une structure [**de \_ \_ Propriétés de \_ cible \_ de rendu HWND d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_hwnd_render_target_properties) .</span><span class="sxs-lookup"><span data-stu-id="4e3df-114">A common use for this structure is to specify the pixel size of a [**D2D1\_HWND\_RENDER\_TARGET\_PROPERTIES**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_hwnd_render_target_properties) structure.</span></span> <span data-ttu-id="4e3df-115">L’exemple suivant illustre l’utilisation de cette structure.</span><span class="sxs-lookup"><span data-stu-id="4e3df-115">The following provides an example of using this structure.</span></span>


```C++
    if (!m_pRenderTarget)
    {
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



## <a name="requirements"></a><span data-ttu-id="4e3df-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4e3df-116">Requirements</span></span>



| <span data-ttu-id="4e3df-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4e3df-117">Requirement</span></span> | <span data-ttu-id="4e3df-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="4e3df-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e3df-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e3df-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4e3df-120">Windows 7, Windows Vista avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Vista, applications \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="4e3df-120">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="4e3df-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e3df-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4e3df-122">Windows Server 2008 R2, Windows Server 2008 avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Server 2008 pour applications \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="4e3df-122">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="4e3df-123">Téléphone minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e3df-123">Minimum supported phone</span></span><br/>  | <span data-ttu-id="4e3df-124">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="4e3df-124">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="4e3df-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="4e3df-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e3df-126"><dt>D2DBaseTypes. h (inclure D2d1. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4e3df-126"><dt>D2DBaseTypes.h (include D2d1.h)</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="4e3df-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e3df-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e3df-128">**\_Taille ( \_ U) D2D**</span><span class="sxs-lookup"><span data-stu-id="4e3df-128">**D2D\_SIZE\_U**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_size_u)
</dt> <dt>

[<span data-ttu-id="4e3df-129">**D2D1 \_ taille \_ F**</span><span class="sxs-lookup"><span data-stu-id="4e3df-129">**D2D1\_SIZE\_F**</span></span>](d2d1-size-f.md)
</dt> <dt>

[<span data-ttu-id="4e3df-130">**D2D1::HwndRenderTargetProperties**</span><span class="sxs-lookup"><span data-stu-id="4e3df-130">**D2D1::HwndRenderTargetProperties**</span></span>](/windows/desktop/api/d2d1helper/nf-d2d1helper-hwndrendertargetproperties)
</dt> </dl>

 

