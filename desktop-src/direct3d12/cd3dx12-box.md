---
title: Structure CD3DX12_BOX (D3dx12. h)
description: Structure d’assistance pour faciliter l’initialisation d’une \_ structure de zone D3D12.
ms.assetid: 7E1A352C-D664-4538-BA78-91493980559D
keywords:
- Structure CD3DX12_BOX
topic_type:
- apiref
api_name:
- CD3DX12_BOX
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.topic: reference
ms.localizationpriority: low
ms.date: 05/31/2018
ms.openlocfilehash: c689c9bfe611651248280f7536bd91a9f4d003d4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106537243"
---
# <a name="cd3dx12_box-structure"></a>\_Structure de la boîte de CD3DX12

Structure d’assistance pour faciliter l’initialisation d’une structure de [**\_ zone D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box) .

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_BOX  : public D3D12_BOX{
   CD3DX12_BOX();
   explicit CD3DX12_BOX(const D3D12_BOX& o);
   explicit CD3DX12_BOX(LONG Left, LONG Right);
   explicit CD3DX12_BOX(LONG Left, LONG Top, LONG Right, LONG Bottom);
   explicit CD3DX12_BOX(LONG Left, LONG Top, LONG Front, LONG Right, LONG Bottom, LONG Back);
   ~CD3DX12_BOX();
   operator const D3D12_BOX&() const;
};
```



## <a name="members"></a>Membres

<dl> <dt>

**CD3DX12 \_ Box ()**
</dt> <dd>

Crée une nouvelle instance non initialisée d’une \_ zone CD3DX12.

</dd> <dt>

**zone CD3DX12 explicite \_ (const D3D12 \_ Box& o)**
</dt> <dd>

Crée une nouvelle instance d’une \_ zone CD3DX12, initialisée avec le contenu d’une autre structure de [**\_ zone D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box) .

</dd> <dt>

**zone CD3DX12 explicite \_ (longue gauche, long droit)**
</dt> <dd>

Crée une nouvelle instance d’une \_ zone CD3DX12, en initialisant les paramètres suivants :

LONGUE gauche

LONG droit

</dd> <dt>

**zone CD3DX12 explicite \_ (longue gauche, long haut, long droit, long Bottom)**
</dt> <dd>

Crée une nouvelle instance d’une \_ zone CD3DX12, en initialisant les paramètres suivants :

LONGUE gauche

LONG haut

LONG droit

LONG bas

</dd> <dt>

**zone CD3DX12 explicite \_ (longue gauche, longue, longue, longue, longue, longue, longue, longue, long)**
</dt> <dd>

Crée une nouvelle instance d’une \_ zone CD3DX12, en initialisant les paramètres suivants :

LONGUE gauche

LONG haut

LONG avant

LONG droit

LONG bas

Retour à LONG terme

</dd> <dt>

**~ CD3DX12 \_ Box ()**
</dt> <dd>

Détruit une instance d’une zone CD3DX12 \_ .

</dd> <dt>

**\_const D3D12, zone& () const**
</dt> <dd>

Définit le & opérateur de passage par référence pour le type de structure parent.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Zone D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box)
</dt> <dt>

[Structures d’assistance pour D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





