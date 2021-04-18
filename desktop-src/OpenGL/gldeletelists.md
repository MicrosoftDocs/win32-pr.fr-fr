---
title: fonction glDeleteLists (GL. h)
description: La fonction glDeleteLists supprime un groupe contigu de listes d’affichage.
ms.assetid: 979ab352-99db-4822-922c-a1813b9fcfce
keywords:
- glDeleteLists fonction OpenGL
topic_type:
- apiref
api_name:
- glDeleteLists
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c11ae41273cba5bd050a62ea330cef9da0647769
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511950"
---
# <a name="gldeletelists-function"></a><span data-ttu-id="b20ec-104">glDeleteLists fonction)</span><span class="sxs-lookup"><span data-stu-id="b20ec-104">glDeleteLists function</span></span>

<span data-ttu-id="b20ec-105">La fonction **glDeleteLists** supprime un groupe contigu de listes d’affichage.</span><span class="sxs-lookup"><span data-stu-id="b20ec-105">The **glDeleteLists** function deletes a contiguous group of display lists.</span></span>

## <a name="syntax"></a><span data-ttu-id="b20ec-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b20ec-106">Syntax</span></span>


```C++
void WINAPI glDeleteLists(
   GLuint  list,
   GLsizei range
);
```



## <a name="parameters"></a><span data-ttu-id="b20ec-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b20ec-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b20ec-108">*list*</span><span class="sxs-lookup"><span data-stu-id="b20ec-108">*list*</span></span> 
</dt> <dd>

<span data-ttu-id="b20ec-109">Nom entier de la première liste d’affichage à supprimer.</span><span class="sxs-lookup"><span data-stu-id="b20ec-109">The integer name of the first display list to delete.</span></span>

</dd> <dt>

<span data-ttu-id="b20ec-110">*range*</span><span class="sxs-lookup"><span data-stu-id="b20ec-110">*range*</span></span> 
</dt> <dd>

<span data-ttu-id="b20ec-111">Nombre de listes d’affichage à supprimer.</span><span class="sxs-lookup"><span data-stu-id="b20ec-111">The number of display lists to delete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b20ec-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b20ec-112">Return value</span></span>

<span data-ttu-id="b20ec-113">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="b20ec-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b20ec-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="b20ec-114">Error codes</span></span>

<span data-ttu-id="b20ec-115">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="b20ec-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="b20ec-116">Nom</span><span class="sxs-lookup"><span data-stu-id="b20ec-116">Name</span></span>                                                                                                  | <span data-ttu-id="b20ec-117">Signification</span><span class="sxs-lookup"><span data-stu-id="b20ec-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b20ec-118"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b20ec-118"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="b20ec-119">la *plage* était négative.</span><span class="sxs-lookup"><span data-stu-id="b20ec-119">*range* was negative.</span></span><br/>                                                                                                      |
| <dl> <span data-ttu-id="b20ec-120"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b20ec-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="b20ec-121">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="b20ec-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b20ec-122">Notes</span><span class="sxs-lookup"><span data-stu-id="b20ec-122">Remarks</span></span>

<span data-ttu-id="b20ec-123">La fonction **glDeleteLists** provoque la suppression d’un groupe contigu de listes d’affichage.</span><span class="sxs-lookup"><span data-stu-id="b20ec-123">The **glDeleteLists** function causes a contiguous group of display lists to be deleted.</span></span> <span data-ttu-id="b20ec-124">Le paramètre *List* est le nom de la première liste d’affichage à supprimer, et *Range* est le nombre de listes d’affichage à supprimer.</span><span class="sxs-lookup"><span data-stu-id="b20ec-124">The *list* parameter is the name of the first display list to be deleted, and *range* is the number of display lists to delete.</span></span> <span data-ttu-id="b20ec-125">Toutes *les listes d'* affichage *de la* plage de liste d liste  =  *d*  =    +   -1 sont supprimées.</span><span class="sxs-lookup"><span data-stu-id="b20ec-125">All display lists *d* with *list* = *d* = *list* + *range* - 1 are deleted.</span></span>

<span data-ttu-id="b20ec-126">Tous les emplacements de stockage alloués aux listes d’affichage spécifiées sont libérés, et les noms sont disponibles pour être réutilisés ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="b20ec-126">All storage locations allocated to the specified display lists are freed, and the names are available for reuse at a later time.</span></span> <span data-ttu-id="b20ec-127">Les noms dans la plage qui n’ont pas de liste d’affichage associée sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="b20ec-127">Names within the range that do not have an associated display list are ignored.</span></span> <span data-ttu-id="b20ec-128">Si la *plage* est égale à zéro, rien ne se produit.</span><span class="sxs-lookup"><span data-stu-id="b20ec-128">If *range* is zero, nothing happens.</span></span>

## <a name="requirements"></a><span data-ttu-id="b20ec-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b20ec-129">Requirements</span></span>



| <span data-ttu-id="b20ec-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b20ec-130">Requirement</span></span> | <span data-ttu-id="b20ec-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="b20ec-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b20ec-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b20ec-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b20ec-133">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b20ec-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b20ec-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b20ec-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b20ec-135">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b20ec-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b20ec-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="b20ec-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="b20ec-137"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="b20ec-137"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="b20ec-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b20ec-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="b20ec-139"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b20ec-139"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b20ec-140">DLL</span><span class="sxs-lookup"><span data-stu-id="b20ec-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b20ec-141"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b20ec-141"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b20ec-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b20ec-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b20ec-143">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="b20ec-143">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="b20ec-144">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="b20ec-144">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="b20ec-145">**glCallLists**</span><span class="sxs-lookup"><span data-stu-id="b20ec-145">**glCallLists**</span></span>](glcalllists.md)
</dt> <dt>

[<span data-ttu-id="b20ec-146">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="b20ec-146">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="b20ec-147">**glGenLists**</span><span class="sxs-lookup"><span data-stu-id="b20ec-147">**glGenLists**</span></span>](glgenlists.md)
</dt> <dt>

[<span data-ttu-id="b20ec-148">**glIsList**</span><span class="sxs-lookup"><span data-stu-id="b20ec-148">**glIsList**</span></span>](glislist.md)
</dt> <dt>

[<span data-ttu-id="b20ec-149">**glNewList**</span><span class="sxs-lookup"><span data-stu-id="b20ec-149">**glNewList**</span></span>](glnewlist.md)
</dt> </dl>

 

 





