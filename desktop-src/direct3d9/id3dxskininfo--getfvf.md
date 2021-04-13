---
description: Obtient la valeur de vertex de fonction fixe.
ms.assetid: 9b80c4b9-2e5b-4965-99b9-ad6c459ef413
title: 'ID3DXSkinInfo :: GetFVF, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetFVF
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6d48cd9cea6efd6cb43e6da6877a7aaf42909c71
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322605"
---
# <a name="id3dxskininfogetfvf-method"></a>ID3DXSkinInfo :: GetFVF, méthode

Obtient la valeur de vertex de fonction fixe.

## <a name="syntax"></a>Syntaxe


```C++
DWORD GetFVF();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Retourne les codes de format de vertex flexible.

## <a name="remarks"></a>Notes

Cette méthode peut retourner 0 si le format du vertex ne peut pas être mappé directement à un code de la Commission. Cela se produit pour un maillage créé à partir d’une déclaration de vertex qui n’a pas le même ordre et les mêmes éléments que ceux pris en charge par les codes de la Commission.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo::SetFVF**](id3dxskininfo--setfvf.md)
</dt> </dl>

 

 
