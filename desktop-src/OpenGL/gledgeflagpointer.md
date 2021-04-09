---
title: fonction glEdgeFlagPointer (GL. h)
description: La fonction glEdgeFlagPointer définit un tableau d’indicateurs de bord.
ms.assetid: e0e7e442-533d-4c41-addd-a215ce0b1c56
keywords:
- glEdgeFlagPointer fonction OpenGL
topic_type:
- apiref
api_name:
- glEdgeFlagPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4390a9838fef418763aa4bcafbf815ab0cdf3466
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742205"
---
# <a name="gledgeflagpointer-function"></a><span data-ttu-id="71464-104">glEdgeFlagPointer fonction)</span><span class="sxs-lookup"><span data-stu-id="71464-104">glEdgeFlagPointer function</span></span>

<span data-ttu-id="71464-105">La fonction **glEdgeFlagPointer** définit un tableau d’indicateurs de bord.</span><span class="sxs-lookup"><span data-stu-id="71464-105">The **glEdgeFlagPointer** function defines an array of edge flags.</span></span>

## <a name="syntax"></a><span data-ttu-id="71464-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="71464-106">Syntax</span></span>


```C++
void WINAPI glEdgeFlagPointer(
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a><span data-ttu-id="71464-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="71464-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71464-108">*progrès*</span><span class="sxs-lookup"><span data-stu-id="71464-108">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="71464-109">Décalage d’octet entre les indicateurs de bord consécutifs.</span><span class="sxs-lookup"><span data-stu-id="71464-109">The byte offset between consecutive edge flags.</span></span> <span data-ttu-id="71464-110">Lorsque la valeur de *Stride* est égale à zéro, les indicateurs de périphérie sont étroitement empaquetés dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="71464-110">When *stride* is zero, the edge flags are tightly packed in the array.</span></span>

</dd> <dt>

<span data-ttu-id="71464-111">*pointeur*</span><span class="sxs-lookup"><span data-stu-id="71464-111">*pointer*</span></span> 
</dt> <dd>

<span data-ttu-id="71464-112">Pointeur vers le premier indicateur de bord dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="71464-112">A pointer to the first edge flag in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71464-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="71464-113">Return value</span></span>

<span data-ttu-id="71464-114">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="71464-114">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="71464-115">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="71464-115">Error codes</span></span>

<span data-ttu-id="71464-116">Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="71464-116">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="71464-117">Nom</span><span class="sxs-lookup"><span data-stu-id="71464-117">Name</span></span>                                                                                             | <span data-ttu-id="71464-118">Signification</span><span class="sxs-lookup"><span data-stu-id="71464-118">Meaning</span></span>                                      |
|--------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="71464-119"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="71464-119"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl> | <span data-ttu-id="71464-120">*Stride* ou *Count* était négatif.</span><span class="sxs-lookup"><span data-stu-id="71464-120">*stride* or *count* was negative.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="71464-121">Notes</span><span class="sxs-lookup"><span data-stu-id="71464-121">Remarks</span></span>

<span data-ttu-id="71464-122">La fonction **glEdgeFlagPointer** spécifie l’emplacement et les données d’un tableau d’indicateurs de bord booléen à utiliser lors du rendu.</span><span class="sxs-lookup"><span data-stu-id="71464-122">The **glEdgeFlagPointer** function specifies the location and data of an array of Boolean edge flags to use when rendering.</span></span> <span data-ttu-id="71464-123">Le paramètre *Stride* détermine le décalage d’octets d’un indicateur de bord à l’autre, ce qui permet d’empaqueter des vertex et des attributs dans un tableau unique ou un stockage dans des tableaux séparés.</span><span class="sxs-lookup"><span data-stu-id="71464-123">The *stride* parameter determines the byte offset from one edge flag to the next, which enables the packing of vertices and attributes in a single array or storage in separate arrays.</span></span> <span data-ttu-id="71464-124">Dans certaines implémentations, le stockage des vertex et des attributs dans un tableau unique peut être plus efficace que l’utilisation de tableaux séparés.</span><span class="sxs-lookup"><span data-stu-id="71464-124">In some implementations, storing the vertices and attributes in a single array can be more efficient than using separate arrays.</span></span>

<span data-ttu-id="71464-125">Un tableau d’indicateurs de bord est activé quand vous spécifiez \_ la \_ \_ constante de tableau d’indicateurs de périphérie GL avec [**glEnableClientState**](glenableclientstate.md).</span><span class="sxs-lookup"><span data-stu-id="71464-125">An edge-flag array is enabled when you specify the GL\_EDGE\_FLAG\_ARRAY constant with [**glEnableClientState**](glenableclientstate.md).</span></span> <span data-ttu-id="71464-126">Quand cette option est activée, [**glDrawArrays**](gldrawarrays.md) ou [**glArrayElement**](glarrayelement.md) utilise le tableau d’indicateurs de bord.</span><span class="sxs-lookup"><span data-stu-id="71464-126">When enabled, [**glDrawArrays**](gldrawarrays.md) or [**glArrayElement**](glarrayelement.md) uses the edge-flag array.</span></span> <span data-ttu-id="71464-127">Par défaut, le tableau d’indicateurs de bord est désactivé.</span><span class="sxs-lookup"><span data-stu-id="71464-127">By default the edge-flag array is disabled.</span></span>

<span data-ttu-id="71464-128">Utilisez **glDrawArrays** pour construire une séquence de primitives (du même type) à partir de tableaux d’attributs vertex et vertex prédéfinis.</span><span class="sxs-lookup"><span data-stu-id="71464-128">Use **glDrawArrays** to construct a sequence of primitives (all of the same type) from prespecified vertex and vertex attribute arrays.</span></span> <span data-ttu-id="71464-129">Utilisez **glArrayElement** pour spécifier des primitives en indexant des vertex et des attributs de vertex, et [**glDrawElements**](gldrawelements.md) pour construire une séquence de primitives en indexant des vertex et des attributs de vertex.</span><span class="sxs-lookup"><span data-stu-id="71464-129">Use **glArrayElement** to specify primitives by indexing vertices and vertex attributes, and [**glDrawElements**](gldrawelements.md) to construct a sequence of primitives by indexing vertices and vertex attributes.</span></span>

<span data-ttu-id="71464-130">Vous ne pouvez pas inclure des **glEdgeFlagPointer** dans des listes d’affichage.</span><span class="sxs-lookup"><span data-stu-id="71464-130">You cannot include **glEdgeFlagPointer** in display lists.</span></span>

<span data-ttu-id="71464-131">Lorsque vous spécifiez un tableau d’indicateurs de bord à l’aide de **glEdgeFlagPointer**, les valeurs de tous les paramètres de tableau de l’indicateur de bord de la fonction sont enregistrées dans un État côté client et les éléments de tableau statique peuvent être mis en cache.</span><span class="sxs-lookup"><span data-stu-id="71464-131">When you specify an edge-flag array using **glEdgeFlagPointer**, the values of all the function's edge-flag array parameters are saved in a client-side state and static array elements can be cached.</span></span> <span data-ttu-id="71464-132">Étant donné que les paramètres de tableau de l’indicateur de bord sont dans un État côté client, [**glPushAttrib**](glpushattrib.md) et [**glPopAttrib**](glpopattrib.md) n’enregistrent ni ne restaurent leurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="71464-132">Because the edge-flag array parameters are in a client-side state, [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md) do not save or restore their values.</span></span>

<span data-ttu-id="71464-133">Bien que l’appel de **glEdgeFlagPointer** dans une paire de [](glbegin.md) / [**Glend**](glend.md) glBegin ne génère pas d’erreur, les résultats ne sont pas définis.</span><span class="sxs-lookup"><span data-stu-id="71464-133">Although calling **glEdgeFlagPointer** within a [**glBegin**](glbegin.md)/[**glend**](glend.md) pair does not generate an error, the results are undefined.</span></span>

<span data-ttu-id="71464-134">Les fonctions suivantes récupèrent les informations relatives à la fonction **glEdgeFlagPointer** :</span><span class="sxs-lookup"><span data-stu-id="71464-134">The following functions retrieve information related to the **glEdgeFlagPointer** function:</span></span>

<span data-ttu-id="71464-135">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Edge \_ indicateur \_ tableau \_ Stride</span><span class="sxs-lookup"><span data-stu-id="71464-135">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_EDGE\_FLAG\_ARRAY\_STRIDE</span></span>

<span data-ttu-id="71464-136">**glGet** avec argument valeur de tableau de l' \_ \_ indicateur de périphérie du \_ GL \_</span><span class="sxs-lookup"><span data-stu-id="71464-136">**glGet** with argument GL\_EDGE\_FLAG\_ARRAY\_COUNT</span></span>

<span data-ttu-id="71464-137">[**glGetPointerv**](glgetpointerv.md) avec argument du \_ pointeur de tableau de l’indicateur de bord GL \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="71464-137">[**glGetPointerv**](glgetpointerv.md) with argument GL\_EDGE\_FLAG\_ARRAY\_POINTER</span></span>

<span data-ttu-id="71464-138">[**glIsEnabled**](glisenabled.md) avec argument du \_ \_ tableau d’indicateurs de périphérie du GL \_</span><span class="sxs-lookup"><span data-stu-id="71464-138">[**glIsEnabled**](glisenabled.md) with argument GL\_EDGE\_FLAG\_ARRAY</span></span>

## <a name="requirements"></a><span data-ttu-id="71464-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="71464-139">Requirements</span></span>



| <span data-ttu-id="71464-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="71464-140">Requirement</span></span> | <span data-ttu-id="71464-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="71464-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="71464-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71464-142">Minimum supported client</span></span><br/> | <span data-ttu-id="71464-143">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="71464-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="71464-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71464-144">Minimum supported server</span></span><br/> | <span data-ttu-id="71464-145">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="71464-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="71464-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="71464-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="71464-147"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="71464-147"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="71464-148">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="71464-148">Library</span></span><br/>                  | <dl> <span data-ttu-id="71464-149"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="71464-149"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="71464-150">DLL</span><span class="sxs-lookup"><span data-stu-id="71464-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71464-151"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71464-151"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71464-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71464-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71464-153">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="71464-153">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="71464-154">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="71464-154">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="71464-155">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="71464-155">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="71464-156">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="71464-156">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="71464-157">**glEnableClientState**</span><span class="sxs-lookup"><span data-stu-id="71464-157">**glEnableClientState**</span></span>](glenableclientstate.md)
</dt> <dt>

[<span data-ttu-id="71464-158">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="71464-158">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="71464-159">**glGet**</span><span class="sxs-lookup"><span data-stu-id="71464-159">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="71464-160">**glGetPointerv**</span><span class="sxs-lookup"><span data-stu-id="71464-160">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="71464-161">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="71464-161">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="71464-162">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="71464-162">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="71464-163">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="71464-163">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="71464-164">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="71464-164">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="71464-165">**glPopAttrib**</span><span class="sxs-lookup"><span data-stu-id="71464-165">**glPopAttrib**</span></span>](glpopattrib.md)
</dt> <dt>

[<span data-ttu-id="71464-166">**glPushAttrib**</span><span class="sxs-lookup"><span data-stu-id="71464-166">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="71464-167">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="71464-167">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="71464-168">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="71464-168">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





