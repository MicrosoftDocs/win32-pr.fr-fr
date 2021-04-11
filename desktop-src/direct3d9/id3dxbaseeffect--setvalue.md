---
description: Définir la valeur d’une annotation ou d’un paramètre arbitraire, y compris les types simples, les structs, les tableaux, les chaînes, les nuanceurs et les textures.
ms.assetid: ab71f1a1-3e10-4883-99b4-607e0b5751c2
title: 'ID3DXBaseEffect :: SetValue, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetValue
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 3281306240cefc0312ff9a2af7e056dab74a085b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116254"
---
# <a name="id3dxbaseeffectsetvalue-method"></a><span data-ttu-id="b86ab-103">ID3DXBaseEffect :: SetValue, méthode</span><span class="sxs-lookup"><span data-stu-id="b86ab-103">ID3DXBaseEffect::SetValue method</span></span>

<span data-ttu-id="b86ab-104">Définir la valeur d’une annotation ou d’un paramètre arbitraire, y compris les types simples, les structs, les tableaux, les chaînes, les nuanceurs et les textures.</span><span class="sxs-lookup"><span data-stu-id="b86ab-104">Set the value of an arbitrary parameter or annotation, including simple types, structs, arrays, strings, shaders and textures.</span></span>

## <a name="syntax"></a><span data-ttu-id="b86ab-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b86ab-105">Syntax</span></span>


```C++
HRESULT SetValue(
  [in] D3DXHANDLE hParameter,
  [in] LPCVOID    pData,
  [in] UINT       Bytes
);
```



## <a name="parameters"></a><span data-ttu-id="b86ab-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b86ab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b86ab-107">*hParameter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b86ab-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b86ab-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="b86ab-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="b86ab-109">Identificateur unique.</span><span class="sxs-lookup"><span data-stu-id="b86ab-109">Unique identifier.</span></span> <span data-ttu-id="b86ab-110">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="b86ab-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="b86ab-111">*pData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b86ab-111">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b86ab-112">Type : **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b86ab-112">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b86ab-113">Pointeur vers une mémoire tampon qui contient des données.</span><span class="sxs-lookup"><span data-stu-id="b86ab-113">Pointer to a buffer containing data.</span></span>

</dd> <dt>

<span data-ttu-id="b86ab-114">*Octets* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b86ab-114">*Bytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b86ab-115">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b86ab-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b86ab-116">\[en \] nombre d’octets dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="b86ab-116">\[in\] Number of bytes in the buffer.</span></span> <span data-ttu-id="b86ab-117">Passez à \_ la passerelle par défaut D3DX si vous savez que votre mémoire tampon est suffisamment grande pour contenir le paramètre entier et que vous souhaitez ignorer la validation de la taille.</span><span class="sxs-lookup"><span data-stu-id="b86ab-117">Pass in D3DX\_DEFAULT if you know your buffer is large enough to contain the entire parameter, and you want to skip size validation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b86ab-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b86ab-118">Return value</span></span>

<span data-ttu-id="b86ab-119">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b86ab-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b86ab-120">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b86ab-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b86ab-121">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="b86ab-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="b86ab-122">Notes</span><span class="sxs-lookup"><span data-stu-id="b86ab-122">Remarks</span></span>

<span data-ttu-id="b86ab-123">Cette méthode peut être utilisée à la place de presque tous les appels d’API de jeu d’effets.</span><span class="sxs-lookup"><span data-stu-id="b86ab-123">This method can be used in place of nearly all the effect set API calls.</span></span>

## <a name="requirements"></a><span data-ttu-id="b86ab-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b86ab-124">Requirements</span></span>



| <span data-ttu-id="b86ab-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b86ab-125">Requirement</span></span> | <span data-ttu-id="b86ab-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="b86ab-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b86ab-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="b86ab-127">Header</span></span><br/>  | <dl> <span data-ttu-id="b86ab-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="b86ab-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="b86ab-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b86ab-129">Library</span></span><br/> | <dl> <span data-ttu-id="b86ab-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b86ab-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b86ab-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b86ab-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b86ab-132">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="b86ab-132">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="b86ab-133">**GetValue**</span><span class="sxs-lookup"><span data-stu-id="b86ab-133">**GetValue**</span></span>](id3dxbaseeffect--getvalue.md)
</dt> </dl>

 

 
