---
title: fonction glDisableClientState (GL. h)
description: Les fonctions glEnableClientState et glDisableClientState activent et désactivent les tableaux, respectivement. | fonction glDisableClientState (GL. h)
ms.assetid: b3316519-00ed-45f8-9c4b-2e04c483751e
keywords:
- glDisableClientState fonction OpenGL
topic_type:
- apiref
api_name:
- glDisableClientState
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 163a7c3b679c979e5c800d2aa41ba2abb00e11f4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106522323"
---
# <a name="gldisableclientstate-function"></a><span data-ttu-id="877d1-105">glDisableClientState fonction)</span><span class="sxs-lookup"><span data-stu-id="877d1-105">glDisableClientState function</span></span>

<span data-ttu-id="877d1-106">Les fonctions [**glEnableClientState**](glenableclientstate.md) et **glDisableClientState** activent et désactivent les tableaux, respectivement.</span><span class="sxs-lookup"><span data-stu-id="877d1-106">The [**glEnableClientState**](glenableclientstate.md) and **glDisableClientState** functions enable and disable arrays respectively.</span></span>

## <a name="syntax"></a><span data-ttu-id="877d1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="877d1-107">Syntax</span></span>


```C++
void WINAPI glDisableClientState(
   GLenum array
);
```



## <a name="parameters"></a><span data-ttu-id="877d1-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="877d1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="877d1-109">*array*</span><span class="sxs-lookup"><span data-stu-id="877d1-109">*array*</span></span> 
</dt> <dd>

<span data-ttu-id="877d1-110">Constante symbolique pour le tableau que vous souhaitez activer ou désactiver.</span><span class="sxs-lookup"><span data-stu-id="877d1-110">A symbolic constant for the array you want to enable or disable.</span></span> <span data-ttu-id="877d1-111">Ce paramètre peut prendre l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="877d1-111">This parameter can assume one of the following values.</span></span>



| <span data-ttu-id="877d1-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="877d1-112">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="877d1-113">Signification</span><span class="sxs-lookup"><span data-stu-id="877d1-113">Meaning</span></span>                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_ARRAY"></span><span id="gl_color_array"></span><dl> <span data-ttu-id="877d1-114"><dt>**\_tableau de couleurs GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="877d1-114"><dt>**GL\_COLOR\_ARRAY**</dt></span></span> </dl>                          | <span data-ttu-id="877d1-115">S’il est activé, utilisez des tableaux de couleurs avec des appels à [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)ou [**glDrawArrays**](gldrawarrays.md).</span><span class="sxs-lookup"><span data-stu-id="877d1-115">If enabled, use color arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="877d1-116">Voir aussi [**glColorPointer**](glcolorpointer.md).</span><span class="sxs-lookup"><span data-stu-id="877d1-116">See also [**glColorPointer**](glcolorpointer.md).</span></span><br/>                    |
| <span id="GL_EDGE_FLAG_ARRAY"></span><span id="gl_edge_flag_array"></span><dl> <span data-ttu-id="877d1-117"><dt>**\_tableau d' \_ indicateurs de périphérie du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="877d1-117"><dt>**GL\_EDGE\_FLAG\_ARRAY**</dt></span></span> </dl>             | <span data-ttu-id="877d1-118">S’il est activé, utilisez des tableaux d’indicateurs de bord avec des appels à [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)ou [**glDrawArrays**](gldrawarrays.md).</span><span class="sxs-lookup"><span data-stu-id="877d1-118">If enabled, use edge flag arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="877d1-119">Voir aussi [**glEdgeFlagPointer**](gledgeflagpointer.md).</span><span class="sxs-lookup"><span data-stu-id="877d1-119">See also [**glEdgeFlagPointer**](gledgeflagpointer.md).</span></span><br/>          |
| <span id="GL_INDEX_ARRAY"></span><span id="gl_index_array"></span><dl> <span data-ttu-id="877d1-120"><dt>**\_tableau d’index GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="877d1-120"><dt>**GL\_INDEX\_ARRAY**</dt></span></span> </dl>                          | <span data-ttu-id="877d1-121">S’il est activé, utilisez des tableaux d’index avec des appels à [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)ou [**glDrawArrays**](gldrawarrays.md).</span><span class="sxs-lookup"><span data-stu-id="877d1-121">If enabled, use index arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="877d1-122">Voir aussi [**glIndexPointer**](glindexpointer.md).</span><span class="sxs-lookup"><span data-stu-id="877d1-122">See also [**glIndexPointer**](glindexpointer.md).</span></span><br/>                    |
| <span id="GL_NORMAL_ARRAY"></span><span id="gl_normal_array"></span><dl> <span data-ttu-id="877d1-123"><dt>**\_tableau normal du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="877d1-123"><dt>**GL\_NORMAL\_ARRAY**</dt></span></span> </dl>                       | <span data-ttu-id="877d1-124">S’il est activé, utilisez des tableaux normaux avec des appels à [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)ou [**glDrawArrays**](gldrawarrays.md).</span><span class="sxs-lookup"><span data-stu-id="877d1-124">If enabled, use normal arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="877d1-125">Voir aussi [**glNormalPointer**](glnormalpointer.md).</span><span class="sxs-lookup"><span data-stu-id="877d1-125">See also [**glNormalPointer**](glnormalpointer.md).</span></span><br/>                 |
| <span id="GL_TEXTURE_COORD_ARRAY"></span><span id="gl_texture_coord_array"></span><dl> <span data-ttu-id="877d1-126"><dt>**Tableau de coordonnées de la \_ texture GL \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="877d1-126"><dt>**GL\_TEXTURE\_COORD\_ARRAY**</dt></span></span> </dl> | <span data-ttu-id="877d1-127">S’il est activé, utilisez des tableaux de coordonnées de texture avec des appels à [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)ou [**glDrawArrays**](gldrawarrays.md).</span><span class="sxs-lookup"><span data-stu-id="877d1-127">If enabled, use texture coordinate arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="877d1-128">Voir aussi [**glTexCoordPointer**](gltexcoordpointer.md).</span><span class="sxs-lookup"><span data-stu-id="877d1-128">See also [**glTexCoordPointer**](gltexcoordpointer.md).</span></span><br/> |
| <span id="GL_VERTEX_ARRAY"></span><span id="gl_vertex_array"></span><dl> <span data-ttu-id="877d1-129"><dt>**\_tableau de vertex GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="877d1-129"><dt>**GL\_VERTEX\_ARRAY**</dt></span></span> </dl>                       | <span data-ttu-id="877d1-130">S’il est activé, utilisez des tableaux de vertex avec des appels à [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)ou [**glDrawArrays**](gldrawarrays.md).</span><span class="sxs-lookup"><span data-stu-id="877d1-130">If enabled, use vertex arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="877d1-131">Voir aussi [**glVertexPointer**](glvertexpointer.md).</span><span class="sxs-lookup"><span data-stu-id="877d1-131">See also [**glVertexPointer**](glvertexpointer.md).</span></span><br/>                 |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="877d1-132">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="877d1-132">Return value</span></span>

<span data-ttu-id="877d1-133">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="877d1-133">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="877d1-134">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="877d1-134">Error codes</span></span>

<span data-ttu-id="877d1-135">Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="877d1-135">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="877d1-136">Nom</span><span class="sxs-lookup"><span data-stu-id="877d1-136">Name</span></span>                                                                                             | <span data-ttu-id="877d1-137">Signification</span><span class="sxs-lookup"><span data-stu-id="877d1-137">Meaning</span></span>                                       |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="877d1-138"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="877d1-138"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl> | <span data-ttu-id="877d1-139">le *tableau* n’est pas une valeur acceptée.</span><span class="sxs-lookup"><span data-stu-id="877d1-139">*array* was not an accepted value.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="877d1-140">Notes</span><span class="sxs-lookup"><span data-stu-id="877d1-140">Remarks</span></span>

<span data-ttu-id="877d1-141">Les fonctions [**glEnableClientState**](glenableclientstate.md) et **glDisableClientState** activent et désactivent différents tableaux individuels.</span><span class="sxs-lookup"><span data-stu-id="877d1-141">The [**glEnableClientState**](glenableclientstate.md) and **glDisableClientState** functions enable and disable various individual arrays.</span></span> <span data-ttu-id="877d1-142">Utilisez [**glIsEnabled**](glisenabled.md) ou [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) pour déterminer la valeur actuelle de toutes les fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="877d1-142">Use [**glIsEnabled**](glisenabled.md) or [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) to determine the current setting of any capability.</span></span>

<span data-ttu-id="877d1-143">L’appel de [**glEnableClientState**](glenableclientstate.md) et **glDisableClientState** entre les appels à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md) peut provoquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="877d1-143">Calling [**glEnableClientState**](glenableclientstate.md) and **glDisableClientState** between calls to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md) can cause an error.</span></span> <span data-ttu-id="877d1-144">Si aucune erreur n’est générée, le comportement n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="877d1-144">If no error is generated, the behavior is undefined.</span></span>

> [!Note]  
> <span data-ttu-id="877d1-145">Les fonctions [**glEnableClientState**](glenableclientstate.md) et **glDisableClientState** sont uniquement disponibles dans OpenGL version 1,1 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="877d1-145">The [**glEnableClientState**](glenableclientstate.md) and **glDisableClientState** functions are only available in OpenGL version 1.1 or later.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="877d1-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="877d1-146">Requirements</span></span>



| <span data-ttu-id="877d1-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="877d1-147">Requirement</span></span> | <span data-ttu-id="877d1-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="877d1-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="877d1-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="877d1-149">Minimum supported client</span></span><br/> | <span data-ttu-id="877d1-150">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="877d1-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="877d1-151">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="877d1-151">Minimum supported server</span></span><br/> | <span data-ttu-id="877d1-152">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="877d1-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="877d1-153">En-tête</span><span class="sxs-lookup"><span data-stu-id="877d1-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="877d1-154"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="877d1-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="877d1-155">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="877d1-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="877d1-156"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="877d1-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="877d1-157">DLL</span><span class="sxs-lookup"><span data-stu-id="877d1-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="877d1-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="877d1-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="877d1-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="877d1-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="877d1-160">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="877d1-160">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="877d1-161">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="877d1-161">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="877d1-162">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="877d1-162">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="877d1-163">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="877d1-163">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="877d1-164">**glDrawElements**</span><span class="sxs-lookup"><span data-stu-id="877d1-164">**glDrawElements**</span></span>](gldrawelements.md)
</dt> <dt>

[<span data-ttu-id="877d1-165">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="877d1-165">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="877d1-166">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="877d1-166">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="877d1-167">**glEnableClientState**</span><span class="sxs-lookup"><span data-stu-id="877d1-167">**glEnableClientState**</span></span>](glenableclientstate.md)
</dt> <dt>

[<span data-ttu-id="877d1-168">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="877d1-168">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="877d1-169">**glGetPointerv**</span><span class="sxs-lookup"><span data-stu-id="877d1-169">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="877d1-170">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="877d1-170">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="877d1-171">**glInterleavedArrays**</span><span class="sxs-lookup"><span data-stu-id="877d1-171">**glInterleavedArrays**</span></span>](glinterleavedarrays.md)
</dt> <dt>

[<span data-ttu-id="877d1-172">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="877d1-172">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="877d1-173">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="877d1-173">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="877d1-174">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="877d1-174">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





