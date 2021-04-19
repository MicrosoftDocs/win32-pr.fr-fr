---
description: 'Accédez à la mémoire tampon de vertex du maillage une fois qu’elle a été validée sur l’appareil avec ID3DX10Mesh :: CommitToDevice. Cela diffère de ID3DX10Mesh :: GetVertexBuffer, qui retourne la mémoire tampon de vertex avant qu’elle n’ait été validée sur l’appareil.'
ms.assetid: 621d9105-e55d-47b8-8557-8adb7db19d66
title: 'ID3DX10Mesh :: GetDeviceVertexBuffer, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetDeviceVertexBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9943050d174acb4e8f8e676f56a95cfdcde88f5a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106545298"
---
# <a name="id3dx10meshgetdevicevertexbuffer-method"></a>ID3DX10Mesh :: GetDeviceVertexBuffer, méthode

Accédez à la mémoire tampon de vertex du maillage une fois qu’elle a été validée sur l’appareil avec [**ID3DX10Mesh :: CommitToDevice**](id3dx10mesh-committodevice.md). Cela diffère de [**ID3DX10Mesh :: GetVertexBuffer**](id3dx10mesh-getvertexbuffer.md), qui retourne la mémoire tampon de vertex avant qu’elle n’ait été validée sur l’appareil.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetDeviceVertexBuffer(
  [in]  UINT         iBuffer,
  [out] ID3D10Buffer **ppVertexBuffer
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*iBuffer* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Index identifiant la mémoire tampon de vertex à laquelle accéder.

</dd> <dt>

*ppVertexBuffer* \[ à\]
</dt> <dd>

Type : **[ **ID3D10Buffer**](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)\*\***

Mémoire tampon de vertex une fois qu’elle a été validée sur l’appareil.

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

 

 
