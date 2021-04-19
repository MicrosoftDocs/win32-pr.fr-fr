---
description: Normalise tous les pondérations de l’analyse des composants principaux (PCA) afin qu’elles soient comprises entre-1 et 1. Les vecteurs de base sont modifiés pour refléter cette normalisation.
ms.assetid: f1c87049-a1ec-452e-b556-a2dc95324d5d
title: 'ID3DXPRTCompBuffer :: NormalizeData, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.NormalizeData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9a69dacb25d04b56a14e27a43487911e56a038ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106528572"
---
# <a name="id3dxprtcompbuffernormalizedata-method"></a><span data-ttu-id="ae835-104">ID3DXPRTCompBuffer :: NormalizeData, méthode</span><span class="sxs-lookup"><span data-stu-id="ae835-104">ID3DXPRTCompBuffer::NormalizeData method</span></span>

<span data-ttu-id="ae835-105">Normalise tous les pondérations de l’analyse des composants principaux (PCA) afin qu’elles soient comprises entre-1 et 1.</span><span class="sxs-lookup"><span data-stu-id="ae835-105">Normalizes all principal component analysis (PCA) weights so that they are between -1 and 1.</span></span> <span data-ttu-id="ae835-106">Les vecteurs de base sont modifiés pour refléter cette normalisation.</span><span class="sxs-lookup"><span data-stu-id="ae835-106">Basis vectors are modified to reflect this normalization.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae835-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ae835-107">Syntax</span></span>


```C++
HRESULT NormalizeData();
```



## <a name="parameters"></a><span data-ttu-id="ae835-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ae835-108">Parameters</span></span>

<span data-ttu-id="ae835-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="ae835-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ae835-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ae835-110">Return value</span></span>

<span data-ttu-id="ae835-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ae835-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ae835-112">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ae835-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ae835-113">Si la méthode échoue, la valeur suivante est retournée.</span><span class="sxs-lookup"><span data-stu-id="ae835-113">If the method fails, the following value will be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae835-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ae835-114">Requirements</span></span>



| <span data-ttu-id="ae835-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ae835-115">Requirement</span></span> | <span data-ttu-id="ae835-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="ae835-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae835-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="ae835-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ae835-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae835-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="ae835-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ae835-119">Library</span></span><br/> | <dl> <span data-ttu-id="ae835-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ae835-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ae835-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae835-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae835-122">ID3DXPRTCompBuffer</span><span class="sxs-lookup"><span data-stu-id="ae835-122">ID3DXPRTCompBuffer</span></span>](id3dxprtcompbuffer.md)
</dt> </dl>

 

 




