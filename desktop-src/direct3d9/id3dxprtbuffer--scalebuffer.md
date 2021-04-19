---
description: Multiplie chaque valeur de la mémoire tampon par une valeur de constante.
ms.assetid: 3d7ef530-b83a-4123-a2ed-fff2b21378ee
title: 'ID3DXPRTBuffer :: ScaleBuffer, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.ScaleBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 05bdd066f4b7c33ad06f089551f16f0489608c83
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531582"
---
# <a name="id3dxprtbufferscalebuffer-method"></a><span data-ttu-id="177c0-103">ID3DXPRTBuffer :: ScaleBuffer, méthode</span><span class="sxs-lookup"><span data-stu-id="177c0-103">ID3DXPRTBuffer::ScaleBuffer method</span></span>

<span data-ttu-id="177c0-104">Multiplie chaque valeur de la mémoire tampon par une valeur de constante.</span><span class="sxs-lookup"><span data-stu-id="177c0-104">Multiplies every value in the buffer by a constant value.</span></span>

## <a name="syntax"></a><span data-ttu-id="177c0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="177c0-105">Syntax</span></span>


```C++
HRESULT ScaleBuffer(
  [in] FLOAT Scale
);
```



## <a name="parameters"></a><span data-ttu-id="177c0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="177c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="177c0-107">Mise à l' *échelle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="177c0-107">*Scale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="177c0-108">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="177c0-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="177c0-109">Valeur constante utilisée pour mettre à l’échelle la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="177c0-109">Constant value used to scale the buffer.</span></span> <span data-ttu-id="177c0-110">Chaque valeur de la mémoire tampon est remplacée par le produit de cette valeur et par la valeur de la mémoire tampon d’origine.</span><span class="sxs-lookup"><span data-stu-id="177c0-110">Every value in the buffer is replaced by the product of this value and the original buffer value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="177c0-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="177c0-111">Return value</span></span>

<span data-ttu-id="177c0-112">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="177c0-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="177c0-113">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="177c0-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="177c0-114">Si la méthode échoue, la valeur suivante est retournée.</span><span class="sxs-lookup"><span data-stu-id="177c0-114">If the method fails, the following value will be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="177c0-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="177c0-115">Requirements</span></span>



| <span data-ttu-id="177c0-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="177c0-116">Requirement</span></span> | <span data-ttu-id="177c0-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="177c0-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="177c0-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="177c0-118">Header</span></span><br/>  | <dl> <span data-ttu-id="177c0-119"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="177c0-119"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="177c0-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="177c0-120">Library</span></span><br/> | <dl> <span data-ttu-id="177c0-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="177c0-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="177c0-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="177c0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="177c0-123">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="177c0-123">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> </dl>

 

 
