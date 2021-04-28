---
description: 'Fonction D3DX10ComputeNormalMap : convertit une carte de hauteur en une carte normale. Les composants (x, y, z) de chaque normal sont mappés aux canaux (r, g, b) de la texture de sortie.'
ms.assetid: 535033dd-f078-4d56-8e5d-cdda80ef5992
title: D3DX10ComputeNormalMap, fonction (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10ComputeNormalMap
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 173a8e0c1b3130a399152187eb52288a0306051c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105317"
---
# <a name="d3dx10computenormalmap-function"></a><span data-ttu-id="90a17-104">D3DX10ComputeNormalMap fonction)</span><span class="sxs-lookup"><span data-stu-id="90a17-104">D3DX10ComputeNormalMap function</span></span>

<span data-ttu-id="90a17-105">Convertit une carte de hauteur en une carte normale.</span><span class="sxs-lookup"><span data-stu-id="90a17-105">Converts a height map into a normal map.</span></span> <span data-ttu-id="90a17-106">Les composants (x, y, z) de chaque normal sont mappés aux canaux (r, g, b) de la texture de sortie.</span><span class="sxs-lookup"><span data-stu-id="90a17-106">The (x,y,z) components of each normal are mapped to the (r,g,b) channels of the output texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="90a17-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="90a17-107">Syntax</span></span>


```C++
HRESULT D3DX10ComputeNormalMap(
  _In_ ID3D10Texture2D *pSrcTexture,
  _In_ UINT            Flags,
  _In_ UINT            Channel,
  _In_ FLOAT           Amplitude,
  _In_ ID3D10Texture2D *pDestTexture
);
```



## <a name="parameters"></a><span data-ttu-id="90a17-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="90a17-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90a17-109">*pSrcTexture* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="90a17-109">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90a17-110">Type : **[ **ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***</span><span class="sxs-lookup"><span data-stu-id="90a17-110">Type: **[**ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***</span></span>

<span data-ttu-id="90a17-111">Pointeur vers une interface ID3D10Texture2D représentant la texture de la carte de hauteur source.</span><span class="sxs-lookup"><span data-stu-id="90a17-111">Pointer to an ID3D10Texture2D interface, representing the source height-map texture.</span></span>

</dd> <dt>

<span data-ttu-id="90a17-112">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="90a17-112">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90a17-113">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="90a17-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="90a17-114">Un ou plusieurs \_ indicateurs D3DX NORMALMAP qui contrôlent la génération de mappages normaux.</span><span class="sxs-lookup"><span data-stu-id="90a17-114">One or more D3DX\_NORMALMAP flags that control generation of normal maps.</span></span>

</dd> <dt>

<span data-ttu-id="90a17-115">*Chaîne* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="90a17-115">*Channel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90a17-116">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="90a17-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="90a17-117">Un \_ indicateur de canal D3DX spécifiant la source des informations de hauteur.</span><span class="sxs-lookup"><span data-stu-id="90a17-117">One D3DX\_CHANNEL flag specifying the source of height information.</span></span>

</dd> <dt>

<span data-ttu-id="90a17-118">*Amplitude* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="90a17-118">*Amplitude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90a17-119">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="90a17-119">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="90a17-120">Multiplicateur de valeur constante qui augmente (ou diminue) les valeurs dans la carte normale.</span><span class="sxs-lookup"><span data-stu-id="90a17-120">Constant value multiplier that increases (or decreases) the values in the normal map.</span></span> <span data-ttu-id="90a17-121">Les valeurs plus élevées rendent généralement les bosses plus visibles, les valeurs basses rendent généralement les rugosités moins visibles.</span><span class="sxs-lookup"><span data-stu-id="90a17-121">Higher values usually make bumps more visible, lower values usually make bumps less visible.</span></span>

</dd> <dt>

<span data-ttu-id="90a17-122">*pDestTexture* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="90a17-122">*pDestTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90a17-123">Type : **[ **ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***</span><span class="sxs-lookup"><span data-stu-id="90a17-123">Type: **[**ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***</span></span>

<span data-ttu-id="90a17-124">Pointeur vers une interface ID3D10Texture2D représentant la texture de destination.</span><span class="sxs-lookup"><span data-stu-id="90a17-124">Pointer to an ID3D10Texture2D interface, representing the destination texture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90a17-125">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="90a17-125">Return value</span></span>

<span data-ttu-id="90a17-126">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="90a17-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="90a17-127">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="90a17-127">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="90a17-128">Si la fonction échoue, la valeur de retour peut être la valeur suivante : D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="90a17-128">If the function fails, the return value can be the following value: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="90a17-129">Notes </span><span class="sxs-lookup"><span data-stu-id="90a17-129">Remarks</span></span>

<span data-ttu-id="90a17-130">Cette méthode calcule le normal à l’aide de la différence centrale avec une taille de noyau de 3 x 3.</span><span class="sxs-lookup"><span data-stu-id="90a17-130">This method computes the normal by using the central difference with a kernel size of 3x3.</span></span> <span data-ttu-id="90a17-131">Les canaux RVB dans la destination contiennent des composants (x, y, z) biaisés de la normale.</span><span class="sxs-lookup"><span data-stu-id="90a17-131">RGB channels in the destination contain biased (x,y,z) components of the normal.</span></span> <span data-ttu-id="90a17-132">Le dénominateur de différenciation central est codé en dur sur 2,0.</span><span class="sxs-lookup"><span data-stu-id="90a17-132">The central differencing denominator is hardcoded to 2.0.</span></span>

## <a name="requirements"></a><span data-ttu-id="90a17-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="90a17-133">Requirements</span></span>



| <span data-ttu-id="90a17-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="90a17-134">Requirement</span></span> | <span data-ttu-id="90a17-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="90a17-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="90a17-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="90a17-136">Header</span></span><br/>  | <dl> <span data-ttu-id="90a17-137"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="90a17-137"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="90a17-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="90a17-138">Library</span></span><br/> | <dl> <span data-ttu-id="90a17-139"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="90a17-139"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="90a17-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="90a17-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90a17-141">Fonctions de texture dans D3DX 10</span><span class="sxs-lookup"><span data-stu-id="90a17-141">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
