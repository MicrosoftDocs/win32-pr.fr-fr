---
title: fonction glNormal3fv (GL. h)
description: Définit le vecteur normal actuel. | fonction glNormal3fv (GL. h)
ms.assetid: 8e501de8-5877-4d77-9f32-4596d5217636
keywords:
- glNormal3fv fonction OpenGL
topic_type:
- apiref
api_name:
- glNormal3fv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33de53f6c5d363218f602319dbc71e7436e475ed
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106539420"
---
# <a name="glnormal3fv-function"></a><span data-ttu-id="04a97-105">glNormal3fv fonction)</span><span class="sxs-lookup"><span data-stu-id="04a97-105">glNormal3fv function</span></span>

<span data-ttu-id="04a97-106">Définit le vecteur normal actuel.</span><span class="sxs-lookup"><span data-stu-id="04a97-106">Sets the current normal vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="04a97-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="04a97-107">Syntax</span></span>


```C++
void WINAPI glNormal3fv(
   const GLfloat *v
);
```



## <a name="parameters"></a><span data-ttu-id="04a97-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="04a97-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04a97-109">*v*</span><span class="sxs-lookup"><span data-stu-id="04a97-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="04a97-110">Pointeur vers un tableau de trois éléments : les coordonnées x, y et z du nouveau normal actuel.</span><span class="sxs-lookup"><span data-stu-id="04a97-110">A pointer to an array of three elements: the x, y, and z coordinates of the new current normal.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04a97-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="04a97-111">Return value</span></span>

<span data-ttu-id="04a97-112">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="04a97-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="04a97-113">Notes</span><span class="sxs-lookup"><span data-stu-id="04a97-113">Remarks</span></span>

<span data-ttu-id="04a97-114">La normale actuelle est définie sur les coordonnées données chaque fois que vous appelez la fonction **glNormal3fv**.</span><span class="sxs-lookup"><span data-stu-id="04a97-114">The current normal is set to the given coordinates whenever you call the **glNormal3fv** function.</span></span>

<span data-ttu-id="04a97-115">Les arguments Byte, short ou Integer sont convertis en format à virgule flottante avec un mappage linéaire qui mappe la valeur entière représentable la plus positive à 1,0, et la valeur entière représentable la plus négative à-1,0.</span><span class="sxs-lookup"><span data-stu-id="04a97-115">Byte, short, or integer arguments are converted to floating-point format with a linear mapping that maps the most positive representable integer value to 1.0, and the most negative representable integer value to -1.0.</span></span>

<span data-ttu-id="04a97-116">Les normales spécifiées à l’aide de **glNormal3fv** n’ont pas besoin d’avoir une longueur d’unité.</span><span class="sxs-lookup"><span data-stu-id="04a97-116">Normals specified by using **glNormal3fv** need not have unit length.</span></span> <span data-ttu-id="04a97-117">Si la normalisation est activée, les normales spécifiées avec **glNormal3fv** sont normalisées après la transformation.</span><span class="sxs-lookup"><span data-stu-id="04a97-117">If normalization is enabled, then normals specified with **glNormal3fv** are normalized after transformation.</span></span> <span data-ttu-id="04a97-118">Vous pouvez contrôler la normalisation à l’aide de [**glEnable**](glenable.md) et [**glDisable**](gldisable.md) avec l’argument GL \_ Normalize.</span><span class="sxs-lookup"><span data-stu-id="04a97-118">You can control normalization by using [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with the argument GL\_NORMALIZE.</span></span> <span data-ttu-id="04a97-119">Par défaut, la normalisation est désactivée.</span><span class="sxs-lookup"><span data-stu-id="04a97-119">By default, normalization is disabled.</span></span> <span data-ttu-id="04a97-120">Vous pouvez mettre à jour la normale actuelle à tout moment.</span><span class="sxs-lookup"><span data-stu-id="04a97-120">You can update the current normal can at any time.</span></span> <span data-ttu-id="04a97-121">En particulier, vous pouvez appeler **glNormal3fv** entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="04a97-121">In particular, you can call **glNormal3fv** between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="04a97-122">Les fonctions suivantes récupèrent les informations relatives à **glNormal3fv**:</span><span class="sxs-lookup"><span data-stu-id="04a97-122">The following functions retrieve information related to **glNormal3fv**:</span></span>

<span data-ttu-id="04a97-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ actuel \_ normal</span><span class="sxs-lookup"><span data-stu-id="04a97-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_NORMAL</span></span>

<span data-ttu-id="04a97-124">[**glIsEnable**](glisenabled.md) avec argument GL \_ Normalize</span><span class="sxs-lookup"><span data-stu-id="04a97-124">[**glIsEnable**](glisenabled.md) with argument GL\_NORMALIZE</span></span>

## <a name="requirements"></a><span data-ttu-id="04a97-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="04a97-125">Requirements</span></span>



| <span data-ttu-id="04a97-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="04a97-126">Requirement</span></span> | <span data-ttu-id="04a97-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="04a97-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="04a97-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04a97-128">Minimum supported client</span></span><br/> | <span data-ttu-id="04a97-129">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="04a97-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="04a97-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04a97-130">Minimum supported server</span></span><br/> | <span data-ttu-id="04a97-131">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="04a97-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="04a97-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="04a97-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="04a97-133"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="04a97-133"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="04a97-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="04a97-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="04a97-135"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="04a97-135"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="04a97-136">DLL</span><span class="sxs-lookup"><span data-stu-id="04a97-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04a97-137"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04a97-137"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04a97-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="04a97-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04a97-139">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="04a97-139">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="04a97-140">**glColor**</span><span class="sxs-lookup"><span data-stu-id="04a97-140">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="04a97-141">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="04a97-141">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="04a97-142">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="04a97-142">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="04a97-143">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="04a97-143">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="04a97-144">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="04a97-144">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





