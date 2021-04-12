---
title: fonction glDepthRange (GL. h)
description: La fonction glDepthRange spécifie le mappage des valeurs z des coordonnées de périphérique normalisées aux coordonnées de la fenêtre.
ms.assetid: 44aed5e5-4bd2-4e7f-ad05-1cf4be5254a5
keywords:
- glDepthRange fonction OpenGL
topic_type:
- apiref
api_name:
- glDepthRange
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0bd6a22ae91877c9b20fa5387edd9438942a07d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384255"
---
# <a name="gldepthrange-function"></a><span data-ttu-id="71eac-104">glDepthRange fonction)</span><span class="sxs-lookup"><span data-stu-id="71eac-104">glDepthRange function</span></span>

<span data-ttu-id="71eac-105">La fonction **glDepthRange** spécifie le mappage des valeurs *z* des coordonnées de périphérique normalisées aux coordonnées de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="71eac-105">The **glDepthRange** function specifies the mapping of *z* values from normalized device coordinates to window coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="71eac-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="71eac-106">Syntax</span></span>


```C++
void WINAPI glDepthRange(
   GLclampd zNear,
   GLclampd zFar
);
```



## <a name="parameters"></a><span data-ttu-id="71eac-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="71eac-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71eac-108">*zNear*</span><span class="sxs-lookup"><span data-stu-id="71eac-108">*zNear*</span></span> 
</dt> <dd>

<span data-ttu-id="71eac-109">Mappage du plan de découpage near aux coordonnées de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="71eac-109">The mapping of the near clipping plane to window coordinates.</span></span> <span data-ttu-id="71eac-110">La valeur par défaut est zéro.</span><span class="sxs-lookup"><span data-stu-id="71eac-110">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="71eac-111">*zFar*</span><span class="sxs-lookup"><span data-stu-id="71eac-111">*zFar*</span></span> 
</dt> <dd>

<span data-ttu-id="71eac-112">Mappage du plan de découpage Far aux coordonnées de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="71eac-112">The mapping of the far clipping plane to window coordinates.</span></span> <span data-ttu-id="71eac-113">La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="71eac-113">The default value is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71eac-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="71eac-114">Return value</span></span>

<span data-ttu-id="71eac-115">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="71eac-115">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="71eac-116">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="71eac-116">Error codes</span></span>

<span data-ttu-id="71eac-117">Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="71eac-117">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="71eac-118">Nom</span><span class="sxs-lookup"><span data-stu-id="71eac-118">Name</span></span>                                                                                                  | <span data-ttu-id="71eac-119">Signification</span><span class="sxs-lookup"><span data-stu-id="71eac-119">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="71eac-120"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="71eac-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="71eac-121">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="71eac-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="71eac-122">Notes</span><span class="sxs-lookup"><span data-stu-id="71eac-122">Remarks</span></span>

<span data-ttu-id="71eac-123">Après découpage et division par *w*, les coordonnées *z* sont comprises entre 0,0 et 1,0, ce qui correspond aux plans de découpage near et Far.</span><span class="sxs-lookup"><span data-stu-id="71eac-123">After clipping and division by *w*, *z* -coordinates range from 0.0 to 1.0, corresponding to the near and far clipping planes.</span></span> <span data-ttu-id="71eac-124">La fonction **glDepthRange** spécifie un mappage linéaire des coordonnées *z* normalisées dans cette plage aux coordonnées *z* de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="71eac-124">The **glDepthRange** function specifies a linear mapping of the normalized *z*-coordinates in this range to window *z*-coordinates.</span></span> <span data-ttu-id="71eac-125">Quelle que soit l’implémentation réelle du tampon de profondeur, les valeurs de profondeur de la coordonnée de la fenêtre sont traitées comme si elles sont comprises entre 0,0 et 1,0 (comme les composants de couleur).</span><span class="sxs-lookup"><span data-stu-id="71eac-125">Regardless of the actual depth buffer implementation, window coordinate depth values are treated as though they range from 0.0 through 1.0 (like color components).</span></span> <span data-ttu-id="71eac-126">Ainsi, les valeurs acceptées par **glDepthRange** sont conjointes à cette plage avant d’être acceptées.</span><span class="sxs-lookup"><span data-stu-id="71eac-126">Thus, the values accepted by **glDepthRange** are both clamped to this range before they are accepted.</span></span>

<span data-ttu-id="71eac-127">Le mappage par défaut (0, 1) mappe le plan near à 0 et le plan Far à 1.</span><span class="sxs-lookup"><span data-stu-id="71eac-127">The default mapping of (0,1) maps the near plane to 0 and the far plane to 1.</span></span> <span data-ttu-id="71eac-128">Avec ce mappage, la plage de mémoire tampon de profondeur est entièrement utilisée.</span><span class="sxs-lookup"><span data-stu-id="71eac-128">With this mapping, the depth buffer range is fully utilized.</span></span>

<span data-ttu-id="71eac-129">Il n’est pas nécessaire que *zNear* soit inférieur à *zFar*.</span><span class="sxs-lookup"><span data-stu-id="71eac-129">It is not necessary that *zNear* be less than *zFar*.</span></span> <span data-ttu-id="71eac-130">Les mappages inverses tels que (1,0) sont acceptables.</span><span class="sxs-lookup"><span data-stu-id="71eac-130">Reverse mappings such as (1,0) are acceptable.</span></span>

<span data-ttu-id="71eac-131">La fonction suivante récupère des informations relatives à **glDepthRange**:</span><span class="sxs-lookup"><span data-stu-id="71eac-131">The following function retrieves information related to **glDepthRange**:</span></span>

<span data-ttu-id="71eac-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec la \_ plage de profondeur de l’argument GL \_</span><span class="sxs-lookup"><span data-stu-id="71eac-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_DEPTH\_RANGE</span></span>

## <a name="requirements"></a><span data-ttu-id="71eac-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="71eac-133">Requirements</span></span>



| <span data-ttu-id="71eac-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="71eac-134">Requirement</span></span> | <span data-ttu-id="71eac-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="71eac-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="71eac-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71eac-136">Minimum supported client</span></span><br/> | <span data-ttu-id="71eac-137">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="71eac-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="71eac-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71eac-138">Minimum supported server</span></span><br/> | <span data-ttu-id="71eac-139">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="71eac-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="71eac-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="71eac-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="71eac-141"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="71eac-141"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="71eac-142">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="71eac-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="71eac-143"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="71eac-143"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="71eac-144">DLL</span><span class="sxs-lookup"><span data-stu-id="71eac-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71eac-145"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71eac-145"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71eac-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71eac-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71eac-147">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="71eac-147">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="71eac-148">**glDepthFunc**</span><span class="sxs-lookup"><span data-stu-id="71eac-148">**glDepthFunc**</span></span>](gldepthfunc.md)
</dt> <dt>

[<span data-ttu-id="71eac-149">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="71eac-149">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="71eac-150">**glGet**</span><span class="sxs-lookup"><span data-stu-id="71eac-150">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="71eac-151">**glViewport**</span><span class="sxs-lookup"><span data-stu-id="71eac-151">**glViewport**</span></span>](glviewport.md)
</dt> </dl>

 

 





