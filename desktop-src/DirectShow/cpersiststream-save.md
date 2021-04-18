---
description: Enregistre les données du filtre dans le flux donné.
ms.assetid: f45c8c6e-f0bb-4358-805a-da2669706d34
title: CPersistStream. Save, méthode (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.Save
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c16e4820f846d2d60382fabd6aafe3ad82880193
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526727"
---
# <a name="cpersiststreamsave-method"></a>CPersistStream. Save, méthode

Enregistre les données du filtre dans le flux donné.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Save(
   LPSTREAM pStm,
   BOOL     fClearDirty
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pStm* 
</dt> <dd>

Pointeur vers le flux vers lequel les données doivent être enregistrées.

</dd> <dt>

*fClearDirty* 
</dt> <dd>

Indicateur qui spécifie s’il faut réinitialiser l’indicateur de modification du flux actuel. **True** signifie qu’il doit être réinitialisé. (Lorsque la méthode est appelée dans le cadre d’une opération d’enregistrement, la valeur est généralement **true**; quand elle est appelée dans le cadre d’une opération Enregistrer sous, la valeur est généralement **false**.)

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Notes

Cette fonction membre implémente la méthode **IPersistStream :: Save** . Il appelle **writeInt** avec la version logicielle, appelle [**CPersistStream :: WriteToStream**](cpersiststream-writetostream.md) avec le flux dans *pstm*, puis réinitialise **mPS \_ fDirty**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>PStream. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CPersistStream, classe**](cpersiststream.md)
</dt> </dl>

 

 




