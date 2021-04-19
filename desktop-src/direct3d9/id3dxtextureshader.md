---
description: Interface ID3DXTextureShader.
ms.assetid: 48ea307d-857f-4b73-9e13-de391fbce07b
title: Interface ID3DXTextureShader (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c1b9581bced9d501800a8a8f3cb5d31a563ac261
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538328"
---
# <a name="id3dxtextureshader-interface"></a><span data-ttu-id="b94b1-103">Interface ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="b94b1-103">ID3DXTextureShader interface</span></span>

<span data-ttu-id="b94b1-104">Interface ID3DXTextureShader.</span><span class="sxs-lookup"><span data-stu-id="b94b1-104">The ID3DXTextureShader interface.</span></span>

## <a name="members"></a><span data-ttu-id="b94b1-105">Membres</span><span class="sxs-lookup"><span data-stu-id="b94b1-105">Members</span></span>

<span data-ttu-id="b94b1-106">L’interface **ID3DXTextureShader** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="b94b1-106">The **ID3DXTextureShader** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b94b1-107">**ID3DXTextureShader** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b94b1-107">**ID3DXTextureShader** also has these types of members:</span></span>

-   [<span data-ttu-id="b94b1-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b94b1-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b94b1-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b94b1-109">Methods</span></span>

<span data-ttu-id="b94b1-110">L’interface **ID3DXTextureShader** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="b94b1-110">The **ID3DXTextureShader** interface has these methods.</span></span>



| <span data-ttu-id="b94b1-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="b94b1-111">Method</span></span>                                                                                       | <span data-ttu-id="b94b1-112">Description</span><span class="sxs-lookup"><span data-stu-id="b94b1-112">Description</span></span>                                                                 |
|:---------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------|
| [<span data-ttu-id="b94b1-113">**GetConstant**</span><span class="sxs-lookup"><span data-stu-id="b94b1-113">**GetConstant**</span></span>](id3dxtextureshader--getconstant.md)                                       | <span data-ttu-id="b94b1-114">Obtient une constante en recherchant son index.</span><span class="sxs-lookup"><span data-stu-id="b94b1-114">Gets a constant by looking up its index.</span></span><br/>                         |
| [<span data-ttu-id="b94b1-115">**GetConstantBuffer**</span><span class="sxs-lookup"><span data-stu-id="b94b1-115">**GetConstantBuffer**</span></span>](id3dxtextureshader--getconstantbuffer.md)                           | <span data-ttu-id="b94b1-116">Obtient un pointeur vers la table constante.</span><span class="sxs-lookup"><span data-stu-id="b94b1-116">Get a pointer to the constant table.</span></span><br/>                             |
| [<span data-ttu-id="b94b1-117">**GetConstantByName**</span><span class="sxs-lookup"><span data-stu-id="b94b1-117">**GetConstantByName**</span></span>](id3dxtextureshader--getconstantbyname.md)                           | <span data-ttu-id="b94b1-118">Obtient une constante en recherchant son nom.</span><span class="sxs-lookup"><span data-stu-id="b94b1-118">Gets a constant by looking up its name.</span></span><br/>                          |
| [<span data-ttu-id="b94b1-119">**GetConstantDesc**</span><span class="sxs-lookup"><span data-stu-id="b94b1-119">**GetConstantDesc**</span></span>](id3dxtextureshader--getconstantdesc.md)                               | <span data-ttu-id="b94b1-120">Obtient un pointeur vers le tableau de constantes dans la table constante.</span><span class="sxs-lookup"><span data-stu-id="b94b1-120">Gets a pointer to the array of constants in the constant table.</span></span><br/>  |
| [<span data-ttu-id="b94b1-121">**GetConstantElement**</span><span class="sxs-lookup"><span data-stu-id="b94b1-121">**GetConstantElement**</span></span>](id3dxtextureshader--getconstantelement.md)                         | <span data-ttu-id="b94b1-122">Obtient une constante de la table constante.</span><span class="sxs-lookup"><span data-stu-id="b94b1-122">Get a constant from the constant table.</span></span><br/>                          |
| [<span data-ttu-id="b94b1-123">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="b94b1-123">**GetDesc**</span></span>](id3dxtextureshader--getdesc.md)                                               | <span data-ttu-id="b94b1-124">Obtient une description de la table constante.</span><span class="sxs-lookup"><span data-stu-id="b94b1-124">Gets a description of the constant table.</span></span><br/>                        |
| [<span data-ttu-id="b94b1-125">**GetFunction**</span><span class="sxs-lookup"><span data-stu-id="b94b1-125">**GetFunction**</span></span>](id3dxtextureshader--getfunction.md)                                       | <span data-ttu-id="b94b1-126">Obtient un pointeur vers le flux de fonction DWORD.</span><span class="sxs-lookup"><span data-stu-id="b94b1-126">Gets a pointer to the function DWORD stream.</span></span><br/>                     |
| [<span data-ttu-id="b94b1-127">**SetBool**</span><span class="sxs-lookup"><span data-stu-id="b94b1-127">**SetBool**</span></span>](id3dxtextureshader--setbool.md)                                               | <span data-ttu-id="b94b1-128">Définit une valeur BOOL.</span><span class="sxs-lookup"><span data-stu-id="b94b1-128">Sets a BOOL value.</span></span><br/>                                               |
| [<span data-ttu-id="b94b1-129">**SetBoolArray**</span><span class="sxs-lookup"><span data-stu-id="b94b1-129">**SetBoolArray**</span></span>](id3dxtextureshader--setboolarray.md)                                     | <span data-ttu-id="b94b1-130">Définit un tableau de valeurs BOOL.</span><span class="sxs-lookup"><span data-stu-id="b94b1-130">Sets an array of BOOL values.</span></span><br/>                                    |
| [<span data-ttu-id="b94b1-131">**SetDefaults**</span><span class="sxs-lookup"><span data-stu-id="b94b1-131">**SetDefaults**</span></span>](id3dxtextureshader--setdefaults.md)                                       | <span data-ttu-id="b94b1-132">Affecte aux constantes les valeurs par défaut déclarées dans le nuanceur.</span><span class="sxs-lookup"><span data-stu-id="b94b1-132">Sets the constants to the default values declared in the shader.</span></span><br/> |
| [<span data-ttu-id="b94b1-133">**SetFloat**</span><span class="sxs-lookup"><span data-stu-id="b94b1-133">**SetFloat**</span></span>](id3dxtextureshader--setfloat.md)                                             | <span data-ttu-id="b94b1-134">Définit un nombre à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="b94b1-134">Sets a floating-point number.</span></span><br/>                                    |
| [<span data-ttu-id="b94b1-135">**SetFloatArray**</span><span class="sxs-lookup"><span data-stu-id="b94b1-135">**SetFloatArray**</span></span>](id3dxtextureshader--setfloatarray.md)                                   | <span data-ttu-id="b94b1-136">Définit un tableau de nombres à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="b94b1-136">Sets an array of floating-point numbers.</span></span><br/>                         |
| [<span data-ttu-id="b94b1-137">**SetInt**</span><span class="sxs-lookup"><span data-stu-id="b94b1-137">**SetInt**</span></span>](id3dxtextureshader--setint.md)                                                 | <span data-ttu-id="b94b1-138">Définit une valeur entière.</span><span class="sxs-lookup"><span data-stu-id="b94b1-138">Sets an integer value.</span></span><br/>                                           |
| [<span data-ttu-id="b94b1-139">**SetIntArray**</span><span class="sxs-lookup"><span data-stu-id="b94b1-139">**SetIntArray**</span></span>](id3dxtextureshader--setintarray.md)                                       | <span data-ttu-id="b94b1-140">Définit un tableau d’entiers.</span><span class="sxs-lookup"><span data-stu-id="b94b1-140">Sets an array of integers.</span></span><br/>                                       |
| [<span data-ttu-id="b94b1-141">**SetMatrix**</span><span class="sxs-lookup"><span data-stu-id="b94b1-141">**SetMatrix**</span></span>](id3dxtextureshader--setmatrix.md)                                           | <span data-ttu-id="b94b1-142">Définit une matrice non transposée.</span><span class="sxs-lookup"><span data-stu-id="b94b1-142">Sets a non-transposed matrix.</span></span><br/>                                    |
| [<span data-ttu-id="b94b1-143">**SetMatrixArray**</span><span class="sxs-lookup"><span data-stu-id="b94b1-143">**SetMatrixArray**</span></span>](id3dxtextureshader--setmatrixarray.md)                                 | <span data-ttu-id="b94b1-144">Définit un tableau de matrices non transposées.</span><span class="sxs-lookup"><span data-stu-id="b94b1-144">Sets an array of non-transposed matrices.</span></span><br/>                        |
| [<span data-ttu-id="b94b1-145">**SetMatrixPointerArray**</span><span class="sxs-lookup"><span data-stu-id="b94b1-145">**SetMatrixPointerArray**</span></span>](id3dxtextureshader--setmatrixpointerarray.md)                   | <span data-ttu-id="b94b1-146">Définit un tableau de pointeurs vers des matrices non transposées.</span><span class="sxs-lookup"><span data-stu-id="b94b1-146">Sets an array of pointers to non-transposed matrices.</span></span><br/>            |
| [<span data-ttu-id="b94b1-147">**SetMatrixTranspose**</span><span class="sxs-lookup"><span data-stu-id="b94b1-147">**SetMatrixTranspose**</span></span>](id3dxtextureshader--setmatrixtranspose.md)                         | <span data-ttu-id="b94b1-148">Définit une matrice transposée.</span><span class="sxs-lookup"><span data-stu-id="b94b1-148">Sets a transposed matrix.</span></span><br/>                                        |
| [<span data-ttu-id="b94b1-149">**SetMatrixTransposeArray**</span><span class="sxs-lookup"><span data-stu-id="b94b1-149">**SetMatrixTransposeArray**</span></span>](id3dxtextureshader--setmatrixtransposearray.md)               | <span data-ttu-id="b94b1-150">Définit un tableau de matrices transposées.</span><span class="sxs-lookup"><span data-stu-id="b94b1-150">Sets an array of transposed matrices.</span></span><br/>                            |
| [<span data-ttu-id="b94b1-151">**SetMatrixTransposePointerArray**</span><span class="sxs-lookup"><span data-stu-id="b94b1-151">**SetMatrixTransposePointerArray**</span></span>](id3dxtextureshader--setmatrixtransposepointerarray.md) | <span data-ttu-id="b94b1-152">Définit un tableau de pointeurs vers des matrices transposées.</span><span class="sxs-lookup"><span data-stu-id="b94b1-152">Sets an array of pointers to transposed matrices.</span></span><br/>                |
| [<span data-ttu-id="b94b1-153">**SetValue**</span><span class="sxs-lookup"><span data-stu-id="b94b1-153">**SetValue**</span></span>](id3dxtextureshader--setvalue.md)                                             | <span data-ttu-id="b94b1-154">Définit la table de constantes avec les données dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="b94b1-154">Sets the constant table with the data in the buffer.</span></span><br/>             |
| [<span data-ttu-id="b94b1-155">**SetVector**</span><span class="sxs-lookup"><span data-stu-id="b94b1-155">**SetVector**</span></span>](id3dxtextureshader--setvector.md)                                           | <span data-ttu-id="b94b1-156">Définit un vecteur 4D.</span><span class="sxs-lookup"><span data-stu-id="b94b1-156">Sets a 4D vector.</span></span><br/>                                                |
| [<span data-ttu-id="b94b1-157">**SetVectorArray**</span><span class="sxs-lookup"><span data-stu-id="b94b1-157">**SetVectorArray**</span></span>](id3dxtextureshader--setvectorarray.md)                                 | <span data-ttu-id="b94b1-158">Définit un tableau de vecteurs 4D.</span><span class="sxs-lookup"><span data-stu-id="b94b1-158">Sets an array of 4D vectors.</span></span><br/>                                     |



 

## <a name="remarks"></a><span data-ttu-id="b94b1-159">Notes</span><span class="sxs-lookup"><span data-stu-id="b94b1-159">Remarks</span></span>

<span data-ttu-id="b94b1-160">L’interface **ID3DXTextureShader** est obtenue en appelant la fonction [**D3DXCreateTextureShader**](d3dxcreatetextureshader.md) .</span><span class="sxs-lookup"><span data-stu-id="b94b1-160">The **ID3DXTextureShader** interface is obtained by calling the [**D3DXCreateTextureShader**](d3dxcreatetextureshader.md) function.</span></span>

<span data-ttu-id="b94b1-161">L’interface **ID3DXTextureShader** , comme toutes les interfaces com, hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="b94b1-161">The **ID3DXTextureShader** interface, like all COM interfaces, inherits the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span>

<span data-ttu-id="b94b1-162">Le type LPD3DXTEXTURESHADER est défini comme un pointeur vers l’interface **ID3DXTextureShader** .</span><span class="sxs-lookup"><span data-stu-id="b94b1-162">The LPD3DXTEXTURESHADER type is defined as a pointer to the **ID3DXTextureShader** interface.</span></span>


```
typedef interface ID3DXTextureShader *LPD3DXTEXTURESHADER;
```



## <a name="requirements"></a><span data-ttu-id="b94b1-163">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b94b1-163">Requirements</span></span>



| <span data-ttu-id="b94b1-164">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b94b1-164">Requirement</span></span> | <span data-ttu-id="b94b1-165">Valeur</span><span class="sxs-lookup"><span data-stu-id="b94b1-165">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b94b1-166">En-tête</span><span class="sxs-lookup"><span data-stu-id="b94b1-166">Header</span></span><br/>  | <dl> <span data-ttu-id="b94b1-167"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="b94b1-167"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="b94b1-168">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b94b1-168">Library</span></span><br/> | <dl> <span data-ttu-id="b94b1-169"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b94b1-169"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b94b1-170">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b94b1-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b94b1-171">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="b94b1-171">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
