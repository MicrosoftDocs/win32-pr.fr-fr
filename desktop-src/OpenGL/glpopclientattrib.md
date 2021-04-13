---
title: fonction glPopClientAttrib (GL. h)
description: Les fonctions glPushClientAttrib et glPopClientAttrib permettent d’enregistrer et de restaurer des groupes de variables d’état client sur la pile client-Attribute. | fonction glPopClientAttrib (GL. h)
ms.assetid: 030a3955-35bf-4862-9691-54b0c24514e8
keywords:
- glPopClientAttrib fonction OpenGL
topic_type:
- apiref
api_name:
- glPopClientAttrib
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e9f09e9c7292754a736594a9bf3d57a70063744
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322317"
---
# <a name="glpopclientattrib-function"></a><span data-ttu-id="b5cec-105">glPopClientAttrib fonction)</span><span class="sxs-lookup"><span data-stu-id="b5cec-105">glPopClientAttrib function</span></span>

<span data-ttu-id="b5cec-106">Les fonctions [**glPushClientAttrib**](glpushclientattrib.md) et **glPopClientAttrib** permettent d’enregistrer et de restaurer des groupes de variables d’état client sur la pile client-Attribute.</span><span class="sxs-lookup"><span data-stu-id="b5cec-106">The [**glPushClientAttrib**](glpushclientattrib.md) and **glPopClientAttrib** functions save and restore groups of client-state variables on the client-attribute stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5cec-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b5cec-107">Syntax</span></span>


```C++
void WINAPI glPopClientAttrib(void);
```



## <a name="parameters"></a><span data-ttu-id="b5cec-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b5cec-108">Parameters</span></span>

<span data-ttu-id="b5cec-109">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="b5cec-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b5cec-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b5cec-110">Return value</span></span>

<span data-ttu-id="b5cec-111">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="b5cec-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b5cec-112">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="b5cec-112">Error codes</span></span>

<span data-ttu-id="b5cec-113">Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="b5cec-113">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="b5cec-114">Nom</span><span class="sxs-lookup"><span data-stu-id="b5cec-114">Name</span></span>                                                                                               | <span data-ttu-id="b5cec-115">Signification</span><span class="sxs-lookup"><span data-stu-id="b5cec-115">Meaning</span></span>                                                                       |
|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b5cec-116"><dt>**dépassement de capacité de la \_ pile GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b5cec-116"><dt>**GL\_STACK\_OVERFLOW**</dt></span></span> </dl> | <span data-ttu-id="b5cec-117">La fonction a été appelée alors que la pile client-attribut était pleine.</span><span class="sxs-lookup"><span data-stu-id="b5cec-117">The function was called while the client-attribute stack was full.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b5cec-118">Notes</span><span class="sxs-lookup"><span data-stu-id="b5cec-118">Remarks</span></span>

<span data-ttu-id="b5cec-119">La fonction **glPushClientAttrib** utilise son paramètre mask pour déterminer les groupes de variables d’état client qui sont enregistrés sur la pile client-Attribute.</span><span class="sxs-lookup"><span data-stu-id="b5cec-119">The **glPushClientAttrib** function uses its mask parameter to determine which groups of client-state variables are saved on the client-attribute stack.</span></span> <span data-ttu-id="b5cec-120">Vous pouvez utiliser l’opérateur de bits or pour joindre des constantes symboliques acceptées afin de définir des bits et de construire un masque.</span><span class="sxs-lookup"><span data-stu-id="b5cec-120">You can use the bitwise OR operator to join together accepted symbolic constants to set bits and construct a mask.</span></span>

<span data-ttu-id="b5cec-121">La fonction **glPopClientAttrib** restaure les valeurs des variables d’état client enregistrées avec **glPushclientAttrib**.</span><span class="sxs-lookup"><span data-stu-id="b5cec-121">The **glPopClientAttrib** function restores the values of the client-state variables last saved with **glPushclientAttrib**.</span></span> <span data-ttu-id="b5cec-122">Les variables d’état client qui n’ont pas encore été enregistrées restent inchangées.</span><span class="sxs-lookup"><span data-stu-id="b5cec-122">Client-state variables not previously saved are left unchanged.</span></span> <span data-ttu-id="b5cec-123">L’envoi d’attributs vers une pile d’attribut client complète ou la déduplication d’attributs d’une pile vide définit un indicateur d’erreur et aucune autre modification n’est apportée à l’État OpenGL.</span><span class="sxs-lookup"><span data-stu-id="b5cec-123">Pushing attributes onto a full client-attribute stack or popping attributes off an empty stack sets an error flag and no other change is made to the OpenGL state.</span></span> <span data-ttu-id="b5cec-124">Par défaut, la pile des attributs du client est vide.</span><span class="sxs-lookup"><span data-stu-id="b5cec-124">By default the client attribute stack is empty.</span></span>

<span data-ttu-id="b5cec-125">Certaines valeurs d’état client OpenGL ne peuvent pas être enregistrées sur la pile client-Attribute.</span><span class="sxs-lookup"><span data-stu-id="b5cec-125">Some OpenGL client-state values cannot be saved on the client-attribute stack.</span></span> <span data-ttu-id="b5cec-126">Par exemple, vous ne pouvez pas enregistrer les États Select ou feedback sur la pile client-Attribute.</span><span class="sxs-lookup"><span data-stu-id="b5cec-126">For example, you cannot save the select or feedback states on the client-attribute stack.</span></span> <span data-ttu-id="b5cec-127">La profondeur de la pile client-attribute est d’au moins 16.</span><span class="sxs-lookup"><span data-stu-id="b5cec-127">The depth of the client-attribute stack is at least 16.</span></span>

<span data-ttu-id="b5cec-128">Les fonctions **glPushclientAttrib** et **glPopClientAttrib** ne sont pas compilées dans des listes d’affichage, mais sont exécutées immédiatement.</span><span class="sxs-lookup"><span data-stu-id="b5cec-128">The **glPushclientAttrib** and **glPopClientAttrib** functions are not compiled into display lists, but are executed immediately.</span></span>

<span data-ttu-id="b5cec-129">Les fonctions **glPushClientAttrib** et **glPopClientAttrib** peuvent uniquement envoyer et dépiler les modes de stockage de pixels et les États du client de tableau de vertex.</span><span class="sxs-lookup"><span data-stu-id="b5cec-129">The **glPushClientAttrib** and **glPopClientAttrib** functions can only push and pop pixel storage modes and vertex array client states.</span></span> <span data-ttu-id="b5cec-130">Vous devez utiliser [**glPushAttrib**](glpushattrib.md) et [**glPopAttrib**](glpopattrib.md) pour les États push et pop qui sont conservés sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="b5cec-130">You must use [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md) to push and pop states that are kept on the server.</span></span>

> [!Note]  
> <span data-ttu-id="b5cec-131">Les fonctions **glPushClientAttrib** et **glPopClientAttrib** sont uniquement disponibles dans OpenGL version 1,1 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="b5cec-131">The **glPushClientAttrib** and **glPopClientAttrib** functions are only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="b5cec-132">Les fonctions suivantes récupèrent les informations relatives à **glPushClientAttrib** et **glPopClientAttrib**:</span><span class="sxs-lookup"><span data-stu-id="b5cec-132">The following functions retrieve information related to **glPushClientAttrib** and **glPopClientAttrib**:</span></span>

<span data-ttu-id="b5cec-133">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument de la profondeur de la pile de l' \_ attribut GL client \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="b5cec-133">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CLIENT\_ATTRIB\_STACK\_DEPTH</span></span>

<span data-ttu-id="b5cec-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Max. profondeur de la pile des \_ attributs du client \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="b5cec-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAX\_CLIENT\_ATTRIB\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="b5cec-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b5cec-135">Requirements</span></span>



| <span data-ttu-id="b5cec-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b5cec-136">Requirement</span></span> | <span data-ttu-id="b5cec-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5cec-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5cec-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5cec-138">Minimum supported client</span></span><br/> | <span data-ttu-id="b5cec-139">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b5cec-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b5cec-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5cec-140">Minimum supported server</span></span><br/> | <span data-ttu-id="b5cec-141">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b5cec-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b5cec-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="b5cec-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5cec-143"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5cec-143"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="b5cec-144">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b5cec-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="b5cec-145"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5cec-145"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b5cec-146">DLL</span><span class="sxs-lookup"><span data-stu-id="b5cec-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5cec-147"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5cec-147"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5cec-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5cec-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5cec-149">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="b5cec-149">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="b5cec-150">**glDisableClientState**</span><span class="sxs-lookup"><span data-stu-id="b5cec-150">**glDisableClientState**</span></span>](gldisableclientstate.md)
</dt> <dt>

[<span data-ttu-id="b5cec-151">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="b5cec-151">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="b5cec-152">**glEnableClientState**</span><span class="sxs-lookup"><span data-stu-id="b5cec-152">**glEnableClientState**</span></span>](glenableclientstate.md)
</dt> <dt>

[<span data-ttu-id="b5cec-153">**glGet**</span><span class="sxs-lookup"><span data-stu-id="b5cec-153">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="b5cec-154">**glGetError**</span><span class="sxs-lookup"><span data-stu-id="b5cec-154">**glGetError**</span></span>](glgeterror.md)
</dt> <dt>

[<span data-ttu-id="b5cec-155">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="b5cec-155">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="b5cec-156">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="b5cec-156">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="b5cec-157">**glNewList**</span><span class="sxs-lookup"><span data-stu-id="b5cec-157">**glNewList**</span></span>](glnewlist.md)
</dt> <dt>

[<span data-ttu-id="b5cec-158">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="b5cec-158">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="b5cec-159">**glPushAttrib**</span><span class="sxs-lookup"><span data-stu-id="b5cec-159">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="b5cec-160">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="b5cec-160">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="b5cec-161">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="b5cec-161">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





