---
title: fonction glMatrixMode (GL. h)
description: La fonction glMatrixMode spécifie la matrice qui est la matrice actuelle.
ms.assetid: f1006ea3-322a-42a9-b33c-6c7181985ef9
keywords:
- glMatrixMode fonction OpenGL
topic_type:
- apiref
api_name:
- glMatrixMode
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9877d62fc6e721cc6757206c7c2d07d24f3e879b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104680"
---
# <a name="glmatrixmode-function"></a><span data-ttu-id="3c587-104">glMatrixMode fonction)</span><span class="sxs-lookup"><span data-stu-id="3c587-104">glMatrixMode function</span></span>

<span data-ttu-id="3c587-105">La fonction **glMatrixMode** spécifie la matrice qui est la matrice actuelle.</span><span class="sxs-lookup"><span data-stu-id="3c587-105">The **glMatrixMode** function specifies which matrix is the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c587-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3c587-106">Syntax</span></span>


```C++
void WINAPI glMatrixMode(
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="3c587-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3c587-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c587-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="3c587-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="3c587-109">Pile de matrices qui est la cible pour les opérations de matrice suivantes.</span><span class="sxs-lookup"><span data-stu-id="3c587-109">The matrix stack that is the target for subsequent matrix operations.</span></span> <span data-ttu-id="3c587-110">Le paramètre *mode* peut prendre l’une des trois valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="3c587-110">The *mode* parameter can assume one of three values.</span></span>



| <span data-ttu-id="3c587-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="3c587-111">Value</span></span>                                                                                                                                                         | <span data-ttu-id="3c587-112">Signification</span><span class="sxs-lookup"><span data-stu-id="3c587-112">Meaning</span></span>                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="GL_MODELVIEW"></span><span id="gl_modelview"></span><dl> <span data-ttu-id="3c587-113"><dt>**\_MODELVIEW GL**</dt></span><span class="sxs-lookup"><span data-stu-id="3c587-113"><dt>**GL\_MODELVIEW**</dt></span></span> </dl>    | <span data-ttu-id="3c587-114">Applique les opérations de matrice suivantes à la pile de matrices modelview.</span><span class="sxs-lookup"><span data-stu-id="3c587-114">Applies subsequent matrix operations to the modelview matrix stack.</span></span><br/>  |
| <span id="GL_PROJECTION"></span><span id="gl_projection"></span><dl> <span data-ttu-id="3c587-115"><dt>**\_projection GL**</dt></span><span class="sxs-lookup"><span data-stu-id="3c587-115"><dt>**GL\_PROJECTION**</dt></span></span> </dl> | <span data-ttu-id="3c587-116">Applique les opérations de matrice suivantes à la pile de matrice de projection.</span><span class="sxs-lookup"><span data-stu-id="3c587-116">Applies subsequent matrix operations to the projection matrix stack.</span></span><br/> |
| <span id="GL_TEXTURE"></span><span id="gl_texture"></span><dl> <span data-ttu-id="3c587-117"><dt>**\_texture GL**</dt></span><span class="sxs-lookup"><span data-stu-id="3c587-117"><dt>**GL\_TEXTURE**</dt></span></span> </dl>          | <span data-ttu-id="3c587-118">Applique les opérations de matrice suivantes à la pile de matrice de texture.</span><span class="sxs-lookup"><span data-stu-id="3c587-118">Applies subsequent matrix operations to the texture matrix stack.</span></span><br/>    |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c587-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3c587-119">Return value</span></span>

<span data-ttu-id="3c587-120">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="3c587-120">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3c587-121">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="3c587-121">Error codes</span></span>

<span data-ttu-id="3c587-122">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="3c587-122">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="3c587-123">Nom</span><span class="sxs-lookup"><span data-stu-id="3c587-123">Name</span></span>                                                                                                  | <span data-ttu-id="3c587-124">Signification</span><span class="sxs-lookup"><span data-stu-id="3c587-124">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3c587-125"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3c587-125"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="3c587-126">le *mode* n’était pas une valeur acceptée.</span><span class="sxs-lookup"><span data-stu-id="3c587-126">*mode* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="3c587-127"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3c587-127"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="3c587-128">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="3c587-128">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="3c587-129">Notes</span><span class="sxs-lookup"><span data-stu-id="3c587-129">Remarks</span></span>

<span data-ttu-id="3c587-130">La fonction **glMatrixMode** définit le mode matrice actuel.</span><span class="sxs-lookup"><span data-stu-id="3c587-130">The **glMatrixMode** function sets the current matrix mode.</span></span>

<span data-ttu-id="3c587-131">La fonction suivante récupère des informations relatives à **glMatrixMode**:</span><span class="sxs-lookup"><span data-stu-id="3c587-131">The following function retrieves information related to **glMatrixMode**:</span></span>

<span data-ttu-id="3c587-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec l’argument \_ mode de matrice GL \_</span><span class="sxs-lookup"><span data-stu-id="3c587-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="3c587-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3c587-133">Requirements</span></span>



| <span data-ttu-id="3c587-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3c587-134">Requirement</span></span> | <span data-ttu-id="3c587-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="3c587-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c587-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c587-136">Minimum supported client</span></span><br/> | <span data-ttu-id="3c587-137">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3c587-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3c587-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c587-138">Minimum supported server</span></span><br/> | <span data-ttu-id="3c587-139">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3c587-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3c587-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="3c587-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c587-141"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c587-141"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="3c587-142">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3c587-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="3c587-143"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c587-143"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="3c587-144">DLL</span><span class="sxs-lookup"><span data-stu-id="3c587-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c587-145"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c587-145"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c587-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c587-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c587-147">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="3c587-147">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="3c587-148">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="3c587-148">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="3c587-149">**glLoadMatrix**</span><span class="sxs-lookup"><span data-stu-id="3c587-149">**glLoadMatrix**</span></span>](glloadmatrix.md)
</dt> <dt>

[<span data-ttu-id="3c587-150">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="3c587-150">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> </dl>

 

 





