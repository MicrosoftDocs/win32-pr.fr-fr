---
title: MemcpySubresource, fonction (D3dx12. h)
description: Copie une sous-ressource ligne par ligne.
ms.assetid: 33A9F99D-FD85-4FD6-AFD6-7A10F16C3D9B
keywords:
- MemcpySubresource fonction)
topic_type:
- apiref
api_name:
- MemcpySubresource
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c27e8cf9ffda237c2dad017b3a981ff71498a22c1c7b54ede032d6bf8c012a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117733361"
---
# <a name="memcpysubresource-function"></a>MemcpySubresource fonction)

Copie une sous-ressource ligne par ligne.

## <a name="syntax"></a>Syntaxe


```C++
void inline MemcpySubresource(
  _In_ const D3D12_MEMCPY_DEST      *pDest,
  _In_ const D3D12_SUBRESOURCE_DATA *pSrc,
             SIZE_T                 RowSizeInBytes,
             UINT                   NumRows,
             UINT                   NumSlices
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDEST* \[ dans\]
</dt> <dd>

Type : **const [**D3D12 \_ MEMCPY \_ dest**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_memcpy_dest) \***

Pointeur vers une structure [**de \_ \_ dest D3D12 MEMCPY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_memcpy_dest) qui décrit la destination de l’opération de copie de mémoire.

</dd> <dt>

*pSrc* \[ dans\]
</dt> <dd>

Type : **const [**D3D12 les \_ \_ données**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) \*** de sous-ressource

Pointeur vers une structure [**de \_ \_ données**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) de sous-ressource D3D12 qui décrit la source de l’opération de copie de mémoire.

</dd> <dt>

*RowSizeInBytes* 
</dt> <dd>

Type : **[ **taille \_ T**](/windows/desktop/WinProg/windows-data-types)**

Taille, en octets, de chaque ligne.

</dd> <dt>

*NumRows* 
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Nombre de lignes.

</dd> <dt>

*NumSlices* 
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Nombre de secteurs.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Prenez également en compte les méthodes suivantes :

-   [**ID3D12Resource::WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource)
-   [**ID3D12Resource::ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource)
-   [**ID3D12GraphicsCommandList::CopyResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)

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

 

