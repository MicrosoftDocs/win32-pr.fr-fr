---
title: D3DX11CreateEffectFromMemory, fonction (D3dx11effect. h)
description: Crée un effet à partir d’un fichier ou d’un effet binaire.
ms.assetid: 4aa65efb-4c6b-4faf-b48f-01329bdff6cd
keywords:
- Fonction D3DX11CreateEffectFromMemory Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateEffectFromMemory
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c99cdef28acae9419a5b597d5be1703ea9e866d521d7f94bb330b151abc74842
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124804"
---
# <a name="d3dx11createeffectfrommemory-function"></a>D3DX11CreateEffectFromMemory fonction)

Crée un effet à partir d’un fichier ou d’un effet binaire.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DX11CreateEffectFromMemory(
   void          *pData,
   SIZE_T        DataLength,
   UINT          FXFlags,
   ID3D11Device  *pDevice,
   ID3DX11Effect **ppEffect
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pData* 
</dt> <dd>

Type : **void \***

Objet blob de données d’effet compilé.

</dd> <dt>

*DataLength* 
</dt> <dd>

Type : **[ **taille \_ T**](/windows/desktop/WinProg/windows-data-types)**

Longueur de l’objet blob de données.

</dd> <dt>

*FXFlags* 
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Il n’existe aucun indicateur d’effet. Définit la valeur zéro.

</dd> <dt>

*pDevice* 
</dt> <dd>

Type : **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***

Pointeur vers le [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) sur lequel créer des ressources d’effet.

</dd> <dt>

*ppEffect* 
</dt> <dd>

Type : **[ **ID3DX11Effect**](id3dx11effect.md)\*\***

Adresse de l’interface [**ID3DX11Effect**](id3dx11effect.md) nouvellement créée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Remarques

> [!Note]  
> Vous devez utiliser la [source Effects 11](https://github.com/Microsoft/FX11) pour créer votre application Effects-type. Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Effets 11 fonctions](d3d11-graphics-reference-effects11-functions.md)
</dt> </dl>

 

