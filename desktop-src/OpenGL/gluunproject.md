---
title: gluUnProject, fonction (Glu. h)
description: La fonction gluUnProject mappe les coordonnées de la fenêtre aux coordonnées de l’objet.
ms.assetid: 6a719fc2-ad40-4b22-9c99-5753f5dbb8a0
keywords:
- gluUnProject fonction OpenGL
topic_type:
- apiref
api_name:
- gluUnProject
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f45311171dd3d71c9e699953c049e0813f2df361
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512201"
---
# <a name="gluunproject-function"></a><span data-ttu-id="474f4-104">gluUnProject fonction)</span><span class="sxs-lookup"><span data-stu-id="474f4-104">gluUnProject function</span></span>

<span data-ttu-id="474f4-105">La fonction **gluUnProject** mappe les coordonnées de la fenêtre aux coordonnées de l’objet.</span><span class="sxs-lookup"><span data-stu-id="474f4-105">The **gluUnProject** function maps window coordinates to object coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="474f4-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="474f4-106">Syntax</span></span>


```C++
int WINAPI gluUnProject(
         GLdouble winx,
         GLdouble winy,
         GLdouble winz,
   const GLdouble modelMatrix[16],
   const GLdouble projMatrix[16],
   const GLint    viewport[4],
         GLdouble *objx,
         GLdouble *objy,
         GLdouble *objz
);
```



## <a name="parameters"></a><span data-ttu-id="474f4-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="474f4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="474f4-108">*winx*</span><span class="sxs-lookup"><span data-stu-id="474f4-108">*winx*</span></span> 
</dt> <dd>

<span data-ttu-id="474f4-109">Coordonnée de fenêtre x à mapper.</span><span class="sxs-lookup"><span data-stu-id="474f4-109">The x window coordinate to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="474f4-110">*winy*</span><span class="sxs-lookup"><span data-stu-id="474f4-110">*winy*</span></span> 
</dt> <dd>

<span data-ttu-id="474f4-111">Coordonnée de fenêtre y à mapper.</span><span class="sxs-lookup"><span data-stu-id="474f4-111">The y window coordinate to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="474f4-112">*winz*</span><span class="sxs-lookup"><span data-stu-id="474f4-112">*winz*</span></span> 
</dt> <dd>

<span data-ttu-id="474f4-113">Coordonnée de fenêtre z à mapper.</span><span class="sxs-lookup"><span data-stu-id="474f4-113">The z window coordinate to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="474f4-114">*modelMatrix*</span><span class="sxs-lookup"><span data-stu-id="474f4-114">*modelMatrix*</span></span> 
</dt> <dd>

<span data-ttu-id="474f4-115">Matrice modelview (à partir d’un appel [**glGetDoublev**](glgetdoublev.md) ).</span><span class="sxs-lookup"><span data-stu-id="474f4-115">The modelview matrix (as from a [**glGetDoublev**](glgetdoublev.md) call).</span></span>

</dd> <dt>

<span data-ttu-id="474f4-116">*projMatrix*</span><span class="sxs-lookup"><span data-stu-id="474f4-116">*projMatrix*</span></span> 
</dt> <dd>

<span data-ttu-id="474f4-117">Matrice de projection (à partir d’un appel **glGetDoublev** ).</span><span class="sxs-lookup"><span data-stu-id="474f4-117">The projection matrix (as from a **glGetDoublev** call).</span></span>

</dd> <dt>

<span data-ttu-id="474f4-118">*vue*</span><span class="sxs-lookup"><span data-stu-id="474f4-118">*viewport*</span></span> 
</dt> <dd>

<span data-ttu-id="474f4-119">La fenêtre d’affichage (à partir d’un appel [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ).</span><span class="sxs-lookup"><span data-stu-id="474f4-119">The viewport (as from a [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) call).</span></span>

</dd> <dt>

<span data-ttu-id="474f4-120">*objx*</span><span class="sxs-lookup"><span data-stu-id="474f4-120">*objx*</span></span> 
</dt> <dd>

<span data-ttu-id="474f4-121">Coordonnée de l’objet x calculé.</span><span class="sxs-lookup"><span data-stu-id="474f4-121">The computed x object coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="474f4-122">*objy*</span><span class="sxs-lookup"><span data-stu-id="474f4-122">*objy*</span></span> 
</dt> <dd>

<span data-ttu-id="474f4-123">Coordonnée de l’objet y calculé.</span><span class="sxs-lookup"><span data-stu-id="474f4-123">The computed y object coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="474f4-124">*objz*</span><span class="sxs-lookup"><span data-stu-id="474f4-124">*objz*</span></span> 
</dt> <dd>

<span data-ttu-id="474f4-125">Coordonnée de l’objet z calculé.</span><span class="sxs-lookup"><span data-stu-id="474f4-125">The computed z object coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="474f4-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="474f4-126">Return value</span></span>

<span data-ttu-id="474f4-127">Si la fonction est réussie, la valeur de retour est GL \_ true.</span><span class="sxs-lookup"><span data-stu-id="474f4-127">If the function succeeds, the return value is GL\_TRUE.</span></span>

<span data-ttu-id="474f4-128">Si la fonction échoue, la valeur de retour est GL \_ false.</span><span class="sxs-lookup"><span data-stu-id="474f4-128">If the function fails, the return value is GL\_FALSE.</span></span>

## <a name="remarks"></a><span data-ttu-id="474f4-129">Notes</span><span class="sxs-lookup"><span data-stu-id="474f4-129">Remarks</span></span>

<span data-ttu-id="474f4-130">La fonction **gluUnProject** mappe les coordonnées de fenêtre spécifiées en coordonnées d’objet à l’aide de *modelMatrix*, *projMatrix* et *Viewport*.</span><span class="sxs-lookup"><span data-stu-id="474f4-130">The **gluUnProject** function maps the specified window coordinates into object coordinates using *modelMatrix*, *projMatrix*, and *viewport*.</span></span> <span data-ttu-id="474f4-131">Le résultat est stocké dans *objX*, *objy* et *objz*.</span><span class="sxs-lookup"><span data-stu-id="474f4-131">The result is stored in *objx*, *objy*, and *objz*.</span></span>

## <a name="requirements"></a><span data-ttu-id="474f4-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="474f4-132">Requirements</span></span>



| <span data-ttu-id="474f4-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="474f4-133">Requirement</span></span> | <span data-ttu-id="474f4-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="474f4-134">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="474f4-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="474f4-135">Minimum supported client</span></span><br/> | <span data-ttu-id="474f4-136">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="474f4-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="474f4-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="474f4-137">Minimum supported server</span></span><br/> | <span data-ttu-id="474f4-138">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="474f4-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="474f4-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="474f4-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="474f4-140"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="474f4-140"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="474f4-141">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="474f4-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="474f4-142"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="474f4-142"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="474f4-143">DLL</span><span class="sxs-lookup"><span data-stu-id="474f4-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="474f4-144"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="474f4-144"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="474f4-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="474f4-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="474f4-146">**glGet**</span><span class="sxs-lookup"><span data-stu-id="474f4-146">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="474f4-147">**glGetDoublev**</span><span class="sxs-lookup"><span data-stu-id="474f4-147">**glGetDoublev**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="474f4-148">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="474f4-148">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="474f4-149">**gluProject**</span><span class="sxs-lookup"><span data-stu-id="474f4-149">**gluProject**</span></span>](gluproject.md)
</dt> </dl>

 

 





