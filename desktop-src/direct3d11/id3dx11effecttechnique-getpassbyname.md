---
title: Méthode ID3DX11EffectTechnique GetPassByName (D3dx11effect. h)
description: Obtenir un passage par nom.
ms.assetid: 07c7502e-2af9-4898-8cd4-106d6814fb85
keywords:
- Méthode GetPassByName Direct3D 11
- Méthode GetPassByName Direct3D 11, interface ID3DX11EffectTechnique
- Interface ID3DX11EffectTechnique Direct3D 11, méthode GetPassByName
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.GetPassByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfad489fe6c4eda8ea417a9f272bcc0a7d4035eb04bc675cf599e4f5381234db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118532361"
---
# <a name="id3dx11effecttechniquegetpassbyname-method"></a>ID3DX11EffectTechnique :: GetPassByName, méthode

Obtenir un passage par nom.

## <a name="syntax"></a>Syntaxe


```C++
ID3DX11EffectPass* GetPassByName(
   LPCSTR Name
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Nom* 
</dt> <dd>

Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Nom de la passe.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **ID3DX11EffectPass**](id3dx11effectpass.md)\***

Pointeur vers un [**ID3DX11EffectPass**](id3dx11effectpass.md).

## <a name="remarks"></a>Remarques

Une technique contient une ou plusieurs passes ; obtenir une passe à l’aide d’un nom ou d’un index.

> [!Note]  
> Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets. Vous devez utiliser la source Effects 11 pour créer votre application Effects-type. Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Bibliothèque<br/> | <dl> <dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DX11EffectTechnique](id3dx11effecttechnique.md)
</dt> </dl>

 

