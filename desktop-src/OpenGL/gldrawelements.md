---
title: fonction glDrawElements (GL. h)
description: La fonction glDrawElements restitue les primitives à partir des données de tableau.
ms.assetid: fb433294-106e-48d5-ad49-4434934fe072
keywords:
- glDrawElements fonction OpenGL
topic_type:
- apiref
api_name:
- glDrawElements
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 976e779235dc330467d610406156534b5e72841d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508790"
---
# <a name="gldrawelements-function"></a><span data-ttu-id="c0199-104">glDrawElements fonction)</span><span class="sxs-lookup"><span data-stu-id="c0199-104">glDrawElements function</span></span>

<span data-ttu-id="c0199-105">La fonction **glDrawElements** restitue les primitives à partir des données de tableau.</span><span class="sxs-lookup"><span data-stu-id="c0199-105">The **glDrawElements** function renders primitives from array data.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0199-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c0199-106">Syntax</span></span>


```C++
void WINAPI glDrawElements(
         GLenum  mode,
         GLsizei count,
         GLenum  type,
   const GLvoid  *indices
);
```



## <a name="parameters"></a><span data-ttu-id="c0199-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c0199-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0199-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="c0199-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="c0199-109">Type de primitives à restituer.</span><span class="sxs-lookup"><span data-stu-id="c0199-109">The kind of primitives to render.</span></span> <span data-ttu-id="c0199-110">Elle peut prendre l’une des valeurs symboliques suivantes : les \_ points de la comptabilité, la bande de facturation GL, la \_ \_ boucle de lignes GL, les \_ \_ \_ lignes de GL, la \_ bande triangulaire GL \_ , le \_ \_ ventilateur de triangle GL, \_ les triangles GL, le GL \_ Quad \_ Strip, \_ les quads GL et le \_ polygone GL.</span><span class="sxs-lookup"><span data-stu-id="c0199-110">It can assume one of the following symbolic values: GL\_POINTS, GL\_LINE\_STRIP, GL\_LINE\_LOOP, GL\_LINES, GL\_TRIANGLE\_STRIP, GL\_TRIANGLE\_FAN, GL\_TRIANGLES, GL\_QUAD\_STRIP, GL\_QUADS, and GL\_POLYGON.</span></span>

</dd> <dt>

<span data-ttu-id="c0199-111">*count*</span><span class="sxs-lookup"><span data-stu-id="c0199-111">*count*</span></span> 
</dt> <dd>

<span data-ttu-id="c0199-112">Nombre d’éléments à rendre.</span><span class="sxs-lookup"><span data-stu-id="c0199-112">The number of elements to be rendered.</span></span>

</dd> <dt>

<span data-ttu-id="c0199-113">*type*</span><span class="sxs-lookup"><span data-stu-id="c0199-113">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="c0199-114">Type des valeurs dans les index.</span><span class="sxs-lookup"><span data-stu-id="c0199-114">The type of the values in indices.</span></span> <span data-ttu-id="c0199-115">Doit être l’un des \_ octets non signés GL \_ , GL \_ unsigned \_ short ou GL \_ unsigned \_ int.</span><span class="sxs-lookup"><span data-stu-id="c0199-115">Must be one of GL\_UNSIGNED\_BYTE, GL\_UNSIGNED\_SHORT, or GL\_UNSIGNED\_INT.</span></span>

</dd> <dt>

<span data-ttu-id="c0199-116">*index*</span><span class="sxs-lookup"><span data-stu-id="c0199-116">*indices*</span></span> 
</dt> <dd>

<span data-ttu-id="c0199-117">Pointeur vers l’emplacement où les index sont stockés.</span><span class="sxs-lookup"><span data-stu-id="c0199-117">A pointer to the location where the indices are stored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0199-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c0199-118">Return value</span></span>

<span data-ttu-id="c0199-119">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="c0199-119">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c0199-120">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="c0199-120">Error codes</span></span>

<span data-ttu-id="c0199-121">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="c0199-121">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="c0199-122">Nom</span><span class="sxs-lookup"><span data-stu-id="c0199-122">Name</span></span>                                                                                                  | <span data-ttu-id="c0199-123">Signification</span><span class="sxs-lookup"><span data-stu-id="c0199-123">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c0199-124"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c0199-124"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="c0199-125">le *mode* n’était pas une valeur acceptée.</span><span class="sxs-lookup"><span data-stu-id="c0199-125">*mode* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="c0199-126"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c0199-126"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="c0199-127">*Count* est une valeur négative.</span><span class="sxs-lookup"><span data-stu-id="c0199-127">*count* was a negative value.</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="c0199-128"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c0199-128"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="c0199-129">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="c0199-129">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c0199-130">Notes</span><span class="sxs-lookup"><span data-stu-id="c0199-130">Remarks</span></span>

<span data-ttu-id="c0199-131">La fonction **glDrawElements** vous permet de spécifier plusieurs primitives géométriques avec très peu d’appels de fonction.</span><span class="sxs-lookup"><span data-stu-id="c0199-131">The **glDrawElements** function enables you to specify multiple geometric primitives with very few function calls.</span></span> <span data-ttu-id="c0199-132">Au lieu d’appeler une fonction OpenGL pour passer chaque vertex, normal ou couleur, vous pouvez spécifier des tableaux distincts de vertex, de normales et de couleurs à l’avance, et les utiliser pour définir une séquence de primitives (tout du même type) à l’aide d’un seul appel à **glDrawElements**.</span><span class="sxs-lookup"><span data-stu-id="c0199-132">Instead of calling an OpenGL function to pass each individual vertex, normal, or color, you can specify separate arrays of vertices, normals, and colors beforehand and use them to define a sequence of primitives (all of the same type) with a single call to **glDrawElements**.</span></span>

<span data-ttu-id="c0199-133">Quand vous appelez la fonction **glDrawElements** , elle utilise des éléments séquentiels *Count* d' *index* pour construire une séquence de primitives géométriques.</span><span class="sxs-lookup"><span data-stu-id="c0199-133">When you call the **glDrawElements** function, it uses *count* sequential elements from *indices* to construct a sequence of geometric primitives.</span></span> <span data-ttu-id="c0199-134">Le paramètre *mode* spécifie le type de primitives construites et la façon dont les éléments de tableau sont utilisés pour construire ces Primitives.</span><span class="sxs-lookup"><span data-stu-id="c0199-134">The *mode* parameter specifies what kind of primitives are constructed, and how the array elements are used to construct these primitives.</span></span> <span data-ttu-id="c0199-135">Si le \_ \_ tableau de vertex GL n’est pas activé, aucune primitive géométrique n’est générée.</span><span class="sxs-lookup"><span data-stu-id="c0199-135">If GL\_VERTEX\_ARRAY is not enabled, no geometric primitives are generated.</span></span>

<span data-ttu-id="c0199-136">Les attributs de vertex modifiés par **glDrawElements** ont une valeur non spécifiée après le retour de **glDrawElements** .</span><span class="sxs-lookup"><span data-stu-id="c0199-136">Vertex attributes that are modified by **glDrawElements** have an unspecified value after **glDrawElements** returns.</span></span> <span data-ttu-id="c0199-137">Par exemple, si le \_ tableau de couleurs GL \_ est activé, la valeur de la couleur actuelle est non définie après l’exécution de **glDrawElements** .</span><span class="sxs-lookup"><span data-stu-id="c0199-137">For example, if GL\_COLOR\_ARRAY is enabled, the value of the current color is undefined after **glDrawElements** executes.</span></span> <span data-ttu-id="c0199-138">Les attributs qui ne sont pas modifiés restent inchangés.</span><span class="sxs-lookup"><span data-stu-id="c0199-138">Attributes that aren't modified remain unchanged.</span></span>

<span data-ttu-id="c0199-139">Vous pouvez inclure la fonction **glDrawElements** dans les listes d’affichage.</span><span class="sxs-lookup"><span data-stu-id="c0199-139">You can include the **glDrawElements** function in display lists.</span></span> <span data-ttu-id="c0199-140">Lorsque **glDrawElements** est inclus dans une liste d’affichage, les données de tableau nécessaires (déterminées par les pointeurs de tableau et activés) sont également entrées dans la liste d’affichage.</span><span class="sxs-lookup"><span data-stu-id="c0199-140">When **glDrawElements** is included in a display list, the necessary array data (determined by the array pointers and enables) is also entered into the display list.</span></span> <span data-ttu-id="c0199-141">Étant donné que les pointeurs de tableau et active sont des variables d’État côté client, leurs valeurs affectent les listes d’affichage quand les listes sont créées, et non lors de l’exécution des listes.</span><span class="sxs-lookup"><span data-stu-id="c0199-141">Because the array pointers and enables are client-side state variables, their values affect display lists when the lists are created, not when the lists are executed.</span></span>

> [!Note]  
> <span data-ttu-id="c0199-142">La fonction **glDrawElements** est disponible uniquement dans OpenGL version 1,1 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="c0199-142">The **glDrawElements** function is only available in OpenGL version 1.1 or later.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c0199-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0199-143">Requirements</span></span>



| <span data-ttu-id="c0199-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c0199-144">Requirement</span></span> | <span data-ttu-id="c0199-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="c0199-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0199-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c0199-146">Minimum supported client</span></span><br/> | <span data-ttu-id="c0199-147">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c0199-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c0199-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c0199-148">Minimum supported server</span></span><br/> | <span data-ttu-id="c0199-149">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c0199-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c0199-150">En-tête</span><span class="sxs-lookup"><span data-stu-id="c0199-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0199-151"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0199-151"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="c0199-152">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c0199-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="c0199-153"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c0199-153"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="c0199-154">DLL</span><span class="sxs-lookup"><span data-stu-id="c0199-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0199-155"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0199-155"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0199-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0199-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0199-157">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="c0199-157">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="c0199-158">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="c0199-158">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="c0199-159">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="c0199-159">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="c0199-160">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="c0199-160">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="c0199-161">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="c0199-161">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="c0199-162">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="c0199-162">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="c0199-163">**glGetPointerv**</span><span class="sxs-lookup"><span data-stu-id="c0199-163">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="c0199-164">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="c0199-164">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="c0199-165">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="c0199-165">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="c0199-166">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="c0199-166">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="c0199-167">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="c0199-167">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





