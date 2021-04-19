---
title: gluBuild1DMipmaps, fonction (Glu. h)
description: La fonction gluBuild1DMipmaps crée des des mipmaps 1D.
ms.assetid: 52ed924f-7a72-4458-b1b8-8e5d3021f60a
keywords:
- gluBuild1DMipmaps fonction OpenGL
topic_type:
- apiref
api_name:
- gluBuild1DMipmaps
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 089357488c7eae18e26258018473e9008fb29d24
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510129"
---
# <a name="glubuild1dmipmaps-function"></a><span data-ttu-id="3c6c7-104">gluBuild1DMipmaps fonction)</span><span class="sxs-lookup"><span data-stu-id="3c6c7-104">gluBuild1DMipmaps function</span></span>

<span data-ttu-id="3c6c7-105">La fonction **gluBuild1DMipmaps** crée des des mipmaps 1D.</span><span class="sxs-lookup"><span data-stu-id="3c6c7-105">The **gluBuild1DMipmaps** function creates 1-D mipmaps.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c6c7-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3c6c7-106">Syntax</span></span>


```C++
void WINAPI gluBuild1DMipmaps(
         GLenum target,
         GLint  components,
         GLint  width,
         GLenum format,
         GLenum type,
   const void   *data
);
```



## <a name="parameters"></a><span data-ttu-id="3c6c7-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3c6c7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c6c7-108">*cible*</span><span class="sxs-lookup"><span data-stu-id="3c6c7-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="3c6c7-109">Texture cible.</span><span class="sxs-lookup"><span data-stu-id="3c6c7-109">The target texture.</span></span> <span data-ttu-id="3c6c7-110">Doit être une \_ texture GL \_ 1D.</span><span class="sxs-lookup"><span data-stu-id="3c6c7-110">Must be GL\_TEXTURE\_1D.</span></span>

</dd> <dt>

<span data-ttu-id="3c6c7-111">*components*</span><span class="sxs-lookup"><span data-stu-id="3c6c7-111">*components*</span></span> 
</dt> <dd>

<span data-ttu-id="3c6c7-112">Nombre de composants de couleur dans la texture.</span><span class="sxs-lookup"><span data-stu-id="3c6c7-112">The number of color components in the texture.</span></span> <span data-ttu-id="3c6c7-113">Doit être 1, 2, 3 ou 4.</span><span class="sxs-lookup"><span data-stu-id="3c6c7-113">Must be 1, 2, 3, or 4.</span></span>

</dd> <dt>

<span data-ttu-id="3c6c7-114">*width*</span><span class="sxs-lookup"><span data-stu-id="3c6c7-114">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="3c6c7-115">Largeur de l’image de texture.</span><span class="sxs-lookup"><span data-stu-id="3c6c7-115">The width of the texture image.</span></span>

</dd> <dt>

<span data-ttu-id="3c6c7-116">*format*</span><span class="sxs-lookup"><span data-stu-id="3c6c7-116">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="3c6c7-117">Format des données de pixels.</span><span class="sxs-lookup"><span data-stu-id="3c6c7-117">The format of the pixel data.</span></span> <span data-ttu-id="3c6c7-118">Les valeurs suivantes sont valides : GL \_ Color \_ index, GL \_ Red, GL \_ Green, GL \_ Blue, GL \_ alpha, GL \_ RGB, GL \_ RVBA, GL \_ BGR \_ ext, GL \_ BGRA \_ ext, GL \_ luminance ou GL \_ luminance \_ alpha.</span><span class="sxs-lookup"><span data-stu-id="3c6c7-118">The following values are valid: GL\_COLOR\_INDEX, GL\_RED, GL\_GREEN, GL\_BLUE, GL\_ALPHA, GL\_RGB, GL\_RGBA, GL\_BGR\_EXT, GL\_BGRA\_EXT, GL\_LUMINANCE, or GL\_LUMINANCE\_ALPHA.</span></span>

</dd> <dt>

<span data-ttu-id="3c6c7-119">*type*</span><span class="sxs-lookup"><span data-stu-id="3c6c7-119">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="3c6c7-120">Type de données pour les *données*.</span><span class="sxs-lookup"><span data-stu-id="3c6c7-120">The data type for *data*.</span></span> <span data-ttu-id="3c6c7-121">Les valeurs suivantes sont valides : \_ octet non signé GL \_ , \_ octet GL, bitmap GL \_ , GL \_ non signé \_ short, GL \_ short, GL \_ unsigned \_ int, GL \_ int ou GL \_ float.</span><span class="sxs-lookup"><span data-stu-id="3c6c7-121">The following values are valid: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_BITMAP, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, or GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="3c6c7-122">*data*</span><span class="sxs-lookup"><span data-stu-id="3c6c7-122">*data*</span></span> 
</dt> <dd>

<span data-ttu-id="3c6c7-123">Pointeur vers les données de l’image en mémoire.</span><span class="sxs-lookup"><span data-stu-id="3c6c7-123">A pointer to the image data in memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c6c7-124">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3c6c7-124">Return value</span></span>

<span data-ttu-id="3c6c7-125">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="3c6c7-125">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c6c7-126">Notes</span><span class="sxs-lookup"><span data-stu-id="3c6c7-126">Remarks</span></span>

<span data-ttu-id="3c6c7-127">La fonction **gluBuild1DMipmaps** obtient l’image d’entrée et génère toutes les images mipmap (à l’aide de [**gluScaleImage**](gluscaleimage.md)) afin que l’image d’entrée puisse être utilisée comme image de texture mipmapped.</span><span class="sxs-lookup"><span data-stu-id="3c6c7-127">The **gluBuild1DMipmaps** function obtains the input image and generates all mipmap images (using [**gluScaleImage**](gluscaleimage.md)) so that the input image can be used as a mipmapped texture image.</span></span> <span data-ttu-id="3c6c7-128">La fonction [**glTexImage1D**](glteximage1d.md) est ensuite appelée pour charger chacune des images.</span><span class="sxs-lookup"><span data-stu-id="3c6c7-128">The [**glTexImage1D**](glteximage1d.md) function is then called to load each of the images.</span></span> <span data-ttu-id="3c6c7-129">Si la largeur de l’image d’entrée n’est pas une puissance de deux, l’image est mise à l’échelle à la puissance de deux la plus proche pour que les des mipmaps soient générés.</span><span class="sxs-lookup"><span data-stu-id="3c6c7-129">If the width of the input image is not a power of two, then the image is scaled to the nearest power of two before the mipmaps are generated.</span></span>

<span data-ttu-id="3c6c7-130">Une valeur de retour de zéro indique une réussite.</span><span class="sxs-lookup"><span data-stu-id="3c6c7-130">A return value of zero indicates success.</span></span> <span data-ttu-id="3c6c7-131">Dans le cas contraire, un code d’erreur GLU est retourné (voir [**gluErrorString**](gluerrorstring.md)).</span><span class="sxs-lookup"><span data-stu-id="3c6c7-131">Otherwise, a GLU error code is returned (see [**gluErrorString**](gluerrorstring.md)).</span></span>

<span data-ttu-id="3c6c7-132">Pour obtenir une description des valeurs acceptables pour le paramètre *format* , consultez **glTexImage1D**.</span><span class="sxs-lookup"><span data-stu-id="3c6c7-132">For a description of the acceptable values for the *format* parameter, see **glTexImage1D**.</span></span> <span data-ttu-id="3c6c7-133">Pour obtenir une description des valeurs acceptables pour le paramètre de *type* , consultez [**glDrawPixels**](gldrawpixels.md).</span><span class="sxs-lookup"><span data-stu-id="3c6c7-133">For a description of the acceptable values for the *type* parameter, see [**glDrawPixels**](gldrawpixels.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3c6c7-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3c6c7-134">Requirements</span></span>



| <span data-ttu-id="3c6c7-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3c6c7-135">Requirement</span></span> | <span data-ttu-id="3c6c7-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="3c6c7-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3c6c7-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c6c7-137">Minimum supported client</span></span><br/> | <span data-ttu-id="3c6c7-138">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3c6c7-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="3c6c7-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c6c7-139">Minimum supported server</span></span><br/> | <span data-ttu-id="3c6c7-140">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3c6c7-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="3c6c7-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="3c6c7-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c6c7-142"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c6c7-142"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="3c6c7-143">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3c6c7-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="3c6c7-144"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c6c7-144"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="3c6c7-145">DLL</span><span class="sxs-lookup"><span data-stu-id="3c6c7-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c6c7-146"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c6c7-146"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c6c7-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c6c7-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c6c7-148">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="3c6c7-148">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="3c6c7-149">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="3c6c7-149">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="3c6c7-150">**gluBuild2DMipmaps**</span><span class="sxs-lookup"><span data-stu-id="3c6c7-150">**gluBuild2DMipmaps**</span></span>](glubuild2dmipmaps.md)
</dt> <dt>

[<span data-ttu-id="3c6c7-151">**gluScaleImage**</span><span class="sxs-lookup"><span data-stu-id="3c6c7-151">**gluScaleImage**</span></span>](gluscaleimage.md)
</dt> </dl>

 

 





