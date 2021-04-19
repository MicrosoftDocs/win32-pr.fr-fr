---
title: GUID d’attribut d’adaptateur DXCore
description: 'Les GUID d’attribut de l’adaptateur suivants sont déclarés dans `dxcore_interface.h` et sont utilisés avec les méthodes [IDXCoreAdapterFactory :: CreateAdapterList](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-createadapterlist.md) et [IDXCoreAdapter :: IsAttributeSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isattributesupported.md) .'
keywords:
- DXCore, attribut d’adaptateur, GUID
topic_type:
- apiref
api_name:
- DXCore adapter attribute GUIDs
api_location:
- dxcore_interface.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: a532552f144dfc21aa5d6a368aecd915d30b40c8
ms.sourcegitcommit: 8737f32d64e5f01c1d38aab92736e4088d6c446e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/31/2021
ms.locfileid: "106534952"
---
# <a name="dxcore-adapter-attribute-guids"></a><span data-ttu-id="1e645-104">GUID d’attribut d’adaptateur DXCore</span><span class="sxs-lookup"><span data-stu-id="1e645-104">DXCore adapter attribute GUIDs</span></span>

<span data-ttu-id="1e645-105">Les GUID d’attribut de l’adaptateur suivants sont déclarés dans `dxcore_interface.h` et sont utilisés avec les méthodes [IDXCoreAdapterFactory :: CreateAdapterList](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-createadapterlist.md) et [IDXCoreAdapter :: IsAttributeSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isattributesupported.md) .</span><span class="sxs-lookup"><span data-stu-id="1e645-105">The following adapter attribute GUIDs are declared in `dxcore_interface.h`, and are used with the [IDXCoreAdapterFactory::CreateAdapterList](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-createadapterlist.md) and [IDXCoreAdapter::IsAttributeSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isattributesupported.md) methods.</span></span> <span data-ttu-id="1e645-106">Pour un adaptateur donné, un ou plusieurs des attributs peuvent s’appliquer.</span><span class="sxs-lookup"><span data-stu-id="1e645-106">For any given adapter, one or more of the attributes could apply.</span></span>

| <span data-ttu-id="1e645-107">GUID</span><span class="sxs-lookup"><span data-stu-id="1e645-107">GUID</span></span> | <span data-ttu-id="1e645-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="1e645-108">Value</span></span> |
|-|-|
| <span data-ttu-id="1e645-109">`DXCORE_ADAPTER_ATTRIBUTE_D3D11_GRAPHICS`.</span><span class="sxs-lookup"><span data-stu-id="1e645-109">`DXCORE_ADAPTER_ATTRIBUTE_D3D11_GRAPHICS`.</span></span> <span data-ttu-id="1e645-110">Spécifie un adaptateur qui prend en charge l’utilisation des API graphiques [Direct3D 11](/windows/win32/direct3d11) .</span><span class="sxs-lookup"><span data-stu-id="1e645-110">Specifies an adapter that supports being used with the [Direct3D 11](/windows/win32/direct3d11) graphics APIs.</span></span> <span data-ttu-id="1e645-111">Aucune garantie n’est faite sur des fonctionnalités spécifiques, ni sur la garantie que le système d’exploitation dans sa configuration actuelle prend en charge ces API.</span><span class="sxs-lookup"><span data-stu-id="1e645-111">No guarantees are made about specific features, nor is a guarantee made that the OS in its current configuration supports these APIs.</span></span> | <span data-ttu-id="1e645-112">0x8c47866b, 0x7583, 0x450d, 0xF0, 0xF0, 0x6b, 0xad, 0xA8, 0x95, 0xaf, 0x4B</span><span class="sxs-lookup"><span data-stu-id="1e645-112">0x8c47866b, 0x7583, 0x450d, 0xf0, 0xf0, 0x6b, 0xad, 0xa8, 0x95, 0xaf, 0x4b</span></span> |
| <span data-ttu-id="1e645-113">`DXCORE_ADAPTER_ATTRIBUTE_D3D12_GRAPHICS`.</span><span class="sxs-lookup"><span data-stu-id="1e645-113">`DXCORE_ADAPTER_ATTRIBUTE_D3D12_GRAPHICS`.</span></span> <span data-ttu-id="1e645-114">Spécifie un adaptateur qui prend en charge l’utilisation des API graphiques [Direct3D 12](/windows/win32/direct3d12) .</span><span class="sxs-lookup"><span data-stu-id="1e645-114">Specifies an adapter that supports being used with the [Direct3D 12](/windows/win32/direct3d12) graphics APIs.</span></span> <span data-ttu-id="1e645-115">Aucune garantie n’est faite sur des fonctionnalités spécifiques, ni sur la garantie que le système d’exploitation dans sa configuration actuelle prend en charge ces API.</span><span class="sxs-lookup"><span data-stu-id="1e645-115">No guarantees are made about specific features, nor is a guarantee made that the OS in its current configuration supports these APIs.</span></span> | <span data-ttu-id="1e645-116">0x0c9ece4d, 0x2f6e, 0x4f01, 0x8C, 0x96, 0xe8, 0x9e, 0x33, 0x1B, 0x47, 0xb1</span><span class="sxs-lookup"><span data-stu-id="1e645-116">0x0c9ece4d, 0x2f6e, 0x4f01, 0x8c, 0x96, 0xe8, 0x9e, 0x33, 0x1b, 0x47, 0xb1</span></span> |
| <span data-ttu-id="1e645-117">`DXCORE_ADAPTER_ATTRIBUTE_D3D12_CORE_COMPUTE`.</span><span class="sxs-lookup"><span data-stu-id="1e645-117">`DXCORE_ADAPTER_ATTRIBUTE_D3D12_CORE_COMPUTE`.</span></span> <span data-ttu-id="1e645-118">Spécifie un adaptateur qui prend en charge l’utilisation des API de calcul de [base Direct3D 12](../direct3d12/core-feature-levels.md) .</span><span class="sxs-lookup"><span data-stu-id="1e645-118">Specifies an adapter that supports being used with the [Direct3D 12 Core](../direct3d12/core-feature-levels.md) compute APIs.</span></span> <span data-ttu-id="1e645-119">Aucune garantie n’est faite sur des fonctionnalités spécifiques, ni sur la garantie que le système d’exploitation dans sa configuration actuelle prend en charge ces API.</span><span class="sxs-lookup"><span data-stu-id="1e645-119">No guarantees are made about specific features, nor is a guarantee made that the OS in its current configuration supports these APIs.</span></span> | <span data-ttu-id="1e645-120">0x248e2800, 0xa793, 0x4724, 0xAB, 0xAA, 0x23, 0xA6, 0xDE, 0x1B, 0xe0, 0X90</span><span class="sxs-lookup"><span data-stu-id="1e645-120">0x248e2800, 0xa793, 0x4724, 0xab, 0xaa, 0x23, 0xa6, 0xde, 0x1b, 0xe0, 0x90</span></span> |

## <a name="requirements"></a><span data-ttu-id="1e645-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1e645-121">Requirements</span></span>

| <span data-ttu-id="1e645-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1e645-122">Requirement</span></span> | <span data-ttu-id="1e645-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="1e645-123">Value</span></span> |
|-|-|
| <span data-ttu-id="1e645-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="1e645-124">Header</span></span> | <span data-ttu-id="1e645-125">dxcore_interface. h</span><span class="sxs-lookup"><span data-stu-id="1e645-125">dxcore_interface.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="1e645-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e645-126">See also</span></span>

* [<span data-ttu-id="1e645-127">IDXCoreAdapterFactory::CreateAdapterList</span><span class="sxs-lookup"><span data-stu-id="1e645-127">IDXCoreAdapterFactory::CreateAdapterList</span></span>](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-createadapterlist.md)
* [<span data-ttu-id="1e645-128">IDXCoreAdapter::IsAttributeSupported</span><span class="sxs-lookup"><span data-stu-id="1e645-128">IDXCoreAdapter::IsAttributeSupported</span></span>](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isattributesupported.md)
* [<span data-ttu-id="1e645-129">Référence DXCore</span><span class="sxs-lookup"><span data-stu-id="1e645-129">DXCore Reference</span></span>](./dxcore-reference.md)
* [<span data-ttu-id="1e645-130">Utilisation de DXCore pour énumérer des adaptateurs</span><span class="sxs-lookup"><span data-stu-id="1e645-130">Using DXCore to enumerate adapters</span></span>](./dxcore-enum-adapters.md)
* [<span data-ttu-id="1e645-131">Graphiques Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="1e645-131">Direct3D 12 graphics</span></span>](../direct3d12/direct3d-12-graphics.md)
