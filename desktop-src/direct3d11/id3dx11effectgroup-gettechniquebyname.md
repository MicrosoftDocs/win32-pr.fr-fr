---
title: Méthode ID3DX11EffectGroup GetTechniqueByName (D3dx11effect. h)
description: Obtient une technique par nom. | Méthode ID3DX11EffectGroup GetTechniqueByName (D3dx11effect. h)
ms.assetid: 160c6d57-bec4-4718-8fad-fc9c0746736c
keywords:
- Méthode GetTechniqueByName Direct3D 11
- Méthode GetTechniqueByName Direct3D 11, interface ID3DX11EffectGroup
- Interface ID3DX11EffectGroup Direct3D 11, méthode GetTechniqueByName
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup.GetTechniqueByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5121f67345ba863d773d8e7a73a5d6fa8b69895
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974571"
---
# <a name="id3dx11effectgroupgettechniquebyname-method"></a>ID3DX11EffectGroup :: GetTechniqueByName, méthode

Obtient une technique par nom.

## <a name="syntax"></a>Syntaxe


```C++
ID3DX11EffectTechnique* GetTechniqueByName(
   LPCSTR Name
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Nom* 
</dt> <dd>

Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Nom de la technique.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***

Pointeur vers un [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md), ou **null** si la technique est introuvable.

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

[ID3DX11EffectGroup](id3dx11effectgroup.md)
</dt> </dl>

 

