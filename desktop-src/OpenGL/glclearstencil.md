---
title: fonction glClearStencil (GL. h)
description: La fonction glClearStencil spécifie la valeur Clear pour la mémoire tampon du stencil.
ms.assetid: bbde8fa8-78f3-45bd-bac3-5d03839acc52
keywords:
- glClearStencil fonction OpenGL
topic_type:
- apiref
api_name:
- glClearStencil
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78d831540b4c7833368bbac075835faaec359695
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942264"
---
# <a name="glclearstencil-function"></a><span data-ttu-id="14923-104">glClearStencil fonction)</span><span class="sxs-lookup"><span data-stu-id="14923-104">glClearStencil function</span></span>

<span data-ttu-id="14923-105">La fonction **glClearStencil** spécifie la valeur Clear pour la mémoire tampon du stencil.</span><span class="sxs-lookup"><span data-stu-id="14923-105">The **glClearStencil** function specifies the clear value for the stencil buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="14923-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="14923-106">Syntax</span></span>


```C++
void WINAPI glClearStencil(
   GLint s
);
```



## <a name="parameters"></a><span data-ttu-id="14923-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="14923-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14923-108">*s*</span><span class="sxs-lookup"><span data-stu-id="14923-108">*s*</span></span> 
</dt> <dd>

<span data-ttu-id="14923-109">Index utilisé lorsque la mémoire tampon du stencil est effacée.</span><span class="sxs-lookup"><span data-stu-id="14923-109">The index used when the stencil buffer is cleared.</span></span> <span data-ttu-id="14923-110">La valeur par défaut est zéro.</span><span class="sxs-lookup"><span data-stu-id="14923-110">The default value is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14923-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="14923-111">Return value</span></span>

<span data-ttu-id="14923-112">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="14923-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="14923-113">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="14923-113">Error codes</span></span>

<span data-ttu-id="14923-114">Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="14923-114">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="14923-115">Nom</span><span class="sxs-lookup"><span data-stu-id="14923-115">Name</span></span>                                                                                                  | <span data-ttu-id="14923-116">Signification</span><span class="sxs-lookup"><span data-stu-id="14923-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="14923-117"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="14923-117"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="14923-118">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="14923-118">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="14923-119">Notes</span><span class="sxs-lookup"><span data-stu-id="14923-119">Remarks</span></span>

<span data-ttu-id="14923-120">La fonction **glClearStencil** spécifie l’index utilisé par [**glClear**](glclear.md) pour effacer la mémoire tampon du stencil.</span><span class="sxs-lookup"><span data-stu-id="14923-120">The **glClearStencil** function specifies the index used by [**glClear**](glclear.md) to clear the stencil buffer.</span></span> <span data-ttu-id="14923-121">Le paramètre *s* est masqué par 2 <sup>m</sup>  -1, où *m* est le nombre de bits dans la mémoire tampon du stencil.</span><span class="sxs-lookup"><span data-stu-id="14923-121">The *s* parameter is masked with 2 <sup>m</sup>  - 1, where *m* is the number of bits in the stencil buffer.</span></span>

<span data-ttu-id="14923-122">Les fonctions suivantes récupèrent les informations relatives à la fonction **glClearStencil** :</span><span class="sxs-lookup"><span data-stu-id="14923-122">The following functions retrieve information related to the **glClearStencil** function:</span></span>

<span data-ttu-id="14923-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument \_ \_ valeur Clear du stencil du GL \_</span><span class="sxs-lookup"><span data-stu-id="14923-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_STENCIL\_CLEAR\_VALUE</span></span>

<span data-ttu-id="14923-124">**glGet** avec arguments de stencil de la comptabilité GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="14923-124">**glGet** with argument GL\_STENCIL\_BITS</span></span>

## <a name="requirements"></a><span data-ttu-id="14923-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="14923-125">Requirements</span></span>



| <span data-ttu-id="14923-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="14923-126">Requirement</span></span> | <span data-ttu-id="14923-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="14923-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="14923-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="14923-128">Minimum supported client</span></span><br/> | <span data-ttu-id="14923-129">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="14923-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="14923-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="14923-130">Minimum supported server</span></span><br/> | <span data-ttu-id="14923-131">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="14923-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="14923-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="14923-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="14923-133"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="14923-133"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="14923-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="14923-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="14923-135"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="14923-135"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="14923-136">DLL</span><span class="sxs-lookup"><span data-stu-id="14923-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14923-137"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14923-137"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14923-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="14923-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14923-139">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="14923-139">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="14923-140">**glClear**</span><span class="sxs-lookup"><span data-stu-id="14923-140">**glClear**</span></span>](glclear.md)
</dt> <dt>

[<span data-ttu-id="14923-141">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="14923-141">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="14923-142">**glGet**</span><span class="sxs-lookup"><span data-stu-id="14923-142">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

 





