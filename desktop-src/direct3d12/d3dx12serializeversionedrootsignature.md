---
title: D3DX12SerializeVersionedRootSignature, fonction (D3dx12. h)
description: Permet d’activer les fonctionnalités de signature racine 1,1 lorsqu’elles sont disponibles et ne nécessite pas la gestion de deux chemins de code pour générer des signatures racines. Cette méthode d’assistance reconstruit une signature racine version 1,0 quand la version 1,1 n’est pas prise en charge.
ms.assetid: 0F6BA6C1-9A33-4E99-BF34-4A0358E7427D
keywords:
- D3DX12SerializeVersionedRootSignature fonction)
topic_type:
- apiref
api_name:
- D3DX12SerializeVersionedRootSignature
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70a9d0424f7f7a7f89edde18273c5d1fa22fae28
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106520306"
---
# <a name="d3dx12serializeversionedrootsignature-function"></a><span data-ttu-id="bd280-105">D3DX12SerializeVersionedRootSignature fonction)</span><span class="sxs-lookup"><span data-stu-id="bd280-105">D3DX12SerializeVersionedRootSignature function</span></span>

<span data-ttu-id="bd280-106">Permet d’activer les fonctionnalités de signature racine 1,1 lorsqu’elles sont disponibles et ne nécessite pas la gestion de deux chemins de code pour générer des signatures racines.</span><span class="sxs-lookup"><span data-stu-id="bd280-106">Helps enable root signature 1.1 features when they are available, and does not require maintaining two code paths for building root signatures.</span></span> <span data-ttu-id="bd280-107">Cette méthode d’assistance reconstruit une signature racine version 1,0 quand la version 1,1 n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="bd280-107">This helper method reconstructs a version 1.0 root signature when version 1.1 is not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd280-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bd280-108">Syntax</span></span>


```C++
HRESULT inline D3DX12SerializeVersionedRootSignature(
  _In_      const D3D12_VERSIONED_ROOT_SIGNATURE_DESC *pRootSignatureDesc,
                  D3D_ROOT_SIGNATURE_VERSION          MaxVersion,
  _Out_           ID3DBlob                            **ppBlob,
  _Out_opt_       ID3DBlob                            **ppErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="bd280-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bd280-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd280-110">*pRootSignatureDesc* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bd280-110">*pRootSignatureDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd280-111">Type : **const D3D12 \_ version de la racine avec version gérée \_ \_ \_ desc \***</span><span class="sxs-lookup"><span data-stu-id="bd280-111">Type: **const D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC\***</span></span>

<span data-ttu-id="bd280-112">Spécifie une description de la [**\_ \_ \_ signature \_ racine avec version D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) qui contient une description de toute version d’une signature racine.</span><span class="sxs-lookup"><span data-stu-id="bd280-112">Specifies a [**D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) that contains a description of any version of a root signature.</span></span>

</dd> <dt>

<span data-ttu-id="bd280-113">*MaxVersion*</span><span class="sxs-lookup"><span data-stu-id="bd280-113">*MaxVersion*</span></span> 
</dt> <dd>

<span data-ttu-id="bd280-114">Type : **\_ version de \_ signature \_ racine D3D**</span><span class="sxs-lookup"><span data-stu-id="bd280-114">Type: **D3D\_ROOT\_SIGNATURE\_VERSION**</span></span>

<span data-ttu-id="bd280-115">Spécifie la version maximale prise en charge de la signature de la [**\_ racine \_ \_ D3D**](/windows/desktop/api/d3d12/ne-d3d12-d3d_root_signature_version).</span><span class="sxs-lookup"><span data-stu-id="bd280-115">Specifies the maximum supported [**D3D\_ROOT\_SIGNATURE\_VERSION**](/windows/desktop/api/d3d12/ne-d3d12-d3d_root_signature_version).</span></span>

</dd> <dt>

<span data-ttu-id="bd280-116">*ppBlob* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="bd280-116">*ppBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bd280-117">Type : **ID3DBlob \* \***</span><span class="sxs-lookup"><span data-stu-id="bd280-117">Type: **ID3DBlob\*\***</span></span>

<span data-ttu-id="bd280-118">Pointeur vers un bloc de mémoire qui reçoit un pointeur vers l’interface [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) que vous pouvez utiliser pour accéder à la signature racine sérialisée.</span><span class="sxs-lookup"><span data-stu-id="bd280-118">A pointer to a memory block that receives a pointer to the [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) interface that you can use to access the serialized root signature.</span></span>

</dd> <dt>

<span data-ttu-id="bd280-119">*ppErrorBlob* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="bd280-119">*ppErrorBlob* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bd280-120">Type : **ID3DBlob \* \***</span><span class="sxs-lookup"><span data-stu-id="bd280-120">Type: **ID3DBlob\*\***</span></span>

<span data-ttu-id="bd280-121">Pointeur vers un bloc de mémoire qui reçoit un pointeur vers l’interface [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) que vous pouvez utiliser pour accéder aux messages d’erreur du sérialiseur, ou **null** s’il n’y a aucune erreur.</span><span class="sxs-lookup"><span data-stu-id="bd280-121">A pointer to a memory block that receives a pointer to the [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) interface that you can use to access serializer error messages, or **NULL** if there are no errors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd280-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bd280-122">Return value</span></span>

<span data-ttu-id="bd280-123">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bd280-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bd280-124">Retourne **S \_ OK** en cas de réussite ; sinon, retourne l’un des [codes de retour Direct3D 12](d3d12-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="bd280-124">Returns **S\_OK** if successful; otherwise, returns one of the [Direct3D 12 Return Codes](d3d12-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bd280-125">Notes</span><span class="sxs-lookup"><span data-stu-id="bd280-125">Remarks</span></span>

<span data-ttu-id="bd280-126">Cette fonction a été publiée pour coïncider avec la mise à jour anniversaire de Windows 10 (14393).</span><span class="sxs-lookup"><span data-stu-id="bd280-126">This function was released to coincide with the Windows 10 Anniversary Update (14393).</span></span> <span data-ttu-id="bd280-127">Pour prendre en charge les versions de Windows 10 antérieures à cela, l’utilisation de cette fonction requiert que d3d12. lib soit configuré pour le *chargement différé*.</span><span class="sxs-lookup"><span data-stu-id="bd280-127">In order to support Windows 10 versions prior to this, use of this function requires d3d12.lib be set up for *delay loading*.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd280-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bd280-128">Requirements</span></span>



| <span data-ttu-id="bd280-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bd280-129">Requirement</span></span> | <span data-ttu-id="bd280-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="bd280-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bd280-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="bd280-131">Header</span></span><br/>  | <dl> <span data-ttu-id="bd280-132"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd280-132"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="bd280-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bd280-133">Library</span></span><br/> | <dl> <span data-ttu-id="bd280-134"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bd280-134"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="bd280-135">DLL</span><span class="sxs-lookup"><span data-stu-id="bd280-135">DLL</span></span><br/>     | <dl> <span data-ttu-id="bd280-136"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd280-136"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd280-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bd280-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd280-138">**D3D12SerializeVersionedRootSignature**</span><span class="sxs-lookup"><span data-stu-id="bd280-138">**D3D12SerializeVersionedRootSignature**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializeversionedrootsignature)
</dt> <dt>

[<span data-ttu-id="bd280-139">Fonctions d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="bd280-139">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> </dl>

 

