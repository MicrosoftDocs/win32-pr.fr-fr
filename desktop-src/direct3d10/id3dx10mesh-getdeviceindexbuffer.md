---
description: 'Accédez à la mémoire tampon d’index du maillage une fois qu’elle a été validée sur l’appareil avec ID3DX10Mesh :: CommitToDevice. Cela diffère de ID3DX10Mesh :: GetIndexBuffer, qui retourne la mémoire tampon d’index avant qu’elle ait été validée sur l’appareil.'
ms.assetid: 94d21f50-91b5-4f8d-ac73-7a851bba8685
title: 'ID3DX10Mesh :: GetDeviceIndexBuffer, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetDeviceIndexBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3ec3e65cfc4acb5a903bcf18d2f707d39127e975
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106537270"
---
# <a name="id3dx10meshgetdeviceindexbuffer-method"></a>ID3DX10Mesh :: GetDeviceIndexBuffer, méthode

Accédez à la mémoire tampon d’index du maillage une fois qu’elle a été validée sur l’appareil avec [**ID3DX10Mesh :: CommitToDevice**](id3dx10mesh-committodevice.md). Cela diffère de [**ID3DX10Mesh :: GetIndexBuffer**](id3dx10mesh-getindexbuffer.md), qui retourne la mémoire tampon d’index avant qu’elle ait été validée sur l’appareil.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetDeviceIndexBuffer(
  [out] ID3D10Buffer **ppIndexBuffer
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppIndexBuffer* \[ à\]
</dt> <dd>

Type : **[ **ID3D10Buffer**](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)\*\***

Mémoire tampon d’index une fois qu’elle a été validée sur l’appareil.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Notes

Si la mémoire tampon d’index du maillage n’a pas déjà été validée sur l’appareil, cette API valide automatiquement le tampon d’index avant de retourner un pointeur vers la mémoire tampon.

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

 

 




