---
title: D3DX12SerializeVersionedRootSignature, fonction (D3dx12. h)
description: Permet d’activer les fonctionnalités de signature racine 1,1 lorsqu’elles sont disponibles et ne nécessite pas la gestion de deux chemins de code pour générer des signatures racines. Cette méthode d’assistance reconstruit une signature racine version 1,0 quand la version 1,1 n’est pas prise en charge.
ms.assetid: 0F6BA6C1-9A33-4E99-BF34-4A0358E7427D
keywords:
- D3DX12SerializeVersionedRootSignature fonction)
topic_type:
- apiref
api_name:
- D3DX12SerializeVersionedRootSignature
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70a9d0424f7f7a7f89edde18273c5d1fa22fae28
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106520306"
---
# <a name="d3dx12serializeversionedrootsignature-function"></a>D3DX12SerializeVersionedRootSignature fonction)

Permet d’activer les fonctionnalités de signature racine 1,1 lorsqu’elles sont disponibles et ne nécessite pas la gestion de deux chemins de code pour générer des signatures racines. Cette méthode d’assistance reconstruit une signature racine version 1,0 quand la version 1,1 n’est pas prise en charge.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT inline D3DX12SerializeVersionedRootSignature(
  _In_      const D3D12_VERSIONED_ROOT_SIGNATURE_DESC *pRootSignatureDesc,
                  D3D_ROOT_SIGNATURE_VERSION          MaxVersion,
  _Out_           ID3DBlob                            **ppBlob,
  _Out_opt_       ID3DBlob                            **ppErrorBlob
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pRootSignatureDesc* \[ dans\]
</dt> <dd>

Type : **const D3D12 \_ version de la racine avec version gérée \_ \_ \_ desc \***

Spécifie une description de la [**\_ \_ \_ signature \_ racine avec version D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) qui contient une description de toute version d’une signature racine.

</dd> <dt>

*MaxVersion* 
</dt> <dd>

Type : **\_ version de \_ signature \_ racine D3D**

Spécifie la version maximale prise en charge de la signature de la [**\_ racine \_ \_ D3D**](/windows/desktop/api/d3d12/ne-d3d12-d3d_root_signature_version).

</dd> <dt>

*ppBlob* \[ à\]
</dt> <dd>

Type : **ID3DBlob \* \***

Pointeur vers un bloc de mémoire qui reçoit un pointeur vers l’interface [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) que vous pouvez utiliser pour accéder à la signature racine sérialisée.

</dd> <dt>

*ppErrorBlob* \[ out, facultatif\]
</dt> <dd>

Type : **ID3DBlob \* \***

Pointeur vers un bloc de mémoire qui reçoit un pointeur vers l’interface [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) que vous pouvez utiliser pour accéder aux messages d’erreur du sérialiseur, ou **null** s’il n’y a aucune erreur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Retourne **S \_ OK** en cas de réussite ; sinon, retourne l’un des [codes de retour Direct3D 12](d3d12-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Notes

Cette fonction a été publiée pour coïncider avec la mise à jour anniversaire de Windows 10 (14393). Pour prendre en charge les versions de Windows 10 antérieures à cela, l’utilisation de cette fonction requiert que d3d12. lib soit configuré pour le *chargement différé*.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx12. h</dt> </dl>  |
| Bibliothèque<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**D3D12SerializeVersionedRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializeversionedrootsignature)
</dt> <dt>

[Fonctions d’assistance pour D3D12](helper-functions-for-d3d12.md)
</dt> </dl>

 

