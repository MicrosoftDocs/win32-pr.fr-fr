---
title: fonction glGetMapdv (GL. h)
description: Les fonctions glGetMapdv, glGetMapfv et glGetMapiv retournent les paramètres de l’évaluateur. | fonction glGetMapdv (GL. h)
ms.assetid: 3b4fc03b-ada4-4f4a-a234-fa6439f2e5c8
keywords:
- glGetMapdv fonction OpenGL
topic_type:
- apiref
api_name:
- glGetMapdv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbf7dd5104ce7a47b0d1215221c115a7191f4548
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106527728"
---
# <a name="glgetmapdv-function"></a><span data-ttu-id="452cd-105">glGetMapdv fonction)</span><span class="sxs-lookup"><span data-stu-id="452cd-105">glGetMapdv function</span></span>

<span data-ttu-id="452cd-106">Les fonctions **glGetMapdv**, [**glGetMapfv**](glgetmapfv.md)et [**glGetMapiv**](glgetmapiv.md) retournent les paramètres de l’évaluateur.</span><span class="sxs-lookup"><span data-stu-id="452cd-106">The **glGetMapdv**, [**glGetMapfv**](glgetmapfv.md), and [**glGetMapiv**](glgetmapiv.md) functions return evaluator parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="452cd-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="452cd-107">Syntax</span></span>


```C++
void WINAPI glGetMapdv(
   GLenum   target,
   GLenum   query,
   GLdouble *v
);
```



## <a name="parameters"></a><span data-ttu-id="452cd-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="452cd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="452cd-109">*cible*</span><span class="sxs-lookup"><span data-stu-id="452cd-109">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="452cd-110">Nom symbolique d’une carte.</span><span class="sxs-lookup"><span data-stu-id="452cd-110">The symbolic name of a map.</span></span> <span data-ttu-id="452cd-111">Les valeurs acceptées sont les suivantes : GL \_ Map1 \_ couleur \_ 4, \_ index GL Map1 \_ , GL \_ Map1 \_ normal, GL \_ Map1 \_ texture \_ Coord \_ 1, GL \_ Map1 \_ texture \_ Coord \_ 2, GL \_ Map1 \_ texture \_ Coord \_ 3, GL \_ Map1 \_ texture \_ Coord \_ 4, GL \_ Map1 \_ vertex \_ 3, GL \_ Map1 \_ vertex \_ 4, GL map2 couleur 4, GL map2 index, GL map2 normal, GL map2 texture Coord 1, GL map2 texture Coord \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ 2, GL map2 texture Coord \_ \_ \_ \_ \_ \_ \_ \_ 3, GL \_ map2 texture Coord \_ \_ \_ 4, GL \_ map2 \_ vertex \_ 3 et GL \_ map2 \_ vertex \_ 4.</span><span class="sxs-lookup"><span data-stu-id="452cd-111">The following are accepted values: GL\_MAP1\_COLOR\_4, GL\_MAP1\_INDEX, GL\_MAP1\_NORMAL, GL\_MAP1\_TEXTURE\_COORD\_1, GL\_MAP1\_TEXTURE\_COORD\_2, GL\_MAP1\_TEXTURE\_COORD\_3, GL\_MAP1\_TEXTURE\_COORD\_4, GL\_MAP1\_VERTEX\_3, GL\_MAP1\_VERTEX\_4, GL\_MAP2\_COLOR\_4, GL\_MAP2\_INDEX, GL\_MAP2\_NORMAL, GL\_MAP2\_TEXTURE\_COORD\_1, GL\_MAP2\_TEXTURE\_COORD\_2, GL\_MAP2\_TEXTURE\_COORD\_3, GL\_MAP2\_TEXTURE\_COORD\_4, GL\_MAP2\_VERTEX\_3, and GL\_MAP2\_VERTEX\_4.</span></span>

</dd> <dt>

<span data-ttu-id="452cd-112">*query*</span><span class="sxs-lookup"><span data-stu-id="452cd-112">*query*</span></span> 
</dt> <dd>

<span data-ttu-id="452cd-113">Spécifie le paramètre à retourner.</span><span class="sxs-lookup"><span data-stu-id="452cd-113">Specifies which parameter to return.</span></span> <span data-ttu-id="452cd-114">Les noms symboliques suivants sont acceptés.</span><span class="sxs-lookup"><span data-stu-id="452cd-114">The following symbolic names are accepted.</span></span>



| <span data-ttu-id="452cd-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="452cd-115">Value</span></span>                                                                                                                                             | <span data-ttu-id="452cd-116">Signification</span><span class="sxs-lookup"><span data-stu-id="452cd-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COEFF"></span><span id="gl_coeff"></span><dl> <span data-ttu-id="452cd-117"><dt>**\_Coeff GL**</dt></span><span class="sxs-lookup"><span data-stu-id="452cd-117"><dt>**GL\_COEFF**</dt></span></span> </dl>    | <span data-ttu-id="452cd-118">Le paramètre *v* retourne les points de contrôle de la fonction évaluateur.</span><span class="sxs-lookup"><span data-stu-id="452cd-118">The *v* parameter returns the control points for the evaluator function.</span></span> <span data-ttu-id="452cd-119">Les évaluateurs unidimensionnels retournent des points de contrôle d' *ordre* et les évaluateurs à deux dimensions retournent des points de contrôle *uorder* *x* *Vorder* .</span><span class="sxs-lookup"><span data-stu-id="452cd-119">One-dimensional evaluators return *order* control points, and two-dimensional evaluators return *uorder* *x* *vorder* control points.</span></span> <span data-ttu-id="452cd-120">Chaque point de contrôle est constitué d’un, deux, trois ou quatre valeurs à virgule flottante, à virgule flottante simple précision ou à virgule flottante double précision, selon le type de l’évaluateur.</span><span class="sxs-lookup"><span data-stu-id="452cd-120">Each control point consists of one, two, three, or four integer, single-precision floating-point, or double-precision floating-point values, depending on the type of the evaluator.</span></span> <span data-ttu-id="452cd-121">Les points de contrôle à deux dimensions sont retournés dans l’ordre ligne-principal, ce qui incrémente rapidement l’index *uorder* et l’index *Vorder* après chaque ligne.</span><span class="sxs-lookup"><span data-stu-id="452cd-121">Two-dimensional control points are returned in row-major order, incrementing the *uorder* index quickly, and the *vorder* index after each row.</span></span> <span data-ttu-id="452cd-122">Les valeurs entières, quand elles sont demandées, sont calculées en arrondissant les valeurs à virgule flottante internes aux valeurs entières les plus proches.</span><span class="sxs-lookup"><span data-stu-id="452cd-122">Integer values, when requested, are computed by rounding the internal floating-point values to the nearest integer values.</span></span><br/> |
| <span id="GL_ORDER"></span><span id="gl_order"></span><dl> <span data-ttu-id="452cd-123"><dt>**\_commande GL**</dt></span><span class="sxs-lookup"><span data-stu-id="452cd-123"><dt>**GL\_ORDER**</dt></span></span> </dl>    | <span data-ttu-id="452cd-124">Le paramètre *v* retourne l’ordre de la fonction évaluateur.</span><span class="sxs-lookup"><span data-stu-id="452cd-124">The *v* parameter returns the order of the evaluator function.</span></span> <span data-ttu-id="452cd-125">Les évaluateurs unidimensionnels retournent une valeur unique, *Order*.</span><span class="sxs-lookup"><span data-stu-id="452cd-125">One-dimensional evaluators return a single value, *order*.</span></span> <span data-ttu-id="452cd-126">Les évaluateurs à deux dimensions retournent deux valeurs, *uorder* et *Vorder*.</span><span class="sxs-lookup"><span data-stu-id="452cd-126">Two-dimensional evaluators return two values, *uorder* and *vorder*.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="GL_DOMAIN"></span><span id="gl_domain"></span><dl> <span data-ttu-id="452cd-127"><dt>**\_domaine GL**</dt></span><span class="sxs-lookup"><span data-stu-id="452cd-127"><dt>**GL\_DOMAIN**</dt></span></span> </dl> | <span data-ttu-id="452cd-128">Le paramètre *v* retourne les paramètres de mappage linéaires *u* et *v* .</span><span class="sxs-lookup"><span data-stu-id="452cd-128">The *v* parameter returns the linear *u* and *v* mapping parameters.</span></span> <span data-ttu-id="452cd-129">Les évaluateurs unidimensionnels retournent deux valeurs, *u* 1 et *u* 2, comme spécifié par [**glMap1**](glmap1.md).</span><span class="sxs-lookup"><span data-stu-id="452cd-129">One-dimensional evaluators return two values, *u* 1 and *u* 2, as specified by [**glMap1**](glmap1.md).</span></span> <span data-ttu-id="452cd-130">Les évaluateurs à deux dimensions retournent quatre valeurs (*U1*, *U2*, *v1* et *v2*), comme spécifié par [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="452cd-130">Two-dimensional evaluators return four values (*u1*, *u2*, *v1*, and *v2*) as specified by [**glMap2**](glmap2.md).</span></span> <span data-ttu-id="452cd-131">Les valeurs entières, quand elles sont demandées, sont calculées en arrondissant les valeurs à virgule flottante internes aux valeurs entières les plus proches.</span><span class="sxs-lookup"><span data-stu-id="452cd-131">Integer values, when requested, are computed by rounding the internal floating-point values to the nearest integer values.</span></span><br/>                                                                                                                                                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="452cd-132">*v*</span><span class="sxs-lookup"><span data-stu-id="452cd-132">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="452cd-133">Retourne les données demandées.</span><span class="sxs-lookup"><span data-stu-id="452cd-133">Returns the requested data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="452cd-134">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="452cd-134">Return value</span></span>

<span data-ttu-id="452cd-135">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="452cd-135">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="452cd-136">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="452cd-136">Error codes</span></span>

<span data-ttu-id="452cd-137">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="452cd-137">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="452cd-138">Nom</span><span class="sxs-lookup"><span data-stu-id="452cd-138">Name</span></span>                                                                                                  | <span data-ttu-id="452cd-139">Signification</span><span class="sxs-lookup"><span data-stu-id="452cd-139">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="452cd-140"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="452cd-140"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="452cd-141">la *cible* ou la *requête* n’était pas une valeur acceptée.</span><span class="sxs-lookup"><span data-stu-id="452cd-141">*target* or *query* was not an accepted value.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="452cd-142"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="452cd-142"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="452cd-143">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="452cd-143">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="452cd-144">Notes</span><span class="sxs-lookup"><span data-stu-id="452cd-144">Remarks</span></span>

<span data-ttu-id="452cd-145">La fonction **glGetMap** retourne les paramètres de l’évaluateur.</span><span class="sxs-lookup"><span data-stu-id="452cd-145">The **glGetMap** function returns evaluator parameters.</span></span> <span data-ttu-id="452cd-146">(Les fonctions **glMap1** et **glMap2** définissent les évaluateurs.) Le paramètre *target* spécifie un mappage, la *requête* sélectionne un paramètre spécifique, et *v* pointe vers le stockage où les valeurs sont retournées.</span><span class="sxs-lookup"><span data-stu-id="452cd-146">(The **glMap1** and **glMap2** functions define evaluators.) The *target* parameter specifies a map, *query* selects a specific parameter, and *v* points to storage where the values will be returned.</span></span>

<span data-ttu-id="452cd-147">Les valeurs acceptables pour le paramètre *target* sont décrites dans [**glMap1**](glmap1.md) et [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="452cd-147">The acceptable values for the *target* parameter are described in [**glMap1**](glmap1.md) and [**glMap2**](glmap2.md).</span></span>

<span data-ttu-id="452cd-148">Si une erreur est générée, aucune modification n’est apportée au contenu de *v*.</span><span class="sxs-lookup"><span data-stu-id="452cd-148">If an error is generated, no change is made to the contents of *v*.</span></span>

## <a name="requirements"></a><span data-ttu-id="452cd-149">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="452cd-149">Requirements</span></span>



| <span data-ttu-id="452cd-150">Condition requise</span><span class="sxs-lookup"><span data-stu-id="452cd-150">Requirement</span></span> | <span data-ttu-id="452cd-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="452cd-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="452cd-152">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="452cd-152">Minimum supported client</span></span><br/> | <span data-ttu-id="452cd-153">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="452cd-153">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="452cd-154">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="452cd-154">Minimum supported server</span></span><br/> | <span data-ttu-id="452cd-155">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="452cd-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="452cd-156">En-tête</span><span class="sxs-lookup"><span data-stu-id="452cd-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="452cd-157"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="452cd-157"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="452cd-158">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="452cd-158">Library</span></span><br/>                  | <dl> <span data-ttu-id="452cd-159"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="452cd-159"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="452cd-160">DLL</span><span class="sxs-lookup"><span data-stu-id="452cd-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="452cd-161"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="452cd-161"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="452cd-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="452cd-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="452cd-163">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="452cd-163">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="452cd-164">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="452cd-164">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="452cd-165">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="452cd-165">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="452cd-166">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="452cd-166">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="452cd-167">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="452cd-167">**glMap2**</span></span>](glmap2.md)
</dt> </dl>

 

 





