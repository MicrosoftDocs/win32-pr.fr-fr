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
ms.openlocfilehash: 44b6be239286e13cecbf6eb501b333cba5541f6de1dfd8e217166d9620bdfbd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118279659"
---
# <a name="dxcore-adapter-attribute-guids"></a>GUID d’attribut d’adaptateur DXCore

Les GUID d’attribut de l’adaptateur suivants sont déclarés dans `dxcore_interface.h` et sont utilisés avec les méthodes [IDXCoreAdapterFactory :: CreateAdapterList](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-createadapterlist.md) et [IDXCoreAdapter :: IsAttributeSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isattributesupported.md) . Pour un adaptateur donné, un ou plusieurs des attributs peuvent s’appliquer.

| GUID | Valeur |
|-|-|
| `DXCORE_ADAPTER_ATTRIBUTE_D3D11_GRAPHICS`. Spécifie un adaptateur qui prend en charge l’utilisation des API graphiques [Direct3D 11](/windows/win32/direct3d11) . Aucune garantie n’est faite sur des fonctionnalités spécifiques, ni sur la garantie que le système d’exploitation dans sa configuration actuelle prend en charge ces API. | 0x8c47866b, 0x7583, 0x450d, 0xF0, 0xF0, 0x6b, 0xad, 0xA8, 0x95, 0xaf, 0x4B |
| `DXCORE_ADAPTER_ATTRIBUTE_D3D12_GRAPHICS`. Spécifie un adaptateur qui prend en charge l’utilisation des API graphiques [Direct3D 12](/windows/win32/direct3d12) . Aucune garantie n’est faite sur des fonctionnalités spécifiques, ni sur la garantie que le système d’exploitation dans sa configuration actuelle prend en charge ces API. | 0x0c9ece4d, 0x2f6e, 0x4f01, 0x8C, 0x96, 0xe8, 0x9e, 0x33, 0x1B, 0x47, 0xb1 |
| `DXCORE_ADAPTER_ATTRIBUTE_D3D12_CORE_COMPUTE`. Spécifie un adaptateur qui prend en charge l’utilisation des API de calcul de [base Direct3D 12](../direct3d12/core-feature-levels.md) . Aucune garantie n’est faite sur des fonctionnalités spécifiques, ni sur la garantie que le système d’exploitation dans sa configuration actuelle prend en charge ces API. | 0x248e2800, 0xa793, 0x4724, 0xAB, 0xAA, 0x23, 0xA6, 0xDE, 0x1B, 0xe0, 0X90 |

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-|-|
| En-tête | dxcore_interface. h |

## <a name="see-also"></a>Voir aussi

* [IDXCoreAdapterFactory::CreateAdapterList](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-createadapterlist.md)
* [IDXCoreAdapter::IsAttributeSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isattributesupported.md)
* [Référence DXCore](./dxcore-reference.md)
* [Utilisation de DXCore pour énumérer des adaptateurs](./dxcore-enum-adapters.md)
* [Graphiques Direct3D 12](../direct3d12/direct3d-12-graphics.md)
