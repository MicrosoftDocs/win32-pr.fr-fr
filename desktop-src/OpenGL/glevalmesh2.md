---
title: fonction glEvalMesh2 (GL. h)
description: Calcule une grille à deux dimensions de points ou de lignes.
ms.assetid: 21e94388-903e-4b9d-8e54-9c914d0ce372
keywords:
- glEvalMesh2 fonction OpenGL
topic_type:
- apiref
api_name:
- glEvalMesh2
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 531e9f1f6288116d052c728654cd2cf03f38550a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740669"
---
# <a name="glevalmesh2-function"></a><span data-ttu-id="b6119-104">glEvalMesh2 fonction)</span><span class="sxs-lookup"><span data-stu-id="b6119-104">glEvalMesh2 function</span></span>

<span data-ttu-id="b6119-105">Calcule une grille à deux dimensions de points ou de lignes.</span><span class="sxs-lookup"><span data-stu-id="b6119-105">Computes a two-dimensional grid of points or lines.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6119-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b6119-106">Syntax</span></span>


```C++
void WINAPI glEvalMesh2(
   GLenum mode,
   GLint  i1,
   GLint  i2,
   GLint  j1,
   GLint  j2
);
```



## <a name="parameters"></a><span data-ttu-id="b6119-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b6119-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6119-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="b6119-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="b6119-109">Valeur qui spécifie s’il faut calculer un maillage à deux dimensions de points, de lignes ou de polygones.</span><span class="sxs-lookup"><span data-stu-id="b6119-109">A value that specifies whether to compute a two-dimensional mesh of points, lines, or polygons.</span></span> <span data-ttu-id="b6119-110">Les constantes symboliques suivantes sont acceptées : \_ point GL, \_ ligne GL et \_ remplissage GL.</span><span class="sxs-lookup"><span data-stu-id="b6119-110">The following symbolic constants are accepted: GL\_POINT, GL\_LINE, and GL\_FILL.</span></span>

</dd> <dt>

<span data-ttu-id="b6119-111">*I1*</span><span class="sxs-lookup"><span data-stu-id="b6119-111">*i1*</span></span> 
</dt> <dd>

<span data-ttu-id="b6119-112">Première valeur entière pour la variable de domaine Grid i.</span><span class="sxs-lookup"><span data-stu-id="b6119-112">The first integer value for grid domain variable i.</span></span>

</dd> <dt>

<span data-ttu-id="b6119-113">*I2*</span><span class="sxs-lookup"><span data-stu-id="b6119-113">*i2*</span></span> 
</dt> <dd>

<span data-ttu-id="b6119-114">Dernière valeur entière pour la variable de domaine Grid i.</span><span class="sxs-lookup"><span data-stu-id="b6119-114">The last integer value for grid domain variable i.</span></span>

</dd> <dt>

<span data-ttu-id="b6119-115">*j1*</span><span class="sxs-lookup"><span data-stu-id="b6119-115">*j1*</span></span> 
</dt> <dd>

<span data-ttu-id="b6119-116">Première valeur entière pour la variable de domaine Grid j.</span><span class="sxs-lookup"><span data-stu-id="b6119-116">The first integer value for grid domain variable j.</span></span>

</dd> <dt>

<span data-ttu-id="b6119-117">*J2*</span><span class="sxs-lookup"><span data-stu-id="b6119-117">*j2*</span></span> 
</dt> <dd>

<span data-ttu-id="b6119-118">Dernière valeur entière pour la variable de domaine Grid j.</span><span class="sxs-lookup"><span data-stu-id="b6119-118">The last integer value for grid domain variable j.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6119-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b6119-119">Return value</span></span>

<span data-ttu-id="b6119-120">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="b6119-120">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b6119-121">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="b6119-121">Error codes</span></span>

<span data-ttu-id="b6119-122">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="b6119-122">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="b6119-123">Nom</span><span class="sxs-lookup"><span data-stu-id="b6119-123">Name</span></span>                                                                                                  | <span data-ttu-id="b6119-124">Signification</span><span class="sxs-lookup"><span data-stu-id="b6119-124">Meaning</span></span>                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b6119-125"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b6119-125"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="b6119-126">Indique que le *mode* n’est pas une valeur acceptée.</span><span class="sxs-lookup"><span data-stu-id="b6119-126">Indicates that *mode* is not an accepted value.</span></span> <br/>                                                                            |
| <dl> <span data-ttu-id="b6119-127"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b6119-127"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="b6119-128">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="b6119-128">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="b6119-129">Notes</span><span class="sxs-lookup"><span data-stu-id="b6119-129">Remarks</span></span>

<span data-ttu-id="b6119-130">Utilisez [**glMapGrid**](glmapgrid-functions.md) et [**glEvalMesh**](glevalmesh-functions.md) en tandem pour générer et évaluer efficacement une série de valeurs de domaine de mappage uniformément espacées.</span><span class="sxs-lookup"><span data-stu-id="b6119-130">Use [**glMapGrid**](glmapgrid-functions.md) and [**glEvalMesh**](glevalmesh-functions.md) in tandem to efficiently generate and evaluate a series of evenly spaced map domain values.</span></span> <span data-ttu-id="b6119-131">La fonction **glEvalMesh** effectue un pas à pas dans le domaine entier d’une grille unidimensionnelle ou à deux dimensions, dont la plage est le domaine des mappages d’évaluation spécifiés par [**glMap1**](glmap1.md) et [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="b6119-131">The **glEvalMesh** function steps through the integer domain of a one- or two-dimensional grid, whose range is the domain of the evaluation maps specified by [**glMap1**](glmap1.md) and [**glMap2**](glmap2.md).</span></span> <span data-ttu-id="b6119-132">Le paramètre mode détermine si les vertex résultants sont connectés en tant que points, lignes ou polygones pleins.</span><span class="sxs-lookup"><span data-stu-id="b6119-132">The mode parameter determines whether the resulting vertices are connected as points, lines, or filled polygons.</span></span>

<span data-ttu-id="b6119-133">Dans le cas à deux dimensions, **glEvalMesh2**, Let</span><span class="sxs-lookup"><span data-stu-id="b6119-133">In the two-dimensional case, **glEvalMesh2**, let</span></span>

<span data-ttu-id="b6119-134">?</span><span class="sxs-lookup"><span data-stu-id="b6119-134">?</span></span> <span data-ttu-id="b6119-135">u = (U2 U1)/n</span><span class="sxs-lookup"><span data-stu-id="b6119-135">u = (u2 u1)/n</span></span>

<span data-ttu-id="b6119-136">?</span><span class="sxs-lookup"><span data-stu-id="b6119-136">?</span></span> <span data-ttu-id="b6119-137">v = (V2 V1)/m,</span><span class="sxs-lookup"><span data-stu-id="b6119-137">v = (v2 v1)/m,</span></span>

<span data-ttu-id="b6119-138">où n, U1, U2, m, v1 et v2 sont les arguments de la fonction [**glMapGrid2**](glmapgrid-functions.md) la plus récente.</span><span class="sxs-lookup"><span data-stu-id="b6119-138">where n, u1, u2, m, v1, and v2 are the arguments to the most recent [**glMapGrid2**](glmapgrid-functions.md) function.</span></span> <span data-ttu-id="b6119-139">Ensuite, si le *mode* est \_ remplissage GL, **glEvalMesh2** est équivalent à :</span><span class="sxs-lookup"><span data-stu-id="b6119-139">Then, if *mode* is GL\_FILL, **glEvalMesh2** is equivalent to:</span></span>

<span data-ttu-id="b6119-140">pour (j = J1 ; j < J2 ; j + = 1)</span><span class="sxs-lookup"><span data-stu-id="b6119-140">for (j = j1; j < j2; j += 1)</span></span>

<span data-ttu-id="b6119-141">{</span><span class="sxs-lookup"><span data-stu-id="b6119-141">{</span></span>

<span data-ttu-id="b6119-142">[**glBegin**](glbegin.md)( \_ bande à quatre processeurs GL \_ );</span><span class="sxs-lookup"><span data-stu-id="b6119-142">[**glBegin**](glbegin.md)(GL\_QUAD\_STRIP);</span></span>

<span data-ttu-id="b6119-143">pour (i = I1 ; i <= i2 ; i + = 1)</span><span class="sxs-lookup"><span data-stu-id="b6119-143">for (i = i1; i <= i2; i += 1)</span></span>

<span data-ttu-id="b6119-144">{</span><span class="sxs-lookup"><span data-stu-id="b6119-144">{</span></span>

<span data-ttu-id="b6119-145">[**glEvalCoord2**](glevalcoord2d.md)(i ? u + U1 (), j ?</span><span class="sxs-lookup"><span data-stu-id="b6119-145">[**glEvalCoord2**](glevalcoord2d.md)(i? u + u1 ( ) , j ?</span></span> <span data-ttu-id="b6119-146">v + v1);</span><span class="sxs-lookup"><span data-stu-id="b6119-146">v + v1);</span></span>

<span data-ttu-id="b6119-147">[**glEvalCoord2**](glevalcoord2d.md)(i ? u + U1 (), (j + 1) ?</span><span class="sxs-lookup"><span data-stu-id="b6119-147">[**glEvalCoord2**](glevalcoord2d.md)(i? u + u1 ( ) , (j+1) ?</span></span> <span data-ttu-id="b6119-148">v + v1);</span><span class="sxs-lookup"><span data-stu-id="b6119-148">v + v1);</span></span>

<span data-ttu-id="b6119-149">}</span><span class="sxs-lookup"><span data-stu-id="b6119-149">}</span></span>

<span data-ttu-id="b6119-150">[**glEnd**](glend.md)(); }</span><span class="sxs-lookup"><span data-stu-id="b6119-150">[**glEnd**](glend.md)( ); }</span></span>

<span data-ttu-id="b6119-151">Si le *mode* est \_ line GL, un appel à **glEvalMesh2** est équivalent à :</span><span class="sxs-lookup"><span data-stu-id="b6119-151">If *mode* is GL\_LINE, then a call to **glEvalMesh2** is equivalent to:</span></span>

<span data-ttu-id="b6119-152">pour (j = J1 ; j <= J2 ; j + = 1)</span><span class="sxs-lookup"><span data-stu-id="b6119-152">for (j = j1; j <= j2; j += 1)</span></span>

<span data-ttu-id="b6119-153">{</span><span class="sxs-lookup"><span data-stu-id="b6119-153">{</span></span>

<span data-ttu-id="b6119-154">[**glBegin**](glbegin.md)( \_ bande de lignes GL \_ );</span><span class="sxs-lookup"><span data-stu-id="b6119-154">[**glBegin**](glbegin.md)(GL\_LINE\_STRIP);</span></span>

<span data-ttu-id="b6119-155">pour (i = I1 ; i <= i2 ; i + = 1)</span><span class="sxs-lookup"><span data-stu-id="b6119-155">for (i = i1; i <= i2; i += 1)</span></span>

<span data-ttu-id="b6119-156">{</span><span class="sxs-lookup"><span data-stu-id="b6119-156">{</span></span>

<span data-ttu-id="b6119-157">[**glEvalCoord2**](glevalcoord2d.md)(i ? u + U1, j ? v + v1);</span><span class="sxs-lookup"><span data-stu-id="b6119-157">[**glEvalCoord2**](glevalcoord2d.md)(i? u + u1, j? v + v1);</span></span>

<span data-ttu-id="b6119-158">}</span><span class="sxs-lookup"><span data-stu-id="b6119-158">}</span></span>

<span data-ttu-id="b6119-159">[**glEnd**](glend.md)();</span><span class="sxs-lookup"><span data-stu-id="b6119-159">[**glEnd**](glend.md)( );</span></span>

<span data-ttu-id="b6119-160">}</span><span class="sxs-lookup"><span data-stu-id="b6119-160">}</span></span>

<span data-ttu-id="b6119-161">pour (i = I1 ; i <= i2 ; i + = 1)</span><span class="sxs-lookup"><span data-stu-id="b6119-161">for (i = i1; i <= i2; i += 1)</span></span>

<span data-ttu-id="b6119-162">{</span><span class="sxs-lookup"><span data-stu-id="b6119-162">{</span></span>

<span data-ttu-id="b6119-163">[**glBegin**](glbegin.md)( \_ bande de lignes GL \_ );</span><span class="sxs-lookup"><span data-stu-id="b6119-163">[**glBegin**](glbegin.md)(GL\_LINE\_STRIP);</span></span>

<span data-ttu-id="b6119-164">pour (j = J1 ; j <= J1 ; j + = 1)</span><span class="sxs-lookup"><span data-stu-id="b6119-164">for (j = j1; j <= j1; j += 1)</span></span>

<span data-ttu-id="b6119-165">{</span><span class="sxs-lookup"><span data-stu-id="b6119-165">{</span></span>

<span data-ttu-id="b6119-166">[**glEvalCoord2**](glevalcoord2d.md)(i ? u + U1, j ? v + v1);</span><span class="sxs-lookup"><span data-stu-id="b6119-166">[**glEvalCoord2**](glevalcoord2d.md)(i? u + u1, j? v + v1);</span></span>

<span data-ttu-id="b6119-167">}</span><span class="sxs-lookup"><span data-stu-id="b6119-167">}</span></span>

<span data-ttu-id="b6119-168">glEnd( );</span><span class="sxs-lookup"><span data-stu-id="b6119-168">glEnd( );</span></span>

<span data-ttu-id="b6119-169">}</span><span class="sxs-lookup"><span data-stu-id="b6119-169">}</span></span>

<span data-ttu-id="b6119-170">Enfin, si le *mode* est \_ point GL, un appel à **glEvalMesh2** est équivalent à :</span><span class="sxs-lookup"><span data-stu-id="b6119-170">And finally, if *mode* is GL\_POINT, then a call to **glEvalMesh2** is equivalent to:</span></span>

<span data-ttu-id="b6119-171">[**glBegin**](glbegin.md)(points du GL \_ );</span><span class="sxs-lookup"><span data-stu-id="b6119-171">[**glBegin**](glbegin.md)(GL\_POINTS);</span></span>

<span data-ttu-id="b6119-172">pour (j = J1 ; j <= J2 ; j + = 1)</span><span class="sxs-lookup"><span data-stu-id="b6119-172">for (j = j1; j <= j2; j += 1)</span></span>

<span data-ttu-id="b6119-173">{</span><span class="sxs-lookup"><span data-stu-id="b6119-173">{</span></span>

<span data-ttu-id="b6119-174">pour (i = I1 ; i <= i2 ; i + = 1)</span><span class="sxs-lookup"><span data-stu-id="b6119-174">for (i = i1; i <= i2; i += 1)</span></span>

<span data-ttu-id="b6119-175">{</span><span class="sxs-lookup"><span data-stu-id="b6119-175">{</span></span>

<span data-ttu-id="b6119-176">[**glEvalCoord2**](glevalcoord2d.md)(i ? u + U1, j ? v + v1);</span><span class="sxs-lookup"><span data-stu-id="b6119-176">[**glEvalCoord2**](glevalcoord2d.md)(i? u + u1, j? v + v1);</span></span>

<span data-ttu-id="b6119-177">}</span><span class="sxs-lookup"><span data-stu-id="b6119-177">}</span></span>

<span data-ttu-id="b6119-178">}</span><span class="sxs-lookup"><span data-stu-id="b6119-178">}</span></span>

<span data-ttu-id="b6119-179">[**glEnd**](glend.md)();</span><span class="sxs-lookup"><span data-stu-id="b6119-179">[**glEnd**](glend.md)( );</span></span>

<span data-ttu-id="b6119-180">Dans les trois cas, les seules exigences numériques absolues sont que si i = n, la valeur est calculée à partir de i ? u + U1 est exactement U2 et, si j = m, la valeur est-elle calculée à partir de j ? v + v1 est exactement v2.</span><span class="sxs-lookup"><span data-stu-id="b6119-180">In all three cases, the only absolute numeric requirements are that if i = n, then the value computed from i? u + u1 is exactly u2, and if j = m, then the value computed from j? v + v1 is exactly v2.</span></span> <span data-ttu-id="b6119-181">Les fonctions suivantes récupèrent des informations relatives à **glEvalMesh**:</span><span class="sxs-lookup"><span data-stu-id="b6119-181">The following functions retrieve information relating to **glEvalMesh**:</span></span>

<span data-ttu-id="b6119-182">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Map1 \_ Grid \_ Domain</span><span class="sxs-lookup"><span data-stu-id="b6119-182">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP1\_GRID\_DOMAIN</span></span>

<span data-ttu-id="b6119-183">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ map2 \_ Grid \_ Domain</span><span class="sxs-lookup"><span data-stu-id="b6119-183">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP2\_GRID\_DOMAIN</span></span>

<span data-ttu-id="b6119-184">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec des \_ segments de \_ grille \_ Map1 d’argument GL</span><span class="sxs-lookup"><span data-stu-id="b6119-184">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP1\_GRID\_SEGMENTS</span></span>

<span data-ttu-id="b6119-185">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec des \_ segments de \_ grille \_ map2 d’argument GL</span><span class="sxs-lookup"><span data-stu-id="b6119-185">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP2\_GRID\_SEGMENTS</span></span>

## <a name="requirements"></a><span data-ttu-id="b6119-186">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b6119-186">Requirements</span></span>



| <span data-ttu-id="b6119-187">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b6119-187">Requirement</span></span> | <span data-ttu-id="b6119-188">Valeur</span><span class="sxs-lookup"><span data-stu-id="b6119-188">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b6119-189">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b6119-189">Minimum supported client</span></span><br/> | <span data-ttu-id="b6119-190">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b6119-190">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b6119-191">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b6119-191">Minimum supported server</span></span><br/> | <span data-ttu-id="b6119-192">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b6119-192">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b6119-193">En-tête</span><span class="sxs-lookup"><span data-stu-id="b6119-193">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6119-194"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6119-194"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="b6119-195">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b6119-195">Library</span></span><br/>                  | <dl> <span data-ttu-id="b6119-196"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b6119-196"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b6119-197">DLL</span><span class="sxs-lookup"><span data-stu-id="b6119-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6119-198"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6119-198"><dt>Opengl32.dll</dt></span></span> </dl> |



 

 





