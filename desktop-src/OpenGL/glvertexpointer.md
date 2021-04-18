---
title: fonction glVertexPointer (GL. h)
description: La fonction glVertexPointer définit un tableau de données de vertex.
ms.assetid: e5f97fdc-9448-4389-8533-3855a3213feb
keywords:
- glVertexPointer fonction OpenGL
topic_type:
- apiref
api_name:
- glVertexPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 422dd1a7938cc5adb183ff7e17c59a8f52eb4909
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466315"
---
# <a name="glvertexpointer-function"></a><span data-ttu-id="8135a-104">glVertexPointer fonction)</span><span class="sxs-lookup"><span data-stu-id="8135a-104">glVertexPointer function</span></span>

<span data-ttu-id="8135a-105">La fonction **glVertexPointer** définit un tableau de données de vertex.</span><span class="sxs-lookup"><span data-stu-id="8135a-105">The **glVertexPointer** function defines an array of vertex data.</span></span>

## <a name="syntax"></a><span data-ttu-id="8135a-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8135a-106">Syntax</span></span>


```C++
void WINAPI glVertexPointer(
         GLint   size,
         GLenum  type,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a><span data-ttu-id="8135a-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8135a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8135a-108">*size*</span><span class="sxs-lookup"><span data-stu-id="8135a-108">*size*</span></span> 
</dt> <dd>

<span data-ttu-id="8135a-109">Nombre de coordonnées par vertex.</span><span class="sxs-lookup"><span data-stu-id="8135a-109">The number of coordinates per vertex.</span></span> <span data-ttu-id="8135a-110">La valeur de *Size* doit être 2, 3 ou 4.</span><span class="sxs-lookup"><span data-stu-id="8135a-110">The value of *size* must be 2, 3, or 4.</span></span>

</dd> <dt>

<span data-ttu-id="8135a-111">*type*</span><span class="sxs-lookup"><span data-stu-id="8135a-111">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="8135a-112">Type de données de chaque coordonnée dans le tableau à l’aide des constantes symboliques suivantes : GL \_ short, GL \_ int, GL \_ float et GL \_ double.</span><span class="sxs-lookup"><span data-stu-id="8135a-112">The data type of each coordinate in the array using the following symbolic constants: GL\_SHORT, GL\_INT, GL\_FLOAT, and GL\_DOUBLE.</span></span>

</dd> <dt>

<span data-ttu-id="8135a-113">*progrès*</span><span class="sxs-lookup"><span data-stu-id="8135a-113">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="8135a-114">Décalage d’octet entre les vertex consécutifs.</span><span class="sxs-lookup"><span data-stu-id="8135a-114">The byte offset between consecutive vertices.</span></span> <span data-ttu-id="8135a-115">Lorsque la valeur de *Stride* est égale à zéro, les vertex sont étroitement empaquetés dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="8135a-115">When *stride* is zero, the vertices are tightly packed in the array.</span></span>

</dd> <dt>

<span data-ttu-id="8135a-116">*pointeur*</span><span class="sxs-lookup"><span data-stu-id="8135a-116">*pointer*</span></span> 
</dt> <dd>

<span data-ttu-id="8135a-117">Pointeur vers la première coordonnée du premier vertex dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="8135a-117">A pointer to the first coordinate of the first vertex in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8135a-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8135a-118">Return value</span></span>

<span data-ttu-id="8135a-119">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="8135a-119">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8135a-120">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="8135a-120">Error codes</span></span>

<span data-ttu-id="8135a-121">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="8135a-121">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="8135a-122">Nom</span><span class="sxs-lookup"><span data-stu-id="8135a-122">Name</span></span>                                                                                              | <span data-ttu-id="8135a-123">Signification</span><span class="sxs-lookup"><span data-stu-id="8135a-123">Meaning</span></span>                                       |
|---------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="8135a-124"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8135a-124"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="8135a-125">la *taille* n’est pas 2, 3 ou 4.</span><span class="sxs-lookup"><span data-stu-id="8135a-125">*size* was not 2, 3, or 4.</span></span> <br/>        |
| <dl> <span data-ttu-id="8135a-126"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8135a-126"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>  | <span data-ttu-id="8135a-127">le *type* n’est pas une valeur acceptée.</span><span class="sxs-lookup"><span data-stu-id="8135a-127">*type* was not an accepted value.</span></span><br/>  |
| <dl> <span data-ttu-id="8135a-128"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8135a-128"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="8135a-129">*Stride* ou *Count* était négatif.</span><span class="sxs-lookup"><span data-stu-id="8135a-129">*stride* or *count* was negative.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="8135a-130">Notes</span><span class="sxs-lookup"><span data-stu-id="8135a-130">Remarks</span></span>

<span data-ttu-id="8135a-131">La fonction **glVertexPointer** spécifie l’emplacement et les données d’un tableau de coordonnées de vertex à utiliser lors du rendu.</span><span class="sxs-lookup"><span data-stu-id="8135a-131">The **glVertexPointer** function specifies the location and data of an array of vertex coordinates to use when rendering.</span></span> <span data-ttu-id="8135a-132">Le paramètre *Size* spécifie le nombre de coordonnées par vertex.</span><span class="sxs-lookup"><span data-stu-id="8135a-132">The *size* parameter specifies the number of coordinates per vertex.</span></span> <span data-ttu-id="8135a-133">Le paramètre de *type* spécifie le type de données de chaque coordonnée de vertex.</span><span class="sxs-lookup"><span data-stu-id="8135a-133">The *type* parameter specifies the data type of each vertex coordinate.</span></span> <span data-ttu-id="8135a-134">Le paramètre *Stride* détermine le décalage d’octets d’un vertex à l’autre, ce qui permet d’empaqueter des vertex et des attributs dans un tableau unique ou un stockage dans des tableaux séparés.</span><span class="sxs-lookup"><span data-stu-id="8135a-134">The *stride* parameter determines the byte offset from one vertex to the next, enabling the packing of vertices and attributes in a single array or storage in separate arrays.</span></span> <span data-ttu-id="8135a-135">Dans certaines implémentations, le stockage des vertex et des attributs dans un tableau unique peut être plus efficace que l’utilisation de tableaux distincts (consultez [**glInterleavedArrays**](glinterleavedarrays.md)).</span><span class="sxs-lookup"><span data-stu-id="8135a-135">In some implementations, storing the vertices and attributes in a single array can be more efficient than using separate arrays (see [**glInterleavedArrays**](glinterleavedarrays.md)).</span></span>

<span data-ttu-id="8135a-136">Un tableau de vertex est activé quand vous spécifiez \_ la \_ constante de tableau de vertex GL avec [**glEnableClientState**](glenableclientstate.md).</span><span class="sxs-lookup"><span data-stu-id="8135a-136">A vertex array is enabled when you specify the GL\_VERTEX\_ARRAY constant with [**glEnableClientState**](glenableclientstate.md).</span></span> <span data-ttu-id="8135a-137">Quand cette option est activée, [**glDrawArrays**](gldrawarrays.md), [**glDrawElements**](gldrawelements.md)et [**glArrayElement**](glarrayelement.md) utilisent le tableau de vertex.</span><span class="sxs-lookup"><span data-stu-id="8135a-137">When enabled, [**glDrawArrays**](gldrawarrays.md), [**glDrawElements**](gldrawelements.md), and [**glArrayElement**](glarrayelement.md) use the vertex array.</span></span> <span data-ttu-id="8135a-138">Par défaut, le tableau de vertex est désactivé.</span><span class="sxs-lookup"><span data-stu-id="8135a-138">By default, the vertex array is disabled.</span></span>

<span data-ttu-id="8135a-139">Vous ne pouvez pas inclure des **glVertexPointer** dans des listes d’affichage.</span><span class="sxs-lookup"><span data-stu-id="8135a-139">You cannot include **glVertexPointer** in display lists.</span></span>

<span data-ttu-id="8135a-140">Lorsque vous spécifiez un tableau de vertex à l’aide de **glVertexPointer**, les valeurs de tous les paramètres de tableau de vertex de la fonction sont enregistrées dans un État côté client et les éléments de tableau statique peuvent être mis en cache.</span><span class="sxs-lookup"><span data-stu-id="8135a-140">When you specify a vertex array using **glVertexPointer**, the values of all the function's vertex array parameters are saved in a client-side state, and static array elements can be cached.</span></span> <span data-ttu-id="8135a-141">Étant donné que les paramètres du tableau de vertex sont l’État côté client, leurs valeurs ne sont pas enregistrées ou restaurées par [**glPushAttrib**](glpushattrib.md) et **glPopAttrib**.</span><span class="sxs-lookup"><span data-stu-id="8135a-141">Because the vertex array parameters are client-side state, their values are not saved or restored by [**glPushAttrib**](glpushattrib.md) and **glPopAttrib**.</span></span>

<span data-ttu-id="8135a-142">Bien qu’aucune erreur ne soit générée si vous appelez **glVertexPointer** dans des paires [**glBegin**](glbegin.md) et [**glEnd**](glend.md) , les résultats ne sont pas définis.</span><span class="sxs-lookup"><span data-stu-id="8135a-142">Although no error is generated if you call **glVertexPointer** within [**glBegin**](glbegin.md) and [**glEnd**](glend.md) pairs, the results are undefined.</span></span>

<span data-ttu-id="8135a-143">Les fonctions suivantes récupèrent les informations relatives à **glVertexPointer**:</span><span class="sxs-lookup"><span data-stu-id="8135a-143">The following functions retrieve information related to **glVertexPointer**:</span></span>

<span data-ttu-id="8135a-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ vertex de \_ tableau \_ taille</span><span class="sxs-lookup"><span data-stu-id="8135a-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_VERTEX\_ARRAY\_SIZE</span></span>

<span data-ttu-id="8135a-145">**glGet** avec argument GL \_ vertex de \_ tableau \_ Stride</span><span class="sxs-lookup"><span data-stu-id="8135a-145">**glGet** with argument GL\_VERTEX\_ARRAY\_STRIDE</span></span>

<span data-ttu-id="8135a-146">**glGet** avec argument \_ nombre de \_ tableaux de vertex GL \_</span><span class="sxs-lookup"><span data-stu-id="8135a-146">**glGet** with argument GL\_VERTEX\_ARRAY\_COUNT</span></span>

<span data-ttu-id="8135a-147">**glGet** avec argument \_ type de \_ tableau de vertex GL \_</span><span class="sxs-lookup"><span data-stu-id="8135a-147">**glGet** with argument GL\_VERTEX\_ARRAY\_TYPE</span></span>

<span data-ttu-id="8135a-148">[**glGetPointerv**](glgetpointerv.md) avec un \_ pointeur de \_ tableau de vertex d’argument GL \_</span><span class="sxs-lookup"><span data-stu-id="8135a-148">[**glGetPointerv**](glgetpointerv.md) with argument GL\_VERTEX\_ARRAY\_POINTER</span></span>

<span data-ttu-id="8135a-149">[**glIsEnabled**](glisenabled.md) avec argument GL \_ vertex \_ Array</span><span class="sxs-lookup"><span data-stu-id="8135a-149">[**glIsEnabled**](glisenabled.md) with argument GL\_VERTEX\_ARRAY</span></span>

## <a name="requirements"></a><span data-ttu-id="8135a-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8135a-150">Requirements</span></span>



| <span data-ttu-id="8135a-151">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8135a-151">Requirement</span></span> | <span data-ttu-id="8135a-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="8135a-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8135a-153">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8135a-153">Minimum supported client</span></span><br/> | <span data-ttu-id="8135a-154">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8135a-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="8135a-155">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8135a-155">Minimum supported server</span></span><br/> | <span data-ttu-id="8135a-156">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8135a-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8135a-157">En-tête</span><span class="sxs-lookup"><span data-stu-id="8135a-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="8135a-158"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="8135a-158"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="8135a-159">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8135a-159">Library</span></span><br/>                  | <dl> <span data-ttu-id="8135a-160"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8135a-160"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="8135a-161">DLL</span><span class="sxs-lookup"><span data-stu-id="8135a-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8135a-162"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8135a-162"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8135a-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8135a-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8135a-164">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="8135a-164">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="8135a-165">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="8135a-165">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="8135a-166">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="8135a-166">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="8135a-167">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="8135a-167">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="8135a-168">**glEnableClientState**</span><span class="sxs-lookup"><span data-stu-id="8135a-168">**glEnableClientState**</span></span>](glenableclientstate.md)
</dt> <dt>

[<span data-ttu-id="8135a-169">**glGetPointerv**</span><span class="sxs-lookup"><span data-stu-id="8135a-169">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="8135a-170">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="8135a-170">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="8135a-171">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="8135a-171">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="8135a-172">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="8135a-172">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="8135a-173">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="8135a-173">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="8135a-174">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="8135a-174">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> </dl>

 

 





