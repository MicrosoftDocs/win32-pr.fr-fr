---
title: Structure CD3DX12_RT_FORMAT_ARRAY (D3dx12. h)
description: Structure d’assistance pour faciliter l’initialisation d’une \_ structure de tableau de \_ format D3D12 RT \_ .
ms.assetid: E890DD33-599F-4B20-BD15-2734867788E5
keywords:
- Structure CD3DX12_RT_FORMAT_ARRAY
topic_type:
- apiref
api_name:
- CD3DX12_RT_FORMAT_ARRAY
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a9c153b98e84176d2682f028657176902fb68ebc0e8e1e52c69c196842dc2fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988359"
---
# <a name="cd3dx12_rt_format_array-structure"></a>\_Structure de \_ tableau de format CD3DX12 RT \_

Structure d’assistance pour faciliter l’initialisation d’une structure de [**\_ tableau de \_ format \_ D3D12 RT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) .

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_RT_FORMAT_ARRAY  : public D3D12_RT_FORMAT_ARRAY{
  CD3DX12_RT_FORMAT_ARRAY CD3DX12_RT_FORMAT_ARRAY();
  CD3DX12_RT_FORMAT_ARRAY explicit CD3DX12_RT_FORMAT_ARRAY(const D3D12_RT_FORMAT_ARRAY& o);
  CD3DX12_RT_FORMAT_ARRAY explicit CD3DX12_RT_FORMAT_ARRAY(const DXGI_FORMAT* pFormats, UINT NumFormats);
                          operator const D3D12_RT_FORMAT_ARRAY&() const;
};
```



## <a name="members"></a>Membres

<dl> <dt>

**\_ \_ Tableau de format CD3DX12 RT \_ ()**
</dt> <dd>

Crée une nouvelle instance non initialisée d’un \_ tableau de format CD3DX12 \_ RT \_ .

</dd> <dt>

**\_ \_ tableau de format CD3DX12 RT explicite \_ (const D3D12 \_ RT \_ format \_ tableau& o)**
</dt> <dd>

Crée une nouvelle instance d’un \_ tableau de format CD3DX12 RT \_ \_ , initialisée avec les valeurs copiées à partir d’une structure de [**\_ \_ \_ tableau de format D3D12 RT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) .

</dd> <dt>

**\_ \_ tableau de format CD3DX12 RT explicite \_ (const dxgi \_ format \* pFormats, uint NumFormats)**
</dt> <dd>

Crée une nouvelle instance d’un \_ tableau de format CD3DX12 RT \_ \_ , initialisée avec les valeurs passées dans la liste de paramètres. Le contenu du tableau spécifié par le paramètre *pFormats* est copié dans le tableau de membres **RTFormats**. Le tableau spécifié par *pFormats* est supposé avoir la même taille que **RTFormats**.

</dd> <dt>

**const D3D12 \_ RT \_ FORMAT \_ tableau& () const**
</dt> <dd>

Conversion implicite en structure de [**\_ tableau de \_ format \_ D3D12 RT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) . Étant donné \_ que \_ \_ le tableau de format D3D12 RT est le type sous-jacent de \_ stencil de profondeur CD3DX12 \_ \_ DESC1, l’objet est simplement retourné en tant que référence de tableau de format const D3D12 \_ RT \_ \_ à lui-même.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures d’assistance pour D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**\_Tableau de \_ format D3D12 RT \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)
</dt> </dl>

 

 





