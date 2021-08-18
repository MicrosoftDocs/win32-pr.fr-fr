---
title: Méthode ID3DX11EffectVariable GetRawValue (D3dx11effect. h)
description: obtenir des données
ms.assetid: 1b2a319c-880c-4f5a-b4e9-17405351b7d9
keywords:
- Méthode GetRawValue Direct3D 11
- Méthode GetRawValue Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, méthode GetRawValue
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetRawValue
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2a2f0f79f231eab37c46eba138b72b0678e9ea323c86b736a55682bb7b771cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117734102"
---
# <a name="id3dx11effectvariablegetrawvalue-method"></a>ID3DX11EffectVariable :: GetRawValue, méthode

obtenir des données

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetRawValue(
   void *pData,
   UINT Offset,
   UINT Count
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pData* 
</dt> <dd>

Type : **void \***

Pointeur vers la variable.

</dd> <dt>

*Offset* 
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Décalage (en octets) entre le début du pointeur et les données.

</dd> <dt>

*Count* 
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Nombre d’octets à récupérer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.

## <a name="remarks"></a>Remarques

Cette méthode n’effectue aucune conversion ou vérification de type ; C’est pourquoi il s’agit d’un moyen très rapide d’accéder à des éléments de tableau.

> [!Note]  
> Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets. Vous devez utiliser la source Effects 11 pour créer votre application Effects-type. Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Bibliothèque<br/> | <dl> <dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DX11EffectVariable](id3dx11effectvariable.md)
</dt> </dl>

 

