---
title: fonction glClearDepth (GL. h)
description: La fonction glClearDepth spécifie la valeur Clear pour la mémoire tampon de profondeur.
ms.assetid: 8e26ae78-edc1-4201-a0db-d5bc8ae6dc82
keywords:
- glClearDepth fonction OpenGL
topic_type:
- apiref
api_name:
- glClearDepth
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cf968c7ae172bf4ce354c84b2071d62304327ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317289"
---
# <a name="glcleardepth-function"></a><span data-ttu-id="93e28-104">glClearDepth fonction)</span><span class="sxs-lookup"><span data-stu-id="93e28-104">glClearDepth function</span></span>

<span data-ttu-id="93e28-105">La fonction **glClearDepth** spécifie la valeur Clear pour la mémoire tampon de profondeur.</span><span class="sxs-lookup"><span data-stu-id="93e28-105">The **glClearDepth** function specifies the clear value for the depth buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="93e28-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="93e28-106">Syntax</span></span>


```C++
void WINAPI glClearDepth(
   GLclampd depth
);
```



## <a name="parameters"></a><span data-ttu-id="93e28-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="93e28-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93e28-108">*profondeur*</span><span class="sxs-lookup"><span data-stu-id="93e28-108">*depth*</span></span> 
</dt> <dd>

<span data-ttu-id="93e28-109">Valeur de profondeur utilisée lorsque la mémoire tampon de profondeur est effacée.</span><span class="sxs-lookup"><span data-stu-id="93e28-109">The depth value used when the depth buffer is cleared.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93e28-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="93e28-110">Return value</span></span>

<span data-ttu-id="93e28-111">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="93e28-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="93e28-112">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="93e28-112">Error codes</span></span>

<span data-ttu-id="93e28-113">Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="93e28-113">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="93e28-114">Nom</span><span class="sxs-lookup"><span data-stu-id="93e28-114">Name</span></span>                                                                                                  | <span data-ttu-id="93e28-115">Signification</span><span class="sxs-lookup"><span data-stu-id="93e28-115">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="93e28-116"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="93e28-116"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="93e28-117">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="93e28-117">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="93e28-118">Notes</span><span class="sxs-lookup"><span data-stu-id="93e28-118">Remarks</span></span>

<span data-ttu-id="93e28-119">La fonction **glClearDepth** spécifie la valeur de profondeur utilisée par [**glClear**](glclear.md) pour effacer la mémoire tampon de profondeur.</span><span class="sxs-lookup"><span data-stu-id="93e28-119">The **glClearDepth** function specifies the depth value used by [**glClear**](glclear.md) to clear the depth buffer.</span></span> <span data-ttu-id="93e28-120">Les valeurs spécifiées par **glClearDepth** sont ancrées à la plage \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="93e28-120">Values specified by **glClearDepth** are clamped to the range \[0,1\].</span></span>

<span data-ttu-id="93e28-121">La fonction suivante récupère les informations relatives à la fonction **glClearDepth** :</span><span class="sxs-lookup"><span data-stu-id="93e28-121">The following function retrieves information related to the **glClearDepth** function:</span></span>

<span data-ttu-id="93e28-122">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ profondeur \_ effacer la \_ valeur</span><span class="sxs-lookup"><span data-stu-id="93e28-122">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_DEPTH\_CLEAR\_VALUE</span></span>

## <a name="requirements"></a><span data-ttu-id="93e28-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="93e28-123">Requirements</span></span>



| <span data-ttu-id="93e28-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="93e28-124">Requirement</span></span> | <span data-ttu-id="93e28-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="93e28-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="93e28-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="93e28-126">Minimum supported client</span></span><br/> | <span data-ttu-id="93e28-127">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="93e28-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="93e28-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="93e28-128">Minimum supported server</span></span><br/> | <span data-ttu-id="93e28-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="93e28-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="93e28-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="93e28-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="93e28-131"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="93e28-131"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="93e28-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="93e28-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="93e28-133"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="93e28-133"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="93e28-134">DLL</span><span class="sxs-lookup"><span data-stu-id="93e28-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93e28-135"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93e28-135"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93e28-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93e28-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93e28-137">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="93e28-137">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="93e28-138">**glClear**</span><span class="sxs-lookup"><span data-stu-id="93e28-138">**glClear**</span></span>](glclear.md)
</dt> <dt>

[<span data-ttu-id="93e28-139">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="93e28-139">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="93e28-140">**glGet**</span><span class="sxs-lookup"><span data-stu-id="93e28-140">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

 





