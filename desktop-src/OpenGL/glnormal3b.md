---
title: fonction glNormal3b (GL. h)
description: Définit le vecteur normal actuel. | fonction glNormal3b (GL. h)
ms.assetid: b6976143-bc9a-4766-9f7e-5380c3a24173
keywords:
- glNormal3b fonction OpenGL
topic_type:
- apiref
api_name:
- glNormal3b
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a09a92b718881670ed5625fd5aa94a23193cdd6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103869709"
---
# <a name="glnormal3b-function"></a><span data-ttu-id="4ede1-105">glNormal3b fonction)</span><span class="sxs-lookup"><span data-stu-id="4ede1-105">glNormal3b function</span></span>

<span data-ttu-id="4ede1-106">Définit le vecteur normal actuel.</span><span class="sxs-lookup"><span data-stu-id="4ede1-106">Sets the current normal vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ede1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4ede1-107">Syntax</span></span>


```C++
void WINAPI glNormal3b(
   GLbyte nx,
   GLbyte ny,
   GLbyte nz
);
```



## <a name="parameters"></a><span data-ttu-id="4ede1-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4ede1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ede1-109">*NX*</span><span class="sxs-lookup"><span data-stu-id="4ede1-109">*nx*</span></span> 
</dt> <dd>

<span data-ttu-id="4ede1-110">Spécifie la coordonnée x du nouveau vecteur normal actuel.</span><span class="sxs-lookup"><span data-stu-id="4ede1-110">Specifies the x-coordinate for the new current normal vector.</span></span>

</dd> <dt>

<span data-ttu-id="4ede1-111">*NY*</span><span class="sxs-lookup"><span data-stu-id="4ede1-111">*ny*</span></span> 
</dt> <dd>

<span data-ttu-id="4ede1-112">Spécifie la coordonnée y du nouveau vecteur normal actuel.</span><span class="sxs-lookup"><span data-stu-id="4ede1-112">Specifies the y-coordinate for the new current normal vector.</span></span>

</dd> <dt>

<span data-ttu-id="4ede1-113">*NZ*</span><span class="sxs-lookup"><span data-stu-id="4ede1-113">*nz*</span></span> 
</dt> <dd>

<span data-ttu-id="4ede1-114">Spécifie la coordonnée z du nouveau vecteur normal actuel.</span><span class="sxs-lookup"><span data-stu-id="4ede1-114">Specifies the z-coordinate for the new current normal vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ede1-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4ede1-115">Return value</span></span>

<span data-ttu-id="4ede1-116">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="4ede1-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ede1-117">Notes</span><span class="sxs-lookup"><span data-stu-id="4ede1-117">Remarks</span></span>

<span data-ttu-id="4ede1-118">La normale actuelle est définie sur les coordonnées données chaque fois que vous appelez la fonction **glNormal3b** .</span><span class="sxs-lookup"><span data-stu-id="4ede1-118">The current normal is set to the given coordinates whenever you call the **glNormal3b** function.</span></span>

<span data-ttu-id="4ede1-119">Les arguments Byte, short ou Integer sont convertis en format à virgule flottante à l’aide d’un mappage linéaire qui mappe la valeur entière représentable la plus positive à 1,0, et la valeur entière la plus négative à-1,0.</span><span class="sxs-lookup"><span data-stu-id="4ede1-119">Byte, short, or integer arguments are converted to floating-point format by using a linear mapping that maps the most positive representable integer value to 1.0, and the most negative representable integer value to -1.0.</span></span>

<span data-ttu-id="4ede1-120">Les normales spécifiées avec **glNormal3b** n’ont pas besoin d’avoir une longueur d’unité.</span><span class="sxs-lookup"><span data-stu-id="4ede1-120">Normals specified with **glNormal3b** need not have unit length.</span></span> <span data-ttu-id="4ede1-121">Si la normalisation est activée, les normales spécifiées avec **glNormal3b** sont normalisées après la transformation.</span><span class="sxs-lookup"><span data-stu-id="4ede1-121">If normalization is enabled, then normals specified with **glNormal3b** are normalized after transformation.</span></span> <span data-ttu-id="4ede1-122">Vous pouvez contrôler la normalisation à l’aide de [**glEnable**](glenable.md) et [**glDisable**](gldisable.md) avec l’argument GL \_ Normalize.</span><span class="sxs-lookup"><span data-stu-id="4ede1-122">You can control normalization by using [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with the argument GL\_NORMALIZE.</span></span> <span data-ttu-id="4ede1-123">Par défaut, la normalisation est désactivée.</span><span class="sxs-lookup"><span data-stu-id="4ede1-123">By default, normalization is disabled.</span></span> <span data-ttu-id="4ede1-124">Vous pouvez mettre à jour la normale actuelle à tout moment.</span><span class="sxs-lookup"><span data-stu-id="4ede1-124">You can update the current normal at any time.</span></span> <span data-ttu-id="4ede1-125">En particulier, vous pouvez appeler **glNormal3b** entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="4ede1-125">In particular, you can call **glNormal3b** between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="4ede1-126">Les fonctions suivantes récupèrent les informations relatives à **glNormal3b**:</span><span class="sxs-lookup"><span data-stu-id="4ede1-126">The following functions retrieve information related to **glNormal3b**:</span></span>

<span data-ttu-id="4ede1-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ actuel \_ normal</span><span class="sxs-lookup"><span data-stu-id="4ede1-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_NORMAL</span></span>

<span data-ttu-id="4ede1-128">[**glIsEnable**](glisenabled.md) avec argument GL \_ Normalize</span><span class="sxs-lookup"><span data-stu-id="4ede1-128">[**glIsEnable**](glisenabled.md) with argument GL\_NORMALIZE</span></span>

## <a name="requirements"></a><span data-ttu-id="4ede1-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4ede1-129">Requirements</span></span>



| <span data-ttu-id="4ede1-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4ede1-130">Requirement</span></span> | <span data-ttu-id="4ede1-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="4ede1-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ede1-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4ede1-132">Minimum supported client</span></span><br/> | <span data-ttu-id="4ede1-133">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4ede1-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="4ede1-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4ede1-134">Minimum supported server</span></span><br/> | <span data-ttu-id="4ede1-135">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4ede1-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4ede1-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="4ede1-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ede1-137"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ede1-137"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="4ede1-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4ede1-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="4ede1-139"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4ede1-139"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="4ede1-140">DLL</span><span class="sxs-lookup"><span data-stu-id="4ede1-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ede1-141"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ede1-141"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ede1-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4ede1-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ede1-143">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="4ede1-143">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="4ede1-144">**glColor**</span><span class="sxs-lookup"><span data-stu-id="4ede1-144">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="4ede1-145">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="4ede1-145">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="4ede1-146">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="4ede1-146">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="4ede1-147">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="4ede1-147">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="4ede1-148">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="4ede1-148">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





