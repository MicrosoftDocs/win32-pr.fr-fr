---
title: Méthode ID3DX11EffectVectorVariable GetBoolVectorArray (D3dx11effect. h)
description: Obtient un tableau de vecteurs à quatre composants qui contiennent des données booléennes.
ms.assetid: f600a480-e68e-4b05-8c76-2fe30520172b
keywords:
- Méthode GetBoolVectorArray Direct3D 11
- Méthode GetBoolVectorArray Direct3D 11, interface ID3DX11EffectVectorVariable
- Interface ID3DX11EffectVectorVariable Direct3D 11, méthode GetBoolVectorArray
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable.GetBoolVectorArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e541989d9ac0410faf5331623c8a8de29dccd1bf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992317"
---
# <a name="id3dx11effectvectorvariablegetboolvectorarray-method"></a><span data-ttu-id="572ff-106">ID3DX11EffectVectorVariable :: GetBoolVectorArray, méthode</span><span class="sxs-lookup"><span data-stu-id="572ff-106">ID3DX11EffectVectorVariable::GetBoolVectorArray method</span></span>

<span data-ttu-id="572ff-107">Obtient un tableau de vecteurs à quatre composants qui contiennent des données booléennes.</span><span class="sxs-lookup"><span data-stu-id="572ff-107">Get an array of four-component vectors that contain boolean data.</span></span>

## <a name="syntax"></a><span data-ttu-id="572ff-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="572ff-108">Syntax</span></span>


```C++
HRESULT GetBoolVectorArray(
   BOOL *pData,
   UINT Offset,
   UINT Count
);
```



## <a name="parameters"></a><span data-ttu-id="572ff-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="572ff-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="572ff-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="572ff-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="572ff-111">Type : **[ **bool**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="572ff-111">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="572ff-112">Pointeur vers le début des données à définir.</span><span class="sxs-lookup"><span data-stu-id="572ff-112">A pointer to the start of the data to set.</span></span>

</dd> <dt>

<span data-ttu-id="572ff-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="572ff-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="572ff-114">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="572ff-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="572ff-115">Doit avoir la valeur 0 ; elle est réservée à une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="572ff-115">Must be set to 0; this is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="572ff-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="572ff-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="572ff-117">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="572ff-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="572ff-118">Nombre d’éléments de tableau à définir.</span><span class="sxs-lookup"><span data-stu-id="572ff-118">The number of array elements to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="572ff-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="572ff-119">Return value</span></span>

<span data-ttu-id="572ff-120">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="572ff-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="572ff-121">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="572ff-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="572ff-122">Notes</span><span class="sxs-lookup"><span data-stu-id="572ff-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="572ff-123">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="572ff-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="572ff-124">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="572ff-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="572ff-125">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="572ff-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="572ff-126">Spécifications</span><span class="sxs-lookup"><span data-stu-id="572ff-126">Requirements</span></span>



| <span data-ttu-id="572ff-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="572ff-127">Requirement</span></span> | <span data-ttu-id="572ff-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="572ff-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="572ff-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="572ff-129">Header</span></span><br/>  | <dl> <span data-ttu-id="572ff-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="572ff-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="572ff-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="572ff-131">Library</span></span><br/> | <dl> <span data-ttu-id="572ff-132"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="572ff-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="572ff-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="572ff-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="572ff-134">ID3DX11EffectVectorVariable</span><span class="sxs-lookup"><span data-stu-id="572ff-134">ID3DX11EffectVectorVariable</span></span>](id3dx11effectvectorvariable.md)
</dt> </dl>

 

