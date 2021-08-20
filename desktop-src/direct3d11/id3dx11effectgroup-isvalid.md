---
title: ID3DX11EffectGroup IsValid, méthode (D3dx11effect. h)
description: Testez un effet pour voir s’il contient une syntaxe valide. | ID3DX11EffectGroup IsValid, méthode (D3dx11effect. h)
ms.assetid: 05829749-cef0-40ed-beab-556a65a1ac96
keywords:
- Méthode IsValid Direct3D 11
- Méthode IsValid Direct3D 11, interface ID3DX11EffectGroup
- Interface ID3DX11EffectGroup Direct3D 11, méthode IsValid
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup.IsValid
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab28c0658c45e4091233e75c6456a9446da46a5a6d4a045bf3a533d881b42ec6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046247"
---
# <a name="id3dx11effectgroupisvalid-method"></a>ID3DX11EffectGroup :: IsValid, méthode

Testez un effet pour voir s’il contient une syntaxe valide.

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

[ID3DX11EffectGroup](id3dx11effectgroup.md)
</dt> </dl>

 

