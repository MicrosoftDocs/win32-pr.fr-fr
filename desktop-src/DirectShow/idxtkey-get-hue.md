---
description: La \_ méthode obtenir la teinte récupère la valeur de teinte sur laquelle la clé doit être ajoutée. Cette propriété s’applique uniquement lorsque le type de clé est DXTKEY \_ teinte.
ms.assetid: d37fedd6-f29f-4f16-821b-c5f8520c4e12
title: 'IDxtKey :: get_Hue, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_Hue
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a003dc0cba632e354a0188571f87266902ce1396adcabb862aee258e5701f2cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997479"
---
# <a name="idxtkeyget_hue-method"></a>IDxtKey :: obtient la \_ méthode Hue

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `get_Hue` méthode récupère la valeur de teinte sur laquelle la clé doit être ajoutée. Cette propriété s’applique uniquement lorsque le type de clé est DXTKEY \_ teinte.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Hue(
  [out, retval] int *pVal
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pval* \[ out, retval\]
</dt> <dd>

Reçoit la valeur de teinte sur laquelle la clé doit être ajoutée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> pour obtenir Qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Configuration requise



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

 

 




