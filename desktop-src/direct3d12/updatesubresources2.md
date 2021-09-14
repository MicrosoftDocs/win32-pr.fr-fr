---
title: Updatesubresources par (allocation de segment de mémoire), fonction (D3dx12. h)
description: Met à jour les sous-ressources avec une implémentation d’allocation de tas.
ms.assetid: 328D8755-D328-471D-AAF4-9771CBFF7539
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
ms.openlocfilehash: c97abe59bdd0334fe4b7badf03e44ddc03b85495
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012857"
---
# <a name="updatesubresources-heap-allocating-function"></a>Updatesubresources par (allocation du tas) (fonction)

Met à jour les sous-ressources avec une implémentation d’allocation de tas.

## <a name="syntax"></a>Syntaxe


```C++
UINT64 inline UpdateSubresources(
  _In_ ID3D12GraphicsCommandList *pCmdList,
  _In_ ID3D12Resource            *pDestinationResource,
  _In_ ID3D12Resource            *pIntermediate,
       UINT64                    IntermediateOffset,
  _In_ UINT                      FirstSubresource,
  _In_ UINT                      NumSubresources,
  _In_ D3D12_SUBRESOURCE_DATA    *pSrcData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pCmdList* \[ dans\]
</dt> <dd>

Type : **[ **ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***

Pointeur vers l’interface [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist) pour la liste de commandes.

</dd> <dt>

*pDestinationResource* \[ dans\]
</dt> <dd>

Type : **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***

Pointeur vers l’interface [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) qui représente la ressource de destination.

</dd> <dt>

*pIntermediate* \[ dans\]
</dt> <dd>

Type : **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***

Pointeur vers l’interface [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) qui représente la ressource intermédiaire.

</dd> <dt>

*IntermediateOffset* 
</dt> <dd>

Type : **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**

Offset, en octets, de la ressource intermédiaire.

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

*pSrcData* \[ dans\]
</dt> <dd>

Type : données de sous- **[ **\_ ressource \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)\***

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

 

