---
description: Obtient un pointeur vers la mémoire tampon de maillage pour modifier son contenu.
ms.assetid: d15ed47a-450e-404a-bcc2-a641abc2d02e
title: 'ID3DX10MeshBuffer :: Map, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10MeshBuffer.Map
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1b8cb03e128a6673963ce2d3cde993babb03da5c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322954"
---
# <a name="id3dx10meshbuffermap-method"></a>ID3DX10MeshBuffer :: Map, méthode

Obtient un pointeur vers la mémoire tampon de maillage pour modifier son contenu.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Map(
  [out] void   **ppData,
  [out] SIZE_T *pSize
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppData* \[ à\]
</dt> <dd>

Type : **void \* \***

Pointeur vers les données de la mémoire tampon.

</dd> <dt>

*psize* \[ à\]
</dt> <dd>

Type : **[ **taille \_ T**](../winprog/windows-data-types.md)\***

Taille, en octets, de la mémoire tampon.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Notes



|                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------|
| Différences entre Direct3D 9 et Direct3D 10 :<br/> Map () dans Direct3D 10 est analogue à la carte de ressources () dans Direct3D 9.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DX10MeshBuffer](id3dx10meshbuffer.md)
</dt> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
