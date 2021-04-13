---
title: fonction glClearIndex (GL. h)
description: La fonction glClearIndex spécifie la valeur Clear pour les mémoires tampons d’index de couleurs.
ms.assetid: 87983d93-c5a1-445f-8621-1c2952d93a0f
keywords:
- glClearIndex fonction OpenGL
topic_type:
- apiref
api_name:
- glClearIndex
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85b1ed90b017828e13d387e1e6db440c1d781cb5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465658"
---
# <a name="glclearindex-function"></a><span data-ttu-id="9c926-104">glClearIndex fonction)</span><span class="sxs-lookup"><span data-stu-id="9c926-104">glClearIndex function</span></span>

<span data-ttu-id="9c926-105">La fonction **glClearIndex** spécifie la valeur Clear pour les mémoires tampons d’index de couleurs.</span><span class="sxs-lookup"><span data-stu-id="9c926-105">The **glClearIndex** function specifies the clear value for the color-index buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c926-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9c926-106">Syntax</span></span>


```C++
void WINAPI glClearIndex(
   GLfloat c
);
```



## <a name="parameters"></a><span data-ttu-id="9c926-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9c926-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c926-108">*c*</span><span class="sxs-lookup"><span data-stu-id="9c926-108">*c*</span></span> 
</dt> <dd>

<span data-ttu-id="9c926-109">Index utilisé lorsque les mémoires tampons d’index de couleurs sont effacées.</span><span class="sxs-lookup"><span data-stu-id="9c926-109">The index used when the color-index buffers are cleared.</span></span> <span data-ttu-id="9c926-110">La valeur par défaut est zéro.</span><span class="sxs-lookup"><span data-stu-id="9c926-110">The default value is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c926-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9c926-111">Return value</span></span>

<span data-ttu-id="9c926-112">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="9c926-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9c926-113">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="9c926-113">Error codes</span></span>

<span data-ttu-id="9c926-114">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="9c926-114">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="9c926-115">Nom</span><span class="sxs-lookup"><span data-stu-id="9c926-115">Name</span></span>                                                                                                  | <span data-ttu-id="9c926-116">Signification</span><span class="sxs-lookup"><span data-stu-id="9c926-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9c926-117"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9c926-117"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="9c926-118">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="9c926-118">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="9c926-119">Notes</span><span class="sxs-lookup"><span data-stu-id="9c926-119">Remarks</span></span>

<span data-ttu-id="9c926-120">La fonction **glClearIndex** spécifie l’index utilisé par [**glClear**](glclear.md) pour effacer les mémoires tampons d’index de couleurs.</span><span class="sxs-lookup"><span data-stu-id="9c926-120">The **glClearIndex** function specifies the index used by [**glClear**](glclear.md) to clear the color-index buffers.</span></span> <span data-ttu-id="9c926-121">Le paramètre *c* n’est pas ancré.</span><span class="sxs-lookup"><span data-stu-id="9c926-121">The *c* parameter is not clamped.</span></span> <span data-ttu-id="9c926-122">Au lieu de cela, *c* est converti en une valeur à virgule fixe avec une précision non spécifiée à droite du point binaire.</span><span class="sxs-lookup"><span data-stu-id="9c926-122">Rather, *c* is converted to a fixed-point value with unspecified precision to the right of the binary point.</span></span> <span data-ttu-id="9c926-123">La partie entière de cette valeur est ensuite masquée par 2 <sup>m</sup>  -1, où *m* est le nombre de bits dans un index de couleur stocké dans le trame.</span><span class="sxs-lookup"><span data-stu-id="9c926-123">The integer part of this value is then masked with 2 <sup>m</sup>  - 1, where *m* is the number of bits in a color index stored in the framebuffer.</span></span>

<span data-ttu-id="9c926-124">Les fonctions suivantes récupèrent les informations relatives à **glClearIndex**:</span><span class="sxs-lookup"><span data-stu-id="9c926-124">The following functions retrieve information related to **glClearIndex**:</span></span>

<span data-ttu-id="9c926-125">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument \_ \_ valeur Clear de l’index GL \_</span><span class="sxs-lookup"><span data-stu-id="9c926-125">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_INDEX\_CLEAR\_VALUE</span></span>

<span data-ttu-id="9c926-126">**glGet** avec arguments GL \_ index \_ bits</span><span class="sxs-lookup"><span data-stu-id="9c926-126">**glGet** with argument GL\_INDEX\_BITS</span></span>

## <a name="requirements"></a><span data-ttu-id="9c926-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9c926-127">Requirements</span></span>



| <span data-ttu-id="9c926-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9c926-128">Requirement</span></span> | <span data-ttu-id="9c926-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="9c926-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c926-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9c926-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9c926-131">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9c926-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9c926-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9c926-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9c926-133">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9c926-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9c926-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="9c926-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c926-135"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c926-135"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="9c926-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9c926-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="9c926-137"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9c926-137"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9c926-138">DLL</span><span class="sxs-lookup"><span data-stu-id="9c926-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c926-139"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c926-139"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c926-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9c926-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c926-141">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="9c926-141">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="9c926-142">**glClear**</span><span class="sxs-lookup"><span data-stu-id="9c926-142">**glClear**</span></span>](glclear.md)
</dt> <dt>

[<span data-ttu-id="9c926-143">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="9c926-143">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="9c926-144">**glGet**</span><span class="sxs-lookup"><span data-stu-id="9c926-144">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

 





