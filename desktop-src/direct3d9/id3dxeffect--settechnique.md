---
description: Définit la technique active.
ms.assetid: 18f19773-a9f8-47f9-9334-acc95e0f0eb7
title: 'ID3DXEffect :: SetTechnique, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.SetTechnique
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e93fbff9eb74e8885675b7ccf4ea69cc53d5da53
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953810"
---
# <a name="id3dxeffectsettechnique-method"></a><span data-ttu-id="1702c-103">ID3DXEffect :: SetTechnique, méthode</span><span class="sxs-lookup"><span data-stu-id="1702c-103">ID3DXEffect::SetTechnique method</span></span>

<span data-ttu-id="1702c-104">Définit la technique active.</span><span class="sxs-lookup"><span data-stu-id="1702c-104">Sets the active technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="1702c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1702c-105">Syntax</span></span>


```C++
HRESULT SetTechnique(
  [in] D3DXHANDLE hTechnique
);
```



## <a name="parameters"></a><span data-ttu-id="1702c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1702c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1702c-107">*hTechnique* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1702c-107">*hTechnique* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1702c-108">Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="1702c-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="1702c-109">Handle unique de la technique.</span><span class="sxs-lookup"><span data-stu-id="1702c-109">Unique handle to the technique.</span></span> <span data-ttu-id="1702c-110">Consultez [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="1702c-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1702c-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1702c-111">Return value</span></span>

<span data-ttu-id="1702c-112">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1702c-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1702c-113">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1702c-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="1702c-114">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="1702c-114">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="1702c-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1702c-115">Requirements</span></span>



| <span data-ttu-id="1702c-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1702c-116">Requirement</span></span> | <span data-ttu-id="1702c-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="1702c-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1702c-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="1702c-118">Header</span></span><br/>  | <dl> <span data-ttu-id="1702c-119"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="1702c-119"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="1702c-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1702c-120">Library</span></span><br/> | <dl> <span data-ttu-id="1702c-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1702c-121"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="1702c-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1702c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1702c-123">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="1702c-123">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 




