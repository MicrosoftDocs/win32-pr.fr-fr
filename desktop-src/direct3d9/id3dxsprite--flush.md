---
description: 'Force tous les sprites regroupés par lot à être envoyés à l’appareil. Les États des appareils restent tels qu’ils étaient après le dernier appel à ID3DXSprite :: Begin. La liste des sprites regroupés par lot est alors effacée.'
ms.assetid: e5717bde-e339-4344-8ce7-b0c3fe118887
title: 'ID3DXSprite :: Flush, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.Flush
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3bcd89984672f0dcfa2df120ede1abdfee23d171
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535185"
---
# <a name="id3dxspriteflush-method"></a><span data-ttu-id="da79b-105">ID3DXSprite :: Flush, méthode</span><span class="sxs-lookup"><span data-stu-id="da79b-105">ID3DXSprite::Flush method</span></span>

<span data-ttu-id="da79b-106">Force tous les sprites regroupés par lot à être envoyés à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="da79b-106">Forces all batched sprites to be submitted to the device.</span></span> <span data-ttu-id="da79b-107">Les États des appareils restent tels qu’ils étaient après le dernier appel à [**ID3DXSprite :: Begin**](id3dxsprite--begin.md).</span><span class="sxs-lookup"><span data-stu-id="da79b-107">Device states remain as they were after the last call to [**ID3DXSprite::Begin**](id3dxsprite--begin.md).</span></span> <span data-ttu-id="da79b-108">La liste des sprites regroupés par lot est alors effacée.</span><span class="sxs-lookup"><span data-stu-id="da79b-108">The list of batched sprites is then cleared.</span></span>

## <a name="syntax"></a><span data-ttu-id="da79b-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="da79b-109">Syntax</span></span>


```C++
HRESULT Flush();
```



## <a name="parameters"></a><span data-ttu-id="da79b-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="da79b-110">Parameters</span></span>

<span data-ttu-id="da79b-111">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="da79b-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="da79b-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="da79b-112">Return value</span></span>

<span data-ttu-id="da79b-113">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="da79b-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="da79b-114">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="da79b-114">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="da79b-115">Si la méthode échoue, la valeur suivante est retournée. D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="da79b-115">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="requirements"></a><span data-ttu-id="da79b-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="da79b-116">Requirements</span></span>



| <span data-ttu-id="da79b-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="da79b-117">Requirement</span></span> | <span data-ttu-id="da79b-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="da79b-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="da79b-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="da79b-119">Header</span></span><br/>  | <dl> <span data-ttu-id="da79b-120"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="da79b-120"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="da79b-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="da79b-121">Library</span></span><br/> | <dl> <span data-ttu-id="da79b-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="da79b-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="da79b-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da79b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da79b-124">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="da79b-124">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> <dt>

[<span data-ttu-id="da79b-125">**ID3DXSprite :: fin**</span><span class="sxs-lookup"><span data-stu-id="da79b-125">**ID3DXSprite::End**</span></span>](id3dxsprite--end.md)
</dt> </dl>

 

 




