---
title: ID3DX11EffectPass IsValid, méthode (D3dx11effect. h)
description: Testez un passage pour voir s’il contient une syntaxe valide.
ms.assetid: 3c6ddcef-1303-4161-889c-c3ca271b6ad0
keywords:
- Méthode IsValid Direct3D 11
- Méthode IsValid Direct3D 11, interface ID3DX11EffectPass
- Interface ID3DX11EffectPass Direct3D 11, méthode IsValid
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.IsValid
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c4d184f1912e3518c63e3e1720c0438acee9c84eba52b7a3a6717bbb2d9e091
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118534945"
---
# <a name="id3dx11effectpassisvalid-method"></a>ID3DX11EffectPass :: IsValid, méthode

Testez un passage pour voir s’il contient une syntaxe valide.

## <a name="syntax"></a>Syntaxe


```C++
BOOL IsValid();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **[ **bool**](/windows/desktop/WinProg/windows-data-types)**

**True** si la syntaxe du code est valide ; Sinon, **false**.

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

[ID3DX11EffectPass](id3dx11effectpass.md)
</dt> </dl>

 

