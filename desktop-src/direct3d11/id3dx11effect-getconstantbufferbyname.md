---
title: Méthode ID3DX11Effect GetConstantBufferByName (D3dx11effect. h)
description: Obtient une mémoire tampon constante par nom.
ms.assetid: 11757615-4068-430d-9ab0-f83f02af8e55
keywords:
- Méthode GetConstantBufferByName Direct3D 11
- Méthode GetConstantBufferByName Direct3D 11, interface ID3DX11Effect
- Interface ID3DX11Effect Direct3D 11, méthode GetConstantBufferByName
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetConstantBufferByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa01d20bfeebfa3f689a58aae5c5face8b879e3c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008081"
---
# <a name="id3dx11effectgetconstantbufferbyname-method"></a>ID3DX11Effect :: GetConstantBufferByName, méthode

Obtient une mémoire tampon constante par nom.

## <a name="syntax"></a>Syntaxe


```C++
ID3DX11EffectConstantBuffer* GetConstantBufferByName(
   LPCSTR Name
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Nom* 
</dt> <dd>

Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Nom de la mémoire tampon constante.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***

Pointeur vers la mémoire tampon constante indiquée par le nom. Consultez [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).

## <a name="remarks"></a>Notes

Un effet qui contient une variable qui sera lue/écrite par une application nécessite au moins une mémoire tampon constante. Pour des performances optimales, un effet doit organiser des variables en une ou plusieurs mémoires tampons constantes en fonction de leur fréquence de mise à jour.

> [!Note]  
> Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets. Vous devez utiliser la source Effects 11 pour créer votre application Effects-type. Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Bibliothèque<br/> | <dl> <dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

