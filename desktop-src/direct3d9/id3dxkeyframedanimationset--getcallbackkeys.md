---
description: 'ID3DXKeyframedAnimationSet :: GetCallbackKeys, méthode-remplit un tableau avec les données de clé de rappel utilisées pour l’animation d’image clé.'
ms.assetid: 2a2aa04a-a889-415b-8aa2-cc5f2bed1f9a
title: 'ID3DXKeyframedAnimationSet :: GetCallbackKeys, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetCallbackKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5f3bdb7049de3b5d6aad10b5ff5100d01d05e3ee
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093717"
---
# <a name="id3dxkeyframedanimationsetgetcallbackkeys-method"></a><span data-ttu-id="abdf2-103">ID3DXKeyframedAnimationSet :: GetCallbackKeys, méthode</span><span class="sxs-lookup"><span data-stu-id="abdf2-103">ID3DXKeyframedAnimationSet::GetCallbackKeys method</span></span>

<span data-ttu-id="abdf2-104">Remplit un tableau avec les données de clé de rappel utilisées pour l’animation d’image clé.</span><span class="sxs-lookup"><span data-stu-id="abdf2-104">Fills an array with callback key data used for key frame animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="abdf2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="abdf2-105">Syntax</span></span>


```C++
HRESULT GetCallbackKeys(
  [out] LPD3DXKEY_CALLBACK pCallbackKeys
);
```



## <a name="parameters"></a><span data-ttu-id="abdf2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="abdf2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abdf2-107">*pCallbackKeys* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="abdf2-107">*pCallbackKeys* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="abdf2-108">Type : **[ **\_ rappel LPD3DXKEY**](d3dxkey-callback.md)**</span><span class="sxs-lookup"><span data-stu-id="abdf2-108">Type: **[**LPD3DXKEY\_CALLBACK**](d3dxkey-callback.md)**</span></span>

<span data-ttu-id="abdf2-109">Pointeur vers un tableau alloué par l’utilisateur de structures de [**\_ rappel D3DXKEY**](d3dxkey-callback.md) que la méthode doit remplir avec les données de rappel.</span><span class="sxs-lookup"><span data-stu-id="abdf2-109">Pointer to a user-allocated array of [**D3DXKEY\_CALLBACK**](d3dxkey-callback.md) structures that the method is to fill with callback data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abdf2-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="abdf2-110">Return value</span></span>

<span data-ttu-id="abdf2-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="abdf2-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="abdf2-112">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="abdf2-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="abdf2-113">Si la méthode échoue, la valeur suivante est retournée : D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="abdf2-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="abdf2-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="abdf2-114">Requirements</span></span>



| <span data-ttu-id="abdf2-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="abdf2-115">Requirement</span></span> | <span data-ttu-id="abdf2-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="abdf2-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="abdf2-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="abdf2-117">Header</span></span><br/>  | <dl> <span data-ttu-id="abdf2-118"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="abdf2-118"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="abdf2-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="abdf2-119">Library</span></span><br/> | <dl> <span data-ttu-id="abdf2-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="abdf2-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="abdf2-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="abdf2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abdf2-122">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="abdf2-122">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> <dt>

[<span data-ttu-id="abdf2-123">**ID3DXKeyframedAnimationSet::GetNumCallbackKeys**</span><span class="sxs-lookup"><span data-stu-id="abdf2-123">**ID3DXKeyframedAnimationSet::GetNumCallbackKeys**</span></span>](id3dxkeyframedanimationset--getnumcallbackkeys.md)
</dt> </dl>

 

 




