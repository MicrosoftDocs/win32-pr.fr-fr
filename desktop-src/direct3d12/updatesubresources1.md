---
title: Updatesubresources par, fonction (D3dx12. h)
description: Met à jour les sous-ressources, tous les tableaux de sous-ressources doivent être remplis, en général en appelant ID3D12Device GetCopyableFootprints.
ms.assetid: D6885165-095E-452D-8D93-A2C43A215F48
keywords:
- Updatesubresources par fonction)
topic_type:
- apiref
api_name:
- UpdateSubresources
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 885ee058aacbfca238448830f2b7b1b54a298f89
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012856"
---
# <a name="updatesubresources-function"></a>Updatesubresources par fonction)

Met à jour les sous-ressources, tous les tableaux de sous-ressources doivent être remplis, en général en appelant [**ID3D12Device :: GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints).

## <a name="syntax"></a>Syntaxe


```C++
UINT64 inline UpdateSubresources(
  _In_       ID3D12GraphicsCommandList          *pCmdList,
  _In_       ID3D12Resource                     *pDestinationResource,
  _In_       ID3D12Resource                     *pIntermediate,
  _In_       UINT                               FirstSubresource,
  _In_       UINT                               NumSubresources,
             UINT64                             RequiredSize,
  _In_ const D3D12_PLACED_SUBRESOURCE_FOOTPRINT *pLayouts,
  _In_ const UINT                               *pNumRows,
  _In_ const UINT64                             *pRowSizesInBytes,
  _In_ const D3D12_SUBRESOURCE_DATA             *pSrcData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pCmdList* \[ dans\]
</dt> <dd>

Type : **[ **ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***

La liste de commandes, en tant que pointeur vers un [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).

</dd> <dt>

*pDestinationResource* \[ dans\]
</dt> <dd>

Type : **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***

La ressource de destination, en tant que pointeur vers un [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).

</dd> <dt>

*pIntermediate* \[ dans\]
</dt> <dd>

Type : **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***

Ressource intermédiaire, en tant que pointeur vers un [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).

</dd> <dt>

*FirstSubresource* \[ dans\]
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Index de la première sous-ressource dans la ressource. La plage de valeurs valides est comprise entre 0 et des sous- \_ ressources D3D12 req \_ .

</dd> <dt>

*NumSubresources* \[ dans\]
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Nombre de sous-ressources dans la ressource. La plage de valeurs valides est comprise entre 0 et (D3D12 \_ req \_ Resources- *FirstSubresource*).

</dd> <dt>

*RequiredSize* 
</dt> <dd>

Type : **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**

Taille requise, en octets, de la mise à jour.

</dd> <dt>

*pLayouts* \[ dans\]
</dt> <dd>

Type : **const [**D3D12 a \_ placé l' \_ \_ encombrement**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint) \*** des sous-ressources

Pointeur vers un tableau (de longueur *NumSubresources*) de pointeurs vers les structures qui contiennent la description et le placement des sous-ressources de la ressource.

</dd> <dt>

*pNumRows* \[ dans\]
</dt> <dd>

Type : **const [**uint**](/windows/desktop/WinProg/windows-data-types) \***

Pointeur vers un tableau (de longueur *NumSubresources*) de Uints contenant le nombre de lignes pour chaque sous-ressource.

</dd> <dt>

*pRowSizesInBytes* \[ dans\]
</dt> <dd>

Type : **const [**UINT64**](/windows/desktop/WinProg/windows-data-types) \***

Pointeur vers un tableau (de longueur *NumSubresources*) de uint qui contient la taille, en octets, de chaque ligne.

</dd> <dt>

*pSrcData* \[ dans\]
</dt> <dd>

Type : **const [**D3D12 les \_ \_ données**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) \*** de sous-ressource

Pointeur vers un tableau (de longueur *NumSubresources*) de pointeurs vers des structures de données de sous- [**\_ \_ ressources D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) contenant les descriptions des données de sous-ressources utilisées pour la mise à jour.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**

Taille en octets de la mémoire tampon.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx12. h</dt> </dl>  |
| Bibliothèque<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions d’assistance pour D3D12](helper-functions-for-d3d12.md)
</dt> <dt>

[Sous-ressources](subresources.md)
</dt> </dl>

 

