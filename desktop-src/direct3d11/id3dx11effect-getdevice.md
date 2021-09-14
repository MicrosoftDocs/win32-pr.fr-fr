---
title: Méthode ID3DX11Effect GetDevice (D3dx11effect. h)
description: Récupérez l’appareil qui a créé l’effet.
ms.assetid: efcc0358-9842-46eb-a521-ea220ec18735
keywords:
- Méthode GetDevice Direct3D 11
- Méthode GetDevice Direct3D 11, interface ID3DX11Effect
- Interface ID3DX11Effect Direct3D 11, méthode GetDevice
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetDevice
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25317740cade8a937aeeeac29f5a608bb4a43931
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126916688"
---
# <a name="id3dx11effectgetdevice-method"></a>ID3DX11Effect :: GetDevice, méthode

Récupérez l’appareil qui a créé l’effet.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetDevice(
   ID3D11Device **ppDevice
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppDevice* 
</dt> <dd>

Type : **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\*\***

Pointeur vers un [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device).

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.

## <a name="remarks"></a>Notes

Un effet est créé pour un appareil spécifique, en appelant une fonction telle que [**D3DX11CreateEffectFromMemory**](d3dx11createeffectfrommemory.md).

> [!Note]  
> Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets. Vous devez utiliser la source Effects 11 pour créer votre application Effects-type. Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Bibliothèque<br/> | <dl> <dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

 





