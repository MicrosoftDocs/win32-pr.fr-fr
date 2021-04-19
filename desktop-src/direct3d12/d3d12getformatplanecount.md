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
# <a name="d3d12getformatplanecount-function"></a>D3D12GetFormatPlaneCount fonction)

Obtient le nombre de plans pour le format DXGI spécifié pour la carte virtuelle spécifiée (un **ID3D12Device**).

## <a name="syntax"></a>Syntaxe


```C++
UINT8 inline D3D12GetFormatPlaneCount(
  _In_ ID3D12Device *pDevice,
       DXGI_FORMAT  Format
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDevice* \[ dans\]
</dt> <dd>

Type : **[ **ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device)\***

Carte virtuelle ( [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device)) pour laquelle obtenir le nombre de plans.

</dd> <dt>

*Format* 
</dt> <dd>

Type : **[ **dxgi \_ format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

[**\_ Format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) pour lequel obtenir le nombre de plans.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UINT8**

Nombre de plans pour le format spécifié sur la carte virtuelle spécifiée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx12. h</dt> </dl>  |
| Bibliothèque<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_ \_ \_ Informations sur le format de données \_ de la fonctionnalité D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_info)
</dt> <dt>

[**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)
</dt> <dt>

[Fonctions d’assistance pour D3D12](helper-functions-for-d3d12.md)
</dt> </dl>

 

