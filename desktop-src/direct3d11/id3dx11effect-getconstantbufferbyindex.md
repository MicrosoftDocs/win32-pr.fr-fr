---
title: Méthode ID3DX11Effect GetConstantBufferByIndex (D3dx11effect. h)
description: Obtient une mémoire tampon constante par index.
ms.assetid: 146b146b-89ff-4d56-9ac7-e67a92a30e26
keywords:
- Méthode GetConstantBufferByIndex Direct3D 11
- Méthode GetConstantBufferByIndex Direct3D 11, interface ID3DX11Effect
- Interface ID3DX11Effect Direct3D 11, méthode GetConstantBufferByIndex
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetConstantBufferByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d2ce34bb6bde85600e57182151e8c270885e60f919f22a723228b14dd17927a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632599"
---
# <a name="id3dx11effectgetconstantbufferbyindex-method"></a>ID3DX11Effect :: GetConstantBufferByIndex, méthode

Obtient une mémoire tampon constante par index.

## <a name="syntax"></a>Syntaxe


```C++
ID3DX11EffectConstantBuffer* GetConstantBufferByIndex(
   UINT Index
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Index* 
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Index de base zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***

Pointeur vers un [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).

## <a name="remarks"></a>Remarques

Un effet qui contient une variable qui sera lue/écrite par une application nécessite au moins une mémoire tampon constante. Pour des performances optimales, un effet doit organiser des variables en une ou plusieurs mémoires tampons constantes en fonction de leur fréquence de mise à jour.

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

 

