---
title: fonction glMultMatrixf (GL. h)
description: La fonction glMultMatrixf multiplie la matrice actuelle par une matrice arbitraire. | fonction glMultMatrixf (GL. h)
ms.assetid: fea5e557-09bd-4c45-89cc-9f3739b577bb
keywords:
- glMultMatrixf fonction OpenGL
topic_type:
- apiref
api_name:
- glMultMatrixf
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f981b78dc2d9f152a4a7d1f40c4a2d1f120944b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104568380"
---
# <a name="glmultmatrixf-function"></a><span data-ttu-id="09267-105">glMultMatrixf fonction)</span><span class="sxs-lookup"><span data-stu-id="09267-105">glMultMatrixf function</span></span>

<span data-ttu-id="09267-106">Les fonctions [**glMultMatrixd**](glmultmatrixd.md) et **glMultMatrixf** multiplient la matrice actuelle par une matrice arbitraire.</span><span class="sxs-lookup"><span data-stu-id="09267-106">The [**glMultMatrixd**](glmultmatrixd.md) and **glMultMatrixf** functions multiply the current matrix by an arbitrary matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="09267-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="09267-107">Syntax</span></span>


```C++
void WINAPI glMultMatrixf(
   const GLfloat *m
);
```



## <a name="parameters"></a><span data-ttu-id="09267-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="09267-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09267-109">*m*</span><span class="sxs-lookup"><span data-stu-id="09267-109">*m*</span></span> 
</dt> <dd>

<span data-ttu-id="09267-110">Pointeur vers une matrice 4x4 stockée dans la colonne dans l’ordre décroissant de 16 valeurs consécutives.</span><span class="sxs-lookup"><span data-stu-id="09267-110">A pointer to a 4x4 matrix stored in column-major order as 16 consecutive values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09267-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="09267-111">Return value</span></span>

<span data-ttu-id="09267-112">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="09267-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="09267-113">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="09267-113">Error codes</span></span>

<span data-ttu-id="09267-114">Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="09267-114">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="09267-115">Nom</span><span class="sxs-lookup"><span data-stu-id="09267-115">Name</span></span>                                                                                                  | <span data-ttu-id="09267-116">Signification</span><span class="sxs-lookup"><span data-stu-id="09267-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="09267-117"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="09267-117"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="09267-118">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="09267-118">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="09267-119">Notes</span><span class="sxs-lookup"><span data-stu-id="09267-119">Remarks</span></span>

<span data-ttu-id="09267-120">La fonction **glMultMatrix** multiplie la matrice actuelle par celle spécifiée dans *m*.</span><span class="sxs-lookup"><span data-stu-id="09267-120">The **glMultMatrix** function multiplies the current matrix by the one specified in *m*.</span></span> <span data-ttu-id="09267-121">Autrement dit, si M est la matrice actuelle et T est la matrice transmise à **glMultMatrix**, m est remplacé par m T.</span><span class="sxs-lookup"><span data-stu-id="09267-121">That is, if M is the current matrix and T is the matrix passed to **glMultMatrix**, then M is replaced with M   T.</span></span>

<span data-ttu-id="09267-122">La matrice actuelle est la matrice de projection, la matrice modelview ou la matrice de texture, déterminée par le mode matrice en cours (voir [**glMatrixMode**](glmatrixmode.md)).</span><span class="sxs-lookup"><span data-stu-id="09267-122">The current matrix is the projection matrix, modelview matrix, or texture matrix, determined by the current matrix mode (see [**glMatrixMode**](glmatrixmode.md)).</span></span>

<span data-ttu-id="09267-123">Le paramètre *m* pointe vers une matrice 4x4 de valeurs à virgule flottante simple précision ou à virgule flottante double précision stockées dans l’ordre des colonnes.</span><span class="sxs-lookup"><span data-stu-id="09267-123">The *m* parameter points to a 4x4 matrix of single-precision or double-precision floating-point values stored in column-major order.</span></span> <span data-ttu-id="09267-124">Autrement dit, la matrice est stockée comme indiqué dans l’image suivante.</span><span class="sxs-lookup"><span data-stu-id="09267-124">That is, the matrix is stored as shown in the following image.</span></span>

![! [Diagramme montrant la matrice 4x4 vers laquelle pointe le paramètre m.]](images/multi01.png)

<span data-ttu-id="09267-126">Les fonctions suivantes récupèrent les informations relatives à **glMultMatrix**:</span><span class="sxs-lookup"><span data-stu-id="09267-126">The following functions retrieve information related to **glMultMatrix**:</span></span>

<span data-ttu-id="09267-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec l’argument \_ mode de matrice GL \_</span><span class="sxs-lookup"><span data-stu-id="09267-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="09267-128">**glGet** avec argument GL \_ MODELVIEW \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="09267-128">**glGet** with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="09267-129">**glGet** avec argument \_ matrice de projection de la comptabilité \_</span><span class="sxs-lookup"><span data-stu-id="09267-129">**glGet** with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="09267-130">matrice de texture **glGet** avec argument GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="09267-130">**glGet** with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="09267-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="09267-131">Requirements</span></span>



| <span data-ttu-id="09267-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="09267-132">Requirement</span></span> | <span data-ttu-id="09267-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="09267-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="09267-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="09267-134">Minimum supported client</span></span><br/> | <span data-ttu-id="09267-135">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="09267-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="09267-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="09267-136">Minimum supported server</span></span><br/> | <span data-ttu-id="09267-137">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="09267-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="09267-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="09267-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="09267-139"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="09267-139"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="09267-140">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="09267-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="09267-141"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="09267-141"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="09267-142">DLL</span><span class="sxs-lookup"><span data-stu-id="09267-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09267-143"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09267-143"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09267-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09267-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09267-145">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="09267-145">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="09267-146">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="09267-146">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="09267-147">**glLoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="09267-147">**glLoadIdentity**</span></span>](glloadidentity.md)
</dt> <dt>

[<span data-ttu-id="09267-148">**glLoadMatrix**</span><span class="sxs-lookup"><span data-stu-id="09267-148">**glLoadMatrix**</span></span>](glloadmatrix.md)
</dt> <dt>

[<span data-ttu-id="09267-149">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="09267-149">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="09267-150">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="09267-150">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> </dl>

 

 





