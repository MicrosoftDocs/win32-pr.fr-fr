---
title: Méthode ID3DX11Effect GetTechniqueByName (D3dx11effect. h)
description: Obtient une technique par nom. | Méthode ID3DX11Effect GetTechniqueByName (D3dx11effect. h)
ms.assetid: 0f7fa02c-dfbf-4971-86ad-3429f99f84e0
keywords:
- Méthode GetTechniqueByName Direct3D 11
- Méthode GetTechniqueByName Direct3D 11, interface ID3DX11Effect
- Interface ID3DX11Effect Direct3D 11, méthode GetTechniqueByName
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetTechniqueByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62822789746cc9eb120d5102de12f8bc8174fa010db1bbdfff62119685390cd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118808122"
---
# <a name="id3dx11effectgettechniquebyname-method"></a>ID3DX11Effect :: GetTechniqueByName, méthode

Obtient une technique par nom.

## <a name="syntax"></a>Syntaxe


```C++
ID3DX11EffectTechnique* GetTechniqueByName(
   LPCSTR Name
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Nom* 
</dt> <dd>

Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Nom de la technique.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***

Pointeur vers un [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md). Si une technique portant le nom approprié est introuvable, une technique non valide est retournée. [**ID3DX11EffectTechnique :: IsValid**](id3dx11effecttechnique-isvalid.md) doit être appelé sur la technique retournée pour déterminer s’il est valide.

## <a name="remarks"></a>Remarques

Un effet contient une ou plusieurs techniques ; chaque technique contient une ou plusieurs passes. Vous pouvez accéder à une technique à l’aide de son nom ou d’un index.

> [!Note]  
> Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets. Vous devez utiliser la source Effects 11 pour créer votre application Effects-type. Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Bibliothèque<br/> | <dl> <dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

