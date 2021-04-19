---
title: fonction glNormal3f (GL. h)
description: Définit le vecteur normal actuel. | fonction glNormal3f (GL. h)
ms.assetid: 8407996e-47fd-4c30-91f6-53d4341a1fca
keywords:
- glNormal3f fonction OpenGL
topic_type:
- apiref
api_name:
- glNormal3f
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72e83b874b1588ad8bd91da9e5c9f831062de9cc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106524819"
---
# <a name="glnormal3f-function"></a><span data-ttu-id="f846e-105">glNormal3f fonction)</span><span class="sxs-lookup"><span data-stu-id="f846e-105">glNormal3f function</span></span>

<span data-ttu-id="f846e-106">Définit le vecteur normal actuel.</span><span class="sxs-lookup"><span data-stu-id="f846e-106">Sets the current normal vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="f846e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f846e-107">Syntax</span></span>


```C++
void WINAPI glNormal3f(
   GLfloat nx,
   GLfloat ny,
   GLfloat nz
);
```



## <a name="parameters"></a><span data-ttu-id="f846e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f846e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f846e-109">*NX*</span><span class="sxs-lookup"><span data-stu-id="f846e-109">*nx*</span></span> 
</dt> <dd>

<span data-ttu-id="f846e-110">Spécifie la coordonnée x du nouveau vecteur normal actuel.</span><span class="sxs-lookup"><span data-stu-id="f846e-110">Specifies the x-coordinate for the new current normal vector.</span></span>

</dd> <dt>

<span data-ttu-id="f846e-111">*NY*</span><span class="sxs-lookup"><span data-stu-id="f846e-111">*ny*</span></span> 
</dt> <dd>

<span data-ttu-id="f846e-112">Spécifie la coordonnée y du nouveau vecteur normal actuel.</span><span class="sxs-lookup"><span data-stu-id="f846e-112">Specifies the y-coordinate for the new current normal vector.</span></span>

</dd> <dt>

<span data-ttu-id="f846e-113">*NZ*</span><span class="sxs-lookup"><span data-stu-id="f846e-113">*nz*</span></span> 
</dt> <dd>

<span data-ttu-id="f846e-114">Spécifie la coordonnée z du nouveau vecteur normal actuel.</span><span class="sxs-lookup"><span data-stu-id="f846e-114">Specifies the z-coordinate for the new current normal vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f846e-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f846e-115">Return value</span></span>

<span data-ttu-id="f846e-116">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="f846e-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f846e-117">Notes</span><span class="sxs-lookup"><span data-stu-id="f846e-117">Remarks</span></span>

<span data-ttu-id="f846e-118">La normale actuelle est définie sur les coordonnées données chaque fois que vous appelez la fonction **glNormal3f** .</span><span class="sxs-lookup"><span data-stu-id="f846e-118">The current normal is set to the given coordinates whenever you call the **glNormal3f** function.</span></span>

<span data-ttu-id="f846e-119">Les arguments Byte, short ou Integer sont convertis en format à virgule flottante avec un mappage linéaire qui mappe la valeur entière représentable la plus positive à 1,0, et la valeur entière représentable la plus négative à-1,0.</span><span class="sxs-lookup"><span data-stu-id="f846e-119">Byte, short, or integer arguments are converted to floating-point format with a linear mapping that maps the most positive representable integer value to 1.0, and the most negative representable integer value to -1.0.</span></span>

<span data-ttu-id="f846e-120">Les normales spécifiées à l’aide de **glNormal3f** n’ont pas besoin d’avoir une longueur d’unité.</span><span class="sxs-lookup"><span data-stu-id="f846e-120">Normals specified by using **glNormal3f** need not have unit length.</span></span> <span data-ttu-id="f846e-121">Si la normalisation est activée, les normales spécifiées avec **glNormal3f** sont normalisées après la transformation.</span><span class="sxs-lookup"><span data-stu-id="f846e-121">If normalization is enabled, then normals specified with **glNormal3f** are normalized after transformation.</span></span> <span data-ttu-id="f846e-122">Vous pouvez contrôler la normalisation à l’aide de [**glEnable**](glenable.md) et [**glDisable**](gldisable.md) avec l’argument GL \_ Normalize.</span><span class="sxs-lookup"><span data-stu-id="f846e-122">You can control normalization by using [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with the argument GL\_NORMALIZE.</span></span> <span data-ttu-id="f846e-123">Par défaut, la normalisation est désactivée.</span><span class="sxs-lookup"><span data-stu-id="f846e-123">By default, normalization is disabled.</span></span> <span data-ttu-id="f846e-124">Vous pouvez mettre à jour la normale actuelle à tout moment.</span><span class="sxs-lookup"><span data-stu-id="f846e-124">You can update the current normal at any time.</span></span> <span data-ttu-id="f846e-125">En particulier, vous pouvez appeler **glNormal3f** entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="f846e-125">In particular, you can call **glNormal3f** between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="f846e-126">Les fonctions suivantes récupèrent les informations relatives à **glNormal3f**:</span><span class="sxs-lookup"><span data-stu-id="f846e-126">The following functions retrieve information related to **glNormal3f**:</span></span>

<span data-ttu-id="f846e-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ actuel \_ normal</span><span class="sxs-lookup"><span data-stu-id="f846e-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_NORMAL</span></span>

<span data-ttu-id="f846e-128">[**glIsEnable**](glisenabled.md) avec argument GL \_ Normalize</span><span class="sxs-lookup"><span data-stu-id="f846e-128">[**glIsEnable**](glisenabled.md) with argument GL\_NORMALIZE</span></span>

## <a name="requirements"></a><span data-ttu-id="f846e-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f846e-129">Requirements</span></span>



| <span data-ttu-id="f846e-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f846e-130">Requirement</span></span> | <span data-ttu-id="f846e-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="f846e-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f846e-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f846e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f846e-133">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f846e-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f846e-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f846e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f846e-135">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f846e-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f846e-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="f846e-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="f846e-137"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="f846e-137"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="f846e-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f846e-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="f846e-139"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f846e-139"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f846e-140">DLL</span><span class="sxs-lookup"><span data-stu-id="f846e-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f846e-141"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f846e-141"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f846e-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f846e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f846e-143">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="f846e-143">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="f846e-144">**glColor**</span><span class="sxs-lookup"><span data-stu-id="f846e-144">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="f846e-145">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="f846e-145">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="f846e-146">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="f846e-146">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="f846e-147">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="f846e-147">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="f846e-148">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="f846e-148">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





