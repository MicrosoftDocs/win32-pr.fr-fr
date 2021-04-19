---
description: 'Forcer l’envoi de tous les sprites par lot à l’appareil. Les États des appareils restent tels qu’ils étaient après le dernier appel à ID3DX10Sprite :: Begin. La liste des sprites regroupés par lot est alors effacée.'
ms.assetid: ae03e17c-1a14-4a41-a9a9-8757d2f7a81d
title: 'ID3DX10Sprite :: Flush, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.Flush
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 748be56a7b89223db1957b9c0144143edd90ee4c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106532694"
---
# <a name="id3dx10spriteflush-method"></a><span data-ttu-id="81d94-105">ID3DX10Sprite :: Flush, méthode</span><span class="sxs-lookup"><span data-stu-id="81d94-105">ID3DX10Sprite::Flush method</span></span>

<span data-ttu-id="81d94-106">Forcer l’envoi de tous les sprites par lot à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="81d94-106">Force all batched sprites to be submitted to the device.</span></span> <span data-ttu-id="81d94-107">Les États des appareils restent tels qu’ils étaient après le dernier appel à ID3DX10Sprite :: Begin.</span><span class="sxs-lookup"><span data-stu-id="81d94-107">Device states remain as they were after the last call to ID3DX10Sprite::Begin.</span></span> <span data-ttu-id="81d94-108">La liste des sprites regroupés par lot est alors effacée.</span><span class="sxs-lookup"><span data-stu-id="81d94-108">The list of batched sprites is then cleared.</span></span>

## <a name="syntax"></a><span data-ttu-id="81d94-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="81d94-109">Syntax</span></span>


```C++
HRESULT Flush();
```



## <a name="parameters"></a><span data-ttu-id="81d94-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="81d94-110">Parameters</span></span>

<span data-ttu-id="81d94-111">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="81d94-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="81d94-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="81d94-112">Return value</span></span>

<span data-ttu-id="81d94-113">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="81d94-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="81d94-114">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="81d94-114">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="81d94-115">Si la méthode échoue, la valeur suivante est retournée : D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="81d94-115">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="81d94-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="81d94-116">Requirements</span></span>



| <span data-ttu-id="81d94-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="81d94-117">Requirement</span></span> | <span data-ttu-id="81d94-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="81d94-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="81d94-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="81d94-119">Header</span></span><br/>  | <dl> <span data-ttu-id="81d94-120"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="81d94-120"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="81d94-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="81d94-121">Library</span></span><br/> | <dl> <span data-ttu-id="81d94-122"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="81d94-122"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81d94-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81d94-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81d94-124">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="81d94-124">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="81d94-125">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="81d94-125">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




