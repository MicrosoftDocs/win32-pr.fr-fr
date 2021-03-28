---
title: Méthode ID3DX11EffectVectorVariable GetIntVector (D3dx11effect. h)
description: Obtient un vecteur à quatre composants qui contient des données de type entier.
ms.assetid: 27c75cfb-7c6f-43f4-9489-186006a60203
keywords:
- Méthode GetIntVector Direct3D 11
- Méthode GetIntVector Direct3D 11, interface ID3DX11EffectVectorVariable
- Interface ID3DX11EffectVectorVariable Direct3D 11, méthode GetIntVector
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable.GetIntVector
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e661ecce642cae4cf94a1bc35f92dc1afad16a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104531011"
---
# <a name="id3dx11effectvectorvariablegetintvector-method"></a>ID3DX11EffectVectorVariable :: GetIntVector, méthode

Obtient un vecteur à quatre composants qui contient des données de type entier.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetIntVector(
   int *pData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pData* 
</dt> <dd>

Type : **[ **int**](/windows/desktop/WinProg/windows-data-types)\***

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

 

