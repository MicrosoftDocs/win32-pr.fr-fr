---
title: Méthode ID3DX11EffectGroup GetTechniqueByIndex (D3dx11effect. h)
description: Obtient une technique par index. | Méthode ID3DX11EffectGroup GetTechniqueByIndex (D3dx11effect. h)
ms.assetid: b0962957-20d1-4ec6-9f8e-acc7a62c5f4e
keywords:
- Méthode GetTechniqueByIndex Direct3D 11
- Méthode GetTechniqueByIndex Direct3D 11, interface ID3DX11EffectGroup
- Interface ID3DX11EffectGroup Direct3D 11, méthode GetTechniqueByIndex
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup.GetTechniqueByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 654b090b3481a915557569e0801e75b8ad089c66cfca4a893d6f865345088171
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046287"
---
# <a name="id3dx11effectgroupgettechniquebyindex-method"></a>ID3DX11EffectGroup :: GetTechniqueByIndex, méthode

Obtient une technique par index.

## <a name="syntax"></a>Syntaxe


```C++
ID3DX11EffectTechnique* GetTechniqueByIndex(
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

Type : **[ **ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***

Pointeur vers un [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md).

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

 

