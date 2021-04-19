---
title: fonction glPushName (GL. h)
description: Les fonctions glPushName et glPopName poussent et dépilent la pile de noms. | fonction glPushName (GL. h)
ms.assetid: e4319018-42c0-4567-b67f-31dbdbee9b13
keywords:
- glPushName fonction OpenGL
topic_type:
- apiref
api_name:
- glPushName
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ff783a108f5cb1ac34141c6c57f47b16e23531a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106545239"
---
# <a name="glpushname-function"></a><span data-ttu-id="81acf-105">glPushName fonction)</span><span class="sxs-lookup"><span data-stu-id="81acf-105">glPushName function</span></span>

<span data-ttu-id="81acf-106">Les fonctions **glPushName** et [**glPopName**](glpopname.md) poussent et dépilent la pile de noms.</span><span class="sxs-lookup"><span data-stu-id="81acf-106">The **glPushName** and [**glPopName**](glpopname.md) functions push and pop the name stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="81acf-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="81acf-107">Syntax</span></span>


```C++
void WINAPI glPushName(
   GLuint name
);
```



## <a name="parameters"></a><span data-ttu-id="81acf-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="81acf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81acf-109">*name*</span><span class="sxs-lookup"><span data-stu-id="81acf-109">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="81acf-110">Nom qui fera l’objet d’un push dans la pile de noms.</span><span class="sxs-lookup"><span data-stu-id="81acf-110">A name that will be pushed onto the name stack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81acf-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="81acf-111">Return value</span></span>

<span data-ttu-id="81acf-112">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="81acf-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="81acf-113">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="81acf-113">Error codes</span></span>

<span data-ttu-id="81acf-114">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="81acf-114">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="81acf-115">Nom</span><span class="sxs-lookup"><span data-stu-id="81acf-115">Name</span></span>                                                                                                  | <span data-ttu-id="81acf-116">Signification</span><span class="sxs-lookup"><span data-stu-id="81acf-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="81acf-117"><dt>**dépassement de capacité de la \_ pile GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="81acf-117"><dt>**GL\_STACK\_OVERFLOW**</dt></span></span> </dl>    | <span data-ttu-id="81acf-118">La fonction a été appelée alors que la pile de matrices actuelle était pleine.</span><span class="sxs-lookup"><span data-stu-id="81acf-118">The function was called while the current matrix stack was full.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="81acf-119"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="81acf-119"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="81acf-120">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="81acf-120">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="81acf-121">Notes</span><span class="sxs-lookup"><span data-stu-id="81acf-121">Remarks</span></span>

<span data-ttu-id="81acf-122">La fonction **glPushName** provoque un push du nom dans la pile de noms, qui est initialement vide.</span><span class="sxs-lookup"><span data-stu-id="81acf-122">The **glPushName** function causes name to be pushed onto the name stack, which is initially empty.</span></span> <span data-ttu-id="81acf-123">La fonction [**glPopName**](glpopname.md) Dépile un nom en haut de la pile.</span><span class="sxs-lookup"><span data-stu-id="81acf-123">The [**glPopName**](glpopname.md) function pops one name off the top of the stack.</span></span> <span data-ttu-id="81acf-124">La pile de noms est utilisée en mode de sélection pour permettre l’identification unique des jeux de commandes de rendu.</span><span class="sxs-lookup"><span data-stu-id="81acf-124">The name stack is used during selection mode to allow sets of rendering commands to be uniquely identified.</span></span> <span data-ttu-id="81acf-125">Il se compose d’un ensemble ordonné d’entiers non signés.</span><span class="sxs-lookup"><span data-stu-id="81acf-125">It consists of an ordered set of unsigned integers.</span></span>

<span data-ttu-id="81acf-126">La pile de noms est toujours vide lorsque le mode de rendu n’est pas la sélection de la comptabilité \_ .</span><span class="sxs-lookup"><span data-stu-id="81acf-126">The name stack is always empty while the render mode is not GL\_SELECT.</span></span> <span data-ttu-id="81acf-127">Les appels à **glPushName** ou [**glPopName**](glpopname.md) alors que le mode de rendu n’est pas GL \_ Select sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="81acf-127">Calls to **glPushName** or [**glPopName**](glpopname.md) while the render mode is not GL\_SELECT are ignored.</span></span>

<span data-ttu-id="81acf-128">Les fonctions suivantes récupèrent les informations relatives à **glPushName** et [**glPopName**](glpopname.md):</span><span class="sxs-lookup"><span data-stu-id="81acf-128">The following functions retrieve information related to **glPushName** and [**glPopName**](glpopname.md):</span></span>

<span data-ttu-id="81acf-129">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument de la profondeur de la \_ pile nom GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="81acf-129">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_NAME\_STACK\_DEPTH</span></span>

<span data-ttu-id="81acf-130">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Max \_ nom \_ \_ profondeur de la pile</span><span class="sxs-lookup"><span data-stu-id="81acf-130">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAX\_NAME\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="81acf-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="81acf-131">Requirements</span></span>



| <span data-ttu-id="81acf-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="81acf-132">Requirement</span></span> | <span data-ttu-id="81acf-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="81acf-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="81acf-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="81acf-134">Minimum supported client</span></span><br/> | <span data-ttu-id="81acf-135">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="81acf-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="81acf-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="81acf-136">Minimum supported server</span></span><br/> | <span data-ttu-id="81acf-137">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="81acf-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="81acf-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="81acf-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="81acf-139"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="81acf-139"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="81acf-140">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="81acf-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="81acf-141"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="81acf-141"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="81acf-142">DLL</span><span class="sxs-lookup"><span data-stu-id="81acf-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81acf-143"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81acf-143"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81acf-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81acf-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81acf-145">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="81acf-145">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="81acf-146">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="81acf-146">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="81acf-147">**glInitNames**</span><span class="sxs-lookup"><span data-stu-id="81acf-147">**glInitNames**</span></span>](glinitnames.md)
</dt> <dt>

[<span data-ttu-id="81acf-148">**glLoadName**</span><span class="sxs-lookup"><span data-stu-id="81acf-148">**glLoadName**</span></span>](glloadname.md)
</dt> <dt>

[<span data-ttu-id="81acf-149">**glRenderMode**</span><span class="sxs-lookup"><span data-stu-id="81acf-149">**glRenderMode**</span></span>](glrendermode.md)
</dt> <dt>

[<span data-ttu-id="81acf-150">**glSelectBuffer**</span><span class="sxs-lookup"><span data-stu-id="81acf-150">**glSelectBuffer**</span></span>](glselectbuffer.md)
</dt> </dl>

 

 





