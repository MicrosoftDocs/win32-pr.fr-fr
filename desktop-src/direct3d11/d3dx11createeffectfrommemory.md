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
ms.openlocfilehash: 467d2094a7124b96a08c7bab6d7a4209deee9996
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127517112"
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

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Notes

> [!Note]  
> Vous devez utiliser la [source Effects 11](https://github.com/Microsoft/FX11) pour créer votre application Effects-type. Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Effets 11 fonctions](d3d11-graphics-reference-effects11-functions.md)
</dt> </dl>

 

