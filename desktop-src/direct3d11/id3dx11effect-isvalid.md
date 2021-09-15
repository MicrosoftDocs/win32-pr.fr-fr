---
title: ID3DX11Effect IsValid, méthode (D3dx11effect. h)
description: Testez un effet pour voir s’il contient une syntaxe valide. | ID3DX11Effect IsValid, méthode (D3dx11effect. h)
ms.assetid: 42bf0069-1828-4f55-99f5-d0f81eb04336
keywords:
- Méthode IsValid Direct3D 11
- Méthode IsValid Direct3D 11, interface ID3DX11Effect
- Interface ID3DX11Effect Direct3D 11, méthode IsValid
topic_type:
- apiref
api_name:
- ID3DX11Effect.IsValid
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea88aef9e3864fc77380b3459860178c8537a6a5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403877"
---
# <a name="id3dx11effectisvalid-method"></a>ID3DX11Effect :: IsValid, méthode

Testez un effet pour voir s’il contient une syntaxe valide.

## <a name="syntax"></a>Syntaxe


```C++
BOOL IsValid();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Type : **[ **bool**](/windows/desktop/WinProg/windows-data-types)**

**True** si la syntaxe du code est valide ; Sinon, **false**.

## <a name="remarks"></a>Notes

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

 

