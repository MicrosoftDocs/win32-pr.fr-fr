---
title: fonction glNormalPointer (GL. h)
description: La fonction glNormalPointer définit un tableau de normales.
ms.assetid: 6ffb0522-87cc-4be1-a5b1-f6fd30e04b43
keywords:
- glNormalPointer fonction OpenGL
topic_type:
- apiref
api_name:
- glNormalPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c2f3abbfbd989351af647557ec64f8ee3172dc5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942867"
---
# <a name="glnormalpointer-function"></a><span data-ttu-id="07179-104">glNormalPointer fonction)</span><span class="sxs-lookup"><span data-stu-id="07179-104">glNormalPointer function</span></span>

<span data-ttu-id="07179-105">La fonction **glNormalPointer** définit un tableau de normales.</span><span class="sxs-lookup"><span data-stu-id="07179-105">The **glNormalPointer** function defines an array of normals.</span></span>

## <a name="syntax"></a><span data-ttu-id="07179-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="07179-106">Syntax</span></span>


```C++
void WINAPI glNormalPointer(
         GLenum  type,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a><span data-ttu-id="07179-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="07179-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07179-108">*type*</span><span class="sxs-lookup"><span data-stu-id="07179-108">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="07179-109">Type de données de chaque coordonnée dans le tableau à l’aide des constantes symboliques suivantes : GL \_ Byte, GL \_ short, GL \_ int, GL \_ float et GL \_ double.</span><span class="sxs-lookup"><span data-stu-id="07179-109">The data type of each coordinate in the array using the following symbolic constants: GL\_BYTE, GL\_SHORT, GL\_INT, GL\_FLOAT, and GL\_DOUBLE.</span></span>

</dd> <dt>

<span data-ttu-id="07179-110">*progrès*</span><span class="sxs-lookup"><span data-stu-id="07179-110">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="07179-111">Décalage d’octet entre les normales consécutives.</span><span class="sxs-lookup"><span data-stu-id="07179-111">The byte offset between consecutive normals.</span></span> <span data-ttu-id="07179-112">Lorsque la valeur de *Stride* est égale à zéro, les normales sont étroitement compressées dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="07179-112">When *stride* is zero, the normals are tightly packed in the array.</span></span>

</dd> <dt>

<span data-ttu-id="07179-113">*pointeur*</span><span class="sxs-lookup"><span data-stu-id="07179-113">*pointer*</span></span> 
</dt> <dd>

<span data-ttu-id="07179-114">Pointeur vers la première normale dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="07179-114">A pointer to the first normal in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07179-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="07179-115">Return value</span></span>

<span data-ttu-id="07179-116">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="07179-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="07179-117">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="07179-117">Error codes</span></span>

<span data-ttu-id="07179-118">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="07179-118">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="07179-119">Nom</span><span class="sxs-lookup"><span data-stu-id="07179-119">Name</span></span>                                                                                                  | <span data-ttu-id="07179-120">Signification</span><span class="sxs-lookup"><span data-stu-id="07179-120">Meaning</span></span>                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="07179-121"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="07179-121"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="07179-122">le *type* n’est pas une valeur acceptée.</span><span class="sxs-lookup"><span data-stu-id="07179-122">*type* was not an accepted value.</span></span><br/> |
| <dl> <span data-ttu-id="07179-123"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="07179-123"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="07179-124">*Stride* ou *Count* était négatif.</span><span class="sxs-lookup"><span data-stu-id="07179-124">*stride* or *count* was negative.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="07179-125">Notes</span><span class="sxs-lookup"><span data-stu-id="07179-125">Remarks</span></span>

<span data-ttu-id="07179-126">La fonction **glNormalPointer** spécifie l’emplacement et les données d’un tableau de normales à utiliser lors du rendu.</span><span class="sxs-lookup"><span data-stu-id="07179-126">The **glNormalPointer** function specifies the location and data of an array of normals to use when rendering.</span></span> <span data-ttu-id="07179-127">Le paramètre de *type* spécifie le type de données de chaque coordonnée normale.</span><span class="sxs-lookup"><span data-stu-id="07179-127">The *type* parameter specifies the data type of each normal coordinate.</span></span> <span data-ttu-id="07179-128">Le paramètre *Stride* détermine le décalage d’octets d’un perpendiculaire à l’autre, ce qui permet d’empaqueter des vertex et des attributs dans un tableau unique ou un stockage dans des tableaux séparés.</span><span class="sxs-lookup"><span data-stu-id="07179-128">The *stride* parameter determines the byte offset from one normal to the next, enabling the packing of vertices and attributes in a single array or storage in separate arrays.</span></span> <span data-ttu-id="07179-129">Dans certaines implémentations, le stockage des vertex et des attributs dans un tableau unique peut être plus efficace que l’utilisation de tableaux séparés. Pour plus d’informations, consultez [**glInterleavedArrays**](glinterleavedarrays.md) .</span><span class="sxs-lookup"><span data-stu-id="07179-129">In some implementations storing the vertices and attributes in a single array can be more efficient than using separate arrays; see [**glInterleavedArrays**](glinterleavedarrays.md) for details.</span></span>

<span data-ttu-id="07179-130">Un tableau normal est activé lorsque vous spécifiez la \_ \_ constante de tableau de la table normale GL avec [**glEnableClientState**](glenableclientstate.md).</span><span class="sxs-lookup"><span data-stu-id="07179-130">A normal array is enabled when you specify the GL\_NORMAL\_ARRAY constant with [**glEnableClientState**](glenableclientstate.md).</span></span> <span data-ttu-id="07179-131">Quand cette option est activée, [**glDrawArrays**](gldrawarrays.md), [**glDrawElements**](gldrawelements.md) et [**glArrayElement**](glarrayelement.md) utilisent le tableau normal.</span><span class="sxs-lookup"><span data-stu-id="07179-131">When enabled, [**glDrawArrays**](gldrawarrays.md), [**glDrawElements**](gldrawelements.md) and [**glArrayElement**](glarrayelement.md) use the normal array.</span></span> <span data-ttu-id="07179-132">Par défaut, le tableau normal est désactivé.</span><span class="sxs-lookup"><span data-stu-id="07179-132">By default the normal array is disabled.</span></span>

<span data-ttu-id="07179-133">Vous ne pouvez pas inclure des **glNormalPointer** dans des listes d’affichage.</span><span class="sxs-lookup"><span data-stu-id="07179-133">You cannot include **glNormalPointer** in display lists.</span></span>

<span data-ttu-id="07179-134">Lorsque vous spécifiez un tableau normal à l’aide de **glNormalPointer**, les valeurs de tous les paramètres de tableau normaux de la fonction sont enregistrées dans un État côté client.</span><span class="sxs-lookup"><span data-stu-id="07179-134">When you specify a normal array using **glNormalPointer**, the values of all the function's normal array parameters are saved in a client-side state.</span></span> <span data-ttu-id="07179-135">Étant donné que les paramètres de tableau normaux sont enregistrés dans un État côté client, leurs valeurs ne sont pas enregistrées ou restaurées par [**glPushAttrib**](glpushattrib.md) et [**glPopAttrib**](glpopattrib.md).</span><span class="sxs-lookup"><span data-stu-id="07179-135">Because the normal array parameters are saved in a client-side state, their values are not saved or restored by [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md).</span></span>

<span data-ttu-id="07179-136">Bien qu’aucune erreur ne soit générée lorsque vous appelez **glNormalPointer** dans des paires [**glBegin**](glbegin.md) et [**glEnd**](glend.md) , les résultats ne sont pas définis.</span><span class="sxs-lookup"><span data-stu-id="07179-136">Although no error is generated when you call **glNormalPointer** within [**glBegin**](glbegin.md) and [**glEnd**](glend.md) pairs, the results are undefined.</span></span>

<span data-ttu-id="07179-137">Les fonctions suivantes sont associées à **glNormalPointer**:</span><span class="sxs-lookup"><span data-stu-id="07179-137">The following functions are associated with **glNormalPointer**:</span></span>

<span data-ttu-id="07179-138">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ normal \_ tableau \_ Stride</span><span class="sxs-lookup"><span data-stu-id="07179-138">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_NORMAL\_ARRAY\_STRIDE</span></span>

<span data-ttu-id="07179-139">**glGet** avec argument GL- \_ nombre normal de \_ tableaux \_</span><span class="sxs-lookup"><span data-stu-id="07179-139">**glGet** with argument GL\_NORMAL\_ARRAY\_COUNT</span></span>

<span data-ttu-id="07179-140">**glGet** avec argument GL \_ - \_ type tableau normal \_</span><span class="sxs-lookup"><span data-stu-id="07179-140">**glGet** with argument GL\_NORMAL\_ARRAY\_TYPE</span></span>

<span data-ttu-id="07179-141">**glGetPointerv** avec argument GL \_ - \_ pointeur de tableau normal \_</span><span class="sxs-lookup"><span data-stu-id="07179-141">**glGetPointerv** with argument GL\_NORMAL\_ARRAY\_POINTER</span></span>

<span data-ttu-id="07179-142">[**glIsEnabled**](glisenabled.md) avec argument GL \_ - \_ tableau normal</span><span class="sxs-lookup"><span data-stu-id="07179-142">[**glIsEnabled**](glisenabled.md) with argument GL\_NORMAL\_ARRAY</span></span>

## <a name="requirements"></a><span data-ttu-id="07179-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="07179-143">Requirements</span></span>



| <span data-ttu-id="07179-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="07179-144">Requirement</span></span> | <span data-ttu-id="07179-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="07179-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="07179-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="07179-146">Minimum supported client</span></span><br/> | <span data-ttu-id="07179-147">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="07179-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="07179-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="07179-148">Minimum supported server</span></span><br/> | <span data-ttu-id="07179-149">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="07179-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="07179-150">En-tête</span><span class="sxs-lookup"><span data-stu-id="07179-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="07179-151"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="07179-151"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="07179-152">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="07179-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="07179-153"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="07179-153"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="07179-154">DLL</span><span class="sxs-lookup"><span data-stu-id="07179-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07179-155"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07179-155"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07179-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07179-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07179-157">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="07179-157">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="07179-158">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="07179-158">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="07179-159">**glDrawElements**</span><span class="sxs-lookup"><span data-stu-id="07179-159">**glDrawElements**</span></span>](gldrawelements.md)
</dt> <dt>

[<span data-ttu-id="07179-160">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="07179-160">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="07179-161">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="07179-161">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="07179-162">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="07179-162">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="07179-163">**glGetPointerv**</span><span class="sxs-lookup"><span data-stu-id="07179-163">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="07179-164">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="07179-164">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="07179-165">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="07179-165">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="07179-166">**glInterleavedArrays**</span><span class="sxs-lookup"><span data-stu-id="07179-166">**glInterleavedArrays**</span></span>](glinterleavedarrays.md)
</dt> <dt>

[<span data-ttu-id="07179-167">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="07179-167">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="07179-168">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="07179-168">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> <dt>

[<span data-ttu-id="07179-169">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="07179-169">**glGetString**</span></span>](glgetstring.md)
</dt> </dl>

 

 





