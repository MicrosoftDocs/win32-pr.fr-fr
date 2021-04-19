---
title: gluLoadSamplingMatrices, fonction (Glu. h)
description: La fonction gluLoadSamplingMatrices charge des matrices d’échantillonnage et de cullinging rationnelles (NURBS) non uniformes.
ms.assetid: 7fdbc4e2-a037-4f07-bb03-e51feea42775
keywords:
- gluLoadSamplingMatrices fonction OpenGL
topic_type:
- apiref
api_name:
- gluLoadSamplingMatrices
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 293b8bace0dff7d89bfcffa2af33738e0e59de7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510128"
---
# <a name="gluloadsamplingmatrices-function"></a><span data-ttu-id="19d2d-104">gluLoadSamplingMatrices fonction)</span><span class="sxs-lookup"><span data-stu-id="19d2d-104">gluLoadSamplingMatrices function</span></span>

<span data-ttu-id="19d2d-105">La fonction **gluLoadSamplingMatrices** charge des matrices d’échantillonnage et de Cullinging rationnelles ([NURBS](using-nurbs-curves-and-surfaces.md)) non uniformes.</span><span class="sxs-lookup"><span data-stu-id="19d2d-105">The **gluLoadSamplingMatrices** function loads Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) sampling and culling matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="19d2d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="19d2d-106">Syntax</span></span>


```C++
void WINAPI gluLoadSamplingMatrices(
         GLUnurbs *nobj,
   const GLfloat  modelMatrix[16],
   const GLfloat  projMatrix[16],
   const GLint    viewport[4]
);
```



## <a name="parameters"></a><span data-ttu-id="19d2d-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="19d2d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19d2d-108">*nobj*</span><span class="sxs-lookup"><span data-stu-id="19d2d-108">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="19d2d-109">Objet NURBS (créé avec [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span><span class="sxs-lookup"><span data-stu-id="19d2d-109">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="19d2d-110">*modelMatrix*</span><span class="sxs-lookup"><span data-stu-id="19d2d-110">*modelMatrix*</span></span> 
</dt> <dd>

<span data-ttu-id="19d2d-111">Matrice modelview (à partir d’un appel [**glGetFloatv**](glgetfloatv.md) ).</span><span class="sxs-lookup"><span data-stu-id="19d2d-111">A modelview matrix (as from a [**glGetFloatv**](glgetfloatv.md) call).</span></span>

</dd> <dt>

<span data-ttu-id="19d2d-112">*projMatrix*</span><span class="sxs-lookup"><span data-stu-id="19d2d-112">*projMatrix*</span></span> 
</dt> <dd>

<span data-ttu-id="19d2d-113">Matrice de projection (à partir d’un appel **glGetFloatv** ).</span><span class="sxs-lookup"><span data-stu-id="19d2d-113">A projection matrix (as from a **glGetFloatv** call).</span></span>

</dd> <dt>

<span data-ttu-id="19d2d-114">*vue*</span><span class="sxs-lookup"><span data-stu-id="19d2d-114">*viewport*</span></span> 
</dt> <dd>

<span data-ttu-id="19d2d-115">Une fenêtre d’affichage (à partir d’un appel [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ).</span><span class="sxs-lookup"><span data-stu-id="19d2d-115">A viewport (as from a [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) call).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19d2d-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="19d2d-116">Return value</span></span>

<span data-ttu-id="19d2d-117">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="19d2d-117">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="19d2d-118">Notes</span><span class="sxs-lookup"><span data-stu-id="19d2d-118">Remarks</span></span>

<span data-ttu-id="19d2d-119">La fonction **gluLoadSamplingMatrices** utilise *modelMatrix*, *projMatrix* et *Viewport* pour recalculer les matrices d’échantillonnage et de Culling stockées dans *nobj*.</span><span class="sxs-lookup"><span data-stu-id="19d2d-119">The **gluLoadSamplingMatrices** function uses *modelMatrix*, *projMatrix*, and *viewport* to recompute the sampling and culling matrices stored in *nobj*.</span></span> <span data-ttu-id="19d2d-120">La matrice d’échantillonnage détermine la précision avec laquelle une courbe ou surface NURBS doit être fractionnée pour satisfaire la tolérance d’échantillonnage (telle que déterminée par la \_ propriété tolérance d’échantillonnage Glu \_ ).</span><span class="sxs-lookup"><span data-stu-id="19d2d-120">The sampling matrix determines how finely a NURBS curve or surface must be tessellated to satisfy the sampling tolerance (as determined by the GLU\_SAMPLING\_TOLERANCE property).</span></span> <span data-ttu-id="19d2d-121">La matrice de Culling est utilisée pour décider si une courbe ou une surface NURBS doit être éliminée avant le rendu (lorsque la \_ propriété Glu Culling est activée).</span><span class="sxs-lookup"><span data-stu-id="19d2d-121">The culling matrix is used in deciding if a NURBS curve or surface should be culled before rendering (when the GLU\_CULLING property is turned on).</span></span>

<span data-ttu-id="19d2d-122">La fonction **gluLoadSamplingMatrices** est nécessaire uniquement si la propriété de la \_ matrice de chargement automatique Glu \_ \_ est désactivée (voir [**gluNurbsProperty**](glunurbsproperty.md)).</span><span class="sxs-lookup"><span data-stu-id="19d2d-122">The **gluLoadSamplingMatrices** function is necessary only if the GLU\_AUTO\_LOAD\_MATRIX property is turned off (see [**gluNurbsProperty**](glunurbsproperty.md)).</span></span> <span data-ttu-id="19d2d-123">Bien qu’il soit pratique de conserver la \_ \_ propriété matrice de chargement automatique Glu \_ activée, cela nécessite un aller-retour au serveur OpenGL pour obtenir les valeurs actuelles de la matrice modelview, de la matrice de projection et de la fenêtre d’affichage.)</span><span class="sxs-lookup"><span data-stu-id="19d2d-123">Although it can be convenient to leave the GLU\_AUTO\_LOAD\_MATRIX property turned on, doing so necessitates a round trip to the OpenGL server to get the current values of the modelview matrix, projection matrix, and viewport.)</span></span>

## <a name="requirements"></a><span data-ttu-id="19d2d-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="19d2d-124">Requirements</span></span>



| <span data-ttu-id="19d2d-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="19d2d-125">Requirement</span></span> | <span data-ttu-id="19d2d-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="19d2d-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="19d2d-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="19d2d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="19d2d-128">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="19d2d-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="19d2d-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="19d2d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="19d2d-130">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="19d2d-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="19d2d-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="19d2d-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="19d2d-132"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="19d2d-132"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="19d2d-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="19d2d-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="19d2d-134"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="19d2d-134"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="19d2d-135">DLL</span><span class="sxs-lookup"><span data-stu-id="19d2d-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19d2d-136"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19d2d-136"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19d2d-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="19d2d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19d2d-138">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="19d2d-138">**glGetFloatv**</span></span>](glgetfloatv.md)
</dt> <dt>

[<span data-ttu-id="19d2d-139">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="19d2d-139">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="19d2d-140">**gluGetNurbsProperty**</span><span class="sxs-lookup"><span data-stu-id="19d2d-140">**gluGetNurbsProperty**</span></span>](glugetnurbsproperty.md)
</dt> <dt>

[<span data-ttu-id="19d2d-141">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="19d2d-141">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> </dl>

 

 





