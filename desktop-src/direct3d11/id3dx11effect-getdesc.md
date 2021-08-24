---
title: Méthode ID3DX11Effect GetDesc (D3dx11effect. h)
description: Obtient une description de l’effet.
ms.assetid: ca684786-c813-48d1-acad-e78aafd1c0db
keywords:
- Méthode GetDesc Direct3D 11
- Méthode GetDesc Direct3D 11, interface ID3DX11Effect
- Interface ID3DX11Effect Direct3D 11, méthode GetDesc
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9461dafb6b8da66ffa2a84e0d9d61c119a67c33bd967ae5183252e875fb6192
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676949"
---
# <a name="id3dx11effectgetdesc-method"></a>ID3DX11Effect :: GetDesc, méthode

Obtient une description de l’effet.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetDesc(
   D3DX11_EFFECT_DESC *pDesc
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDesc* 
</dt> <dd>

Type : **[ **D3DX11 \_ effet \_ desc**](d3dx11-effect-desc.md)\***

Pointeur vers une description d’effet (consultez [**D3DX11 \_ Effect \_ desc**](d3dx11-effect-desc.md)).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.

## <a name="remarks"></a>Remarques

Une description d’effet contient des informations de base sur un effet tel que les techniques qu’il contient et les ressources de mémoire tampon constantes dont il a besoin.

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

 

 





