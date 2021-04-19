---
title: fonction glNormal3dv (GL. h)
description: Définit le vecteur normal actuel. | fonction glNormal3dv (GL. h)
ms.assetid: 9d4f8d3c-f4c4-4165-a5f9-edc89319008b
keywords:
- glNormal3dv fonction OpenGL
topic_type:
- apiref
api_name:
- glNormal3dv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84f2c2cefd5b0373808347e8a9ef17eb2ca2f863
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106525835"
---
# <a name="glnormal3dv-function"></a><span data-ttu-id="9ff08-105">glNormal3dv fonction)</span><span class="sxs-lookup"><span data-stu-id="9ff08-105">glNormal3dv function</span></span>

<span data-ttu-id="9ff08-106">Définit le vecteur normal actuel.</span><span class="sxs-lookup"><span data-stu-id="9ff08-106">Sets the current normal vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ff08-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9ff08-107">Syntax</span></span>


```C++
void WINAPI glNormal3dv(
   const GLdouble *v
);
```



## <a name="parameters"></a><span data-ttu-id="9ff08-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9ff08-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ff08-109">*v*</span><span class="sxs-lookup"><span data-stu-id="9ff08-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="9ff08-110">Pointeur vers un tableau de trois éléments : les coordonnées x, y et z du nouveau normal actuel.</span><span class="sxs-lookup"><span data-stu-id="9ff08-110">A pointer to an array of three elements: the x, y, and z coordinates of the new current normal.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ff08-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9ff08-111">Return value</span></span>

<span data-ttu-id="9ff08-112">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="9ff08-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ff08-113">Notes</span><span class="sxs-lookup"><span data-stu-id="9ff08-113">Remarks</span></span>

<span data-ttu-id="9ff08-114">La normale actuelle est définie sur les coordonnées données chaque fois que vous appelez la fonction **glNormal3dv**.</span><span class="sxs-lookup"><span data-stu-id="9ff08-114">The current normal is set to the given coordinates whenever you call the **glNormal3dv** function.</span></span>

<span data-ttu-id="9ff08-115">Les arguments Byte, short ou Integer sont convertis en format à virgule flottante avec un mappage linéaire qui mappe la valeur entière représentable la plus positive à 1,0, et la valeur entière représentable la plus négative à-1,0.</span><span class="sxs-lookup"><span data-stu-id="9ff08-115">Byte, short, or integer arguments are converted to floating-point format with a linear mapping that maps the most positive representable integer value to 1.0, and the most negative representable integer value to -1.0.</span></span>

<span data-ttu-id="9ff08-116">Les normales spécifiées à l’aide de **glNormal3dv** n’ont pas besoin d’avoir une longueur d’unité.</span><span class="sxs-lookup"><span data-stu-id="9ff08-116">Normals specified by using **glNormal3dv** need not have unit length.</span></span> <span data-ttu-id="9ff08-117">Si la normalisation est activée, les normales spécifiées avec **glNormal3dv** sont normalisées après la transformation.</span><span class="sxs-lookup"><span data-stu-id="9ff08-117">If normalization is enabled, then normals specified with **glNormal3dv** are normalized after transformation.</span></span> <span data-ttu-id="9ff08-118">Vous pouvez contrôler la normalisation à l’aide de [**glEnable**](glenable.md) et [**glDisable**](gldisable.md) avec l’argument GL \_ Normalize.</span><span class="sxs-lookup"><span data-stu-id="9ff08-118">You can control normalization by using [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with the argument GL\_NORMALIZE.</span></span> <span data-ttu-id="9ff08-119">Par défaut, la normalisation est désactivée.</span><span class="sxs-lookup"><span data-stu-id="9ff08-119">By default, normalization is disabled.</span></span> <span data-ttu-id="9ff08-120">Vous pouvez mettre à jour la normale actuelle à tout moment.</span><span class="sxs-lookup"><span data-stu-id="9ff08-120">You can update the current normal at any time.</span></span> <span data-ttu-id="9ff08-121">En particulier, vous pouvez appeler **glNormal3dv** entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="9ff08-121">In particular, you can call **glNormal3dv** between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="9ff08-122">Les fonctions suivantes récupèrent les informations relatives à **glNormal3dv**:</span><span class="sxs-lookup"><span data-stu-id="9ff08-122">The following functions retrieve information related to **glNormal3dv**:</span></span>

<span data-ttu-id="9ff08-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ actuel \_ normal</span><span class="sxs-lookup"><span data-stu-id="9ff08-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_NORMAL</span></span>

<span data-ttu-id="9ff08-124">[**glIsEnable**](glisenabled.md) avec argument GL \_ Normalize</span><span class="sxs-lookup"><span data-stu-id="9ff08-124">[**glIsEnable**](glisenabled.md) with argument GL\_NORMALIZE</span></span>

## <a name="requirements"></a><span data-ttu-id="9ff08-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9ff08-125">Requirements</span></span>



| <span data-ttu-id="9ff08-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9ff08-126">Requirement</span></span> | <span data-ttu-id="9ff08-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ff08-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ff08-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9ff08-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9ff08-129">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9ff08-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9ff08-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9ff08-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9ff08-131">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9ff08-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9ff08-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="9ff08-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ff08-133"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ff08-133"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="9ff08-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9ff08-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="9ff08-135"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9ff08-135"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9ff08-136">DLL</span><span class="sxs-lookup"><span data-stu-id="9ff08-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ff08-137"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ff08-137"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ff08-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9ff08-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ff08-139">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="9ff08-139">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="9ff08-140">**glColor**</span><span class="sxs-lookup"><span data-stu-id="9ff08-140">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="9ff08-141">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="9ff08-141">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="9ff08-142">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="9ff08-142">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="9ff08-143">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="9ff08-143">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="9ff08-144">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="9ff08-144">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





