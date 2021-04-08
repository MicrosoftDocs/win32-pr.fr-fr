---
title: fonction glPassThrough (GL. h)
description: La fonction glPassThrough place un marqueur dans la mémoire tampon de commentaires.
ms.assetid: 14664ac6-eb25-46ae-86d8-7ece31df103f
keywords:
- glPassThrough fonction OpenGL
topic_type:
- apiref
api_name:
- glPassThrough
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd1174dd933d46813a89c35b781d0408c3ac5476
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741133"
---
# <a name="glpassthrough-function"></a><span data-ttu-id="922ae-104">glPassThrough fonction)</span><span class="sxs-lookup"><span data-stu-id="922ae-104">glPassThrough function</span></span>

<span data-ttu-id="922ae-105">La fonction **glPassThrough** place un marqueur dans la mémoire tampon de commentaires.</span><span class="sxs-lookup"><span data-stu-id="922ae-105">The **glPassThrough** function places a marker in the feedback buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="922ae-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="922ae-106">Syntax</span></span>


```C++
void WINAPI glPassThrough(
   GLfloat token
);
```



## <a name="parameters"></a><span data-ttu-id="922ae-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="922ae-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="922ae-108">*token*</span><span class="sxs-lookup"><span data-stu-id="922ae-108">*token*</span></span> 
</dt> <dd>

<span data-ttu-id="922ae-109">Valeur de marqueur à placer dans la mémoire tampon de commentaires.</span><span class="sxs-lookup"><span data-stu-id="922ae-109">A marker value to be placed in the feedback buffer.</span></span> <span data-ttu-id="922ae-110">Elle est indiquée avec la valeur d’identification unique suivante.</span><span class="sxs-lookup"><span data-stu-id="922ae-110">It is indicated with the following unique identifying value.</span></span>



| <span data-ttu-id="922ae-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="922ae-111">Value</span></span>                                                                                                                                                                                   | <span data-ttu-id="922ae-112">Signification</span><span class="sxs-lookup"><span data-stu-id="922ae-112">Meaning</span></span>                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_PASS_THROUGH_TOKEN"></span><span id="gl_pass_through_token"></span><dl> <span data-ttu-id="922ae-113"><dt>**\_jeton de transfert GL \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="922ae-113"><dt>**GL\_PASS\_THROUGH\_TOKEN**</dt></span></span> </dl> | <span data-ttu-id="922ae-114">L’ordre des commandes **glPassThrough** en ce qui concerne la spécification des primitives graphiques est conservé.</span><span class="sxs-lookup"><span data-stu-id="922ae-114">The order of **glPassThrough** commands with respect to the specification of graphics primitives is maintained.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="922ae-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="922ae-115">Return value</span></span>

<span data-ttu-id="922ae-116">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="922ae-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="922ae-117">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="922ae-117">Error codes</span></span>

<span data-ttu-id="922ae-118">Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="922ae-118">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="922ae-119">Nom</span><span class="sxs-lookup"><span data-stu-id="922ae-119">Name</span></span>                                                                                                  | <span data-ttu-id="922ae-120">Signification</span><span class="sxs-lookup"><span data-stu-id="922ae-120">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="922ae-121"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="922ae-121"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="922ae-122">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="922ae-122">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="922ae-123">Notes</span><span class="sxs-lookup"><span data-stu-id="922ae-123">Remarks</span></span>

<span data-ttu-id="922ae-124">Les commentaires sont un mode de rendu OpenGL sélectionné en appelant [**glRenderMode**](glrendermode.md) avec des commentaires sur le GL \_ .</span><span class="sxs-lookup"><span data-stu-id="922ae-124">Feedback is an OpenGL render mode selected by calling [**glRenderMode**](glrendermode.md) with GL\_FEEDBACK.</span></span> <span data-ttu-id="922ae-125">Lorsque OpenGL est en mode commentaires, aucun Pixel n’est généré par pixellisation.</span><span class="sxs-lookup"><span data-stu-id="922ae-125">When OpenGL is in feedback mode, no pixels are produced by rasterization.</span></span> <span data-ttu-id="922ae-126">Au lieu de cela, les informations sur les primitives qui auraient été pixellisées sont renvoyées à l’application par OpenGL.</span><span class="sxs-lookup"><span data-stu-id="922ae-126">Instead, information about primitives that would have been rasterized is fed back to the application by OpenGL.</span></span> <span data-ttu-id="922ae-127">Consultez [**glFeedbackBuffer**](glfeedbackbuffer.md) pour obtenir une description de la mémoire tampon de commentaires et les valeurs qu’elle contient.</span><span class="sxs-lookup"><span data-stu-id="922ae-127">See [**glFeedbackBuffer**](glfeedbackbuffer.md) for a description of the feedback buffer and the values in it.</span></span>

<span data-ttu-id="922ae-128">La fonction **glPassThrough** insère un marqueur défini par l’utilisateur dans la mémoire tampon de commentaires lorsqu’il est exécuté en mode commentaires.</span><span class="sxs-lookup"><span data-stu-id="922ae-128">The **glPassThrough** function inserts a user-defined marker in the feedback buffer when it is executed in feedback mode.</span></span> <span data-ttu-id="922ae-129">Le paramètre de *jeton* est retourné comme s’il s’agissait d’une primitive.</span><span class="sxs-lookup"><span data-stu-id="922ae-129">The *token* parameter is returned as if it were a primitive.</span></span>

<span data-ttu-id="922ae-130">La fonction **glPassThrough** est ignorée si OpenGL n’est pas en mode commentaires.</span><span class="sxs-lookup"><span data-stu-id="922ae-130">The **glPassThrough** function is ignored if OpenGL is not in feedback mode.</span></span>

<span data-ttu-id="922ae-131">La fonction suivante récupère des informations relatives à **glPassThrough**:</span><span class="sxs-lookup"><span data-stu-id="922ae-131">The following function retrieves information related to **glPassThrough**:</span></span>

<span data-ttu-id="922ae-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Render \_ mode</span><span class="sxs-lookup"><span data-stu-id="922ae-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_RENDER\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="922ae-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="922ae-133">Requirements</span></span>



| <span data-ttu-id="922ae-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="922ae-134">Requirement</span></span> | <span data-ttu-id="922ae-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="922ae-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="922ae-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="922ae-136">Minimum supported client</span></span><br/> | <span data-ttu-id="922ae-137">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="922ae-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="922ae-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="922ae-138">Minimum supported server</span></span><br/> | <span data-ttu-id="922ae-139">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="922ae-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="922ae-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="922ae-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="922ae-141"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="922ae-141"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="922ae-142">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="922ae-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="922ae-143"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="922ae-143"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="922ae-144">DLL</span><span class="sxs-lookup"><span data-stu-id="922ae-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="922ae-145"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="922ae-145"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="922ae-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="922ae-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="922ae-147">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="922ae-147">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="922ae-148">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="922ae-148">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="922ae-149">**glFeedbackBuffer**</span><span class="sxs-lookup"><span data-stu-id="922ae-149">**glFeedbackBuffer**</span></span>](glfeedbackbuffer.md)
</dt> <dt>

[<span data-ttu-id="922ae-150">**glRenderMode**</span><span class="sxs-lookup"><span data-stu-id="922ae-150">**glRenderMode**</span></span>](glrendermode.md)
</dt> </dl>

 

 





