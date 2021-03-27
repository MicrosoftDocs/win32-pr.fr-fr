---
title: D3DX11ComputeNormalMap, fonction (D3DX11tex. h)
description: 'Remarque : la bibliothèque de l’utilitaire D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store. Notez qu’au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser la bibliothèque DirectXTex, ComputeNormalMap.'
ms.assetid: 3ccdbd9a-669e-48ff-97d5-e5a6c7d2fb26
keywords:
- Fonction D3DX11ComputeNormalMap Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11ComputeNormalMap
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4399282c325fde0ea46679da9e9b84331b8c125b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211878"
---
# <a name="d3dx11computenormalmap-function"></a><span data-ttu-id="ce7a5-105">D3DX11ComputeNormalMap fonction)</span><span class="sxs-lookup"><span data-stu-id="ce7a5-105">D3DX11ComputeNormalMap function</span></span>

> [!Note]  
> <span data-ttu-id="ce7a5-106">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="ce7a5-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="ce7a5-107">Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser la bibliothèque [DirectXTex](https://github.com/Microsoft/DirectXTex) , **ComputeNormalMap**.</span><span class="sxs-lookup"><span data-stu-id="ce7a5-107">Instead of using this function, we recommend that you use the [DirectXTex](https://github.com/Microsoft/DirectXTex) library, **ComputeNormalMap**.</span></span>

 

<span data-ttu-id="ce7a5-108">Convertit une carte de hauteur en une carte normale.</span><span class="sxs-lookup"><span data-stu-id="ce7a5-108">Converts a height map into a normal map.</span></span> <span data-ttu-id="ce7a5-109">Les composants (x, y, z) de chaque normal sont mappés aux canaux (r, g, b) de la texture de sortie.</span><span class="sxs-lookup"><span data-stu-id="ce7a5-109">The (x,y,z) components of each normal are mapped to the (r,g,b) channels of the output texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce7a5-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ce7a5-110">Syntax</span></span>


```C++
HRESULT D3DX11ComputeNormalMap(
  _In_ ID3D11DeviceContext *pContext,
  _In_ ID3D11Texture2D     *pSrcTexture,
  _In_ UINT                Flags,
  _In_ UINT                Channel,
  _In_ FLOAT               Amplitude,
  _In_ ID3D11Texture2D     *pDestTexture
);
```



## <a name="parameters"></a><span data-ttu-id="ce7a5-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ce7a5-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce7a5-112">*pContext* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ce7a5-112">*pContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce7a5-113">Type : **[ **ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span><span class="sxs-lookup"><span data-stu-id="ce7a5-113">Type: **[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span></span>

<span data-ttu-id="ce7a5-114">Pointeur vers une interface [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) représentant la texture de la carte de hauteur source.</span><span class="sxs-lookup"><span data-stu-id="ce7a5-114">Pointer to an [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) interface, representing the source height-map texture.</span></span>

</dd> <dt>

<span data-ttu-id="ce7a5-115">*pSrcTexture* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ce7a5-115">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce7a5-116">Type : **[ **ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***</span><span class="sxs-lookup"><span data-stu-id="ce7a5-116">Type: **[**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***</span></span>

<span data-ttu-id="ce7a5-117">Pointeur vers une interface [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) représentant la texture de la carte de hauteur source.</span><span class="sxs-lookup"><span data-stu-id="ce7a5-117">Pointer to an [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) interface, representing the source height-map texture.</span></span>

</dd> <dt>

<span data-ttu-id="ce7a5-118">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="ce7a5-118">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce7a5-119">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ce7a5-119">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ce7a5-120">Un ou plusieurs \_ indicateurs D3DX NORMALMAP qui contrôlent la génération de mappages normaux.</span><span class="sxs-lookup"><span data-stu-id="ce7a5-120">One or more D3DX\_NORMALMAP flags that control generation of normal maps.</span></span>

</dd> <dt>

<span data-ttu-id="ce7a5-121">*Chaîne* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ce7a5-121">*Channel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce7a5-122">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ce7a5-122">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ce7a5-123">Un \_ indicateur de canal D3DX spécifiant la source des informations de hauteur.</span><span class="sxs-lookup"><span data-stu-id="ce7a5-123">One D3DX\_CHANNEL flag specifying the source of height information.</span></span>

</dd> <dt>

<span data-ttu-id="ce7a5-124">*Amplitude* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ce7a5-124">*Amplitude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce7a5-125">Type : **[ **float**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ce7a5-125">Type: **[**FLOAT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ce7a5-126">Multiplicateur de valeur constante qui augmente (ou diminue) les valeurs dans la carte normale.</span><span class="sxs-lookup"><span data-stu-id="ce7a5-126">Constant value multiplier that increases (or decreases) the values in the normal map.</span></span> <span data-ttu-id="ce7a5-127">Les valeurs plus élevées rendent généralement les bosses plus visibles, les valeurs basses rendent généralement les rugosités moins visibles.</span><span class="sxs-lookup"><span data-stu-id="ce7a5-127">Higher values usually make bumps more visible, lower values usually make bumps less visible.</span></span>

</dd> <dt>

<span data-ttu-id="ce7a5-128">*pDestTexture* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ce7a5-128">*pDestTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce7a5-129">Type : **[ **ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***</span><span class="sxs-lookup"><span data-stu-id="ce7a5-129">Type: **[**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***</span></span>

<span data-ttu-id="ce7a5-130">Pointeur vers une interface [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) représentant la texture de destination.</span><span class="sxs-lookup"><span data-stu-id="ce7a5-130">Pointer to an [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) interface, representing the destination texture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce7a5-131">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ce7a5-131">Return value</span></span>

<span data-ttu-id="ce7a5-132">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ce7a5-132">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ce7a5-133">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ce7a5-133">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ce7a5-134">Si la fonction échoue, la valeur de retour peut être la valeur suivante : D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="ce7a5-134">If the function fails, the return value can be the following value: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce7a5-135">Notes</span><span class="sxs-lookup"><span data-stu-id="ce7a5-135">Remarks</span></span>

<span data-ttu-id="ce7a5-136">Cette méthode calcule le normal à l’aide de la différence centrale avec une taille de noyau de 3 x 3.</span><span class="sxs-lookup"><span data-stu-id="ce7a5-136">This method computes the normal by using the central difference with a kernel size of 3x3.</span></span> <span data-ttu-id="ce7a5-137">Les canaux RVB dans la destination contiennent des composants (x, y, z) biaisés de la normale.</span><span class="sxs-lookup"><span data-stu-id="ce7a5-137">RGB channels in the destination contain biased (x,y,z) components of the normal.</span></span> <span data-ttu-id="ce7a5-138">Le dénominateur de différenciation central est codé en dur sur 2,0.</span><span class="sxs-lookup"><span data-stu-id="ce7a5-138">The central differencing denominator is hardcoded to 2.0.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce7a5-139">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ce7a5-139">Requirements</span></span>



| <span data-ttu-id="ce7a5-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ce7a5-140">Requirement</span></span> | <span data-ttu-id="ce7a5-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="ce7a5-141">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce7a5-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="ce7a5-142">Header</span></span><br/>  | <dl> <span data-ttu-id="ce7a5-143"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce7a5-143"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="ce7a5-144">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ce7a5-144">Library</span></span><br/> | <dl> <span data-ttu-id="ce7a5-145"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ce7a5-145"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="ce7a5-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ce7a5-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce7a5-147">D3DX, fonctions</span><span class="sxs-lookup"><span data-stu-id="ce7a5-147">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

