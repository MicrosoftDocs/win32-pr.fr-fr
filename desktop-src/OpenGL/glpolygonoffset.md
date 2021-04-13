---
title: fonction glPolygonOffset (GL. h)
description: La fonction glPolygonOffset définit l’échelle et les unités que OpenGL utilise pour calculer les valeurs de profondeur.
ms.assetid: 06bc1aba-1692-40f0-8535-2cb65b487490
keywords:
- glPolygonOffset fonction OpenGL
topic_type:
- apiref
api_name:
- glPolygonOffset
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84fa7d130fcc300fc1ebe33d091253e33f2d1e03
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384812"
---
# <a name="glpolygonoffset-function"></a><span data-ttu-id="47ca8-104">glPolygonOffset fonction)</span><span class="sxs-lookup"><span data-stu-id="47ca8-104">glPolygonOffset function</span></span>

<span data-ttu-id="47ca8-105">La fonction **glPolygonOffset** définit l’échelle et les unités que OpenGL utilise pour calculer les valeurs de profondeur.</span><span class="sxs-lookup"><span data-stu-id="47ca8-105">The **glPolygonOffset** function sets the scale and units OpenGL uses to calculate depth values.</span></span>

## <a name="syntax"></a><span data-ttu-id="47ca8-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="47ca8-106">Syntax</span></span>


```C++
void WINAPI glPolygonOffset(
   GLfloat factor,
   GLfloat units
);
```



## <a name="parameters"></a><span data-ttu-id="47ca8-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="47ca8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47ca8-108">*factorisés*</span><span class="sxs-lookup"><span data-stu-id="47ca8-108">*factor*</span></span> 
</dt> <dd>

<span data-ttu-id="47ca8-109">Spécifie un facteur d’échelle qui est utilisé pour créer un décalage de profondeur variable pour chaque polygone.</span><span class="sxs-lookup"><span data-stu-id="47ca8-109">Specifies a scale factor that is used to create a variable depth offset for each polygon.</span></span> <span data-ttu-id="47ca8-110">La valeur initiale est zéro.</span><span class="sxs-lookup"><span data-stu-id="47ca8-110">The initial value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="47ca8-111">*sections*</span><span class="sxs-lookup"><span data-stu-id="47ca8-111">*units*</span></span> 
</dt> <dd>

<span data-ttu-id="47ca8-112">Spécifie une valeur qui est multipliée par une valeur spécifique à l’implémentation pour créer un décalage de profondeur constante.</span><span class="sxs-lookup"><span data-stu-id="47ca8-112">Specifies a value that is multiplied by an implementation-specific value to create a constant depth offset.</span></span> <span data-ttu-id="47ca8-113">La valeur initiale est 0.</span><span class="sxs-lookup"><span data-stu-id="47ca8-113">The initial value is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47ca8-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="47ca8-114">Return value</span></span>

<span data-ttu-id="47ca8-115">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="47ca8-115">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="47ca8-116">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="47ca8-116">Error codes</span></span>

<span data-ttu-id="47ca8-117">Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="47ca8-117">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="47ca8-118">Nom</span><span class="sxs-lookup"><span data-stu-id="47ca8-118">Name</span></span>                                                                                                  | <span data-ttu-id="47ca8-119">Signification</span><span class="sxs-lookup"><span data-stu-id="47ca8-119">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="47ca8-120"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="47ca8-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="47ca8-121">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="47ca8-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="47ca8-122">Notes</span><span class="sxs-lookup"><span data-stu-id="47ca8-122">Remarks</span></span>

<span data-ttu-id="47ca8-123">Lorsque \_ \_ l’option décalage du polygone GL est activée, la valeur de profondeur de chaque fragment sera décalée après avoir été interpolée à partir des valeurs de profondeur des vertex appropriés.</span><span class="sxs-lookup"><span data-stu-id="47ca8-123">When GL\_POLYGON\_OFFSET is enabled, each fragment's depth value will be offset after it is interpolated from the depth values of the appropriate vertices.</span></span> <span data-ttu-id="47ca8-124">La valeur du décalage est unités *Factor* \* ? z + r \* , où ? z est une mesure du changement de profondeur par rapport à la zone d’écran du polygone, et r est la plus petite valeur qui est garantie pour produire un offset pouvant être résolu pour une implémentation donnée.</span><span class="sxs-lookup"><span data-stu-id="47ca8-124">The value of the offset is *factor* \* ?z + r \**units*, where ?z is a measurement of the change in depth relative to the screen area of the polygon, and r is the smallest value that is guaranteed to produce a resolvable offset for a given implementation.</span></span> <span data-ttu-id="47ca8-125">Le décalage est ajouté avant l’exécution du test de profondeur et avant que la valeur ne soit écrite dans la mémoire tampon de profondeur.</span><span class="sxs-lookup"><span data-stu-id="47ca8-125">The offset is added before the depth test is performed and before the value is written into the depth buffer.</span></span>

<span data-ttu-id="47ca8-126">La fonction **glPolygonOffset** est utile pour afficher des images de ligne masquée, pour appliquer des dépassements aux surfaces et pour le rendu de solides avec des bords en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="47ca8-126">The **glPolygonOffset** function is useful for rendering hidden-line images, for applying decals to surfaces, and for rendering solids with highlighted edges.</span></span>

<span data-ttu-id="47ca8-127">La fonction **glPolygonOffset** n’a aucun effet sur les coordonnées de profondeur placées dans la mémoire tampon de commentaires.</span><span class="sxs-lookup"><span data-stu-id="47ca8-127">The **glPolygonOffset** function has no effect on depth coordinates placed in the feedback buffer.</span></span> <span data-ttu-id="47ca8-128">Elle n’a pas non plus d’effet sur la sélection.</span><span class="sxs-lookup"><span data-stu-id="47ca8-128">It also has no effect on selection.</span></span>

<span data-ttu-id="47ca8-129">Les fonctions suivantes récupèrent les informations relatives à **glPolygonOffset**:</span><span class="sxs-lookup"><span data-stu-id="47ca8-129">The following functions retrieve information related to **glPolygonOffset**:</span></span>

-   <span data-ttu-id="47ca8-130">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument du \_ \_ facteur de décalage du polygone du GL \_</span><span class="sxs-lookup"><span data-stu-id="47ca8-130">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_POLYGON\_OFFSET\_FACTOR</span></span>
-   <span data-ttu-id="47ca8-131">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec arguments GL \_ \_ unité de décalage de polygone \_</span><span class="sxs-lookup"><span data-stu-id="47ca8-131">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_POLYGON\_OFFSET\_UNITS</span></span>
-   <span data-ttu-id="47ca8-132">[**glIsEnabled**](glisenabled.md) avec argument de \_ \_ remplissage de décalage de polygone de GL \_</span><span class="sxs-lookup"><span data-stu-id="47ca8-132">[**glIsEnabled**](glisenabled.md) with argument GL\_POLYGON\_OFFSET\_FILL</span></span>
-   <span data-ttu-id="47ca8-133">[**glIsEnabled**](glisenabled.md) avec argument GL \_ polygone \_ \_ ligne décalage</span><span class="sxs-lookup"><span data-stu-id="47ca8-133">[**glIsEnabled**](glisenabled.md) with argument GL\_POLYGON\_OFFSET\_LINE</span></span>
-   <span data-ttu-id="47ca8-134">[**glIsEnabled**](glisenabled.md) avec argument du \_ \_ point de décalage du polygone du GL \_</span><span class="sxs-lookup"><span data-stu-id="47ca8-134">[**glIsEnabled**](glisenabled.md) with argument GL\_POLYGON\_OFFSET\_POINT</span></span>

> [!Note]  
> <span data-ttu-id="47ca8-135">La fonction **glPolygonOffset** est disponible uniquement dans OpenGl version 1,1 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="47ca8-135">The **glPolygonOffset** function is only available in OpenGl version 1.1 or greater.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="47ca8-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="47ca8-136">Requirements</span></span>



| <span data-ttu-id="47ca8-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="47ca8-137">Requirement</span></span> | <span data-ttu-id="47ca8-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="47ca8-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="47ca8-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="47ca8-139">Minimum supported client</span></span><br/> | <span data-ttu-id="47ca8-140">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="47ca8-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="47ca8-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="47ca8-141">Minimum supported server</span></span><br/> | <span data-ttu-id="47ca8-142">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="47ca8-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="47ca8-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="47ca8-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="47ca8-144"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="47ca8-144"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="47ca8-145">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="47ca8-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="47ca8-146"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="47ca8-146"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="47ca8-147">DLL</span><span class="sxs-lookup"><span data-stu-id="47ca8-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47ca8-148"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47ca8-148"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47ca8-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="47ca8-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47ca8-150">**glDepthFunc**</span><span class="sxs-lookup"><span data-stu-id="47ca8-150">**glDepthFunc**</span></span>](gldepthfunc.md)
</dt> <dt>

[<span data-ttu-id="47ca8-151">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="47ca8-151">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="47ca8-152">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="47ca8-152">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="47ca8-153">**glGet**</span><span class="sxs-lookup"><span data-stu-id="47ca8-153">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="47ca8-154">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="47ca8-154">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="47ca8-155">**glLineWidth**</span><span class="sxs-lookup"><span data-stu-id="47ca8-155">**glLineWidth**</span></span>](gllinewidth.md)
</dt> <dt>

[<span data-ttu-id="47ca8-156">**glStencilOp**</span><span class="sxs-lookup"><span data-stu-id="47ca8-156">**glStencilOp**</span></span>](glstencilop.md)
</dt> <dt>

[<span data-ttu-id="47ca8-157">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="47ca8-157">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> </dl>

 

 





