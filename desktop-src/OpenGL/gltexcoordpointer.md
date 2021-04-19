---
title: fonction glTexCoordPointer (GL. h)
description: La fonction glTexCoordPointer définit un tableau de coordonnées de texture.
ms.assetid: c3640a1b-ccc7-4f1a-94a5-a164f7377dbc
keywords:
- glTexCoordPointer fonction OpenGL
topic_type:
- apiref
api_name:
- glTexCoordPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: febc9c79bdbc4a1ed1c14380af47f36309f12662
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513237"
---
# <a name="gltexcoordpointer-function"></a><span data-ttu-id="35087-104">glTexCoordPointer fonction)</span><span class="sxs-lookup"><span data-stu-id="35087-104">glTexCoordPointer function</span></span>

<span data-ttu-id="35087-105">La fonction **glTexCoordPointer** définit un tableau de coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="35087-105">The **glTexCoordPointer** function defines an array of texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="35087-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="35087-106">Syntax</span></span>


```C++
void WINAPI glTexCoordPointer(
         GLint   size,
         GLenum  type,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a><span data-ttu-id="35087-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="35087-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35087-108">*size*</span><span class="sxs-lookup"><span data-stu-id="35087-108">*size*</span></span> 
</dt> <dd>

<span data-ttu-id="35087-109">Nombre de coordonnées par élément de tableau.</span><span class="sxs-lookup"><span data-stu-id="35087-109">The number of coordinates per array element.</span></span> <span data-ttu-id="35087-110">La valeur de *Size* doit être 1, 2, 3 ou 4.</span><span class="sxs-lookup"><span data-stu-id="35087-110">The value of *size* must be 1, 2, 3, or 4.</span></span>

</dd> <dt>

<span data-ttu-id="35087-111">*type*</span><span class="sxs-lookup"><span data-stu-id="35087-111">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="35087-112">Type de données de chaque coordonnée de texture dans le tableau à l’aide des constantes symboliques suivantes : **GL \_ short**, **GL \_ int**, **GL \_ float** et **GL \_ double**.</span><span class="sxs-lookup"><span data-stu-id="35087-112">The data type of each texture coordinate in the array using the following symbolic constants: **GL\_SHORT**, **GL\_INT**, **GL\_FLOAT**, and **GL\_DOUBLE**.</span></span>

</dd> <dt>

<span data-ttu-id="35087-113">*progrès*</span><span class="sxs-lookup"><span data-stu-id="35087-113">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="35087-114">Offset d’octet entre les éléments de tableau consécutifs.</span><span class="sxs-lookup"><span data-stu-id="35087-114">The byte offset between consecutive array elements.</span></span> <span data-ttu-id="35087-115">Quand *Stride* est égal à zéro, les éléments de tableau sont étroitement empaquetés dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="35087-115">When *stride* is zero, the array elements are tightly packed in the array.</span></span>

</dd> <dt>

<span data-ttu-id="35087-116">*pointeur*</span><span class="sxs-lookup"><span data-stu-id="35087-116">*pointer*</span></span> 
</dt> <dd>

<span data-ttu-id="35087-117">Pointeur vers la première coordonnée du premier élément dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="35087-117">A pointer to the first coordinate of the first element in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35087-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="35087-118">Return value</span></span>

<span data-ttu-id="35087-119">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="35087-119">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="35087-120">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="35087-120">Error codes</span></span>

<span data-ttu-id="35087-121">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="35087-121">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="35087-122">Nom</span><span class="sxs-lookup"><span data-stu-id="35087-122">Name</span></span>                                                                                              | <span data-ttu-id="35087-123">Signification</span><span class="sxs-lookup"><span data-stu-id="35087-123">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="35087-124"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="35087-124"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>  | <span data-ttu-id="35087-125">le *type* n’est pas une valeur acceptée.</span><span class="sxs-lookup"><span data-stu-id="35087-125">*type* was not an accepted value.</span></span><br/> |
| <dl> <span data-ttu-id="35087-126"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="35087-126"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="35087-127">la *taille* n’est pas 1, 2, 3 ou 4.</span><span class="sxs-lookup"><span data-stu-id="35087-127">*size* was not 1, 2, 3, or 4.</span></span><br/>     |
| <dl> <span data-ttu-id="35087-128"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="35087-128"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="35087-129">*Stride* était négatif.</span><span class="sxs-lookup"><span data-stu-id="35087-129">*stride* was negative.</span></span><br/>            |



## <a name="remarks"></a><span data-ttu-id="35087-130">Notes</span><span class="sxs-lookup"><span data-stu-id="35087-130">Remarks</span></span>

<span data-ttu-id="35087-131">La fonction **glTexCoordPointer** spécifie l’emplacement et les données d’un tableau de coordonnées de texture à utiliser lors du rendu. Le paramètre *Size* spécifie le nombre de coordonnées utilisées pour chaque élément du tableau. Le paramètre de *type* spécifie le type de données de chaque coordonnée de texture.</span><span class="sxs-lookup"><span data-stu-id="35087-131">The **glTexCoordPointer** function specifies the location and data of an array of texture coordinates to use when rendering.The *size* parameter specifies the number of coordinates used for each element of the array.The *type* parameter specifies the data type of each texture coordinate.</span></span> <span data-ttu-id="35087-132">Le paramètre *Stride* détermine le décalage d’octets d’un élément de tableau à l’autre, ce qui permet d’empaqueter des vertex et des attributs dans un tableau unique ou un stockage dans des tableaux séparés.</span><span class="sxs-lookup"><span data-stu-id="35087-132">The *stride* parameter determines the byte offset from one array element to the next, enabling the packing of vertices and attributes in a single array or storage in separate arrays.</span></span> <span data-ttu-id="35087-133">Dans certaines implémentations, le stockage des vertex et des attributs dans un tableau unique peut être plus efficace que l’utilisation de tableaux séparés.</span><span class="sxs-lookup"><span data-stu-id="35087-133">In some implementations, storing the vertices and attributes in a single array can be more efficient than using separate arrays.</span></span> <span data-ttu-id="35087-134">Pour plus d’informations, consultez [**glInterleavedArrays**](glinterleavedarrays.md).</span><span class="sxs-lookup"><span data-stu-id="35087-134">For more information, see [**glInterleavedArrays**](glinterleavedarrays.md).</span></span> <span data-ttu-id="35087-135">Lorsqu’un tableau de coordonnées de texture est spécifié, la taille, le type, la Stride et le pointeur sont enregistrés à l’État côté client.</span><span class="sxs-lookup"><span data-stu-id="35087-135">When a texture coordinate array is specified, size, type, stride, and pointer are saved client-side state.</span></span>

<span data-ttu-id="35087-136">Un tableau de coordonnées de texture est activé quand vous spécifiez la constante de **\_ \_ \_ tableau** de coordonnées de la texture GL avec [**glEnableClientState**](glenableclientstate.md).</span><span class="sxs-lookup"><span data-stu-id="35087-136">A texture coordinate array is enabled when you specify the **GL\_TEXTURE\_COORD\_ARRAY** constant with [**glEnableClientState**](glenableclientstate.md).</span></span> <span data-ttu-id="35087-137">Quand cette option est activée, [**glDrawArrays**](gldrawarrays.md), [**glDrawElements**](gldrawelements.md)et [**glArrayElement**](glarrayelement.md) utilisent le tableau de coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="35087-137">When enabled, [**glDrawArrays**](gldrawarrays.md), [**glDrawElements**](gldrawelements.md), and [**glArrayElement**](glarrayelement.md) use the texture coordinate array.</span></span> <span data-ttu-id="35087-138">Par défaut, le tableau de coordonnées de texture est désactivé.</span><span class="sxs-lookup"><span data-stu-id="35087-138">By default the texture coordinate array is disabled.</span></span>

<span data-ttu-id="35087-139">Vous ne pouvez pas inclure des **glTexCoordPointer** dans des listes d’affichage.</span><span class="sxs-lookup"><span data-stu-id="35087-139">You cannot include **glTexCoordPointer** in display lists.</span></span>

<span data-ttu-id="35087-140">Lorsque vous spécifiez un tableau de coordonnées de texture à l’aide de **glTexCoordPointer**, les valeurs de tous les paramètres de tableau de coordonnées de texture de la fonction sont enregistrées dans un État côté client et les éléments de tableau statique peuvent être mis en cache.</span><span class="sxs-lookup"><span data-stu-id="35087-140">When you specify a texture coordinate array using **glTexCoordPointer**, the values of all the function's texture coordinate array parameters are saved in a client-side state, and static array elements can be cached.</span></span> <span data-ttu-id="35087-141">Étant donné que les paramètres de tableau de coordonnées de texture sont des États côté client, leurs valeurs ne sont pas enregistrées ou restaurées par [**glPushAttrib**](glpushattrib.md) et [**glPopAttrib**](glpopattrib.md).</span><span class="sxs-lookup"><span data-stu-id="35087-141">Because the texture coordinate array parameters are client-side state, their values are not saved or restored by [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md).</span></span>

<span data-ttu-id="35087-142">Bien qu’aucune erreur ne soit générée lorsque vous appelez **glTexCoordPointer** dans des paires [**glBegin**](glbegin.md) et [**glEnd**](glend.md) , les résultats ne sont pas définis.</span><span class="sxs-lookup"><span data-stu-id="35087-142">Although no error is generated when you call **glTexCoordPointer** within [**glBegin**](glbegin.md) and [**glEnd**](glend.md) pairs, the results are undefined.</span></span>

<span data-ttu-id="35087-143">Les fonctions suivantes récupèrent les informations relatives à **glTexCoordPointer**:</span><span class="sxs-lookup"><span data-stu-id="35087-143">The following functions retrieve information related to **glTexCoordPointer**:</span></span>

<span data-ttu-id="35087-144">[**glIsEnabled**](glisenabled.md) avec argument **GL \_ texture \_ Coord \_ tableau**</span><span class="sxs-lookup"><span data-stu-id="35087-144">[**glIsEnabled**](glisenabled.md) with argument **GL\_TEXTURE\_COORD\_ARRAY**</span></span>

<span data-ttu-id="35087-145">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument **taille de la texture du GL \_ \_ \_ \_ taille du tableau**</span><span class="sxs-lookup"><span data-stu-id="35087-145">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument **GL\_TEXTURE\_COORD\_ARRAY\_SIZE**</span></span>

<span data-ttu-id="35087-146">**glGet** avec argument **GL \_ texture \_ Coord \_ tableau \_ Stride**</span><span class="sxs-lookup"><span data-stu-id="35087-146">**glGet** with argument **GL\_TEXTURE\_COORD\_ARRAY\_STRIDE**</span></span>

<span data-ttu-id="35087-147">**glGet** avec argument **\_ \_ \_ \_ nombre** de coordonnées de la texture du GL</span><span class="sxs-lookup"><span data-stu-id="35087-147">**glGet** with argument **GL\_TEXTURE\_COORD\_ARRAY\_COUNT**</span></span>

<span data-ttu-id="35087-148">**glGet** avec argument de la **\_ texture GL \_ \_ \_ type de tableau** de coordonnées</span><span class="sxs-lookup"><span data-stu-id="35087-148">**glGet** with argument **GL\_TEXTURE\_COORD\_ARRAY\_TYPE**</span></span>

<span data-ttu-id="35087-149">[**glGetPointerv**](glgetpointerv.md) avec argument de la **texture du GL \_ pointeur de \_ \_ tableau \_ de repère**</span><span class="sxs-lookup"><span data-stu-id="35087-149">[**glGetPointerv**](glgetpointerv.md) with argument **GL\_TEXTURE\_COORD\_ARRAY\_POINTER**</span></span>

## <a name="requirements"></a><span data-ttu-id="35087-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="35087-150">Requirements</span></span>



| <span data-ttu-id="35087-151">Condition requise</span><span class="sxs-lookup"><span data-stu-id="35087-151">Requirement</span></span> | <span data-ttu-id="35087-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="35087-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="35087-153">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35087-153">Minimum supported client</span></span><br/> | <span data-ttu-id="35087-154">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="35087-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="35087-155">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35087-155">Minimum supported server</span></span><br/> | <span data-ttu-id="35087-156">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="35087-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="35087-157">En-tête</span><span class="sxs-lookup"><span data-stu-id="35087-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="35087-158"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="35087-158"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="35087-159">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="35087-159">Library</span></span><br/>                  | <dl> <span data-ttu-id="35087-160"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="35087-160"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="35087-161">DLL</span><span class="sxs-lookup"><span data-stu-id="35087-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35087-162"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35087-162"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35087-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="35087-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35087-164">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="35087-164">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="35087-165">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="35087-165">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="35087-166">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="35087-166">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="35087-167">**glDrawElements**</span><span class="sxs-lookup"><span data-stu-id="35087-167">**glDrawElements**</span></span>](gldrawelements.md)
</dt> <dt>

[<span data-ttu-id="35087-168">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="35087-168">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="35087-169">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="35087-169">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="35087-170">**glGetPointerv**</span><span class="sxs-lookup"><span data-stu-id="35087-170">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="35087-171">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="35087-171">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="35087-172">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="35087-172">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="35087-173">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="35087-173">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="35087-174">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="35087-174">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="35087-175">**glPopClientAttrib**</span><span class="sxs-lookup"><span data-stu-id="35087-175">**glPopClientAttrib**</span></span>](glpopclientattrib.md)
</dt> <dt>

[<span data-ttu-id="35087-176">**glPushClientAttrib**</span><span class="sxs-lookup"><span data-stu-id="35087-176">**glPushClientAttrib**</span></span>](glpushclientattrib.md)
</dt> <dt>

[<span data-ttu-id="35087-177">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="35087-177">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="35087-178">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="35087-178">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





