---
title: gluPerspective, fonction (Glu. h)
description: La fonction gluPerspective définit une matrice de projection de perspective.
ms.assetid: 125e2828-a2d7-4c6c-9370-eb21a581ced8
keywords:
- gluPerspective fonction OpenGL
topic_type:
- apiref
api_name:
- gluPerspective
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf30fc7dc4c6ba5a56efd3def6a5a7178f81ed49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385052"
---
# <a name="gluperspective-function"></a><span data-ttu-id="412de-104">gluPerspective fonction)</span><span class="sxs-lookup"><span data-stu-id="412de-104">gluPerspective function</span></span>

<span data-ttu-id="412de-105">La fonction **gluPerspective** définit une matrice de projection de perspective.</span><span class="sxs-lookup"><span data-stu-id="412de-105">The **gluPerspective** function sets up a perspective projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="412de-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="412de-106">Syntax</span></span>


```C++
void WINAPI gluPerspective(
   GLdouble fovy,
   GLdouble aspect,
   GLdouble zNear,
   GLdouble zFar
);
```



## <a name="parameters"></a><span data-ttu-id="412de-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="412de-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="412de-108">*fovy*</span><span class="sxs-lookup"><span data-stu-id="412de-108">*fovy*</span></span> 
</dt> <dd>

<span data-ttu-id="412de-109">Champ d’angle de vue, en degrés, dans l’axe y.</span><span class="sxs-lookup"><span data-stu-id="412de-109">The field of view angle, in degrees, in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="412de-110">*aspect*</span><span class="sxs-lookup"><span data-stu-id="412de-110">*aspect*</span></span> 
</dt> <dd>

<span data-ttu-id="412de-111">Proportions qui détermine le champ de vue sur l’axe x.</span><span class="sxs-lookup"><span data-stu-id="412de-111">The aspect ratio that determines the field of view in the x-direction.</span></span> <span data-ttu-id="412de-112">Les proportions sont le rapport entre *x* (largeur) et *y* (hauteur).</span><span class="sxs-lookup"><span data-stu-id="412de-112">The aspect ratio is the ratio of *x* (width) to *y* (height).</span></span>

</dd> <dt>

<span data-ttu-id="412de-113">*zNear*</span><span class="sxs-lookup"><span data-stu-id="412de-113">*zNear*</span></span> 
</dt> <dd>

<span data-ttu-id="412de-114">Distance entre la visionneuse et le plan de découpage proche (toujours positive).</span><span class="sxs-lookup"><span data-stu-id="412de-114">The distance from the viewer to the near clipping plane (always positive).</span></span>

</dd> <dt>

<span data-ttu-id="412de-115">*zFar*</span><span class="sxs-lookup"><span data-stu-id="412de-115">*zFar*</span></span> 
</dt> <dd>

<span data-ttu-id="412de-116">Distance entre la visionneuse et le plan de découpage Far (toujours positive).</span><span class="sxs-lookup"><span data-stu-id="412de-116">The distance from the viewer to the far clipping plane (always positive).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="412de-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="412de-117">Return value</span></span>

<span data-ttu-id="412de-118">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="412de-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="412de-119">Notes</span><span class="sxs-lookup"><span data-stu-id="412de-119">Remarks</span></span>

<span data-ttu-id="412de-120">La fonction **gluPerspective** spécifie un frustum d’affichage dans le système de coordonnées universel.</span><span class="sxs-lookup"><span data-stu-id="412de-120">The **gluPerspective** function specifies a viewing frustum into the world coordinate system.</span></span> <span data-ttu-id="412de-121">En général, les proportions dans **gluPerspective** doivent correspondre aux proportions de la fenêtre d’affichage associée.</span><span class="sxs-lookup"><span data-stu-id="412de-121">In general, the aspect ratio in **gluPerspective** should match the aspect ratio of the associated viewport.</span></span> <span data-ttu-id="412de-122">Par exemple, l' *aspect* = 2,0 signifie que l’angle de vue de la visionneuse est deux fois plus large dans *x* que dans *y*.</span><span class="sxs-lookup"><span data-stu-id="412de-122">For example, *aspect* = 2.0 means the viewer's angle of view is twice as wide in *x* as it is in *y*.</span></span> <span data-ttu-id="412de-123">Si la fenêtre d’affichage est deux fois plus larges que sa hauteur, elle affiche l’image sans distorsion.</span><span class="sxs-lookup"><span data-stu-id="412de-123">If the viewport is twice as wide as it is tall, it displays the image without distortion.</span></span>

<span data-ttu-id="412de-124">La matrice générée par **gluPerspective** est multipliée par la matrice actuelle, tout comme si [**glMultMatrix**](glmultmatrix.md) était appelé avec la matrice générée.</span><span class="sxs-lookup"><span data-stu-id="412de-124">The matrix generated by **gluPerspective** is multiplied by the current matrix, just as if [**glMultMatrix**](glmultmatrix.md) were called with the generated matrix.</span></span> <span data-ttu-id="412de-125">Pour charger la matrice de perspective sur la pile de matrice actuelle, faites précéder l’appel à **gluPerspective** d’un appel à [**glLoadIdentity**](glloadidentity.md).</span><span class="sxs-lookup"><span data-stu-id="412de-125">To load the perspective matrix onto the current matrix stack instead, precede the call to **gluPerspective** with a call to [**glLoadIdentity**](glloadidentity.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="412de-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="412de-126">Requirements</span></span>



| <span data-ttu-id="412de-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="412de-127">Requirement</span></span> | <span data-ttu-id="412de-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="412de-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="412de-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="412de-129">Minimum supported client</span></span><br/> | <span data-ttu-id="412de-130">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="412de-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="412de-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="412de-131">Minimum supported server</span></span><br/> | <span data-ttu-id="412de-132">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="412de-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="412de-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="412de-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="412de-134"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="412de-134"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="412de-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="412de-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="412de-136"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="412de-136"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="412de-137">DLL</span><span class="sxs-lookup"><span data-stu-id="412de-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="412de-138"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="412de-138"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="412de-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="412de-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="412de-140">**glFrustum**</span><span class="sxs-lookup"><span data-stu-id="412de-140">**glFrustum**</span></span>](glfrustum.md)
</dt> <dt>

[<span data-ttu-id="412de-141">**glLoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="412de-141">**glLoadIdentity**</span></span>](glloadidentity.md)
</dt> <dt>

[<span data-ttu-id="412de-142">**glMultMatrix**</span><span class="sxs-lookup"><span data-stu-id="412de-142">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="412de-143">**gluOrtho2D**</span><span class="sxs-lookup"><span data-stu-id="412de-143">**gluOrtho2D**</span></span>](gluortho2d.md)
</dt> </dl>

 

 





