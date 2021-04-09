---
description: Extrait les coefficients de projection de l’analyse des composants principaux (PCA) par exemple à partir d’un tampon de données compressées ID3DXPRTCompBuffer et ajoute les données à un objet IDirect3DTexture9.
ms.assetid: 2159e57d-b8e5-421f-b20a-ac58b29e3c45
title: 'ID3DXPRTCompBuffer :: ExtractTexture, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractTexture
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a6a2200c680c19019375a5e33d2d8b675992dc38
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104043130"
---
# <a name="id3dxprtcompbufferextracttexture-method"></a><span data-ttu-id="40818-103">ID3DXPRTCompBuffer :: ExtractTexture, méthode</span><span class="sxs-lookup"><span data-stu-id="40818-103">ID3DXPRTCompBuffer::ExtractTexture method</span></span>

<span data-ttu-id="40818-104">Extrait les coefficients de projection de l’analyse des composants principaux (PCA) par exemple à partir d’un tampon de données compressées [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) et ajoute les données à un objet [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) .</span><span class="sxs-lookup"><span data-stu-id="40818-104">Extracts the per-sample principal component analysis (PCA) projection coefficients from an [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) compressed data buffer and adds the data to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="40818-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="40818-105">Syntax</span></span>


```C++
HRESULT ExtractTexture(
  [in] UINT               StartPCA,
  [in] UINT               NumPCA,
  [in] LPDIRECT3DTEXTURE9 pTexture
);
```



## <a name="parameters"></a><span data-ttu-id="40818-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="40818-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40818-107">*StartPCA* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="40818-107">*StartPCA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40818-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="40818-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="40818-109">Valeur de départ du coefficient de mémoire tampon à partir duquel extraire les données de texture.</span><span class="sxs-lookup"><span data-stu-id="40818-109">Starting value of the buffer coefficient from which to extract texture data.</span></span>

</dd> <dt>

<span data-ttu-id="40818-110">*NumPCA* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="40818-110">*NumPCA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40818-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="40818-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="40818-112">Nombre de coefficients d’APC à extraire de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="40818-112">Number of PCA coefficients to extract from the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="40818-113">*pTexture* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="40818-113">*pTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40818-114">Type : **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="40818-114">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="40818-115">Pointeur vers un objet de texture [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) qui stocke les coefficients de l’APC.</span><span class="sxs-lookup"><span data-stu-id="40818-115">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) texture object that will store PCA coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40818-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="40818-116">Return value</span></span>

<span data-ttu-id="40818-117">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="40818-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="40818-118">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="40818-118">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="40818-119">Si la méthode échoue, la valeur suivante est retournée.</span><span class="sxs-lookup"><span data-stu-id="40818-119">If the method fails, the following value will be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="40818-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="40818-120">Requirements</span></span>



| <span data-ttu-id="40818-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="40818-121">Requirement</span></span> | <span data-ttu-id="40818-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="40818-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="40818-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="40818-123">Header</span></span><br/>  | <dl> <span data-ttu-id="40818-124"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="40818-124"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="40818-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="40818-125">Library</span></span><br/> | <dl> <span data-ttu-id="40818-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="40818-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="40818-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="40818-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40818-128">ID3DXPRTCompBuffer</span><span class="sxs-lookup"><span data-stu-id="40818-128">ID3DXPRTCompBuffer</span></span>](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
