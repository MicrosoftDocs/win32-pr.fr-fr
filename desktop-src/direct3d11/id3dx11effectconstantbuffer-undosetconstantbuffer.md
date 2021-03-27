---
title: Méthode ID3DX11EffectConstantBuffer UndoSetConstantBuffer (D3dx11effect. h)
description: Restaure une mémoire tampon constante définie précédemment.
ms.assetid: 6c5e1256-3a92-4bfe-8614-f09d627bc3db
keywords:
- Méthode UndoSetConstantBuffer Direct3D 11
- Méthode UndoSetConstantBuffer Direct3D 11, interface ID3DX11EffectConstantBuffer
- Interface ID3DX11EffectConstantBuffer Direct3D 11, méthode UndoSetConstantBuffer
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer.UndoSetConstantBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c95a26f1ea92d5bfe1975e3fe4dc1961046e5535
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394223"
---
# <a name="id3dx11effectconstantbufferundosetconstantbuffer-method"></a><span data-ttu-id="5ec3d-106">ID3DX11EffectConstantBuffer :: UndoSetConstantBuffer, méthode</span><span class="sxs-lookup"><span data-stu-id="5ec3d-106">ID3DX11EffectConstantBuffer::UndoSetConstantBuffer method</span></span>

<span data-ttu-id="5ec3d-107">Restaure une mémoire tampon constante définie précédemment.</span><span class="sxs-lookup"><span data-stu-id="5ec3d-107">Reverts a previously set constant buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ec3d-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5ec3d-108">Syntax</span></span>


```C++
HRESULT UndoSetConstantBuffer();
```



## <a name="parameters"></a><span data-ttu-id="5ec3d-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5ec3d-109">Parameters</span></span>

<span data-ttu-id="5ec3d-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="5ec3d-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5ec3d-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5ec3d-111">Return value</span></span>

<span data-ttu-id="5ec3d-112">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5ec3d-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5ec3d-113">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="5ec3d-113">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5ec3d-114">Notes</span><span class="sxs-lookup"><span data-stu-id="5ec3d-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5ec3d-115">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="5ec3d-115">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="5ec3d-116">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="5ec3d-116">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="5ec3d-117">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="5ec3d-117">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5ec3d-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="5ec3d-118">Requirements</span></span>



| <span data-ttu-id="5ec3d-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5ec3d-119">Requirement</span></span> | <span data-ttu-id="5ec3d-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="5ec3d-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ec3d-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="5ec3d-121">Header</span></span><br/>  | <dl> <span data-ttu-id="5ec3d-122"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ec3d-122"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="5ec3d-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5ec3d-123">Library</span></span><br/> | <dl> <span data-ttu-id="5ec3d-124"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="5ec3d-124"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ec3d-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ec3d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ec3d-126">ID3DX11EffectConstantBuffer</span><span class="sxs-lookup"><span data-stu-id="5ec3d-126">ID3DX11EffectConstantBuffer</span></span>](id3dx11effectconstantbuffer.md)
</dt> </dl>

 

 





