---
title: Méthode ID3DX11EffectVectorVariable GetBoolVector (D3dx11effect. h)
description: Obtenir un vecteur à quatre composants qui contient des données booléennes.
ms.assetid: ecaf5705-d13b-4d61-9766-d2ff183af789
keywords:
- Méthode GetBoolVector Direct3D 11
- Méthode GetBoolVector Direct3D 11, interface ID3DX11EffectVectorVariable
- Interface ID3DX11EffectVectorVariable Direct3D 11, méthode GetBoolVector
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable.GetBoolVector
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a24563bd7c685579115e3b10309fb0a1c158c2e4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974646"
---
# <a name="id3dx11effectvectorvariablegetboolvector-method"></a>ID3DX11EffectVectorVariable :: GetBoolVector, méthode

Obtenir un vecteur à quatre composants qui contient des données booléennes.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetBoolVector(
   BOOL *pData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pData* 
</dt> <dd>

Type : **[ **bool**](/windows/desktop/WinProg/windows-data-types)\***

Pointeur vers le premier composant.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

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

[ID3DX11EffectVectorVariable](id3dx11effectvectorvariable.md)
</dt> </dl>

 

