---
title: fonction glEvalMesh1 (GL. h)
description: Calcule une grille unidimensionnelle de points ou de lignes.
ms.assetid: 176a4b81-f1a7-42fc-8ecd-bba77a0ec5b3
keywords:
- glEvalMesh1 fonction OpenGL
topic_type:
- apiref
api_name:
- glEvalMesh1
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8950dcf397816fca8eb5a6add45c45512c48866
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508786"
---
# <a name="glevalmesh1-function"></a><span data-ttu-id="ae01d-104">glEvalMesh1 fonction)</span><span class="sxs-lookup"><span data-stu-id="ae01d-104">glEvalMesh1 function</span></span>

<span data-ttu-id="ae01d-105">Calcule une grille unidimensionnelle de points ou de lignes.</span><span class="sxs-lookup"><span data-stu-id="ae01d-105">Computes a one-dimensional grid of points or lines.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae01d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ae01d-106">Syntax</span></span>


```C++
void WINAPI glEvalMesh1(
   GLenum mode,
   GLint  i1,
   GLint  i2
);
```



## <a name="parameters"></a><span data-ttu-id="ae01d-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ae01d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae01d-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="ae01d-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="ae01d-109">Valeur qui spécifie s’il faut calculer un maillage unidimensionnel de points ou de lignes.</span><span class="sxs-lookup"><span data-stu-id="ae01d-109">A value that specifies whether to compute a one-dimensional mesh of points or lines.</span></span> <span data-ttu-id="ae01d-110">Les constantes symboliques suivantes sont acceptées : le \_ point GL et la \_ ligne GL.</span><span class="sxs-lookup"><span data-stu-id="ae01d-110">The following symbolic constants are accepted: GL\_POINT and GL\_LINE.</span></span>

</dd> <dt>

<span data-ttu-id="ae01d-111">*I1*</span><span class="sxs-lookup"><span data-stu-id="ae01d-111">*i1*</span></span> 
</dt> <dd>

<span data-ttu-id="ae01d-112">Première valeur entière pour la variable de domaine Grid i.</span><span class="sxs-lookup"><span data-stu-id="ae01d-112">The first integer value for grid domain variable i.</span></span>

</dd> <dt>

<span data-ttu-id="ae01d-113">*I2*</span><span class="sxs-lookup"><span data-stu-id="ae01d-113">*i2*</span></span> 
</dt> <dd>

<span data-ttu-id="ae01d-114">Dernière valeur entière pour la variable de domaine Grid i.</span><span class="sxs-lookup"><span data-stu-id="ae01d-114">The last integer value for grid domain variable i.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae01d-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ae01d-115">Return value</span></span>

<span data-ttu-id="ae01d-116">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="ae01d-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ae01d-117">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="ae01d-117">Error codes</span></span>

<span data-ttu-id="ae01d-118">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="ae01d-118">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="ae01d-119">Nom</span><span class="sxs-lookup"><span data-stu-id="ae01d-119">Name</span></span>                                                                                                  | <span data-ttu-id="ae01d-120">Signification</span><span class="sxs-lookup"><span data-stu-id="ae01d-120">Meaning</span></span>                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ae01d-121"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ae01d-121"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="ae01d-122">Indique que le *mode* n’est pas une valeur acceptée.</span><span class="sxs-lookup"><span data-stu-id="ae01d-122">Indicates that *mode* is not an accepted value.</span></span> <br/>                                                                            |
| <dl> <span data-ttu-id="ae01d-123"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ae01d-123"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="ae01d-124">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="ae01d-124">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="ae01d-125">Notes</span><span class="sxs-lookup"><span data-stu-id="ae01d-125">Remarks</span></span>

<span data-ttu-id="ae01d-126">Utilisez [**glMapGrid**](glmapgrid-functions.md) et [**glEvalMesh**](glevalmesh-functions.md) ensemble pour générer et évaluer efficacement une série de valeurs de domaine de mappage uniformément espacées.</span><span class="sxs-lookup"><span data-stu-id="ae01d-126">Use [**glMapGrid**](glmapgrid-functions.md) and [**glEvalMesh**](glevalmesh-functions.md) together to efficiently generate and evaluate a series of evenly spaced map domain values.</span></span> <span data-ttu-id="ae01d-127">La fonction **glEvalMesh** effectue un pas à pas dans le domaine entier d’une grille unidimensionnelle ou à deux dimensions, dont la plage est le domaine des mappages d’évaluation spécifiés par [**glMap1**](glmap1.md) et [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="ae01d-127">The **glEvalMesh** function steps through the integer domain of a one- or two-dimensional grid, whose range is the domain of the evaluation maps specified by [**glMap1**](glmap1.md) and [**glMap2**](glmap2.md).</span></span> <span data-ttu-id="ae01d-128">Le paramètre mode détermine si les vertex résultants sont connectés en tant que points, lignes ou polygones pleins.</span><span class="sxs-lookup"><span data-stu-id="ae01d-128">The mode parameter determines whether the resulting vertices are connected as points, lines, or filled polygons.</span></span>

<span data-ttu-id="ae01d-129">Dans le cas unidimensionnel, **glEvalMesh1**, la maille est générée comme si le fragment de code suivant était exécuté :</span><span class="sxs-lookup"><span data-stu-id="ae01d-129">In the one-dimensional case, **glEvalMesh1**, the mesh is generated as if the following code fragment were executed:</span></span>

<span data-ttu-id="ae01d-130">[**glBegin**](glbegin.md)(*type*);</span><span class="sxs-lookup"><span data-stu-id="ae01d-130">[**glBegin**](glbegin.md)(*type*);</span></span>

<span data-ttu-id="ae01d-131">pour (i = I1 ; i <= i2 ; i + = 1)</span><span class="sxs-lookup"><span data-stu-id="ae01d-131">for (i = i1; i <= i2; i += 1)</span></span>

<span data-ttu-id="ae01d-132">{</span><span class="sxs-lookup"><span data-stu-id="ae01d-132">{</span></span>

<span data-ttu-id="ae01d-133">[**glEvalCoord1**](glevalcoord1d.md)(i ? u + U1)</span><span class="sxs-lookup"><span data-stu-id="ae01d-133">[**glEvalCoord1**](glevalcoord1d.md)(i?u + u1)</span></span>

<span data-ttu-id="ae01d-134">}</span><span class="sxs-lookup"><span data-stu-id="ae01d-134">}</span></span>

<span data-ttu-id="ae01d-135">[**glEnd**](glend.md)();</span><span class="sxs-lookup"><span data-stu-id="ae01d-135">[**glEnd**](glend.md)( );</span></span>

<span data-ttu-id="ae01d-136">where</span><span class="sxs-lookup"><span data-stu-id="ae01d-136">where</span></span>

<span data-ttu-id="ae01d-137">? u = (U2 U1)/n</span><span class="sxs-lookup"><span data-stu-id="ae01d-137">?u = (u2 u1) / n</span></span>

<span data-ttu-id="ae01d-138">et n, U1 et U2 sont les arguments de la fonction [**glMapGrid1**](glmapgrid1d.md) la plus récente.</span><span class="sxs-lookup"><span data-stu-id="ae01d-138">and n, u1, and u2 are the arguments to the most recent [**glMapGrid1**](glmapgrid1d.md) function.</span></span> <span data-ttu-id="ae01d-139">Le paramètre de *type* est \_ points du GL si le mode est mode GL \_ , ou \_ lignes GL si le mode est \_ ligne GL.</span><span class="sxs-lookup"><span data-stu-id="ae01d-139">The *type* parameter is GL\_POINTS if mode is GL\_POINT, or GL\_LINES if mode is GL\_LINE.</span></span> <span data-ttu-id="ae01d-140">La seule exigence numérique absolue est que si i = n, la valeur calculée à partir de i ? u + U1 est exactement U2.</span><span class="sxs-lookup"><span data-stu-id="ae01d-140">The one absolute numeric requirement is that if i = n, then the value computed from i?u + u1 is exactly u2.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae01d-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ae01d-141">Requirements</span></span>



| <span data-ttu-id="ae01d-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ae01d-142">Requirement</span></span> | <span data-ttu-id="ae01d-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="ae01d-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae01d-144">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ae01d-144">Minimum supported client</span></span><br/> | <span data-ttu-id="ae01d-145">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ae01d-145">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ae01d-146">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ae01d-146">Minimum supported server</span></span><br/> | <span data-ttu-id="ae01d-147">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ae01d-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ae01d-148">En-tête</span><span class="sxs-lookup"><span data-stu-id="ae01d-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae01d-149"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae01d-149"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="ae01d-150">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ae01d-150">Library</span></span><br/>                  | <dl> <span data-ttu-id="ae01d-151"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ae01d-151"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ae01d-152">DLL</span><span class="sxs-lookup"><span data-stu-id="ae01d-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae01d-153"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae01d-153"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae01d-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae01d-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae01d-155">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="ae01d-155">**glBegin**</span></span>](glbegin.md)
</dt> </dl>

 

 





