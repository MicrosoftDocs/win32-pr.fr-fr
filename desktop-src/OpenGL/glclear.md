---
title: fonction glClear (GL. h)
description: La fonction glClear efface les mémoires tampons à des valeurs prédéfinies.
ms.assetid: 9818f969-3145-45ea-aa9c-2abed953a8e0
keywords:
- glClear fonction OpenGL
topic_type:
- apiref
api_name:
- glClear
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0db935e46c65c42976024a8afbb98028294710c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510145"
---
# <a name="glclear-function"></a><span data-ttu-id="ce0de-104">glClear fonction)</span><span class="sxs-lookup"><span data-stu-id="ce0de-104">glClear function</span></span>

<span data-ttu-id="ce0de-105">La fonction **glClear** efface les mémoires tampons à des valeurs prédéfinies.</span><span class="sxs-lookup"><span data-stu-id="ce0de-105">The **glClear** function clears buffers to preset values.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce0de-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ce0de-106">Syntax</span></span>


```C++
void WINAPI glClear(
   GLbitfield mask
);
```



## <a name="parameters"></a><span data-ttu-id="ce0de-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ce0de-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce0de-108">*mask*</span><span class="sxs-lookup"><span data-stu-id="ce0de-108">*mask*</span></span> 
</dt> <dd>

<span data-ttu-id="ce0de-109">Opérateurs de bits or de masques qui indiquent les mémoires tampons à effacer.</span><span class="sxs-lookup"><span data-stu-id="ce0de-109">Bitwise OR operators of masks that indicate the buffers to be cleared.</span></span> <span data-ttu-id="ce0de-110">Les quatre masques sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="ce0de-110">The four masks are as follows.</span></span>



| <span data-ttu-id="ce0de-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="ce0de-111">Value</span></span>                                                                                                                                                                                   | <span data-ttu-id="ce0de-112">Signification</span><span class="sxs-lookup"><span data-stu-id="ce0de-112">Meaning</span></span>                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="GL_COLOR_BUFFER_BIT"></span><span id="gl_color_buffer_bit"></span><dl> <span data-ttu-id="ce0de-113"><dt>**\_bit de \_ mémoire tampon de couleur GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ce0de-113"><dt>**GL\_COLOR\_BUFFER\_BIT**</dt></span></span> </dl>       | <span data-ttu-id="ce0de-114">Mémoires tampons actuellement activées pour l’écriture de couleurs.</span><span class="sxs-lookup"><span data-stu-id="ce0de-114">The buffers currently enabled for color writing.</span></span><br/> |
| <span id="GL_DEPTH_BUFFER_BIT"></span><span id="gl_depth_buffer_bit"></span><dl> <span data-ttu-id="ce0de-115"><dt>**\_bit de \_ mémoire tampon de profondeur GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ce0de-115"><dt>**GL\_DEPTH\_BUFFER\_BIT**</dt></span></span> </dl>       | <span data-ttu-id="ce0de-116">Mémoire tampon de profondeur.</span><span class="sxs-lookup"><span data-stu-id="ce0de-116">The depth buffer.</span></span><br/>                                |
| <span id="GL_ACCUM_BUFFER_BIT"></span><span id="gl_accum_buffer_bit"></span><dl> <span data-ttu-id="ce0de-117"><dt>**\_bit de tampon amort \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ce0de-117"><dt>**GL\_ACCUM\_BUFFER\_BIT**</dt></span></span> </dl>       | <span data-ttu-id="ce0de-118">Mémoire tampon d’accumulation.</span><span class="sxs-lookup"><span data-stu-id="ce0de-118">The accumulation buffer.</span></span><br/>                         |
| <span id="GL_STENCIL_BUFFER_BIT"></span><span id="gl_stencil_buffer_bit"></span><dl> <span data-ttu-id="ce0de-119"><dt>**\_bit de \_ tampon de stencil du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ce0de-119"><dt>**GL\_STENCIL\_BUFFER\_BIT**</dt></span></span> </dl> | <span data-ttu-id="ce0de-120">Mémoire tampon de stencil.</span><span class="sxs-lookup"><span data-stu-id="ce0de-120">The stencil buffer.</span></span><br/>                              |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce0de-121">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ce0de-121">Return value</span></span>

<span data-ttu-id="ce0de-122">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="ce0de-122">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ce0de-123">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="ce0de-123">Error codes</span></span>

<span data-ttu-id="ce0de-124">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="ce0de-124">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="ce0de-125">Nom</span><span class="sxs-lookup"><span data-stu-id="ce0de-125">Name</span></span>                                                                                                  | <span data-ttu-id="ce0de-126">Signification</span><span class="sxs-lookup"><span data-stu-id="ce0de-126">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ce0de-127"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ce0de-127"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="ce0de-128">Tout bit autre que les quatre bits définis a été défini dans *Mask*.</span><span class="sxs-lookup"><span data-stu-id="ce0de-128">Any bit other than the four defined bits was set in *mask*.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="ce0de-129"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ce0de-129"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="ce0de-130">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="ce0de-130">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ce0de-131">Notes</span><span class="sxs-lookup"><span data-stu-id="ce0de-131">Remarks</span></span>

<span data-ttu-id="ce0de-132">La **fonction glClear** définit la zone Bitplane de la fenêtre sur les valeurs précédemment sélectionnées par [**glClearColor**](glclearcolor.md), [**glClearIndex**](glclearindex.md), [**glClearDepth**](glcleardepth.md), [**glClearStencil**](glclearstencil.md)et [**glClearAccum**](glclearaccum.md).</span><span class="sxs-lookup"><span data-stu-id="ce0de-132">The **glClear** function sets the bitplane area of the window to values previously selected by [**glClearColor**](glclearcolor.md), [**glClearIndex**](glclearindex.md), [**glClearDepth**](glcleardepth.md), [**glClearStencil**](glclearstencil.md), and [**glClearAccum**](glclearaccum.md).</span></span> <span data-ttu-id="ce0de-133">Vous pouvez effacer plusieurs mémoires tampons de couleurs simultanément en sélectionnant plusieurs mémoires tampons à la fois à l’aide de [**glDrawBuffer**](gldrawbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="ce0de-133">You can clear multiple color buffers simultaneously by selecting more than one buffer at a time using [**glDrawBuffer**](gldrawbuffer.md).</span></span>

<span data-ttu-id="ce0de-134">Le test de propriété en pixels, le test de ciseaux, le tramage et la mémoire tampon writemasks affectent le fonctionnement de **glClear**.</span><span class="sxs-lookup"><span data-stu-id="ce0de-134">The pixel-ownership test, the scissor test, dithering, and the buffer writemasks affect the operation of **glClear**.</span></span> <span data-ttu-id="ce0de-135">La zone de ciseaux délimite la région effacée.</span><span class="sxs-lookup"><span data-stu-id="ce0de-135">The scissor box bounds the cleared region.</span></span> <span data-ttu-id="ce0de-136">La fonction **glClear** ignore la fonction alpha, la fonction Blend, l’opération logique, le stencil, le mappage de texture et la mise en mémoire tampon *z*.</span><span class="sxs-lookup"><span data-stu-id="ce0de-136">The **glClear** function ignores the alpha function, blend function, logical operation, stenciling, texture mapping, and *z*-buffering.</span></span>

<span data-ttu-id="ce0de-137">La fonction **glClear** accepte un seul argument (*Mask*) qui est l’opération de bits or de plusieurs valeurs indiquant la mémoire tampon à effacer.</span><span class="sxs-lookup"><span data-stu-id="ce0de-137">The **glClear** function takes a single argument (*mask*) that is the bitwise OR of several values indicating which buffer is to be cleared.</span></span>

<span data-ttu-id="ce0de-138">La valeur à laquelle chaque mémoire tampon est désactivée dépend du paramètre de la valeur Clear de cette mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="ce0de-138">The value to which each buffer is cleared depends on the setting of the clear value for that buffer.</span></span>

<span data-ttu-id="ce0de-139">Si aucune mémoire tampon n’est présente, un appel **glClear** dirigé vers cette mémoire tampon n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="ce0de-139">If a buffer is not present, a **glClear** call directed at that buffer has no effect.</span></span>

<span data-ttu-id="ce0de-140">Les fonctions suivantes récupèrent les informations relatives à **glClear**:</span><span class="sxs-lookup"><span data-stu-id="ce0de-140">The following functions retrieve information related to **glClear**:</span></span>

<span data-ttu-id="ce0de-141">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Amort \_ Clear \_ value</span><span class="sxs-lookup"><span data-stu-id="ce0de-141">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_ACCUM\_CLEAR\_VALUE</span></span>

<span data-ttu-id="ce0de-142">**glGet** avec argument GL \_ profondeur \_ effacer la \_ valeur</span><span class="sxs-lookup"><span data-stu-id="ce0de-142">**glGet** with argument GL\_DEPTH\_CLEAR\_VALUE</span></span>

<span data-ttu-id="ce0de-143">**glGet** avec argument \_ \_ valeur Clear de l’index GL \_</span><span class="sxs-lookup"><span data-stu-id="ce0de-143">**glGet** with argument GL\_INDEX\_CLEAR\_VALUE</span></span>

<span data-ttu-id="ce0de-144">**glGet** avec argument \_ \_ valeur Clear de couleur GL \_</span><span class="sxs-lookup"><span data-stu-id="ce0de-144">**glGet** with argument GL\_COLOR\_CLEAR\_VALUE</span></span>

<span data-ttu-id="ce0de-145">**glGet** avec argument \_ \_ valeur Clear du stencil du GL \_</span><span class="sxs-lookup"><span data-stu-id="ce0de-145">**glGet** with argument GL\_STENCIL\_CLEAR\_VALUE</span></span>

## <a name="requirements"></a><span data-ttu-id="ce0de-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ce0de-146">Requirements</span></span>



| <span data-ttu-id="ce0de-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ce0de-147">Requirement</span></span> | <span data-ttu-id="ce0de-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="ce0de-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce0de-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ce0de-149">Minimum supported client</span></span><br/> | <span data-ttu-id="ce0de-150">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ce0de-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ce0de-151">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ce0de-151">Minimum supported server</span></span><br/> | <span data-ttu-id="ce0de-152">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ce0de-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ce0de-153">En-tête</span><span class="sxs-lookup"><span data-stu-id="ce0de-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce0de-154"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce0de-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="ce0de-155">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ce0de-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="ce0de-156"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ce0de-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ce0de-157">DLL</span><span class="sxs-lookup"><span data-stu-id="ce0de-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce0de-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce0de-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce0de-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ce0de-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce0de-160">**glClearAccum**</span><span class="sxs-lookup"><span data-stu-id="ce0de-160">**glClearAccum**</span></span>](glclearaccum.md)
</dt> <dt>

[<span data-ttu-id="ce0de-161">**glClearColor**</span><span class="sxs-lookup"><span data-stu-id="ce0de-161">**glClearColor**</span></span>](glclearcolor.md)
</dt> <dt>

[<span data-ttu-id="ce0de-162">**glClearDepth**</span><span class="sxs-lookup"><span data-stu-id="ce0de-162">**glClearDepth**</span></span>](glcleardepth.md)
</dt> <dt>

[<span data-ttu-id="ce0de-163">**glClearIndex**</span><span class="sxs-lookup"><span data-stu-id="ce0de-163">**glClearIndex**</span></span>](glclearindex.md)
</dt> <dt>

[<span data-ttu-id="ce0de-164">**glClearStencil**</span><span class="sxs-lookup"><span data-stu-id="ce0de-164">**glClearStencil**</span></span>](glclearstencil.md)
</dt> <dt>

[<span data-ttu-id="ce0de-165">**glDrawBuffer**</span><span class="sxs-lookup"><span data-stu-id="ce0de-165">**glDrawBuffer**</span></span>](gldrawbuffer.md)
</dt> <dt>

[<span data-ttu-id="ce0de-166">**glGet**</span><span class="sxs-lookup"><span data-stu-id="ce0de-166">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="ce0de-167">**glScissor**</span><span class="sxs-lookup"><span data-stu-id="ce0de-167">**glScissor**</span></span>](glscissor.md)
</dt> </dl>

 

 





