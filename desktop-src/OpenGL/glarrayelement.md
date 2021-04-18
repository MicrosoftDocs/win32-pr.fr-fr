---
title: fonction glArrayElement (GL. h)
description: La fonction glArrayElement spécifie les éléments de tableau utilisés pour le rendu d’un vertex.
ms.assetid: 2c4d76bb-e4c9-4baa-a190-66298b8a4335
keywords:
- glArrayElement fonction OpenGL
topic_type:
- apiref
api_name:
- glArrayElement
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a20aff9fcaa5bf922bc9447f7b7022a8cd1a9c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512402"
---
# <a name="glarrayelement-function"></a><span data-ttu-id="75646-104">glArrayElement fonction)</span><span class="sxs-lookup"><span data-stu-id="75646-104">glArrayElement function</span></span>

<span data-ttu-id="75646-105">La fonction **glArrayElement** spécifie les éléments de tableau utilisés pour le rendu d’un vertex.</span><span class="sxs-lookup"><span data-stu-id="75646-105">The **glArrayElement** function specifies the array elements used to render a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="75646-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="75646-106">Syntax</span></span>


```C++
void WINAPI glArrayElement(
   GLint index
);
```



## <a name="parameters"></a><span data-ttu-id="75646-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="75646-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75646-108">*index*</span><span class="sxs-lookup"><span data-stu-id="75646-108">*index*</span></span> 
</dt> <dd>

<span data-ttu-id="75646-109">Index dans les tableaux activés.</span><span class="sxs-lookup"><span data-stu-id="75646-109">An index in the enabled arrays.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75646-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="75646-110">Return value</span></span>

<span data-ttu-id="75646-111">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="75646-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="75646-112">Notes</span><span class="sxs-lookup"><span data-stu-id="75646-112">Remarks</span></span>

<span data-ttu-id="75646-113">Utilisez la fonction **glArrayElement** dans les paires [**glBegin**](glbegin.md) et [**glEnd**](glend.md) pour spécifier les données de vertex et d’attribut pour les primitives de point, de ligne et de polygone.</span><span class="sxs-lookup"><span data-stu-id="75646-113">Use the **glArrayElement** function within [**glBegin**](glbegin.md) and [**glEnd**](glend.md) pairs to specify vertex and attribute data for point, line, and polygon primitives.</span></span> <span data-ttu-id="75646-114">La fonction **glArrayElement** spécifie les données d’un vertex unique à l’aide de données de vertex et d’attribut situées à l' *index* des tableaux de vertex activés.</span><span class="sxs-lookup"><span data-stu-id="75646-114">The **glArrayElement** function specifies the data for a single vertex using vertex and attribute data located at the *index* of the enabled vertex arrays.</span></span>

<span data-ttu-id="75646-115">Vous pouvez utiliser **glArrayElement** pour construire des primitives en indexant les données de vertex, plutôt que par diffusion en continu dans les tableaux de données de premier à dernier ordre.</span><span class="sxs-lookup"><span data-stu-id="75646-115">You can use **glArrayElement** to construct primitives by indexing vertex data, rather than by streaming through arrays of data in first-to-last order.</span></span> <span data-ttu-id="75646-116">Étant donné que **glArrayElement** spécifie un seul vertex uniquement, vous pouvez spécifier explicitement des attributs pour des primitives individuelles.</span><span class="sxs-lookup"><span data-stu-id="75646-116">Because **glArrayElement** specifies a single vertex only, you can explicitly specify attributes for individual primitives.</span></span> <span data-ttu-id="75646-117">Par exemple, vous pouvez définir un seul normal pour chaque triangle.</span><span class="sxs-lookup"><span data-stu-id="75646-117">For example, you can set a single normal for each individual triangle.</span></span>

<span data-ttu-id="75646-118">Lorsque vous incluez des appels à **glArrayElement** dans des listes d’affichage, les données de tableau nécessaires, déterminées par les pointeurs de tableau et les valeurs Enable, sont également entrées dans la liste d’affichage.</span><span class="sxs-lookup"><span data-stu-id="75646-118">When you include calls to **glArrayElement** in display lists, the necessary array data, determined by the array pointers and enable values, is entered in the display list also.</span></span> <span data-ttu-id="75646-119">Les valeurs de pointeur de tableau et d’activation sont déterminées lors de la création des listes d’affichage, et non lors de l’exécution des listes d’affichage.</span><span class="sxs-lookup"><span data-stu-id="75646-119">Array pointer and enable values are determined when display lists are created, not when display lists are executed.</span></span>

<span data-ttu-id="75646-120">Vous pouvez lire et mettre en cache les données du tableau statique à tout moment avec **glArrayElement**.</span><span class="sxs-lookup"><span data-stu-id="75646-120">You can read and cache static array data at any time with **glArrayElement**.</span></span> <span data-ttu-id="75646-121">Lorsque vous modifiez les éléments d’un tableau statique sans spécifier à nouveau le tableau, les résultats de tous les appels suivants à **glArrayElement** ne sont pas définis.</span><span class="sxs-lookup"><span data-stu-id="75646-121">When you modify the elements of a static array without specifying the array again, the results of any subsequent calls to **glArrayElement** are undefined.</span></span>

<span data-ttu-id="75646-122">Quand vous appelez **glArrayElement** sans appeler d’abord **glEnableClientState**( \_ tableau de vertex GL \_ ), aucun dessin ne se produit, mais les attributs correspondant aux tableaux activés sont modifiés.</span><span class="sxs-lookup"><span data-stu-id="75646-122">When you call **glArrayElement** without first calling **glEnableClientState**(GL\_VERTEX\_ARRAY), no drawing occurs, but the attributes corresponding to enabled arrays are modified.</span></span> <span data-ttu-id="75646-123">Bien qu’aucune erreur ne soit générée lorsque vous spécifiez un tableau dans les paires **glBegin** et **glEnd** , les résultats ne sont pas définis.</span><span class="sxs-lookup"><span data-stu-id="75646-123">Although no error is generated when you specify an array within **glBegin** and **glEnd** pairs, the results are undefined.</span></span>

> [!Note]  
> <span data-ttu-id="75646-124">La fonction **glArrayElement** est disponible uniquement dans OpenGL version 1,1 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="75646-124">The **glArrayElement** function is only available in OpenGL version 1.1 or later.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="75646-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="75646-125">Requirements</span></span>



| <span data-ttu-id="75646-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="75646-126">Requirement</span></span> | <span data-ttu-id="75646-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="75646-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="75646-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="75646-128">Minimum supported client</span></span><br/> | <span data-ttu-id="75646-129">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="75646-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="75646-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="75646-130">Minimum supported server</span></span><br/> | <span data-ttu-id="75646-131">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="75646-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="75646-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="75646-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="75646-133"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="75646-133"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="75646-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="75646-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="75646-135"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="75646-135"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="75646-136">DLL</span><span class="sxs-lookup"><span data-stu-id="75646-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75646-137"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75646-137"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75646-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75646-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75646-139">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="75646-139">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="75646-140">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="75646-140">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="75646-141">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="75646-141">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="75646-142">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="75646-142">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="75646-143">**glEnableClientState**</span><span class="sxs-lookup"><span data-stu-id="75646-143">**glEnableClientState**</span></span>](glenableclientstate.md)
</dt> <dt>

[<span data-ttu-id="75646-144">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="75646-144">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="75646-145">**glGetPointerv**</span><span class="sxs-lookup"><span data-stu-id="75646-145">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="75646-146">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="75646-146">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="75646-147">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="75646-147">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="75646-148">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="75646-148">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="75646-149">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="75646-149">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="75646-150">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="75646-150">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





