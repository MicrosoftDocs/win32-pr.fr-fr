---
title: fonction glCallList (GL. h)
description: La fonction glCallList exécute une liste d’affichage.
ms.assetid: 9373d32e-b11e-4a80-8713-da2c1d8d9368
keywords:
- glCallList fonction OpenGL
topic_type:
- apiref
api_name:
- glCallList
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0d356adc5d16ceb0ea10e3834d8dbb98abed2b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104131"
---
# <a name="glcalllist-function"></a><span data-ttu-id="9f754-104">glCallList fonction)</span><span class="sxs-lookup"><span data-stu-id="9f754-104">glCallList function</span></span>

<span data-ttu-id="9f754-105">La fonction **glCallList** exécute une liste d’affichage.</span><span class="sxs-lookup"><span data-stu-id="9f754-105">The **glCallList** function executes a display list.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f754-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9f754-106">Syntax</span></span>


```C++
void WINAPI glCallList(
   GLuint list
);
```



## <a name="parameters"></a><span data-ttu-id="9f754-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9f754-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f754-108">*list*</span><span class="sxs-lookup"><span data-stu-id="9f754-108">*list*</span></span> 
</dt> <dd>

<span data-ttu-id="9f754-109">Nom entier de la liste d’affichage à exécuter.</span><span class="sxs-lookup"><span data-stu-id="9f754-109">The integer name of the display list to be executed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f754-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9f754-110">Return value</span></span>

<span data-ttu-id="9f754-111">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="9f754-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f754-112">Notes</span><span class="sxs-lookup"><span data-stu-id="9f754-112">Remarks</span></span>

<span data-ttu-id="9f754-113">L’appel de la fonction **glCallList** commence l’exécution de la liste d’affichage nommée.</span><span class="sxs-lookup"><span data-stu-id="9f754-113">Invoking the **glCallList** function begins execution of the named display list.</span></span> <span data-ttu-id="9f754-114">Les fonctions enregistrées dans la liste d’affichage sont exécutées dans l’ordre, de la même façon que si vous les avez appelées sans utiliser de liste d’affichage.</span><span class="sxs-lookup"><span data-stu-id="9f754-114">The functions saved in the display list are executed in order, just as if you called them without using a display list.</span></span> <span data-ttu-id="9f754-115">Si la *liste* n’a pas été définie en tant que liste d’affichage, **glCallList** est ignoré.</span><span class="sxs-lookup"><span data-stu-id="9f754-115">If *list* has not been defined as a display list, **glCallList** is ignored.</span></span>

<span data-ttu-id="9f754-116">La fonction **glCallList** peut apparaître à l’intérieur d’une liste d’affichage.</span><span class="sxs-lookup"><span data-stu-id="9f754-116">The **glCallList** function can appear inside a display list.</span></span> <span data-ttu-id="9f754-117">Pour éviter la possibilité d’une récurrence infinie résultant de l’appel d’une liste d’affichage, une limite est placée sur le niveau d’imbrication des listes d’affichage au cours de l’exécution de la liste d’affichage.</span><span class="sxs-lookup"><span data-stu-id="9f754-117">To avoid the possibility of infinite recursion resulting from display lists calling one another, a limit is placed on the nesting level of display lists during display-list execution.</span></span> <span data-ttu-id="9f754-118">Toutefois, cette limite est d’au moins 64. elle dépend de l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="9f754-118">This limit is at least 64, however, it depends on the implementation.</span></span>

<span data-ttu-id="9f754-119">L’État OpenGL n’est pas enregistré et restauré à travers un appel à **glCallList**.</span><span class="sxs-lookup"><span data-stu-id="9f754-119">The OpenGL state is not saved and restored across a call to **glCallList**.</span></span> <span data-ttu-id="9f754-120">Ainsi, les modifications apportées à l’État OpenGL pendant l’exécution d’une liste d’affichage sont conservées après la fin de l’exécution de la liste d’affichage.</span><span class="sxs-lookup"><span data-stu-id="9f754-120">Thus, changes made to the OpenGL state during the execution of a display list remain after execution of the display list is completed.</span></span> <span data-ttu-id="9f754-121">Pour conserver l’État OpenGL sur les appels **glCallList** , utilisez [**glPushAttrib**](glpushattrib.md), [**glPopAttrib**](glpopattrib.md), [**glPushMatrix**](glpushmatrix.md)et [**glPopMatrix**](glpopmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="9f754-121">To preserve the OpenGL state across **glCallList** calls, use [**glPushAttrib**](glpushattrib.md), [**glPopAttrib**](glpopattrib.md), [**glPushMatrix**](glpushmatrix.md), and [**glPopMatrix**](glpopmatrix.md).</span></span>

<span data-ttu-id="9f754-122">Vous pouvez exécuter des listes d’affichage entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md), à condition que la liste d’affichage comprenne uniquement les fonctions autorisées dans cet intervalle.</span><span class="sxs-lookup"><span data-stu-id="9f754-122">You can execute display lists between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md), as long as the display list includes only functions that are allowed in this interval.</span></span>

<span data-ttu-id="9f754-123">Les fonctions suivantes récupèrent les informations relatives à **glCallList**:</span><span class="sxs-lookup"><span data-stu-id="9f754-123">The following functions retrieve information related to **glCallList**:</span></span>

<span data-ttu-id="9f754-124">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL \_ Max \_ List \_ imbrication</span><span class="sxs-lookup"><span data-stu-id="9f754-124">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAX\_LIST\_NESTING</span></span>

[<span data-ttu-id="9f754-125">**glIsList**</span><span class="sxs-lookup"><span data-stu-id="9f754-125">**glIsList**</span></span>](glislist.md)

## <a name="requirements"></a><span data-ttu-id="9f754-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9f754-126">Requirements</span></span>



| <span data-ttu-id="9f754-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9f754-127">Requirement</span></span> | <span data-ttu-id="9f754-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="9f754-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f754-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9f754-129">Minimum supported client</span></span><br/> | <span data-ttu-id="9f754-130">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9f754-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9f754-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9f754-131">Minimum supported server</span></span><br/> | <span data-ttu-id="9f754-132">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9f754-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9f754-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="9f754-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f754-134"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f754-134"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="9f754-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9f754-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="9f754-136"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9f754-136"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9f754-137">DLL</span><span class="sxs-lookup"><span data-stu-id="9f754-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f754-138"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f754-138"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f754-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9f754-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f754-140">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="9f754-140">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="9f754-141">**glCallLists**</span><span class="sxs-lookup"><span data-stu-id="9f754-141">**glCallLists**</span></span>](glcalllists.md)
</dt> <dt>

[<span data-ttu-id="9f754-142">**glDeleteLists**</span><span class="sxs-lookup"><span data-stu-id="9f754-142">**glDeleteLists**</span></span>](gldeletelists.md)
</dt> <dt>

[<span data-ttu-id="9f754-143">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="9f754-143">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="9f754-144">**glGenLists**</span><span class="sxs-lookup"><span data-stu-id="9f754-144">**glGenLists**</span></span>](glgenlists.md)
</dt> <dt>

[<span data-ttu-id="9f754-145">**glGet**</span><span class="sxs-lookup"><span data-stu-id="9f754-145">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="9f754-146">**glIsList**</span><span class="sxs-lookup"><span data-stu-id="9f754-146">**glIsList**</span></span>](glislist.md)
</dt> <dt>

[<span data-ttu-id="9f754-147">**glNewList**</span><span class="sxs-lookup"><span data-stu-id="9f754-147">**glNewList**</span></span>](glnewlist.md)
</dt> <dt>

[<span data-ttu-id="9f754-148">**glPopAttrib**</span><span class="sxs-lookup"><span data-stu-id="9f754-148">**glPopAttrib**</span></span>](glpopattrib.md)
</dt> <dt>

[<span data-ttu-id="9f754-149">**glPopMatrix**</span><span class="sxs-lookup"><span data-stu-id="9f754-149">**glPopMatrix**</span></span>](glpopmatrix.md)
</dt> <dt>

[<span data-ttu-id="9f754-150">**glPushAttrib**</span><span class="sxs-lookup"><span data-stu-id="9f754-150">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="9f754-151">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="9f754-151">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> </dl>

 

 





