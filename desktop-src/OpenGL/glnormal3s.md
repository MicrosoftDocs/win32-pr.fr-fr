---
title: fonction glNormal3s (GL. h)
description: Définit le vecteur normal actuel. | fonction glNormal3s (GL. h)
ms.assetid: 4fd98ad5-266d-4ef1-9c1f-2b5166ee65d7
keywords:
- glNormal3s fonction OpenGL
topic_type:
- apiref
api_name:
- glNormal3s
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7941fa4e2c4e5ef00a5a14ce1eb913fb22a1f58
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104211500"
---
# <a name="glnormal3s-function"></a><span data-ttu-id="add76-105">glNormal3s fonction)</span><span class="sxs-lookup"><span data-stu-id="add76-105">glNormal3s function</span></span>

<span data-ttu-id="add76-106">Définit le vecteur normal actuel.</span><span class="sxs-lookup"><span data-stu-id="add76-106">Sets the current normal vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="add76-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="add76-107">Syntax</span></span>


```C++
void WINAPI glNormal3s(
   GLshort nx,
   GLshort ny,
   GLshort nz
);
```



## <a name="parameters"></a><span data-ttu-id="add76-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="add76-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="add76-109">*NX*</span><span class="sxs-lookup"><span data-stu-id="add76-109">*nx*</span></span> 
</dt> <dd>

<span data-ttu-id="add76-110">Spécifie la coordonnée x du nouveau vecteur normal actuel.</span><span class="sxs-lookup"><span data-stu-id="add76-110">Specifies the x-coordinate of the new current normal vector.</span></span>

</dd> <dt>

<span data-ttu-id="add76-111">*NY*</span><span class="sxs-lookup"><span data-stu-id="add76-111">*ny*</span></span> 
</dt> <dd>

<span data-ttu-id="add76-112">Spécifie la coordonnée y du nouveau vecteur normal actuel.</span><span class="sxs-lookup"><span data-stu-id="add76-112">Specifies the y-coordinate of the new current normal vector.</span></span>

</dd> <dt>

<span data-ttu-id="add76-113">*NZ*</span><span class="sxs-lookup"><span data-stu-id="add76-113">*nz*</span></span> 
</dt> <dd>

<span data-ttu-id="add76-114">Spécifie la coordonnée z du nouveau vecteur normal actuel.</span><span class="sxs-lookup"><span data-stu-id="add76-114">Specifies the z-coordinate of the new current normal vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="add76-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="add76-115">Return value</span></span>

<span data-ttu-id="add76-116">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="add76-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="add76-117">Notes</span><span class="sxs-lookup"><span data-stu-id="add76-117">Remarks</span></span>

<span data-ttu-id="add76-118">La normale actuelle est définie sur les coordonnées données chaque fois que vous appelez la fonction **glNormal3s**.</span><span class="sxs-lookup"><span data-stu-id="add76-118">The current normal is set to the given coordinates whenever you call the **glNormal3s** function.</span></span>

<span data-ttu-id="add76-119">Les arguments Byte, short ou Integer sont convertis en format à virgule flottante avec un mappage linéaire qui mappe la valeur entière représentable la plus positive à 1,0, et la valeur entière représentable la plus négative à-1,0.</span><span class="sxs-lookup"><span data-stu-id="add76-119">Byte, short, or integer arguments are converted to floating-point format with a linear mapping that maps the most positive representable integer value to 1.0, and the most negative representable integer value to -1.0.</span></span>

<span data-ttu-id="add76-120">Les normales spécifiées à l’aide de **glNormal3s** n’ont pas besoin d’avoir une longueur d’unité.</span><span class="sxs-lookup"><span data-stu-id="add76-120">Normals specified by using **glNormal3s** need not have unit length.</span></span> <span data-ttu-id="add76-121">Si la normalisation est activée, les normales spécifiées avec **glNormal3s** sont normalisées après la transformation.</span><span class="sxs-lookup"><span data-stu-id="add76-121">If normalization is enabled, then normals specified with **glNormal3s** are normalized after transformation.</span></span> <span data-ttu-id="add76-122">Vous pouvez contrôler normalizationby à l’aide de [**glEnable**](glenable.md) et [**glDisable**](gldisable.md) avec l’argument GL \_ Normalize.</span><span class="sxs-lookup"><span data-stu-id="add76-122">You can control normalizationby using [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with the argument GL\_NORMALIZE.</span></span> <span data-ttu-id="add76-123">Par défaut, la normalisation est désactivée.</span><span class="sxs-lookup"><span data-stu-id="add76-123">By default, normalization is disabled.</span></span> <span data-ttu-id="add76-124">Vous pouvez mettre à jour la normale actuelle à tout moment.</span><span class="sxs-lookup"><span data-stu-id="add76-124">You can update the current normal at any time.</span></span> <span data-ttu-id="add76-125">En particulier, vous pouvez appeler **glNormal3s** entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="add76-125">In particular, you can call **glNormal3s** between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="add76-126">Les fonctions suivantes récupèrent les informations relatives à **glNormal3s**:</span><span class="sxs-lookup"><span data-stu-id="add76-126">The following functions retrieve information related to **glNormal3s**:</span></span>

<span data-ttu-id="add76-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ actuel \_ normal</span><span class="sxs-lookup"><span data-stu-id="add76-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_NORMAL</span></span>

<span data-ttu-id="add76-128">[**glIsEnable**](glisenabled.md) avec argument GL \_ Normalize</span><span class="sxs-lookup"><span data-stu-id="add76-128">[**glIsEnable**](glisenabled.md) with argument GL\_NORMALIZE</span></span>

## <a name="requirements"></a><span data-ttu-id="add76-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="add76-129">Requirements</span></span>



| <span data-ttu-id="add76-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="add76-130">Requirement</span></span> | <span data-ttu-id="add76-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="add76-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="add76-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="add76-132">Minimum supported client</span></span><br/> | <span data-ttu-id="add76-133">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="add76-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="add76-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="add76-134">Minimum supported server</span></span><br/> | <span data-ttu-id="add76-135">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="add76-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="add76-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="add76-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="add76-137"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="add76-137"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="add76-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="add76-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="add76-139"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="add76-139"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="add76-140">DLL</span><span class="sxs-lookup"><span data-stu-id="add76-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="add76-141"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="add76-141"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="add76-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="add76-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="add76-143">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="add76-143">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="add76-144">**glColor**</span><span class="sxs-lookup"><span data-stu-id="add76-144">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="add76-145">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="add76-145">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="add76-146">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="add76-146">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="add76-147">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="add76-147">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="add76-148">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="add76-148">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





