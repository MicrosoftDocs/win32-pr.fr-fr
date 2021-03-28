---
title: Méthode ID3DX11EffectPass GetAnnotationByName (D3dx11effect. h)
description: Obtient une annotation par nom. | Méthode ID3DX11EffectPass GetAnnotationByName (D3dx11effect. h)
ms.assetid: b54a4fb0-62c7-4d96-af30-f9ae04ff7dab
keywords:
- Méthode GetAnnotationByName Direct3D 11
- Méthode GetAnnotationByName Direct3D 11, interface ID3DX11EffectPass
- Interface ID3DX11EffectPass Direct3D 11, méthode GetAnnotationByName
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetAnnotationByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d129f1548e7f63c47906ac736cbddb5f6b2548b2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953936"
---
# <a name="id3dx11effectpassgetannotationbyname-method"></a>ID3DX11EffectPass :: GetAnnotationByName, méthode

Obtient une annotation par nom.

## <a name="syntax"></a>Syntaxe


```C++
ID3DX11EffectVariable* GetAnnotationByName(
   LPCSTR Name
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Nom* 
</dt> <dd>

Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Nom de l’annotation.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***

Pointeur vers un [**ID3DX11EffectVariable**](id3dx11effectvariable.md).

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

[ID3DX11EffectPass](id3dx11effectpass.md)
</dt> </dl>

 

