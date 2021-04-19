---
title: D3D12GetFormatPlaneCount, fonction (D3dx12. h)
description: Obtient le nombre de plans pour le format DXGI spécifié pour la carte virtuelle spécifiée (un ID3D12Device).
ms.assetid: CD21F6F9-A9AA-4CE8-A430-57C70326CB4B
keywords:
- D3D12GetFormatPlaneCount fonction)
topic_type:
- apiref
api_name:
- D3D12GetFormatPlaneCount
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bfc2e88c162068de2b97c9df5071398e2fab068
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106540923"
---
# <a name="d3d12getformatplanecount-function"></a><span data-ttu-id="95d07-104">D3D12GetFormatPlaneCount fonction)</span><span class="sxs-lookup"><span data-stu-id="95d07-104">D3D12GetFormatPlaneCount function</span></span>

<span data-ttu-id="95d07-105">Obtient le nombre de plans pour le format DXGI spécifié pour la carte virtuelle spécifiée (un **ID3D12Device**).</span><span class="sxs-lookup"><span data-stu-id="95d07-105">Gets the number of planes for the specified DXGI format for the specified virtual adapter (an **ID3D12Device**).</span></span>

## <a name="syntax"></a><span data-ttu-id="95d07-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="95d07-106">Syntax</span></span>


```C++
UINT8 inline D3D12GetFormatPlaneCount(
  _In_ ID3D12Device *pDevice,
       DXGI_FORMAT  Format
);
```



## <a name="parameters"></a><span data-ttu-id="95d07-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="95d07-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95d07-108">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="95d07-108">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95d07-109">Type : **[ **ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device)\***</span><span class="sxs-lookup"><span data-stu-id="95d07-109">Type: **[**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device)\***</span></span>

<span data-ttu-id="95d07-110">Carte virtuelle ( [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device)) pour laquelle obtenir le nombre de plans.</span><span class="sxs-lookup"><span data-stu-id="95d07-110">The virtual adapter (an [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device)) for which to get the plane count.</span></span>

</dd> <dt>

<span data-ttu-id="95d07-111">*Format*</span><span class="sxs-lookup"><span data-stu-id="95d07-111">*Format*</span></span> 
</dt> <dd>

<span data-ttu-id="95d07-112">Type : **[ **dxgi \_ format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="95d07-112">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="95d07-113">[**\_ Format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) pour lequel obtenir le nombre de plans.</span><span class="sxs-lookup"><span data-stu-id="95d07-113">The [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) for which to get the plane count.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95d07-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="95d07-114">Return value</span></span>

<span data-ttu-id="95d07-115">Type : **UINT8**</span><span class="sxs-lookup"><span data-stu-id="95d07-115">Type: **UINT8**</span></span>

<span data-ttu-id="95d07-116">Nombre de plans pour le format spécifié sur la carte virtuelle spécifiée.</span><span class="sxs-lookup"><span data-stu-id="95d07-116">The plane count for the specified format on the specified virtual adapter.</span></span>

## <a name="requirements"></a><span data-ttu-id="95d07-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="95d07-117">Requirements</span></span>



| <span data-ttu-id="95d07-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="95d07-118">Requirement</span></span> | <span data-ttu-id="95d07-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="95d07-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="95d07-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="95d07-120">Header</span></span><br/>  | <dl> <span data-ttu-id="95d07-121"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="95d07-121"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="95d07-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="95d07-122">Library</span></span><br/> | <dl> <span data-ttu-id="95d07-123"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="95d07-123"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="95d07-124">DLL</span><span class="sxs-lookup"><span data-stu-id="95d07-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="95d07-125"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95d07-125"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95d07-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95d07-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95d07-127">**\_ \_ \_ Informations sur le format de données \_ de la fonctionnalité D3D12**</span><span class="sxs-lookup"><span data-stu-id="95d07-127">**D3D12\_FEATURE\_DATA\_FORMAT\_INFO**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_info)
</dt> <dt>

[<span data-ttu-id="95d07-128">**CheckFeatureSupport**</span><span class="sxs-lookup"><span data-stu-id="95d07-128">**CheckFeatureSupport**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)
</dt> <dt>

[<span data-ttu-id="95d07-129">Fonctions d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="95d07-129">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> </dl>

 

