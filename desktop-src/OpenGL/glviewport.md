---
title: fonction glViewport (GL. h)
description: La fonction glViewport définit la fenêtre d’affichage.
ms.assetid: 11816b2f-ee18-42ef-a782-2e96699dd087
keywords:
- glViewport fonction OpenGL
topic_type:
- apiref
api_name:
- glViewport
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5e8eedb9c66211deda92ef6a84e8c1dd2073362
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104569716"
---
# <a name="glviewport-function"></a><span data-ttu-id="4a234-104">glViewport fonction)</span><span class="sxs-lookup"><span data-stu-id="4a234-104">glViewport function</span></span>

<span data-ttu-id="4a234-105">La fonction **glViewport** définit la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="4a234-105">The **glViewport** function sets the viewport.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a234-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4a234-106">Syntax</span></span>


```C++
void WINAPI glViewport(
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height
);
```



## <a name="parameters"></a><span data-ttu-id="4a234-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4a234-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a234-108">*x*</span><span class="sxs-lookup"><span data-stu-id="4a234-108">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="4a234-109">Angle inférieur gauche du rectangle de la fenêtre d’affichage, en pixels.</span><span class="sxs-lookup"><span data-stu-id="4a234-109">The lower-left corner of the viewport rectangle, in pixels.</span></span> <span data-ttu-id="4a234-110">La valeur par défaut est (0,0).</span><span class="sxs-lookup"><span data-stu-id="4a234-110">The default is (0,0).</span></span>

</dd> <dt>

<span data-ttu-id="4a234-111">*y*</span><span class="sxs-lookup"><span data-stu-id="4a234-111">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="4a234-112">Angle inférieur gauche du rectangle de la fenêtre d’affichage, en pixels.</span><span class="sxs-lookup"><span data-stu-id="4a234-112">The lower-left corner of the viewport rectangle, in pixels.</span></span> <span data-ttu-id="4a234-113">La valeur par défaut est (0,0).</span><span class="sxs-lookup"><span data-stu-id="4a234-113">The default is (0,0).</span></span>

</dd> <dt>

<span data-ttu-id="4a234-114">*width*</span><span class="sxs-lookup"><span data-stu-id="4a234-114">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="4a234-115">Largeur de la fenêtre d'affichage.</span><span class="sxs-lookup"><span data-stu-id="4a234-115">The width of the viewport.</span></span> <span data-ttu-id="4a234-116">Lorsqu’un contexte OpenGL est attaché pour la première fois à une fenêtre, la *largeur* et la *hauteur* sont définies sur les dimensions de cette fenêtre.</span><span class="sxs-lookup"><span data-stu-id="4a234-116">When an OpenGL context is first attached to a window, *width* and *height* are set to the dimensions of that window.</span></span>

</dd> <dt>

<span data-ttu-id="4a234-117">*height*</span><span class="sxs-lookup"><span data-stu-id="4a234-117">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="4a234-118">Hauteur de la fenêtre d'affichage.</span><span class="sxs-lookup"><span data-stu-id="4a234-118">The height of the viewport.</span></span> <span data-ttu-id="4a234-119">Lorsqu’un contexte OpenGL est attaché pour la première fois à une fenêtre, la *largeur* et la *hauteur* sont définies sur les dimensions de cette fenêtre.</span><span class="sxs-lookup"><span data-stu-id="4a234-119">When an OpenGL context is first attached to a window, *width* and *height* are set to the dimensions of that window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a234-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4a234-120">Return value</span></span>

<span data-ttu-id="4a234-121">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="4a234-121">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4a234-122">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="4a234-122">Error codes</span></span>

<span data-ttu-id="4a234-123">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="4a234-123">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="4a234-124">Nom</span><span class="sxs-lookup"><span data-stu-id="4a234-124">Name</span></span>                                                                                                  | <span data-ttu-id="4a234-125">Signification</span><span class="sxs-lookup"><span data-stu-id="4a234-125">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4a234-126"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4a234-126"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="4a234-127">La *largeur* ou la *hauteur* était négative.</span><span class="sxs-lookup"><span data-stu-id="4a234-127">Either *width* or *height* was negative.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="4a234-128"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4a234-128"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="4a234-129">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="4a234-129">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="4a234-130">Notes</span><span class="sxs-lookup"><span data-stu-id="4a234-130">Remarks</span></span>

<span data-ttu-id="4a234-131">La fonction **glViewport** spécifie la transformation affine de *x* et *y* à partir des coordonnées de l’appareil normalisées en coordonnées de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="4a234-131">The **glViewport** function specifies the affine transformation of *x* and *y* from normalized device coordinates to window coordinates.</span></span> <span data-ttu-id="4a234-132">Let (*x*<sub>ND</sub> , *y*<sub>ND</sub> ) sont des coordonnées de périphérique normalisées.</span><span class="sxs-lookup"><span data-stu-id="4a234-132">Let (*x*<sub>nd</sub> , *y*<sub>nd</sub> ) be normalized device coordinates.</span></span> <span data-ttu-id="4a234-133">Les coordonnées de la fenêtre (*x*<sub>w</sub> , *y*<sub>w</sub> ) sont ensuite calculées comme suit :</span><span class="sxs-lookup"><span data-stu-id="4a234-133">The window coordinates (*x*<sub>w</sub> , *y*<sub>w</sub> ) are then computed as follows:</span></span>

![Équation qui indique le calcul des coordonnées de la fenêtre.](images/view01.png)

<span data-ttu-id="4a234-135">La largeur et la hauteur de la fenêtre d’affichage sont ancrées silencieusement à une plage qui dépend de l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="4a234-135">Viewport width and height are silently clamped to a range that depends on the implementation.</span></span> <span data-ttu-id="4a234-136">Cette plage est interrogée en appelant **glGet** avec l’argument GL \_ Max \_ VIEWPORT \_ DIMS.</span><span class="sxs-lookup"><span data-stu-id="4a234-136">This range is queried by calling **glGet** with argument GL\_MAX\_VIEWPORT\_DIMS.</span></span>

<span data-ttu-id="4a234-137">Les fonctions suivantes récupèrent les informations relatives à **glViewport**:</span><span class="sxs-lookup"><span data-stu-id="4a234-137">The following functions retrieve information related to **glViewport**:</span></span>

<span data-ttu-id="4a234-138">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec l’argument GL \_ VIEWPORT</span><span class="sxs-lookup"><span data-stu-id="4a234-138">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_VIEWPORT</span></span>

<span data-ttu-id="4a234-139">**glGet** avec l’argument GL \_ Max \_ VIEWPORT \_ DIMS</span><span class="sxs-lookup"><span data-stu-id="4a234-139">**glGet** with argument GL\_MAX\_VIEWPORT\_DIMS</span></span>

## <a name="requirements"></a><span data-ttu-id="4a234-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4a234-140">Requirements</span></span>



| <span data-ttu-id="4a234-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4a234-141">Requirement</span></span> | <span data-ttu-id="4a234-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="4a234-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a234-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4a234-143">Minimum supported client</span></span><br/> | <span data-ttu-id="4a234-144">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4a234-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="4a234-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4a234-145">Minimum supported server</span></span><br/> | <span data-ttu-id="4a234-146">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4a234-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4a234-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="4a234-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a234-148"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a234-148"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="4a234-149">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4a234-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="4a234-150"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4a234-150"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="4a234-151">DLL</span><span class="sxs-lookup"><span data-stu-id="4a234-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a234-152"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a234-152"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a234-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4a234-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a234-154">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="4a234-154">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="4a234-155">**glDepthRange**</span><span class="sxs-lookup"><span data-stu-id="4a234-155">**glDepthRange**</span></span>](gldepthrange.md)
</dt> </dl>

 

 





