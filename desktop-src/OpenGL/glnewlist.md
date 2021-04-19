---
title: fonction glNewList (GL. h)
description: Les fonctions glNewList et glEndList créent ou remplacent une liste d’affichage. | fonction glNewList (GL. h)
ms.assetid: 9c6556d4-855f-4cba-94cc-27b5f1e4607a
keywords:
- glNewList fonction OpenGL
topic_type:
- apiref
api_name:
- glNewList
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6135f67c07f69d24df67d4f1899404359efaa7aa
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106520283"
---
# <a name="glnewlist-function"></a><span data-ttu-id="20dbd-105">glNewList fonction)</span><span class="sxs-lookup"><span data-stu-id="20dbd-105">glNewList function</span></span>

<span data-ttu-id="20dbd-106">Les fonctions **glNewList** et [**glEndList**](glendlist.md) créent ou remplacent une liste d’affichage.</span><span class="sxs-lookup"><span data-stu-id="20dbd-106">The **glNewList** and [**glEndList**](glendlist.md) functions create or replace a display list.</span></span>

## <a name="syntax"></a><span data-ttu-id="20dbd-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="20dbd-107">Syntax</span></span>


```C++
void WINAPI glNewList(
   GLuint list,
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="20dbd-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="20dbd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20dbd-109">*list*</span><span class="sxs-lookup"><span data-stu-id="20dbd-109">*list*</span></span> 
</dt> <dd>

<span data-ttu-id="20dbd-110">Nom de la liste d’affichage.</span><span class="sxs-lookup"><span data-stu-id="20dbd-110">The display list name.</span></span>

</dd> <dt>

<span data-ttu-id="20dbd-111">*mode*</span><span class="sxs-lookup"><span data-stu-id="20dbd-111">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="20dbd-112">Mode de compilation.</span><span class="sxs-lookup"><span data-stu-id="20dbd-112">The compilation mode.</span></span> <span data-ttu-id="20dbd-113">Les valeurs suivantes sont acceptées.</span><span class="sxs-lookup"><span data-stu-id="20dbd-113">The following values are accepted.</span></span>



| <span data-ttu-id="20dbd-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="20dbd-114">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="20dbd-115">Signification</span><span class="sxs-lookup"><span data-stu-id="20dbd-115">Meaning</span></span>                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="GL_COMPILE"></span><span id="gl_compile"></span><dl> <span data-ttu-id="20dbd-116"><dt>**compilation du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="20dbd-116"><dt>**GL\_COMPILE**</dt></span></span> </dl>                                       | <span data-ttu-id="20dbd-117">Les commandes sont simplement compilées.</span><span class="sxs-lookup"><span data-stu-id="20dbd-117">Commands are merely compiled.</span></span><br/>                                     |
| <span id="GL_COMPILE_AND_EXECUTE"></span><span id="gl_compile_and_execute"></span><dl> <span data-ttu-id="20dbd-118"><dt>**\_compilation \_ et \_ exécution du GL**</dt></span><span class="sxs-lookup"><span data-stu-id="20dbd-118"><dt>**GL\_COMPILE\_AND\_EXECUTE**</dt></span></span> </dl> | <span data-ttu-id="20dbd-119">Les commandes sont exécutées lorsqu’elles sont compilées dans la liste d’affichage.</span><span class="sxs-lookup"><span data-stu-id="20dbd-119">Commands are executed as they are compiled into the display list.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20dbd-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="20dbd-120">Return value</span></span>

<span data-ttu-id="20dbd-121">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="20dbd-121">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="20dbd-122">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="20dbd-122">Error codes</span></span>

<span data-ttu-id="20dbd-123">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="20dbd-123">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="20dbd-124">Nom</span><span class="sxs-lookup"><span data-stu-id="20dbd-124">Name</span></span>                                                                                                  | <span data-ttu-id="20dbd-125">Signification</span><span class="sxs-lookup"><span data-stu-id="20dbd-125">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="20dbd-126"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="20dbd-126"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="20dbd-127">la *liste* était égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="20dbd-127">*list* was zero.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="20dbd-128"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="20dbd-128"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="20dbd-129">le *mode* n’était pas une valeur acceptée.</span><span class="sxs-lookup"><span data-stu-id="20dbd-129">*mode* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="20dbd-130"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="20dbd-130"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="20dbd-131">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="20dbd-131">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="20dbd-132">Notes</span><span class="sxs-lookup"><span data-stu-id="20dbd-132">Remarks</span></span>

<span data-ttu-id="20dbd-133">Les listes d’affichage sont des groupes de commandes OpenGL qui ont été stockées pour une exécution ultérieure.</span><span class="sxs-lookup"><span data-stu-id="20dbd-133">Display lists are groups of OpenGL commands that have been stored for subsequent execution.</span></span> <span data-ttu-id="20dbd-134">Les listes d’affichage sont créées avec **glNewList**.</span><span class="sxs-lookup"><span data-stu-id="20dbd-134">The display lists are created with **glNewList**.</span></span> <span data-ttu-id="20dbd-135">Toutes les commandes suivantes sont placées dans la liste d’affichage, dans l’ordre d’émission, jusqu’à ce que **glEndList** soit appelé.</span><span class="sxs-lookup"><span data-stu-id="20dbd-135">All subsequent commands are placed in the display list, in the order issued, until **glEndList** is called.</span></span>

<span data-ttu-id="20dbd-136">La fonction **glNewList** a deux paramètres.</span><span class="sxs-lookup"><span data-stu-id="20dbd-136">The **glNewList** function has two parameters.</span></span> <span data-ttu-id="20dbd-137">Le premier paramètre, *List*, est un entier positif qui devient le nom unique de la liste d’affichage.</span><span class="sxs-lookup"><span data-stu-id="20dbd-137">The first parameter, *list*, is a positive integer that becomes the unique name for the display list.</span></span> <span data-ttu-id="20dbd-138">Les noms peuvent être créés et réservés avec [**glGenLists**](glgenlists.md) et testés pour l’unicité avec [**glIsList**](glislist.md).</span><span class="sxs-lookup"><span data-stu-id="20dbd-138">Names can be created and reserved with [**glGenLists**](glgenlists.md) and tested for uniqueness with [**glIsList**](glislist.md).</span></span> <span data-ttu-id="20dbd-139">Le deuxième paramètre, *mode*, est une constante symbolique qui peut prendre l’une des deux valeurs précédentes.</span><span class="sxs-lookup"><span data-stu-id="20dbd-139">The second parameter, *mode*, is a symbolic constant that can assume one of the two preceding values.</span></span>

<span data-ttu-id="20dbd-140">Certaines commandes ne sont pas compilées dans la liste d’affichage, mais sont exécutées immédiatement, quel que soit le mode de liste d’affichage.</span><span class="sxs-lookup"><span data-stu-id="20dbd-140">Certain commands are not compiled into the display list, but are executed immediately, regardless of the display list mode.</span></span> <span data-ttu-id="20dbd-141">Ces commandes sont [**glColorPointer**](glcolorpointer.md), [**glDeleteLists**](gldeletelists.md), [**glDisableClientState**](gldisableclientstate.md), [**glEdgeFlagPointer**](gledgeflagpointer.md), [**glEnableClientState**](glenableclientstate.md), [**glFeedbackBuffer**](glfeedbackbuffer.md), [**glFinish**](glfinish.md), [**glFlush**](glflush.md), [**glGenLists**](glgenlists.md), [**glIndexPointer**](glindexpointer.md), [**glInterleavedArrays**](glinterleavedarrays.md), [**glIsEnabled**](glisenabled.md), [**glIsList**](glislist.md), [**glNormalPointer**](glnormalpointer.md), [**glPopClientAttrib**](glpopclientattrib.md), [**glPixelStore**](glpixelstore-functions.md), [**glPushClientAttrib**](glpushclientattrib.md), [**glReadPixels**](glreadpixels.md), [**glRenderMode**](glrendermode.md), [**glSelectBuffer**](glselectbuffer.md), [**glTexCoordPointer**](gltexcoordpointer.md), [**glVertexPointer**](glvertexpointer.md)et toutes les routines [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) .</span><span class="sxs-lookup"><span data-stu-id="20dbd-141">These commands are [**glColorPointer**](glcolorpointer.md), [**glDeleteLists**](gldeletelists.md), [**glDisableClientState**](gldisableclientstate.md), [**glEdgeFlagPointer**](gledgeflagpointer.md), [**glEnableClientState**](glenableclientstate.md), [**glFeedbackBuffer**](glfeedbackbuffer.md), [**glFinish**](glfinish.md), [**glFlush**](glflush.md), [**glGenLists**](glgenlists.md), [**glIndexPointer**](glindexpointer.md), [**glInterleavedArrays**](glinterleavedarrays.md), [**glIsEnabled**](glisenabled.md), [**glIsList**](glislist.md), [**glNormalPointer**](glnormalpointer.md), [**glPopClientAttrib**](glpopclientattrib.md), [**glPixelStore**](glpixelstore-functions.md), [**glPushClientAttrib**](glpushclientattrib.md), [**glReadPixels**](glreadpixels.md), [**glRenderMode**](glrendermode.md), [**glSelectBuffer**](glselectbuffer.md), [**glTexCoordPointer**](gltexcoordpointer.md), [**glVertexPointer**](glvertexpointer.md), and all of the [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) routines.</span></span>

<span data-ttu-id="20dbd-142">De même, [**glTexImage2D**](glteximage2d.md) et [**glTexImage1D**](glteximage1d.md) sont exécutés immédiatement et ne sont pas compilés dans la liste d’affichage lorsque leur premier argument est la texture du \_ proxy GL \_ \_ 2D ou la \_ texture du proxy GL \_ \_ 1D, respectivement.</span><span class="sxs-lookup"><span data-stu-id="20dbd-142">Similarly, [**glTexImage2D**](glteximage2d.md) and [**glTexImage1D**](glteximage1d.md) are executed immediately and not compiled into the display list when their first argument is GL\_PROXY\_TEXTURE\_2D or GL\_PROXY\_TEXTURE\_1D, respectively.</span></span>

<span data-ttu-id="20dbd-143">Lorsque la fonction **glEndList** est rencontrée, la définition de la liste d’affichage est effectuée en associant la liste avec la *liste* de noms uniques (spécifiée dans la commande **glNewList** ).</span><span class="sxs-lookup"><span data-stu-id="20dbd-143">When the **glEndList** function is encountered, the display list definition is completed by associating the list with the unique name *list* (specified in the **glNewList** command).</span></span> <span data-ttu-id="20dbd-144">Si une liste d’affichage avec la *liste* de noms existe déjà, elle est remplacée uniquement lorsque **glEndList** est appelé.</span><span class="sxs-lookup"><span data-stu-id="20dbd-144">If a display list with name *list* already exists, it is replaced only when **glEndList** is called.</span></span>

<span data-ttu-id="20dbd-145">Les fonctions [**glCallList**](glcalllist.md) et [**glCallLists**](glcalllists.md) peuvent être entrées dans des listes d’affichage.</span><span class="sxs-lookup"><span data-stu-id="20dbd-145">The [**glCallList**](glcalllist.md) and [**glCallLists**](glcalllists.md) functions can be entered into display lists.</span></span> <span data-ttu-id="20dbd-146">Les commandes de la liste d’affichage ou des listes exécutées par **glCallList** ou **glCallLists** ne sont pas incluses dans la liste d’affichage en cours de création, même si le mode de création de liste est la \_ compilation et l’exécution du GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="20dbd-146">The commands in the display list or lists executed by **glCallList** or **glCallLists** are not included in the display list being created, even if the list creation mode is GL\_COMPILE\_AND\_EXECUTE.</span></span>

<span data-ttu-id="20dbd-147">La fonction suivante récupère des informations relatives à **glNewList**:</span><span class="sxs-lookup"><span data-stu-id="20dbd-147">The following function retrieves information related to **glNewList**:</span></span>

<span data-ttu-id="20dbd-148">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec l’argument \_ mode de matrice GL \_</span><span class="sxs-lookup"><span data-stu-id="20dbd-148">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="20dbd-149">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="20dbd-149">Requirements</span></span>



| <span data-ttu-id="20dbd-150">Condition requise</span><span class="sxs-lookup"><span data-stu-id="20dbd-150">Requirement</span></span> | <span data-ttu-id="20dbd-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="20dbd-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="20dbd-152">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="20dbd-152">Minimum supported client</span></span><br/> | <span data-ttu-id="20dbd-153">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="20dbd-153">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="20dbd-154">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="20dbd-154">Minimum supported server</span></span><br/> | <span data-ttu-id="20dbd-155">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="20dbd-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="20dbd-156">En-tête</span><span class="sxs-lookup"><span data-stu-id="20dbd-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="20dbd-157"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="20dbd-157"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="20dbd-158">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="20dbd-158">Library</span></span><br/>                  | <dl> <span data-ttu-id="20dbd-159"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="20dbd-159"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="20dbd-160">DLL</span><span class="sxs-lookup"><span data-stu-id="20dbd-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20dbd-161"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20dbd-161"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20dbd-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20dbd-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20dbd-163">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="20dbd-163">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="20dbd-164">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="20dbd-164">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="20dbd-165">**glCallLists**</span><span class="sxs-lookup"><span data-stu-id="20dbd-165">**glCallLists**</span></span>](glcalllists.md)
</dt> <dt>

[<span data-ttu-id="20dbd-166">**glDeleteLists**</span><span class="sxs-lookup"><span data-stu-id="20dbd-166">**glDeleteLists**</span></span>](gldeletelists.md)
</dt> <dt>

[<span data-ttu-id="20dbd-167">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="20dbd-167">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="20dbd-168">**glEndList**</span><span class="sxs-lookup"><span data-stu-id="20dbd-168">**glEndList**</span></span>](glendlist.md)
</dt> <dt>

[<span data-ttu-id="20dbd-169">**glGenLists**</span><span class="sxs-lookup"><span data-stu-id="20dbd-169">**glGenLists**</span></span>](glgenlists.md)
</dt> <dt>

[<span data-ttu-id="20dbd-170">**glIsList**</span><span class="sxs-lookup"><span data-stu-id="20dbd-170">**glIsList**</span></span>](glislist.md)
</dt> </dl>

 

 





