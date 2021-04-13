---
title: fonction glIsTexture (GL. h)
description: La fonction glIsTexture détermine si un nom correspond à une texture.
ms.assetid: 89d06642-ff28-4a67-ac7f-ca58150f301e
keywords:
- glIsTexture fonction OpenGL
topic_type:
- apiref
api_name:
- glIsTexture
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8897cc0eb004da701f28b410f2ca28b6194c9d26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466638"
---
# <a name="glistexture-function"></a><span data-ttu-id="bf9be-104">glIsTexture fonction)</span><span class="sxs-lookup"><span data-stu-id="bf9be-104">glIsTexture function</span></span>

<span data-ttu-id="bf9be-105">La fonction **glIsTexture** détermine si un nom correspond à une texture.</span><span class="sxs-lookup"><span data-stu-id="bf9be-105">The **glIsTexture** function determines if a name corresponds to a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf9be-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bf9be-106">Syntax</span></span>


```C++
GLboolean WINAPI glIsTexture(
   GLuint texture
);
```



## <a name="parameters"></a><span data-ttu-id="bf9be-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bf9be-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf9be-108">*motif*</span><span class="sxs-lookup"><span data-stu-id="bf9be-108">*texture*</span></span> 
</dt> <dd>

<span data-ttu-id="bf9be-109">Valeur qui est le nom d’une texture.</span><span class="sxs-lookup"><span data-stu-id="bf9be-109">A value that is the name of a texture.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="bf9be-110">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="bf9be-110">Error codes</span></span>

<span data-ttu-id="bf9be-111">Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="bf9be-111">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="bf9be-112">Nom</span><span class="sxs-lookup"><span data-stu-id="bf9be-112">Name</span></span>                                                                                                  | <span data-ttu-id="bf9be-113">Signification</span><span class="sxs-lookup"><span data-stu-id="bf9be-113">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bf9be-114"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bf9be-114"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="bf9be-115">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="bf9be-115">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="bf9be-116">Notes</span><span class="sxs-lookup"><span data-stu-id="bf9be-116">Remarks</span></span>

<span data-ttu-id="bf9be-117">Si le paramètre de *texture* est actuellement le nom d’une texture, la fonction **glIsTexture** retourne la \_ valeur GL true.</span><span class="sxs-lookup"><span data-stu-id="bf9be-117">If the *texture* parameter is currently the name of a texture, the **glIsTexture** function returns GL\_TRUE.</span></span> <span data-ttu-id="bf9be-118">La fonction **glIsTexture** retourne GL \_ false si la *texture* est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="bf9be-118">The **glIsTexture** function returns GL\_FALSE if *texture* is zero.</span></span> <span data-ttu-id="bf9be-119">Elle retourne également \_ le GL false s’il s’agit d’une valeur différente de zéro qui n’est pas le nom d’une texture actuellement, ou si une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="bf9be-119">It also returns GL\_FALSE if it is a non-zero value that is not currently the name of a texture, or if an error occurs.</span></span>

<span data-ttu-id="bf9be-120">Vous ne pouvez pas inclure d’appels à **glIsTexture** dans des listes d’affichage.</span><span class="sxs-lookup"><span data-stu-id="bf9be-120">You cannot include calls to **glIsTexture** in display lists.</span></span>

> [!Note]  
> <span data-ttu-id="bf9be-121">La fonction **glIsTexture** est disponible uniquement dans OpenGL version 1,1 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="bf9be-121">The **glIsTexture** function is only available in OpenGL version 1.1 or later.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bf9be-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bf9be-122">Requirements</span></span>



| <span data-ttu-id="bf9be-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bf9be-123">Requirement</span></span> | <span data-ttu-id="bf9be-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="bf9be-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf9be-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf9be-125">Minimum supported client</span></span><br/> | <span data-ttu-id="bf9be-126">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bf9be-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="bf9be-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf9be-127">Minimum supported server</span></span><br/> | <span data-ttu-id="bf9be-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bf9be-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bf9be-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="bf9be-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf9be-130"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf9be-130"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="bf9be-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bf9be-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="bf9be-132"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bf9be-132"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="bf9be-133">DLL</span><span class="sxs-lookup"><span data-stu-id="bf9be-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf9be-134"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf9be-134"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf9be-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf9be-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf9be-136">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="bf9be-136">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="bf9be-137">**glBindTexture**</span><span class="sxs-lookup"><span data-stu-id="bf9be-137">**glBindTexture**</span></span>](glbindtexture.md)
</dt> <dt>

[<span data-ttu-id="bf9be-138">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="bf9be-138">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="bf9be-139">**glGenTextures**</span><span class="sxs-lookup"><span data-stu-id="bf9be-139">**glGenTextures**</span></span>](glgentextures.md)
</dt> <dt>

[<span data-ttu-id="bf9be-140">**glGet**</span><span class="sxs-lookup"><span data-stu-id="bf9be-140">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="bf9be-141">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="bf9be-141">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="bf9be-142">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="bf9be-142">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="bf9be-143">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="bf9be-143">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="bf9be-144">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="bf9be-144">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





