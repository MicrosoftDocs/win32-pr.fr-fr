---
title: fonction glScissor (GL. h)
description: La fonction glScissor définit la zone de ciseaux.
ms.assetid: c06a1d20-bf7b-4283-b0fe-8bd80bece4ce
keywords:
- glScissor fonction OpenGL
topic_type:
- apiref
api_name:
- glScissor
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e18559bb30260dcb4285980d8dc75642a7c9ec6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466918"
---
# <a name="glscissor-function"></a><span data-ttu-id="6b8aa-104">glScissor fonction)</span><span class="sxs-lookup"><span data-stu-id="6b8aa-104">glScissor function</span></span>

<span data-ttu-id="6b8aa-105">La fonction **glScissor** définit la zone de ciseaux.</span><span class="sxs-lookup"><span data-stu-id="6b8aa-105">The **glScissor** function defines the scissor box.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b8aa-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6b8aa-106">Syntax</span></span>


```C++
void WINAPI glScissor(
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height
);
```



## <a name="parameters"></a><span data-ttu-id="6b8aa-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6b8aa-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b8aa-108">*x*</span><span class="sxs-lookup"><span data-stu-id="6b8aa-108">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="6b8aa-109">Coordonnée x (axe vertical) du coin inférieur gauche de la zone de ciseaux.</span><span class="sxs-lookup"><span data-stu-id="6b8aa-109">The x (vertical axis) coordinate for the lower-left corner of the scissor box.</span></span>

</dd> <dt>

<span data-ttu-id="6b8aa-110">*y*</span><span class="sxs-lookup"><span data-stu-id="6b8aa-110">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="6b8aa-111">Coordonnée y (axe horizontal) du coin inférieur gauche de la zone de ciseaux.</span><span class="sxs-lookup"><span data-stu-id="6b8aa-111">The y (horizontal axis) coordinate for the lower-left corner of the scissor box.</span></span> <span data-ttu-id="6b8aa-112">Ensemble, x et y spécifient l’angle inférieur gauche de la zone de ciseaux.</span><span class="sxs-lookup"><span data-stu-id="6b8aa-112">Together, x and y specify the lower-left corner of the scissor box.</span></span> <span data-ttu-id="6b8aa-113">À l’origine (0,0).</span><span class="sxs-lookup"><span data-stu-id="6b8aa-113">Initially (0,0).</span></span>

</dd> <dt>

<span data-ttu-id="6b8aa-114">*width*</span><span class="sxs-lookup"><span data-stu-id="6b8aa-114">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="6b8aa-115">Largeur de la zone de ciseaux.</span><span class="sxs-lookup"><span data-stu-id="6b8aa-115">The width of the scissor box.</span></span>

</dd> <dt>

<span data-ttu-id="6b8aa-116">*height*</span><span class="sxs-lookup"><span data-stu-id="6b8aa-116">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="6b8aa-117">Hauteur de la zone de ciseaux.</span><span class="sxs-lookup"><span data-stu-id="6b8aa-117">The height of the scissor box.</span></span> <span data-ttu-id="6b8aa-118">Lorsqu’un contexte OpenGL est attaché pour la *première fois* à une fenêtre, la *largeur* et la *hauteur* sont définies sur les dimensions de cette fenêtre.</span><span class="sxs-lookup"><span data-stu-id="6b8aa-118">When an OpenGL context is *first* attached to a window, *width* and *height* are set to the dimensions of that window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b8aa-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6b8aa-119">Return value</span></span>

<span data-ttu-id="6b8aa-120">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="6b8aa-120">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6b8aa-121">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="6b8aa-121">Error codes</span></span>

<span data-ttu-id="6b8aa-122">Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="6b8aa-122">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="6b8aa-123">Nom</span><span class="sxs-lookup"><span data-stu-id="6b8aa-123">Name</span></span>                                                                                                  | <span data-ttu-id="6b8aa-124">Signification</span><span class="sxs-lookup"><span data-stu-id="6b8aa-124">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6b8aa-125"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6b8aa-125"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="6b8aa-126">La *largeur* ou la *hauteur* était négative.</span><span class="sxs-lookup"><span data-stu-id="6b8aa-126">Either *width* or *height* was negative.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="6b8aa-127"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6b8aa-127"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="6b8aa-128">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="6b8aa-128">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="6b8aa-129">Notes</span><span class="sxs-lookup"><span data-stu-id="6b8aa-129">Remarks</span></span>

<span data-ttu-id="6b8aa-130">La fonction **glScissor** définit un rectangle, appelé zone de ciseaux, dans les coordonnées de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="6b8aa-130">The **glScissor** function defines a rectangle, called the scissor box, in window coordinates.</span></span> <span data-ttu-id="6b8aa-131">Les deux premiers paramètres, *x* et *y*, spécifient l’angle inférieur gauche de la zone.</span><span class="sxs-lookup"><span data-stu-id="6b8aa-131">The first two parameters, *x* and *y*, specify the lower-left corner of the box.</span></span> <span data-ttu-id="6b8aa-132">Les paramètres de *largeur* et de *hauteur* spécifient la largeur et la hauteur de la zone.</span><span class="sxs-lookup"><span data-stu-id="6b8aa-132">The *width* and *height* parameters specify the width and height of the box.</span></span>

<span data-ttu-id="6b8aa-133">Le test de ciseaux est activé et désactivé à l’aide de [**glEnable**](glenable.md) et de **GLDISABLE** avec argument GL \_ ciseaux \_ test.</span><span class="sxs-lookup"><span data-stu-id="6b8aa-133">The scissor test is enabled and disabled using [**glEnable**](glenable.md) and **glDisable** with argument GL\_SCISSOR\_TEST.</span></span> <span data-ttu-id="6b8aa-134">Pendant que le test de ciseaux est activé, seuls les pixels qui se trouvent dans la zone de ciseaux peuvent être modifiés en dessinant des commandes.</span><span class="sxs-lookup"><span data-stu-id="6b8aa-134">While the scissor test is enabled, only pixels that lie within the scissor box can be modified by drawing commands.</span></span> <span data-ttu-id="6b8aa-135">Les coordonnées de fenêtre ont des valeurs entières aux angles partagés de trame pixels. par conséquent, **glScissor**(0, 0, 1, 1) autorise uniquement la modification du pixel inférieur gauche de la fenêtre, tandis que **glScissor**(0, 0, 0, 0) interdit la modification de tous les pixels de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="6b8aa-135">Window coordinates have integer values at the shared corners of framebuffer pixels, so **glScissor**(0,0,1,1) allows only the lower-left pixel in the window to be modified, and **glScissor**(0,0,0,0) disallows modification to all pixels in the window.</span></span>

<span data-ttu-id="6b8aa-136">Lorsque le test de ciseaux est désactivé, c’est comme si la zone de la ciseaux inclue la fenêtre entière.</span><span class="sxs-lookup"><span data-stu-id="6b8aa-136">When the scissor test is disabled, it is as though the scissor box includes the entire window.</span></span>

<span data-ttu-id="6b8aa-137">Les fonctions suivantes récupèrent les informations relatives à **glScissor**:</span><span class="sxs-lookup"><span data-stu-id="6b8aa-137">The following functions retrieve information related to **glScissor**:</span></span>

<span data-ttu-id="6b8aa-138">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ ciseaux \_ zone</span><span class="sxs-lookup"><span data-stu-id="6b8aa-138">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_SCISSOR\_BOX</span></span>

<span data-ttu-id="6b8aa-139">[**glIsEnabled**](glisenabled.md) avec argument GL \_ de \_ test de ciseaux</span><span class="sxs-lookup"><span data-stu-id="6b8aa-139">[**glIsEnabled**](glisenabled.md) with argument GL\_SCISSOR\_TEST</span></span>

## <a name="requirements"></a><span data-ttu-id="6b8aa-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6b8aa-140">Requirements</span></span>



| <span data-ttu-id="6b8aa-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6b8aa-141">Requirement</span></span> | <span data-ttu-id="6b8aa-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="6b8aa-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b8aa-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6b8aa-143">Minimum supported client</span></span><br/> | <span data-ttu-id="6b8aa-144">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6b8aa-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6b8aa-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6b8aa-145">Minimum supported server</span></span><br/> | <span data-ttu-id="6b8aa-146">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6b8aa-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6b8aa-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="6b8aa-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b8aa-148"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b8aa-148"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="6b8aa-149">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6b8aa-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="6b8aa-150"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6b8aa-150"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="6b8aa-151">DLL</span><span class="sxs-lookup"><span data-stu-id="6b8aa-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b8aa-152"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b8aa-152"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b8aa-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6b8aa-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b8aa-154">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="6b8aa-154">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="6b8aa-155">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="6b8aa-155">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="6b8aa-156">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="6b8aa-156">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="6b8aa-157">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="6b8aa-157">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="6b8aa-158">**glViewport**</span><span class="sxs-lookup"><span data-stu-id="6b8aa-158">**glViewport**</span></span>](glviewport.md)
</dt> </dl>

 

 





