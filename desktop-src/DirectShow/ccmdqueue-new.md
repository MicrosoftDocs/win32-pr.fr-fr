---
description: La nouvelle méthode initialise une commande à exécuter et retourne un nouvel objet CDeferredCommand.
ms.assetid: bdd80747-a15b-422a-b742-ebfa4076bdf7
title: CCmdQueue. New, méthode (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.New
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c8b6ad22b67df863e699649f22f513a98ca1306751a1d449a683f306c9cc2938
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910389"
---
# <a name="ccmdqueuenew-method"></a>CCmdQueue. New, méthode

La `New` méthode initialise une commande à exécuter et retourne un nouvel objet [**CDeferredCommand**](cdeferredcommand.md) .

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT New(
   CDeferredCommand **ppCmd,
   LPUNKNOWN        pUnk,
   REFTIME          time,
   GUID             *iid,
   long             dispidMethod,
   short            wFlags,
   long             cArgs,
   VARIANT          *pDispParams,
   VARIANT          *pvarResult,
   short            *puArgErr,
   BOOL             bStream
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppCmd* 
</dt> <dd>

Adresse d’un pointeur vers un objet [**CDeferredCommand**](cdeferredcommand.md) par lequel une application peut annuler la commande, définir une nouvelle heure de présentation pour celle-ci ou récupérer des informations d’estimation.

</dd> <dt>

*pUnk* 
</dt> <dd>

Pointeur vers l’objet qui exécutera la commande.

</dd> <dt>

*time* 
</dt> <dd>

Heure à laquelle exécuter la ou les commandes mises en file d’attente.

</dd> <dt>

*vaut* 
</dt> <dd>

Pointeur vers l’identificateur global unique (**GUID**) de l’interface à appeler.

</dd> <dt>

*dispidMethod* 
</dt> <dd>

Méthode sur l’interface à appeler.

</dd> <dt>

*wFlags* 
</dt> <dd>

Indicateurs décrivant le contexte de l'appel. Ce paramètre prend en charge les mêmes indicateurs que la méthode **IDispatch :: Invoke** .

</dd> <dt>

*cArgs* 
</dt> <dd>

Nombre d’arguments passés.

</dd> <dt>

*pDispParams* 
</dt> <dd>

Pointeur vers la liste des types variant associés aux paramètres de dispatch.

</dd> <dt>

*pvarResult* 
</dt> <dd>

Pointeur vers la liste où les résultats, le cas échéant, doivent être retournés.

</dd> <dt>

*puArgErr* 
</dt> <dd>

Pointeur vers l’index dans la liste de paramètres *pDispParams* où la dernière erreur s’est produite.

</dd> <dt>

*bStream* 
</dt> <dd>

Valeur indiquant si le paramètre de *temps* est une valeur de flux de temps (**true**) ou une valeur d’heure de présentation (**false**).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK en cas de réussite. Retourne E \_ OUTOFMEMORY si *ppCmd* renvoie de la création du nouvel objet [**CDeferredCommand**](cdeferredcommand.md) avec la valeur **null**. Sinon, retourne un **HRESULT** qui indique une erreur lors de la tentative de création d’un nouvel objet **CDeferredCommand** . En cas d’erreur, aucun objet n’a été mis en file d’attente.

## <a name="remarks"></a>Remarques

Le nouvel objet [**CDeferredCommand**](cdeferredcommand.md) sera initialisé avec les paramètres et sera ajouté à la file d’attente pendant la construction. Cette méthode est similaire à la méthode **IDispatch :: Invoke** .

Les valeurs du paramètre *wFlags* sont les suivantes :



| Valeur                    | Description                                                                                                                                                          |
|--------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DISPATCH ( \_ méthode)         | Le membre est exécuté en tant que méthode. Si une propriété porte le même nom, vous pouvez définir à la fois cet indicateur et l' \_ indicateur PROPERTYGET (Dispatch.                                       |
| DISTRIBUER \_ PropertyGet (    | Le membre est récupéré en tant que propriété ou membre de données.                                                                                                          |
| DISTRIBUER \_ PROPERTYPUT    | Le membre est modifié en tant que propriété ou membre de données.                                                                                                            |
| DISTRIBUER \_ PROPERTYPUTREF | Le membre est modifié via une assignation de référence, plutôt que comme une assignation de valeur. Cette valeur est valide uniquement lorsque la propriété accepte une référence à un objet. |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CCmdQueue, classe**](ccmdqueue.md)
</dt> </dl>

 

 




