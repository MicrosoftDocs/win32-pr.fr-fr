---
title: fonction glClearAccum (GL. h)
description: La fonction glClearAccum spécifie les valeurs claires pour la mémoire tampon d’accumulation.
ms.assetid: 77d8f340-be47-43f4-96fc-31025a4c8b4e
keywords:
- glClearAccum fonction OpenGL
topic_type:
- apiref
api_name:
- glClearAccum
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3098e87a47509b8c05035171a8f31e57d8618424
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104128"
---
# <a name="glclearaccum-function"></a><span data-ttu-id="74400-104">glClearAccum fonction)</span><span class="sxs-lookup"><span data-stu-id="74400-104">glClearAccum function</span></span>

<span data-ttu-id="74400-105">La fonction **glClearAccum** spécifie les valeurs claires pour la mémoire tampon d’accumulation.</span><span class="sxs-lookup"><span data-stu-id="74400-105">The **glClearAccum** function specifies the clear values for the accumulation buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="74400-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="74400-106">Syntax</span></span>


```C++
void WINAPI glClearAccum(
   GLfloat red,
   GLfloat green,
   GLfloat blue,
   GLfloat alpha
);
```



## <a name="parameters"></a><span data-ttu-id="74400-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="74400-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74400-108">*rouge*</span><span class="sxs-lookup"><span data-stu-id="74400-108">*red*</span></span> 
</dt> <dd>

<span data-ttu-id="74400-109">Valeur rouge utilisée lorsque la mémoire tampon d’accumulation est effacée.</span><span class="sxs-lookup"><span data-stu-id="74400-109">The red value used when the accumulation buffer is cleared.</span></span> <span data-ttu-id="74400-110">La valeur par défaut est zéro.</span><span class="sxs-lookup"><span data-stu-id="74400-110">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="74400-111">*écologie*</span><span class="sxs-lookup"><span data-stu-id="74400-111">*green*</span></span> 
</dt> <dd>

<span data-ttu-id="74400-112">Valeur verte utilisée lorsque la mémoire tampon d’accumulation est effacée.</span><span class="sxs-lookup"><span data-stu-id="74400-112">The green value used when the accumulation buffer is cleared.</span></span> <span data-ttu-id="74400-113">La valeur par défaut est zéro.</span><span class="sxs-lookup"><span data-stu-id="74400-113">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="74400-114">*bleu*</span><span class="sxs-lookup"><span data-stu-id="74400-114">*blue*</span></span> 
</dt> <dd>

<span data-ttu-id="74400-115">Valeur bleue utilisée lorsque la mémoire tampon d’accumulation est effacée.</span><span class="sxs-lookup"><span data-stu-id="74400-115">The blue value used when the accumulation buffer is cleared.</span></span> <span data-ttu-id="74400-116">La valeur par défaut est zéro.</span><span class="sxs-lookup"><span data-stu-id="74400-116">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="74400-117">*alpha*</span><span class="sxs-lookup"><span data-stu-id="74400-117">*alpha*</span></span> 
</dt> <dd>

<span data-ttu-id="74400-118">Valeur alpha utilisée lorsque la mémoire tampon d’accumulation est effacée.</span><span class="sxs-lookup"><span data-stu-id="74400-118">The alpha value used when the accumulation buffer is cleared.</span></span> <span data-ttu-id="74400-119">La valeur par défaut est zéro.</span><span class="sxs-lookup"><span data-stu-id="74400-119">The default value is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74400-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="74400-120">Return value</span></span>

<span data-ttu-id="74400-121">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="74400-121">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="74400-122">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="74400-122">Error codes</span></span>

<span data-ttu-id="74400-123">Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="74400-123">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="74400-124">Nom</span><span class="sxs-lookup"><span data-stu-id="74400-124">Name</span></span>                                                                                                  | <span data-ttu-id="74400-125">Signification</span><span class="sxs-lookup"><span data-stu-id="74400-125">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="74400-126"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="74400-126"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="74400-127">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="74400-127">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="74400-128">Notes</span><span class="sxs-lookup"><span data-stu-id="74400-128">Remarks</span></span>

<span data-ttu-id="74400-129">La fonction **glClearAccum** spécifie les valeurs rouge, vert, bleu et alpha utilisées par [**glClear**](glclear.md) pour effacer la mémoire tampon d’accumulation.</span><span class="sxs-lookup"><span data-stu-id="74400-129">The **glClearAccum** function specifies the red, green, blue, and alpha values used by [**glClear**](glclear.md) to clear the accumulation buffer.</span></span>

<span data-ttu-id="74400-130">Les valeurs spécifiées par **glClearAccum** sont ancrées à la plage \[ 1, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="74400-130">Values specified by **glClearAccum** are clamped to the range \[1,1\].</span></span>

<span data-ttu-id="74400-131">La fonction suivante récupère des informations relatives à **glClearAccum**:</span><span class="sxs-lookup"><span data-stu-id="74400-131">The following function retrieves information related to **glClearAccum**:</span></span>

<span data-ttu-id="74400-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Amort \_ Clear \_ value</span><span class="sxs-lookup"><span data-stu-id="74400-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_ACCUM\_CLEAR\_VALUE</span></span>

## <a name="requirements"></a><span data-ttu-id="74400-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="74400-133">Requirements</span></span>



| <span data-ttu-id="74400-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="74400-134">Requirement</span></span> | <span data-ttu-id="74400-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="74400-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="74400-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="74400-136">Minimum supported client</span></span><br/> | <span data-ttu-id="74400-137">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="74400-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="74400-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="74400-138">Minimum supported server</span></span><br/> | <span data-ttu-id="74400-139">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="74400-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="74400-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="74400-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="74400-141"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="74400-141"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="74400-142">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="74400-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="74400-143"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="74400-143"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="74400-144">DLL</span><span class="sxs-lookup"><span data-stu-id="74400-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74400-145"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74400-145"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74400-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="74400-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74400-147">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="74400-147">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="74400-148">**glClear**</span><span class="sxs-lookup"><span data-stu-id="74400-148">**glClear**</span></span>](glclear.md)
</dt> <dt>

[<span data-ttu-id="74400-149">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="74400-149">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="74400-150">**glGet**</span><span class="sxs-lookup"><span data-stu-id="74400-150">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

 





