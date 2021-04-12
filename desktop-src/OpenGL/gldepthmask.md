---
title: fonction glDepthMask (GL. h)
description: La fonction glDepthMask active ou désactive l’écriture dans le tampon de profondeur.
ms.assetid: 067b18e2-f21a-4dde-8fa6-dd975746e189
keywords:
- glDepthMask fonction OpenGL
topic_type:
- apiref
api_name:
- glDepthMask
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5873d517770f1ce61f9a2eaad3ea7cce7b4fd7ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384816"
---
# <a name="gldepthmask-function"></a><span data-ttu-id="f0706-104">glDepthMask fonction)</span><span class="sxs-lookup"><span data-stu-id="f0706-104">glDepthMask function</span></span>

<span data-ttu-id="f0706-105">La fonction **glDepthMask** active ou désactive l’écriture dans le tampon de profondeur.</span><span class="sxs-lookup"><span data-stu-id="f0706-105">The **glDepthMask** function enables or disables writing into the depth buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0706-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f0706-106">Syntax</span></span>


```C++
void WINAPI glDepthMask(
   GLboolean flag
);
```



## <a name="parameters"></a><span data-ttu-id="f0706-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f0706-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0706-108">*flag*</span><span class="sxs-lookup"><span data-stu-id="f0706-108">*flag*</span></span> 
</dt> <dd>

<span data-ttu-id="f0706-109">Spécifie si la mémoire tampon de profondeur est activée pour l’écriture.</span><span class="sxs-lookup"><span data-stu-id="f0706-109">Specifies whether the depth buffer is enabled for writing.</span></span> <span data-ttu-id="f0706-110">Si l' *indicateur* est égal à zéro, l’écriture dans le tampon de profondeur est désactivée.</span><span class="sxs-lookup"><span data-stu-id="f0706-110">If *flag* is zero, depth-buffer writing is disabled.</span></span> <span data-ttu-id="f0706-111">Dans le cas contraire, il est activé.</span><span class="sxs-lookup"><span data-stu-id="f0706-111">Otherwise, it is enabled.</span></span> <span data-ttu-id="f0706-112">Initialement, l’écriture dans la mémoire tampon de profondeur est activée.</span><span class="sxs-lookup"><span data-stu-id="f0706-112">Initially, depth-buffer writing is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0706-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f0706-113">Return value</span></span>

<span data-ttu-id="f0706-114">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="f0706-114">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f0706-115">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="f0706-115">Error codes</span></span>

<span data-ttu-id="f0706-116">Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="f0706-116">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="f0706-117">Nom</span><span class="sxs-lookup"><span data-stu-id="f0706-117">Name</span></span>                                                                                                  | <span data-ttu-id="f0706-118">Signification</span><span class="sxs-lookup"><span data-stu-id="f0706-118">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f0706-119"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f0706-119"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="f0706-120">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="f0706-120">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f0706-121">Notes</span><span class="sxs-lookup"><span data-stu-id="f0706-121">Remarks</span></span>

<span data-ttu-id="f0706-122">La fonction suivante récupère des informations relatives à **glDepthMask**:</span><span class="sxs-lookup"><span data-stu-id="f0706-122">The following function retrieves information related to **glDepthMask**:</span></span>

<span data-ttu-id="f0706-123">**glGet** avec argument GL \_ Depth \_ WRITEMASK</span><span class="sxs-lookup"><span data-stu-id="f0706-123">**glGet** with argument GL\_DEPTH\_WRITEMASK</span></span>

## <a name="requirements"></a><span data-ttu-id="f0706-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f0706-124">Requirements</span></span>



| <span data-ttu-id="f0706-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f0706-125">Requirement</span></span> | <span data-ttu-id="f0706-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="f0706-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0706-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f0706-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f0706-128">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f0706-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f0706-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f0706-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f0706-130">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f0706-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f0706-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="f0706-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0706-132"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0706-132"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="f0706-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f0706-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="f0706-134"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f0706-134"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f0706-135">DLL</span><span class="sxs-lookup"><span data-stu-id="f0706-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0706-136"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0706-136"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0706-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f0706-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0706-138">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="f0706-138">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="f0706-139">**glColorMask**</span><span class="sxs-lookup"><span data-stu-id="f0706-139">**glColorMask**</span></span>](glcolormask.md)
</dt> <dt>

[<span data-ttu-id="f0706-140">**glDepthFunc**</span><span class="sxs-lookup"><span data-stu-id="f0706-140">**glDepthFunc**</span></span>](gldepthfunc.md)
</dt> <dt>

[<span data-ttu-id="f0706-141">**glDepthRange**</span><span class="sxs-lookup"><span data-stu-id="f0706-141">**glDepthRange**</span></span>](gldepthrange.md)
</dt> <dt>

[<span data-ttu-id="f0706-142">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="f0706-142">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="f0706-143">**glGet**</span><span class="sxs-lookup"><span data-stu-id="f0706-143">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="f0706-144">**glIndexMask**</span><span class="sxs-lookup"><span data-stu-id="f0706-144">**glIndexMask**</span></span>](glindexmask.md)
</dt> <dt>

[<span data-ttu-id="f0706-145">**glStencilMask**</span><span class="sxs-lookup"><span data-stu-id="f0706-145">**glStencilMask**</span></span>](glstencilmask.md)
</dt> </dl>

 

 





