---
title: fonction glClearColor (GL. h)
description: La fonction glClearColor spécifie des valeurs claires pour les mémoires tampons de couleur.
ms.assetid: f938e3f4-9db3-4c24-97ae-531b6799224e
keywords:
- glClearColor fonction OpenGL
topic_type:
- apiref
api_name:
- glClearColor
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34005ce34900f5fee8a4c9b2f1b963b7fe4bb6d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741940"
---
# <a name="glclearcolor-function"></a><span data-ttu-id="239e6-104">glClearColor fonction)</span><span class="sxs-lookup"><span data-stu-id="239e6-104">glClearColor function</span></span>

<span data-ttu-id="239e6-105">La fonction **glClearColor** spécifie des valeurs claires pour les mémoires tampons de couleur.</span><span class="sxs-lookup"><span data-stu-id="239e6-105">The **glClearColor** function specifies clear values for the color buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="239e6-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="239e6-106">Syntax</span></span>


```C++
void WINAPI glClearColor(
   GLclampf red,
   GLclampf green,
   GLclampf blue,
   GLclampf alpha
);
```



## <a name="parameters"></a><span data-ttu-id="239e6-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="239e6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="239e6-108">*rouge*</span><span class="sxs-lookup"><span data-stu-id="239e6-108">*red*</span></span> 
</dt> <dd>

<span data-ttu-id="239e6-109">Valeur rouge utilisée par [**glClear**](glclear.md) pour effacer les mémoires tampons de couleurs.</span><span class="sxs-lookup"><span data-stu-id="239e6-109">The red value that [**glClear**](glclear.md) uses to clear the color buffers.</span></span> <span data-ttu-id="239e6-110">La valeur par défaut est zéro.</span><span class="sxs-lookup"><span data-stu-id="239e6-110">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="239e6-111">*écologie*</span><span class="sxs-lookup"><span data-stu-id="239e6-111">*green*</span></span> 
</dt> <dd>

<span data-ttu-id="239e6-112">Valeur verte utilisée par [**glClear**](glclear.md) pour effacer les mémoires tampons de couleurs.</span><span class="sxs-lookup"><span data-stu-id="239e6-112">The green value that [**glClear**](glclear.md) uses to clear the color buffers.</span></span> <span data-ttu-id="239e6-113">La valeur par défaut est zéro.</span><span class="sxs-lookup"><span data-stu-id="239e6-113">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="239e6-114">*bleu*</span><span class="sxs-lookup"><span data-stu-id="239e6-114">*blue*</span></span> 
</dt> <dd>

<span data-ttu-id="239e6-115">Valeur bleue utilisée par [**glClear**](glclear.md) pour effacer les mémoires tampons de couleurs.</span><span class="sxs-lookup"><span data-stu-id="239e6-115">The blue value that [**glClear**](glclear.md) uses to clear the color buffers.</span></span> <span data-ttu-id="239e6-116">La valeur par défaut est zéro.</span><span class="sxs-lookup"><span data-stu-id="239e6-116">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="239e6-117">*alpha*</span><span class="sxs-lookup"><span data-stu-id="239e6-117">*alpha*</span></span> 
</dt> <dd>

<span data-ttu-id="239e6-118">Valeur alpha utilisée par [**glClear**](glclear.md) pour effacer les mémoires tampons de couleurs.</span><span class="sxs-lookup"><span data-stu-id="239e6-118">The alpha value that [**glClear**](glclear.md) uses to clear the color buffers.</span></span> <span data-ttu-id="239e6-119">La valeur par défaut est zéro.</span><span class="sxs-lookup"><span data-stu-id="239e6-119">The default value is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="239e6-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="239e6-120">Return value</span></span>

<span data-ttu-id="239e6-121">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="239e6-121">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="239e6-122">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="239e6-122">Error codes</span></span>

<span data-ttu-id="239e6-123">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="239e6-123">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="239e6-124">Nom</span><span class="sxs-lookup"><span data-stu-id="239e6-124">Name</span></span>                                                                                                  | <span data-ttu-id="239e6-125">Signification</span><span class="sxs-lookup"><span data-stu-id="239e6-125">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="239e6-126"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="239e6-126"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="239e6-127">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="239e6-127">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="239e6-128">Notes</span><span class="sxs-lookup"><span data-stu-id="239e6-128">Remarks</span></span>

<span data-ttu-id="239e6-129">La fonction **glClearColor** spécifie les valeurs rouge, vert, bleu et alpha utilisées par [**glClear**](glclear.md) pour effacer les mémoires tampons de couleur.</span><span class="sxs-lookup"><span data-stu-id="239e6-129">The **glClearColor** function specifies the red, green, blue, and alpha values used by [**glClear**](glclear.md) to clear the color buffers.</span></span> <span data-ttu-id="239e6-130">Les valeurs spécifiées par **glClearColor** sont ancrées à la plage \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="239e6-130">Values specified by **glClearColor** are clamped to the range \[0,1\].</span></span>

<span data-ttu-id="239e6-131">Les fonctions suivantes récupèrent les informations relatives à la fonction **glClearColor** :</span><span class="sxs-lookup"><span data-stu-id="239e6-131">The following functions retrieve information related to the **glClearColor** function:</span></span>

<span data-ttu-id="239e6-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Amort \_ Clear \_ value</span><span class="sxs-lookup"><span data-stu-id="239e6-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_ACCUM\_CLEAR\_VALUE</span></span>

<span data-ttu-id="239e6-133">**glGet** avec argument \_ \_ valeur Clear de couleur GL \_</span><span class="sxs-lookup"><span data-stu-id="239e6-133">**glGet** with argument GL\_COLOR\_CLEAR\_VALUE</span></span>

## <a name="requirements"></a><span data-ttu-id="239e6-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="239e6-134">Requirements</span></span>



| <span data-ttu-id="239e6-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="239e6-135">Requirement</span></span> | <span data-ttu-id="239e6-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="239e6-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="239e6-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="239e6-137">Minimum supported client</span></span><br/> | <span data-ttu-id="239e6-138">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="239e6-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="239e6-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="239e6-139">Minimum supported server</span></span><br/> | <span data-ttu-id="239e6-140">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="239e6-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="239e6-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="239e6-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="239e6-142"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="239e6-142"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="239e6-143">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="239e6-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="239e6-144"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="239e6-144"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="239e6-145">DLL</span><span class="sxs-lookup"><span data-stu-id="239e6-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="239e6-146"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="239e6-146"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="239e6-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="239e6-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="239e6-148">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="239e6-148">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="239e6-149">**glClear**</span><span class="sxs-lookup"><span data-stu-id="239e6-149">**glClear**</span></span>](glclear.md)
</dt> <dt>

[<span data-ttu-id="239e6-150">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="239e6-150">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="239e6-151">**glGet**</span><span class="sxs-lookup"><span data-stu-id="239e6-151">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

 





