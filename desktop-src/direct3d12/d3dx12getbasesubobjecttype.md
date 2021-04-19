---
title: D3DX12GetBaseSubobjectType, fonction (D3dx12. h)
description: Retourne le type de sous-objet qui correspond à la classe de base du type de sous-objet passé.
ms.assetid: 3744B042-094C-4EA4-8185-A018B728D843
keywords:
- D3DX12GetBaseSubobjectType fonction)
topic_type:
- apiref
api_name:
- D3DX12GetBaseSubobjectType
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b39f1c61be682d55512772bef1258aecdb009a5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106532421"
---
# <a name="d3dx12getbasesubobjecttype-function"></a>D3DX12GetBaseSubobjectType fonction)

Retourne le type de sous-objet qui correspond à la classe de base du type de sous-objet passé.

## <a name="syntax"></a>Syntaxe


```C++
D3D12_PIPELINE_STATE_SUBOBJECT_TYPE inline D3DX12GetBaseSubobjectType(
   D3D12_PIPELINE_STATE_SUBOBJECT_TYPE SubobjectType
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*SubobjectType* 
</dt> <dd>

Type : **\_ type de \_ \_ \_ sous-objet état du pipeline D3D12**

Valeur d’énumération qui spécifie le type de sous-objet qui vous intéresse.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **\_ type de \_ \_ \_ sous-objet état du pipeline D3D12**

Si *SubobjectType* correspond à un type de données de sous-objet dérivé d’un autre type de données de sous-objet, le type de sous-objet du type de données de sous-objet de base est retourné ; dans le cas contraire, le type de sous-objet passé est retourné. Par exemple, si la profondeur de type de sous-objet de l' **État du \_ pipeline D3D12 \_ \_ \_ \_ \_ STENCIL1** est passée, le stencil de profondeur du type de sous-objet de l' **\_ État du pipeline \_ \_ \_ \_ \_ D3D12** est retourné.

## <a name="remarks"></a>Notes

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx12. h</dt> </dl>  |
| Bibliothèque<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions d’assistance pour D3D12](helper-functions-for-d3d12.md)
</dt> </dl>

 

 





