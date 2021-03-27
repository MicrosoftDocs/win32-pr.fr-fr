---
title: Méthode ID3DX11EffectMatrixVariable SetMatrixTransposeArray (D3dx11effect. h)
description: Transposez et définissez un tableau de matrices à virgule flottante.
ms.assetid: 08223022-5e77-4a84-9b68-b9b0c9a02270
keywords:
- Méthode SetMatrixTransposeArray Direct3D 11
- Méthode SetMatrixTransposeArray Direct3D 11, interface ID3DX11EffectMatrixVariable
- Interface ID3DX11EffectMatrixVariable Direct3D 11, méthode SetMatrixTransposeArray
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.SetMatrixTransposeArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f70676b76658b5732c1a2ee15858f83694272b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953962"
---
# <a name="id3dx11effectmatrixvariablesetmatrixtransposearray-method"></a><span data-ttu-id="a6885-106">ID3DX11EffectMatrixVariable :: SetMatrixTransposeArray, méthode</span><span class="sxs-lookup"><span data-stu-id="a6885-106">ID3DX11EffectMatrixVariable::SetMatrixTransposeArray method</span></span>

<span data-ttu-id="a6885-107">Transposez et définissez un tableau de matrices à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="a6885-107">Transpose and set an array of floating-point matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6885-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a6885-108">Syntax</span></span>


```C++
HRESULT SetMatrixTransposeArray(
   float *pData,
   UINT  Offset,
   UINT  Count
);
```



## <a name="parameters"></a><span data-ttu-id="a6885-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a6885-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6885-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="a6885-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="a6885-111">Type : **float \***</span><span class="sxs-lookup"><span data-stu-id="a6885-111">Type: **float\***</span></span>

<span data-ttu-id="a6885-112">Pointeur vers un tableau de matrices.</span><span class="sxs-lookup"><span data-stu-id="a6885-112">A pointer to an array of matrices.</span></span>

</dd> <dt>

<span data-ttu-id="a6885-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="a6885-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="a6885-114">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a6885-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a6885-115">Décalage (en nombre de matrices) entre le début du tableau et la première matrice à définir.</span><span class="sxs-lookup"><span data-stu-id="a6885-115">The offset (in number of matrices) between the start of the array and the first matrix to set.</span></span>

</dd> <dt>

<span data-ttu-id="a6885-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="a6885-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="a6885-117">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a6885-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a6885-118">Nombre de matrices dans le tableau à définir.</span><span class="sxs-lookup"><span data-stu-id="a6885-118">The number of matrices in the array to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6885-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a6885-119">Return value</span></span>

<span data-ttu-id="a6885-120">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a6885-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a6885-121">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="a6885-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a6885-122">Notes</span><span class="sxs-lookup"><span data-stu-id="a6885-122">Remarks</span></span>

<span data-ttu-id="a6885-123">En transposant une matrice, vous réorganisez l’ordre des données de l’ordre des colonnes de lignes à l’ordre des lignes (ou vice versa).</span><span class="sxs-lookup"><span data-stu-id="a6885-123">Transposing a matrix will rearrange the data order from row-column order to column-row order (or vice versa).</span></span>

> [!Note]  
> <span data-ttu-id="a6885-124">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="a6885-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="a6885-125">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="a6885-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="a6885-126">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="a6885-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a6885-127">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a6885-127">Requirements</span></span>



| <span data-ttu-id="a6885-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a6885-128">Requirement</span></span> | <span data-ttu-id="a6885-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="a6885-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6885-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="a6885-130">Header</span></span><br/>  | <dl> <span data-ttu-id="a6885-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6885-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="a6885-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a6885-132">Library</span></span><br/> | <dl> <span data-ttu-id="a6885-133"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="a6885-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6885-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a6885-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6885-135">ID3DX11EffectMatrixVariable</span><span class="sxs-lookup"><span data-stu-id="a6885-135">ID3DX11EffectMatrixVariable</span></span>](id3dx11effectmatrixvariable.md)
</dt> </dl>

 

