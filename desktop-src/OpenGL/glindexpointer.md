---
title: fonction glIndexPointer (GL. h)
description: La fonction glIndexPointer définit un tableau d’index de couleurs.
ms.assetid: b435d950-1f87-4041-93e4-f1f8786cabdb
keywords:
- glIndexPointer fonction OpenGL
topic_type:
- apiref
api_name:
- glIndexPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cca6858d7d1e3f13e4155bd40307a53b22e80a56
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464338"
---
# <a name="glindexpointer-function"></a><span data-ttu-id="f81b1-104">glIndexPointer fonction)</span><span class="sxs-lookup"><span data-stu-id="f81b1-104">glIndexPointer function</span></span>

<span data-ttu-id="f81b1-105">La fonction **glIndexPointer** définit un tableau d’index de couleurs.</span><span class="sxs-lookup"><span data-stu-id="f81b1-105">The **glIndexPointer** function defines an array of color indexes.</span></span>

## <a name="syntax"></a><span data-ttu-id="f81b1-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f81b1-106">Syntax</span></span>


```C++
void WINAPI glIndexPointer(
         GLenum  type,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a><span data-ttu-id="f81b1-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f81b1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f81b1-108">*type*</span><span class="sxs-lookup"><span data-stu-id="f81b1-108">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="f81b1-109">Type de données de chaque index de couleur dans le tableau à l’aide des constantes symboliques suivantes : GL \_ short, GL \_ int, GL \_ float, GL \_ double.</span><span class="sxs-lookup"><span data-stu-id="f81b1-109">The data type of each color index in the array using the following symbolic constants: GL\_SHORT, GL\_INT, GL\_FLOAT, GL\_DOUBLE.</span></span>

</dd> <dt>

<span data-ttu-id="f81b1-110">*progrès*</span><span class="sxs-lookup"><span data-stu-id="f81b1-110">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="f81b1-111">Décalage d’octet entre les index de couleurs consécutifs.</span><span class="sxs-lookup"><span data-stu-id="f81b1-111">The byte offset between consecutive color indexes.</span></span> <span data-ttu-id="f81b1-112">Lorsque la valeur de *Stride* est égale à zéro, les index de couleur sont fortement compressés dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="f81b1-112">When *stride* is zero, the color indexes are tightly packed in the array.</span></span>

</dd> <dt>

<span data-ttu-id="f81b1-113">*pointeur*</span><span class="sxs-lookup"><span data-stu-id="f81b1-113">*pointer*</span></span> 
</dt> <dd>

<span data-ttu-id="f81b1-114">Pointeur vers le premier index de couleur dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="f81b1-114">A pointer to the first color index in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f81b1-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f81b1-115">Return value</span></span>

<span data-ttu-id="f81b1-116">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="f81b1-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f81b1-117">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="f81b1-117">Error codes</span></span>

<span data-ttu-id="f81b1-118">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="f81b1-118">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="f81b1-119">Nom</span><span class="sxs-lookup"><span data-stu-id="f81b1-119">Name</span></span>                                                                                              | <span data-ttu-id="f81b1-120">Signification</span><span class="sxs-lookup"><span data-stu-id="f81b1-120">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="f81b1-121"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f81b1-121"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>  | <span data-ttu-id="f81b1-122">le *type* n’est pas une valeur acceptée.</span><span class="sxs-lookup"><span data-stu-id="f81b1-122">*type* was not an accepted value.</span></span><br/> |
| <dl> <span data-ttu-id="f81b1-123"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f81b1-123"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="f81b1-124">*Stride* ou *Count* était négatif.</span><span class="sxs-lookup"><span data-stu-id="f81b1-124">*stride* or *count* was negative.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f81b1-125">Notes</span><span class="sxs-lookup"><span data-stu-id="f81b1-125">Remarks</span></span>

<span data-ttu-id="f81b1-126">La fonction **glIndexPointer** spécifie l’emplacement et les données d’un tableau d’index de couleurs à utiliser lors du rendu.</span><span class="sxs-lookup"><span data-stu-id="f81b1-126">The **glIndexPointer** function specifies the location and data of an array of color indexes to use when rendering.</span></span> <span data-ttu-id="f81b1-127">Le paramètre de *type* spécifie le type de données de chaque index de couleur et *Stride* détermine le décalage d’octets d’un index de couleur à l’autre, ce qui permet de compresser les vertex et les attributs dans un tableau unique ou de stocker dans des tableaux séparés.</span><span class="sxs-lookup"><span data-stu-id="f81b1-127">The *type* parameter specifies the data type of each color index and *stride* determines the byte offset from one color index to the next, enabling the packing of vertices and attributes in a single array or storage in separate arrays.</span></span> <span data-ttu-id="f81b1-128">Dans certaines implémentations, le stockage des vertex et des attributs dans un tableau unique peut être plus efficace que l’utilisation de tableaux séparés.</span><span class="sxs-lookup"><span data-stu-id="f81b1-128">In some implementations, storing the vertices and attributes in a single array can be more efficient than using separate arrays.</span></span> <span data-ttu-id="f81b1-129">Pour plus d’informations, consultez [**glInterleavedArrays**](glinterleavedarrays.md).</span><span class="sxs-lookup"><span data-stu-id="f81b1-129">For more information, see [**glInterleavedArrays**](glinterleavedarrays.md).</span></span>

<span data-ttu-id="f81b1-130">Un tableau d’index de couleurs est activé lorsque vous spécifiez \_ la \_ constante de tableau d’index GL avec [**glEnableClientState**](glenableclientstate.md).</span><span class="sxs-lookup"><span data-stu-id="f81b1-130">A color-index array is enabled when you specify the GL\_INDEX\_ARRAY constant with [**glEnableClientState**](glenableclientstate.md).</span></span> <span data-ttu-id="f81b1-131">Quand cette option est activée, [**glDrawArrays**](gldrawarrays.md) et [**glArrayElement**](glarrayelement.md) utilisent le tableau d’index de couleurs.</span><span class="sxs-lookup"><span data-stu-id="f81b1-131">When enabled, [**glDrawArrays**](gldrawarrays.md) and [**glArrayElement**](glarrayelement.md) use the color-index array.</span></span> <span data-ttu-id="f81b1-132">Par défaut, le tableau d’index de couleurs est désactivé.</span><span class="sxs-lookup"><span data-stu-id="f81b1-132">By default the color-index array is disabled.</span></span>

<span data-ttu-id="f81b1-133">Vous ne pouvez pas inclure des **glIndexPointer** dans des listes d’affichage.</span><span class="sxs-lookup"><span data-stu-id="f81b1-133">You cannot include **glIndexPointer** in display lists.</span></span>

<span data-ttu-id="f81b1-134">Lorsque vous spécifiez un tableau d’index de couleurs à l’aide de **glIndexPointer**, les valeurs de tous les paramètres du tableau d’index de couleurs de la fonction sont enregistrées dans un État côté client et les éléments de tableau statique peuvent être mis en cache.</span><span class="sxs-lookup"><span data-stu-id="f81b1-134">When you specify a color-index array using **glIndexPointer**, the values of all the function's color-index array parameters are saved in a client-side state and static array elements can be cached.</span></span> <span data-ttu-id="f81b1-135">Étant donné que les paramètres de tableau d’index de couleurs sont un État côté client, leurs valeurs ne sont pas enregistrées ou restaurées par [**glPushAttrib**](glpushattrib.md) et **glPopAttrib**.</span><span class="sxs-lookup"><span data-stu-id="f81b1-135">Because the color-index array parameters are client-side state, their values are not saved or restored by [**glPushAttrib**](glpushattrib.md) and **glPopAttrib**.</span></span>

<span data-ttu-id="f81b1-136">Bien qu’aucune erreur ne soit générée lorsque vous appelez **glIndexPointer** dans des paires [**glBegin**](glbegin.md) et **glEnd** , les résultats ne sont pas définis.</span><span class="sxs-lookup"><span data-stu-id="f81b1-136">Although no error is generated when you call **glIndexPointer** within [**glBegin**](glbegin.md) and **glEnd** pairs, the results are undefined.</span></span>

<span data-ttu-id="f81b1-137">Les fonctions suivantes récupèrent les informations relatives à **glIndexPointer**:</span><span class="sxs-lookup"><span data-stu-id="f81b1-137">The following functions retrieve information related to **glIndexPointer**:</span></span>

<span data-ttu-id="f81b1-138">[**glIsEnabled**](glisenabled.md) avec argument \_ table d’index GL \_</span><span class="sxs-lookup"><span data-stu-id="f81b1-138">[**glIsEnabled**](glisenabled.md) with argument GL\_INDEX\_ARRAY</span></span>

<span data-ttu-id="f81b1-139">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ index \_ tableau \_ Stride</span><span class="sxs-lookup"><span data-stu-id="f81b1-139">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_INDEX\_ARRAY\_STRIDE</span></span>

<span data-ttu-id="f81b1-140">**glGet** avec argument \_ nombre de \_ tableaux d’index GL \_</span><span class="sxs-lookup"><span data-stu-id="f81b1-140">**glGet** with argument GL\_INDEX\_ARRAY\_COUNT</span></span>

<span data-ttu-id="f81b1-141">**glGet** avec argument \_ \_ type tableau d’index GL \_</span><span class="sxs-lookup"><span data-stu-id="f81b1-141">**glGet** with argument GL\_INDEX\_ARRAY\_TYPE</span></span>

<span data-ttu-id="f81b1-142">**glGet** avec argument \_ taille du \_ tableau d’index GL \_</span><span class="sxs-lookup"><span data-stu-id="f81b1-142">**glGet** with argument GL\_INDEX\_ARRAY\_SIZE</span></span>

<span data-ttu-id="f81b1-143">[**glGetPointerv**](glgetpointerv.md) avec argument, \_ \_ pointeur de tableau d’index GL \_</span><span class="sxs-lookup"><span data-stu-id="f81b1-143">[**glGetPointerv**](glgetpointerv.md) with argument GL\_INDEX\_ARRAY\_POINTER</span></span>

## <a name="requirements"></a><span data-ttu-id="f81b1-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f81b1-144">Requirements</span></span>



| <span data-ttu-id="f81b1-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f81b1-145">Requirement</span></span> | <span data-ttu-id="f81b1-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="f81b1-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f81b1-147">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f81b1-147">Minimum supported client</span></span><br/> | <span data-ttu-id="f81b1-148">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f81b1-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f81b1-149">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f81b1-149">Minimum supported server</span></span><br/> | <span data-ttu-id="f81b1-150">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f81b1-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f81b1-151">En-tête</span><span class="sxs-lookup"><span data-stu-id="f81b1-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="f81b1-152"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="f81b1-152"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="f81b1-153">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f81b1-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="f81b1-154"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f81b1-154"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f81b1-155">DLL</span><span class="sxs-lookup"><span data-stu-id="f81b1-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f81b1-156"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f81b1-156"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f81b1-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f81b1-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f81b1-158">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="f81b1-158">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="f81b1-159">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="f81b1-159">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="f81b1-160">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="f81b1-160">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="f81b1-161">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="f81b1-161">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="f81b1-162">**glGetPointerv**</span><span class="sxs-lookup"><span data-stu-id="f81b1-162">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="f81b1-163">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="f81b1-163">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="f81b1-164">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="f81b1-164">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="f81b1-165">**glPushAttrib**</span><span class="sxs-lookup"><span data-stu-id="f81b1-165">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="f81b1-166">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="f81b1-166">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="f81b1-167">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="f81b1-167">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





