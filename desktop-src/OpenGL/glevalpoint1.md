---
title: fonction glEvalPoint1 (GL. h)
description: Les fonctions glEvalPoint1 et glEvalPoint2 génèrent et évaluent un point unique dans une maille. | fonction glEvalPoint1 (GL. h)
ms.assetid: 5ef1d2f0-d77b-4bb8-a0d4-45c1a6a91c18
keywords:
- glEvalPoint1 fonction OpenGL
topic_type:
- apiref
api_name:
- glEvalPoint1
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34b9c3b8e17f5a0554c1864a401ecf49343806c7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103870005"
---
# <a name="glevalpoint1-function"></a><span data-ttu-id="b88fb-105">glEvalPoint1 fonction)</span><span class="sxs-lookup"><span data-stu-id="b88fb-105">glEvalPoint1 function</span></span>

<span data-ttu-id="b88fb-106">Les fonctions [**glEvalPoint1**](glevalpoint.md) et **glEvalPoint2** génèrent et évaluent un point unique dans une maille.</span><span class="sxs-lookup"><span data-stu-id="b88fb-106">The [**glEvalPoint1**](glevalpoint.md) and **glEvalPoint2** functions generate and evaluate a single point in a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="b88fb-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b88fb-107">Syntax</span></span>


```C++
void glEvalPoint1(
   GLint i
);
```



## <a name="parameters"></a><span data-ttu-id="b88fb-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b88fb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b88fb-109">*i*</span><span class="sxs-lookup"><span data-stu-id="b88fb-109">*i*</span></span> 
</dt> <dd>

<span data-ttu-id="b88fb-110">Valeur entière pour la variable de domaine Grid *i*.</span><span class="sxs-lookup"><span data-stu-id="b88fb-110">The integer value for grid domain variable *i*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b88fb-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b88fb-111">Return value</span></span>

<span data-ttu-id="b88fb-112">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="b88fb-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b88fb-113">Notes</span><span class="sxs-lookup"><span data-stu-id="b88fb-113">Remarks</span></span>

<span data-ttu-id="b88fb-114">Les fonctions [**glMapGrid**](glmapgrid-functions.md) et [**glEvalMesh**](glevalmesh-functions.md) sont utilisées en tandem pour générer et évaluer efficacement une série de valeurs de domaine de mappage uniformément espacées.</span><span class="sxs-lookup"><span data-stu-id="b88fb-114">The [**glMapGrid**](glmapgrid-functions.md) and [**glEvalMesh**](glevalmesh-functions.md) functions are used in tandem to efficiently generate and evaluate a series of evenly spaced map domain values.</span></span> <span data-ttu-id="b88fb-115">Vous pouvez utiliser **glEvalPoint** pour évaluer un seul point de grille dans le même Gridspace parcouru par **glEvalMesh**.</span><span class="sxs-lookup"><span data-stu-id="b88fb-115">You can use **glEvalPoint** to evaluate a single grid point in the same gridspace that is traversed by **glEvalMesh**.</span></span> <span data-ttu-id="b88fb-116">L’appel de [**glEvalPoint1**](glevalpoint.md) équivaut à appeler</span><span class="sxs-lookup"><span data-stu-id="b88fb-116">Calling [**glEvalPoint1**](glevalpoint.md) is equivalent to calling</span></span>

<span data-ttu-id="b88fb-117">**glEvalCoord1** (*i* ?*u*  + *u* 1);</span><span class="sxs-lookup"><span data-stu-id="b88fb-117">**glEvalCoord1** (*i* ?*u* +*u* 1 );</span></span>

<span data-ttu-id="b88fb-118">where</span><span class="sxs-lookup"><span data-stu-id="b88fb-118">where</span></span>

<span data-ttu-id="b88fb-119">? *u* = (*u* 2 *u* 1)/*n*</span><span class="sxs-lookup"><span data-stu-id="b88fb-119">?*u* = (*u* 2 *u* 1 )/*n*</span></span>

<span data-ttu-id="b88fb-120">et *n*, *u* 1 et *u* 2 sont les arguments de la fonction **glMapGrid1** la plus récente.</span><span class="sxs-lookup"><span data-stu-id="b88fb-120">and *n*, *u* 1 , and *u* 2 are the arguments to the most recent **glMapGrid1** function.</span></span> <span data-ttu-id="b88fb-121">La seule exigence numérique absolue est que si *i*  =  *n*, la valeur calculée à partir de (*i* ?*u* + U1) est exactement *u* 2.</span><span class="sxs-lookup"><span data-stu-id="b88fb-121">The one absolute numeric requirement is that if *i* = *n*, then the value computed from (*i* ?*u* + u1 ) is exactly *u* 2 .</span></span>

<span data-ttu-id="b88fb-122">Dans le cas à deux dimensions, **glEvalPoint2**, Let</span><span class="sxs-lookup"><span data-stu-id="b88fb-122">In the two-dimensional case, **glEvalPoint2**, let</span></span>

<span data-ttu-id="b88fb-123">? *u* = (*u* 2 *u* 1)/*n*</span><span class="sxs-lookup"><span data-stu-id="b88fb-123">?*u* = (*u* 2 *u* 1 )/*n*</span></span>

<span data-ttu-id="b88fb-124">? *v* = (*v* 2 *v* 1)/*m*</span><span class="sxs-lookup"><span data-stu-id="b88fb-124">?*v* = (*v* 2 *v* 1 )/*m*</span></span>

<span data-ttu-id="b88fb-125">où *n*, *u* 1, *u* 2, *m*, *v* 1 et *v* 2 sont les arguments de la fonction **glMapGrid2** la plus récente.</span><span class="sxs-lookup"><span data-stu-id="b88fb-125">where *n*, *u* 1 , *u* 2 , *m*, *v* 1 , and *v* 2  are the arguments to the most recent **glMapGrid2** function.</span></span> <span data-ttu-id="b88fb-126">La fonction **glEvalPoint2** est alors équivalente à l’appel de</span><span class="sxs-lookup"><span data-stu-id="b88fb-126">Then the **glEvalPoint2** function is equivalent to calling</span></span>

<span data-ttu-id="b88fb-127">**glEvalCoord2** (*i* ?*u*  +  *u* 1, *j* ?*v*  +  *v* 1);</span><span class="sxs-lookup"><span data-stu-id="b88fb-127">**glEvalCoord2** (*i* ?*u* + *u* 1 , *j* ?*v* + *v* 1 );</span></span>

<span data-ttu-id="b88fb-128">Les seules exigences numériques absolues sont que si *i* = *n*, la valeur est calculée à partir de (*i* ?*u*  +  *u* 1) est exactement U2 et, si *j*  =  *m*, la valeur calculée à partir de (*j* ?*v*  +  *v* 1) est exactement *v* 2.</span><span class="sxs-lookup"><span data-stu-id="b88fb-128">The only absolute numeric requirements are that if *i*=*n*, then the value computed from (*i* ?*u* + *u* 1 ) is exactly u2 , and if *j* = *m*, then the value computed from (*j* ?*v* + *v* 1  ) is exactly *v* 2 .</span></span>

<span data-ttu-id="b88fb-129">Les fonctions suivantes récupèrent des informations relatives à [**glEvalPoint1**](glevalpoint.md) et **glEvalPoint2**:</span><span class="sxs-lookup"><span data-stu-id="b88fb-129">The following functions retrieve information relating to [**glEvalPoint1**](glevalpoint.md) and **glEvalPoint2**:</span></span>

<span data-ttu-id="b88fb-130">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Map1 \_ Grid \_ Domain</span><span class="sxs-lookup"><span data-stu-id="b88fb-130">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP1\_GRID\_DOMAIN</span></span>

<span data-ttu-id="b88fb-131">**glGet** avec argument GL \_ map2 \_ Grid \_ Domain</span><span class="sxs-lookup"><span data-stu-id="b88fb-131">**glGet** with argument GL\_MAP2\_GRID\_DOMAIN</span></span>

<span data-ttu-id="b88fb-132">**glGet** avec des \_ segments de \_ grille \_ Map1 d’argument GL</span><span class="sxs-lookup"><span data-stu-id="b88fb-132">**glGet** with argument GL\_MAP1\_GRID\_SEGMENTS</span></span>

<span data-ttu-id="b88fb-133">**glGet** avec des \_ segments de \_ grille \_ map2 d’argument GL</span><span class="sxs-lookup"><span data-stu-id="b88fb-133">**glGet** with argument GL\_MAP2\_GRID\_SEGMENTS</span></span>

## <a name="requirements"></a><span data-ttu-id="b88fb-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b88fb-134">Requirements</span></span>



| <span data-ttu-id="b88fb-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b88fb-135">Requirement</span></span> | <span data-ttu-id="b88fb-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="b88fb-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b88fb-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b88fb-137">Minimum supported client</span></span><br/> | <span data-ttu-id="b88fb-138">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b88fb-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b88fb-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b88fb-139">Minimum supported server</span></span><br/> | <span data-ttu-id="b88fb-140">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b88fb-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b88fb-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="b88fb-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="b88fb-142"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="b88fb-142"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="b88fb-143">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b88fb-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="b88fb-144"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b88fb-144"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b88fb-145">DLL</span><span class="sxs-lookup"><span data-stu-id="b88fb-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b88fb-146"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b88fb-146"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b88fb-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b88fb-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b88fb-148">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="b88fb-148">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="b88fb-149">**glEvalMesh**</span><span class="sxs-lookup"><span data-stu-id="b88fb-149">**glEvalMesh**</span></span>](glevalmesh-functions.md)
</dt> <dt>

[<span data-ttu-id="b88fb-150">**glGet**</span><span class="sxs-lookup"><span data-stu-id="b88fb-150">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="b88fb-151">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="b88fb-151">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="b88fb-152">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="b88fb-152">**glMap2**</span></span>](glmap2.md)
</dt> <dt>

[<span data-ttu-id="b88fb-153">**glMapGrid**</span><span class="sxs-lookup"><span data-stu-id="b88fb-153">**glMapGrid**</span></span>](glmapgrid-functions.md)
</dt> </dl>

 

 





