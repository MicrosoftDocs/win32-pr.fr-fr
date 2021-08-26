---
title: Structure CD3DX12_SUBRESOURCE_FOOTPRINT (D3dx12. h)
description: Une structure d’assistance pour faciliter l’initialisation d’une structure d’encombrement des sous- \_ ressources D3D12 \_ .
ms.assetid: 17266FB0-41B5-4A70-A896-206B54F5E76F
keywords:
- Structure CD3DX12_SUBRESOURCE_FOOTPRINT
topic_type:
- apiref
api_name:
- CD3DX12_SUBRESOURCE_FOOTPRINT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d32c3da3e133a5509543ffaa4fbf80b4c565730f13d3b9e92753658c96efcfcd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069729"
---
# <a name="cd3dx12_subresource_footprint-structure"></a>Structure d’encombrement des sous- \_ ressources CD3DX12 \_

Une structure d’assistance pour faciliter l’initialisation d’une structure [**d' \_ \_ Encombrement**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) des sous-ressources D3D12.

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_SUBRESOURCE_FOOTPRINT  : public D3D12_SUBRESOURCE_FOOTPRINT{
   CD3DX12_SUBRESOURCE_FOOTPRINT();
   explicit CD3DX12_SUBRESOURCE_FOOTPRINT(const D3D12_SUBRESOURCE_FOOTPRINT &o);
   CD3DX12_SUBRESOURCE_FOOTPRINT(DXGI_FORMAT format, UINT width, UINT height, UINT depth, UINT rowPitch);
   explicit CD3DX12_SUBRESOURCE_FOOTPRINT(const D3D12_RESOURCE_DESC& resDesc, UINT rowPitch);
   operator const D3D12_SUBRESOURCE_FOOTPRINT&() const;
};
```



## <a name="members"></a>Membres

<dl> <dt>

**\_Encombrement des sous-ressources CD3DX12 \_ ()**
</dt> <dd>

Crée une nouvelle instance non initialisée d’un encombrement de sous- \_ ressources CD3DX12 \_ .

</dd> <dt>

**encombrement explicite des \_ sous-ressources CD3DX12 \_ (D3D12 des sous-ressources const \_ \_ &o)**
</dt> <dd>

Crée une nouvelle instance d’un encombrement de sous- \_ ressources CD3DX12 \_ , initialisée avec le contenu d’une autre structure d’encombrement de sous- [**\_ ressources \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) .

</dd> <dt>

**\_Encombrement des sous-ressources CD3DX12 \_ ( \_ format de format dxgi, largeur UINT, hauteur uint, UINT Depth, uint rowPitch)**
</dt> <dd>

Crée une nouvelle instance d’un encombrement de sous- \_ ressources CD3DX12 \_ , en initialisant les paramètres suivants :

[**Dxgi \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Format de format

Largeur UINT

Hauteur UINT

Profondeur UINT

UINT rowPitch

</dd> <dt>

**encombrement explicite des \_ sous-ressources CD3DX12 \_ (CONSt D3D12 \_ resource \_ desc& resDesc, uint rowPitch)**
</dt> <dd>

Crée une nouvelle instance d’un encombrement de sous- \_ ressources CD3DX12 \_ , en initialisant les paramètres suivants :

[**D3D12 \_ \_Description**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) de la ressource& resDesc

UINT rowPitch

</dd> <dt>

**const D3D12 \_ sous-ressource \_ encombrement& () const**
</dt> <dd>

Définit le & opérateur de passage par référence pour le type de structure parent.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Encombrement des sous- \_ ressources D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint)
</dt> <dt>

[Structures d’assistance pour D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

