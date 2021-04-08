---
title: fonction glNormal3d (GL. h)
description: Définit le vecteur normal actuel. | fonction glNormal3d (GL. h)
ms.assetid: d256aef0-3ad5-4e70-b1c8-6402434b1e67
keywords:
- glNormal3d fonction OpenGL
topic_type:
- apiref
api_name:
- glNormal3d
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c6ab158e298ff20cce635ab4002f38ca82fdaa2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104043061"
---
# <a name="glnormal3d-function"></a><span data-ttu-id="6ae8f-105">glNormal3d fonction)</span><span class="sxs-lookup"><span data-stu-id="6ae8f-105">glNormal3d function</span></span>

<span data-ttu-id="6ae8f-106">Définit le vecteur normal actuel.</span><span class="sxs-lookup"><span data-stu-id="6ae8f-106">Sets the current normal vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ae8f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6ae8f-107">Syntax</span></span>


```C++
void WINAPI glNormal3d(
   GLdouble nx,
   GLdouble ny,
   GLdouble nz
);
```



## <a name="parameters"></a><span data-ttu-id="6ae8f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6ae8f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ae8f-109">*NX*</span><span class="sxs-lookup"><span data-stu-id="6ae8f-109">*nx*</span></span> 
</dt> <dd>

<span data-ttu-id="6ae8f-110">Spécifie la coordonnée x du nouveau vecteur normal actuel.</span><span class="sxs-lookup"><span data-stu-id="6ae8f-110">Specifies the x-coordinate for the new current normal vector.</span></span>

</dd> <dt>

<span data-ttu-id="6ae8f-111">*NY*</span><span class="sxs-lookup"><span data-stu-id="6ae8f-111">*ny*</span></span> 
</dt> <dd>

<span data-ttu-id="6ae8f-112">Spécifie la coordonnée y du nouveau vecteur normal actuel.</span><span class="sxs-lookup"><span data-stu-id="6ae8f-112">Specifies the y-coordinate for the new current normal vector.</span></span>

</dd> <dt>

<span data-ttu-id="6ae8f-113">*NZ*</span><span class="sxs-lookup"><span data-stu-id="6ae8f-113">*nz*</span></span> 
</dt> <dd>

<span data-ttu-id="6ae8f-114">Spécifie la coordonnée z du nouveau vecteur normal actuel.</span><span class="sxs-lookup"><span data-stu-id="6ae8f-114">Specifies the z-coordinate for the new current normal vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ae8f-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6ae8f-115">Return value</span></span>

<span data-ttu-id="6ae8f-116">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="6ae8f-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ae8f-117">Notes</span><span class="sxs-lookup"><span data-stu-id="6ae8f-117">Remarks</span></span>

<span data-ttu-id="6ae8f-118">La normale actuelle est définie sur les coordonnées données chaque fois que vous appelez la fonction **glNormal3d**.</span><span class="sxs-lookup"><span data-stu-id="6ae8f-118">The current normal is set to the given coordinates whenever you call the **glNormal3d** function.</span></span>

<span data-ttu-id="6ae8f-119">Les arguments Byte, short ou Integer sont convertis en format à virgule flottante à l’aide d’un mappage linéaire qui mappe la valeur entière représentable la plus positive à 1,0, et la valeur entière la plus négative à-1,0.</span><span class="sxs-lookup"><span data-stu-id="6ae8f-119">Byte, short, or integer arguments are converted to floating-point format by using a linear mapping that maps the most positive representable integer value to 1.0, and the most negative representable integer value to -1.0.</span></span>

<span data-ttu-id="6ae8f-120">Les normales spécifiées à l’aide de **glNormal3d** n’ont pas besoin d’avoir une longueur d’unité.</span><span class="sxs-lookup"><span data-stu-id="6ae8f-120">Normals specified by using **glNormal3d** need not have unit length.</span></span> <span data-ttu-id="6ae8f-121">Si la normalisation est activée, les normales spécifiées avec **glNormal3d** sont normalisées après la transformation.</span><span class="sxs-lookup"><span data-stu-id="6ae8f-121">If normalization is enabled, then normals specified with **glNormal3d** are normalized after transformation.</span></span> <span data-ttu-id="6ae8f-122">Vous pouvez contrôler la normalisation à l’aide de [**glEnable**](glenable.md) et [**glDisable**](gldisable.md) avec l’argument GL \_ Normalize.</span><span class="sxs-lookup"><span data-stu-id="6ae8f-122">You can control normalization by using [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with the argument GL\_NORMALIZE.</span></span> <span data-ttu-id="6ae8f-123">Par défaut, la normalisation est désactivée.</span><span class="sxs-lookup"><span data-stu-id="6ae8f-123">By default, normalization is disabled.</span></span> <span data-ttu-id="6ae8f-124">Vous pouvez mettre à jour la normale actuelle à tout moment.</span><span class="sxs-lookup"><span data-stu-id="6ae8f-124">You can update the current normal at any time.</span></span> <span data-ttu-id="6ae8f-125">En particulier, vous pouvez appeler **glNormal3d** entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="6ae8f-125">In particular, you can call **glNormal3d** between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="6ae8f-126">Les fonctions suivantes récupèrent les informations relatives à **glNormal3d**:</span><span class="sxs-lookup"><span data-stu-id="6ae8f-126">The following functions retrieve information related to **glNormal3d**:</span></span>

<span data-ttu-id="6ae8f-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ actuel \_ normal</span><span class="sxs-lookup"><span data-stu-id="6ae8f-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_NORMAL</span></span>

<span data-ttu-id="6ae8f-128">[**glIsEnable**](glisenabled.md) avec argument GL \_ Normalize</span><span class="sxs-lookup"><span data-stu-id="6ae8f-128">[**glIsEnable**](glisenabled.md) with argument GL\_NORMALIZE</span></span>

## <a name="requirements"></a><span data-ttu-id="6ae8f-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6ae8f-129">Requirements</span></span>



| <span data-ttu-id="6ae8f-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6ae8f-130">Requirement</span></span> | <span data-ttu-id="6ae8f-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="6ae8f-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ae8f-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6ae8f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="6ae8f-133">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6ae8f-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6ae8f-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6ae8f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="6ae8f-135">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6ae8f-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6ae8f-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="6ae8f-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ae8f-137"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ae8f-137"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="6ae8f-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6ae8f-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="6ae8f-139"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6ae8f-139"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="6ae8f-140">DLL</span><span class="sxs-lookup"><span data-stu-id="6ae8f-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ae8f-141"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ae8f-141"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ae8f-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6ae8f-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ae8f-143">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="6ae8f-143">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="6ae8f-144">**glColor**</span><span class="sxs-lookup"><span data-stu-id="6ae8f-144">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="6ae8f-145">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="6ae8f-145">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="6ae8f-146">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="6ae8f-146">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="6ae8f-147">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="6ae8f-147">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="6ae8f-148">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="6ae8f-148">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





