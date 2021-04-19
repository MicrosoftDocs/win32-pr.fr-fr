---
description: Extrait les ID de cluster par exemple à partir d’un tampon de données compressées ID3DXPRTCompBuffer.
ms.assetid: d78d82ab-58bc-4b73-9ca0-8b7f06867618
title: 'ID3DXPRTCompBuffer :: ExtractClusterIDs, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractClusterIDs
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ef68a972109e89e318adb83ab388c653c6a3deed
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106537291"
---
# <a name="id3dxprtcompbufferextractclusterids-method"></a><span data-ttu-id="412bc-103">ID3DXPRTCompBuffer :: ExtractClusterIDs, méthode</span><span class="sxs-lookup"><span data-stu-id="412bc-103">ID3DXPRTCompBuffer::ExtractClusterIDs method</span></span>

<span data-ttu-id="412bc-104">Extrait les ID de cluster par exemple à partir d’un tampon de données compressées [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="412bc-104">Extracts the per-sample cluster IDs from an [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) compressed data buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="412bc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="412bc-105">Syntax</span></span>


```C++
HRESULT ExtractClusterIDs(
  [in, out] UINT *pClusterIDs
);
```



## <a name="parameters"></a><span data-ttu-id="412bc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="412bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="412bc-107">*pClusterIDs* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="412bc-107">*pClusterIDs* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="412bc-108">Type : **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="412bc-108">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="412bc-109">Pointeur vers l’emplacement dans la mémoire où les ID sont écrits.</span><span class="sxs-lookup"><span data-stu-id="412bc-109">Pointer to the location in memory where IDs are written.</span></span> <span data-ttu-id="412bc-110">La longueur de la mémoire requise est la valeur retournée par [**ID3DXPRTCompBuffer :: GetNumSamples**](id3dxprtcompbuffer--getnumsamples.md).</span><span class="sxs-lookup"><span data-stu-id="412bc-110">The length of memory required is the value returned by [**ID3DXPRTCompBuffer::GetNumSamples**](id3dxprtcompbuffer--getnumsamples.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="412bc-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="412bc-111">Return value</span></span>

<span data-ttu-id="412bc-112">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="412bc-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="412bc-113">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="412bc-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="412bc-114">Si la méthode échoue, la valeur suivante est retournée.</span><span class="sxs-lookup"><span data-stu-id="412bc-114">If the method fails, the following value will be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="412bc-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="412bc-115">Requirements</span></span>



| <span data-ttu-id="412bc-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="412bc-116">Requirement</span></span> | <span data-ttu-id="412bc-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="412bc-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="412bc-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="412bc-118">Header</span></span><br/>  | <dl> <span data-ttu-id="412bc-119"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="412bc-119"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="412bc-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="412bc-120">Library</span></span><br/> | <dl> <span data-ttu-id="412bc-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="412bc-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="412bc-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="412bc-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="412bc-123">ID3DXPRTCompBuffer</span><span class="sxs-lookup"><span data-stu-id="412bc-123">ID3DXPRTCompBuffer</span></span>](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
