---
title: Structure CD3DX12_RESOURCE_DESC1 (D3dx12. h)
description: Structure d’assistance pour faciliter l’initialisation d’une structure [**D3DX12_RESOURCE_DESC1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_view_instancing_desc) .
keywords:
- Structure CD3DX12_RESOURCE_DESC1
topic_type:
- apiref
api_name:
- CD3DX12_RESOURCE_DESC1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2021
ms.openlocfilehash: 87fe62c475e1d961258671355c4c9be133bf0a41
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918511"
---
# <a name="cd3dx12_resource_desc1-structure"></a>Structure CD3DX12_RESOURCE_DESC1

Structure d’assistance pour faciliter l’initialisation d’une structure [**D3DX12_RESOURCE_DESC1**](/windows/win32/api/d3d12/D3DX12_RESOURCE_DESC1/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_desc1) .

## <a name="syntax"></a>Syntaxe

```cpp
struct CD3DX12_RESOURCE_DESC1 : public D3D12_RESOURCE_DESC1
{
    CD3DX12_RESOURCE_DESC1();
    explicit CD3DX12_RESOURCE_DESC1(const D3D12_RESOURCE_DESC1& o) noexcept;
    CD3DX12_RESOURCE_DESC1(
        D3D12_RESOURCE_DIMENSION dimension,
        UINT64 alignment,
        UINT64 width,
        UINT height,
        UINT16 depthOrArraySize,
        UINT16 mipLevels,
        DXGI_FORMAT format,
        UINT sampleCount,
        UINT sampleQuality,
        D3D12_TEXTURE_LAYOUT layout,
        D3D12_RESOURCE_FLAGS flags,
        UINT samplerFeedbackMipRegionWidth = 0,
        UINT samplerFeedbackMipRegionHeight = 0,
        UINT samplerFeedbackMipRegionDepth = 0) noexcept;
    static inline CD3DX12_RESOURCE_DESC1 Buffer(
        const D3D12_RESOURCE_ALLOCATION_INFO& resAllocInfo,
        D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE) noexcept;
    static inline CD3DX12_RESOURCE_DESC1 Buffer(
        UINT64 width,
        D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE,
        UINT64 alignment = 0) noexcept;
    static inline CD3DX12_RESOURCE_DESC1 Tex1D(
        DXGI_FORMAT format,
        UINT64 width,
        UINT16 arraySize = 1,
        UINT16 mipLevels = 0,
        D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE,
        D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN,
        UINT64 alignment = 0) noexcept;
    static inline CD3DX12_RESOURCE_DESC1 Tex2D(
        DXGI_FORMAT format,
        UINT64 width,
        UINT height,
        UINT16 arraySize = 1,
        UINT16 mipLevels = 0,
        UINT sampleCount = 1,
        UINT sampleQuality = 0,
        D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE,
        D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN,
        UINT64 alignment = 0,
        UINT samplerFeedbackMipRegionWidth = 0,
        UINT samplerFeedbackMipRegionHeight = 0,
        UINT samplerFeedbackMipRegionDepth = 0) noexcept;
    static inline CD3DX12_RESOURCE_DESC1 Tex3D(
        DXGI_FORMAT format,
        UINT64 width,
        UINT height,
        UINT16 depth,
        UINT16 mipLevels = 0,
        D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE,
        D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN,
        UINT64 alignment = 0) noexcept;
    inline UINT16 Depth() const noexcept;
    inline UINT16 ArraySize() const noexcept;
    inline UINT8 PlaneCount(_In_ ID3D12Device* pDevice) const noexcept;
    inline UINT Subresources(_In_ ID3D12Device* pDevice) const noexcept;
    inline UINT CalcSubresource(UINT MipSlice, UINT ArraySlice, UINT PlaneSlice) noexcept;
};
inline bool operator==(const D3D12_RESOURCE_DESC1& l, const D3D12_RESOURCE_DESC1& r) noexcept;
inline bool operator!=(const D3D12_RESOURCE_DESC1& l, const D3D12_RESOURCE_DESC1& r) noexcept;
```

## <a name="members"></a>Membres

`CD3DX12_RESOURCE_DESC1`

Constructeur par défaut. Crée une nouvelle instance non initialisée d’un **CD3DX12_RESOURCE_DESC1**.

`CD3DX12_RESOURCE_DESC1(const D3D12_RESOURCE_DESC1&)`

Constructeur qui crée une nouvelle instance d’un **CD3DX12_RESOURCE_DESC1** initialisé avec le contenu d’une structure [**D3DX12_RESOURCE_DESC1**](/windows/win32/api/d3d12/D3DX12_RESOURCE_DESC1/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_desc1) .

`CD3DX12_RESOURCE_DESC1(D3D12_RESOURCE_DIMENSION, UINT64, UINT64, UINT, UINT16, UINT16, DXGI_FORMAT, UINT, UINT, D3D12_TEXTURE_LAYOUT, D3D12_RESOURCE_FLAGS, UINT = 0, UINT = 0, UINT = 0)`

Constructeur qui crée une nouvelle instance d’un **CD3DX12_RESOURCE_DESC1** initialisé avec les paramètres qui lui sont passés.

`Buffer(const D3D12_RESOURCE_ALLOCATION_INFO&, D3D12_RESOURCE_FLAGS = D3D12_RESOURCE_FLAG_NONE)`

Fonction statique qui construit et retourne une nouvelle instance d’une **CD3DX12_RESOURCE_DESC1** initialisée avec ces valeurs.

|Membre de données|value|
|-|-|
|Dimension|D3D12_RESOURCE_DIMENSION_BUFFER|
|Alignment|*resAllocInfo*. Repère|
|Largeur|*resAllocInfo*. SizeInBytes|
|Hauteur|1|
|DepthOrArraySize|1|
|Miplevels a|1|
|Format|DXGI_FORMAT_UNKNOWN|
|SampleDesc. Count|1|
|SampleDesc. Quality|0|
|Layout|D3D12_TEXTURE_LAYOUT_ROW_MAJOR|
|Indicateurs|*flags*|
|SamplerFeedbackMipRegion. Width|0|
|SamplerFeedbackMipRegion. Height|0|
|SamplerFeedbackMipRegion. Depth|0|

`Buffer(UINT64, D3D12_RESOURCE_FLAGS = D3D12_RESOURCE_FLAG_NONE, UINT64 = 0)`

Fonction statique qui construit et retourne une nouvelle instance d’une **CD3DX12_RESOURCE_DESC1** initialisée avec ces valeurs.

|Membre de données|value|
|-|-|
|Dimension|D3D12_RESOURCE_DIMENSION_BUFFER|
|Alignment|*repère*|
|Largeur|*width*|
|Hauteur|1|
|DepthOrArraySize|1|
|Miplevels a|1|
|Format|DXGI_FORMAT_UNKNOWN|
|SampleDesc. Count|1|
|SampleDesc. Quality|0|
|Layout|D3D12_TEXTURE_LAYOUT_ROW_MAJOR|
|Indicateurs|*flags*|
|SamplerFeedbackMipRegion. Width|0|
|SamplerFeedbackMipRegion. Height|0|
|SamplerFeedbackMipRegion. Depth|0|

`Tex1D(DXGI_FORMAT, UINT64, UINT16 = 1, UINT16 = 0, D3D12_RESOURCE_FLAGS D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 = 0)`

Fonction statique qui construit et retourne une nouvelle instance d’une **CD3DX12_RESOURCE_DESC1** initialisée avec ces valeurs.

|Membre de données|value|
|-|-|
|Dimension|D3D12_RESOURCE_DIMENSION_TEXTURE1D|
|Alignment|*repère*|
|Largeur|*width*|
|Hauteur|1|
|DepthOrArraySize|*arraySize*|
|Miplevels a|*Miplevels a*|
|Format|*format*|
|SampleDesc. Count|1|
|SampleDesc. Quality|0|
|Layout|*dispose*|
|Indicateurs|*flags*|
|SamplerFeedbackMipRegion. Width|0|
|SamplerFeedbackMipRegion. Height|0|
|SamplerFeedbackMipRegion. Depth|0|

`Tex2D(DXGI_FORMAT, UINT64, UINT, UINT16 = 1, UINT16 = 0, UINT = 1, UINT = 0, D3D12_RESOURCE_FLAGS = D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 = 0, UINT = 0, UINT = 0, UINT = 0)`

Fonction statique qui construit et retourne une nouvelle instance d’une **CD3DX12_RESOURCE_DESC1** initialisée avec ces valeurs.

|Membre de données|value|
|-|-|
|Dimension|D3D12_RESOURCE_DIMENSION_TEXTURE2D|
|Alignment|*repère*|
|Largeur|*width*|
|Hauteur|*height*|
|DepthOrArraySize|*arraySize*|
|Miplevels a|*Miplevels a*|
|Format|*format*|
|SampleDesc. Count|*sampleCount*|
|SampleDesc. Quality|*sampleQuality*|
|Layout|*dispose*|
|Indicateurs|*flags*|
|SamplerFeedbackMipRegion. Width|*samplerFeedbackMipRegionWidth*|
|SamplerFeedbackMipRegion. Height|*samplerFeedbackMipRegionHeight*|
|SamplerFeedbackMipRegion. Depth|*samplerFeedbackMipRegionDepth*|

`Tex3D(DXGI_FORMAT, UINT64, UINT, UINT16, UINT16 = 0, D3D12_RESOURCE_FLAGS = D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 = 0)`

Fonction statique qui construit et retourne une nouvelle instance d’une **CD3DX12_RESOURCE_DESC1** initialisée avec ces valeurs.

|Membre de données|value|
|-|-|
|Dimension|D3D12_RESOURCE_DIMENSION_TEXTURE3D|
|Alignment|*repère*|
|Largeur|*width*|
|Hauteur|*height*|
|DepthOrArraySize|*profondeur*|
|Miplevels a|*Miplevels a*|
|Format|*format*|
|SampleDesc. Count|1|
|SampleDesc. Quality|0|
|Layout|*dispose*|
|Indicateurs|*flags*|
|SamplerFeedbackMipRegion. Width|0|
|SamplerFeedbackMipRegion. Height|0|
|SamplerFeedbackMipRegion. Depth|0|

`Depth`

Retourne un **UINT16** contenant la profondeur de la ressource.

`ArraySize`

Retourne un **UINT16** contenant la taille du tableau de la ressource.

`PlaneCount(ID3D12Device*)`

Retourne un **UINT8** contenant le nombre de plans pour le format de la ressource.

`Subresources(ID3D12Device*)`

Retourne un **uint** qui contient le nombre de sous-ressources dans la ressource.

`CalcSubresource(UINT, UINT, UINT)`

Caculates et retourne un **uint** qui contient un index de sous-ressources pour la ressource en fonction des paramètres qui lui sont passés.

`operator==(const D3D12_RESOURCE_DESC1&, const D3D12_RESOURCE_DESC1&)`

Fonction libre qui retourne `true` si les deux paramètres sont égaux au niveau du membre ; sinon, `false` .

`operator!=(const D3D12_RESOURCE_DESC1&, const D3D12_RESOURCE_DESC1&)`

Fonction libre qui retourne `true` si les deux paramètres sont non égaux au niveau du membre ; sinon, `false` .

## <a name="requirements"></a>Spécifications

| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête | [D3dx12. h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Voir aussi

* [D3DX12_RESOURCE_DESC1](/windows/win32/api/d3d12/D3DX12_RESOURCE_DESC1/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_desc1)
* [Structures d’assistance pour Direct3D 12](helper-structures-for-d3d12.md)
