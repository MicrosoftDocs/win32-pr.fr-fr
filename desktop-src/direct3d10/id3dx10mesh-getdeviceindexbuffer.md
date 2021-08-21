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
ms.openlocfilehash: 869bd40b49801a1469ca08baa3a493cc23e6f6238624380411c8d91de829c79b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990369"
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

## <a name="remarks"></a>Remarques

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

 

 




