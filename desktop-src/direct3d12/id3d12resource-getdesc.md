---
title: Méthode ID3D12Resource GetDesc
description: Obtient la description de la ressource.
ms.assetid: B8D84D69-6B13-4E86-8EF6-A841354B1E5C
keywords:
- Méthode GetDesc
- Méthode GetDesc, interface ID3D12Resource
- Interface ID3D12Resource, méthode GetDesc
topic_type:
- apiref
api_name:
- ID3D12Resource.GetDesc
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
api_location:
- d3d12.h
ms.openlocfilehash: 179acfa051212a2f98eb94441cbfad9fd7d9bbab47e4616f82a4f4cff3d41035
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069629"
---
# <a name="id3d12resourcegetdesc-method"></a>ID3D12Resource :: GetDesc, méthode

Obtient la description de la ressource.

## <a name="syntax"></a>Syntaxe


```C++
D3D12_RESOURCE_DESC GetDesc();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : description de la **[ **\_ ressource \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc)**

Structure de description de la ressource Direct3D 12.

## <a name="examples"></a>Exemples

Retourne la taille requise d’une mémoire tampon à utiliser pour le téléchargement de données.


```C++
// Returns required size of a buffer to be used for data upload
inline UINT64 GetRequiredIntermediateSize(
    _In_ ID3D12Resource* pDestinationResource,
    _In_range_(0,D3D12_REQ_SUBRESOURCES) UINT FirstSubresource,
    _In_range_(0,D3D12_REQ_SUBRESOURCES-FirstSubresource) UINT NumSubresources)
{
    D3D12_RESOURCE_DESC Desc = pDestinationResource->GetDesc();
    UINT64 RequiredSize = 0;
    
    ID3D12Device* pDevice;
    pDestinationResource->GetDevice(__uuidof(*pDevice), reinterpret_cast<void**>(&pDevice));
    pDevice->GetCopyableFootprints(&Desc, FirstSubresource, NumSubresources, 0, nullptr, nullptr, nullptr, &RequiredSize);
    pDevice->Release();
    
    return RequiredSize;
}
```



Reportez-vous à l' [exemple de code dans la référence D3D12](notes-on-example-code.md).

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)
</dt> </dl>

 

 




