---
description: 'Supprime les données de maillage de l’appareil qui a été validé sur l’appareil (avec ID3DX10Mesh :: CommitToDevice).'
ms.assetid: 60eee1f8-f04b-4f33-8f86-0564d0334f97
title: ID3DX10Mesh ::D méthode iscard (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.Discard
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f861de8eefff603954e896a1b6684afc8806764f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106537256"
---
# <a name="id3dx10meshdiscard-method"></a>ID3DX10Mesh ::D méthode iscard

Supprime les données de maillage de l’appareil qui a été validé sur l’appareil (avec [**ID3DX10Mesh :: CommitToDevice**](id3dx10mesh-committodevice.md)).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Discard(
  [in] D3DX10_MESH_DISCARD_FLAGS dwDiscard
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwDiscard* \[ dans\]
</dt> <dd>

Type : **[ **d3dx10 \_ Mesh \_ ignore \_ Flags**](d3dx10-mesh-discard-flags.md)**

Spécifie les éléments de données de maillage à ignorer de l’appareil. Consultez [**\_ indicateurs d3dx10 \_ Mesh \_ ignore**](d3dx10-mesh-discard-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




