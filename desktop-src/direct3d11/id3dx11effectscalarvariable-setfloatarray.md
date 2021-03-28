---
title: Méthode ID3DX11EffectScalarVariable SetFloatArray (D3dx11effect. h)
description: Définissez un tableau de variables à virgule flottante.
ms.assetid: af7f3fb1-e5a8-43c9-8c8a-5ee7b3b01242
keywords:
- Méthode SetFloatArray Direct3D 11
- Méthode SetFloatArray Direct3D 11, interface ID3DX11EffectScalarVariable
- Interface ID3DX11EffectScalarVariable Direct3D 11, méthode SetFloatArray
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.SetFloatArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 591efd87026caeaadb8de7f29a2741dfccd5028a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953804"
---
# <a name="id3dx11effectscalarvariablesetfloatarray-method"></a><span data-ttu-id="f8938-106">ID3DX11EffectScalarVariable :: SetFloatArray, méthode</span><span class="sxs-lookup"><span data-stu-id="f8938-106">ID3DX11EffectScalarVariable::SetFloatArray method</span></span>

<span data-ttu-id="f8938-107">Définissez un tableau de variables à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="f8938-107">Set an array of floating-point variables.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8938-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f8938-108">Syntax</span></span>


```C++
HRESULT SetFloatArray(
   float *pData,
   UINT  Offset,
   UINT  Count
);
```



## <a name="parameters"></a><span data-ttu-id="f8938-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f8938-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8938-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="f8938-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="f8938-111">Type : **float \***</span><span class="sxs-lookup"><span data-stu-id="f8938-111">Type: **float\***</span></span>

<span data-ttu-id="f8938-112">Pointeur vers le début des données à définir.</span><span class="sxs-lookup"><span data-stu-id="f8938-112">A pointer to the start of the data to set.</span></span>

</dd> <dt>

<span data-ttu-id="f8938-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="f8938-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="f8938-114">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f8938-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f8938-115">Doit avoir la valeur 0 ; elle est réservée à une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="f8938-115">Must be set to 0; this is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="f8938-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="f8938-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="f8938-117">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f8938-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f8938-118">Nombre d’éléments de tableau à définir.</span><span class="sxs-lookup"><span data-stu-id="f8938-118">The number of array elements to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8938-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f8938-119">Return value</span></span>

<span data-ttu-id="f8938-120">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f8938-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f8938-121">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="f8938-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f8938-122">Notes</span><span class="sxs-lookup"><span data-stu-id="f8938-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f8938-123">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="f8938-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="f8938-124">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="f8938-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="f8938-125">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="f8938-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f8938-126">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f8938-126">Requirements</span></span>



| <span data-ttu-id="f8938-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f8938-127">Requirement</span></span> | <span data-ttu-id="f8938-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="f8938-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8938-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="f8938-129">Header</span></span><br/>  | <dl> <span data-ttu-id="f8938-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8938-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="f8938-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f8938-131">Library</span></span><br/> | <dl> <span data-ttu-id="f8938-132"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="f8938-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8938-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8938-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8938-134">ID3DX11EffectScalarVariable</span><span class="sxs-lookup"><span data-stu-id="f8938-134">ID3DX11EffectScalarVariable</span></span>](id3dx11effectscalarvariable.md)
</dt> </dl>

 

