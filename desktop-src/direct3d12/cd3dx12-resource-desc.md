---
title: Structure CD3DX12_RESOURCE_DESC (D3dx12. h)
description: Une structure d’assistance pour faciliter l’initialisation d’une structure d’application de \_ Description de ressource D3D12 \_ .
ms.assetid: F18D41BE-8AEF-444E-AC8B-EC57C63BF083
keywords:
- Structure CD3DX12_RESOURCE_DESC
topic_type:
- apiref
api_name:
- CD3DX12_RESOURCE_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b341646b2dee7f469235c0b0bc9bb4550e56ff5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918508"
---
# <a name="cd3dx12_resource_desc-structure"></a>CD3DX12, structure de description de la \_ ressource \_

Une structure d’assistance pour faciliter l’initialisation d’une structure d’application de [**\_ \_ Description de ressource D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) .

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_RESOURCE_DESC  : public D3D12_RESOURCE_DESC{
                        CD3DX12_RESOURCE_DESC();
                        explicit CD3DX12_RESOURCE_DESC(const D3D12_RESOURCE_DESC& o);
                        CD3DX12_RESOURCE_DESC(D3D12_RESOURCE_DIMENSION dimension, UINT64 alignment, UINT64 width, UINT height, UINT16 depthOrArraySize, UINT16 mipLevels, DXGI_FORMAT format, UINT sampleCount, UINT sampleQuality, D3D12_TEXTURE_LAYOUT layout, D3D12_RESOURCE_FLAGS flags);
  CD3DX12_RESOURCE_DESC static inline Buffer(const D3D12_RESOURCE_ALLOCATION_INFO& resAllocInfo, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE);
  CD3DX12_RESOURCE_DESC static inline Buffer(UINT64 width, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE, UINT64 alignment = 0);
  CD3DX12_RESOURCE_DESC static inline Tex1D(DXGI_FORMAT format, UINT64 width, UINT16 arraySize = 1, UINT16 mipLevels = 0, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 alignment = 0);
  CD3DX12_RESOURCE_DESC static inline Tex2D(DXGI_FORMAT format, UINT64 width, UINT height, UINT16 arraySize = 1, UINT16 mipLevels = 0, UINT sampleCount = 1, UINT sampleQuality = 0, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 alignment = 0);
  CD3DX12_RESOURCE_DESC static inline Tex3D(DXGI_FORMAT format, UINT64 width, UINT height, UINT16 depth, UINT16 mipLevels = 0, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 alignment = 0);
  UINT16                inline Depth() const;
  UINT16                inline ArraySize() const;
  UINT8                 inline PlaneCount(ID3D12Device* pDevice) const;
  UINT                  inline Subresources(ID3D12Device* pDevice) const;
  UINT                  inline CalcSubresource(UINT MipSlice, UINT ArraySlice, UINT PlaneSlice);
                        operator const D3D12_RESOURCE_DESC&() const;
                        operator == (const D3D12_RESOURCE_DESC& l, const D3D12_RESOURCE_DESC& r);
                        operator !=  (const D3D12_RESOURCE_DESC& l, const D3D12_RESOURCE_DESC& r);
};
```



## <a name="members"></a>Membres

<dl> <dt>

**\_Description de la ressource CD3DX12 \_ ()**
</dt> <dd>

Crée une nouvelle instance non initialisée d’une description de la \_ ressource CD3DX12 \_ .

</dd> <dt>

**Description de la ressource CD3DX12 explicite \_ \_ (CONSt D3D12 \_ resource \_ desc& o)**
</dt> <dd>

Crée une nouvelle instance d’une description de la \_ ressource CD3DX12 \_ , initialisée avec le contenu d’une autre structure [**\_ \_ desc des ressources D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) .

</dd> <dt>

**CD3DX12 \_ Resource \_ desc ( \_ dimension de dimension de ressource D3D12 \_ , alignement de UInt64, mise en forme de UInt64, hauteur uint, UINT16 depthOrArraySize, UInt16 miplevels a, \_ format de format dxgi, uint sampleCount, uint sampleQuality, \_ \_ disposition de texture de texture D3D12, \_ indicateurs d’indicateurs de ressources D3D12 \_ )**
</dt> <dd>

Crée une nouvelle instance d’une \_ Description de \_ la ressource CD3DX12, en initialisant les paramètres suivants :

[**D3D12 \_ Dimension de \_ dimension de ressource**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension)

Alignement de UINT64

La largeur UINT64

Hauteur UINT

UINT16 depthOrArraySize

UINT16 Miplevels a

[**Dxgi \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Format de format

UINT sampleCount

UINT sampleQuality

[**D3D12 \_ Disposition \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) de la texture

[**D3D12 \_ Indicateurs \_ de ressource**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) indicateurs

</dd> <dt>

**Mémoire tampon Inline statique (const D3D12 \_ Resource \_ ALLOCATION \_ info& resAllocInfo, D3D12 \_ indicateurs de ressource \_ indicateurs = D3D12 \_ indicateur de ressource \_ \_ aucun)**
</dt> <dd>

Spécifie une fonction qui initialise les paramètres suivants :

[**D3D12 \_ \_ \_ Informations d’allocation de ressources**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo

possibilité [**D3D12 \_ Indicateurs \_ de ressource**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) indicateurs = \_ indicateur de ressource D3D12 \_ \_ aucun

</dd> <dt>

**Mémoire tampon Inline statique (UINT64 Width, D3D12 \_ Resource \_ Flags Flags = D3D12 \_ Resource \_ Flag \_ None, UINT64 Alignment = 0)**
</dt> <dd>

Spécifie une fonction qui initialise les paramètres suivants :

La largeur UINT64

possibilité [**D3D12 \_ Indicateurs \_ de ressource**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) indicateurs = \_ indicateur de ressource D3D12 \_ \_ aucun

possibilité -Alignement de UINT64 = 0

</dd> <dt>

**static Inline Tex1D ( \_ format de format dxgi, UINT64 Width, UINT16 arraySize = 1, UINT16 miplevels a = 0, D3D12 \_ Resource \_ Flags Flags = D3D12 \_ \_ indicateur de ressource \_ None, D3D12 \_ texture \_ disposition layout = D3D12 \_ \_ disposition de texture \_ inconnue, alignement UINT64 = 0)**
</dt> <dd>

Spécifie une fonction qui initialise les paramètres suivants :

[**Dxgi \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Format de format

La largeur UINT64

possibilité UINT16 arraySize = 1

possibilité UINT16 Miplevels a = 0

possibilité [**D3D12 \_ Indicateurs \_ de ressource**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) indicateurs = \_ indicateur de ressource D3D12 \_ \_ aucun

possibilité [**D3D12 \_ Disposition \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) de la disposition de texture = \_ disposition de texture D3D12 \_ \_ inconnue

possibilité -Alignement de UINT64 = 0

</dd> <dt>

**static Inline Tex2D ( \_ format de format dxgi, UINT64 Width, valeur uint Height, UINT16 arraySize = 1, UINT16 miplevels a = 0, uint sampleCount = 1, uint sampleQuality = 0, D3D12 \_ Resource \_ Flags Flags = D3D12 \_ ressource \_ indicateur \_ None, D3D12 \_ texture \_ Layout disposition = D3D12 \_ \_ disposition de texture \_ inconnue, alignement de UINT64 = 0)**
</dt> <dd>

Spécifie une fonction qui initialise les paramètres suivants :

[**Dxgi \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Format de format

La largeur UINT64

Hauteur UINT

possibilité UINT16 arraySize = 1

possibilité UINT16 Miplevels a = 0

possibilité UINT sampleCount = 1

possibilité UINT sampleQuality = 0

possibilité [**D3D12 \_ Indicateurs \_ de ressource**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) indicateurs = \_ indicateur de ressource D3D12 \_ \_ aucun

possibilité [**D3D12 \_ Disposition \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) de la disposition de texture = \_ disposition de texture D3D12 \_ \_ inconnue

possibilité -Alignement de UINT64 = 0

</dd> <dt>

**static Inline Tex3D ( \_ format de format dxgi, UINT64 Width, valeur uint Height, fonction UInt16 Depth, Uint16 miplevels a = 0, D3D12 \_ Resource \_ Flags Flags = D3D12 \_ \_ indicateur \_ de ressource None, D3D12 \_ texture \_ disposition layout = D3D12 \_ \_ disposition de texture \_ inconnue, alignement UINT64 = 0)**
</dt> <dd>

Spécifie une fonction qui initialise les paramètres suivants :

[**Dxgi \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Format de format

La largeur UINT64

Hauteur UINT

Profondeur UINT16

possibilité UINT16 Miplevels a = 0

possibilité [**D3D12 \_ Indicateurs \_ de ressource**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) indicateurs = \_ indicateur de ressource D3D12 \_ \_ aucun

possibilité [**D3D12 \_ Disposition \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) de la disposition de texture = \_ disposition de texture D3D12 \_ \_ inconnue

possibilité -Alignement de UINT64 = 0

</dd> <dt>

**const de profondeur inline ()**
</dt> <dd>

Si dimension = = [**D3D12 \_ ressource \_ dimension**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension) \_ TEXTURE3D, retourne DepthOrArraySize. Si dimension ! = D3D12 \_ ressource \_ dimension \_ TEXTURE3D, retourne 1.

</dd> <dt>

**const Inline ArraySize ()**
</dt> <dd>

Si dimension ! = D3D12 \_ ressource \_ dimension \_ TEXTURE3D, retourne DepthOrArraySize. Si dimension = = D3D12 \_ ressource \_ dimension \_ TEXTURE3D, retourne 1. Voir [**la \_ \_ dimension de ressource D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension) \_ TEXTURE3D.

</dd> <dt>

**Inline PlaneCount (ID3D12Device \* pDevice) const**
</dt> <dd>

Retourne D3D12GetFormatPlaneCount (pDevice, format). Consultez [**D3D12GetFormatPlaneCount**](d3d12getformatplanecount.md) et [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device).

</dd> <dt>

**sous-ressources en ligne (ID3D12Device \* pDevice) const**
</dt> <dd>

Retourne le nombre de sous-ressources, calculé en tant que Miplevels a \* ArraySize () \* PlaneCount (pDevice).

</dd> <dt>

**Inline CalcSubresource (UINT MipSlice, UINT ArraySlice, UINT PlaneSlice)**
</dt> <dd>

Calcule un index de sous-ressource, à l’aide de [**D3D12CalcSubresource**](d3d12calcsubresource.md).

</dd> <dt>

**const D3D12 \_ Resource \_ desc& () const**
</dt> <dd>

Définit le & opérateur de passage par référence pour le type de structure parent.

</dd> <dt>

**opérateur = = (const D3D12 \_ Resource \_ desc& l, CONSt D3D12 \_ resource \_ desc& r)**
</dt> <dd>

Retourne la valeur true si tous les membres de chaque structure sont identiques.

</dd> <dt>

**opérateur ! = (const D3D12 \_ Resource \_ desc& l, CONSt D3D12 \_ resource \_ desc& r)**
</dt> <dd>

Retourne la valeur false si tous les membres de chaque structure sont identiques.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Description de la \_ ressource D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc)
</dt> <dt>

[Structures d’assistance pour D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

