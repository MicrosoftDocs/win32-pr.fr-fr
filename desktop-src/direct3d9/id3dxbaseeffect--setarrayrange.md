---
description: Définissez la plage d’un tableau à transmettre à l’appareil.
ms.assetid: 43f1c258-770c-4756-9033-e5667b379fe6
title: 'ID3DXBaseEffect :: SetArrayRange, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetArrayRange
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 59b981c1f2aff18d4bdb57f5726136945203f5fe
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116170"
---
# <a name="id3dxbaseeffectsetarrayrange-method"></a><span data-ttu-id="ae9fb-103">ID3DXBaseEffect :: SetArrayRange, méthode</span><span class="sxs-lookup"><span data-stu-id="ae9fb-103">ID3DXBaseEffect::SetArrayRange method</span></span>

<span data-ttu-id="ae9fb-104">Définissez la plage d’un tableau à transmettre à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ae9fb-104">Set the range of an array to pass to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae9fb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ae9fb-105">Syntax</span></span>


```C++
HRESULT SetArrayRange(
  [in] D3DXHANDLE hParameter,
  [in] UINT       Start,
  [in] UINT       Stop
);
```



## <a name="parameters"></a><span data-ttu-id="ae9fb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ae9fb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae9fb-107">*hParameter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ae9fb-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae9fb-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="ae9fb-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="ae9fb-109">Identificateur unique.</span><span class="sxs-lookup"><span data-stu-id="ae9fb-109">Unique identifier.</span></span> <span data-ttu-id="ae9fb-110">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="ae9fb-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae9fb-111">*Démarrer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ae9fb-111">*Start* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae9fb-112">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ae9fb-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ae9fb-113">Index de début.</span><span class="sxs-lookup"><span data-stu-id="ae9fb-113">Start index.</span></span>

</dd> <dt>

<span data-ttu-id="ae9fb-114">*Arrêter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ae9fb-114">*Stop* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae9fb-115">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ae9fb-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ae9fb-116">Arrêter l’index.</span><span class="sxs-lookup"><span data-stu-id="ae9fb-116">Stop index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae9fb-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ae9fb-117">Return value</span></span>

<span data-ttu-id="ae9fb-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ae9fb-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ae9fb-119">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ae9fb-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ae9fb-120">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="ae9fb-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae9fb-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ae9fb-121">Requirements</span></span>



| <span data-ttu-id="ae9fb-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ae9fb-122">Requirement</span></span> | <span data-ttu-id="ae9fb-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="ae9fb-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae9fb-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="ae9fb-124">Header</span></span><br/>  | <dl> <span data-ttu-id="ae9fb-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae9fb-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="ae9fb-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ae9fb-126">Library</span></span><br/> | <dl> <span data-ttu-id="ae9fb-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ae9fb-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ae9fb-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae9fb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae9fb-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="ae9fb-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
