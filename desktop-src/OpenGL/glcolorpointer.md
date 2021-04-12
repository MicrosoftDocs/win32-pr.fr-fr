---
title: fonction glColorPointer (GL. h)
description: La fonction glColorPointer définit un tableau de couleurs.
ms.assetid: 4d9d05fb-691d-4b71-b079-c42dc7103055
keywords:
- glColorPointer fonction OpenGL
topic_type:
- apiref
api_name:
- glColorPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9abced52f0d0664e998ad8380e33d43d4af36bcc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464727"
---
# <a name="glcolorpointer-function"></a><span data-ttu-id="d0311-104">glColorPointer fonction)</span><span class="sxs-lookup"><span data-stu-id="d0311-104">glColorPointer function</span></span>

<span data-ttu-id="d0311-105">La fonction **glColorPointer** définit un tableau de couleurs.</span><span class="sxs-lookup"><span data-stu-id="d0311-105">The **glColorPointer** function defines an array of colors.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0311-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d0311-106">Syntax</span></span>


```C++
void WINAPI glColorPointer(
         GLint   size,
         GLenum  type,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a><span data-ttu-id="d0311-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d0311-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0311-108">*size*</span><span class="sxs-lookup"><span data-stu-id="d0311-108">*size*</span></span> 
</dt> <dd>

<span data-ttu-id="d0311-109">Nombre de composants par couleur.</span><span class="sxs-lookup"><span data-stu-id="d0311-109">The number of components per color.</span></span> <span data-ttu-id="d0311-110">La valeur doit être 3 ou 4.</span><span class="sxs-lookup"><span data-stu-id="d0311-110">The value must be either 3 or 4.</span></span>

</dd> <dt>

<span data-ttu-id="d0311-111">*type*</span><span class="sxs-lookup"><span data-stu-id="d0311-111">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="d0311-112">Type de données de chaque composant de couleur dans un tableau de couleurs.</span><span class="sxs-lookup"><span data-stu-id="d0311-112">The data type of each color component in a color array.</span></span> <span data-ttu-id="d0311-113">Les types de données acceptables sont spécifiés avec les constantes suivantes : GL \_ Byte, GL \_ unsigned \_ Byte, GL \_ short, GL \_ unsigned \_ short, GL \_ int, GL \_ unsigned \_ int, GL \_ float ou GL \_ double.</span><span class="sxs-lookup"><span data-stu-id="d0311-113">Acceptable data types are specified with the following constants: GL\_BYTE, GL\_UNSIGNED\_BYTE, GL\_SHORT, GL\_UNSIGNED\_SHORT, GL\_INT, GL\_UNSIGNED\_INT, GL\_FLOAT, or GL\_DOUBLE.</span></span>

</dd> <dt>

<span data-ttu-id="d0311-114">*progrès*</span><span class="sxs-lookup"><span data-stu-id="d0311-114">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="d0311-115">Décalage d’octet entre les couleurs consécutives.</span><span class="sxs-lookup"><span data-stu-id="d0311-115">The byte offset between consecutive colors.</span></span> <span data-ttu-id="d0311-116">Quand *Stride* est égal à zéro, les couleurs sont étroitement compressées dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="d0311-116">When *stride* is zero, the colors are tightly packed in the array.</span></span>

</dd> <dt>

<span data-ttu-id="d0311-117">*pointeur*</span><span class="sxs-lookup"><span data-stu-id="d0311-117">*pointer*</span></span> 
</dt> <dd>

<span data-ttu-id="d0311-118">Pointeur vers le premier composant du premier élément de couleur dans un tableau de couleurs.</span><span class="sxs-lookup"><span data-stu-id="d0311-118">A pointer to the first component of the first color element in a color array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0311-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d0311-119">Return value</span></span>

<span data-ttu-id="d0311-120">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="d0311-120">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d0311-121">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="d0311-121">Error codes</span></span>

<span data-ttu-id="d0311-122">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="d0311-122">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="d0311-123">Nom</span><span class="sxs-lookup"><span data-stu-id="d0311-123">Name</span></span>                                                                                              | <span data-ttu-id="d0311-124">Signification</span><span class="sxs-lookup"><span data-stu-id="d0311-124">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="d0311-125"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d0311-125"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="d0311-126">la *taille* n’est pas 3 ou 4.</span><span class="sxs-lookup"><span data-stu-id="d0311-126">*size* was not 3 or 4.</span></span><br/>            |
| <dl> <span data-ttu-id="d0311-127"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d0311-127"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>  | <span data-ttu-id="d0311-128">le *type* n’est pas une valeur acceptée.</span><span class="sxs-lookup"><span data-stu-id="d0311-128">*type* was not an accepted value.</span></span><br/> |
| <dl> <span data-ttu-id="d0311-129"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d0311-129"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="d0311-130">*Stride* ou *Count* était négatif.</span><span class="sxs-lookup"><span data-stu-id="d0311-130">*stride* or *count* was negative.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d0311-131">Notes</span><span class="sxs-lookup"><span data-stu-id="d0311-131">Remarks</span></span>

<span data-ttu-id="d0311-132">La fonction **glColorPointer** spécifie l’emplacement et le format de données d’un tableau de composants de couleur à utiliser lors du rendu.</span><span class="sxs-lookup"><span data-stu-id="d0311-132">The **glColorPointer** function specifies the location and data format of an array of color components to use when rendering.</span></span> <span data-ttu-id="d0311-133">Le paramètre *Stride* détermine le décalage d’octets d’une couleur à l’autre, ce qui permet de compresser des attributs vertex dans un tableau unique ou un stockage dans des tableaux séparés.</span><span class="sxs-lookup"><span data-stu-id="d0311-133">The *stride* parameter determines the byte offset from one color to the next, enabling the packing of vertex attributes in a single array or storage in separate arrays.</span></span> <span data-ttu-id="d0311-134">Dans certaines implémentations, le stockage des attributs de vertex dans un tableau unique peut être plus efficace que l’utilisation de tableaux séparés.</span><span class="sxs-lookup"><span data-stu-id="d0311-134">In some implementations, storing vertex attributes in a single array can be more efficient than the use of separate arrays.</span></span>

<span data-ttu-id="d0311-135">Activez le tableau de couleurs en spécifiant \_ la \_ constante de tableau de couleur GL avec [**glEnableClientState**](glenableclientstate.md).</span><span class="sxs-lookup"><span data-stu-id="d0311-135">Enabled the color array by specifying the GL\_COLOR\_ARRAY constant with [**glEnableClientState**](glenableclientstate.md).</span></span> <span data-ttu-id="d0311-136">L’appel de [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)ou [**glDrawArrays**](gldrawarrays.md) utilise le tableau de couleurs qui est donc activé.</span><span class="sxs-lookup"><span data-stu-id="d0311-136">Calling [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md) uses the color array that is thus enabled.</span></span> <span data-ttu-id="d0311-137">Par défaut, le tableau de couleurs est désactivé.</span><span class="sxs-lookup"><span data-stu-id="d0311-137">By default, the color array is disabled.</span></span> <span data-ttu-id="d0311-138">Les appels **glColorPointer** ne peuvent pas être entrés dans les listes d’affichage.</span><span class="sxs-lookup"><span data-stu-id="d0311-138">The **glColorPointer** calls cannot by entered in display lists.</span></span>

<span data-ttu-id="d0311-139">Lorsque vous spécifiez un tableau de couleurs à l’aide de **glColorPointer**, les valeurs de tous les paramètres du tableau de couleurs de la fonction sont enregistrées dans un État côté client et vous pouvez mettre en cache des éléments de tableau statique.</span><span class="sxs-lookup"><span data-stu-id="d0311-139">When you specify a color array using **glColorPointer**, the values of all the function's color array parameters are saved in a client-side state, and you can cache static array elements.</span></span> <span data-ttu-id="d0311-140">Étant donné que les paramètres du tableau de couleurs sont dans un État côté client, [**glPushAttrib**](glpushattrib.md) et [**glPopAttrib**](glpopattrib.md) n’enregistrent ni ne restaurent les valeurs des paramètres.</span><span class="sxs-lookup"><span data-stu-id="d0311-140">Because the color array parameters are in a client-side state, [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md) do not save or restore the parameters' values.</span></span>

<span data-ttu-id="d0311-141">Bien que la spécification du tableau de couleurs dans les paires [**glBegin**](glbegin.md) et [**Glend**](glend.md) ne génère pas d’erreur, les résultats ne sont pas définis.</span><span class="sxs-lookup"><span data-stu-id="d0311-141">Although specifying the color array within [**glBegin**](glbegin.md) and [**glend**](glend.md) pairs does not generate an error, the results are undefined.</span></span>

<span data-ttu-id="d0311-142">Les fonctions suivantes récupèrent les informations relatives à la fonction **glColorPointer** :</span><span class="sxs-lookup"><span data-stu-id="d0311-142">The following functions retrieve information related to the **glColorPointer** function:</span></span>

<span data-ttu-id="d0311-143">[**glIsEnabled**](glisenabled.md) avec argument de \_ tableau de couleur de GL \_</span><span class="sxs-lookup"><span data-stu-id="d0311-143">[**glIsEnabled**](glisenabled.md) with argument GL\_COLOR\_ARRAY</span></span>

<span data-ttu-id="d0311-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ \_ taille de tableau de couleurs \_</span><span class="sxs-lookup"><span data-stu-id="d0311-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_COLOR\_ARRAY\_SIZE</span></span>

<span data-ttu-id="d0311-145">**glGet** avec argument GL \_ couleur \_ de \_ type tableau</span><span class="sxs-lookup"><span data-stu-id="d0311-145">**glGet** with argument GL\_COLOR\_ARRAY\_TYPE</span></span>

<span data-ttu-id="d0311-146">**glGet** avec argument GL \_ tableau des couleurs \_ \_ Stride</span><span class="sxs-lookup"><span data-stu-id="d0311-146">**glGet** with argument GL\_COLOR\_ARRAY\_STRIDE</span></span>

<span data-ttu-id="d0311-147">**glGet** avec argument \_ nombre de \_ MATRICEs de couleurs GL \_</span><span class="sxs-lookup"><span data-stu-id="d0311-147">**glGet** with argument GL\_COLOR\_ARRAY\_COUNT</span></span>

<span data-ttu-id="d0311-148">[**glGetPointerv**](glgetpointerv.md) avec argument, \_ \_ pointeur de tableau de couleur de GL \_</span><span class="sxs-lookup"><span data-stu-id="d0311-148">[**glGetPointerv**](glgetpointerv.md) with argument GL\_COLOR\_ARRAY\_POINTER</span></span>

## <a name="requirements"></a><span data-ttu-id="d0311-149">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d0311-149">Requirements</span></span>



| <span data-ttu-id="d0311-150">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d0311-150">Requirement</span></span> | <span data-ttu-id="d0311-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="d0311-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0311-152">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d0311-152">Minimum supported client</span></span><br/> | <span data-ttu-id="d0311-153">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d0311-153">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d0311-154">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d0311-154">Minimum supported server</span></span><br/> | <span data-ttu-id="d0311-155">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d0311-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d0311-156">En-tête</span><span class="sxs-lookup"><span data-stu-id="d0311-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0311-157"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0311-157"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="d0311-158">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d0311-158">Library</span></span><br/>                  | <dl> <span data-ttu-id="d0311-159"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d0311-159"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="d0311-160">DLL</span><span class="sxs-lookup"><span data-stu-id="d0311-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0311-161"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0311-161"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0311-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d0311-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0311-163">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="d0311-163">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="d0311-164">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="d0311-164">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="d0311-165">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="d0311-165">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="d0311-166">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="d0311-166">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="d0311-167">**glEnableClientState**</span><span class="sxs-lookup"><span data-stu-id="d0311-167">**glEnableClientState**</span></span>](glenableclientstate.md)
</dt> <dt>

[<span data-ttu-id="d0311-168">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="d0311-168">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="d0311-169">**glGet**</span><span class="sxs-lookup"><span data-stu-id="d0311-169">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="d0311-170">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="d0311-170">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="d0311-171">**glGetPointerv**</span><span class="sxs-lookup"><span data-stu-id="d0311-171">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="d0311-172">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="d0311-172">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="d0311-173">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="d0311-173">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="d0311-174">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="d0311-174">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="d0311-175">**glPopAttrib**</span><span class="sxs-lookup"><span data-stu-id="d0311-175">**glPopAttrib**</span></span>](glpopattrib.md)
</dt> <dt>

[<span data-ttu-id="d0311-176">**glPushAttrib**</span><span class="sxs-lookup"><span data-stu-id="d0311-176">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="d0311-177">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="d0311-177">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="d0311-178">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="d0311-178">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





