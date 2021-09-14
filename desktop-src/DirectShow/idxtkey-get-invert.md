---
description: La \_ méthode obtenir une inversion récupère une valeur booléenne indiquant si l’opération de clé est inversée. Cette propriété s’applique à tous les types de clés, à l’exception de DXTKEY \_ alpha.
ms.assetid: 2ccf2066-3d9c-493b-bc54-a03e7d075531
title: 'IDxtKey :: get_Invert, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_Invert
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 51b95758adf6690f6d4fa479ac1cc2c585fa9352
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127296695"
---
# <a name="idxtkeyget_invert-method"></a>IDxtKey :: obtient la \_ méthode inversée

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `get_Invert` méthode récupère une valeur booléenne indiquant si l’opération de clé est inversée. Cette propriété s’applique à tous les types de clés, à l’exception de DXTKEY \_ alpha.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Invert(
  [out, retval] BOOL *pVal
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pval* \[ out, retval\]
</dt> <dd>

Reçoit l’une des valeurs suivantes.



| Valeur     | Description                                                                       |
|-----------|-----------------------------------------------------------------------------------|
| **TRUE**  | Les pixels de l’image superposée sont inversés par rapport à l’opération par défaut. |
| **FALSE** | Les pixels de l’image superposée sont rendus transparents par défaut.         |



 

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> pour obtenir Qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IDxtKey**](idxtkey.md)
</dt> <dt>

[**IDxtKey :: obtient \_ KeyType**](idxtkey-get-keytype.md)
</dt> </dl>

 

 




