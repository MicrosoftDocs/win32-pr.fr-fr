---
title: gluScaleImage, fonction (Glu. h)
description: La fonction gluScaleImage met à l’échelle une image à une taille arbitraire.
ms.assetid: f47191e8-b22d-4f6a-949a-9c7782d6d338
keywords:
- gluScaleImage fonction OpenGL
topic_type:
- apiref
api_name:
- gluScaleImage
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7da95f1545996a83adeb27deaceb7fab6290005e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383836"
---
# <a name="gluscaleimage-function"></a><span data-ttu-id="c0766-104">gluScaleImage fonction)</span><span class="sxs-lookup"><span data-stu-id="c0766-104">gluScaleImage function</span></span>

<span data-ttu-id="c0766-105">La fonction **gluScaleImage** met à l’échelle une image à une taille arbitraire.</span><span class="sxs-lookup"><span data-stu-id="c0766-105">The **gluScaleImage** function scales an image to an arbitrary size.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0766-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c0766-106">Syntax</span></span>


```C++
int WINAPI gluScaleImage(
         GLenum format,
         GLint  widthin,
         GLint  heightin,
         GLenum typein,
   const void   *datain,
         GLint  widthout,
         GLint  heightout,
         GLenum typeout,
         void   *dataout
);
```



## <a name="parameters"></a><span data-ttu-id="c0766-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c0766-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0766-108">*format*</span><span class="sxs-lookup"><span data-stu-id="c0766-108">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="c0766-109">Format des données de pixels.</span><span class="sxs-lookup"><span data-stu-id="c0766-109">The format of the pixel data.</span></span> <span data-ttu-id="c0766-110">Les valeurs symboliques suivantes sont valides \_ : \_ index de couleur GL, \_ index de stencils GL \_ , \_ \_ composant de profondeur GL, comptabilité GL \_ , vert GL, bleu GL, GL \_ \_ \_ alpha, GL \_ RVB, GL \_ RVBA, GL \_ BGR \_ ext, GL \_ BGRA \_ ext, luminance du GL \_ et \_ luminance alpha du GL \_ .</span><span class="sxs-lookup"><span data-stu-id="c0766-110">The following symbolic values are valid: GL\_COLOR\_INDEX, GL\_STENCIL\_INDEX, GL\_DEPTH\_COMPONENT, GL\_RED, GL\_GREEN, GL\_BLUE, GL\_ALPHA, GL\_RGB, GL\_RGBA, GL\_BGR\_EXT, GL\_BGRA\_EXT, GL\_LUMINANCE, and GL\_LUMINANCE\_ALPHA.</span></span>

</dd> <dt>

<span data-ttu-id="c0766-111">*largeur*</span><span class="sxs-lookup"><span data-stu-id="c0766-111">*widthin*</span></span> 
</dt> <dd>

<span data-ttu-id="c0766-112">Largeur de l’image source qui est mise à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="c0766-112">The width of the source image that is scaled.</span></span>

</dd> <dt>

<span data-ttu-id="c0766-113">*hauteur*</span><span class="sxs-lookup"><span data-stu-id="c0766-113">*heightin*</span></span> 
</dt> <dd>

<span data-ttu-id="c0766-114">Hauteur de l’image source qui est mise à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="c0766-114">The height of the source image that is scaled.</span></span>

</dd> <dt>

<span data-ttu-id="c0766-115">*type*</span><span class="sxs-lookup"><span data-stu-id="c0766-115">*typein*</span></span> 
</dt> <dd>

<span data-ttu-id="c0766-116">Type de données pour la *donnée*.</span><span class="sxs-lookup"><span data-stu-id="c0766-116">The data type for *datain*.</span></span> <span data-ttu-id="c0766-117">Il doit s’agir de l’une des valeurs suivantes : \_ octet non signé GL \_ , \_ octet GL, \_ bitmap GL, GL \_ non signé \_ short, GL \_ short, GL \_ unsigned \_ int, GL \_ int ou GL \_ float.</span><span class="sxs-lookup"><span data-stu-id="c0766-117">Must be one of the following: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_BITMAP, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, or GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="c0766-118">*données*</span><span class="sxs-lookup"><span data-stu-id="c0766-118">*datain*</span></span> 
</dt> <dd>

<span data-ttu-id="c0766-119">Pointeur vers l’image source.</span><span class="sxs-lookup"><span data-stu-id="c0766-119">A pointer to the source image.</span></span>

</dd> <dt>

<span data-ttu-id="c0766-120">*widthout*</span><span class="sxs-lookup"><span data-stu-id="c0766-120">*widthout*</span></span> 
</dt> <dd>

<span data-ttu-id="c0766-121">Largeur de l’image de destination.</span><span class="sxs-lookup"><span data-stu-id="c0766-121">The width of the destination image.</span></span>

</dd> <dt>

<span data-ttu-id="c0766-122">*heightout*</span><span class="sxs-lookup"><span data-stu-id="c0766-122">*heightout*</span></span> 
</dt> <dd>

<span data-ttu-id="c0766-123">Hauteur de l’image de destination.</span><span class="sxs-lookup"><span data-stu-id="c0766-123">The height of the destination image.</span></span>

</dd> <dt>

<span data-ttu-id="c0766-124">*typeout*</span><span class="sxs-lookup"><span data-stu-id="c0766-124">*typeout*</span></span> 
</dt> <dd>

<span data-ttu-id="c0766-125">Type de données pour *dataout*.</span><span class="sxs-lookup"><span data-stu-id="c0766-125">The data type for *dataout*.</span></span> <span data-ttu-id="c0766-126">Il doit s’agir de l’une des valeurs suivantes : \_ octet non signé GL \_ , \_ octet GL, \_ bitmap GL, GL \_ non signé \_ short, GL \_ short, GL \_ unsigned \_ int, GL \_ int ou GL \_ float.</span><span class="sxs-lookup"><span data-stu-id="c0766-126">Must be one of the following: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_BITMAP, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, or GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="c0766-127">*dataout*</span><span class="sxs-lookup"><span data-stu-id="c0766-127">*dataout*</span></span> 
</dt> <dd>

<span data-ttu-id="c0766-128">Pointeur vers l’image de destination.</span><span class="sxs-lookup"><span data-stu-id="c0766-128">A pointer to the destination image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0766-129">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c0766-129">Return value</span></span>

<span data-ttu-id="c0766-130">Si la fonction aboutit, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="c0766-130">If the function succeeds, the return value is zero.</span></span>

<span data-ttu-id="c0766-131">Si la fonction échoue, la valeur de retour est un code d’erreur GLU (consultez [**gluErrorString**](gluerrorstring.md)).</span><span class="sxs-lookup"><span data-stu-id="c0766-131">If the function fails, the return value is a GLU error code (see [**gluErrorString**](gluerrorstring.md)).</span></span>

## <a name="remarks"></a><span data-ttu-id="c0766-132">Notes</span><span class="sxs-lookup"><span data-stu-id="c0766-132">Remarks</span></span>

<span data-ttu-id="c0766-133">La fonction **gluScaleImage** met à l’échelle une image de pixel en utilisant les modes de stockage de pixels appropriés pour décompresser les données de l’image source et les données de package dans l’image de destination.</span><span class="sxs-lookup"><span data-stu-id="c0766-133">The **gluScaleImage** function scales a pixel image using the appropriate pixel store modes to unpack data from the source image and pack data into the destination image.</span></span>

<span data-ttu-id="c0766-134">Lors de la réduction d’une image, **gluScaleImage** utilise un filtre de zone pour échantillonner l’image source et créer des pixels pour l’image de destination.</span><span class="sxs-lookup"><span data-stu-id="c0766-134">When shrinking an image, **gluScaleImage** uses a box filter to sample the source image and create pixels for the destination image.</span></span> <span data-ttu-id="c0766-135">Lors de l’agrandissement d’une image, les pixels de l’image source sont interpolés de manière linéaire pour créer l’image de destination.</span><span class="sxs-lookup"><span data-stu-id="c0766-135">When magnifying an image, the pixels from the source image are linearly interpolated to create the destination image.</span></span>

<span data-ttu-id="c0766-136">Pour obtenir une description des valeurs acceptables pour les paramètres *format*, *type* et *typeout* , consultez [**glReadPixels**](glreadpixels.md).</span><span class="sxs-lookup"><span data-stu-id="c0766-136">For a description of the acceptable values for the *format*, *typein*, and *typeout* parameters, see [**glReadPixels**](glreadpixels.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c0766-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0766-137">Requirements</span></span>



| <span data-ttu-id="c0766-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c0766-138">Requirement</span></span> | <span data-ttu-id="c0766-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="c0766-139">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c0766-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c0766-140">Minimum supported client</span></span><br/> | <span data-ttu-id="c0766-141">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c0766-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="c0766-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c0766-142">Minimum supported server</span></span><br/> | <span data-ttu-id="c0766-143">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c0766-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c0766-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="c0766-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0766-145"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0766-145"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="c0766-146">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c0766-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="c0766-147"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c0766-147"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="c0766-148">DLL</span><span class="sxs-lookup"><span data-stu-id="c0766-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0766-149"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0766-149"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0766-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0766-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0766-151">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="c0766-151">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="c0766-152">**glReadPixels**</span><span class="sxs-lookup"><span data-stu-id="c0766-152">**glReadPixels**</span></span>](glreadpixels.md)
</dt> <dt>

[<span data-ttu-id="c0766-153">**gluBuild1DMipmaps**</span><span class="sxs-lookup"><span data-stu-id="c0766-153">**gluBuild1DMipmaps**</span></span>](glubuild1dmipmaps.md)
</dt> <dt>

[<span data-ttu-id="c0766-154">**gluBuild2DMipmaps**</span><span class="sxs-lookup"><span data-stu-id="c0766-154">**gluBuild2DMipmaps**</span></span>](glubuild2dmipmaps.md)
</dt> <dt>

[<span data-ttu-id="c0766-155">**gluErrorString**</span><span class="sxs-lookup"><span data-stu-id="c0766-155">**gluErrorString**</span></span>](gluerrorstring.md)
</dt> </dl>

 

 





