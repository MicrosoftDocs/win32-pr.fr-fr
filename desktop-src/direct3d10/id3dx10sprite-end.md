---
description: 'Appelez-le après ID3DX10Sprite :: Flush. Si \_ \_ \_ l’état de l’enregistrement d3dx10 Sprite a été spécifié lors de l’appel de ID3DX10Sprite :: Begin, cette API restaure l’état de l’appareil sur la manière dont il se trouvait avant l’appel de ID3DX10Sprite :: Begin.'
ms.assetid: 71645edb-be4a-4d87-9fb0-557cf5cf10e5
title: 'ID3DX10Sprite :: end, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.End
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 02d25e41916bd5d7605f3c0e1bc6e7998ea06e86
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539930"
---
# <a name="id3dx10spriteend-method"></a><span data-ttu-id="207c0-104">ID3DX10Sprite :: end, méthode</span><span class="sxs-lookup"><span data-stu-id="207c0-104">ID3DX10Sprite::End method</span></span>

<span data-ttu-id="207c0-105">Appelez-le après ID3DX10Sprite :: Flush.</span><span class="sxs-lookup"><span data-stu-id="207c0-105">Call this after ID3DX10Sprite::Flush.</span></span> <span data-ttu-id="207c0-106">Si \_ \_ \_ l’état de l’enregistrement d3dx10 Sprite a été spécifié lors de l’appel de ID3DX10Sprite :: Begin, cette API restaure l’état de l’appareil sur la manière dont il se trouvait avant l’appel de ID3DX10Sprite :: Begin.</span><span class="sxs-lookup"><span data-stu-id="207c0-106">If D3DX10\_SPRITE\_SAVE\_STATE was specified when ID3DX10Sprite::Begin was called, this API will restore the device state to how it was before ID3DX10Sprite::Begin was called.</span></span>

## <a name="syntax"></a><span data-ttu-id="207c0-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="207c0-107">Syntax</span></span>


```C++
HRESULT End();
```



## <a name="parameters"></a><span data-ttu-id="207c0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="207c0-108">Parameters</span></span>

<span data-ttu-id="207c0-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="207c0-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="207c0-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="207c0-110">Return value</span></span>

<span data-ttu-id="207c0-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="207c0-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="207c0-112">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="207c0-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="207c0-113">Si la méthode échoue, la valeur suivante est retournée : D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="207c0-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="207c0-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="207c0-114">Requirements</span></span>



| <span data-ttu-id="207c0-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="207c0-115">Requirement</span></span> | <span data-ttu-id="207c0-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="207c0-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="207c0-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="207c0-117">Header</span></span><br/>  | <dl> <span data-ttu-id="207c0-118"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="207c0-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="207c0-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="207c0-119">Library</span></span><br/> | <dl> <span data-ttu-id="207c0-120"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="207c0-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="207c0-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="207c0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="207c0-122">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="207c0-122">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="207c0-123">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="207c0-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




