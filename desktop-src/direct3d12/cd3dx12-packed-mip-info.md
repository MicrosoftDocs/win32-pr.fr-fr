---
title: Structure CD3DX12_PACKED_MIP_INFO (D3dx12. h)
description: Structure d’assistance pour faciliter l’initialisation d’une \_ structure d’informations MIP D3D12 compressée \_ \_ .
ms.assetid: B3549D78-C354-48FC-A012-1F835DBD585E
keywords:
- Structure CD3DX12_PACKED_MIP_INFO
topic_type:
- apiref
api_name:
- CD3DX12_PACKED_MIP_INFO
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f4565bbac6189cffc5358213437463b4abc0322
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539863"
---
# <a name="cd3dx12_packed_mip_info-structure"></a>\_Structure d' \_ informations MIP CD3DX12 compressée \_

Structure d’assistance pour faciliter l’initialisation d’une structure d' [**\_ \_ \_ informations MIP D3D12 compressée**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info) .

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_PACKED_MIP_INFO  : public D3D12_PACKED_MIP_INFO{
   CD3DX12_PACKED_MIP_INFO();
   explicit CD3DX12_PACKED_MIP_INFO(const D3D12_PACKED_MIP_INFO &o);
   CD3DX12_PACKED_MIP_INFO(UINT8 numStandardMips, UINT8 numPackedMips, UINT numTilesForPackedMips, UINT startTileIndexInOverallResource);
   operator const D3D12_PACKED_MIP_INFO&() const;
};
```



## <a name="members"></a>Membres

<dl> <dt>

**\_Informations MIP CD3DX12 compressées \_ \_ ()**
</dt> <dd>

Crée une nouvelle instance non initialisée d’une \_ information MIP CD3DX12 compressée \_ \_ .

</dd> <dt>

**\_informations MIP CD3DX12 compressées explicites \_ \_ (const D3D12 \_ condensé \_ MIP \_ info &o)**
</dt> <dd>

Crée une instance d’une \_ information MIP CD3DX12 compressée \_ \_ , initialisée avec le contenu d’une autre structure d' [**\_ \_ \_ informations MIP compressée D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info) .

</dd> <dt>

**\_Informations MIP CD3DX12 compressées \_ \_ (UINT8 NumStandardMips, UINT8 NumPackedMips, UINT NumTilesForPackedMips, uint startTileIndexInOverallResource)**
</dt> <dd>

Crée une instance d’une \_ information MIP CD3DX12 compressée \_ \_ , en initialisant les paramètres suivants :

UINT8 numStandardMips

UINT8 numPackedMips

UINT numTilesForPackedMips

UINT startTileIndexInOverallResource

</dd> <dt>

**const D3D12 \_ compressée \_ MIP \_ info& () const**
</dt> <dd>

Définit le & opérateur de passage par référence pour le type de structure parent.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_ \_ Informations MIP compressé \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info)
</dt> <dt>

[Structures d’assistance pour D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





