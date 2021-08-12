---
title: Fonction Updatesubresources par (allocation de pile) (D3dx12. h)
description: Met à jour les sous-ressources avec une implémentation d’allocation de pile.
ms.assetid: 2F30FDF1-4450-473E-AEA8-C5FF54260BCE
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
ms.openlocfilehash: 43ffe9dd9e519b402126976db8ceaf1aba32f6d36a73745c951bb6a8db52a7fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118300444"
---
# <a name="updatesubresources-stack-allocating-function"></a>Updatesubresources par (allocation de pile) (fonction)

Met à jour les sous-ressources avec une implémentation d’allocation de pile.

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

*IntermediateOffset* 
</dt> <dd>

Type : **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**

Offset, en octets, de la ressource intermédiaire.

</dd> <dt>

*FirstSubresource* \[ dans\]
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Index de la première sous-ressource dans la ressource. Les valeurs valides sont comprises entre 0 et *MaxSubresources*.

</dd> <dt>

*NumSubresources* \[ dans\]
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Nombre de sous-ressources dans la ressource. Les valeurs valides sont comprises entre 1 et (*MaxSubresources*  -  *FirstSubresource*).

</dd> <dt>

*pSrcData* \[ dans\]
</dt> <dd>

Type : données de sous- **[ **\_ ressource \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)\***

Pointeur vers un tableau (de longueur *NumSubresources*) de pointeurs vers des structures de données de sous- [**\_ \_ ressources D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) contenant les descriptions des données de sous-ressources utilisées pour la mise à jour.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**

Taille en octets de la mémoire tampon.

## <a name="remarks"></a>Notes

La déclaration de cette fonction commence par : `template <UINT MaxSubresources>`

## <a name="requirements"></a>Configuration requise



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

 

