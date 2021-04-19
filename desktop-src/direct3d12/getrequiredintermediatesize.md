---
title: GetRequiredIntermediateSize, fonction (D3dx12. h)
description: Retourne la taille requise d’une mémoire tampon à utiliser pour le téléchargement de données.
ms.assetid: 424B52E9-DE52-40D2-B8B0-C27FD3D3C298
keywords:
- GetRequiredIntermediateSize fonction)
topic_type:
- apiref
api_name:
- GetRequiredIntermediateSize
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15293ce1588704d55f41c364c35db57cbf4c869d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106537267"
---
# <a name="getrequiredintermediatesize-function"></a>GetRequiredIntermediateSize fonction)

Retourne la taille requise d’une mémoire tampon à utiliser pour le téléchargement de données.

## <a name="syntax"></a>Syntaxe


```C++
UINT64 inline GetRequiredIntermediateSize(
  _In_ ID3D12Resource *pDestinationResource,
  _In_ UINT           FirstSubresource,
  _In_ UINT           NumSubresources
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDestinationResource* \[ dans\]
</dt> <dd>

Type : **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***

Pointeur vers l’interface [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) qui représente la ressource de destination.

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

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**

Taille de la mémoire tampon, en octets.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx12. h</dt> </dl>  |
| Bibliothèque<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions d’assistance pour D3D12](helper-functions-for-d3d12.md)
</dt> </dl>

 

