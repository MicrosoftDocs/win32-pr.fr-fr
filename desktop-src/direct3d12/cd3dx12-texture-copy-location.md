---
title: Structure CD3DX12_TEXTURE_COPY_LOCATION (D3dx12. h)
description: Structure d’assistance pour permettre l’initialisation facile d’une structure d' \_ emplacement de copie de texture D3D12 \_ \_ .
ms.assetid: 8BA93729-2FFB-4C09-88B0-779049BAF385
keywords:
- Structure CD3DX12_TEXTURE_COPY_LOCATION
topic_type:
- apiref
api_name:
- CD3DX12_TEXTURE_COPY_LOCATION
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d0a1ee179d2400bc04df9c3214d97d3c7a861357f33b7805e492a24f769bdba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119639"
---
# <a name="cd3dx12_texture_copy_location-structure"></a>CD3DX12 \_ structure de l’emplacement de copie de texture \_ \_

Structure d’assistance pour permettre l’initialisation facile d’une structure [**d' \_ \_ \_ emplacement de copie de texture D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) .

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_TEXTURE_COPY_LOCATION  : public D3D12_TEXTURE_COPY_LOCATION{
   CD3DX12_TEXTURE_COPY_LOCATION();
   explicit CD3DX12_TEXTURE_COPY_LOCATION(const D3D12_TEXTURE_COPY_LOCATION &o);
   CD3DX12_TEXTURE_COPY_LOCATION(ID3D12Resource* pRes);
   CD3DX12_TEXTURE_COPY_LOCATION(ID3D12Resource* pRes, D3D12_PLACED_SUBRESOURCE_FOOTPRINT const& Footprint);
   CD3DX12_TEXTURE_COPY_LOCATION(ID3D12Resource* pRes, UINT Sub);
};
```



## <a name="members"></a>Membres

<dl> <dt>

**\_ \_ \_ Emplacement de copie de texture CD3DX12 ()**
</dt> <dd>

Crée une nouvelle instance non initialisée d’un \_ emplacement de copie de texture CD3DX12 \_ \_ .

</dd> <dt>

**\_ \_ emplacement de copie de texture CD3DX12 explicite \_ (const D3D12 \_ texture \_ \_ location &o)**
</dt> <dd>

Crée une nouvelle instance d’un \_ emplacement de copie de texture CD3DX12 \_ \_ , initialisée avec le contenu d’une autre structure d’emplacement de [**\_ copie de texture \_ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) .

</dd> <dt>

**\_ \_ \_ Emplacement de copie de texture CD3DX12 (ID3D12Resource \* pRes)**
</dt> <dd>

Crée une nouvelle instance d’un \_ emplacement de copie de texture CD3DX12 \_ \_ , en initialisant les paramètres suivants :

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* Régisseur

</dd> <dt>

**\_ \_ \_ Emplacement de copie de texture CD3DX12 (ID3D12RESOURCE \* pRes, D3D12 a placé l’empreinte de sous- \_ \_ ressources \_ const& encombrement)**
</dt> <dd>

Crée une nouvelle instance d’un \_ emplacement de copie de texture CD3DX12 \_ \_ , en initialisant les paramètres suivants :

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* Régisseur

[**D3D12 \_ Empreinte \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint) des& CONSt imposées sur les sous-ressources

</dd> <dt>

**\_ \_ \_ Emplacement de copie de texture CD3DX12 (ID3D12RESOURCE \* pRes, uint Sub)**
</dt> <dd>

Crée une nouvelle instance d’un \_ emplacement de copie de texture CD3DX12 \_ \_ , en initialisant les paramètres suivants :

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* Régisseur

UINT Sub

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Emplacement de \_ copie de texture D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location)
</dt> <dt>

[Structures d’assistance pour D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





