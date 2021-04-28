---
description: 'ID3DXCompressedAnimationSet :: GetCallbackKeys, méthode-remplit un tableau avec les données de clé de rappel utilisées pour l’animation d’image clé.'
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
ms.openlocfilehash: d7c430358b5ba7f66c5a79b08ae01925141e659f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115327"
---
# <a name="id3dxcompressedanimationsetgetcallbackkeys-method"></a><span data-ttu-id="12047-103">ID3DXCompressedAnimationSet :: GetCallbackKeys, méthode</span><span class="sxs-lookup"><span data-stu-id="12047-103">ID3DXCompressedAnimationSet::GetCallbackKeys method</span></span>

<span data-ttu-id="12047-104">Remplit un tableau avec les données de clé de rappel utilisées pour l’animation d’image clé.</span><span class="sxs-lookup"><span data-stu-id="12047-104">Fills an array with callback key data used for key frame animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="12047-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="12047-105">Syntax</span></span>


```C++
HRESULT GetCallbackKeys(
  [out] LPD3DXKEY_CALLBACK pCallbackKeys
);
```



## <a name="parameters"></a><span data-ttu-id="12047-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="12047-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12047-107">*pCallbackKeys* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="12047-107">*pCallbackKeys* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="12047-108">Type : **[ **\_ rappel LPD3DXKEY**](d3dxkey-callback.md)**</span><span class="sxs-lookup"><span data-stu-id="12047-108">Type: **[**LPD3DXKEY\_CALLBACK**](d3dxkey-callback.md)**</span></span>

<span data-ttu-id="12047-109">Pointeur vers un tableau alloué par l’utilisateur de structures de [**\_ rappel D3DXKEY**](d3dxkey-callback.md) que la méthode doit remplir avec les données de rappel.</span><span class="sxs-lookup"><span data-stu-id="12047-109">Pointer to a user-allocated array of [**D3DXKEY\_CALLBACK**](d3dxkey-callback.md) structures that the method is to fill with callback data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12047-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="12047-110">Return value</span></span>

<span data-ttu-id="12047-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="12047-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="12047-112">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="12047-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="12047-113">Si la méthode échoue, la valeur suivante est retournée : D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="12047-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="12047-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="12047-114">Requirements</span></span>



| <span data-ttu-id="12047-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="12047-115">Requirement</span></span> | <span data-ttu-id="12047-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="12047-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="12047-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="12047-117">Header</span></span><br/>  | <dl> <span data-ttu-id="12047-118"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="12047-118"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="12047-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="12047-119">Library</span></span><br/> | <dl> <span data-ttu-id="12047-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="12047-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="12047-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12047-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12047-122">ID3DXCompressedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="12047-122">ID3DXCompressedAnimationSet</span></span>](id3dxcompressedanimationset.md)
</dt> <dt>

[<span data-ttu-id="12047-123">**ID3DXCompressedAnimationSet::GetNumCallbackKeys**</span><span class="sxs-lookup"><span data-stu-id="12047-123">**ID3DXCompressedAnimationSet::GetNumCallbackKeys**</span></span>](id3dxcompressedanimationset--getnumcallbackkeys.md)
</dt> </dl>

 

 




