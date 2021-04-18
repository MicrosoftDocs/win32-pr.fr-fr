---
description: La \_ méthode obtenir KeyType récupère le type de clé.
ms.assetid: 902cbd46-529a-45d8-afa2-a8dd9439769a
title: 'IDxtKey :: get_KeyType, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_KeyType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7341815169549f24db55518e021b9e5096286a65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533023"
---
# <a name="idxtkeyget_keytype-method"></a>IDxtKey :: obtient la \_ méthode KeyType

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

La `get_KeyType` méthode récupère le type de clé.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_KeyType(
  [out, retval] int *pVal
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pval* \[ out, retval\]
</dt> <dd>

Reçoit l’une des valeurs d’énumération suivantes.



| Valeur             | Description                                           |
|-------------------|-------------------------------------------------------|
| DXTKEY \_ RGB       | Clé Chroma. (Clé sur la valeur RVB.)                       |
| DXTKEY \_ NONRED    | Clé Nonred. (Rend les zones bleues et vertes transparentes.) |
| \_luminance DXTKEY | Clé de luminance.                                        |
| DXTKEY \_ alpha     | Clé par valeur alpha.                                   |
| DXTKEY \_ teinte       | Clé par teinte.                                           |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IDxtKey**](idxtkey.md)
</dt> </dl>

 

 




