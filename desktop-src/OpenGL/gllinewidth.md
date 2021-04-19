---
title: fonction glLineWidth (GL. h)
description: La fonction glLineWidth spécifie la largeur des lignes pixellisées.
ms.assetid: 13a69fd7-5eee-42ec-bd05-5bd3c838d4d7
keywords:
- glLineWidth fonction OpenGL
topic_type:
- apiref
api_name:
- glLineWidth
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa4cecafc9e5d8e0f55c6e9d0dbfe49924d54f14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106518127"
---
# <a name="gllinewidth-function"></a><span data-ttu-id="1444e-104">glLineWidth fonction)</span><span class="sxs-lookup"><span data-stu-id="1444e-104">glLineWidth function</span></span>

<span data-ttu-id="1444e-105">La fonction **glLineWidth** spécifie la largeur des lignes pixellisées.</span><span class="sxs-lookup"><span data-stu-id="1444e-105">The **glLineWidth** function specifies the width of rasterized lines.</span></span>

## <a name="syntax"></a><span data-ttu-id="1444e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1444e-106">Syntax</span></span>


```C++
void WINAPI glLineWidth(
   GLfloat width
);
```



## <a name="parameters"></a><span data-ttu-id="1444e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1444e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1444e-108">*width*</span><span class="sxs-lookup"><span data-stu-id="1444e-108">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="1444e-109">Largeur des lignes pixellisées.</span><span class="sxs-lookup"><span data-stu-id="1444e-109">The width of rasterized lines.</span></span> <span data-ttu-id="1444e-110">La valeur par défaut est 1,0.</span><span class="sxs-lookup"><span data-stu-id="1444e-110">The default is 1.0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1444e-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1444e-111">Return value</span></span>

<span data-ttu-id="1444e-112">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="1444e-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1444e-113">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="1444e-113">Error codes</span></span>

<span data-ttu-id="1444e-114">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="1444e-114">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="1444e-115">Nom</span><span class="sxs-lookup"><span data-stu-id="1444e-115">Name</span></span>                                                                                                  | <span data-ttu-id="1444e-116">Signification</span><span class="sxs-lookup"><span data-stu-id="1444e-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1444e-117"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1444e-117"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="1444e-118">la *largeur* était inférieure ou égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="1444e-118">*width* was less than or equal to zero.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="1444e-119"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1444e-119"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="1444e-120">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="1444e-120">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="1444e-121">Notes</span><span class="sxs-lookup"><span data-stu-id="1444e-121">Remarks</span></span>

<span data-ttu-id="1444e-122">La fonction **glLineWidth** spécifie la largeur pixellisée des lignes avec et sans alias.</span><span class="sxs-lookup"><span data-stu-id="1444e-122">The **glLineWidth** function specifies the rasterized width of both aliased and antialiased lines.</span></span> <span data-ttu-id="1444e-123">L’utilisation d’une largeur de ligne autre que 1,0 a des effets différents, selon que l’anticrénelage de ligne est activé ou non.</span><span class="sxs-lookup"><span data-stu-id="1444e-123">Using a line width other than 1.0 has different effects, depending on whether line antialiasing is enabled.</span></span> <span data-ttu-id="1444e-124">L’anticrénelage de ligne est contrôlé en appelant [**glEnable**](glenable.md) et **glDisable** avec l’argument GL \_ line \_ Smooth.</span><span class="sxs-lookup"><span data-stu-id="1444e-124">Line antialiasing is controlled by calling [**glEnable**](glenable.md) and **glDisable** with argument GL\_LINE\_SMOOTH.</span></span>

<span data-ttu-id="1444e-125">Si l’anticrénelage de ligne est désactivé, la largeur réelle est déterminée en arrondissant la largeur fournie à l’entier le plus proche.</span><span class="sxs-lookup"><span data-stu-id="1444e-125">If line antialiasing is disabled, the actual width is determined by rounding the supplied width to the nearest integer.</span></span> <span data-ttu-id="1444e-126">(Si l’arrondi donne la valeur 0,0, c’est comme si la largeur de ligne était 1,0) Si \| ?</span><span class="sxs-lookup"><span data-stu-id="1444e-126">(If the rounding results in the value 0.0, it is as if the line width were 1.0) If \| ?</span></span> <span data-ttu-id="1444e-127">x \|  =  \| ?</span><span class="sxs-lookup"><span data-stu-id="1444e-127">x \| = \| ?</span></span> <span data-ttu-id="1444e-128">y \| , les pixels *i* sont remplis dans chaque colonne pixellisée, où *i* est la valeur arrondie de *Width*.</span><span class="sxs-lookup"><span data-stu-id="1444e-128">y \|, *i* pixels are filled in each column that is rasterized, where *i* is the rounded value of *width*.</span></span> <span data-ttu-id="1444e-129">Dans le cas *contraire, les* pixels sont remplis sur chaque ligne pixellisée.</span><span class="sxs-lookup"><span data-stu-id="1444e-129">Otherwise, *i* pixels are filled in each row that is rasterized.</span></span>

<span data-ttu-id="1444e-130">Si l’anticrénelage est activé, la pixellisation de ligne produit un fragment pour chaque carré de pixel qui croise la région située dans le rectangle dont la largeur est égale à la largeur de la ligne active, la longueur est égale à la longueur réelle de la ligne et est centrée sur le segment de ligne mathématique.</span><span class="sxs-lookup"><span data-stu-id="1444e-130">If antialiasing is enabled, line rasterization produces a fragment for each pixel square that intersects the region lying within the rectangle having width equal to the current line width, length equal to the actual length of the line, and centered on the mathematical line segment.</span></span> <span data-ttu-id="1444e-131">La valeur de couverture pour chaque fragment correspond à la zone de coordonnées de la fenêtre de l’intersection de la zone rectangulaire avec le carré de pixels correspondant.</span><span class="sxs-lookup"><span data-stu-id="1444e-131">The coverage value for each fragment is the window coordinate area of the intersection of the rectangular region with the corresponding pixel square.</span></span> <span data-ttu-id="1444e-132">Cette valeur est enregistrée et utilisée dans l’étape de pixellisation finale.</span><span class="sxs-lookup"><span data-stu-id="1444e-132">This value is saved and used in the final rasterization step.</span></span>

<span data-ttu-id="1444e-133">Toutes les largeurs ne peuvent pas être prises en charge lorsque l’anticrénelage de ligne est activé.</span><span class="sxs-lookup"><span data-stu-id="1444e-133">Not all widths can be supported when line antialiasing is enabled.</span></span> <span data-ttu-id="1444e-134">Si une largeur non prise en charge est demandée, la largeur la plus proche prise en charge est utilisée.</span><span class="sxs-lookup"><span data-stu-id="1444e-134">If an unsupported width is requested, the nearest supported width is used.</span></span> <span data-ttu-id="1444e-135">Seule la largeur 1,0 est garantie pour être prise en charge ; d’autres dépendent de l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="1444e-135">Only width 1.0 is guaranteed to be supported; others depend on the implementation.</span></span> <span data-ttu-id="1444e-136">Vous pouvez interroger la plage des largeurs prises en charge et la différence de taille entre les largeurs prises en charge au sein de la plage en appelant **glGet** avec les arguments \_ plage de largeur de ligne GL \_ \_ et largeur de \_ ligne GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="1444e-136">The range of supported widths and the size difference between supported widths within the range can be queried by calling **glGet** with arguments GL\_LINE\_WIDTH\_RANGE and GL\_LINE\_WIDTH\_GRANULARITY.</span></span>

<span data-ttu-id="1444e-137">La largeur de ligne spécifiée par **glLineWidth** est toujours retournée lorsque la \_ largeur de ligne GL \_ est interrogée.</span><span class="sxs-lookup"><span data-stu-id="1444e-137">The line width specified by **glLineWidth** is always returned when GL\_LINE\_WIDTH is queried.</span></span> <span data-ttu-id="1444e-138">Le verrouillage et l’arrondi pour les lignes avec et sans alias n’ont aucun effet sur la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="1444e-138">Clamping and rounding for aliased and antialiased lines have no effect on the specified value.</span></span>

<span data-ttu-id="1444e-139">La largeur de ligne non anticrénelage peut être ancrée à un maximum dépendant de l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="1444e-139">Non-antialiased line width may be clamped to an implementation-dependent maximum.</span></span> <span data-ttu-id="1444e-140">Même si ce nombre maximal ne peut pas être interrogé, il ne doit pas être inférieur à la valeur maximale pour les lignes avec un alias, arrondi à la valeur entière la plus proche.</span><span class="sxs-lookup"><span data-stu-id="1444e-140">Although this maximum cannot be queried, it must be no less than the maximum value for antialiased lines, rounded to the nearest integer value.</span></span>

<span data-ttu-id="1444e-141">Les fonctions suivantes récupèrent les informations relatives à **glLineWidth**:</span><span class="sxs-lookup"><span data-stu-id="1444e-141">The following functions retrieve information related to **glLineWidth**:</span></span>

<span data-ttu-id="1444e-142">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec l’argument \_ largeur de ligne du GL \_</span><span class="sxs-lookup"><span data-stu-id="1444e-142">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_LINE\_WIDTH</span></span>

<span data-ttu-id="1444e-143">**glGet** avec l’argument \_ \_ plage de largeur de ligne GL \_</span><span class="sxs-lookup"><span data-stu-id="1444e-143">**glGet** with argument GL\_LINE\_WIDTH\_RANGE</span></span>

<span data-ttu-id="1444e-144">**glGet** avec la \_ \_ granularité de la largeur de ligne de l’argument GL \_</span><span class="sxs-lookup"><span data-stu-id="1444e-144">**glGet** with argument GL\_LINE\_WIDTH\_GRANULARITY</span></span>

<span data-ttu-id="1444e-145">[**glIsEnabled**](glisenabled.md) avec argument GL \_ ligne \_ Smooth</span><span class="sxs-lookup"><span data-stu-id="1444e-145">[**glIsEnabled**](glisenabled.md) with argument GL\_LINE\_SMOOTH</span></span>

## <a name="requirements"></a><span data-ttu-id="1444e-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1444e-146">Requirements</span></span>



| <span data-ttu-id="1444e-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1444e-147">Requirement</span></span> | <span data-ttu-id="1444e-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="1444e-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1444e-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1444e-149">Minimum supported client</span></span><br/> | <span data-ttu-id="1444e-150">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1444e-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1444e-151">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1444e-151">Minimum supported server</span></span><br/> | <span data-ttu-id="1444e-152">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1444e-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1444e-153">En-tête</span><span class="sxs-lookup"><span data-stu-id="1444e-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="1444e-154"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="1444e-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="1444e-155">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1444e-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="1444e-156"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1444e-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="1444e-157">DLL</span><span class="sxs-lookup"><span data-stu-id="1444e-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1444e-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1444e-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1444e-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1444e-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1444e-160">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="1444e-160">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="1444e-161">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="1444e-161">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="1444e-162">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="1444e-162">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="1444e-163">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="1444e-163">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





