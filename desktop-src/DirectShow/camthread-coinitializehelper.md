---
description: La méthode CoInitializeHelper appelle la fonction CoInitializeEx au début du thread.
ms.assetid: 1a981e1e-c059-4e51-81d8-33bcb39ee580
title: Méthode CAMThread. CoInitializeHelper (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CoInitializeHelper
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6c3eb7fbcb9e4abada43098339a29d208ded0d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539622"
---
# <a name="camthreadcoinitializehelper-method"></a>Méthode CAMThread. CoInitializeHelper

La `CoInitializeHelper` méthode appelle la fonction CoInitializeEx au début du thread.

## <a name="syntax"></a>Syntaxe


```C++
static HRESULT CoInitializeHelper();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes.



| Code de retour                                                                             | Description                                              |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | La fonction CoInitializeEx n’est pas disponible.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>    | Opération réussie.<br/>                                      |
| <dl> <dt>**E \_ échec**</dt> </dl>  | Échec.<br/>                                      |



 

## <a name="remarks"></a>Notes

La méthode [**CAMThread :: InitialThreadProc**](camthread-initialthreadproc.md) appelle cette méthode d’assistance, qui appelle la fonction CoInitializeEx. Elle utilise l’indicateur coinit \_ Disable \_ OLE1DDE pour désactiver l’échange dynamique de données (DDE). Pour plus d’informations, consultez le kit de développement Platform SDK.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (include streams. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CAMThread, classe**](camthread.md)
</dt> </dl>

 

 




