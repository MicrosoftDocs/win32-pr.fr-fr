---
description: Extrait les vecteurs de base de la moyenne et de l’analyse des composants principaux (PCA) pour un cluster donné à partir d’une mémoire tampon de données compressées ID3DXPRTCompBuffer.
ms.assetid: dcb1372f-2c8f-4d18-9840-5982b2ed0d6e
title: 'ID3DXPRTCompBuffer :: ExtractBasis, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractBasis
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ebedef91c9f3d1e277a099ffd295903e9ba77ba8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531557"
---
# <a name="id3dxprtcompbufferextractbasis-method"></a><span data-ttu-id="c3705-103">ID3DXPRTCompBuffer :: ExtractBasis, méthode</span><span class="sxs-lookup"><span data-stu-id="c3705-103">ID3DXPRTCompBuffer::ExtractBasis method</span></span>

<span data-ttu-id="c3705-104">Extrait les vecteurs de base de la moyenne et de l’analyse des composants principaux (PCA) pour un cluster donné à partir d’une mémoire tampon de données compressées [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="c3705-104">Extracts the mean and principal component analysis (PCA) basis vectors for a given cluster from an [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) compressed data buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3705-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c3705-105">Syntax</span></span>


```C++
HRESULT ExtractBasis(
  [in]      UINT  Cluster,
  [in, out] FLOAT *pClusterBasis
);
```



## <a name="parameters"></a><span data-ttu-id="c3705-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c3705-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3705-107">*Cluster* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c3705-107">*Cluster* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3705-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c3705-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c3705-109">Cluster pour lequel la base sera extraite.</span><span class="sxs-lookup"><span data-stu-id="c3705-109">Cluster for which the basis will be extracted.</span></span>

</dd> <dt>

<span data-ttu-id="c3705-110">*pClusterBasis* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c3705-110">*pClusterBasis* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c3705-111">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c3705-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c3705-112">Pointeur vers un tableau de données vectorielles de base pour le cluster.</span><span class="sxs-lookup"><span data-stu-id="c3705-112">Pointer to an array of basis vector data for Cluster.</span></span> <span data-ttu-id="c3705-113">La taille des données FLOAT stockées est : (1 + nombre de vecteurs PCA par cluster) \* (nombre de coefficients) (nombre de \* canaux de couleur)</span><span class="sxs-lookup"><span data-stu-id="c3705-113">The size of the FLOAT data stored will be: (1 + Number of PCA vectors per cluster) \* (Number of coefficients) \* (Number of color channels)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3705-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c3705-114">Return value</span></span>

<span data-ttu-id="c3705-115">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c3705-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c3705-116">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c3705-116">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="c3705-117">Si la méthode échoue, la valeur suivante est retournée.</span><span class="sxs-lookup"><span data-stu-id="c3705-117">If the method fails, the following value will be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3705-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c3705-118">Requirements</span></span>



| <span data-ttu-id="c3705-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c3705-119">Requirement</span></span> | <span data-ttu-id="c3705-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3705-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c3705-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="c3705-121">Header</span></span><br/>  | <dl> <span data-ttu-id="c3705-122"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3705-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="c3705-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c3705-123">Library</span></span><br/> | <dl> <span data-ttu-id="c3705-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c3705-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c3705-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3705-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3705-126">ID3DXPRTCompBuffer</span><span class="sxs-lookup"><span data-stu-id="c3705-126">ID3DXPRTCompBuffer</span></span>](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
