---
title: fonction glRotated (GL. h)
description: La fonction glRotated multiplie la matrice actuelle par une matrice de rotation.
ms.assetid: 9adfeb5b-8c2a-4acf-a251-6ba23cc4c3a6
keywords:
- glRotated fonction OpenGL
topic_type:
- apiref
api_name:
- glRotated
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d0678e9da6f0b68047708f45fda1c9da66d8139
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509410"
---
# <a name="glrotated-function"></a><span data-ttu-id="1ff41-104">glRotated fonction)</span><span class="sxs-lookup"><span data-stu-id="1ff41-104">glRotated function</span></span>

<span data-ttu-id="1ff41-105">La fonction **glRotated** multiplie la matrice actuelle par une matrice de rotation.</span><span class="sxs-lookup"><span data-stu-id="1ff41-105">The **glRotated** function multiplies the current matrix by a rotation matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ff41-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1ff41-106">Syntax</span></span>


```C++
void WINAPI glRotated(
   GLdouble angle,
   GLdouble x,
   GLdouble y,
   GLdouble z
);
```



## <a name="parameters"></a><span data-ttu-id="1ff41-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1ff41-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ff41-108">*angle*</span><span class="sxs-lookup"><span data-stu-id="1ff41-108">*angle*</span></span> 
</dt> <dd>

<span data-ttu-id="1ff41-109">Angle de rotation, en degrés.</span><span class="sxs-lookup"><span data-stu-id="1ff41-109">The angle of rotation, in degrees.</span></span>

</dd> <dt>

<span data-ttu-id="1ff41-110">*x*</span><span class="sxs-lookup"><span data-stu-id="1ff41-110">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="1ff41-111">Coordonnée *x* d’un vecteur.</span><span class="sxs-lookup"><span data-stu-id="1ff41-111">The *x* coordinate of a vector.</span></span>

</dd> <dt>

<span data-ttu-id="1ff41-112">*y*</span><span class="sxs-lookup"><span data-stu-id="1ff41-112">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="1ff41-113">Coordonnée *y* d’un vecteur.</span><span class="sxs-lookup"><span data-stu-id="1ff41-113">The *y* coordinate of a vector.</span></span>

</dd> <dt>

<span data-ttu-id="1ff41-114">*z*</span><span class="sxs-lookup"><span data-stu-id="1ff41-114">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="1ff41-115">Coordonnée *z* d’un vecteur.</span><span class="sxs-lookup"><span data-stu-id="1ff41-115">The *z* coordinate of a vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ff41-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1ff41-116">Return value</span></span>

<span data-ttu-id="1ff41-117">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="1ff41-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1ff41-118">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="1ff41-118">Error codes</span></span>

<span data-ttu-id="1ff41-119">Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="1ff41-119">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="1ff41-120">Nom</span><span class="sxs-lookup"><span data-stu-id="1ff41-120">Name</span></span>                                                                                                  | <span data-ttu-id="1ff41-121">Signification</span><span class="sxs-lookup"><span data-stu-id="1ff41-121">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1ff41-122"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1ff41-122"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="1ff41-123">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="1ff41-123">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="1ff41-124">Notes</span><span class="sxs-lookup"><span data-stu-id="1ff41-124">Remarks</span></span>

<span data-ttu-id="1ff41-125">La fonction **glRotated** calcule une matrice qui effectue une rotation dans le sens inverse des degrés d' *angle* sur le vecteur à partir de l’origine jusqu’au point (*x*, *y*, *z*).</span><span class="sxs-lookup"><span data-stu-id="1ff41-125">The **glRotated** function computes a matrix that performs a counterclockwise rotation of *angle* degrees about the vector from the origin through the point (*x*, *y*, *z*).</span></span>

<span data-ttu-id="1ff41-126">La matrice actuelle (voir [**glMatrixMode**](glmatrixmode.md)) est multipliée par cette matrice de rotation, le produit remplaçant la matrice actuelle.</span><span class="sxs-lookup"><span data-stu-id="1ff41-126">The current matrix (see [**glMatrixMode**](glmatrixmode.md)) is multiplied by this rotation matrix, with the product replacing the current matrix.</span></span> <span data-ttu-id="1ff41-127">Autrement dit, si M est la matrice actuelle et que R est la matrice de translation, M est remplacé par M R.</span><span class="sxs-lookup"><span data-stu-id="1ff41-127">That is, if M is the current matrix and R is the translation matrix, then M is replaced with M   R.</span></span>

<span data-ttu-id="1ff41-128">Si le mode matriciel est GL \_ MODELVIEW ou GL \_ projection, tous les objets dessinés après l’appel de **glRotated** sont pivotés.</span><span class="sxs-lookup"><span data-stu-id="1ff41-128">If the matrix mode is either GL\_MODELVIEW or GL\_PROJECTION, all objects drawn after **glRotated** is called are rotated.</span></span> <span data-ttu-id="1ff41-129">Utilisez [**glPushMatrix**](glpushmatrix.md) et [**glPopMatrix**](glpopmatrix.md) pour enregistrer et restaurer le système de coordonnées non pivoté.</span><span class="sxs-lookup"><span data-stu-id="1ff41-129">Use [**glPushMatrix**](glpushmatrix.md) and [**glPopMatrix**](glpopmatrix.md) to save and restore the unrotated coordinate system.</span></span>

<span data-ttu-id="1ff41-130">Les fonctions suivantes récupèrent les informations relatives à **glRotated**:</span><span class="sxs-lookup"><span data-stu-id="1ff41-130">The following functions retrieve information related to **glRotated**:</span></span>

<span data-ttu-id="1ff41-131">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Render \_ mode</span><span class="sxs-lookup"><span data-stu-id="1ff41-131">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_RENDER\_MODE</span></span>

<span data-ttu-id="1ff41-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec l’argument \_ mode de matrice GL \_</span><span class="sxs-lookup"><span data-stu-id="1ff41-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="1ff41-133">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ MODELVIEW \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="1ff41-133">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="1ff41-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument \_ matrice de projection de la comptabilité \_</span><span class="sxs-lookup"><span data-stu-id="1ff41-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="1ff41-135">matrice de texture [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="1ff41-135">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="1ff41-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1ff41-136">Requirements</span></span>



| <span data-ttu-id="1ff41-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1ff41-137">Requirement</span></span> | <span data-ttu-id="1ff41-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="1ff41-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ff41-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1ff41-139">Minimum supported client</span></span><br/> | <span data-ttu-id="1ff41-140">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1ff41-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1ff41-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1ff41-141">Minimum supported server</span></span><br/> | <span data-ttu-id="1ff41-142">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1ff41-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1ff41-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="1ff41-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ff41-144"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ff41-144"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="1ff41-145">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1ff41-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="1ff41-146"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1ff41-146"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="1ff41-147">DLL</span><span class="sxs-lookup"><span data-stu-id="1ff41-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ff41-148"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ff41-148"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ff41-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ff41-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ff41-150">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="1ff41-150">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="1ff41-151">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="1ff41-151">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="1ff41-152">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="1ff41-152">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="1ff41-153">**glMultMatrix**</span><span class="sxs-lookup"><span data-stu-id="1ff41-153">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="1ff41-154">**glPopMatrix**</span><span class="sxs-lookup"><span data-stu-id="1ff41-154">**glPopMatrix**</span></span>](glpopmatrix.md)
</dt> <dt>

[<span data-ttu-id="1ff41-155">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="1ff41-155">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> <dt>

[<span data-ttu-id="1ff41-156">**glScale**</span><span class="sxs-lookup"><span data-stu-id="1ff41-156">**glScale**</span></span>](glscale.md)
</dt> <dt>

[<span data-ttu-id="1ff41-157">**glTranslate**</span><span class="sxs-lookup"><span data-stu-id="1ff41-157">**glTranslate**</span></span>](gltranslate.md)
</dt> </dl>

 

 





