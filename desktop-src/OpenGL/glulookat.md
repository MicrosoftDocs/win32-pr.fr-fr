---
title: gluLookAt, fonction (Glu. h)
description: La fonction gluLookAt définit une transformation d’affichage.
ms.assetid: 1fd87701-19c2-49b9-99ac-10e70aaedbfd
keywords:
- gluLookAt fonction OpenGL
topic_type:
- apiref
api_name:
- gluLookAt
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5866f3c06ef6969c95eeef4b23fff7a4e7852eb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844386"
---
# <a name="glulookat-function"></a><span data-ttu-id="fc2de-104">gluLookAt fonction)</span><span class="sxs-lookup"><span data-stu-id="fc2de-104">gluLookAt function</span></span>

<span data-ttu-id="fc2de-105">La fonction **gluLookAt** définit une transformation d’affichage.</span><span class="sxs-lookup"><span data-stu-id="fc2de-105">The **gluLookAt** function defines a viewing transformation.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc2de-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fc2de-106">Syntax</span></span>


```C++
void WINAPI gluLookAt(
   GLdouble eyex,
   GLdouble eyey,
   GLdouble eyez,
   GLdouble centerx,
   GLdouble centery,
   GLdouble centerz,
   GLdouble upx,
   GLdouble upy,
   GLdouble upz
);
```



## <a name="parameters"></a><span data-ttu-id="fc2de-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fc2de-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc2de-108">*eyex*</span><span class="sxs-lookup"><span data-stu-id="fc2de-108">*eyex*</span></span> 
</dt> <dd>

<span data-ttu-id="fc2de-109">Position du point oculaire.</span><span class="sxs-lookup"><span data-stu-id="fc2de-109">The position of the eye point.</span></span>

</dd> <dt>

<span data-ttu-id="fc2de-110">*eyey*</span><span class="sxs-lookup"><span data-stu-id="fc2de-110">*eyey*</span></span> 
</dt> <dd>

<span data-ttu-id="fc2de-111">Position du point oculaire.</span><span class="sxs-lookup"><span data-stu-id="fc2de-111">The position of the eye point.</span></span>

</dd> <dt>

<span data-ttu-id="fc2de-112">*eyez*</span><span class="sxs-lookup"><span data-stu-id="fc2de-112">*eyez*</span></span> 
</dt> <dd>

<span data-ttu-id="fc2de-113">Position du point oculaire.</span><span class="sxs-lookup"><span data-stu-id="fc2de-113">The position of the eye point.</span></span>

</dd> <dt>

<span data-ttu-id="fc2de-114">*Center*</span><span class="sxs-lookup"><span data-stu-id="fc2de-114">*centerx*</span></span> 
</dt> <dd>

<span data-ttu-id="fc2de-115">Position du point de référence.</span><span class="sxs-lookup"><span data-stu-id="fc2de-115">The position of the reference point.</span></span>

</dd> <dt>

<span data-ttu-id="fc2de-116">*CenterY*</span><span class="sxs-lookup"><span data-stu-id="fc2de-116">*centery*</span></span> 
</dt> <dd>

<span data-ttu-id="fc2de-117">Position du point de référence.</span><span class="sxs-lookup"><span data-stu-id="fc2de-117">The position of the reference point.</span></span>

</dd> <dt>

<span data-ttu-id="fc2de-118">*CenterZ*</span><span class="sxs-lookup"><span data-stu-id="fc2de-118">*centerz*</span></span> 
</dt> <dd>

<span data-ttu-id="fc2de-119">Position du point de référence.</span><span class="sxs-lookup"><span data-stu-id="fc2de-119">The position of the reference point.</span></span>

</dd> <dt>

<span data-ttu-id="fc2de-120">*UPX*</span><span class="sxs-lookup"><span data-stu-id="fc2de-120">*upx*</span></span> 
</dt> <dd>

<span data-ttu-id="fc2de-121">Direction du vecteur up.</span><span class="sxs-lookup"><span data-stu-id="fc2de-121">The direction of the up vector.</span></span>

</dd> <dt>

<span data-ttu-id="fc2de-122">*upy*</span><span class="sxs-lookup"><span data-stu-id="fc2de-122">*upy*</span></span> 
</dt> <dd>

<span data-ttu-id="fc2de-123">Direction du vecteur up.</span><span class="sxs-lookup"><span data-stu-id="fc2de-123">The direction of the up vector.</span></span>

</dd> <dt>

<span data-ttu-id="fc2de-124">*upz*</span><span class="sxs-lookup"><span data-stu-id="fc2de-124">*upz*</span></span> 
</dt> <dd>

<span data-ttu-id="fc2de-125">Direction du vecteur up.</span><span class="sxs-lookup"><span data-stu-id="fc2de-125">The direction of the up vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc2de-126">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="fc2de-126">Return value</span></span>

<span data-ttu-id="fc2de-127">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="fc2de-127">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc2de-128">Notes</span><span class="sxs-lookup"><span data-stu-id="fc2de-128">Remarks</span></span>

<span data-ttu-id="fc2de-129">La fonction **gluLookAt** crée une matrice d’affichage dérivée d’un point oculaire, un point de référence indiquant le centre de la scène et un vecteur up.</span><span class="sxs-lookup"><span data-stu-id="fc2de-129">The **gluLookAt** function creates a viewing matrix derived from an eye point, a reference point indicating the center of the scene, and an up vector.</span></span> <span data-ttu-id="fc2de-130">La matrice mappe le point de référence à l’axe z négatif et l’œil au point d’origine, de sorte que lorsque vous utilisez une matrice de projection classique, le centre de la scène est mappé au centre de la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="fc2de-130">The matrix maps the reference point to the negative z-axis and the eye point to the origin, so that when you use a typical projection matrix, the center of the scene maps to the center of the viewport.</span></span> <span data-ttu-id="fc2de-131">De même, la direction décrite par le vecteur vers le haut projeté sur le plan d’affichage est mappée sur l’axe des y positif afin qu’il pointe vers le haut dans la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="fc2de-131">Similarly, the direction described by the up vector projected onto the viewing plane is mapped to the positive y-axis so that it points upward in the viewport.</span></span> <span data-ttu-id="fc2de-132">Le vecteur up ne doit pas être parallèle à la ligne de vue du point de vue du point de référence.</span><span class="sxs-lookup"><span data-stu-id="fc2de-132">The up vector must not be parallel to the line of sight from the eye to the reference point.</span></span>

<span data-ttu-id="fc2de-133">La matrice générée par **gluLookAt** postmultiplies la matrice actuelle.</span><span class="sxs-lookup"><span data-stu-id="fc2de-133">The matrix generated by **gluLookAt** postmultiplies the current matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc2de-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fc2de-134">Requirements</span></span>



| <span data-ttu-id="fc2de-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fc2de-135">Requirement</span></span> | <span data-ttu-id="fc2de-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="fc2de-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fc2de-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fc2de-137">Minimum supported client</span></span><br/> | <span data-ttu-id="fc2de-138">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fc2de-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="fc2de-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fc2de-139">Minimum supported server</span></span><br/> | <span data-ttu-id="fc2de-140">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fc2de-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="fc2de-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="fc2de-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc2de-142"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc2de-142"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="fc2de-143">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fc2de-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="fc2de-144"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fc2de-144"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="fc2de-145">DLL</span><span class="sxs-lookup"><span data-stu-id="fc2de-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc2de-146"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc2de-146"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc2de-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fc2de-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc2de-148">**glFrustum**</span><span class="sxs-lookup"><span data-stu-id="fc2de-148">**glFrustum**</span></span>](glfrustum.md)
</dt> <dt>

[<span data-ttu-id="fc2de-149">**gluPerspective**</span><span class="sxs-lookup"><span data-stu-id="fc2de-149">**gluPerspective**</span></span>](gluperspective.md)
</dt> </dl>

 

 





