---
title: fonction glLoadMatrixd (GL. h)
description: La fonction glLoadMatrixd remplace la matrice actuelle par une matrice arbitraire. | fonction glLoadMatrixd (GL. h)
ms.assetid: 66c499f7-3f55-4de2-b67b-5b775b5854e0
keywords:
- glLoadMatrixd fonction OpenGL
topic_type:
- apiref
api_name:
- glLoadMatrixd
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4715da159dff60024adb3c7331cbf03c7c3759ce
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106522294"
---
# <a name="glloadmatrixd-function"></a><span data-ttu-id="11c08-105">glLoadMatrixd fonction)</span><span class="sxs-lookup"><span data-stu-id="11c08-105">glLoadMatrixd function</span></span>

<span data-ttu-id="11c08-106">Les fonctions **glLoadMatrixd** et [**glLoadMatrixf**](glloadmatrixf.md) remplacent la matrice actuelle par une matrice arbitraire.</span><span class="sxs-lookup"><span data-stu-id="11c08-106">The **glLoadMatrixd** and [**glLoadMatrixf**](glloadmatrixf.md) functions replace the current matrix with an arbitrary matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="11c08-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="11c08-107">Syntax</span></span>


```C++
void WINAPI glLoadMatrixd(
   const GLdouble *m
);
```



## <a name="parameters"></a><span data-ttu-id="11c08-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="11c08-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11c08-109">*m*</span><span class="sxs-lookup"><span data-stu-id="11c08-109">*m*</span></span> 
</dt> <dd>

<span data-ttu-id="11c08-110">Pointeur vers une matrice 4x4 stockée dans la colonne dans l’ordre décroissant de 16 valeurs consécutives.</span><span class="sxs-lookup"><span data-stu-id="11c08-110">A pointer to a 4x4 matrix stored in column-major order as 16 consecutive values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11c08-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="11c08-111">Return value</span></span>

<span data-ttu-id="11c08-112">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="11c08-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="11c08-113">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="11c08-113">Error codes</span></span>

<span data-ttu-id="11c08-114">Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="11c08-114">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="11c08-115">Nom</span><span class="sxs-lookup"><span data-stu-id="11c08-115">Name</span></span>                                                                                                  | <span data-ttu-id="11c08-116">Signification</span><span class="sxs-lookup"><span data-stu-id="11c08-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="11c08-117"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="11c08-117"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="11c08-118">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="11c08-118">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="11c08-119">Notes</span><span class="sxs-lookup"><span data-stu-id="11c08-119">Remarks</span></span>

<span data-ttu-id="11c08-120">La fonction **glLoadMatrix** remplace la matrice actuelle par celle spécifiée dans *m*.</span><span class="sxs-lookup"><span data-stu-id="11c08-120">The **glLoadMatrix** function replaces the current matrix with the one specified in *m*.</span></span> <span data-ttu-id="11c08-121">La matrice actuelle est la matrice de projection, la matrice modelview ou la matrice de texture, déterminée par le mode matrice en cours (voir [**glMatrixMode**](glmatrixmode.md)).</span><span class="sxs-lookup"><span data-stu-id="11c08-121">The current matrix is the projection matrix, modelview matrix, or texture matrix, determined by the current matrix mode (see [**glMatrixMode**](glmatrixmode.md)).</span></span>

<span data-ttu-id="11c08-122">Le paramètre *m* pointe vers une matrice 4x4 de valeurs à virgule flottante simple précision ou à virgule flottante double précision stockées dans l’ordre des colonnes.</span><span class="sxs-lookup"><span data-stu-id="11c08-122">The *m* parameter points to a 4x4 matrix of single-precision or double-precision floating-point values stored in column-major order.</span></span> <span data-ttu-id="11c08-123">Autrement dit, la matrice est stockée comme indiqué dans l’image suivante.</span><span class="sxs-lookup"><span data-stu-id="11c08-123">That is, the matrix is stored as shown in the following image.</span></span>

![Diagramme montrant la matrice 4x4 vers laquelle pointe le paramètre m.](images/load02.png)

<span data-ttu-id="11c08-125">Les fonctions suivantes récupèrent les informations relatives à **glLoadMatrix**:</span><span class="sxs-lookup"><span data-stu-id="11c08-125">The following functions retrieve information related to **glLoadMatrix**:</span></span>

<span data-ttu-id="11c08-126">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec l’argument \_ mode de matrice GL \_</span><span class="sxs-lookup"><span data-stu-id="11c08-126">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="11c08-127">**glGet** avec argument GL \_ MODELVIEW \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="11c08-127">**glGet** with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="11c08-128">**glGet** avec argument \_ matrice de projection de la comptabilité \_</span><span class="sxs-lookup"><span data-stu-id="11c08-128">**glGet** with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="11c08-129">matrice de texture **glGet** avec argument GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="11c08-129">**glGet** with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="11c08-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="11c08-130">Requirements</span></span>



| <span data-ttu-id="11c08-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="11c08-131">Requirement</span></span> | <span data-ttu-id="11c08-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="11c08-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="11c08-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="11c08-133">Minimum supported client</span></span><br/> | <span data-ttu-id="11c08-134">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="11c08-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="11c08-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="11c08-135">Minimum supported server</span></span><br/> | <span data-ttu-id="11c08-136">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="11c08-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="11c08-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="11c08-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="11c08-138"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="11c08-138"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="11c08-139">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="11c08-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="11c08-140"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="11c08-140"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="11c08-141">DLL</span><span class="sxs-lookup"><span data-stu-id="11c08-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11c08-142"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11c08-142"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11c08-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="11c08-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11c08-144">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="11c08-144">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="11c08-145">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="11c08-145">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="11c08-146">**glLoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="11c08-146">**glLoadIdentity**</span></span>](glloadidentity.md)
</dt> <dt>

[<span data-ttu-id="11c08-147">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="11c08-147">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="11c08-148">**glMultMatrix**</span><span class="sxs-lookup"><span data-stu-id="11c08-148">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="11c08-149">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="11c08-149">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> </dl>

 

 





