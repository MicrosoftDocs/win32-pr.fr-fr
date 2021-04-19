---
description: Méthode de constructeur.
ms.assetid: 3f758c45-21ec-4728-ba7d-41da7b2fa02f
title: Constructeur CMsgThread. CMsgThread (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.CMsgThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e77d3a84e349ab370b6319cd973f6ba86d632366
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525280"
---
# <a name="cmsgthreadcmsgthread-constructor"></a>Constructeur CMsgThread. CMsgThread

Méthode de constructeur.

## <a name="syntax"></a>Syntaxe


```C++
CMsgThread();
```



## <a name="parameters"></a>Paramètres

Ce constructeur n’a aucun paramètre.

## <a name="remarks"></a>Notes

La construction d’un objet de thread de message ne crée pas automatiquement le thread. Vous devez appeler la fonction membre [**CMsgThread :: CreateThread**](cmsgthread-createthread.md) pour créer le thread.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Msgthrd. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMsgThread, classe**](cmsgthread.md)
</dt> </dl>

 

 




