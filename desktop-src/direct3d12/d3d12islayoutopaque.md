---
title: D3D12IsLayoutOpaque, fonction (D3dx12. h)
description: Indique si la disposition est opaque.
ms.assetid: 43B46A18-A725-4999-BD97-108032793A95
keywords:
- D3D12IsLayoutOpaque fonction)
topic_type:
- apiref
api_name:
- D3D12IsLayoutOpaque
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 971c44688e57dd1081d33a4a077a8dcadcb89abf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531314"
---
# <a name="d3d12islayoutopaque-function"></a>D3D12IsLayoutOpaque fonction)

Indique si la disposition est opaque.

## <a name="syntax"></a>Syntaxe


```C++
bool inline D3D12IsLayoutOpaque(
   D3D12_TEXTURE_LAYOUT Layout
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Disposition* 
</dt> <dd>

Type : **[ **\_ \_ mise en page de texture D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout)**

Disposition à vérifier, en tant que [**\_ \_ disposition de texture D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **bool**

Valeur **booléenne** qui indique si la disposition est opaque. Une disposition est opaque si elle est D3D12 \_ disposition de texture \_ \_ inconnue ou \_ disposition de texture D3D12 \_ \_ 64 Ko \_ non définis \_ SWIZZLE.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx12. h</dt> </dl>  |
| Bibliothèque<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions d’assistance pour D3D12](helper-functions-for-d3d12.md)
</dt> </dl>

 

 





