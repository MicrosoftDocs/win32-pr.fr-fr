---
title: Méthode ID3DX11EffectMatrixVariable GetMatrixTransposeArray (D3dx11effect. h)
description: Transposez et récupérez un tableau de matrices à virgule flottante.
ms.assetid: cfcdbda0-b321-4e94-8d09-bb9d7ddfb4a5
keywords:
- Méthode GetMatrixTransposeArray Direct3D 11
- Méthode GetMatrixTransposeArray Direct3D 11, interface ID3DX11EffectMatrixVariable
- Interface ID3DX11EffectMatrixVariable Direct3D 11, méthode GetMatrixTransposeArray
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.GetMatrixTransposeArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80d0a43e69ccf88c15d8296c024535dec42b3f31
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974551"
---
# <a name="id3dx11effectmatrixvariablegetmatrixtransposearray-method"></a><span data-ttu-id="fc922-106">ID3DX11EffectMatrixVariable :: GetMatrixTransposeArray, méthode</span><span class="sxs-lookup"><span data-stu-id="fc922-106">ID3DX11EffectMatrixVariable::GetMatrixTransposeArray method</span></span>

<span data-ttu-id="fc922-107">Transposez et récupérez un tableau de matrices à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="fc922-107">Transpose and get an array of floating-point matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc922-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fc922-108">Syntax</span></span>


```C++
HRESULT GetMatrixTransposeArray(
   float *pData,
   UINT  Offset,
   UINT  Count
);
```



## <a name="parameters"></a><span data-ttu-id="fc922-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fc922-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc922-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="fc922-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="fc922-111">Type : **float \***</span><span class="sxs-lookup"><span data-stu-id="fc922-111">Type: **float\***</span></span>

<span data-ttu-id="fc922-112">Pointeur vers le premier élément d’un tableau de matrices Tranposed.</span><span class="sxs-lookup"><span data-stu-id="fc922-112">A pointer to the first element of an array of tranposed matrices.</span></span>

</dd> <dt>

<span data-ttu-id="fc922-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="fc922-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="fc922-114">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fc922-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fc922-115">Décalage (en nombre de matrices) entre le début du tableau et la première matrice à récupérer.</span><span class="sxs-lookup"><span data-stu-id="fc922-115">The offset (in number of matrices) between the start of the array and the first matrix to get.</span></span>

</dd> <dt>

<span data-ttu-id="fc922-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="fc922-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="fc922-117">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fc922-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fc922-118">Nombre de matrices dans le tableau à récupérer.</span><span class="sxs-lookup"><span data-stu-id="fc922-118">The number of matrices in the array to get.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc922-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fc922-119">Return value</span></span>

<span data-ttu-id="fc922-120">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fc922-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fc922-121">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="fc922-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fc922-122">Notes</span><span class="sxs-lookup"><span data-stu-id="fc922-122">Remarks</span></span>

<span data-ttu-id="fc922-123">En transposant une matrice, vous réorganisez l’ordre des données de l’ordre des colonnes de lignes à l’ordre des lignes (ou vice versa).</span><span class="sxs-lookup"><span data-stu-id="fc922-123">Transposing a matrix will rearrange the data order from row-column order to column-row order (or vice versa).</span></span>

> [!Note]  
> <span data-ttu-id="fc922-124">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="fc922-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="fc922-125">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="fc922-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="fc922-126">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="fc922-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fc922-127">Spécifications</span><span class="sxs-lookup"><span data-stu-id="fc922-127">Requirements</span></span>



| <span data-ttu-id="fc922-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fc922-128">Requirement</span></span> | <span data-ttu-id="fc922-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="fc922-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc922-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="fc922-130">Header</span></span><br/>  | <dl> <span data-ttu-id="fc922-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc922-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="fc922-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fc922-132">Library</span></span><br/> | <dl> <span data-ttu-id="fc922-133"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="fc922-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc922-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fc922-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc922-135">ID3DX11EffectMatrixVariable</span><span class="sxs-lookup"><span data-stu-id="fc922-135">ID3DX11EffectMatrixVariable</span></span>](id3dx11effectmatrixvariable.md)
</dt> </dl>

 

