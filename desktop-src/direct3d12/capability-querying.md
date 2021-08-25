---
title: Interrogation des fonctionnalités
description: 'Votre application peut découvrir le niveau de prise en charge de la liaison de ressources, ainsi que de nombreuses autres fonctionnalités, avec un appel à ID3D12Device \: \: CheckFeatureSupport.'
ms.assetid: ECBAF8EF-5D91-46D8-9D6E-A7FA4203B9F8
ms.date: 11/26/2018
ms.localizationpriority: high
ms.topic: article
ms.openlocfilehash: a99174515883f8995167a7b866ab1ef8b77b56f7a0be2bb83f960abd06e47713
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119851399"
---
# <a name="capability-querying"></a>Interrogation des fonctionnalités

Votre application peut découvrir le niveau de prise en charge de la liaison de ressources (ainsi que le niveau de prise en charge pour de nombreuses autres fonctionnalités), avec un appel à [**ID3D12Device :: CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).

## <a name="how-to-query-for-the-resource-binding-tier"></a>Comment interroger le niveau de liaison de ressources

Ce premier exemple se concentre sur la liaison de ressources. Chaque niveau de liaison de ressource est un sur-ensemble de niveaux inférieurs dans les fonctionnalités, de sorte que le code qui fonctionne sur un niveau donné fonctionne sans modification sur un niveau supérieur.

Les couches de liaison de ressources sont des constantes dans l’énumération [**D3D12_RESOURCE_BINDING_TIER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_binding_tier) .

Pour interroger le niveau de liaison de ressources, utilisez un code tel que celui-ci. Cet exemple de code illustre le modèle général pour l’interrogation de l’un des différents types de prise en charge des fonctionnalités.

```cppwinrt
D3D12_RESOURCE_BINDING_TIER get_resource_binding_tier(::ID3D12Device* pIDevice)
{
    D3D12_FEATURE_DATA_D3D12_OPTIONS featureSupport{};
    winrt::check_hresult(
        pIDevice->CheckFeatureSupport(D3D12_FEATURE_D3D12_OPTIONS, &featureSupport, sizeof(featureSupport))
    );

    switch (featureSupport.ResourceBindingTier)
    {
    case D3D12_RESOURCE_BINDING_TIER_1:
        // Tier 1 is supported.
        break;

    case D3D12_RESOURCE_BINDING_TIER_2:
        // Tiers 1 and 2 are supported.
        break;

    case D3D12_RESOURCE_BINDING_TIER_3:
        // Tiers 1, 2, and 3 are supported.
        break;
    }

    return featureSupport.ResourceBindingTier;
}
```

Notez que toute constante énumérée que vous transmettez ([**D3D12_FEATURE_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature), dans ce cas) possède une structure de données correspondante qui reçoit des informations sur cette fonctionnalité ou un ensemble de fonctionnalités ([**D3D12_FEATURE_DATA_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options), dans le cas présent). Transmettez toujours un pointeur vers la structure qui correspond à la constante énumérée que vous transmettez.

## <a name="how-to-query-for-any-feature-level"></a>Comment interroger un niveau de fonctionnalité

Outre le niveau de liaison de ressources, il existe de nombreuses autres fonctionnalités dont le niveau de prise en charge vous permet d’interroger en utilisant le même modèle que celui indiqué dans l’exemple de code ci-dessus. Vous transmettez simplement une constante différente de l’énumération [**D3D12_FEATURE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature) à [**ID3D12Device :: CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) (pour indiquer à l’API la fonctionnalité qui doit demander des informations de support) et vous transmettez un pointeur vers une instance de la structure correspondante (dans laquelle recevoir les informations demandées).

- Transmettez **D3D12_FEATURE_ARCHITECTURE** et [**D3D12_FEATURE_DATA_ARCHITECTURE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture).
- Transmettez **D3D12_FEATURE_ARCHITECTURE1** et [**D3D12_FEATURE_DATA_ARCHITECTURE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture1).
- Transmettez **D3D12_FEATURE_COMMAND_QUEUE_PRIORITY** et [**D3D12_FEATURE_DATA_COMMAND_QUEUE_PRIORITY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_command_queue_priority).
- Transmettez **D3D12_FEATURE_CROSS_NODE** et [**D3D12_FEATURE_DATA_CROSS_NODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_cross_node).
- Transmettez **D3D12_FEATURE_D3D12_OPTIONS** et [**D3D12_FEATURE_DATA_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options).
- Transmettez **D3D12_FEATURE_D3D12_OPTIONS1** et [**D3D12_FEATURE_DATA_D3D12_OPTIONS1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options1).
- Transmettez **D3D12_FEATURE_D3D12_OPTIONS2** et [**D3D12_FEATURE_DATA_D3D12_OPTIONS2**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options2).
- Transmettez **D3D12_FEATURE_D3D12_OPTIONS3** et [**D3D12_FEATURE_DATA_D3D12_OPTIONS3**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3).
- Transmettez **D3D12_FEATURE_D3D12_OPTIONS4** et [**D3D12_FEATURE_DATA_D3D12_OPTIONS4**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options4).
- Transmettez **D3D12_FEATURE_D3D12_OPTIONS5** et [**D3D12_FEATURE_DATA_D3D12_OPTIONS5**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options5).
- Transmettez **D3D12_FEATURE_EXISTING_HEAPS** et [**D3D12_FEATURE_DATA_EXISTING_HEAPS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_existing_heaps).
- Transmettez **D3D12_FEATURE_FEATURE_LEVELS** et [**D3D12_FEATURE_DATA_FEATURE_LEVELS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_feature_levels).
- Transmettez **D3D12_FEATURE_FORMAT_INFO** et [**D3D12_FEATURE_DATA_FORMAT_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_info).
- Transmettez **D3D12_FEATURE_FORMAT_SUPPORT** et [**D3D12_FEATURE_DATA_FORMAT_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_support).
- Transmettez **D3D12_FEATURE_GPU_VIRTUAL_ADDRESS_SUPPORT** et [**D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_gpu_virtual_address_support).
- Transmettez **D3D12_FEATURE_MULTISAMPLE_QUALITY_LEVELS** et [**D3D12_FEATURE_DATA_MULTISAMPLE_QUALITY_LEVELS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_multisample_quality_levels).
- Transmettez **D3D12_FEATURE_PROTECTED_RESOURCE_SESSION_SUPPORT** et [**D3D12_FEATURE_DATA_PROTECTED_RESOURCE_SESSION_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_protected_resource_session_support).
- Transmettez **D3D12_FEATURE_ROOT_SIGNATURE** et [**D3D12_FEATURE_DATA_ROOT_SIGNATURE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_root_signature).
- Transmettez **D3D12_FEATURE_SERIALIZATION** et [**D3D12_FEATURE_DATA_SERIALIZATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_serialization).
- Transmettez **D3D12_FEATURE_SHADER_CACHE** et [**D3D12_FEATURE_DATA_SHADER_CACHE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_shader_cache).
- Transmettez **D3D12_FEATURE_SHADER_MODEL** et [**D3D12_FEATURE_DATA_SHADER_MODEL**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_shader_model).

## <a name="hardware-support-for-dxgi-formats"></a>Prise en charge du matériel pour les formats DXGI

Pour afficher les tableaux des formats de DXGI et des fonctionnalités matérielles, reportez-vous à ces rubriques.

- [Prise en charge du format DXGI pour le matériel de niveau de fonctionnalité Direct3D 12,1](/windows/desktop/direct3ddxgi/hardware-support-for-direct3d-12-1-formats)
- [Prise en charge du format DXGI pour le matériel de niveau de fonctionnalité Direct3D 12,0](/windows/desktop/direct3ddxgi/hardware-support-for-direct3d-12-0-formats)
- [Prise en charge du format DXGI pour le matériel de niveau de fonctionnalité Direct3D 11,1](/windows/desktop/direct3ddxgi/format-support-for-direct3d-11-1-feature-level-hardware)
- [Prise en charge du format DXGI pour le matériel de niveau de fonctionnalité Direct3D 11,0](/windows/desktop/direct3ddxgi/format-support-for-direct3d-11-0-feature-level-hardware)
- [Prise en charge matérielle pour les formats Direct3D 10Level9](/previous-versions//ff471324(v=vs.85))
- [Prise en charge du matériel pour les formats Direct3D 10,1](/previous-versions//cc627091(v=vs.85))
- [Prise en charge matérielle pour les formats Direct3D 10](/previous-versions//cc627090(v=vs.85))

## <a name="related-topics"></a>Rubriques connexes

* [Liaison de ressource dans Direct3D 12](resource-binding.md)
* [Niveaux de fonctionnalité matérielle](hardware-feature-levels.md)
* [Signatures racines](root-signatures.md)