---
description: Remplit un tableau avec les données de clé de rappel utilisées pour l’animation d’image clé.
ms.assetid: 0dc30c1f-9ffb-42ec-8074-84293f16c344
title: 'ID3DXCompressedAnimationSet :: GetCallbackKeys, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXCompressedAnimationSet.GetCallbackKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fe56a3dbdd7d019deb5d7111fa592470bffd244d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535181"
---
# <a name="id3dxcompressedanimationsetgetcallbackkeys-method"></a><span data-ttu-id="0cd64-103">ID3DXCompressedAnimationSet :: GetCallbackKeys, méthode</span><span class="sxs-lookup"><span data-stu-id="0cd64-103">ID3DXCompressedAnimationSet::GetCallbackKeys method</span></span>

<span data-ttu-id="0cd64-104">Remplit un tableau avec les données de clé de rappel utilisées pour l’animation d’image clé.</span><span class="sxs-lookup"><span data-stu-id="0cd64-104">Fills an array with callback key data used for key frame animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cd64-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0cd64-105">Syntax</span></span>


```C++
HRESULT GetCallbackKeys(
  [out] LPD3DXKEY_CALLBACK pCallbackKeys
);
```



## <a name="parameters"></a><span data-ttu-id="0cd64-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0cd64-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cd64-107">*pCallbackKeys* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0cd64-107">*pCallbackKeys* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0cd64-108">Type : **[ **\_ rappel LPD3DXKEY**](d3dxkey-callback.md)**</span><span class="sxs-lookup"><span data-stu-id="0cd64-108">Type: **[**LPD3DXKEY\_CALLBACK**](d3dxkey-callback.md)**</span></span>

<span data-ttu-id="0cd64-109">Pointeur vers un tableau alloué par l’utilisateur de structures de [**\_ rappel D3DXKEY**](d3dxkey-callback.md) que la méthode doit remplir avec les données de rappel.</span><span class="sxs-lookup"><span data-stu-id="0cd64-109">Pointer to a user-allocated array of [**D3DXKEY\_CALLBACK**](d3dxkey-callback.md) structures that the method is to fill with callback data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cd64-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0cd64-110">Return value</span></span>

<span data-ttu-id="0cd64-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0cd64-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0cd64-112">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0cd64-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="0cd64-113">Si la méthode échoue, la valeur suivante est retournée : D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="0cd64-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cd64-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0cd64-114">Requirements</span></span>



| <span data-ttu-id="0cd64-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0cd64-115">Requirement</span></span> | <span data-ttu-id="0cd64-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="0cd64-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0cd64-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="0cd64-117">Header</span></span><br/>  | <dl> <span data-ttu-id="0cd64-118"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="0cd64-118"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="0cd64-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0cd64-119">Library</span></span><br/> | <dl> <span data-ttu-id="0cd64-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0cd64-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0cd64-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0cd64-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cd64-122">ID3DXCompressedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="0cd64-122">ID3DXCompressedAnimationSet</span></span>](id3dxcompressedanimationset.md)
</dt> <dt>

[<span data-ttu-id="0cd64-123">**ID3DXCompressedAnimationSet::GetNumCallbackKeys**</span><span class="sxs-lookup"><span data-stu-id="0cd64-123">**ID3DXCompressedAnimationSet::GetNumCallbackKeys**</span></span>](id3dxcompressedanimationset--getnumcallbackkeys.md)
</dt> </dl>

 

 




