---
title: Structure CD3DX12_RANGE (D3dx12. h)
description: Structure d’assistance pour faciliter l’initialisation d’une \_ structure de plage D3D12.
ms.assetid: 5D5192BF-D14C-487B-A214-F8428E82AF0E
keywords:
- Structure CD3DX12_RANGE
topic_type:
- apiref
api_name:
- CD3DX12_RANGE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66b6b92cd24a981d48252f5ad457f7ac0320e2d7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106528575"
---
# <a name="cd3dx12_range-structure"></a>Structure de la \_ plage CD3DX12

Structure d’assistance pour faciliter l’initialisation d’une structure de [**\_ plage D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range) .

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_RANGE  : public D3D12_RANGE{
   CD3DX12_RANGE();
   explicit CD3DX12_RANGE(const D3D12_RANGE &o);
   CD3DX12_RANGE(SIZE_T begin, SIZE_T end);
   operator const D3D12_RANGE&() const;
};
```



## <a name="members"></a>Membres

<dl> <dt>

**\_Plage CD3DX12 ()**
</dt> <dd>

Crée une nouvelle instance non initialisée d’une \_ plage CD3DX12.

</dd> <dt>

**plage CD3DX12 explicite \_ (const D3D12 \_ Range &o)**
</dt> <dd>

Crée une nouvelle instance d’une \_ plage CD3DX12, initialisée avec le contenu d’une autre structure de [**\_ plage D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range) .

</dd> <dt>

**\_Plage CD3DX12 (taille \_ t début, taille \_ t fin)**
</dt> <dd>

Crée une nouvelle instance d’une \_ plage CD3DX12, en initialisant les paramètres suivants :

TAILLE \_ T début

Fin de la taille \_ T

</dd> <dt>

**\_const, opérateur D3D12& () const**
</dt> <dd>

Définit le & opérateur de passage par référence pour le type de structure parent.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Plage D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range)
</dt> <dt>

[Structures d’assistance pour D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





