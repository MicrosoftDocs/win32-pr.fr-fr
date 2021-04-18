---
description: Extrait les coefficients de projection de l’analyse des composants principaux (PCA) par exemple à partir d’un tampon de données compressées ID3DXPRTCompBuffer.
ms.assetid: 149098c2-35ca-46e9-a13a-94906c95cfd9
title: 'ID3DXPRTCompBuffer :: ExtractPCA, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractPCA
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6ef949e9f88a843f4636643dadd7d00ffd94d98b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522942"
---
# <a name="id3dxprtcompbufferextractpca-method"></a><span data-ttu-id="edb25-103">ID3DXPRTCompBuffer :: ExtractPCA, méthode</span><span class="sxs-lookup"><span data-stu-id="edb25-103">ID3DXPRTCompBuffer::ExtractPCA method</span></span>

<span data-ttu-id="edb25-104">Extrait les coefficients de projection de l’analyse des composants principaux (PCA) par exemple à partir d’un tampon de données compressées [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="edb25-104">Extracts the per-sample principal component analysis (PCA) projection coefficients from an [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) compressed data buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="edb25-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="edb25-105">Syntax</span></span>


```C++
HRESULT ExtractPCA(
  [in] UINT  StartPCA,
  [in] UINT  NumExtract,
  [in] FLOAT *pPCACoefficients
);
```



## <a name="parameters"></a><span data-ttu-id="edb25-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="edb25-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edb25-107">*StartPCA* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="edb25-107">*StartPCA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edb25-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="edb25-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="edb25-109">Index de départ pour les coefficients de projection PCA à extraire de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="edb25-109">Starting index for PCA projection coefficients to extract from the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="edb25-110">*NumExtract* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="edb25-110">*NumExtract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edb25-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="edb25-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="edb25-112">Nombre de coefficients de projection PCA à extraire de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="edb25-112">Number of PCA projection coefficients to extract from the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="edb25-113">*pPCACoefficients* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="edb25-113">*pPCACoefficients* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edb25-114">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="edb25-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="edb25-115">Pointeur vers l’emplacement où les coefficients d’analyse des composants principaux en cluster (CPCA) sont écrits.</span><span class="sxs-lookup"><span data-stu-id="edb25-115">Pointer to the location where clustered principal component analysis (CPCA) coefficients are written.</span></span> <span data-ttu-id="edb25-116">La taille des données écrites est (nombre d’échantillons) \* (nombre de coefficients de l’APC).</span><span class="sxs-lookup"><span data-stu-id="edb25-116">The size of the data written is (Number of Samples) \* (Number of PCA Coefficients).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edb25-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="edb25-117">Return value</span></span>

<span data-ttu-id="edb25-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="edb25-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="edb25-119">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="edb25-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="edb25-120">Si la méthode échoue, la valeur suivante est retournée.</span><span class="sxs-lookup"><span data-stu-id="edb25-120">If the method fails, the following value will be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="edb25-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="edb25-121">Requirements</span></span>



| <span data-ttu-id="edb25-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="edb25-122">Requirement</span></span> | <span data-ttu-id="edb25-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="edb25-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="edb25-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="edb25-124">Header</span></span><br/>  | <dl> <span data-ttu-id="edb25-125"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="edb25-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="edb25-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="edb25-126">Library</span></span><br/> | <dl> <span data-ttu-id="edb25-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="edb25-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="edb25-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="edb25-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edb25-129">ID3DXPRTCompBuffer</span><span class="sxs-lookup"><span data-stu-id="edb25-129">ID3DXPRTCompBuffer</span></span>](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
