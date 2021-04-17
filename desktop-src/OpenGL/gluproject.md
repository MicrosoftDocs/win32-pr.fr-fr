---
title: gluProject, fonction (Glu. h)
description: La fonction gluProject mappe les coordonnées d’objet aux coordonnées de la fenêtre.
ms.assetid: cfd8bc5b-b684-4207-8bdb-bf086858da13
keywords:
- gluProject fonction OpenGL
topic_type:
- apiref
api_name:
- gluProject
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84972d95d381a630bf6caf7f0099ce740a4f2741
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466179"
---
# <a name="gluproject-function"></a><span data-ttu-id="9eb1e-104">gluProject fonction)</span><span class="sxs-lookup"><span data-stu-id="9eb1e-104">gluProject function</span></span>

<span data-ttu-id="9eb1e-105">La fonction **gluProject** mappe les coordonnées d’objet aux coordonnées de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="9eb1e-105">The **gluProject** function maps object coordinates to window coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="9eb1e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9eb1e-106">Syntax</span></span>


```C++
int WINAPI gluProject(
         GLdouble objx,
         GLdouble objy,
         GLdouble objz,
   const GLdouble modelMatrix[16],
   const GLdouble projMatrix[16],
   const GLint    viewport[4],
         GLdouble *winx,
         GLdouble *winy,
         GLdouble *winz
);
```



## <a name="parameters"></a><span data-ttu-id="9eb1e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9eb1e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9eb1e-108">*objx*</span><span class="sxs-lookup"><span data-stu-id="9eb1e-108">*objx*</span></span> 
</dt> <dd>

<span data-ttu-id="9eb1e-109">Coordonnée de l’objet x.</span><span class="sxs-lookup"><span data-stu-id="9eb1e-109">The x object coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="9eb1e-110">*objy*</span><span class="sxs-lookup"><span data-stu-id="9eb1e-110">*objy*</span></span> 
</dt> <dd>

<span data-ttu-id="9eb1e-111">Coordonnée de l’objet y.</span><span class="sxs-lookup"><span data-stu-id="9eb1e-111">The y object coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="9eb1e-112">*objz*</span><span class="sxs-lookup"><span data-stu-id="9eb1e-112">*objz*</span></span> 
</dt> <dd>

<span data-ttu-id="9eb1e-113">Coordonnée de l’objet z.</span><span class="sxs-lookup"><span data-stu-id="9eb1e-113">The z object coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="9eb1e-114">*modelMatrix*</span><span class="sxs-lookup"><span data-stu-id="9eb1e-114">*modelMatrix*</span></span> 
</dt> <dd>

<span data-ttu-id="9eb1e-115">Matrice modelview actuelle (à partir d’un appel [**glGetDoublev**](glgetdoublev.md) ).</span><span class="sxs-lookup"><span data-stu-id="9eb1e-115">The current modelview matrix (as from a [**glGetDoublev**](glgetdoublev.md) call).</span></span>

</dd> <dt>

<span data-ttu-id="9eb1e-116">*projMatrix*</span><span class="sxs-lookup"><span data-stu-id="9eb1e-116">*projMatrix*</span></span> 
</dt> <dd>

<span data-ttu-id="9eb1e-117">La matrice de projection actuelle (à partir d’un appel **glGetDoublev** ).</span><span class="sxs-lookup"><span data-stu-id="9eb1e-117">The current projection matrix (as from a **glGetDoublev** call).</span></span>

</dd> <dt>

<span data-ttu-id="9eb1e-118">*vue*</span><span class="sxs-lookup"><span data-stu-id="9eb1e-118">*viewport*</span></span> 
</dt> <dd>

<span data-ttu-id="9eb1e-119">La fenêtre d’affichage actuelle (à partir d’un appel [**glGetIntegerv**](glgetintegerv.md) ).</span><span class="sxs-lookup"><span data-stu-id="9eb1e-119">The current viewport (as from a [**glGetIntegerv**](glgetintegerv.md) call).</span></span>

</dd> <dt>

<span data-ttu-id="9eb1e-120">*winx*</span><span class="sxs-lookup"><span data-stu-id="9eb1e-120">*winx*</span></span> 
</dt> <dd>

<span data-ttu-id="9eb1e-121">Coordonnée x de la fenêtre calculée.</span><span class="sxs-lookup"><span data-stu-id="9eb1e-121">The computed x window coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="9eb1e-122">*winy*</span><span class="sxs-lookup"><span data-stu-id="9eb1e-122">*winy*</span></span> 
</dt> <dd>

<span data-ttu-id="9eb1e-123">Coordonnée de la fenêtre y calculée.</span><span class="sxs-lookup"><span data-stu-id="9eb1e-123">The computed y window coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="9eb1e-124">*winz*</span><span class="sxs-lookup"><span data-stu-id="9eb1e-124">*winz*</span></span> 
</dt> <dd>

<span data-ttu-id="9eb1e-125">Coordonnée de la fenêtre z calculée.</span><span class="sxs-lookup"><span data-stu-id="9eb1e-125">The computed z window coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9eb1e-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9eb1e-126">Return value</span></span>

<span data-ttu-id="9eb1e-127">Si la fonction est réussie, la valeur de retour est GL \_ true.</span><span class="sxs-lookup"><span data-stu-id="9eb1e-127">If the function succeeds, the return value is GL\_TRUE.</span></span>

<span data-ttu-id="9eb1e-128">Si la fonction échoue, la valeur de retour est GL \_ false.</span><span class="sxs-lookup"><span data-stu-id="9eb1e-128">If the function fails, the return value is GL\_FALSE.</span></span>

## <a name="remarks"></a><span data-ttu-id="9eb1e-129">Notes</span><span class="sxs-lookup"><span data-stu-id="9eb1e-129">Remarks</span></span>

<span data-ttu-id="9eb1e-130">La fonction **gluProject** transforme les coordonnées d’objet spécifiées en coordonnées de fenêtre à l’aide de *modelMatrix*, *projMatrix* et *Viewport*.</span><span class="sxs-lookup"><span data-stu-id="9eb1e-130">The **gluProject** function transforms the specified object coordinates into window coordinates using *modelMatrix*, *projMatrix*, and *viewport*.</span></span> <span data-ttu-id="9eb1e-131">Le résultat est stocké dans *Winx*, *winy* et *WINZ*.</span><span class="sxs-lookup"><span data-stu-id="9eb1e-131">The result is stored in *winx*, *winy*, and *winz*.</span></span>

## <a name="requirements"></a><span data-ttu-id="9eb1e-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9eb1e-132">Requirements</span></span>



| <span data-ttu-id="9eb1e-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9eb1e-133">Requirement</span></span> | <span data-ttu-id="9eb1e-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="9eb1e-134">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9eb1e-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9eb1e-135">Minimum supported client</span></span><br/> | <span data-ttu-id="9eb1e-136">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9eb1e-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="9eb1e-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9eb1e-137">Minimum supported server</span></span><br/> | <span data-ttu-id="9eb1e-138">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9eb1e-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9eb1e-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="9eb1e-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="9eb1e-140"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="9eb1e-140"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="9eb1e-141">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9eb1e-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="9eb1e-142"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9eb1e-142"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9eb1e-143">DLL</span><span class="sxs-lookup"><span data-stu-id="9eb1e-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9eb1e-144"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9eb1e-144"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9eb1e-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9eb1e-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9eb1e-146">**glGetDoublev**</span><span class="sxs-lookup"><span data-stu-id="9eb1e-146">**glGetDoublev**</span></span>](glgetdoublev.md)
</dt> <dt>

[<span data-ttu-id="9eb1e-147">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="9eb1e-147">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="9eb1e-148">**gluUnProject**</span><span class="sxs-lookup"><span data-stu-id="9eb1e-148">**gluUnProject**</span></span>](gluunproject.md)
</dt> </dl>

 

 





