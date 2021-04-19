---
title: fonction glEvalPoint2 (GL. h)
description: Les fonctions glEvalPoint1 et glEvalPoint2 génèrent et évaluent un point unique dans une maille. | fonction glEvalPoint2 (GL. h)
ms.assetid: babae9c7-84a8-4a7e-b6f9-97c4e8bd42fe
keywords:
- glEvalPoint2 fonction OpenGL
topic_type:
- apiref
api_name:
- glEvalPoint2
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fafe728249f988462b0929873bbb195fed1e7c9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106539840"
---
# <a name="glevalpoint2-function"></a><span data-ttu-id="51567-105">glEvalPoint2 fonction)</span><span class="sxs-lookup"><span data-stu-id="51567-105">glEvalPoint2 function</span></span>

<span data-ttu-id="51567-106">Les fonctions [**glEvalPoint1**](glevalpoint.md) et **glEvalPoint2** génèrent et évaluent un point unique dans une maille.</span><span class="sxs-lookup"><span data-stu-id="51567-106">The [**glEvalPoint1**](glevalpoint.md) and **glEvalPoint2** functions generate and evaluate a single point in a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="51567-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="51567-107">Syntax</span></span>


```C++
void glEvalPoint2(
   GLint i,
   GLint j
);
```



## <a name="parameters"></a><span data-ttu-id="51567-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="51567-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51567-109">*i*</span><span class="sxs-lookup"><span data-stu-id="51567-109">*i*</span></span> 
</dt> <dd>

<span data-ttu-id="51567-110">Valeur entière pour la variable de domaine Grid *i*.</span><span class="sxs-lookup"><span data-stu-id="51567-110">The integer value for grid domain variable *i*.</span></span>

</dd> <dt>

<span data-ttu-id="51567-111">*j*</span><span class="sxs-lookup"><span data-stu-id="51567-111">*j*</span></span> 
</dt> <dd>

<span data-ttu-id="51567-112">Valeur entière pour la variable de domaine Grid *j* .</span><span class="sxs-lookup"><span data-stu-id="51567-112">The integer value for grid domain variable *j* .</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51567-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="51567-113">Return value</span></span>

<span data-ttu-id="51567-114">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="51567-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="51567-115">Notes</span><span class="sxs-lookup"><span data-stu-id="51567-115">Remarks</span></span>

<span data-ttu-id="51567-116">Les fonctions [**glMapGrid**](glmapgrid-functions.md) et [**glEvalMesh**](glevalmesh-functions.md) sont utilisées en tandem pour générer et évaluer efficacement une série de valeurs de domaine de mappage uniformément espacées.</span><span class="sxs-lookup"><span data-stu-id="51567-116">The [**glMapGrid**](glmapgrid-functions.md) and [**glEvalMesh**](glevalmesh-functions.md) functions are used in tandem to efficiently generate and evaluate a series of evenly spaced map domain values.</span></span> <span data-ttu-id="51567-117">Vous pouvez utiliser **glEvalPoint** pour évaluer un seul point de grille dans le même Gridspace parcouru par **glEvalMesh**.</span><span class="sxs-lookup"><span data-stu-id="51567-117">You can use **glEvalPoint** to evaluate a single grid point in the same gridspace that is traversed by **glEvalMesh**.</span></span> <span data-ttu-id="51567-118">L’appel de [**glEvalPoint1**](glevalpoint.md) équivaut à appeler</span><span class="sxs-lookup"><span data-stu-id="51567-118">Calling [**glEvalPoint1**](glevalpoint.md) is equivalent to calling</span></span>

<span data-ttu-id="51567-119">**glEvalCoord1** (*i* ?*u*  + *u* 1);</span><span class="sxs-lookup"><span data-stu-id="51567-119">**glEvalCoord1** (*i* ?*u* +*u* 1 );</span></span>

<span data-ttu-id="51567-120">where</span><span class="sxs-lookup"><span data-stu-id="51567-120">where</span></span>

<span data-ttu-id="51567-121">? *u* = (*u* 2 *u* 1)/*n*</span><span class="sxs-lookup"><span data-stu-id="51567-121">?*u* = (*u* 2 *u* 1 )/*n*</span></span>

<span data-ttu-id="51567-122">et *n*, *u* 1 et *u* 2 sont les arguments de la fonction **glMapGrid1** la plus récente.</span><span class="sxs-lookup"><span data-stu-id="51567-122">and *n*, *u* 1 , and *u* 2 are the arguments to the most recent **glMapGrid1** function.</span></span> <span data-ttu-id="51567-123">La seule exigence numérique absolue est que si *i*  =  *n*, la valeur calculée à partir de (*i* ?*u* + U1) est exactement *u* 2.</span><span class="sxs-lookup"><span data-stu-id="51567-123">The one absolute numeric requirement is that if *i* = *n*, then the value computed from (*i* ?*u* + u1 ) is exactly *u* 2 .</span></span>

<span data-ttu-id="51567-124">Dans le cas à deux dimensions, **glEvalPoint2**, Let</span><span class="sxs-lookup"><span data-stu-id="51567-124">In the two-dimensional case, **glEvalPoint2**, let</span></span>

<span data-ttu-id="51567-125">? *u* = (*u* 2 *u* 1)/*n*</span><span class="sxs-lookup"><span data-stu-id="51567-125">?*u* = (*u* 2 *u* 1 )/*n*</span></span>

<span data-ttu-id="51567-126">? *v* = (*v* 2 *v* 1)/*m*</span><span class="sxs-lookup"><span data-stu-id="51567-126">?*v* = (*v* 2 *v* 1 )/*m*</span></span>

<span data-ttu-id="51567-127">où *n*, *u* 1, *u* 2, *m*, *v* 1 et *v* 2 sont les arguments de la fonction **glMapGrid2** la plus récente.</span><span class="sxs-lookup"><span data-stu-id="51567-127">where *n*, *u* 1 , *u* 2 , *m*, *v* 1 , and *v* 2  are the arguments to the most recent **glMapGrid2** function.</span></span> <span data-ttu-id="51567-128">La fonction **glEvalPoint2** est alors équivalente à l’appel de</span><span class="sxs-lookup"><span data-stu-id="51567-128">Then the **glEvalPoint2** function is equivalent to calling</span></span>

<span data-ttu-id="51567-129">**glEvalCoord2** (*i* ?*u*  +  *u* 1, *j* ?*v*  +  *v* 1);</span><span class="sxs-lookup"><span data-stu-id="51567-129">**glEvalCoord2** (*i* ?*u* + *u* 1 , *j* ?*v* + *v* 1 );</span></span>

<span data-ttu-id="51567-130">Les seules exigences numériques absolues sont que si *i* = *n*, la valeur est calculée à partir de (*i* ?*u*  +  *u* 1) est exactement U2 et, si *j*  =  *m*, la valeur calculée à partir de (*j* ?*v*  +  *v* 1) est exactement *v* 2.</span><span class="sxs-lookup"><span data-stu-id="51567-130">The only absolute numeric requirements are that if *i*=*n*, then the value computed from (*i* ?*u* + *u* 1 ) is exactly u2 , and if *j* = *m*, then the value computed from (*j* ?*v* + *v* 1  ) is exactly *v* 2 .</span></span>

<span data-ttu-id="51567-131">Les fonctions suivantes récupèrent des informations relatives à [**glEvalPoint1**](glevalpoint.md) et **glEvalPoint2**:</span><span class="sxs-lookup"><span data-stu-id="51567-131">The following functions retrieve information relating to [**glEvalPoint1**](glevalpoint.md) and **glEvalPoint2**:</span></span>

<span data-ttu-id="51567-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Map1 \_ Grid \_ Domain</span><span class="sxs-lookup"><span data-stu-id="51567-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP1\_GRID\_DOMAIN</span></span>

<span data-ttu-id="51567-133">**glGet** avec argument GL \_ map2 \_ Grid \_ Domain</span><span class="sxs-lookup"><span data-stu-id="51567-133">**glGet** with argument GL\_MAP2\_GRID\_DOMAIN</span></span>

<span data-ttu-id="51567-134">**glGet** avec des \_ segments de \_ grille \_ Map1 d’argument GL</span><span class="sxs-lookup"><span data-stu-id="51567-134">**glGet** with argument GL\_MAP1\_GRID\_SEGMENTS</span></span>

<span data-ttu-id="51567-135">**glGet** avec des \_ segments de \_ grille \_ map2 d’argument GL</span><span class="sxs-lookup"><span data-stu-id="51567-135">**glGet** with argument GL\_MAP2\_GRID\_SEGMENTS</span></span>

## <a name="requirements"></a><span data-ttu-id="51567-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="51567-136">Requirements</span></span>



| <span data-ttu-id="51567-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="51567-137">Requirement</span></span> | <span data-ttu-id="51567-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="51567-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="51567-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="51567-139">Minimum supported client</span></span><br/> | <span data-ttu-id="51567-140">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="51567-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="51567-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="51567-141">Minimum supported server</span></span><br/> | <span data-ttu-id="51567-142">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="51567-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="51567-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="51567-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="51567-144"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="51567-144"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="51567-145">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="51567-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="51567-146"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="51567-146"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="51567-147">DLL</span><span class="sxs-lookup"><span data-stu-id="51567-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51567-148"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51567-148"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51567-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51567-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51567-150">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="51567-150">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="51567-151">**glEvalMesh**</span><span class="sxs-lookup"><span data-stu-id="51567-151">**glEvalMesh**</span></span>](glevalmesh-functions.md)
</dt> <dt>

[<span data-ttu-id="51567-152">**glGet**</span><span class="sxs-lookup"><span data-stu-id="51567-152">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="51567-153">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="51567-153">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="51567-154">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="51567-154">**glMap2**</span></span>](glmap2.md)
</dt> <dt>

[<span data-ttu-id="51567-155">**glMapGrid**</span><span class="sxs-lookup"><span data-stu-id="51567-155">**glMapGrid**</span></span>](glmapgrid-functions.md)
</dt> </dl>

 

 





