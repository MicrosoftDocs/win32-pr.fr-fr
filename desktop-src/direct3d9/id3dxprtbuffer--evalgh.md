---
description: Applique les données de marge de texture stockées à une mémoire tampon de texture ID3DXPRTBuffer.
ms.assetid: 05cc0709-543a-4df5-980a-8549451d396b
title: 'ID3DXPRTBuffer :: EvalGH, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.EvalGH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 23896ff2514db7b5e12b164ea0c0a763b5d1d3b1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531376"
---
# <a name="id3dxprtbufferevalgh-method"></a><span data-ttu-id="e8b0e-103">ID3DXPRTBuffer :: EvalGH, méthode</span><span class="sxs-lookup"><span data-stu-id="e8b0e-103">ID3DXPRTBuffer::EvalGH method</span></span>

<span data-ttu-id="e8b0e-104">Applique les données de marge de texture stockées à une mémoire tampon de texture [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="e8b0e-104">Applies stored texture gutter data to an [**ID3DXPRTBuffer**](id3dxprtbuffer.md) texture buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8b0e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e8b0e-105">Syntax</span></span>


```C++
HRESULT EvalGH();
```



## <a name="parameters"></a><span data-ttu-id="e8b0e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e8b0e-106">Parameters</span></span>

<span data-ttu-id="e8b0e-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="e8b0e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e8b0e-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e8b0e-108">Return value</span></span>

<span data-ttu-id="e8b0e-109">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e8b0e-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e8b0e-110">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e8b0e-110">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="e8b0e-111">Si la méthode échoue, la valeur suivante est retournée.</span><span class="sxs-lookup"><span data-stu-id="e8b0e-111">If the method fails, the following value will be returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8b0e-112">Notes</span><span class="sxs-lookup"><span data-stu-id="e8b0e-112">Remarks</span></span>

<span data-ttu-id="e8b0e-113">Cette méthode effectue un appel interne à [**ID3DXTextureGutterHelper :: ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md) pour récupérer et appliquer les données de la marge de texture.</span><span class="sxs-lookup"><span data-stu-id="e8b0e-113">This method makes an internal call to [**ID3DXTextureGutterHelper::ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md) to retrieve and apply texture gutter data.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8b0e-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e8b0e-114">Requirements</span></span>



| <span data-ttu-id="e8b0e-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e8b0e-115">Requirement</span></span> | <span data-ttu-id="e8b0e-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="e8b0e-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e8b0e-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="e8b0e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="e8b0e-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8b0e-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="e8b0e-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e8b0e-119">Library</span></span><br/> | <dl> <span data-ttu-id="e8b0e-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e8b0e-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e8b0e-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e8b0e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8b0e-122">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="e8b0e-122">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> </dl>

 

 




