---
title: Méthode ID3DX11EffectVectorVariable SetFloatVector (D3dx11effect. h)
description: Définissez un vecteur à quatre composants qui contient des données à virgule flottante.
ms.assetid: fb646df6-b9f9-4d71-93c3-38833076b781
keywords:
- Méthode SetFloatVector Direct3D 11
- Méthode SetFloatVector Direct3D 11, interface ID3DX11EffectVectorVariable
- Interface ID3DX11EffectVectorVariable Direct3D 11, méthode SetFloatVector
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable.SetFloatVector
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5541f2773e992c4c52bf748bceb832d67b28825
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008064"
---
# <a name="id3dx11effectvectorvariablesetfloatvector-method"></a>ID3DX11EffectVectorVariable :: SetFloatVector, méthode

Définissez un vecteur à quatre composants qui contient des données à virgule flottante.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetFloatVector(
   float *pData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pData* 
</dt> <dd>

Type : **float \***

Pointeur vers le premier composant.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.

## <a name="remarks"></a>Notes

> [!Note]  
> Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets. Vous devez utiliser la source Effects 11 pour créer votre application Effects-type. Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Bibliothèque<br/> | <dl> <dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DX11EffectVectorVariable](id3dx11effectvectorvariable.md)
</dt> </dl>

 

 





