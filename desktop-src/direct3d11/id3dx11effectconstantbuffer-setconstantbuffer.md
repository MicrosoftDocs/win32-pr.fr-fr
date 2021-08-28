---
title: Méthode ID3DX11EffectConstantBuffer SetConstantBuffer (D3dx11effect. h)
description: Définissez une mémoire tampon constante.
ms.assetid: 288e029a-e69a-4f58-be3f-8f9900c0e1dd
keywords:
- Méthode SetConstantBuffer Direct3D 11
- Méthode SetConstantBuffer Direct3D 11, interface ID3DX11EffectConstantBuffer
- Interface ID3DX11EffectConstantBuffer Direct3D 11, méthode SetConstantBuffer
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer.SetConstantBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16519067857d89fb7b28c9fd74af8de5e12029d71ac0d60763692bdd45e27138
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046407"
---
# <a name="id3dx11effectconstantbuffersetconstantbuffer-method"></a>ID3DX11EffectConstantBuffer :: SetConstantBuffer, méthode

Définissez une mémoire tampon constante.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetConstantBuffer(
   ID3D11Buffer *pConstantBuffer
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pConstantBuffer* 
</dt> <dd>

Type : **[ **ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)\***

Pointeur vers une interface de mémoire tampon constante. Consultez [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.

## <a name="remarks"></a>Remarques

> [!Note]  
> Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets. Vous devez utiliser la source Effects 11 pour créer votre application Effects-type. Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Bibliothèque<br/> | <dl> <dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DX11EffectConstantBuffer](id3dx11effectconstantbuffer.md)
</dt> </dl>

 

 





