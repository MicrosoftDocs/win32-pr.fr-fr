---
title: gluBuild2DMipmaps, fonction (Glu. h)
description: La fonction gluBuild2DMipmaps crée des des mipmaps 2D.
ms.assetid: ea19a9b0-baf7-436f-afd5-609bc364b3ba
keywords:
- gluBuild2DMipmaps fonction OpenGL
topic_type:
- apiref
api_name:
- gluBuild2DMipmaps
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92402792e41701711e99f469ead67410d6a8c1b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941829"
---
# <a name="glubuild2dmipmaps-function"></a><span data-ttu-id="f1dcf-104">gluBuild2DMipmaps fonction)</span><span class="sxs-lookup"><span data-stu-id="f1dcf-104">gluBuild2DMipmaps function</span></span>

<span data-ttu-id="f1dcf-105">La fonction **gluBuild2DMipmaps** crée des des mipmaps 2D.</span><span class="sxs-lookup"><span data-stu-id="f1dcf-105">The **gluBuild2DMipmaps** function creates 2-D mipmaps.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1dcf-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f1dcf-106">Syntax</span></span>


```C++
void WINAPI gluBuild2DMipmaps(
         GLenum target,
         GLint  components,
         GLint  width,
         GLInt  height,
         GLenum format,
         GLenum type,
   const void   *data
);
```



## <a name="parameters"></a><span data-ttu-id="f1dcf-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f1dcf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1dcf-108">*cible*</span><span class="sxs-lookup"><span data-stu-id="f1dcf-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="f1dcf-109">Texture cible.</span><span class="sxs-lookup"><span data-stu-id="f1dcf-109">The target texture.</span></span> <span data-ttu-id="f1dcf-110">Doit être une \_ texture GL \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="f1dcf-110">Must be GL\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="f1dcf-111">*components*</span><span class="sxs-lookup"><span data-stu-id="f1dcf-111">*components*</span></span> 
</dt> <dd>

<span data-ttu-id="f1dcf-112">Nombre de composants de couleur dans la texture.</span><span class="sxs-lookup"><span data-stu-id="f1dcf-112">The number of color components in the texture.</span></span> <span data-ttu-id="f1dcf-113">Doit être 1, 2, 3 ou 4.</span><span class="sxs-lookup"><span data-stu-id="f1dcf-113">Must be 1, 2, 3, or 4.</span></span>

</dd> <dt>

<span data-ttu-id="f1dcf-114">*width*</span><span class="sxs-lookup"><span data-stu-id="f1dcf-114">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="f1dcf-115">Largeur de l’image de texture.</span><span class="sxs-lookup"><span data-stu-id="f1dcf-115">The width of the texture image.</span></span>

</dd> <dt>

<span data-ttu-id="f1dcf-116">*height*</span><span class="sxs-lookup"><span data-stu-id="f1dcf-116">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="f1dcf-117">Hauteur de l’image de texture.</span><span class="sxs-lookup"><span data-stu-id="f1dcf-117">The height of the texture image.</span></span>

</dd> <dt>

<span data-ttu-id="f1dcf-118">*format*</span><span class="sxs-lookup"><span data-stu-id="f1dcf-118">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="f1dcf-119">Format des données de pixels.</span><span class="sxs-lookup"><span data-stu-id="f1dcf-119">The format of the pixel data.</span></span> <span data-ttu-id="f1dcf-120">Il doit s’agir de l’un des éléments suivants : GL \_ Color \_ index, GL \_ Red, GL \_ Green, GL \_ Blue, GL \_ alpha, GL \_ RGB, GL \_ RVBA, GL \_ BGR \_ ext, GL \_ BGRA \_ ext, GL \_ luminance ou GL \_ luminance \_ alpha.</span><span class="sxs-lookup"><span data-stu-id="f1dcf-120">Must be one of the following: GL\_COLOR\_INDEX, GL\_RED, GL\_GREEN, GL\_BLUE, GL\_ALPHA, GL\_RGB, GL\_RGBA, GL\_BGR\_EXT, GL\_BGRA\_EXT, GL\_LUMINANCE, or GL\_LUMINANCE\_ALPHA.</span></span>

</dd> <dt>

<span data-ttu-id="f1dcf-121">*type*</span><span class="sxs-lookup"><span data-stu-id="f1dcf-121">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="f1dcf-122">Type de données pour les *données*.</span><span class="sxs-lookup"><span data-stu-id="f1dcf-122">The data type for *data*.</span></span> <span data-ttu-id="f1dcf-123">Il doit s’agir de l’une des valeurs suivantes : \_ octet non signé GL \_ , \_ octet GL, \_ bitmap GL, GL \_ non signé \_ short, GL \_ short, GL \_ unsigned \_ int, GL \_ int ou GL \_ float.</span><span class="sxs-lookup"><span data-stu-id="f1dcf-123">Must be one of the following: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_BITMAP, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, or GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="f1dcf-124">*data*</span><span class="sxs-lookup"><span data-stu-id="f1dcf-124">*data*</span></span> 
</dt> <dd>

<span data-ttu-id="f1dcf-125">Pointeur vers les données de l’image en mémoire.</span><span class="sxs-lookup"><span data-stu-id="f1dcf-125">A pointer to the image data in memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1dcf-126">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f1dcf-126">Return value</span></span>

<span data-ttu-id="f1dcf-127">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="f1dcf-127">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1dcf-128">Notes</span><span class="sxs-lookup"><span data-stu-id="f1dcf-128">Remarks</span></span>

<span data-ttu-id="f1dcf-129">La fonction **gluBuild2DMipmaps** obtient l’image d’entrée et génère toutes les images mipmap (à l’aide de [**gluScaleImage**](gluscaleimage.md)), de sorte que l’image d’entrée peut être utilisée comme image de texture mipmapped.</span><span class="sxs-lookup"><span data-stu-id="f1dcf-129">The **gluBuild2DMipmaps** function obtains the input image and generates all mipmap images (using [**gluScaleImage**](gluscaleimage.md)) so the input image can be used as a mipmapped texture image.</span></span> <span data-ttu-id="f1dcf-130">Pour charger chacune des images, appelez [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="f1dcf-130">To load each of the images, call [**glTexImage2D**](glteximage2d.md).</span></span> <span data-ttu-id="f1dcf-131">Si les dimensions de l’image d’entrée ne sont pas des puissances de deux, l’image est mise à l’échelle afin que la largeur et la hauteur soient des puissances de deux avant la génération des des mipmaps.</span><span class="sxs-lookup"><span data-stu-id="f1dcf-131">If the dimensions of the input image are not powers of two, then the image is scaled so that both the width and height are powers of two before the mipmaps are generated.</span></span>

<span data-ttu-id="f1dcf-132">Une valeur de retour de zéro indique une réussite.</span><span class="sxs-lookup"><span data-stu-id="f1dcf-132">A return value of zero indicates success.</span></span> <span data-ttu-id="f1dcf-133">Dans le cas contraire, un code d’erreur GLU est retourné (voir [**gluErrorString**](gluerrorstring.md)).</span><span class="sxs-lookup"><span data-stu-id="f1dcf-133">Otherwise, a GLU error code is returned (see [**gluErrorString**](gluerrorstring.md)).</span></span>

<span data-ttu-id="f1dcf-134">Pour obtenir une description des valeurs acceptables pour le paramètre *format* , consultez **glTexImage2D**.</span><span class="sxs-lookup"><span data-stu-id="f1dcf-134">For a description of the acceptable values for the *format* parameter, see **glTexImage2D**.</span></span> <span data-ttu-id="f1dcf-135">Pour obtenir une description des valeurs acceptables pour le *type*, consultez [**glDrawPixels**](gldrawpixels.md).</span><span class="sxs-lookup"><span data-stu-id="f1dcf-135">For a description of the acceptable values for *type*, see [**glDrawPixels**](gldrawpixels.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f1dcf-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f1dcf-136">Requirements</span></span>



| <span data-ttu-id="f1dcf-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f1dcf-137">Requirement</span></span> | <span data-ttu-id="f1dcf-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1dcf-138">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f1dcf-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f1dcf-139">Minimum supported client</span></span><br/> | <span data-ttu-id="f1dcf-140">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f1dcf-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f1dcf-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f1dcf-141">Minimum supported server</span></span><br/> | <span data-ttu-id="f1dcf-142">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f1dcf-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f1dcf-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="f1dcf-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1dcf-144"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1dcf-144"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="f1dcf-145">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f1dcf-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="f1dcf-146"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f1dcf-146"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f1dcf-147">DLL</span><span class="sxs-lookup"><span data-stu-id="f1dcf-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1dcf-148"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1dcf-148"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1dcf-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f1dcf-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1dcf-150">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="f1dcf-150">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="f1dcf-151">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="f1dcf-151">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="f1dcf-152">**gluBuild1DMipmaps**</span><span class="sxs-lookup"><span data-stu-id="f1dcf-152">**gluBuild1DMipmaps**</span></span>](glubuild1dmipmaps.md)
</dt> <dt>

[<span data-ttu-id="f1dcf-153">**gluScaleImage**</span><span class="sxs-lookup"><span data-stu-id="f1dcf-153">**gluScaleImage**</span></span>](gluscaleimage.md)
</dt> </dl>

 

 





