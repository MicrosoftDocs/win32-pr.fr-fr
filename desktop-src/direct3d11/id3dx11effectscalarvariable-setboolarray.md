---
title: Méthode ID3DX11EffectScalarVariable SetBoolArray (D3dx11effect. h)
description: Définissez un tableau de variables booléennes.
ms.assetid: 861634a2-547d-497b-b575-bbe6151ade25
keywords:
- Méthode SetBoolArray Direct3D 11
- Méthode SetBoolArray Direct3D 11, interface ID3DX11EffectScalarVariable
- Interface ID3DX11EffectScalarVariable Direct3D 11, méthode SetBoolArray
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.SetBoolArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e982e2475fe20a2aa12bef9c52095eed228bf44
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322689"
---
# <a name="id3dx11effectscalarvariablesetboolarray-method"></a><span data-ttu-id="5e662-106">ID3DX11EffectScalarVariable :: SetBoolArray, méthode</span><span class="sxs-lookup"><span data-stu-id="5e662-106">ID3DX11EffectScalarVariable::SetBoolArray method</span></span>

<span data-ttu-id="5e662-107">Définissez un tableau de variables booléennes.</span><span class="sxs-lookup"><span data-stu-id="5e662-107">Set an array of boolean variables.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e662-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5e662-108">Syntax</span></span>


```C++
HRESULT SetBoolArray(
   BOOL *pData,
   UINT Offset,
   UINT Count
);
```



## <a name="parameters"></a><span data-ttu-id="5e662-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5e662-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e662-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="5e662-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="5e662-111">Type : **[ **bool**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="5e662-111">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="5e662-112">Pointeur vers le début des données à définir.</span><span class="sxs-lookup"><span data-stu-id="5e662-112">A pointer to the start of the data to set.</span></span>

</dd> <dt>

<span data-ttu-id="5e662-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="5e662-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="5e662-114">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="5e662-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="5e662-115">Doit avoir la valeur 0 ; elle est réservée à une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="5e662-115">Must be set to 0; this is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="5e662-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="5e662-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="5e662-117">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="5e662-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="5e662-118">Nombre d’éléments de tableau à définir.</span><span class="sxs-lookup"><span data-stu-id="5e662-118">The number of array elements to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e662-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5e662-119">Return value</span></span>

<span data-ttu-id="5e662-120">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5e662-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5e662-121">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="5e662-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5e662-122">Notes</span><span class="sxs-lookup"><span data-stu-id="5e662-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5e662-123">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="5e662-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="5e662-124">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="5e662-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="5e662-125">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="5e662-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5e662-126">Spécifications</span><span class="sxs-lookup"><span data-stu-id="5e662-126">Requirements</span></span>



| <span data-ttu-id="5e662-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5e662-127">Requirement</span></span> | <span data-ttu-id="5e662-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="5e662-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e662-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="5e662-129">Header</span></span><br/>  | <dl> <span data-ttu-id="5e662-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e662-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="5e662-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5e662-131">Library</span></span><br/> | <dl> <span data-ttu-id="5e662-132"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="5e662-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e662-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e662-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e662-134">ID3DX11EffectScalarVariable</span><span class="sxs-lookup"><span data-stu-id="5e662-134">ID3DX11EffectScalarVariable</span></span>](id3dx11effectscalarvariable.md)
</dt> </dl>

 

