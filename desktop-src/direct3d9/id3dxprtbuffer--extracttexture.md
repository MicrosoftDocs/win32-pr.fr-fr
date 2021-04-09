---
description: Extrait des données de coefficient à partir d’un canal de couleur de la mémoire tampon pour une plage de coefficients spécifiée, et ajoute les données à un objet IDirect3DTexture9.
ms.assetid: 75854676-706a-4675-857e-4f2f8fc8365b
title: 'ID3DXPRTBuffer :: ExtractTexture, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.ExtractTexture
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2ea6cfdc8fb6ec83f847ccf37d06972974ea4de8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953900"
---
# <a name="id3dxprtbufferextracttexture-method"></a><span data-ttu-id="8e1ec-103">ID3DXPRTBuffer :: ExtractTexture, méthode</span><span class="sxs-lookup"><span data-stu-id="8e1ec-103">ID3DXPRTBuffer::ExtractTexture method</span></span>

<span data-ttu-id="8e1ec-104">Extrait des données de coefficient à partir d’un canal de couleur de la mémoire tampon pour une plage de coefficients spécifiée, et ajoute les données à un objet [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) .</span><span class="sxs-lookup"><span data-stu-id="8e1ec-104">Extracts coefficient data from a color channel of the buffer for a specified range of coefficients, and adds the data to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e1ec-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8e1ec-105">Syntax</span></span>


```C++
HRESULT ExtractTexture(
  [in] UINT               Channel,
  [in] UINT               StartCoefficient,
  [in] UINT               NumCoefficients,
  [in] LPDIRECT3DTEXTURE9 pTexture
);
```



## <a name="parameters"></a><span data-ttu-id="8e1ec-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8e1ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e1ec-107">*Chaîne* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8e1ec-107">*Channel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e1ec-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8e1ec-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8e1ec-109">Canal de couleur de la mémoire tampon à partir duquel extraire les données de texture.</span><span class="sxs-lookup"><span data-stu-id="8e1ec-109">Buffer color channel from which to extract texture data.</span></span>

</dd> <dt>

<span data-ttu-id="8e1ec-110">*StartCoefficient* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8e1ec-110">*StartCoefficient* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e1ec-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8e1ec-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8e1ec-112">Valeur de départ du coefficient de mémoire tampon à partir duquel extraire les données de texture.</span><span class="sxs-lookup"><span data-stu-id="8e1ec-112">Starting value of the buffer coefficient from which to extract texture data.</span></span>

</dd> <dt>

<span data-ttu-id="8e1ec-113">*NumCoefficients* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8e1ec-113">*NumCoefficients* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e1ec-114">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8e1ec-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8e1ec-115">Nombre de scalaires, en commençant par StartCoefficient, à partir duquel extraire les données de texture.</span><span class="sxs-lookup"><span data-stu-id="8e1ec-115">Number of scalars, beginning at StartCoefficient, from which to extract texture data.</span></span>

</dd> <dt>

<span data-ttu-id="8e1ec-116">*pTexture* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8e1ec-116">*pTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e1ec-117">Type : **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="8e1ec-117">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="8e1ec-118">Pointeur vers un objet de texture [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) qui stocke les coefficients.</span><span class="sxs-lookup"><span data-stu-id="8e1ec-118">Pointer to a [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) texture object that will store coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e1ec-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8e1ec-119">Return value</span></span>

<span data-ttu-id="8e1ec-120">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8e1ec-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8e1ec-121">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8e1ec-121">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="8e1ec-122">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="8e1ec-122">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e1ec-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8e1ec-123">Requirements</span></span>



| <span data-ttu-id="8e1ec-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8e1ec-124">Requirement</span></span> | <span data-ttu-id="8e1ec-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="8e1ec-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e1ec-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="8e1ec-126">Header</span></span><br/>  | <dl> <span data-ttu-id="8e1ec-127"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e1ec-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="8e1ec-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8e1ec-128">Library</span></span><br/> | <dl> <span data-ttu-id="8e1ec-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8e1ec-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8e1ec-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8e1ec-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e1ec-131">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="8e1ec-131">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> </dl>

 

 
