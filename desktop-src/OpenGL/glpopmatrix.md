---
title: fonction glPopMatrix (GL. h)
description: Les fonctions glPushMatrix et glPopMatrix poussent et dépilent la pile de matrice actuelle. | fonction glPopMatrix (GL. h)
ms.assetid: 7b4fc26e-36c8-4252-aba7-2e8ec6b34f91
keywords:
- glPopMatrix fonction OpenGL
topic_type:
- apiref
api_name:
- glPopMatrix
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41424a8af3ca6599edc7a66f9e498632640022c5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106520268"
---
# <a name="glpopmatrix-function"></a><span data-ttu-id="fd800-105">glPopMatrix fonction)</span><span class="sxs-lookup"><span data-stu-id="fd800-105">glPopMatrix function</span></span>

<span data-ttu-id="fd800-106">Les fonctions [**glPushMatrix**](glpushmatrix.md) et **glPopMatrix** poussent et dépilent la pile de matrice actuelle.</span><span class="sxs-lookup"><span data-stu-id="fd800-106">The [**glPushMatrix**](glpushmatrix.md) and **glPopMatrix** functions push and pop the current matrix stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd800-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fd800-107">Syntax</span></span>


```C++
void WINAPI glPopMatrix(void);
```



## <a name="parameters"></a><span data-ttu-id="fd800-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fd800-108">Parameters</span></span>

<span data-ttu-id="fd800-109">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="fd800-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fd800-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fd800-110">Return value</span></span>

<span data-ttu-id="fd800-111">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="fd800-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fd800-112">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="fd800-112">Error codes</span></span>

<span data-ttu-id="fd800-113">La transmission d’une pile de matrices complète ou la dépilement d’une pile de matrice contenant une seule matrice ne constitue pas une erreur.</span><span class="sxs-lookup"><span data-stu-id="fd800-113">It is an error to push a full matrix stack, or to pop a matrix stack that contains only a single matrix.</span></span> <span data-ttu-id="fd800-114">Dans les deux cas, l’indicateur d’erreur est défini et aucune autre modification n’est apportée à l’État OpenGL.</span><span class="sxs-lookup"><span data-stu-id="fd800-114">In either case, the error flag is set and no other change is made to the OpenGL state.</span></span>

<span data-ttu-id="fd800-115">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="fd800-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="fd800-116">Nom</span><span class="sxs-lookup"><span data-stu-id="fd800-116">Name</span></span>                                                                                                  | <span data-ttu-id="fd800-117">Signification</span><span class="sxs-lookup"><span data-stu-id="fd800-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fd800-118"><dt>**DÉPASSEMENT de capacité de la \_ pile GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fd800-118"><dt>**GL\_STACK\_UNDERFLOW**</dt></span></span> </dl>   | <span data-ttu-id="fd800-119">La fonction a été appelée alors que la pile de matrice actuelle ne contenait qu’une seule matrice.</span><span class="sxs-lookup"><span data-stu-id="fd800-119">The function was called while the current matrix stack contained only a single matrix.</span></span><br/>                                     |
| <dl> <span data-ttu-id="fd800-120"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fd800-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="fd800-121">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="fd800-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="fd800-122">Notes</span><span class="sxs-lookup"><span data-stu-id="fd800-122">Remarks</span></span>

<span data-ttu-id="fd800-123">Il existe une pile de matrices pour chaque mode de matrice.</span><span class="sxs-lookup"><span data-stu-id="fd800-123">There is a stack of matrices for each of the matrix modes.</span></span> <span data-ttu-id="fd800-124">En \_ mode MODELVIEW GL, la profondeur de la pile est au moins égale à 32.</span><span class="sxs-lookup"><span data-stu-id="fd800-124">In GL\_MODELVIEW mode, the stack depth is at least 32.</span></span> <span data-ttu-id="fd800-125">Dans les deux autres modes, \_ la projection GL et \_ la texture GL, la profondeur est au moins égale à 2.</span><span class="sxs-lookup"><span data-stu-id="fd800-125">In the other two modes, GL\_PROJECTION and GL\_TEXTURE, the depth is at least 2.</span></span> <span data-ttu-id="fd800-126">La matrice actuelle dans n’importe quel mode est la matrice située en haut de la pile pour ce mode.</span><span class="sxs-lookup"><span data-stu-id="fd800-126">The current matrix in any mode is the matrix on the top of the stack for that mode.</span></span>

<span data-ttu-id="fd800-127">La fonction [**glPushMatrix**](glpushmatrix.md) pousse la pile de la matrice active d’une unité, en dupliquant la matrice actuelle.</span><span class="sxs-lookup"><span data-stu-id="fd800-127">The [**glPushMatrix**](glpushmatrix.md) function pushes the current matrix stack down by one, duplicating the current matrix.</span></span> <span data-ttu-id="fd800-128">Autrement dit, après un appel **glPushMatrix** , la matrice située en haut de la pile est identique à celle qui se trouve au-dessous.</span><span class="sxs-lookup"><span data-stu-id="fd800-128">That is, after a **glPushMatrix** call, the matrix on the top of the stack is identical to the one below it.</span></span> <span data-ttu-id="fd800-129">La fonction **glPopMatrix** dépile la pile de matrice actuelle, en remplaçant la matrice actuelle par celle qui est située au-dessous de celle-ci sur la pile.</span><span class="sxs-lookup"><span data-stu-id="fd800-129">The **glPopMatrix** function pops the current matrix stack, replacing the current matrix with the one below it on the stack.</span></span> <span data-ttu-id="fd800-130">Initialement, chacune des piles contient une matrice, une matrice d’identité.</span><span class="sxs-lookup"><span data-stu-id="fd800-130">Initially, each of the stacks contains one matrix, an identity matrix.</span></span>

<span data-ttu-id="fd800-131">Les fonctions suivantes récupèrent les informations relatives à [**glPushMatrix**](glpushmatrix.md) et **glPopMatrix**:</span><span class="sxs-lookup"><span data-stu-id="fd800-131">The following functions retrieve information related to [**glPushMatrix**](glpushmatrix.md) and **glPopMatrix**:</span></span>

<span data-ttu-id="fd800-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec l’argument \_ mode de matrice GL \_</span><span class="sxs-lookup"><span data-stu-id="fd800-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="fd800-133">**glGet** avec argument GL \_ MODELVIEW \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="fd800-133">**glGet** with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="fd800-134">**glGet** avec argument \_ matrice de projection de la comptabilité \_</span><span class="sxs-lookup"><span data-stu-id="fd800-134">**glGet** with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="fd800-135">matrice de texture **glGet** avec argument GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="fd800-135">**glGet** with argument GL\_TEXTURE\_MATRIX</span></span>

<span data-ttu-id="fd800-136">**glGet** avec argument GL MODELVIEW de la profondeur de la \_ \_ pile \_</span><span class="sxs-lookup"><span data-stu-id="fd800-136">**glGet** with argument GL\_MODELVIEW\_STACK\_DEPTH</span></span>

<span data-ttu-id="fd800-137">**glGet** avec la profondeur de la pile de projection de l’argument GL \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="fd800-137">**glGet** with argument GL\_PROJECTION\_STACK\_DEPTH</span></span>

<span data-ttu-id="fd800-138">**glGet** avec la profondeur de la pile de texture de l’argument GL \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="fd800-138">**glGet** with argument GL\_TEXTURE\_STACK\_DEPTH</span></span>

<span data-ttu-id="fd800-139">**glGet** avec argument GL \_ Max \_ MODELVIEW \_ \_ profondeur de la pile</span><span class="sxs-lookup"><span data-stu-id="fd800-139">**glGet** with argument GL\_MAX\_MODELVIEW\_STACK\_DEPTH</span></span>

<span data-ttu-id="fd800-140">**glGet** avec l’argument de profondeur de la \_ pile de projection Max GL \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="fd800-140">**glGet** with argument GL\_MAX\_PROJECTION\_STACK\_DEPTH</span></span>

<span data-ttu-id="fd800-141">**glGet** avec argument de la profondeur de la \_ \_ pile texture Max \_ . GL \_</span><span class="sxs-lookup"><span data-stu-id="fd800-141">**glGet** with argument GL\_MAX\_TEXTURE\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="fd800-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fd800-142">Requirements</span></span>



| <span data-ttu-id="fd800-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fd800-143">Requirement</span></span> | <span data-ttu-id="fd800-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd800-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd800-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd800-145">Minimum supported client</span></span><br/> | <span data-ttu-id="fd800-146">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fd800-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="fd800-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd800-147">Minimum supported server</span></span><br/> | <span data-ttu-id="fd800-148">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fd800-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fd800-149">En-tête</span><span class="sxs-lookup"><span data-stu-id="fd800-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd800-150"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd800-150"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="fd800-151">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fd800-151">Library</span></span><br/>                  | <dl> <span data-ttu-id="fd800-152"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fd800-152"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="fd800-153">DLL</span><span class="sxs-lookup"><span data-stu-id="fd800-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd800-154"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd800-154"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd800-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd800-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd800-156">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="fd800-156">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="fd800-157">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="fd800-157">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="fd800-158">**glFrustum**</span><span class="sxs-lookup"><span data-stu-id="fd800-158">**glFrustum**</span></span>](glfrustum.md)
</dt> <dt>

[<span data-ttu-id="fd800-159">**glLoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="fd800-159">**glLoadIdentity**</span></span>](glloadidentity.md)
</dt> <dt>

[<span data-ttu-id="fd800-160">**glLoadMatrix**</span><span class="sxs-lookup"><span data-stu-id="fd800-160">**glLoadMatrix**</span></span>](glloadmatrix.md)
</dt> <dt>

[<span data-ttu-id="fd800-161">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="fd800-161">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="fd800-162">**glMultMatrix**</span><span class="sxs-lookup"><span data-stu-id="fd800-162">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="fd800-163">**glOrtho**</span><span class="sxs-lookup"><span data-stu-id="fd800-163">**glOrtho**</span></span>](glortho.md)
</dt> <dt>

[<span data-ttu-id="fd800-164">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="fd800-164">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> <dt>

[<span data-ttu-id="fd800-165">**glRotate**</span><span class="sxs-lookup"><span data-stu-id="fd800-165">**glRotate**</span></span>](glrotate.md)
</dt> <dt>

[<span data-ttu-id="fd800-166">**glScale**</span><span class="sxs-lookup"><span data-stu-id="fd800-166">**glScale**</span></span>](glscale.md)
</dt> <dt>

[<span data-ttu-id="fd800-167">**glTranslate**</span><span class="sxs-lookup"><span data-stu-id="fd800-167">**glTranslate**</span></span>](gltranslate.md)
</dt> <dt>

[<span data-ttu-id="fd800-168">**glViewport**</span><span class="sxs-lookup"><span data-stu-id="fd800-168">**glViewport**</span></span>](glviewport.md)
</dt> </dl>

 

 





