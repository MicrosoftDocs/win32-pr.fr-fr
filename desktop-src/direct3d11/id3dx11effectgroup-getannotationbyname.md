---
title: Méthode ID3DX11EffectGroup GetAnnotationByName (D3dx11effect. h)
description: Obtient une annotation par nom. | Méthode ID3DX11EffectGroup GetAnnotationByName (D3dx11effect. h)
ms.assetid: c526a249-fb56-47bb-a0c2-b829a1da88e8
keywords:
- Méthode GetAnnotationByName Direct3D 11
- Méthode GetAnnotationByName Direct3D 11, interface ID3DX11EffectGroup
- Interface ID3DX11EffectGroup Direct3D 11, méthode GetAnnotationByName
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup.GetAnnotationByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07d80c0d59a1fd0a58c756d72f6215f13b4e3391e44828aa8e1bcff23063292e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118535737"
---
# <a name="id3dx11effectgroupgetannotationbyname-method"></a>ID3DX11EffectGroup :: GetAnnotationByName, méthode

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

Pointeur vers un [**ID3DX11EffectVariable**](id3dx11effectvariable.md). Notez que si l’annotation est introuvable, le **ID3DX11EffectVariable** retourné est vide. La méthode [**ID3DX11EffectVariable :: IsValid**](id3dx11effectvariable-isvalid.md) doit être appelée pour déterminer si l’annotation a été trouvée.

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

 

