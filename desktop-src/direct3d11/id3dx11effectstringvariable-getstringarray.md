---
title: Méthode ID3DX11EffectStringVariable GetStringArray (D3dx11effect. h)
description: Obtient un tableau de chaînes.
ms.assetid: 2cc45b2f-1851-49d2-8844-3e249c48f327
keywords:
- Méthode GetStringArray Direct3D 11
- Méthode GetStringArray Direct3D 11, interface ID3DX11EffectStringVariable
- Interface ID3DX11EffectStringVariable Direct3D 11, méthode GetStringArray
topic_type:
- apiref
api_name:
- ID3DX11EffectStringVariable.GetStringArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2050ebd7c9ae3735385a379e6ef7bdff0e1cfd6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416077"
---
# <a name="id3dx11effectstringvariablegetstringarray-method"></a>ID3DX11EffectStringVariable :: GetStringArray, méthode

Obtient un tableau de chaînes.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetStringArray(
   LPCSTR *ppStrings,
   UINT   Offset,
   UINT   Count
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppStrings* 
</dt> <dd>

Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)\***

Pointeur vers la première chaîne dans le tableau.

</dd> <dt>

*Offset* 
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Décalage (en nombre de chaînes) entre le début du tableau et la première chaîne à récupérer.

</dd> <dt>

*Count* 
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Nombre de chaînes dans le tableau retourné.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.

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

[ID3DX11EffectStringVariable](id3dx11effectstringvariable.md)
</dt> </dl>

 

