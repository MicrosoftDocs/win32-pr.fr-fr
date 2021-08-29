---
description: La \_ méthode obtenir la luminance récupère la valeur de luminance sur laquelle la clé doit être ajoutée. Cette propriété s’applique uniquement lorsque le type de clé est DXTKEY \_ luminance.
ms.assetid: 92113331-a7b7-4618-81b2-ea02e7bcc923
title: 'IDxtKey :: get_Luminance, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_Luminance
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4035662f8510fd7caab6b2c540bb3194c218c83fde7ce5505c3f6c974394d2e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119792369"
---
# <a name="idxtkeyget_luminance-method"></a>IDxtKey :: obtient la \_ méthode de luminance

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `get_Luminance` méthode récupère la valeur de luminance sur laquelle la clé doit être ajoutée. Cette propriété s’applique uniquement lorsque le type de clé est DXTKEY \_ luminance.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Luminance(
  [out, retval] int *pVal
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pval* \[ out, retval\]
</dt> <dd>

Reçoit la valeur de luminance sur laquelle la clé doit être ajoutée.

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

 

 




