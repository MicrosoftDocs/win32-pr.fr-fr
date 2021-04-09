---
title: fonction glNormal3iv (GL. h)
description: Définit le vecteur normal actuel. | fonction glNormal3iv (GL. h)
ms.assetid: cf50e801-a34c-43bd-b7eb-facb84a6472d
keywords:
- glNormal3iv fonction OpenGL
topic_type:
- apiref
api_name:
- glNormal3iv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5629a12d6c388da2aa133fbe72177646b4f95d63
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103953762"
---
# <a name="glnormal3iv-function"></a><span data-ttu-id="b5986-105">glNormal3iv fonction)</span><span class="sxs-lookup"><span data-stu-id="b5986-105">glNormal3iv function</span></span>

<span data-ttu-id="b5986-106">Définit le vecteur normal actuel.</span><span class="sxs-lookup"><span data-stu-id="b5986-106">Sets the current normal vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5986-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b5986-107">Syntax</span></span>


```C++
void WINAPI glNormal3iv(
   const GLint *v
);
```



## <a name="parameters"></a><span data-ttu-id="b5986-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b5986-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5986-109">*v*</span><span class="sxs-lookup"><span data-stu-id="b5986-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="b5986-110">Pointeur vers un tableau de trois éléments : les coordonnées x, y et z du nouveau normal actuel.</span><span class="sxs-lookup"><span data-stu-id="b5986-110">A pointer to an array of three elements: the x, y, and z coordinates of the new current normal.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5986-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b5986-111">Return value</span></span>

<span data-ttu-id="b5986-112">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="b5986-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5986-113">Notes</span><span class="sxs-lookup"><span data-stu-id="b5986-113">Remarks</span></span>

<span data-ttu-id="b5986-114">La normale actuelle est définie sur les coordonnées données chaque fois que vous appelez la fonction **glNormal3iv**.</span><span class="sxs-lookup"><span data-stu-id="b5986-114">The current normal is set to the given coordinates whenever you call the **glNormal3iv** function.</span></span>

<span data-ttu-id="b5986-115">Les arguments Byte, short ou Integer sont convertis en format à virgule flottante avec un mappage linéaire qui mappe la valeur entière représentable la plus positive à 1,0, et la valeur entière représentable la plus négative à-1,0.</span><span class="sxs-lookup"><span data-stu-id="b5986-115">Byte, short, or integer arguments are converted to floating-point format with a linear mapping that maps the most positive representable integer value to 1.0, and the most negative representable integer value to -1.0.</span></span>

<span data-ttu-id="b5986-116">Les normales spécifiées à l’aide de **glNormal3iv** n’ont pas besoin d’avoir une longueur d’unité.</span><span class="sxs-lookup"><span data-stu-id="b5986-116">Normals specified by using **glNormal3iv** need not have unit length.</span></span> <span data-ttu-id="b5986-117">Si la normalisation est activée, les normales spécifiées avec **glNormal3iv** sont normalisées après la transformation.</span><span class="sxs-lookup"><span data-stu-id="b5986-117">If normalization is enabled, then normals specified with **glNormal3iv** are normalized after transformation.</span></span> <span data-ttu-id="b5986-118">Vous pouvez contrôler la normalisation à l’aide de [**glEnable**](glenable.md) et [**glDisable**](gldisable.md) avec l’argument GL \_ Normalize.</span><span class="sxs-lookup"><span data-stu-id="b5986-118">You can control normalization by using [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with the argument GL\_NORMALIZE.</span></span> <span data-ttu-id="b5986-119">Par défaut, la normalisation est désactivée.</span><span class="sxs-lookup"><span data-stu-id="b5986-119">By default, normalization is disabled.</span></span> <span data-ttu-id="b5986-120">Vous pouvez mettre à jour la normale actuelle à tout moment.</span><span class="sxs-lookup"><span data-stu-id="b5986-120">You can update the current normal at any time.</span></span> <span data-ttu-id="b5986-121">En particulier, vous pouvez appeler **glNormal3iv** entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="b5986-121">In particular, you can call **glNormal3iv** between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="b5986-122">Les fonctions suivantes récupèrent les informations relatives à **glNormal3iv**:</span><span class="sxs-lookup"><span data-stu-id="b5986-122">The following functions retrieve information related to **glNormal3iv**:</span></span>

<span data-ttu-id="b5986-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ actuel \_ normal</span><span class="sxs-lookup"><span data-stu-id="b5986-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_NORMAL</span></span>

<span data-ttu-id="b5986-124">[**glIsEnable**](glisenabled.md) avec argument GL \_ Normalize</span><span class="sxs-lookup"><span data-stu-id="b5986-124">[**glIsEnable**](glisenabled.md) with argument GL\_NORMALIZE</span></span>

## <a name="requirements"></a><span data-ttu-id="b5986-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b5986-125">Requirements</span></span>



| <span data-ttu-id="b5986-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b5986-126">Requirement</span></span> | <span data-ttu-id="b5986-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5986-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5986-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5986-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b5986-129">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b5986-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b5986-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5986-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b5986-131">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b5986-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b5986-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="b5986-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5986-133"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5986-133"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="b5986-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b5986-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="b5986-135"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5986-135"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b5986-136">DLL</span><span class="sxs-lookup"><span data-stu-id="b5986-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5986-137"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5986-137"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5986-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5986-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5986-139">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="b5986-139">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="b5986-140">**glColor**</span><span class="sxs-lookup"><span data-stu-id="b5986-140">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="b5986-141">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="b5986-141">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="b5986-142">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="b5986-142">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="b5986-143">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="b5986-143">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="b5986-144">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="b5986-144">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





