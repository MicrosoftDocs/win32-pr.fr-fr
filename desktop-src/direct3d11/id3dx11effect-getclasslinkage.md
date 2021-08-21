---
title: Méthode ID3DX11Effect GetClassLinkage (D3dx11effect. h)
description: Obtient une interface de liaison de classe.
ms.assetid: 006c900d-3464-4666-9fe9-d62ba8cb2b7f
keywords:
- Méthode GetClassLinkage Direct3D 11
- Méthode GetClassLinkage Direct3D 11, interface ID3DX11Effect
- Interface ID3DX11Effect Direct3D 11, méthode GetClassLinkage
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetClassLinkage
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17f4a34ad8ff2e53d521d4fd7a1510332dddf8ff7197eac17bf4231a26e98f4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632659"
---
# <a name="id3dx11effectgetclasslinkage-method"></a>ID3DX11Effect :: GetClassLinkage, méthode

Obtient une interface de liaison de classe.

## <a name="syntax"></a>Syntaxe


```C++
ID3D11ClassLinkage* GetClassLinkage();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **[ **ID3D11ClassLinkage**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage)\***

Retourne un pointeur vers une interface [**ID3D11ClassLinkage**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage) .

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

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

 





