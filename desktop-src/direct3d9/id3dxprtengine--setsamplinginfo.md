---
description: Définit les propriétés d’échantillonnage utilisées par le simulateur de transfert luminance (PRT) précalculé.
ms.assetid: a33963a7-fbcb-4e1c-a4f3-fb20a99fcf9f
title: 'ID3DXPRTEngine :: SetSamplingInfo, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetSamplingInfo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ab229652fe9e333519acce7d8474d3c4f0cf7ef9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762127"
---
# <a name="id3dxprtenginesetsamplinginfo-method"></a><span data-ttu-id="ff582-103">ID3DXPRTEngine :: SetSamplingInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="ff582-103">ID3DXPRTEngine::SetSamplingInfo method</span></span>

<span data-ttu-id="ff582-104">Définit les propriétés d’échantillonnage utilisées par le simulateur de transfert luminance (PRT) précalculé.</span><span class="sxs-lookup"><span data-stu-id="ff582-104">Sets sampling properties used by the precomputed radiance transfer (PRT) simulator.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff582-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ff582-105">Syntax</span></span>


```C++
HRESULT SetSamplingInfo(
  [in] UINT  NumRays,
  [in] BOOL  UseSphere,
  [in] BOOL  UseCosine,
  [in] BOOL  Adaptive,
  [in] FLOAT AdaptiveThresh
);
```



## <a name="parameters"></a><span data-ttu-id="ff582-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ff582-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff582-107">*NumRays* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ff582-107">*NumRays* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff582-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ff582-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ff582-109">Nombre de rayons de lumière à diriger vers chaque échantillon.</span><span class="sxs-lookup"><span data-stu-id="ff582-109">Number of light rays to direct at each sample.</span></span> <span data-ttu-id="ff582-110">Doit être supérieur à zéro.</span><span class="sxs-lookup"><span data-stu-id="ff582-110">Must be greater than zero.</span></span>

</dd> <dt>

<span data-ttu-id="ff582-111">*UseSphere* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ff582-111">*UseSphere* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff582-112">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ff582-112">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ff582-113">Si la **valeur est true**, les échantillons sont calculés sur une sphère complète.</span><span class="sxs-lookup"><span data-stu-id="ff582-113">If **TRUE**, samples will be computed over a full sphere.</span></span> <span data-ttu-id="ff582-114">Si la **valeur est false**, les échantillons sont calculés sur un hémisphère.</span><span class="sxs-lookup"><span data-stu-id="ff582-114">If **FALSE**, samples will be computed over a hemisphere.</span></span>

</dd> <dt>

<span data-ttu-id="ff582-115">*UseCosine* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ff582-115">*UseCosine* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff582-116">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ff582-116">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ff582-117">Si la **valeur est true**, utilisez une pondération cosinus des échantillons.</span><span class="sxs-lookup"><span data-stu-id="ff582-117">If **TRUE**, use a cosine weighting of samples.</span></span> <span data-ttu-id="ff582-118">Si UseCosine et UseSphere ont tous les deux la **valeur true**, la méthode échoue et une erreur est retournée.</span><span class="sxs-lookup"><span data-stu-id="ff582-118">If both UseCosine and UseSphere are **TRUE**, the method will fail and an error will be returned.</span></span>

</dd> <dt>

<span data-ttu-id="ff582-119">*Adaptative* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ff582-119">*Adaptive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff582-120">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ff582-120">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ff582-121">Doit avoir la **valeur false**.</span><span class="sxs-lookup"><span data-stu-id="ff582-121">Must be **FALSE**.</span></span> <span data-ttu-id="ff582-122">L’échantillonnage adaptatif n’est actuellement pas implémenté.</span><span class="sxs-lookup"><span data-stu-id="ff582-122">Adaptive sampling is currently not implemented.</span></span>

</dd> <dt>

<span data-ttu-id="ff582-123">*AdaptiveThresh* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ff582-123">*AdaptiveThresh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff582-124">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ff582-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ff582-125">Ignoré.</span><span class="sxs-lookup"><span data-stu-id="ff582-125">Ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff582-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ff582-126">Return value</span></span>

<span data-ttu-id="ff582-127">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ff582-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ff582-128">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ff582-128">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ff582-129">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, e \_ NOTIMPL, e \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="ff582-129">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_NOTIMPL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff582-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ff582-130">Requirements</span></span>



| <span data-ttu-id="ff582-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ff582-131">Requirement</span></span> | <span data-ttu-id="ff582-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="ff582-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff582-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="ff582-133">Header</span></span><br/>  | <dl> <span data-ttu-id="ff582-134"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff582-134"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="ff582-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ff582-135">Library</span></span><br/> | <dl> <span data-ttu-id="ff582-136"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ff582-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ff582-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff582-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff582-138">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="ff582-138">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
