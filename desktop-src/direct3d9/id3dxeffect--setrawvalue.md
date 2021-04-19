---
description: Définissez une plage contiguë de constantes de nuanceur avec une copie de mémoire.
ms.assetid: 8a3b5141-c67a-45b9-91c2-1877642164e3
title: 'ID3DXEffect :: SetRawValue, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.SetRawValue
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: cc3ce5eb547032ced5d0d79c533cefd1d2daab3a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106543768"
---
# <a name="id3dxeffectsetrawvalue-method"></a><span data-ttu-id="f0b8c-103">ID3DXEffect :: SetRawValue, méthode</span><span class="sxs-lookup"><span data-stu-id="f0b8c-103">ID3DXEffect::SetRawValue method</span></span>

<span data-ttu-id="f0b8c-104">Définissez une plage contiguë de constantes de nuanceur avec une copie de mémoire.</span><span class="sxs-lookup"><span data-stu-id="f0b8c-104">Set a contiguous range of shader constants with a memory copy.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0b8c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f0b8c-105">Syntax</span></span>


```C++
HRESULT SetRawValue(
  [in] D3DXHANDLE Handle,
  [in] void       *pData,
  [in] DWORD      OffsetInBytes,
  [in] DWORD      Bytes
);
```



## <a name="parameters"></a><span data-ttu-id="f0b8c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f0b8c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0b8c-107">*Gérer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f0b8c-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0b8c-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="f0b8c-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="f0b8c-109">Handle de la valeur à définir, ou nom de la valeur transmise en tant que chaîne.</span><span class="sxs-lookup"><span data-stu-id="f0b8c-109">Handle to the value to set, or the name of the value passed in as a string.</span></span> <span data-ttu-id="f0b8c-110">Le passage d’un handle est plus efficace.</span><span class="sxs-lookup"><span data-stu-id="f0b8c-110">Passing in a handle is more efficient.</span></span> <span data-ttu-id="f0b8c-111">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="f0b8c-111">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="f0b8c-112">*pData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f0b8c-112">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0b8c-113">Type : **void \***</span><span class="sxs-lookup"><span data-stu-id="f0b8c-113">Type: **void\***</span></span>

<span data-ttu-id="f0b8c-114">Pointeur vers une mémoire tampon qui contient les données à définir.</span><span class="sxs-lookup"><span data-stu-id="f0b8c-114">Pointer to a buffer containing the data to be set.</span></span> <span data-ttu-id="f0b8c-115">SetRawValue vérifie la présence de mémoire valide, mais n’effectue aucune vérification des données valides.</span><span class="sxs-lookup"><span data-stu-id="f0b8c-115">SetRawValue checks for valid memory, but does not do any checking for valid data.</span></span>

</dd> <dt>

<span data-ttu-id="f0b8c-116">*OffsetInBytes* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f0b8c-116">*OffsetInBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0b8c-117">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f0b8c-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f0b8c-118">Nombre d’octets entre le début des données d’effet et le début des constantes d’effet que vous allez définir.</span><span class="sxs-lookup"><span data-stu-id="f0b8c-118">Number of bytes between the beginning of the effect data and the beginning of the effect constants you are going to set.</span></span>

</dd> <dt>

<span data-ttu-id="f0b8c-119">*Octets* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f0b8c-119">*Bytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0b8c-120">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f0b8c-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f0b8c-121">Taille de la mémoire tampon à définir, en octets.</span><span class="sxs-lookup"><span data-stu-id="f0b8c-121">The size of the buffer to be set, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0b8c-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f0b8c-122">Return value</span></span>

<span data-ttu-id="f0b8c-123">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f0b8c-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f0b8c-124">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f0b8c-124">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="f0b8c-125">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : E \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="f0b8c-125">If the method fails, the return value can be one of the following:E\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0b8c-126">Notes</span><span class="sxs-lookup"><span data-stu-id="f0b8c-126">Remarks</span></span>

<span data-ttu-id="f0b8c-127">SetRawValue est un moyen très rapide de définir des constantes d’effet, car il effectue une copie de mémoire sans effectuer de validation ou de conversion de données (comme la conversion d’une matrice de lignes principales en colonne-matrice principale).</span><span class="sxs-lookup"><span data-stu-id="f0b8c-127">SetRawValue is a very fast way to set effect constants since it performs a memory copy without performing validation or any data conversion (like converting a row-major matrix to a column-major matrix).</span></span> <span data-ttu-id="f0b8c-128">Utilisez SetRawValue pour définir une série de constantes à effet contigu.</span><span class="sxs-lookup"><span data-stu-id="f0b8c-128">Use SetRawValue to set a series of contiguous effect constants.</span></span> <span data-ttu-id="f0b8c-129">Par exemple, vous pouvez définir un tableau de vingt matrices avec 20 appels à [**ID3DXBaseEffect :: SetMatrix**](id3dxbaseeffect--setmatrix.md) ou à l’aide d’un SetRawValue unique.</span><span class="sxs-lookup"><span data-stu-id="f0b8c-129">For instance, you could set an array of twenty matrices with 20 calls to [**ID3DXBaseEffect::SetMatrix**](id3dxbaseeffect--setmatrix.md) or by using a single SetRawValue.</span></span>

<span data-ttu-id="f0b8c-130">Toutes les valeurs sont supposées être matrix4x4s ou float4s et toutes les matrices sont supposées être dans l’ordre colonne-principal.</span><span class="sxs-lookup"><span data-stu-id="f0b8c-130">All values are expected to be either matrix4x4s or float4s and all matrices are expected to be in column-major order.</span></span> <span data-ttu-id="f0b8c-131">Les valeurs int ou float sont converties en float4 ; par conséquent, il est fortement recommandé d’utiliser SetRawValue avec uniquement des données float4 ou matrix4x4.</span><span class="sxs-lookup"><span data-stu-id="f0b8c-131">Int or float values are cast into a float4; therefore, it is highly recommended that you use SetRawValue with only float4 or matrix4x4 data.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0b8c-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f0b8c-132">Requirements</span></span>



| <span data-ttu-id="f0b8c-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f0b8c-133">Requirement</span></span> | <span data-ttu-id="f0b8c-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="f0b8c-134">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0b8c-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="f0b8c-135">Header</span></span><br/>  | <dl> <span data-ttu-id="f0b8c-136"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0b8c-136"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="f0b8c-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f0b8c-137">Library</span></span><br/> | <dl> <span data-ttu-id="f0b8c-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f0b8c-138"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="f0b8c-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f0b8c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0b8c-140">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="f0b8c-140">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 
