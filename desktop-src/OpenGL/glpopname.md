---
title: fonction glPopName (GL. h)
description: Les fonctions glPushName et glPopName poussent et dépilent la pile de noms. | fonction glPopName (GL. h)
ms.assetid: ee741188-b275-4839-a89d-4d988c547d07
keywords:
- glPopName fonction OpenGL
topic_type:
- apiref
api_name:
- glPopName
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 830c4937b30cca64de3063b42ad16dd3adc87c89
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106535141"
---
# <a name="glpopname-function"></a><span data-ttu-id="279e3-105">glPopName fonction)</span><span class="sxs-lookup"><span data-stu-id="279e3-105">glPopName function</span></span>

<span data-ttu-id="279e3-106">Les fonctions [**glPushName**](glpushname.md) et **glPopName** poussent et dépilent la pile de noms.</span><span class="sxs-lookup"><span data-stu-id="279e3-106">The [**glPushName**](glpushname.md) and **glPopName** functions push and pop the name stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="279e3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="279e3-107">Syntax</span></span>


```C++
void WINAPI glPopName(void);
```



## <a name="parameters"></a><span data-ttu-id="279e3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="279e3-108">Parameters</span></span>

<span data-ttu-id="279e3-109">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="279e3-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="279e3-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="279e3-110">Return value</span></span>

<span data-ttu-id="279e3-111">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="279e3-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="279e3-112">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="279e3-112">Error codes</span></span>

<span data-ttu-id="279e3-113">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="279e3-113">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="279e3-114">Nom</span><span class="sxs-lookup"><span data-stu-id="279e3-114">Name</span></span>                                                                                                  | <span data-ttu-id="279e3-115">Signification</span><span class="sxs-lookup"><span data-stu-id="279e3-115">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="279e3-116"><dt>**DÉPASSEMENT de capacité de la \_ pile GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="279e3-116"><dt>**GL\_STACK\_UNDERFLOW**</dt></span></span> </dl>   | <span data-ttu-id="279e3-117">La fonction a été appelée alors que la pile de matrice actuelle ne contenait qu’une seule matrice.</span><span class="sxs-lookup"><span data-stu-id="279e3-117">The function was called while the current matrix stack contained only a single matrix.</span></span><br/>                                     |
| <dl> <span data-ttu-id="279e3-118"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="279e3-118"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="279e3-119">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="279e3-119">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="279e3-120">Notes</span><span class="sxs-lookup"><span data-stu-id="279e3-120">Remarks</span></span>

<span data-ttu-id="279e3-121">La fonction [**glPushName**](glpushname.md) provoque un push du nom dans la pile de noms, qui est initialement vide.</span><span class="sxs-lookup"><span data-stu-id="279e3-121">The [**glPushName**](glpushname.md) function causes name to be pushed onto the name stack, which is initially empty.</span></span> <span data-ttu-id="279e3-122">La fonction **glPopName** Dépile un nom en haut de la pile.</span><span class="sxs-lookup"><span data-stu-id="279e3-122">The **glPopName** function pops one name off the top of the stack.</span></span> <span data-ttu-id="279e3-123">La pile de noms est utilisée en mode de sélection pour permettre l’identification unique des jeux de commandes de rendu.</span><span class="sxs-lookup"><span data-stu-id="279e3-123">The name stack is used during selection mode to allow sets of rendering commands to be uniquely identified.</span></span> <span data-ttu-id="279e3-124">Il se compose d’un ensemble ordonné d’entiers non signés.</span><span class="sxs-lookup"><span data-stu-id="279e3-124">It consists of an ordered set of unsigned integers.</span></span>

<span data-ttu-id="279e3-125">La pile de noms est toujours vide lorsque le mode de rendu n’est pas la sélection de la comptabilité \_ .</span><span class="sxs-lookup"><span data-stu-id="279e3-125">The name stack is always empty while the render mode is not GL\_SELECT.</span></span> <span data-ttu-id="279e3-126">Les appels à [**glPushName**](glpushname.md) ou **glPopName** alors que le mode de rendu n’est pas GL \_ Select sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="279e3-126">Calls to [**glPushName**](glpushname.md) or **glPopName** while the render mode is not GL\_SELECT are ignored.</span></span>

<span data-ttu-id="279e3-127">Les fonctions suivantes récupèrent les informations relatives à [**glPushName**](glpushname.md) et **glPopName**:</span><span class="sxs-lookup"><span data-stu-id="279e3-127">The following functions retrieve information related to [**glPushName**](glpushname.md) and **glPopName**:</span></span>

<span data-ttu-id="279e3-128">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument de la profondeur de la \_ pile nom GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="279e3-128">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_NAME\_STACK\_DEPTH</span></span>

<span data-ttu-id="279e3-129">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Max \_ nom \_ \_ profondeur de la pile</span><span class="sxs-lookup"><span data-stu-id="279e3-129">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAX\_NAME\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="279e3-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="279e3-130">Requirements</span></span>



| <span data-ttu-id="279e3-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="279e3-131">Requirement</span></span> | <span data-ttu-id="279e3-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="279e3-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="279e3-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="279e3-133">Minimum supported client</span></span><br/> | <span data-ttu-id="279e3-134">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="279e3-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="279e3-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="279e3-135">Minimum supported server</span></span><br/> | <span data-ttu-id="279e3-136">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="279e3-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="279e3-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="279e3-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="279e3-138"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="279e3-138"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="279e3-139">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="279e3-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="279e3-140"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="279e3-140"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="279e3-141">DLL</span><span class="sxs-lookup"><span data-stu-id="279e3-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="279e3-142"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="279e3-142"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="279e3-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="279e3-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="279e3-144">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="279e3-144">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="279e3-145">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="279e3-145">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="279e3-146">**glInitNames**</span><span class="sxs-lookup"><span data-stu-id="279e3-146">**glInitNames**</span></span>](glinitnames.md)
</dt> <dt>

[<span data-ttu-id="279e3-147">**glLoadName**</span><span class="sxs-lookup"><span data-stu-id="279e3-147">**glLoadName**</span></span>](glloadname.md)
</dt> <dt>

[<span data-ttu-id="279e3-148">**glRenderMode**</span><span class="sxs-lookup"><span data-stu-id="279e3-148">**glRenderMode**</span></span>](glrendermode.md)
</dt> <dt>

[<span data-ttu-id="279e3-149">**glSelectBuffer**</span><span class="sxs-lookup"><span data-stu-id="279e3-149">**glSelectBuffer**</span></span>](glselectbuffer.md)
</dt> </dl>

 

 





