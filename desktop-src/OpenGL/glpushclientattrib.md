---
title: fonction glPushClientAttrib (GL. h)
description: Les fonctions glPushClientAttrib et glPopClientAttrib permettent d’enregistrer et de restaurer des groupes de variables d’état client sur la pile client-Attribute. | fonction glPushClientAttrib (GL. h)
ms.assetid: 69f28af6-1023-4546-95ff-169525c23b07
keywords:
- glPushClientAttrib fonction OpenGL
topic_type:
- apiref
api_name:
- glPushClientAttrib
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 944e2e4229f0d36f0009ce337fd3806020322dbf
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322489"
---
# <a name="glpushclientattrib-function"></a><span data-ttu-id="22360-105">glPushClientAttrib fonction)</span><span class="sxs-lookup"><span data-stu-id="22360-105">glPushClientAttrib function</span></span>

<span data-ttu-id="22360-106">Les fonctions **glPushClientAttrib** et [**glPopClientAttrib**](glpopclientattrib.md) permettent d’enregistrer et de restaurer des groupes de variables d’état client sur la pile client-Attribute.</span><span class="sxs-lookup"><span data-stu-id="22360-106">The **glPushClientAttrib** and [**glPopClientAttrib**](glpopclientattrib.md) functions save and restore groups of client-state variables on the client-attribute stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="22360-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="22360-107">Syntax</span></span>


```C++
void WINAPI glPushClientAttrib(
   GLbitfield mask
);
```



## <a name="parameters"></a><span data-ttu-id="22360-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="22360-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22360-109">*mask*</span><span class="sxs-lookup"><span data-stu-id="22360-109">*mask*</span></span> 
</dt> <dd>

<span data-ttu-id="22360-110">Masque qui indique les attributs à enregistrer.</span><span class="sxs-lookup"><span data-stu-id="22360-110">A mask that indicates which attributes to save.</span></span> <span data-ttu-id="22360-111">Voici les constantes de masque symbolique et les États des clients OpenGL associés.</span><span class="sxs-lookup"><span data-stu-id="22360-111">The following are the symbolic mask constants and their associated OpenGL client states.</span></span>



| <span data-ttu-id="22360-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="22360-112">Value</span></span>                                                                                                                                                                                                                                            | <span data-ttu-id="22360-113">Signification</span><span class="sxs-lookup"><span data-stu-id="22360-113">Meaning</span></span>                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <span id="GL_CLIENT_PIXEL_STORE_BIT"></span><span id="gl_client_pixel_store_bit"></span><dl> <span data-ttu-id="22360-114"><dt>**\_bit de \_ magasin de pixels client \_ GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="22360-114"><dt>**GL\_CLIENT\_PIXEL\_STORE\_BIT**</dt></span></span> </dl>                                             | <span data-ttu-id="22360-115">Attributs du mode de stockage en pixels.</span><span class="sxs-lookup"><span data-stu-id="22360-115">Pixel storage mode attributes.</span></span><br/>         |
| <span id="GL_CLIENT_VERTEX_ARRAY_BIT"></span><span id="gl_client_vertex_array_bit"></span><dl> <span data-ttu-id="22360-116"><dt>**\_bit du \_ tableau de vertex client \_ du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="22360-116"><dt>**GL\_CLIENT\_VERTEX\_ARRAY\_BIT**</dt></span></span> </dl>                                          | <span data-ttu-id="22360-117">Attributs du tableau de vertex.</span><span class="sxs-lookup"><span data-stu-id="22360-117">Vertex array attributes.</span></span><br/>               |
| <span id="GL_CLIENT_ALL_ATTRIB_BITs"></span><span id="gl_client_all_attrib_bits"></span><span id="GL_CLIENT_ALL_ATTRIB_BITS"></span><dl> <span data-ttu-id="22360-118"><dt>**\_Bits de \_ tous \_ les \_ octets du client GL**</dt></span><span class="sxs-lookup"><span data-stu-id="22360-118"><dt>**GL\_CLIENT\_ALL\_ATTRIB\_BITs**</dt></span></span> </dl> | <span data-ttu-id="22360-119">tous les attributs d’état client empilables.</span><span class="sxs-lookup"><span data-stu-id="22360-119">all stackable client-state attributes.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22360-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="22360-120">Return value</span></span>

<span data-ttu-id="22360-121">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="22360-121">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="22360-122">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="22360-122">Error codes</span></span>

<span data-ttu-id="22360-123">Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="22360-123">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="22360-124">Nom</span><span class="sxs-lookup"><span data-stu-id="22360-124">Name</span></span>                                                                                               | <span data-ttu-id="22360-125">Signification</span><span class="sxs-lookup"><span data-stu-id="22360-125">Meaning</span></span>                                                                       |
|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="22360-126"><dt>**dépassement de capacité de la \_ pile GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="22360-126"><dt>**GL\_STACK\_OVERFLOW**</dt></span></span> </dl> | <span data-ttu-id="22360-127">La fonction a été appelée alors que la pile client-attribut était pleine.</span><span class="sxs-lookup"><span data-stu-id="22360-127">The function was called while the client-attribute stack was full.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="22360-128">Notes</span><span class="sxs-lookup"><span data-stu-id="22360-128">Remarks</span></span>

<span data-ttu-id="22360-129">La fonction **glPushClientAttrib** utilise son paramètre mask pour déterminer les groupes de variables d’état client qui sont enregistrés sur la pile client-Attribute.</span><span class="sxs-lookup"><span data-stu-id="22360-129">The **glPushClientAttrib** function uses its mask parameter to determine which groups of client-state variables are saved on the client-attribute stack.</span></span> <span data-ttu-id="22360-130">Vous pouvez utiliser l’opérateur de bits or pour joindre des constantes symboliques acceptées afin de définir des bits et de construire un masque.</span><span class="sxs-lookup"><span data-stu-id="22360-130">You can use the bitwise OR operator to join together accepted symbolic constants to set bits and construct a mask.</span></span>

<span data-ttu-id="22360-131">La fonction [**glPopClientAttrib**](glpopclientattrib.md) restaure les valeurs des variables d’état client enregistrées avec **glPushclientAttrib**.</span><span class="sxs-lookup"><span data-stu-id="22360-131">The [**glPopClientAttrib**](glpopclientattrib.md) function restores the values of the client-state variables last saved with **glPushclientAttrib**.</span></span> <span data-ttu-id="22360-132">Les variables d’état client qui n’ont pas encore été enregistrées restent inchangées.</span><span class="sxs-lookup"><span data-stu-id="22360-132">Client-state variables not previously saved are left unchanged.</span></span> <span data-ttu-id="22360-133">L’envoi d’attributs vers une pile d’attribut client complète ou la déduplication d’attributs d’une pile vide définit un indicateur d’erreur et aucune autre modification n’est apportée à l’État OpenGL.</span><span class="sxs-lookup"><span data-stu-id="22360-133">Pushing attributes onto a full client-attribute stack or popping attributes off an empty stack sets an error flag and no other change is made to the OpenGL state.</span></span> <span data-ttu-id="22360-134">Par défaut, la pile des attributs du client est vide.</span><span class="sxs-lookup"><span data-stu-id="22360-134">By default the client attribute stack is empty.</span></span>

<span data-ttu-id="22360-135">Certaines valeurs d’état client OpenGL ne peuvent pas être enregistrées sur la pile client-Attribute.</span><span class="sxs-lookup"><span data-stu-id="22360-135">Some OpenGL client-state values cannot be saved on the client-attribute stack.</span></span> <span data-ttu-id="22360-136">Par exemple, vous ne pouvez pas enregistrer les États Select ou feedback sur la pile client-Attribute.</span><span class="sxs-lookup"><span data-stu-id="22360-136">For example, you cannot save the select or feedback states on the client-attribute stack.</span></span> <span data-ttu-id="22360-137">La profondeur de la pile client-attribute est d’au moins 16.</span><span class="sxs-lookup"><span data-stu-id="22360-137">The depth of the client-attribute stack is at least 16.</span></span>

<span data-ttu-id="22360-138">Les fonctions **glPushclientAttrib** et **glPopClientAttrib** ne sont pas compilées dans des listes d’affichage, mais sont exécutées immédiatement.</span><span class="sxs-lookup"><span data-stu-id="22360-138">The **glPushclientAttrib** and **glPopClientAttrib** functions are not compiled into display lists, but are executed immediately.</span></span>

<span data-ttu-id="22360-139">Les fonctions **glPushClientAttrib** et **glPopClientAttrib** peuvent uniquement envoyer et dépiler les modes de stockage de pixels et les États du client de tableau de vertex.</span><span class="sxs-lookup"><span data-stu-id="22360-139">The **glPushClientAttrib** and **glPopClientAttrib** functions can only push and pop pixel storage modes and vertex array client states.</span></span> <span data-ttu-id="22360-140">Vous devez utiliser [**glPushAttrib**](glpushattrib.md) et [**glPopAttrib**](glpopattrib.md) pour les États push et pop qui sont conservés sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="22360-140">You must use [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md) to push and pop states that are kept on the server.</span></span>

> [!Note]  
> <span data-ttu-id="22360-141">Les fonctions **glPushClientAttrib** et **glPopClientAttrib** sont uniquement disponibles dans OpenGL version 1,1 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="22360-141">The **glPushClientAttrib** and **glPopClientAttrib** functions are only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="22360-142">Les fonctions suivantes récupèrent les informations relatives à **glPushClientAttrib** et **glPopClientAttrib**:</span><span class="sxs-lookup"><span data-stu-id="22360-142">The following functions retrieve information related to **glPushClientAttrib** and **glPopClientAttrib**:</span></span>

<span data-ttu-id="22360-143">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument de la profondeur de la pile de l' \_ attribut GL client \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="22360-143">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CLIENT\_ATTRIB\_STACK\_DEPTH</span></span>

<span data-ttu-id="22360-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Max. profondeur de la pile des \_ attributs du client \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="22360-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAX\_CLIENT\_ATTRIB\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="22360-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="22360-145">Requirements</span></span>



| <span data-ttu-id="22360-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="22360-146">Requirement</span></span> | <span data-ttu-id="22360-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="22360-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="22360-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="22360-148">Minimum supported client</span></span><br/> | <span data-ttu-id="22360-149">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="22360-149">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="22360-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="22360-150">Minimum supported server</span></span><br/> | <span data-ttu-id="22360-151">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="22360-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="22360-152">En-tête</span><span class="sxs-lookup"><span data-stu-id="22360-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="22360-153"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="22360-153"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="22360-154">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="22360-154">Library</span></span><br/>                  | <dl> <span data-ttu-id="22360-155"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="22360-155"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="22360-156">DLL</span><span class="sxs-lookup"><span data-stu-id="22360-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22360-157"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22360-157"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22360-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="22360-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22360-159">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="22360-159">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="22360-160">**glDisableClientState**</span><span class="sxs-lookup"><span data-stu-id="22360-160">**glDisableClientState**</span></span>](gldisableclientstate.md)
</dt> <dt>

[<span data-ttu-id="22360-161">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="22360-161">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="22360-162">**glEnableClientState**</span><span class="sxs-lookup"><span data-stu-id="22360-162">**glEnableClientState**</span></span>](glenableclientstate.md)
</dt> <dt>

[<span data-ttu-id="22360-163">**glGet**</span><span class="sxs-lookup"><span data-stu-id="22360-163">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="22360-164">**glGetError**</span><span class="sxs-lookup"><span data-stu-id="22360-164">**glGetError**</span></span>](glgeterror.md)
</dt> <dt>

[<span data-ttu-id="22360-165">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="22360-165">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="22360-166">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="22360-166">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="22360-167">**glNewList**</span><span class="sxs-lookup"><span data-stu-id="22360-167">**glNewList**</span></span>](glnewlist.md)
</dt> <dt>

[<span data-ttu-id="22360-168">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="22360-168">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="22360-169">**glPushAttrib**</span><span class="sxs-lookup"><span data-stu-id="22360-169">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="22360-170">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="22360-170">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="22360-171">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="22360-171">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





