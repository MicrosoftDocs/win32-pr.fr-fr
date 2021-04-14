---
title: fonction glInterleavedArrays (GL. h)
description: La fonction glInterleavedArrays spécifie et active simultanément plusieurs tableaux entrelacés dans un plus grand tableau d’agrégats.
ms.assetid: f1133949-d755-43e3-bf29-8e4c7fb17980
keywords:
- glInterleavedArrays fonction OpenGL
topic_type:
- apiref
api_name:
- glInterleavedArrays
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41403210e78d1a65dd700561243846d6e45bad67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384119"
---
# <a name="glinterleavedarrays-function"></a><span data-ttu-id="06b31-104">glInterleavedArrays fonction)</span><span class="sxs-lookup"><span data-stu-id="06b31-104">glInterleavedArrays function</span></span>

<span data-ttu-id="06b31-105">La fonction **glInterleavedArrays** spécifie et active simultanément plusieurs tableaux entrelacés dans un plus grand tableau d’agrégats.</span><span class="sxs-lookup"><span data-stu-id="06b31-105">The **glInterleavedArrays** function simultaneously specifies and enables several interleaved arrays in a larger aggregate array.</span></span>

## <a name="syntax"></a><span data-ttu-id="06b31-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="06b31-106">Syntax</span></span>


```C++
void WINAPI glInterleavedArrays(
         GLenum  format,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a><span data-ttu-id="06b31-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="06b31-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06b31-108">*format*</span><span class="sxs-lookup"><span data-stu-id="06b31-108">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="06b31-109">Type de tableau à activer.</span><span class="sxs-lookup"><span data-stu-id="06b31-109">The type of array to enable.</span></span> <span data-ttu-id="06b31-110">Le paramètre peut prendre l’une des valeurs symboliques suivantes : GL \_ V2F, GL \_ V3F, GL \_ C4UB \_ V2F, GL \_ C4UB \_ V3F, GL \_ C3F \_ V3F, GL \_ N3F \_ V3F, GL C4F N3F V3F, \_ \_ \_ GL \_ T2F \_ V3F, GL \_ T4F \_ V4F, GL \_ T2F \_ C4UB \_ V3F, GL T2F C3F V3F, GL T2F N3F V3F \_ \_ \_ \_ \_ \_ , GL \_ T2F \_ C4F N3F V3F \_ \_ ou GL \_ T4F \_ \_ \_ C4F N3F V4F.</span><span class="sxs-lookup"><span data-stu-id="06b31-110">The parameter can assume one of the following symbolic values: GL\_V2F, GL\_V3F, GL\_C4UB\_V2F, GL\_C4UB\_V3F, GL\_C3F\_V3F, GL\_N3F\_V3F, GL\_C4F\_N3F\_V3F, GL\_T2F\_V3F, GL\_T4F\_V4F, GL\_T2F\_C4UB\_V3F, GL\_T2F\_C3F\_V3F, GL\_T2F\_N3F\_V3F, GL\_T2F\_C4F\_N3F\_V3F, or GL\_T4F\_C4F\_N3F\_V4F.</span></span>

</dd> <dt>

<span data-ttu-id="06b31-111">*progrès*</span><span class="sxs-lookup"><span data-stu-id="06b31-111">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="06b31-112">Offset, en octets, entre chaque élément de tableau d’agrégation.</span><span class="sxs-lookup"><span data-stu-id="06b31-112">The offset in bytes between each aggregate array element.</span></span>

</dd> <dt>

<span data-ttu-id="06b31-113">*pointeur*</span><span class="sxs-lookup"><span data-stu-id="06b31-113">*pointer*</span></span> 
</dt> <dd>

<span data-ttu-id="06b31-114">Pointeur vers le premier élément d’un tableau d’agrégats.</span><span class="sxs-lookup"><span data-stu-id="06b31-114">A pointer to the first element of an aggregate array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06b31-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="06b31-115">Return value</span></span>

<span data-ttu-id="06b31-116">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="06b31-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="06b31-117">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="06b31-117">Error codes</span></span>

<span data-ttu-id="06b31-118">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="06b31-118">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="06b31-119">Nom</span><span class="sxs-lookup"><span data-stu-id="06b31-119">Name</span></span>                                                                                                  | <span data-ttu-id="06b31-120">Signification</span><span class="sxs-lookup"><span data-stu-id="06b31-120">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="06b31-121"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="06b31-121"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="06b31-122">le *format* n’est pas une valeur acceptée.</span><span class="sxs-lookup"><span data-stu-id="06b31-122">*format* was not an accepted value.</span></span><br/>                                                                                        |
| <dl> <span data-ttu-id="06b31-123"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="06b31-123"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="06b31-124">*Stride* était une valeur négative.</span><span class="sxs-lookup"><span data-stu-id="06b31-124">*stride* was a negative value.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="06b31-125"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="06b31-125"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="06b31-126">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="06b31-126">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="06b31-127">Notes</span><span class="sxs-lookup"><span data-stu-id="06b31-127">Remarks</span></span>

<span data-ttu-id="06b31-128">Avec la fonction **glInterleavedArrays** , vous pouvez spécifier et activer simultanément plusieurs tableaux de couleur, de texture normale, de texture et de vertex entrelacés dont les éléments font partie d’un élément de tableau d’agrégats plus grand.</span><span class="sxs-lookup"><span data-stu-id="06b31-128">With the **glInterleavedArrays** function, you can simultaneously specify and enable several interleaved color, normal, texture, and vertex arrays whose elements are part of a larger aggregate array element.</span></span> <span data-ttu-id="06b31-129">Pour certaines architectures de mémoire, cette solution est plus efficace que la spécification des tableaux séparément.</span><span class="sxs-lookup"><span data-stu-id="06b31-129">For some memory architectures, this is more efficient than specifying the arrays separately.</span></span>

<span data-ttu-id="06b31-130">Si le paramètre *Stride* est égal à zéro, les éléments de tableau d’agrégation sont stockés consécutivement ; Sinon, les octets *Stride* se produisent entre les éléments du tableau d’agrégation.</span><span class="sxs-lookup"><span data-stu-id="06b31-130">If the *stride* parameter is zero then the aggregate array elements are stored consecutively; otherwise *stride* bytes occur between aggregate array elements.</span></span>

<span data-ttu-id="06b31-131">Le paramètre de *format* sert de clé qui décrit comment extraire des tableaux individuels du tableau d’agrégats :</span><span class="sxs-lookup"><span data-stu-id="06b31-131">The *format* parameter serves as a key that describes how to extract individual arrays from the aggregate array:</span></span>

-   <span data-ttu-id="06b31-132">Si le *format* contient un T, les coordonnées de texture sont extraites du tableau entrelacé.</span><span class="sxs-lookup"><span data-stu-id="06b31-132">If *format* contains a T, then texture coordinates are extracted from the interleaved array.</span></span>
-   <span data-ttu-id="06b31-133">Si C est présent, les valeurs de couleur sont extraites.</span><span class="sxs-lookup"><span data-stu-id="06b31-133">If C is present, color values are extracted.</span></span>
-   <span data-ttu-id="06b31-134">Si N est présent, les coordonnées normales sont extraites.</span><span class="sxs-lookup"><span data-stu-id="06b31-134">If N is present, normal coordinates are extracted.</span></span>
-   <span data-ttu-id="06b31-135">Les coordonnées de vertex sont toujours extraites.</span><span class="sxs-lookup"><span data-stu-id="06b31-135">Vertex coordinates are always extracted.</span></span>
-   <span data-ttu-id="06b31-136">Les chiffres 2, 3 et 4 désignent le nombre de valeurs extraites.</span><span class="sxs-lookup"><span data-stu-id="06b31-136">The digits 2, 3, and 4 denote how many values are extracted.</span></span>
-   <span data-ttu-id="06b31-137">F indique que les valeurs sont extraites en tant que valeurs à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="06b31-137">F indicates that values are extracted as floating point values.</span></span>
-   <span data-ttu-id="06b31-138">Si 4UB suit le C, les couleurs peuvent également être extraites sous forme de 4 octets non signés.</span><span class="sxs-lookup"><span data-stu-id="06b31-138">If 4UB follows the C, colors may also be extracted as 4 unsigned bytes.</span></span> <span data-ttu-id="06b31-139">Si une couleur est extraite sous la forme de 4 octets non signés, l’élément de tableau de vertex qui suit se trouve à la première adresse alignée à virgule flottante possible.</span><span class="sxs-lookup"><span data-stu-id="06b31-139">If a color is extracted as 4 unsigned bytes, the vertex array element that follows is located at the first possible floating-point aligned address.</span></span>

<span data-ttu-id="06b31-140">Si vous appelez **glInterleavedArrays** lors de la compilation d’une liste d’affichage, celle-ci n’est pas compilée dans la liste mais est exécutée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="06b31-140">If you call **glInterleavedArrays** while compiling a display list, it is not compiled into the list but is executed immediately.</span></span>

<span data-ttu-id="06b31-141">Vous ne pouvez pas inclure d’appels à **glInterleavedArrays** dans **glDisableClientState** entre les appels à [**glBegin**](glbegin.md) et l’appel correspondant à **glEnd**.</span><span class="sxs-lookup"><span data-stu-id="06b31-141">You cannot include calls to **glInterleavedArrays** in **glDisableClientState** between calls to [**glBegin**](glbegin.md) and the corresponding call to **glEnd**.</span></span>

> [!Note]  
> <span data-ttu-id="06b31-142">La fonction **glInterleavedArrays** est disponible uniquement dans OpenGL version 1,1 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="06b31-142">The **glInterleavedArrays** function is only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="06b31-143">La fonction **glInterleavedArrays** est implémentée côté client sans protocole.</span><span class="sxs-lookup"><span data-stu-id="06b31-143">The **glInterleavedArrays** function is implemented on the client side with no protocol.</span></span> <span data-ttu-id="06b31-144">Étant donné que les paramètres du tableau de vertex sont des États côté client, ils ne sont pas enregistrés ou restaurés par [**glPushAttrib**](glpushattrib.md) et **glPopAttrib**.</span><span class="sxs-lookup"><span data-stu-id="06b31-144">Because the vertex array parameters are client-side state, they are not saved or restored by [**glPushAttrib**](glpushattrib.md) and **glPopAttrib**.</span></span> <span data-ttu-id="06b31-145">Utilisez [**glPushClientAttrib**](glpushclientattrib.md) et **glPopClientAttrib** à la place.</span><span class="sxs-lookup"><span data-stu-id="06b31-145">Use [**glPushClientAttrib**](glpushclientattrib.md) and **glPopClientAttrib** instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="06b31-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="06b31-146">Requirements</span></span>



| <span data-ttu-id="06b31-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="06b31-147">Requirement</span></span> | <span data-ttu-id="06b31-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="06b31-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="06b31-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="06b31-149">Minimum supported client</span></span><br/> | <span data-ttu-id="06b31-150">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="06b31-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="06b31-151">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="06b31-151">Minimum supported server</span></span><br/> | <span data-ttu-id="06b31-152">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="06b31-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="06b31-153">En-tête</span><span class="sxs-lookup"><span data-stu-id="06b31-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="06b31-154"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="06b31-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="06b31-155">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="06b31-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="06b31-156"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="06b31-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="06b31-157">DLL</span><span class="sxs-lookup"><span data-stu-id="06b31-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06b31-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06b31-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06b31-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="06b31-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06b31-160">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="06b31-160">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="06b31-161">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="06b31-161">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="06b31-162">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="06b31-162">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="06b31-163">**glDrawElements**</span><span class="sxs-lookup"><span data-stu-id="06b31-163">**glDrawElements**</span></span>](gldrawelements.md)
</dt> <dt>

[<span data-ttu-id="06b31-164">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="06b31-164">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="06b31-165">**glEnableClientState**</span><span class="sxs-lookup"><span data-stu-id="06b31-165">**glEnableClientState**</span></span>](glenableclientstate.md)
</dt> <dt>

[<span data-ttu-id="06b31-166">**glGetPointerv**</span><span class="sxs-lookup"><span data-stu-id="06b31-166">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="06b31-167">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="06b31-167">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="06b31-168">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="06b31-168">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="06b31-169">**glPushAttrib**</span><span class="sxs-lookup"><span data-stu-id="06b31-169">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="06b31-170">**glPushClientAttrib**</span><span class="sxs-lookup"><span data-stu-id="06b31-170">**glPushClientAttrib**</span></span>](glpushclientattrib.md)
</dt> <dt>

[<span data-ttu-id="06b31-171">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="06b31-171">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="06b31-172">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="06b31-172">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





