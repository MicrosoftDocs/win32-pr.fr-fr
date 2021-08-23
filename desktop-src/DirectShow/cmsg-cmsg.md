---
description: Construit un objet CMsg.
ms.assetid: b7ee0643-73e4-450d-bff4-ca5006fdcc14
title: Constructeur CMsg. CMsg (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsg.CMsg
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f921c96ae185d8993002c84a09b4efb8bc5977104c274de3a2ffc964a093f1a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831899"
---
# <a name="cmsgcmsg-constructor"></a>Constructeur CMsg. CMsg

Construit un objet [**CMsg**](cmsg.md) .

## <a name="syntax"></a>Syntaxe


```C++
CMsg(
   UINT     u,
   DWORD    dw,
   LPVOID   lp,
   CAMEvent *pEvent
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*u* 
</dt> <dd>

Code de requête, défini par le client de la classe de thread et compris par la fonction de thread de travail remplacée.

</dd> <dt>

*dw* 
</dt> <dd>

Paramètre d’indicateur pour le code de la requête.

</dd> <dt>

*Aid* 
</dt> <dd>

Pointeur vers les données requises par le thread de travail comme valeurs de paramètre ou de retour. Ces données ne doivent pas être basées sur la pile, car elles seront référencées un peu plus tard après la fin de l’opération de mise en file d’attente.

</dd> <dt>

*pEvent* 
</dt> <dd>

Pointeur vers l’objet d’événement qu’un thread de travail peut signaler pour indiquer l’achèvement de l’opération.

</dd> </dl>

## <a name="remarks"></a>Remarques

Cette fonction membre contient une demande pour un thread de travail [**CMsgThread**](cmsgthread.md) sur lequel agir. Tous les paramètres sont passés à la fonction de thread de travail en tant que paramètres lorsque ce message est traité. La signification des paramètres est définie par la fonction cliente qui appelle le thread de travail et la classe dérivée qui fournit la fonction d’exécution du thread de travail.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Msgthrd. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




