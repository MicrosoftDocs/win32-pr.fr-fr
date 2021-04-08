---
title: fonction glSelectBuffer (GL. h)
description: La fonction glSelectBuffer établit une mémoire tampon pour les valeurs du mode de sélection.
ms.assetid: b5c64364-1f47-4281-96b5-95c3f5c8e753
keywords:
- glSelectBuffer fonction OpenGL
topic_type:
- apiref
api_name:
- glSelectBuffer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efa5b97abad6575de77a760c72e3eb05e90461c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740037"
---
# <a name="glselectbuffer-function"></a><span data-ttu-id="cb2bb-104">glSelectBuffer fonction)</span><span class="sxs-lookup"><span data-stu-id="cb2bb-104">glSelectBuffer function</span></span>

<span data-ttu-id="cb2bb-105">La fonction **glSelectBuffer** établit une mémoire tampon pour les valeurs du mode de sélection.</span><span class="sxs-lookup"><span data-stu-id="cb2bb-105">The **glSelectBuffer** function establishes a buffer for selection mode values.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb2bb-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cb2bb-106">Syntax</span></span>


```C++
void WINAPI glSelectBuffer(
   GLsizei size,
   GLuint  *buffer
);
```



## <a name="parameters"></a><span data-ttu-id="cb2bb-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cb2bb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb2bb-108">*size*</span><span class="sxs-lookup"><span data-stu-id="cb2bb-108">*size*</span></span> 
</dt> <dd>

<span data-ttu-id="cb2bb-109">Taille de la *mémoire tampon*.</span><span class="sxs-lookup"><span data-stu-id="cb2bb-109">The size of *buffer*.</span></span>

</dd> <dt>

<span data-ttu-id="cb2bb-110">*mémoire tampon*</span><span class="sxs-lookup"><span data-stu-id="cb2bb-110">*buffer*</span></span> 
</dt> <dd>

<span data-ttu-id="cb2bb-111">Retourne les données de sélection.</span><span class="sxs-lookup"><span data-stu-id="cb2bb-111">Returns the selection data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb2bb-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="cb2bb-112">Return value</span></span>

<span data-ttu-id="cb2bb-113">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="cb2bb-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="cb2bb-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="cb2bb-114">Error codes</span></span>

<span data-ttu-id="cb2bb-115">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="cb2bb-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="cb2bb-116">Nom</span><span class="sxs-lookup"><span data-stu-id="cb2bb-116">Name</span></span>                                                                                                  | <span data-ttu-id="cb2bb-117">Signification</span><span class="sxs-lookup"><span data-stu-id="cb2bb-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cb2bb-118"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cb2bb-118"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="cb2bb-119">la *taille* était négative.</span><span class="sxs-lookup"><span data-stu-id="cb2bb-119">*size* was negative.</span></span><br/>                                                                                                       |
| <dl> <span data-ttu-id="cb2bb-120"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cb2bb-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="cb2bb-121">La fonction a été appelée alors que le mode de rendu était « GL \_ Select ».</span><span class="sxs-lookup"><span data-stu-id="cb2bb-121">The function was called while the render mode was GL\_SELECT.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="cb2bb-122"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cb2bb-122"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="cb2bb-123">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="cb2bb-123">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="cb2bb-124">Notes</span><span class="sxs-lookup"><span data-stu-id="cb2bb-124">Remarks</span></span>

<span data-ttu-id="cb2bb-125">La fonction **glSelectBuffer** a deux paramètres : la *mémoire tampon* est un pointeur vers un tableau d’entiers non signés et la *taille* indique la taille du tableau.</span><span class="sxs-lookup"><span data-stu-id="cb2bb-125">The **glSelectBuffer** function has two parameters: *buffer* is a pointer to an array of unsigned integers, and *size* indicates the size of the array.</span></span> <span data-ttu-id="cb2bb-126">Le paramètre *buffer* retourne des valeurs à partir de la pile de noms (consultez [**glInitNames**](glinitnames.md), [**glLoadName**](glloadname.md), [**glPushName**](glpushname.md)) lorsque le mode de rendu est GL \_ Select (voir [**glRenderMode**](glrendermode.md)).</span><span class="sxs-lookup"><span data-stu-id="cb2bb-126">The *buffer* parameter returns values from the name stack (see [**glInitNames**](glinitnames.md), [**glLoadName**](glloadname.md), [**glPushName**](glpushname.md)) when the rendering mode is GL\_SELECT (see [**glRenderMode**](glrendermode.md)).</span></span> <span data-ttu-id="cb2bb-127">La fonction **glSelectBuffer** doit être émise avant l’activation du mode de sélection, et elle ne doit pas être émise tant que le mode de rendu est GL \_ Select.</span><span class="sxs-lookup"><span data-stu-id="cb2bb-127">The **glSelectBuffer** function must be issued before selection mode is enabled, and it must not be issued while the rendering mode is GL\_SELECT.</span></span>

<span data-ttu-id="cb2bb-128">La sélection est utilisée par un programmeur pour déterminer quelles primitives sont dessinées dans une région d’une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="cb2bb-128">Selection is used by a programmer to determine which primitives are drawn into some region of a window.</span></span> <span data-ttu-id="cb2bb-129">La région est définie par les matrices de modelview et de perspective actuelles.</span><span class="sxs-lookup"><span data-stu-id="cb2bb-129">The region is defined by the current modelview and perspective matrices.</span></span>

<span data-ttu-id="cb2bb-130">En mode de sélection, aucun fragment de pixel n’est produit à partir de la pixellisation.</span><span class="sxs-lookup"><span data-stu-id="cb2bb-130">In selection mode, no pixel fragments are produced from rasterization.</span></span> <span data-ttu-id="cb2bb-131">Au lieu de cela, si une primitive croise le volume de clip défini par l’frustum de visualisation et les plans de découpage définis par l’utilisateur, cette primitive provoque un accès à la sélection.</span><span class="sxs-lookup"><span data-stu-id="cb2bb-131">Instead, if a primitive intersects the clip volume defined by the viewing frustum and the user-defined clipping planes, this primitive causes a selection hit.</span></span> <span data-ttu-id="cb2bb-132">(Avec les polygones, aucun accès n’a lieu si le polygone est éliminé.) Lorsqu’une modification est apportée à la pile de noms, ou lorsque [**glRenderMode**](glrendermode.md) est appelé, un enregistrement d’accès est copié dans *buffer* si des accès ont eu lieu depuis le dernier événement de ce type (modification de la pile de noms ou appel **glRenderMode** ).</span><span class="sxs-lookup"><span data-stu-id="cb2bb-132">(With polygons, no hit occurs if the polygon is culled.) When a change is made to the name stack, or when [**glRenderMode**](glrendermode.md) is called, a hit record is copied to *buffer* if any hits have occurred since the last such event (either a name stack change or a **glRenderMode** call).</span></span> <span data-ttu-id="cb2bb-133">L’enregistrement d’accès se compose du nombre de noms dans la pile de noms au moment de l’événement ; suivi des valeurs de profondeur minimale et maximale de tous les vertex ayant atteint depuis l’événement précédent ; suivi du nom du contenu de la pile, en commençant par le nom inférieur.</span><span class="sxs-lookup"><span data-stu-id="cb2bb-133">The hit record consists of the number of names in the name stack at the time of the event; followed by the minimum and maximum depth values of all vertices that hit since the previous event; followed by the name stack contents, bottom name first.</span></span>

<span data-ttu-id="cb2bb-134">Les valeurs de profondeur retournées sont mappées de telle sorte que la plus grande valeur entière non signée correspond à la profondeur de la coordonnée 1,0 et zéro correspond à la profondeur de la coordonnée de la fenêtre 0,0.</span><span class="sxs-lookup"><span data-stu-id="cb2bb-134">Returned depth values are mapped such that the largest unsigned integer value corresponds to window coordinate depth 1.0, and zero corresponds to window coordinate depth 0.0.</span></span>

<span data-ttu-id="cb2bb-135">Un index interne dans la *mémoire tampon* est réinitialisé à zéro chaque fois que le mode de sélection est entré.</span><span class="sxs-lookup"><span data-stu-id="cb2bb-135">An internal index into *buffer* is reset to zero whenever selection mode is entered.</span></span> <span data-ttu-id="cb2bb-136">Chaque fois qu’un enregistrement atteint est copié dans la *mémoire tampon*, l’index est incrémenté pour pointer vers la cellule située juste après la fin du bloc de namesthat, vers la cellule suivante disponible.</span><span class="sxs-lookup"><span data-stu-id="cb2bb-136">Each time a hit record is copied into *buffer*, the index is incremented to point to the cell just past the end of the block of namesthat is, to the next available cell.</span></span> <span data-ttu-id="cb2bb-137">Si l’enregistrement d’accès est plus grand que le nombre d’emplacements restants dans la *mémoire tampon*, autant de données que possible est copié, et l’indicateur de dépassement de capacité est défini.</span><span class="sxs-lookup"><span data-stu-id="cb2bb-137">If the hit record is larger than the number of remaining locations in *buffer*, as much data as can fit is copied, and the overflow flag is set.</span></span> <span data-ttu-id="cb2bb-138">Si la pile de noms est vide lorsqu’un enregistrement d’accès est copié, cet enregistrement se compose de zéro suivi des valeurs de profondeur minimale et maximale.</span><span class="sxs-lookup"><span data-stu-id="cb2bb-138">If the name stack is empty when a hit record is copied, that record consists of zero followed by the minimum and maximum depth values.</span></span>

<span data-ttu-id="cb2bb-139">Le mode de sélection est fermé en appelant **glRenderMode** avec un argument autre que GL \_ Select.</span><span class="sxs-lookup"><span data-stu-id="cb2bb-139">Selection mode is exited by calling **glRenderMode** with an argument other than GL\_SELECT.</span></span> <span data-ttu-id="cb2bb-140">Chaque fois que **glRenderMode** est appelé alors que le mode de rendu est GL \_ Select, il retourne le nombre d’enregistrements d’accès copiés dans la *mémoire tampon*, réinitialise l’indicateur de dépassement de capacité et le pointeur de mémoire tampon de sélection, puis initialise la pile de noms pour qu’elle soit vide.</span><span class="sxs-lookup"><span data-stu-id="cb2bb-140">Whenever **glRenderMode** is called while the render mode is GL\_SELECT, it returns the number of hit records copied to *buffer*, resets the overflow flag and the selection buffer pointer, and initializes the name stack to be empty.</span></span> <span data-ttu-id="cb2bb-141">Si le bit de dépassement de capacité a été défini lors de l’appel de **glRenderMode** , un nombre d’enregistrements d’accès négatif est retourné.</span><span class="sxs-lookup"><span data-stu-id="cb2bb-141">If the overflow bit was set when **glRenderMode** was called, a negative hit record count is returned.</span></span>

<span data-ttu-id="cb2bb-142">Le contenu de *buffer* n’est pas défini tant que [**glRenderMode**](glrendermode.md) n’est pas appelé avec un argument autre que GL \_ Select.</span><span class="sxs-lookup"><span data-stu-id="cb2bb-142">The contents of *buffer* are undefined until [**glRenderMode**](glrendermode.md) is called with an argument other than GL\_SELECT.</span></span>

<span data-ttu-id="cb2bb-143">Les  / primitives **glEnd** glBegin et les appels à [**glRasterPos**](glrasterpos-functions.md) peuvent entraîner des résultats.</span><span class="sxs-lookup"><span data-stu-id="cb2bb-143">The **glBegin**/**glEnd** primitives and calls to [**glRasterPos**](glrasterpos-functions.md) can result in hits.</span></span>

<span data-ttu-id="cb2bb-144">La fonction suivante récupère des informations relatives à **glSelectBuffer**:</span><span class="sxs-lookup"><span data-stu-id="cb2bb-144">The following function retrieves information related to **glSelectBuffer**:</span></span>

<span data-ttu-id="cb2bb-145">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument de la profondeur de la \_ pile nom GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="cb2bb-145">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_NAME\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="cb2bb-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cb2bb-146">Requirements</span></span>



| <span data-ttu-id="cb2bb-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cb2bb-147">Requirement</span></span> | <span data-ttu-id="cb2bb-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb2bb-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cb2bb-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb2bb-149">Minimum supported client</span></span><br/> | <span data-ttu-id="cb2bb-150">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cb2bb-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="cb2bb-151">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb2bb-151">Minimum supported server</span></span><br/> | <span data-ttu-id="cb2bb-152">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cb2bb-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cb2bb-153">En-tête</span><span class="sxs-lookup"><span data-stu-id="cb2bb-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb2bb-154"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb2bb-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="cb2bb-155">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="cb2bb-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="cb2bb-156"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cb2bb-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="cb2bb-157">DLL</span><span class="sxs-lookup"><span data-stu-id="cb2bb-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb2bb-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb2bb-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb2bb-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cb2bb-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb2bb-160">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="cb2bb-160">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="cb2bb-161">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="cb2bb-161">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="cb2bb-162">**glFeedbackBuffer**</span><span class="sxs-lookup"><span data-stu-id="cb2bb-162">**glFeedbackBuffer**</span></span>](glfeedbackbuffer.md)
</dt> <dt>

[<span data-ttu-id="cb2bb-163">**glInitNames**</span><span class="sxs-lookup"><span data-stu-id="cb2bb-163">**glInitNames**</span></span>](glinitnames.md)
</dt> <dt>

[<span data-ttu-id="cb2bb-164">**glLoadName**</span><span class="sxs-lookup"><span data-stu-id="cb2bb-164">**glLoadName**</span></span>](glloadname.md)
</dt> <dt>

[<span data-ttu-id="cb2bb-165">**glPushName**</span><span class="sxs-lookup"><span data-stu-id="cb2bb-165">**glPushName**</span></span>](glpushname.md)
</dt> <dt>

[<span data-ttu-id="cb2bb-166">**glRenderMode**</span><span class="sxs-lookup"><span data-stu-id="cb2bb-166">**glRenderMode**</span></span>](glrendermode.md)
</dt> </dl>

 

 





