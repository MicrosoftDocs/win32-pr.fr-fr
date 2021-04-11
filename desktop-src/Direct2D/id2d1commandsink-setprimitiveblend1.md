---
title: Méthode ID2D1CommandSink1 SetPrimitiveBlend1
description: Définit un nouveau mode de fusion primitif.
ms.assetid: 3EA9EC07-1B2F-48A2-ABFB-2DA0E2EFFBF4
keywords:
- SetPrimitiveBlend1, méthode Direct2D
- Méthode SetPrimitiveBlend1 Direct2D, interface ID2D1CommandSink1
- ID2D1CommandSink1, méthode SetPrimitiveBlend1
topic_type:
- apiref
api_name:
- ID2D1CommandSink1.SetPrimitiveBlend1
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b3aa961eec873cc84e5b34ce41279c09f580e63d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103545"
---
# <a name="id2d1commandsink1setprimitiveblend1-method"></a><span data-ttu-id="bc44c-106">ID2D1CommandSink1 :: SetPrimitiveBlend1, méthode</span><span class="sxs-lookup"><span data-stu-id="bc44c-106">ID2D1CommandSink1::SetPrimitiveBlend1 method</span></span>

<span data-ttu-id="bc44c-107">Définit un nouveau mode de fusion primitif.</span><span class="sxs-lookup"><span data-stu-id="bc44c-107">Sets a new primitive blend mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc44c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bc44c-108">Syntax</span></span>


```C++
HRESULT SetPrimitiveBlend1(
   D2D1_PRIMITIVE_BLEND primitiveBlend
);
```



## <a name="parameters"></a><span data-ttu-id="bc44c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bc44c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc44c-110">*primitiveBlend*</span><span class="sxs-lookup"><span data-stu-id="bc44c-110">*primitiveBlend*</span></span> 
</dt> <dd>

<span data-ttu-id="bc44c-111">Type : **[ **d2d1 \_ primitive \_ Blend**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend)**</span><span class="sxs-lookup"><span data-stu-id="bc44c-111">Type: **[**D2D1\_PRIMITIVE\_BLEND**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend)**</span></span>

<span data-ttu-id="bc44c-112">Fusion primitive qui s’appliquera aux primitives suivantes.</span><span class="sxs-lookup"><span data-stu-id="bc44c-112">The primitive blend that will apply to subsequent primitives.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc44c-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bc44c-113">Return value</span></span>

<span data-ttu-id="bc44c-114">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="bc44c-114">Type: **HRESULT**</span></span>

<span data-ttu-id="bc44c-115">Si la méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="bc44c-115">If the method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bc44c-116">En cas d’échec, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bc44c-116">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc44c-117">Notes</span><span class="sxs-lookup"><span data-stu-id="bc44c-117">Remarks</span></span>

### <a name="blend-modes"></a><span data-ttu-id="bc44c-118">Modes de fusion</span><span class="sxs-lookup"><span data-stu-id="bc44c-118">Blend modes</span></span>

<span data-ttu-id="bc44c-119">Pour le rendu avec alias (à l’exception du mode MIN), la valeur de sortie O est calculée en interpolant de manière linéaire la valeur *Blend (S, D)* avec la valeur de pixel de destination, en fonction de la quantité de la primitive qui couvre le pixel de destination.</span><span class="sxs-lookup"><span data-stu-id="bc44c-119">For aliased rendering (except for MIN mode), the output value O is computed by linearly interpolating the value *blend(S, D)* with the destination pixel value, based on the amount that the primitive covers the destination pixel.</span></span>

<span data-ttu-id="bc44c-120">Le tableau ci-dessous montre les modes de fusion primitifs pour la fusion avec alias et l’anticrénelage.</span><span class="sxs-lookup"><span data-stu-id="bc44c-120">The table here shows the primitive blend modes for both aliased and antialiased blending.</span></span> <span data-ttu-id="bc44c-121">Les équations figurant dans le tableau utilisent les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="bc44c-121">The equations listed in the table use these elements:</span></span>

-   <span data-ttu-id="bc44c-122">O = sortie</span><span class="sxs-lookup"><span data-stu-id="bc44c-122">O = Output</span></span>
-   <span data-ttu-id="bc44c-123">S = source</span><span class="sxs-lookup"><span data-stu-id="bc44c-123">S = Source</span></span>
-   <span data-ttu-id="bc44c-124">SA = source alpha</span><span class="sxs-lookup"><span data-stu-id="bc44c-124">SA = Source Alpha</span></span>
-   <span data-ttu-id="bc44c-125">D = destination</span><span class="sxs-lookup"><span data-stu-id="bc44c-125">D = Destination</span></span>
-   <span data-ttu-id="bc44c-126">DA = alpha de destination</span><span class="sxs-lookup"><span data-stu-id="bc44c-126">DA = Destination Alpha</span></span>
-   <span data-ttu-id="bc44c-127">C = couverture en pixels</span><span class="sxs-lookup"><span data-stu-id="bc44c-127">C = Pixel coverage</span></span>



| <span data-ttu-id="bc44c-128">Mode de fusion primitif</span><span class="sxs-lookup"><span data-stu-id="bc44c-128">Primitive blend mode</span></span>                 | <span data-ttu-id="bc44c-129">Fusion avec alias</span><span class="sxs-lookup"><span data-stu-id="bc44c-129">Aliased blending</span></span>                            | <span data-ttu-id="bc44c-130">Fusion avec anticrénelage</span><span class="sxs-lookup"><span data-stu-id="bc44c-130">Antialiased blending</span></span>            | <span data-ttu-id="bc44c-131">Description</span><span class="sxs-lookup"><span data-stu-id="bc44c-131">Description</span></span>                                                                                                              |
|--------------------------------------|---------------------------------------------|---------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc44c-132">\_Source de \_ fusion primitive d2d1 \_ \_ sur</span><span class="sxs-lookup"><span data-stu-id="bc44c-132">D2D1\_PRIMITIVE\_BLEND\_SOURCE\_OVER</span></span> | <span data-ttu-id="bc44c-133">O = (S + (1 SA) \* D) \* C + D \* (1 c)</span><span class="sxs-lookup"><span data-stu-id="bc44c-133">O = (S + (1   SA) \* D) \* C + D \* (1   C)</span></span> | <span data-ttu-id="bc44c-134">O = S \* C + D \* (1 sa \* c)</span><span class="sxs-lookup"><span data-stu-id="bc44c-134">O = S \* C + D \*(1   SA \*C)</span></span>   | <span data-ttu-id="bc44c-135">Mode de fusion standard de la source sur la destination.</span><span class="sxs-lookup"><span data-stu-id="bc44c-135">The standard source-over-destination blend mode.</span></span>                                                                         |
| <span data-ttu-id="bc44c-136">\_Copie de \_ fusion \_ primitive d2d1</span><span class="sxs-lookup"><span data-stu-id="bc44c-136">D2D1\_PRIMITIVE\_BLEND\_COPY</span></span>         | <span data-ttu-id="bc44c-137">O = S \* C + D \* (1 c)</span><span class="sxs-lookup"><span data-stu-id="bc44c-137">O = S \* C + D \* (1   C)</span></span>                   | <span data-ttu-id="bc44c-138">O = S \* C + D \* (1 c)</span><span class="sxs-lookup"><span data-stu-id="bc44c-138">O = S \* C + D \* (1   C)</span></span>       | <span data-ttu-id="bc44c-139">La source est copiée vers la destination ; les pixels de destination sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="bc44c-139">The source is copied to the destination; the destination pixels are ignored.</span></span>                                             |
| <span data-ttu-id="bc44c-140">D2D1 \_ primitive \_ fusion \_ min.</span><span class="sxs-lookup"><span data-stu-id="bc44c-140">D2D1\_PRIMITIVE\_BLEND\_MIN</span></span>          | <span data-ttu-id="bc44c-141">O = min (S + 1-SA, D)</span><span class="sxs-lookup"><span data-stu-id="bc44c-141">O = Min(S + 1-SA, D)</span></span>                        | <span data-ttu-id="bc44c-142">O = min (S \* c + 1 sa \* c, D)</span><span class="sxs-lookup"><span data-stu-id="bc44c-142">O = Min(S \* C + 1   SA \*C, D)</span></span> | <span data-ttu-id="bc44c-143">Les valeurs de pixel obtenues utilisent la valeur minimale des valeurs de pixel source et de destination.</span><span class="sxs-lookup"><span data-stu-id="bc44c-143">The resulting pixel values use the minimum of the source and destination pixel values.</span></span> <span data-ttu-id="bc44c-144">Disponible dans Windows 8 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="bc44c-144">Available in Windows 8 and later.</span></span> |
| <span data-ttu-id="bc44c-145">\_Ajouter un \_ mélange \_ primitif d2d1</span><span class="sxs-lookup"><span data-stu-id="bc44c-145">D2D1\_PRIMITIVE\_BLEND\_ADD</span></span>          | <span data-ttu-id="bc44c-146">O = (S + D) \* C + d \* (1 c)</span><span class="sxs-lookup"><span data-stu-id="bc44c-146">O = (S + D) \* C + D \* (1   C)</span></span>             | <span data-ttu-id="bc44c-147">O = S \* C + D</span><span class="sxs-lookup"><span data-stu-id="bc44c-147">O = S \* C + D</span></span>                  | <span data-ttu-id="bc44c-148">Les valeurs de pixel obtenues sont la somme des valeurs de pixel source et de destination.</span><span class="sxs-lookup"><span data-stu-id="bc44c-148">The resulting pixel values are the sum of the source and destination pixel values.</span></span> <span data-ttu-id="bc44c-149">Disponible dans Windows 8 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="bc44c-149">Available in Windows 8 and later.</span></span>     |



 

![illustration des modes de fusion primitifs de Direct2D avec l’opacité et l’arrière-plan variables.](images/primblenddemo.png)

<span data-ttu-id="bc44c-151">Illustration des modes de fusion primitifs avec l’opacité et l’arrière-plan variables.</span><span class="sxs-lookup"><span data-stu-id="bc44c-151">An illustration of the primitive blend modes with varying opacity and backgrounds.</span></span>

<span data-ttu-id="bc44c-152">La fusion primitive s’applique à toute la primitive dessinée sur le contexte, sauf si elle est remplacée par le paramètre *compositeMode* sur l’API [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) .</span><span class="sxs-lookup"><span data-stu-id="bc44c-152">The primitive blend will apply to all of the primitive drawn on the context, unless this is overridden with the *compositeMode* parameter on the [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) API.</span></span>

<span data-ttu-id="bc44c-153">La fusion primitive s’applique à l’intérieur des primitives dessinées sur le contexte.</span><span class="sxs-lookup"><span data-stu-id="bc44c-153">The primitive blend applies to the interior of any primitives drawn on the context.</span></span> <span data-ttu-id="bc44c-154">Dans le cas de [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)), cela sera implicite par le rectangle d’image, le décalage et la transformation universelle.</span><span class="sxs-lookup"><span data-stu-id="bc44c-154">In the case of [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)), this will be implied by the image rectangle, offset and world transform.</span></span>

<span data-ttu-id="bc44c-155">Si la fusion primitive est différente de **d2d1 \_ primitive \_ Blend \_** , le rendu ClearType sera désactivé.</span><span class="sxs-lookup"><span data-stu-id="bc44c-155">If the primitive blend is anything other than **D2D1\_PRIMITIVE\_BLEND\_OVER** then ClearType rendering will be turned off.</span></span> <span data-ttu-id="bc44c-156">Si l’application force explicitement le rendu ClearType dans ces modes, le contexte de dessin sera placé dans un état d’erreur.</span><span class="sxs-lookup"><span data-stu-id="bc44c-156">If the application explicitly forces ClearType rendering in these modes, the drawing context will be placed in an error state.</span></span> <span data-ttu-id="bc44c-157">D2DERR \_ \_ un état incorrect est retourné à partir de [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) ou de [**flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush).</span><span class="sxs-lookup"><span data-stu-id="bc44c-157">D2DERR\_WRONG\_STATE will be returned from either [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush).</span></span>

## <a name="requirements"></a><span data-ttu-id="bc44c-158">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bc44c-158">Requirements</span></span>



| <span data-ttu-id="bc44c-159">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bc44c-159">Requirement</span></span> | <span data-ttu-id="bc44c-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="bc44c-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc44c-161">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bc44c-161">Minimum supported client</span></span><br/> | <span data-ttu-id="bc44c-162">\[Applications Windows 8.1 Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="bc44c-162">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="bc44c-163">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bc44c-163">Minimum supported server</span></span><br/> | <span data-ttu-id="bc44c-164">Applications Windows Server 2012 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="bc44c-164">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="bc44c-165">Téléphone minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bc44c-165">Minimum supported phone</span></span><br/>  | <span data-ttu-id="bc44c-166">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="bc44c-166">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bc44c-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bc44c-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc44c-168">**ID2D1CommandSink1**</span><span class="sxs-lookup"><span data-stu-id="bc44c-168">**ID2D1CommandSink1**</span></span>](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1commandsink1)
</dt> </dl>

 

