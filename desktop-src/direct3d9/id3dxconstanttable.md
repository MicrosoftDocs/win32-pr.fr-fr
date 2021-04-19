---
description: L’interface ID3DXConstantTable est utilisée pour accéder à la table constante. Ce tableau contient les variables utilisées par les nuanceurs et les effets de langages de haut niveau.
ms.assetid: 5d412c77-3d35-4913-86e5-8efa0549a2bb
title: Interface ID3DXConstantTable (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bb2b7614c4d6a0e677f71e66ab94abdb89deb973
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523194"
---
# <a name="id3dxconstanttable-interface"></a><span data-ttu-id="2f38e-104">Interface ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="2f38e-104">ID3DXConstantTable interface</span></span>

<span data-ttu-id="2f38e-105">L’interface ID3DXConstantTable est utilisée pour accéder à la table constante.</span><span class="sxs-lookup"><span data-stu-id="2f38e-105">The ID3DXConstantTable interface is used to access the constant table.</span></span> <span data-ttu-id="2f38e-106">Ce tableau contient les variables utilisées par les nuanceurs et les effets de langages de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="2f38e-106">This table contains the variables that are used by high-level language shaders and effects.</span></span>

## <a name="members"></a><span data-ttu-id="2f38e-107">Membres</span><span class="sxs-lookup"><span data-stu-id="2f38e-107">Members</span></span>

<span data-ttu-id="2f38e-108">L’interface **ID3DXConstantTable** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="2f38e-108">The **ID3DXConstantTable** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2f38e-109">**ID3DXConstantTable** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2f38e-109">**ID3DXConstantTable** also has these types of members:</span></span>

-   [<span data-ttu-id="2f38e-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2f38e-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2f38e-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2f38e-111">Methods</span></span>

<span data-ttu-id="2f38e-112">L’interface **ID3DXConstantTable** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="2f38e-112">The **ID3DXConstantTable** interface has these methods.</span></span>



| <span data-ttu-id="2f38e-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="2f38e-113">Method</span></span>                                                                                       | <span data-ttu-id="2f38e-114">Description</span><span class="sxs-lookup"><span data-stu-id="2f38e-114">Description</span></span>                                                                                                                        |
|:---------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2f38e-115">**GetBufferPointer**</span><span class="sxs-lookup"><span data-stu-id="2f38e-115">**GetBufferPointer**</span></span>](id3dxconstanttable--getbufferpointer.md)                             | <span data-ttu-id="2f38e-116">Obtient un pointeur vers la mémoire tampon qui contient la table constante.</span><span class="sxs-lookup"><span data-stu-id="2f38e-116">Gets a pointer to the buffer that contains the constant table.</span></span><br/>                                                          |
| [<span data-ttu-id="2f38e-117">**GetBufferSize**</span><span class="sxs-lookup"><span data-stu-id="2f38e-117">**GetBufferSize**</span></span>](id3dxconstanttable--getbuffersize.md)                                   | <span data-ttu-id="2f38e-118">Obtient la taille de la mémoire tampon de la table constante.</span><span class="sxs-lookup"><span data-stu-id="2f38e-118">Gets the buffer size of the constant table.</span></span><br/>                                                                             |
| [<span data-ttu-id="2f38e-119">**GetConstant**</span><span class="sxs-lookup"><span data-stu-id="2f38e-119">**GetConstant**</span></span>](id3dxconstanttable--getconstant.md)                                       | <span data-ttu-id="2f38e-120">Obtient une constante en recherchant son index.</span><span class="sxs-lookup"><span data-stu-id="2f38e-120">Gets a constant by looking up its index.</span></span><br/>                                                                                |
| [<span data-ttu-id="2f38e-121">**GetConstantByName**</span><span class="sxs-lookup"><span data-stu-id="2f38e-121">**GetConstantByName**</span></span>](id3dxconstanttable--getconstantbyname.md)                           | <span data-ttu-id="2f38e-122">Obtient une constante en recherchant son nom.</span><span class="sxs-lookup"><span data-stu-id="2f38e-122">Gets a constant by looking up its name.</span></span><br/>                                                                                 |
| [<span data-ttu-id="2f38e-123">**GetConstantDesc**</span><span class="sxs-lookup"><span data-stu-id="2f38e-123">**GetConstantDesc**</span></span>](id3dxconstanttable--getconstantdesc.md)                               | <span data-ttu-id="2f38e-124">Obtient un pointeur vers un tableau de descriptions constantes dans la table constante.</span><span class="sxs-lookup"><span data-stu-id="2f38e-124">Gets a pointer to an array of constant descriptions in the constant table.</span></span><br/>                                              |
| [<span data-ttu-id="2f38e-125">**GetConstantElement**</span><span class="sxs-lookup"><span data-stu-id="2f38e-125">**GetConstantElement**</span></span>](id3dxconstanttable--getconstantelement.md)                         | <span data-ttu-id="2f38e-126">Obtient une constante d’un tableau de constantes.</span><span class="sxs-lookup"><span data-stu-id="2f38e-126">Gets a constant from an array of constants.</span></span> <span data-ttu-id="2f38e-127">Un tableau est constitué d’éléments.</span><span class="sxs-lookup"><span data-stu-id="2f38e-127">An array is made up of elements.</span></span><br/>                                            |
| [<span data-ttu-id="2f38e-128">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="2f38e-128">**GetDesc**</span></span>](id3dxconstanttable--getdesc.md)                                               | <span data-ttu-id="2f38e-129">Obtient une description de la table constante.</span><span class="sxs-lookup"><span data-stu-id="2f38e-129">Gets a description of the constant table.</span></span><br/>                                                                               |
| [<span data-ttu-id="2f38e-130">**GetSamplerIndex**</span><span class="sxs-lookup"><span data-stu-id="2f38e-130">**GetSamplerIndex**</span></span>](id3dxconstanttable--getsamplerindex.md)                               | <span data-ttu-id="2f38e-131">Retourne l’index de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="2f38e-131">Returns the sampler index.</span></span><br/>                                                                                              |
| [<span data-ttu-id="2f38e-132">**SetBool**</span><span class="sxs-lookup"><span data-stu-id="2f38e-132">**SetBool**</span></span>](id3dxconstanttable--setbool.md)                                               | <span data-ttu-id="2f38e-133">Définit une valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="2f38e-133">Sets a Boolean value.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="2f38e-134">**SetBoolArray**</span><span class="sxs-lookup"><span data-stu-id="2f38e-134">**SetBoolArray**</span></span>](id3dxconstanttable--setboolarray.md)                                     | <span data-ttu-id="2f38e-135">Définit un tableau de valeurs booléennes.</span><span class="sxs-lookup"><span data-stu-id="2f38e-135">Sets an array of Boolean values.</span></span><br/>                                                                                        |
| [<span data-ttu-id="2f38e-136">**SetDefaults**</span><span class="sxs-lookup"><span data-stu-id="2f38e-136">**SetDefaults**</span></span>](id3dxconstanttable--setdefaults.md)                                       | <span data-ttu-id="2f38e-137">Affecte aux constantes leurs valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="2f38e-137">Sets the constants to their default values.</span></span> <span data-ttu-id="2f38e-138">Les valeurs par défaut sont déclarées dans les déclarations de variable dans le nuanceur.</span><span class="sxs-lookup"><span data-stu-id="2f38e-138">The default values are declared in the variable declarations in the shader.</span></span><br/> |
| [<span data-ttu-id="2f38e-139">**SetFloat**</span><span class="sxs-lookup"><span data-stu-id="2f38e-139">**SetFloat**</span></span>](id3dxconstanttable--setfloat.md)                                             | <span data-ttu-id="2f38e-140">Définit un nombre à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="2f38e-140">Sets a floating-point number.</span></span><br/>                                                                                           |
| [<span data-ttu-id="2f38e-141">**SetFloatArray**</span><span class="sxs-lookup"><span data-stu-id="2f38e-141">**SetFloatArray**</span></span>](id3dxconstanttable--setfloatarray.md)                                   | <span data-ttu-id="2f38e-142">Définit un tableau de nombres à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="2f38e-142">Sets an array of floating-point numbers.</span></span><br/>                                                                                |
| [<span data-ttu-id="2f38e-143">**SetInt**</span><span class="sxs-lookup"><span data-stu-id="2f38e-143">**SetInt**</span></span>](id3dxconstanttable--setint.md)                                                 | <span data-ttu-id="2f38e-144">Définit une valeur entière.</span><span class="sxs-lookup"><span data-stu-id="2f38e-144">Sets an integer value.</span></span><br/>                                                                                                  |
| [<span data-ttu-id="2f38e-145">**SetIntArray**</span><span class="sxs-lookup"><span data-stu-id="2f38e-145">**SetIntArray**</span></span>](id3dxconstanttable--setintarray.md)                                       | <span data-ttu-id="2f38e-146">Définit un tableau d’entiers.</span><span class="sxs-lookup"><span data-stu-id="2f38e-146">Sets an array of integers.</span></span><br/>                                                                                              |
| [<span data-ttu-id="2f38e-147">**SetMatrix**</span><span class="sxs-lookup"><span data-stu-id="2f38e-147">**SetMatrix**</span></span>](id3dxconstanttable--setmatrix.md)                                           | <span data-ttu-id="2f38e-148">Définit une matrice nontransposed.</span><span class="sxs-lookup"><span data-stu-id="2f38e-148">Sets a nontransposed matrix.</span></span><br/>                                                                                            |
| [<span data-ttu-id="2f38e-149">**SetMatrixArray**</span><span class="sxs-lookup"><span data-stu-id="2f38e-149">**SetMatrixArray**</span></span>](id3dxconstanttable--setmatrixarray.md)                                 | <span data-ttu-id="2f38e-150">Définit un tableau de matrices nontransposed.</span><span class="sxs-lookup"><span data-stu-id="2f38e-150">Sets an array of nontransposed matrices.</span></span><br/>                                                                                |
| [<span data-ttu-id="2f38e-151">**SetMatrixPointerArray**</span><span class="sxs-lookup"><span data-stu-id="2f38e-151">**SetMatrixPointerArray**</span></span>](id3dxconstanttable--setmatrixpointerarray.md)                   | <span data-ttu-id="2f38e-152">Définit un tableau de pointeurs sur les matrices nontransposed.</span><span class="sxs-lookup"><span data-stu-id="2f38e-152">Sets an array of pointers to nontransposed matrices.</span></span><br/>                                                                    |
| [<span data-ttu-id="2f38e-153">**SetMatrixTranspose**</span><span class="sxs-lookup"><span data-stu-id="2f38e-153">**SetMatrixTranspose**</span></span>](id3dxconstanttable--setmatrixtranspose.md)                         | <span data-ttu-id="2f38e-154">Définit une matrice transposée.</span><span class="sxs-lookup"><span data-stu-id="2f38e-154">Sets a transposed matrix.</span></span><br/>                                                                                               |
| [<span data-ttu-id="2f38e-155">**SetMatrixTransposeArray**</span><span class="sxs-lookup"><span data-stu-id="2f38e-155">**SetMatrixTransposeArray**</span></span>](id3dxconstanttable--setmatrixtransposearray.md)               | <span data-ttu-id="2f38e-156">Définit un tableau de matrices transposées.</span><span class="sxs-lookup"><span data-stu-id="2f38e-156">Sets an array of transposed matrices.</span></span><br/>                                                                                   |
| [<span data-ttu-id="2f38e-157">**SetMatrixTransposePointerArray**</span><span class="sxs-lookup"><span data-stu-id="2f38e-157">**SetMatrixTransposePointerArray**</span></span>](id3dxconstanttable--setmatrixtransposepointerarray.md) | <span data-ttu-id="2f38e-158">Définit un tableau de pointeurs vers des matrices transposées.</span><span class="sxs-lookup"><span data-stu-id="2f38e-158">Sets an array of pointers to transposed matrices.</span></span><br/>                                                                       |
| [<span data-ttu-id="2f38e-159">**SetValue**</span><span class="sxs-lookup"><span data-stu-id="2f38e-159">**SetValue**</span></span>](id3dxconstanttable--setvalue.md)                                             | <span data-ttu-id="2f38e-160">Définit le contenu de la mémoire tampon sur la table constante.</span><span class="sxs-lookup"><span data-stu-id="2f38e-160">Sets the contents of the buffer to the constant table.</span></span><br/>                                                                  |
| [<span data-ttu-id="2f38e-161">**SetVector**</span><span class="sxs-lookup"><span data-stu-id="2f38e-161">**SetVector**</span></span>](id3dxconstanttable--setvector.md)                                           | <span data-ttu-id="2f38e-162">Définit un vecteur 4D.</span><span class="sxs-lookup"><span data-stu-id="2f38e-162">Sets a 4D vector.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="2f38e-163">**SetVectorArray**</span><span class="sxs-lookup"><span data-stu-id="2f38e-163">**SetVectorArray**</span></span>](id3dxconstanttable--setvectorarray.md)                                 | <span data-ttu-id="2f38e-164">Définit un tableau de vecteurs 4D.</span><span class="sxs-lookup"><span data-stu-id="2f38e-164">Sets an array of 4D vectors.</span></span><br/>                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="2f38e-165">Notes</span><span class="sxs-lookup"><span data-stu-id="2f38e-165">Remarks</span></span>

<span data-ttu-id="2f38e-166">Le type LPD3DXCONSTANTTABLE est défini comme un pointeur vers l’interface **ID3DXConstantTable** .</span><span class="sxs-lookup"><span data-stu-id="2f38e-166">The LPD3DXCONSTANTTABLE type is defined as a pointer to the **ID3DXConstantTable** interface.</span></span>


```
typedef interface ID3DXConstantTable ID3DXConstantTable;
typedef interface ID3DXConstantTable *LPD3DXCONSTANTTABLE;
```



## <a name="requirements"></a><span data-ttu-id="2f38e-167">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2f38e-167">Requirements</span></span>



| <span data-ttu-id="2f38e-168">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2f38e-168">Requirement</span></span> | <span data-ttu-id="2f38e-169">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f38e-169">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f38e-170">En-tête</span><span class="sxs-lookup"><span data-stu-id="2f38e-170">Header</span></span><br/>  | <dl> <span data-ttu-id="2f38e-171"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f38e-171"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="2f38e-172">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2f38e-172">Library</span></span><br/> | <dl> <span data-ttu-id="2f38e-173"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2f38e-173"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2f38e-174">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2f38e-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f38e-175">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="2f38e-175">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
