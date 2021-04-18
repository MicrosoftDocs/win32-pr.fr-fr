---
description: Méthode de constructeur.
ms.assetid: 0b372fa2-78a9-4e38-813c-f18123716c6d
title: Constructeur CDeferredCommand. CDeferredCommand (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.CDeferredCommand
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e92a2ffc5129ee38fc5061b28ea7ffef49da0f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533483"
---
# <a name="cdeferredcommandcdeferredcommand-constructor"></a>Constructeur CDeferredCommand. CDeferredCommand

Méthode de constructeur.

## <a name="syntax"></a>Syntaxe


```C++
CDeferredCommand(
   CCmdQueue *pQ,
   LPUNKNOWN pUnk,
   HRESULT   *phr,
   LPUNKNOWN pUnkExecutor,
   REFTIME   time,
   GUID      *iid,
   long      dispidMethod,
   short     wFlags,
   long      cArgs,
   VARIANT   *pDispParams,
   VARIANT   *pvarResult,
   short     *puArgErr,
   BOOL      bStream
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Québec* 
</dt> <dd>

Pointeur vers un objet qui expose l’interface [**IQueueCommand**](/windows/desktop/api/Control/nn-control-iqueuecommand) .

</dd> <dt>

*pUnk* 
</dt> <dd>

Pointeur vers l’interface **IUnknown** externe pour l’agrégation.

</dd> <dt>

*phr* 
</dt> <dd>

Pointeur vers une valeur **HRESULT** retournée.

</dd> <dt>

*pUnkExecutor* 
</dt> <dd>

Pointeur vers l’objet qui exécutera cette commande.

</dd> <dt>

*time* 
</dt> <dd>

Heure à laquelle la commande sera exécutée.

</dd> <dt>

*vaut* 
</dt> <dd>

Pointeur vers l’identificateur global unique (**GUID**) de l’interface qui contient la méthode.

</dd> <dt>

*dispidMethod* 
</dt> <dd>

Méthode sur l’interface à appeler.

</dd> <dt>

*wFlags* 
</dt> <dd>

Contexte de l’appel.

</dd> <dt>

*cArgs* 
</dt> <dd>

Nombre d’arguments passés.

</dd> <dt>

*pDispParams* 
</dt> <dd>

Pointeur désignant une liste de types variant d’arguments.

</dd> <dt>

*pvarResult* 
</dt> <dd>

Pointeur vers une liste de types variant retournée, le cas échéant.

</dd> <dt>

*puArgErr* 
</dt> <dd>

Pointeur vers le dernier argument de la liste de paramètres *pDispParams* avec une erreur.

</dd> <dt>

*bStream* 
</dt> <dd>

Valeur indiquant si l’heure de la commande différée est en temps de flux (**true**) ou en temps de présentation (**false**).

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDeferredCommand, classe**](cdeferredcommand.md)
</dt> </dl>

 

 




