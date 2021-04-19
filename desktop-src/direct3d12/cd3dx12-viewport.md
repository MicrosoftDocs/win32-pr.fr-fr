---
title: Structure CD3DX12_VIEWPORT (D3dx12. h)
description: Structure d’assistance pour faciliter l’initialisation d’une \_ structure de fenêtre d’affichage D3D12.
ms.assetid: 1A824F54-596B-450E-A191-B60FBBBB60ED
keywords:
- Structure CD3DX12_VIEWPORT
topic_type:
- apiref
api_name:
- CD3DX12_VIEWPORT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da29adc50b62bd645070d9667bec1e5c7ce7ab15
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535206"
---
# <a name="cd3dx12_viewport-structure"></a>Structure de la \_ fenêtre d’affichage CD3DX12

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]

Structure d’assistance pour faciliter l’initialisation d’une structure de [**\_ fenêtre d’affichage D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_viewport) .

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_VIEWPORT  : public D3D12_VIEWPORT{
   CD3DX12_VIEWPORT();
   explicit CD3DX12_VIEWPORT(const D3D12_VIEWPORT& o);
   explicit CD3DX12_VIEWPORT(FLOAT topLeftX, FLOAT topLeftY, FLOAT width, FLOAT height, FLOAT minDepth = D3D12_MIN_DEPTH, FLOAT maxDepth = D3D12_MAX_DEPTH);
   explicit CD3DX12_VIEWPORT(ID3D12Resource* pResource, UINT mipSlice = 0, FLOAT topLeftX = 0.0f, FLOAT topLeftY = 0.0f, FLOAT minDepth = D3D12_MIN_DEPTH, FLOAT maxDepth = D3D12_MAX_DEPTH);
   ~CD3DX12_VIEWPORT();
   operator const D3D12_VIEWPORT&() const;
};
```



## <a name="members"></a>Membres

<dl> <dt>

**CD3DX12 \_ VIEWPORT ()**
</dt> <dd>

Crée une nouvelle instance non initialisée d’une \_ fenêtre d’affichage CD3DX12.

</dd> <dt>

**Viewport CD3DX12 explicite \_ (fenêtre d’affichage const D3D12 \_& o)**
</dt> <dd>

Crée une nouvelle instance d’une \_ fenêtre d’affichage CD3DX12, en initialisant les paramètres suivants :

& de la fenêtre d’affichage const D3D12 \_

</dd> <dt>

**VIEWPORT CD3DX12 explicite \_ (float topLeftX, float point Left, Floating, float height, float minDepth = D3D12 \_ Min \_ profondeur, float maxdepth = D3D12 \_ Max \_ depth)**
</dt> <dd>

Crée une nouvelle instance d’une \_ fenêtre d’affichage CD3DX12, en initialisant les paramètres suivants :

TopLeftX FLOAT

Virgule flottante à gauche

Largeur de la virgule flottante

Hauteur de flotte

FLOAT minDepth = D3D12 \_ Min \_ Depth

FLOAT maxDepth = D3D12 \_ Max \_ Depth

</dd> <dt>

**VIEWPORT CD3DX12 explicite \_ (ID3D12Resource \* présource, uint mipSlice = 0, float topLeftX = 0.0 f, float Left = 0.0 f, float MINDEPTH = D3D12 \_ Min \_ Depth, float maxdepth = D3D12 \_ Max \_ depth)**
</dt> <dd>

Crée une nouvelle instance d’une \_ fenêtre d’affichage CD3DX12, en initialisant les paramètres suivants :

ID3D12Resource préversion \*

UINT mipSlice = 0

FLOAT topLeftX = 0.0 f

FLOAT Left = 0.0 f

FLOAT minDepth = D3D12 \_ Min \_ Depth

FLOAT maxDepth = D3D12 \_ Max \_ Depth

</dd> <dt>

**~ CD3DX12 \_ VIEWPORT ()**
</dt> <dd>

Détruit une instance d’une fenêtre d' \_ affichage D3DX12.

</dd> <dt>

**\_const D3D12 fenêtre d’affichage& () const**
</dt> <dd>

Définit le & opérateur de passage par référence pour le type de structure parent.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**D3D12 \_ VIEWPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_viewport)
</dt> <dt>

[Structures d’assistance pour D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





