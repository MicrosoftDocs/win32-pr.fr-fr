---
title: fonction glPixelZoom (GL. h)
description: La fonction glPixelZoom spécifie les facteurs de zoom de pixel.
ms.assetid: 57ead7d8-0502-46b4-9f66-dbb3cb75b0f9
keywords:
- glPixelZoom fonction OpenGL
topic_type:
- apiref
api_name:
- glPixelZoom
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 065e1735ca0228046cfb08e2fb441d3cdc02af74
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "106522490"
---
# <a name="glpixelzoom-function"></a><span data-ttu-id="457ea-104">glPixelZoom fonction)</span><span class="sxs-lookup"><span data-stu-id="457ea-104">glPixelZoom function</span></span>

<span data-ttu-id="457ea-105">La fonction **glPixelZoom** spécifie les facteurs de zoom de pixel.</span><span class="sxs-lookup"><span data-stu-id="457ea-105">The **glPixelZoom** function specifies the pixel zoom factors.</span></span>

## <a name="syntax"></a><span data-ttu-id="457ea-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="457ea-106">Syntax</span></span>


```C++
void WINAPI glPixelZoom(
   GLfloat xfactor,
   GLfloat yfactor
);
```



## <a name="parameters"></a><span data-ttu-id="457ea-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="457ea-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="457ea-108">*xfactor*</span><span class="sxs-lookup"><span data-stu-id="457ea-108">*xfactor*</span></span> 
</dt> <dd>

<span data-ttu-id="457ea-109">Facteur de zoom *x* pour les opérations d’écriture de pixels.</span><span class="sxs-lookup"><span data-stu-id="457ea-109">The *x* zoom factor for pixel write operations.</span></span>

</dd> <dt>

<span data-ttu-id="457ea-110">*yfactor*</span><span class="sxs-lookup"><span data-stu-id="457ea-110">*yfactor*</span></span> 
</dt> <dd>

<span data-ttu-id="457ea-111">Facteur de zoom *y* pour les opérations d’écriture de pixels.</span><span class="sxs-lookup"><span data-stu-id="457ea-111">The *y* zoom factor for pixel write operations.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="457ea-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="457ea-112">Return value</span></span>

<span data-ttu-id="457ea-113">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="457ea-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="457ea-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="457ea-114">Error codes</span></span>

<span data-ttu-id="457ea-115">Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="457ea-115">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="457ea-116">Nom</span><span class="sxs-lookup"><span data-stu-id="457ea-116">Name</span></span>                                                                                                  | <span data-ttu-id="457ea-117">Signification</span><span class="sxs-lookup"><span data-stu-id="457ea-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="457ea-118"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="457ea-118"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="457ea-119">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="457ea-119">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="457ea-120">Notes</span><span class="sxs-lookup"><span data-stu-id="457ea-120">Remarks</span></span>

<span data-ttu-id="457ea-121">La fonction **glPixelZoom** spécifie des valeurs pour les facteurs de zoom *x* et *y* .</span><span class="sxs-lookup"><span data-stu-id="457ea-121">The **glPixelZoom** function specifies values for the *x* and *y* zoom factors.</span></span> <span data-ttu-id="457ea-122">Pendant l’exécution de [**glDrawPixels**](gldrawpixels.md) ou [**glCopyPixels**](glcopypixels.md), si (*x*<sub>r</sub> ,*y*<sub>r</sub> ) est la position raster actuelle, et qu’un élément donné se trouve dans la *n* *ième ligne et la* énième colonne du rectangle de pixels, alors les pixels dont les centres se trouvent dans le rectangle avec des angles à</span><span class="sxs-lookup"><span data-stu-id="457ea-122">During the execution of [**glDrawPixels**](gldrawpixels.md) or [**glCopyPixels**](glcopypixels.md), if (*x*<sub>r</sub> ,*y*<sub>r</sub> ) is the current raster position, and a given element is in the *n* th row and *m* th column of the pixel rectangle, then pixels whose centers are in the rectangle with corners at</span></span>

![Équation représentant les emplacements où les pixels sont candidats au remplacement.](images/pix05.png)

<span data-ttu-id="457ea-124">sont des candidats au remplacement.</span><span class="sxs-lookup"><span data-stu-id="457ea-124">are candidates for replacement.</span></span> <span data-ttu-id="457ea-125">Tout pixel dont le Centre se trouve sur le bord inférieur ou gauche de cette zone rectangulaire est également modifié.</span><span class="sxs-lookup"><span data-stu-id="457ea-125">Any pixel whose center lies on the bottom or left edge of this rectangular region is also modified.</span></span>

<span data-ttu-id="457ea-126">Les facteurs de zoom de pixel ne sont pas limités aux valeurs positives.</span><span class="sxs-lookup"><span data-stu-id="457ea-126">Pixel zoom factors are not limited to positive values.</span></span> <span data-ttu-id="457ea-127">Les facteurs de zoom négatifs reflètent l’image résultante sur la position de la trame actuelle.</span><span class="sxs-lookup"><span data-stu-id="457ea-127">Negative zoom factors reflect the resulting image about the current raster position.</span></span>

<span data-ttu-id="457ea-128">Les fonctions suivantes récupèrent les informations relatives à **glPixelZoom**:</span><span class="sxs-lookup"><span data-stu-id="457ea-128">The following functions retrieve information related to **glPixelZoom**:</span></span>

<span data-ttu-id="457ea-129">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Zoom \_ X</span><span class="sxs-lookup"><span data-stu-id="457ea-129">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_ZOOM\_X</span></span>

<span data-ttu-id="457ea-130">**glGet** avec argument GL \_ Zoom \_ Y</span><span class="sxs-lookup"><span data-stu-id="457ea-130">**glGet** with argument GL\_ZOOM\_Y</span></span>

## <a name="requirements"></a><span data-ttu-id="457ea-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="457ea-131">Requirements</span></span>



| <span data-ttu-id="457ea-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="457ea-132">Requirement</span></span> | <span data-ttu-id="457ea-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="457ea-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="457ea-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="457ea-134">Minimum supported client</span></span><br/> | <span data-ttu-id="457ea-135">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="457ea-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="457ea-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="457ea-136">Minimum supported server</span></span><br/> | <span data-ttu-id="457ea-137">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="457ea-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="457ea-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="457ea-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="457ea-139"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="457ea-139"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="457ea-140">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="457ea-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="457ea-141"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="457ea-141"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="457ea-142">DLL</span><span class="sxs-lookup"><span data-stu-id="457ea-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="457ea-143"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="457ea-143"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="457ea-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="457ea-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="457ea-145">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="457ea-145">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="457ea-146">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="457ea-146">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="457ea-147">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="457ea-147">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="457ea-148">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="457ea-148">**glEnd**</span></span>](glend.md)
</dt> </dl>

 

 





