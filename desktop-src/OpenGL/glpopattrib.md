---
title: fonction glPopAttrib (GL. h)
description: Exécute un pop sur la pile d’attributs.
ms.assetid: 6a11392c-d5af-47bb-a66a-691730a58260
keywords:
- glPopAttrib fonction OpenGL
topic_type:
- apiref
api_name:
- glPopAttrib
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2258b0f16e6f61e660384931abc394300a29516
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511772"
---
# <a name="glpopattrib-function"></a><span data-ttu-id="db646-104">glPopAttrib fonction)</span><span class="sxs-lookup"><span data-stu-id="db646-104">glPopAttrib function</span></span>

<span data-ttu-id="db646-105">Exécute un pop sur la pile d’attributs.</span><span class="sxs-lookup"><span data-stu-id="db646-105">Pops the attribute stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="db646-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="db646-106">Syntax</span></span>


```C++
void WINAPI glPopAttrib(void);
```



## <a name="parameters"></a><span data-ttu-id="db646-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="db646-107">Parameters</span></span>

<span data-ttu-id="db646-108">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="db646-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="db646-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="db646-109">Return value</span></span>

<span data-ttu-id="db646-110">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="db646-110">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="db646-111">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="db646-111">Error codes</span></span>

<span data-ttu-id="db646-112">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="db646-112">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="db646-113">Nom</span><span class="sxs-lookup"><span data-stu-id="db646-113">Name</span></span>                                                                                                  | <span data-ttu-id="db646-114">Signification</span><span class="sxs-lookup"><span data-stu-id="db646-114">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="db646-115"><dt>**DÉPASSEMENT de capacité de la \_ pile GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="db646-115"><dt>**GL\_STACK\_UNDERFLOW**</dt></span></span> </dl>   | <span data-ttu-id="db646-116">La fonction a été appelée alors que la pile d’attributs était vide.</span><span class="sxs-lookup"><span data-stu-id="db646-116">The function was called while the attribute stack was empty.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="db646-117"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="db646-117"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="db646-118">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="db646-118">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="db646-119">Notes</span><span class="sxs-lookup"><span data-stu-id="db646-119">Remarks</span></span>

<span data-ttu-id="db646-120">La fonction [**glPushAttrib**](glpushattrib.md) prend un argument, un masque qui indique les groupes de variables d’État à enregistrer sur la pile d’attributs.</span><span class="sxs-lookup"><span data-stu-id="db646-120">The [**glPushAttrib**](glpushattrib.md) function takes one argument, a mask that indicates which groups of state variables to save on the attribute stack.</span></span> <span data-ttu-id="db646-121">Les constantes symboliques sont utilisées pour définir des bits dans le masque.</span><span class="sxs-lookup"><span data-stu-id="db646-121">Symbolic constants are used to set bits in the mask.</span></span> <span data-ttu-id="db646-122">Le paramètre Mask est généralement construit par **ou** à partir de plusieurs de ces constantes ensemble.</span><span class="sxs-lookup"><span data-stu-id="db646-122">The mask parameter is typically constructed by **OR** ing several of these constants together.</span></span> <span data-ttu-id="db646-123">Le fichier de masque spécial GL \_ tous les \_ \_ bits d’attrib peut être utilisé pour enregistrer tous les États empilables.</span><span class="sxs-lookup"><span data-stu-id="db646-123">The special mask GL\_ALL\_ATTRIB\_BITS can be used to save all stackable states.</span></span>

<span data-ttu-id="db646-124">La fonction **glPopAttrib** restaure les valeurs des variables d’état enregistrées avec la dernière commande [**glPushAttrib**](glpushattrib.md) .</span><span class="sxs-lookup"><span data-stu-id="db646-124">The **glPopAttrib** function restores the values of the state variables saved with the last [**glPushAttrib**](glpushattrib.md) command.</span></span> <span data-ttu-id="db646-125">Ceux qui ne sont pas enregistrés restent inchangés.</span><span class="sxs-lookup"><span data-stu-id="db646-125">Those not saved are left unchanged.</span></span>

<span data-ttu-id="db646-126">C’est une erreur de transmettre des attributs à une pile complète, ou d’afficher des attributs sur une pile vide.</span><span class="sxs-lookup"><span data-stu-id="db646-126">It is an error to push attributes onto a full stack, or to pop attributes off an empty stack.</span></span> <span data-ttu-id="db646-127">Dans les deux cas, l’indicateur d’erreur est défini et aucune autre modification n’est apportée à l’État OpenGL.</span><span class="sxs-lookup"><span data-stu-id="db646-127">In either case, the error flag is set and no other change is made to the OpenGL state.</span></span>

<span data-ttu-id="db646-128">Initialement, la pile d’attributs est vide.</span><span class="sxs-lookup"><span data-stu-id="db646-128">Initially, the attribute stack is empty.</span></span>

<span data-ttu-id="db646-129">Toutes les valeurs de l’État OpenGL ne peuvent pas être enregistrées dans la pile d’attributs.</span><span class="sxs-lookup"><span data-stu-id="db646-129">Not all values for the OpenGL state can be saved on the attribute stack.</span></span> <span data-ttu-id="db646-130">Par exemple, les États pixel Pack et unpack, l’état du mode de rendu et l’état de sélection et de commentaires ne peuvent pas être enregistrés.</span><span class="sxs-lookup"><span data-stu-id="db646-130">For example, pixel pack and unpack state, render mode state, and select and feedback state cannot be saved.</span></span>

<span data-ttu-id="db646-131">La profondeur de la pile d’attributs dépend de l’implémentation, mais elle doit être au moins égale à 16.</span><span class="sxs-lookup"><span data-stu-id="db646-131">The depth of the attribute stack depends on the implementation, but it must be at least 16.</span></span>

<span data-ttu-id="db646-132">Les fonctions suivantes récupèrent les informations relatives à [**glPushAttrib**](glpushattrib.md) et **glPopAttrib**:</span><span class="sxs-lookup"><span data-stu-id="db646-132">The following functions retrieve information related to [**glPushAttrib**](glpushattrib.md) and **glPopAttrib**:</span></span>

<span data-ttu-id="db646-133">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument la \_ profondeur de la pile GL attrib \_ \_</span><span class="sxs-lookup"><span data-stu-id="db646-133">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_ATTRIB\_STACK\_DEPTH</span></span>

<span data-ttu-id="db646-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec l’argument GL max. profondeur de la \_ \_ \_ pile \_</span><span class="sxs-lookup"><span data-stu-id="db646-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAX\_ATTRIB\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="db646-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="db646-135">Requirements</span></span>



| <span data-ttu-id="db646-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="db646-136">Requirement</span></span> | <span data-ttu-id="db646-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="db646-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="db646-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="db646-138">Minimum supported client</span></span><br/> | <span data-ttu-id="db646-139">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="db646-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="db646-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="db646-140">Minimum supported server</span></span><br/> | <span data-ttu-id="db646-141">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="db646-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="db646-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="db646-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="db646-143"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="db646-143"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="db646-144">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="db646-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="db646-145"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="db646-145"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="db646-146">DLL</span><span class="sxs-lookup"><span data-stu-id="db646-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db646-147"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db646-147"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db646-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db646-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db646-149">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="db646-149">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="db646-150">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="db646-150">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="db646-151">**glGet**</span><span class="sxs-lookup"><span data-stu-id="db646-151">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="db646-152">**glGetClipPlane**</span><span class="sxs-lookup"><span data-stu-id="db646-152">**glGetClipPlane**</span></span>](glgetclipplane.md)
</dt> <dt>

[<span data-ttu-id="db646-153">**glGetError**</span><span class="sxs-lookup"><span data-stu-id="db646-153">**glGetError**</span></span>](glgeterror.md)
</dt> <dt>

[<span data-ttu-id="db646-154">**glGetLight**</span><span class="sxs-lookup"><span data-stu-id="db646-154">**glGetLight**</span></span>](glgetlight.md)
</dt> <dt>

[<span data-ttu-id="db646-155">**glGetMap**</span><span class="sxs-lookup"><span data-stu-id="db646-155">**glGetMap**</span></span>](glgetmap.md)
</dt> <dt>

[<span data-ttu-id="db646-156">**glGetMaterial**</span><span class="sxs-lookup"><span data-stu-id="db646-156">**glGetMaterial**</span></span>](glgetmaterial.md)
</dt> <dt>

[<span data-ttu-id="db646-157">**glGetPixelMap**</span><span class="sxs-lookup"><span data-stu-id="db646-157">**glGetPixelMap**</span></span>](glgetpixelmap.md)
</dt> <dt>

[<span data-ttu-id="db646-158">**glGetPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="db646-158">**glGetPolygonStipple**</span></span>](glgetpolygonstipple.md)
</dt> <dt>

[<span data-ttu-id="db646-159">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="db646-159">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="db646-160">**glGetTexEnv**</span><span class="sxs-lookup"><span data-stu-id="db646-160">**glGetTexEnv**</span></span>](glgettexenv.md)
</dt> <dt>

[<span data-ttu-id="db646-161">**glGetTexGen**</span><span class="sxs-lookup"><span data-stu-id="db646-161">**glGetTexGen**</span></span>](glgettexgen.md)
</dt> <dt>

[<span data-ttu-id="db646-162">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="db646-162">**glGetTexImage**</span></span>](glgetteximage.md)
</dt> <dt>

[<span data-ttu-id="db646-163">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="db646-163">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md)
</dt> <dt>

[<span data-ttu-id="db646-164">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="db646-164">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="db646-165">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="db646-165">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





