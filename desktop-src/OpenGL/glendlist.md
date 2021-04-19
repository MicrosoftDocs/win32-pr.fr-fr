---
title: fonction glEndList (GL. h)
description: Les fonctions glNewList et glEndList créent ou remplacent une liste d’affichage. | fonction glEndList (GL. h)
ms.assetid: dd749932-7b3c-47e5-8d91-90d272a7dc41
keywords:
- glEndList fonction OpenGL
topic_type:
- apiref
api_name:
- glEndList
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59f8db8c2abea44d678268f804159b60fe695f96
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106531290"
---
# <a name="glendlist-function"></a><span data-ttu-id="6e252-105">glEndList fonction)</span><span class="sxs-lookup"><span data-stu-id="6e252-105">glEndList function</span></span>

<span data-ttu-id="6e252-106">Les fonctions [**glNewList**](glnewlist.md) et **glEndList** créent ou remplacent une liste d’affichage.</span><span class="sxs-lookup"><span data-stu-id="6e252-106">The [**glNewList**](glnewlist.md) and **glEndList** functions create or replace a display list.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e252-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6e252-107">Syntax</span></span>


```C++
void WINAPI glEndList(void);
```



## <a name="parameters"></a><span data-ttu-id="6e252-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6e252-108">Parameters</span></span>

<span data-ttu-id="6e252-109">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="6e252-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6e252-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6e252-110">Return value</span></span>

<span data-ttu-id="6e252-111">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="6e252-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6e252-112">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="6e252-112">Error codes</span></span>

<span data-ttu-id="6e252-113">Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="6e252-113">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="6e252-114">Nom</span><span class="sxs-lookup"><span data-stu-id="6e252-114">Name</span></span>                                                                                                  | <span data-ttu-id="6e252-115">Signification</span><span class="sxs-lookup"><span data-stu-id="6e252-115">Meaning</span></span>                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6e252-116"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6e252-116"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="6e252-117">**glEndList** a été appelé sans **glNewList** précédent, ou si **glNewList** a été appelé pendant la définition d’une liste d’affichage.</span><span class="sxs-lookup"><span data-stu-id="6e252-117">**glEndList** was called without a preceding **glNewList**, or if **glnewlist** was called while a display list was being defined.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="6e252-118">Notes</span><span class="sxs-lookup"><span data-stu-id="6e252-118">Remarks</span></span>

<span data-ttu-id="6e252-119">Les listes d’affichage sont des groupes de commandes OpenGL qui ont été stockées pour une exécution ultérieure.</span><span class="sxs-lookup"><span data-stu-id="6e252-119">Display lists are groups of OpenGL commands that have been stored for subsequent execution.</span></span> <span data-ttu-id="6e252-120">Les listes d’affichage sont créées avec [**glNewList**](glnewlist.md).</span><span class="sxs-lookup"><span data-stu-id="6e252-120">The display lists are created with [**glNewList**](glnewlist.md).</span></span> <span data-ttu-id="6e252-121">Toutes les commandes suivantes sont placées dans la liste d’affichage, dans l’ordre d’émission, jusqu’à ce que **glEndList** soit appelé.</span><span class="sxs-lookup"><span data-stu-id="6e252-121">All subsequent commands are placed in the display list, in the order issued, until **glEndList** is called.</span></span>

<span data-ttu-id="6e252-122">La fonction [**glNewList**](glnewlist.md) a deux paramètres.</span><span class="sxs-lookup"><span data-stu-id="6e252-122">The [**glNewList**](glnewlist.md) function has two parameters.</span></span> <span data-ttu-id="6e252-123">Le premier paramètre, *List*, est un entier positif qui devient le nom unique de la liste d’affichage.</span><span class="sxs-lookup"><span data-stu-id="6e252-123">The first parameter, *list*, is a positive integer that becomes the unique name for the display list.</span></span> <span data-ttu-id="6e252-124">Les noms peuvent être créés et réservés avec [**glGenLists**](glgenlists.md) et testés pour l’unicité avec [**glIsList**](glislist.md).</span><span class="sxs-lookup"><span data-stu-id="6e252-124">Names can be created and reserved with [**glGenLists**](glgenlists.md) and tested for uniqueness with [**glIsList**](glislist.md).</span></span> <span data-ttu-id="6e252-125">Le deuxième paramètre, *mode*, est une constante symbolique qui peut prendre l’une des deux valeurs précédentes.</span><span class="sxs-lookup"><span data-stu-id="6e252-125">The second parameter, *mode*, is a symbolic constant that can assume one of the two preceding values.</span></span>

<span data-ttu-id="6e252-126">Certaines commandes ne sont pas compilées dans la liste d’affichage, mais sont exécutées immédiatement, quel que soit le mode de liste d’affichage.</span><span class="sxs-lookup"><span data-stu-id="6e252-126">Certain commands are not compiled into the display list, but are executed immediately, regardless of the display list mode.</span></span> <span data-ttu-id="6e252-127">Ces commandes sont [**glColorPointer**](glcolorpointer.md), [**glDeleteLists**](gldeletelists.md), [**glDisableClientState**](gldisableclientstate.md), [**glEdgeFlagPointer**](gledgeflagpointer.md), [**glEnableClientState**](glenableclientstate.md), [**glFeedbackBuffer**](glfeedbackbuffer.md), [**glFinish**](glfinish.md), [**glFlush**](glflush.md), [**glGenLists**](glgenlists.md), [**glIndexPointer**](glindexpointer.md), [**glInterleavedArrays**](glinterleavedarrays.md), [**glIsEnabled**](glisenabled.md), [**glIsList**](glislist.md), [**glNormalPointer**](glnormalpointer.md), [**glPopClientAttrib**](glpopclientattrib.md), [**glPixelStore**](glpixelstore-functions.md), [**glPushClientAttrib**](glpushclientattrib.md), [**glReadPixels**](glreadpixels.md), [**glRenderMode**](glrendermode.md), [**glSelectBuffer**](glselectbuffer.md), [**glTexCoordPointer**](gltexcoordpointer.md), [**glVertexPointer**](glvertexpointer.md)et toutes les routines [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) .</span><span class="sxs-lookup"><span data-stu-id="6e252-127">These commands are [**glColorPointer**](glcolorpointer.md), [**glDeleteLists**](gldeletelists.md), [**glDisableClientState**](gldisableclientstate.md), [**glEdgeFlagPointer**](gledgeflagpointer.md), [**glEnableClientState**](glenableclientstate.md), [**glFeedbackBuffer**](glfeedbackbuffer.md), [**glFinish**](glfinish.md), [**glFlush**](glflush.md), [**glGenLists**](glgenlists.md), [**glIndexPointer**](glindexpointer.md), [**glInterleavedArrays**](glinterleavedarrays.md), [**glIsEnabled**](glisenabled.md), [**glIsList**](glislist.md), [**glNormalPointer**](glnormalpointer.md), [**glPopClientAttrib**](glpopclientattrib.md), [**glPixelStore**](glpixelstore-functions.md), [**glPushClientAttrib**](glpushclientattrib.md), [**glReadPixels**](glreadpixels.md), [**glRenderMode**](glrendermode.md), [**glSelectBuffer**](glselectbuffer.md), [**glTexCoordPointer**](gltexcoordpointer.md), [**glVertexPointer**](glvertexpointer.md), and all of the [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) routines.</span></span>

<span data-ttu-id="6e252-128">De même, [**glTexImage2D**](glteximage2d.md) et [**glTexImage1D**](glteximage1d.md) sont exécutés immédiatement et ne sont pas compilés dans la liste d’affichage lorsque leur premier argument est la texture du \_ proxy GL \_ \_ 2D ou la \_ texture du proxy GL \_ \_ 1D, respectivement.</span><span class="sxs-lookup"><span data-stu-id="6e252-128">Similarly, [**glTexImage2D**](glteximage2d.md) and [**glTexImage1D**](glteximage1d.md) are executed immediately and not compiled into the display list when their first argument is GL\_PROXY\_TEXTURE\_2D or GL\_PROXY\_TEXTURE\_1D, respectively.</span></span>

<span data-ttu-id="6e252-129">Lorsque la fonction **glEndList** est rencontrée, la définition de la liste d’affichage est effectuée en associant la liste avec la *liste* de noms uniques (spécifiée dans la commande [**glNewList**](glnewlist.md) ).</span><span class="sxs-lookup"><span data-stu-id="6e252-129">When the **glEndList** function is encountered, the display list definition is completed by associating the list with the unique name *list* (specified in the [**glNewList**](glnewlist.md) command).</span></span> <span data-ttu-id="6e252-130">Si une liste d’affichage avec la *liste* de noms existe déjà, elle est remplacée uniquement lorsque **glEndList** est appelé.</span><span class="sxs-lookup"><span data-stu-id="6e252-130">If a display list with name *list* already exists, it is replaced only when **glEndList** is called.</span></span>

<span data-ttu-id="6e252-131">Les fonctions [**glCallList**](glcalllist.md) et [**glCallLists**](glcalllists.md) peuvent être entrées dans des listes d’affichage.</span><span class="sxs-lookup"><span data-stu-id="6e252-131">The [**glCallList**](glcalllist.md) and [**glCallLists**](glcalllists.md) functions can be entered into display lists.</span></span> <span data-ttu-id="6e252-132">Les commandes de la liste d’affichage ou des listes exécutées par **glCallList** ou **glCallLists** ne sont pas incluses dans la liste d’affichage en cours de création, même si le mode de création de liste est la \_ compilation et l’exécution du GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="6e252-132">The commands in the display list or lists executed by **glCallList** or **glCallLists** are not included in the display list being created, even if the list creation mode is GL\_COMPILE\_AND\_EXECUTE.</span></span>

<span data-ttu-id="6e252-133">La fonction suivante récupère des informations relatives à [**glNewList**](glnewlist.md):</span><span class="sxs-lookup"><span data-stu-id="6e252-133">The following function retrieves information related to [**glNewList**](glnewlist.md):</span></span>

<span data-ttu-id="6e252-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec l’argument \_ mode de matrice GL \_</span><span class="sxs-lookup"><span data-stu-id="6e252-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="6e252-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6e252-135">Requirements</span></span>



| <span data-ttu-id="6e252-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6e252-136">Requirement</span></span> | <span data-ttu-id="6e252-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="6e252-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e252-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6e252-138">Minimum supported client</span></span><br/> | <span data-ttu-id="6e252-139">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6e252-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6e252-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6e252-140">Minimum supported server</span></span><br/> | <span data-ttu-id="6e252-141">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6e252-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6e252-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="6e252-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e252-143"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e252-143"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="6e252-144">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6e252-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="6e252-145"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6e252-145"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="6e252-146">DLL</span><span class="sxs-lookup"><span data-stu-id="6e252-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e252-147"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e252-147"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e252-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6e252-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e252-149">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="6e252-149">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="6e252-150">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="6e252-150">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="6e252-151">**glCallLists**</span><span class="sxs-lookup"><span data-stu-id="6e252-151">**glCallLists**</span></span>](glcalllists.md)
</dt> <dt>

[<span data-ttu-id="6e252-152">**glDeleteLists**</span><span class="sxs-lookup"><span data-stu-id="6e252-152">**glDeleteLists**</span></span>](gldeletelists.md)
</dt> <dt>

[<span data-ttu-id="6e252-153">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="6e252-153">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="6e252-154">**glGenLists**</span><span class="sxs-lookup"><span data-stu-id="6e252-154">**glGenLists**</span></span>](glgenlists.md)
</dt> <dt>

[<span data-ttu-id="6e252-155">**glIsList**</span><span class="sxs-lookup"><span data-stu-id="6e252-155">**glIsList**</span></span>](glislist.md)
</dt> <dt>

[<span data-ttu-id="6e252-156">**glNewList**</span><span class="sxs-lookup"><span data-stu-id="6e252-156">**glNewList**</span></span>](glnewlist.md)
</dt> </dl>

 

 





