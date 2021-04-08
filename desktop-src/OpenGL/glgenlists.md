---
title: fonction glGenLists (GL. h)
description: La fonction glGenLists génère un ensemble contigu de listes d’affichage vides.
ms.assetid: 07a97e89-1fbe-4405-b1b0-c4c47b098633
keywords:
- glGenLists fonction OpenGL
topic_type:
- apiref
api_name:
- glGenLists
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc556e789da9c768a7ed1aef6880ad48022a1ee4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740477"
---
# <a name="glgenlists-function"></a><span data-ttu-id="32a8e-104">glGenLists fonction)</span><span class="sxs-lookup"><span data-stu-id="32a8e-104">glGenLists function</span></span>

<span data-ttu-id="32a8e-105">La fonction **glGenLists** génère un ensemble contigu de listes d’affichage vides.</span><span class="sxs-lookup"><span data-stu-id="32a8e-105">The **glGenLists** function generates a contiguous set of empty display lists.</span></span>

## <a name="syntax"></a><span data-ttu-id="32a8e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="32a8e-106">Syntax</span></span>


```C++
GLuint WINAPI glGenLists(
   GLsizei range
);
```



## <a name="parameters"></a><span data-ttu-id="32a8e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="32a8e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32a8e-108">*range*</span><span class="sxs-lookup"><span data-stu-id="32a8e-108">*range*</span></span> 
</dt> <dd>

<span data-ttu-id="32a8e-109">Nombre de listes d’affichage vides contiguës à générer.</span><span class="sxs-lookup"><span data-stu-id="32a8e-109">The number of contiguous empty display lists to be generated.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="32a8e-110">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="32a8e-110">Error codes</span></span>

<span data-ttu-id="32a8e-111">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="32a8e-111">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="32a8e-112">Nom</span><span class="sxs-lookup"><span data-stu-id="32a8e-112">Name</span></span>                                                                                                  | <span data-ttu-id="32a8e-113">Signification</span><span class="sxs-lookup"><span data-stu-id="32a8e-113">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="32a8e-114"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="32a8e-114"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="32a8e-115">la *plage* était négative.</span><span class="sxs-lookup"><span data-stu-id="32a8e-115">*range* was negative.</span></span><br/>                                                                                                      |
| <dl> <span data-ttu-id="32a8e-116"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="32a8e-116"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="32a8e-117">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="32a8e-117">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="32a8e-118">Notes</span><span class="sxs-lookup"><span data-stu-id="32a8e-118">Remarks</span></span>

<span data-ttu-id="32a8e-119">La fonction **glGenLists** possède un seul argument, *Range*.</span><span class="sxs-lookup"><span data-stu-id="32a8e-119">The **glGenLists** function has one argument, *range*.</span></span> <span data-ttu-id="32a8e-120">Elle retourne un entier *n* de telle sorte que les listes d’affichage vides contiguës de la *plage* , nommées *n*, *n* + 1,.</span><span class="sxs-lookup"><span data-stu-id="32a8e-120">It returns an integer *n* such that *range* contiguous empty display lists, named *n*, *n* + 1, .</span></span> <span data-ttu-id="32a8e-121">.</span><span class="sxs-lookup"><span data-stu-id="32a8e-121">.</span></span> <span data-ttu-id="32a8e-122">., *n* + (*plage* -1) sont créés.</span><span class="sxs-lookup"><span data-stu-id="32a8e-122">., *n* + (*range* - 1), are created.</span></span> <span data-ttu-id="32a8e-123">Si la *plage* est égale à zéro, si aucun groupe de noms contigus de *plage* n’est disponible, ou si une erreur est générée, aucune liste d’affichage n’est générée et zéro est retourné.</span><span class="sxs-lookup"><span data-stu-id="32a8e-123">If *range* is zero, if there is no group of *range* contiguous names available, or if any error is generated, then no display lists are generated and zero is returned.</span></span>

<span data-ttu-id="32a8e-124">La fonction suivante récupère des informations relatives à **glGenLists**:</span><span class="sxs-lookup"><span data-stu-id="32a8e-124">The following function retrieves information related to **glGenLists**:</span></span>

[<span data-ttu-id="32a8e-125">**glIsList**</span><span class="sxs-lookup"><span data-stu-id="32a8e-125">**glIsList**</span></span>](glislist.md)

## <a name="requirements"></a><span data-ttu-id="32a8e-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="32a8e-126">Requirements</span></span>



| <span data-ttu-id="32a8e-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="32a8e-127">Requirement</span></span> | <span data-ttu-id="32a8e-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="32a8e-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="32a8e-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="32a8e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="32a8e-130">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="32a8e-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="32a8e-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="32a8e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="32a8e-132">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="32a8e-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="32a8e-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="32a8e-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="32a8e-134"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="32a8e-134"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="32a8e-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="32a8e-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="32a8e-136"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="32a8e-136"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="32a8e-137">DLL</span><span class="sxs-lookup"><span data-stu-id="32a8e-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32a8e-138"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32a8e-138"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32a8e-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="32a8e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32a8e-140">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="32a8e-140">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="32a8e-141">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="32a8e-141">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="32a8e-142">**glCallLists**</span><span class="sxs-lookup"><span data-stu-id="32a8e-142">**glCallLists**</span></span>](glcalllists.md)
</dt> <dt>

[<span data-ttu-id="32a8e-143">**glDeleteLists**</span><span class="sxs-lookup"><span data-stu-id="32a8e-143">**glDeleteLists**</span></span>](gldeletelists.md)
</dt> <dt>

[<span data-ttu-id="32a8e-144">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="32a8e-144">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="32a8e-145">**glIsList**</span><span class="sxs-lookup"><span data-stu-id="32a8e-145">**glIsList**</span></span>](glislist.md)
</dt> <dt>

[<span data-ttu-id="32a8e-146">**glNewList**</span><span class="sxs-lookup"><span data-stu-id="32a8e-146">**glNewList**</span></span>](glnewlist.md)
</dt> </dl>

 

 





