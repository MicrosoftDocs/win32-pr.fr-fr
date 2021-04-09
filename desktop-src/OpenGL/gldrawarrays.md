---
title: fonction glDrawArrays (GL. h)
description: La fonction glDrawArrays spécifie plusieurs primitives à restituer.
ms.assetid: 6ebd467b-5a63-43e4-b3fd-242c704d7d13
keywords:
- glDrawArrays fonction OpenGL
topic_type:
- apiref
api_name:
- glDrawArrays
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88b20cf3a3e3b2c96a8172f53f8126815efe16d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942260"
---
# <a name="gldrawarrays-function"></a><span data-ttu-id="55b19-104">glDrawArrays fonction)</span><span class="sxs-lookup"><span data-stu-id="55b19-104">glDrawArrays function</span></span>

<span data-ttu-id="55b19-105">La fonction **glDrawArrays** spécifie plusieurs primitives à restituer.</span><span class="sxs-lookup"><span data-stu-id="55b19-105">The **glDrawArrays** function specifies multiple primitives to render.</span></span>

## <a name="syntax"></a><span data-ttu-id="55b19-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="55b19-106">Syntax</span></span>


```C++
void WINAPI glDrawArrays(
   GLenum  mode,
   GLint   first,
   GLsizei count
);
```



## <a name="parameters"></a><span data-ttu-id="55b19-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="55b19-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55b19-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="55b19-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="55b19-109">Type de primitives à restituer.</span><span class="sxs-lookup"><span data-stu-id="55b19-109">The kind of primitives to render.</span></span> <span data-ttu-id="55b19-110">Les constantes suivantes spécifient des types de primitives acceptables : les points de GL, le quadrillage de \_ \_ ligne GL, le \_ \_ \_ Bouclage de ligne GL, les \_ lignes de GL, la \_ bande triangulaire GL \_ , le ventilateur de \_ \_ triangle GL, \_ les triangles GL, le GL \_ Quad \_ Strip, \_ les quads GL et le \_ polygone GL.</span><span class="sxs-lookup"><span data-stu-id="55b19-110">The following constants specify acceptable types of primitives: GL\_POINTS, GL\_LINE\_STRIP, GL\_LINE\_LOOP, GL\_LINES, GL\_TRIANGLE\_STRIP, GL\_TRIANGLE\_FAN, GL\_TRIANGLES, GL\_QUAD\_STRIP, GL\_QUADS, and GL\_POLYGON.</span></span>

</dd> <dt>

<span data-ttu-id="55b19-111">*first*</span><span class="sxs-lookup"><span data-stu-id="55b19-111">*first*</span></span> 
</dt> <dd>

<span data-ttu-id="55b19-112">Index de départ dans les tableaux activés.</span><span class="sxs-lookup"><span data-stu-id="55b19-112">The starting index in the enabled arrays.</span></span>

</dd> <dt>

<span data-ttu-id="55b19-113">*count*</span><span class="sxs-lookup"><span data-stu-id="55b19-113">*count*</span></span> 
</dt> <dd>

<span data-ttu-id="55b19-114">Nombre d’index à restituer.</span><span class="sxs-lookup"><span data-stu-id="55b19-114">The number of indexes to render.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55b19-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="55b19-115">Return value</span></span>

<span data-ttu-id="55b19-116">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="55b19-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="55b19-117">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="55b19-117">Error codes</span></span>

<span data-ttu-id="55b19-118">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="55b19-118">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="55b19-119">Nom</span><span class="sxs-lookup"><span data-stu-id="55b19-119">Name</span></span>                                                                                                  | <span data-ttu-id="55b19-120">Signification</span><span class="sxs-lookup"><span data-stu-id="55b19-120">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="55b19-121"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="55b19-121"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="55b19-122">le *nombre* était négatif.</span><span class="sxs-lookup"><span data-stu-id="55b19-122">*count* was negative.</span></span><br/>                                                                                                      |
| <dl> <span data-ttu-id="55b19-123"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="55b19-123"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="55b19-124">le *mode* n’était pas une valeur acceptée.</span><span class="sxs-lookup"><span data-stu-id="55b19-124">*mode* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="55b19-125"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="55b19-125"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="55b19-126">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="55b19-126">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="55b19-127">Notes</span><span class="sxs-lookup"><span data-stu-id="55b19-127">Remarks</span></span>

<span data-ttu-id="55b19-128">Avec **glDrawArrays**, vous pouvez spécifier plusieurs primitives géométriques à restituer.</span><span class="sxs-lookup"><span data-stu-id="55b19-128">With **glDrawArrays**, you can specify multiple geometric primitives to render.</span></span> <span data-ttu-id="55b19-129">Au lieu d’appeler des fonctions OpenGL distinctes pour passer chaque vertex, normal ou couleur individuel, vous pouvez spécifier des tableaux distincts de vertex, de normales et de couleurs pour définir une séquence de primitives (le même type) avec un appel unique à **glDrawArrays**.</span><span class="sxs-lookup"><span data-stu-id="55b19-129">Instead of calling separate OpenGL functions to pass each individual vertex, normal, or color, you can specify separate arrays of vertices, normals, and colors to define a sequence of primitives (all the same kind) with a single call to **glDrawArrays**.</span></span>

<span data-ttu-id="55b19-130">Quand vous appelez **glDrawArrays**, le *nombre* d’éléments séquentiels de chaque tableau activé est utilisé pour construire une séquence de primitives géométriques, en commençant par le *premier* élément.</span><span class="sxs-lookup"><span data-stu-id="55b19-130">When you call **glDrawArrays**, *count* sequential elements from each enabled array are used to construct a sequence of geometric primitives, beginning with the *first* element.</span></span> <span data-ttu-id="55b19-131">Le paramètre *mode* spécifie le type de primitive à construire et comment utiliser les éléments de tableau pour construire les primitives.</span><span class="sxs-lookup"><span data-stu-id="55b19-131">The *mode* parameter specifies what kind of primitive to construct and how to use the array elements to construct the primitives.</span></span>

<span data-ttu-id="55b19-132">Une fois **glDrawArrays** retourné, les valeurs des attributs vertex modifiés par **glDrawArrays** ne sont pas définies.</span><span class="sxs-lookup"><span data-stu-id="55b19-132">After **glDrawArrays** returns, the values of vertex attributes that are modified by **glDrawArrays** are undefined.</span></span> <span data-ttu-id="55b19-133">Par exemple, si le \_ tableau de couleurs GL \_ est activé, la valeur de la couleur actuelle est non définie après le retour de **glDrawArrays** .</span><span class="sxs-lookup"><span data-stu-id="55b19-133">For example, if GL\_COLOR\_ARRAY is enabled, the value of the current color is undefined after **glDrawArrays** returns.</span></span> <span data-ttu-id="55b19-134">Les attributs non modifiés par **glDrawArrays** restent définis.</span><span class="sxs-lookup"><span data-stu-id="55b19-134">Attributes not modified by **glDrawArrays** remain defined.</span></span> <span data-ttu-id="55b19-135">Lorsque \_ \_ le tableau de vertex GL n’est pas activé, aucune primitive géométrique n’est générée, mais les attributs correspondant aux tableaux activés sont modifiés.</span><span class="sxs-lookup"><span data-stu-id="55b19-135">When GL\_VERTEX\_ARRAY is not enabled, no geometric primitives are generated but the attributes corresponding to enabled arrays are modified.</span></span>

<span data-ttu-id="55b19-136">Vous pouvez inclure des **glDrawArrays** dans des listes d’affichage.</span><span class="sxs-lookup"><span data-stu-id="55b19-136">You can include **glDrawArrays** in display lists.</span></span> <span data-ttu-id="55b19-137">Lorsque vous incluez **glDrawArrays** dans une liste d’affichage, les données de tableau nécessaires, déterminées par les pointeurs de tableau et les activent, sont générées et entrées dans la liste d’affichage.</span><span class="sxs-lookup"><span data-stu-id="55b19-137">When you include **glDrawArrays** in a display list, the necessary array data, determined by the array pointers and the enables, are generated and entered in the display list.</span></span> <span data-ttu-id="55b19-138">Les valeurs des pointeurs de tableau et des activations sont déterminées lors de la création de listes d’affichage.</span><span class="sxs-lookup"><span data-stu-id="55b19-138">The values of array pointers and enables are determined during the creation of display lists.</span></span>

<span data-ttu-id="55b19-139">Vous pouvez lire les données du tableau statique à tout moment.</span><span class="sxs-lookup"><span data-stu-id="55b19-139">You can read static array data at any time.</span></span> <span data-ttu-id="55b19-140">Si des éléments de tableau statique sont modifiés et que le tableau n’est pas spécifié de nouveau, les résultats de tous les appels suivants à **glDrawArrays** ne sont pas définis.</span><span class="sxs-lookup"><span data-stu-id="55b19-140">If any static array elements are modified and the array is not specified again, the results of any subsequent calls to **glDrawArrays** are undefined.</span></span>

<span data-ttu-id="55b19-141">Bien qu’aucune erreur ne soit générée lorsque vous spécifiez un tableau plusieurs fois dans les paires [**glBegin**](glbegin.md) et [**Glend**](glend.md) , les résultats ne sont pas définis.</span><span class="sxs-lookup"><span data-stu-id="55b19-141">Although no error is generated when you specify an array more than once within [**glBegin**](glbegin.md) and [**glend**](glend.md) pairs, the results are undefined.</span></span>

## <a name="requirements"></a><span data-ttu-id="55b19-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="55b19-142">Requirements</span></span>



| <span data-ttu-id="55b19-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="55b19-143">Requirement</span></span> | <span data-ttu-id="55b19-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="55b19-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="55b19-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="55b19-145">Minimum supported client</span></span><br/> | <span data-ttu-id="55b19-146">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="55b19-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="55b19-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="55b19-147">Minimum supported server</span></span><br/> | <span data-ttu-id="55b19-148">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="55b19-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="55b19-149">En-tête</span><span class="sxs-lookup"><span data-stu-id="55b19-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="55b19-150"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="55b19-150"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="55b19-151">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="55b19-151">Library</span></span><br/>                  | <dl> <span data-ttu-id="55b19-152"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="55b19-152"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="55b19-153">DLL</span><span class="sxs-lookup"><span data-stu-id="55b19-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55b19-154"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55b19-154"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55b19-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="55b19-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55b19-156">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="55b19-156">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="55b19-157">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="55b19-157">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="55b19-158">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="55b19-158">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="55b19-159">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="55b19-159">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="55b19-160">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="55b19-160">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="55b19-161">**glGetPointerv**</span><span class="sxs-lookup"><span data-stu-id="55b19-161">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="55b19-162">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="55b19-162">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="55b19-163">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="55b19-163">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="55b19-164">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="55b19-164">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="55b19-165">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="55b19-165">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="55b19-166">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="55b19-166">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





