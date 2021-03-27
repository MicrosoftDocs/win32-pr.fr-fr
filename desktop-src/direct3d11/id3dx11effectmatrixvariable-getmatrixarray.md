---
title: Méthode ID3DX11EffectMatrixVariable GetMatrixArray (D3dx11effect. h)
description: Obtient un tableau de matrices.
ms.assetid: a7598687-a11c-41ad-9fb6-2c16d12f5edc
keywords:
- Méthode GetMatrixArray Direct3D 11
- Méthode GetMatrixArray Direct3D 11, interface ID3DX11EffectMatrixVariable
- Interface ID3DX11EffectMatrixVariable Direct3D 11, méthode GetMatrixArray
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.GetMatrixArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d4a339bf6918868473966b6d79bcbe6b6aa3eaa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953914"
---
# <a name="id3dx11effectmatrixvariablegetmatrixarray-method"></a><span data-ttu-id="4ba8f-106">ID3DX11EffectMatrixVariable :: GetMatrixArray, méthode</span><span class="sxs-lookup"><span data-stu-id="4ba8f-106">ID3DX11EffectMatrixVariable::GetMatrixArray method</span></span>

<span data-ttu-id="4ba8f-107">Obtient un tableau de matrices.</span><span class="sxs-lookup"><span data-stu-id="4ba8f-107">Get an array of matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ba8f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4ba8f-108">Syntax</span></span>


```C++
HRESULT GetMatrixArray(
   float *pData,
   UINT  Offset,
   UINT  Count
);
```



## <a name="parameters"></a><span data-ttu-id="4ba8f-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4ba8f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ba8f-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="4ba8f-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="4ba8f-111">Type : **float \***</span><span class="sxs-lookup"><span data-stu-id="4ba8f-111">Type: **float\***</span></span>

<span data-ttu-id="4ba8f-112">Pointeur vers le premier élément de la première matrice dans un tableau de matrices.</span><span class="sxs-lookup"><span data-stu-id="4ba8f-112">A pointer to the first element of the first matrix in an array of matrices.</span></span>

</dd> <dt>

<span data-ttu-id="4ba8f-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="4ba8f-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="4ba8f-114">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4ba8f-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="4ba8f-115">Décalage (en nombre de matrices) entre le début du tableau et la première matrice retournée.</span><span class="sxs-lookup"><span data-stu-id="4ba8f-115">The offset (in number of matrices) between the start of the array and the first matrix returned.</span></span>

</dd> <dt>

<span data-ttu-id="4ba8f-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="4ba8f-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="4ba8f-117">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4ba8f-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="4ba8f-118">Nombre de matrices dans le tableau retourné.</span><span class="sxs-lookup"><span data-stu-id="4ba8f-118">The number of matrices in the returned array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ba8f-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4ba8f-119">Return value</span></span>

<span data-ttu-id="4ba8f-120">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4ba8f-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4ba8f-121">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="4ba8f-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4ba8f-122">Notes</span><span class="sxs-lookup"><span data-stu-id="4ba8f-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4ba8f-123">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="4ba8f-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="4ba8f-124">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="4ba8f-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="4ba8f-125">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="4ba8f-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4ba8f-126">Spécifications</span><span class="sxs-lookup"><span data-stu-id="4ba8f-126">Requirements</span></span>



| <span data-ttu-id="4ba8f-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4ba8f-127">Requirement</span></span> | <span data-ttu-id="4ba8f-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="4ba8f-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ba8f-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="4ba8f-129">Header</span></span><br/>  | <dl> <span data-ttu-id="4ba8f-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ba8f-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="4ba8f-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4ba8f-131">Library</span></span><br/> | <dl> <span data-ttu-id="4ba8f-132"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="4ba8f-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ba8f-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4ba8f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ba8f-134">ID3DX11EffectMatrixVariable</span><span class="sxs-lookup"><span data-stu-id="4ba8f-134">ID3DX11EffectMatrixVariable</span></span>](id3dx11effectmatrixvariable.md)
</dt> </dl>

 

