---
description: 'Méthode CMediaEvent. Invoke : fournit l’accès aux propriétés et aux méthodes exposées par un objet.'
ms.assetid: 2b091b57-0855-489a-9a33-cfc75f63ad07
title: CMediaEvent. Invoke, méthode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.Invoke
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 37fadefe3163ed4211b8112ec17cc1cfb3fb3625b4aba207db06a25de3e27b17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118655223"
---
# <a name="cmediaeventinvoke-method"></a>CMediaEvent. Invoke, méthode

Fournit l'accès aux propriétés et aux méthodes exposées par un objet.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Invoke(
   DISPID     dispidMember,
   REFIID     riid,
   LCID       lcid,
   WORD       wFlags,
   DISPPARAMS *pdispparams,
   VARIANT    *pvarResult,
   EXCEPINFO  *pexcepinfo,
   UINT       *puArgErr
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dispidMember* 
</dt> <dd>

Identificateur du membre. Utilisez [**CMediaEvent :: GetIDsOfNames**](cmediaevent-getidsofnames.md) ou la documentation de l’objet pour obtenir l’identificateur de dispatch.

</dd> <dt>

*riid* 
</dt> <dd>

Réservé pour un usage futur. Doit être un IID \_ null.

</dd> <dt>

*lcid* 
</dt> <dd>

Contexte des paramètres régionaux dans lequel interpréter les arguments.

</dd> <dt>

*wFlags* 
</dt> <dd>

Indicateurs décrivant le contexte de l' `CMediaEvent::Invoke` appel.

</dd> <dt>

*pdispparams* 
</dt> <dd>

Pointeur vers une structure qui contient un tableau d’arguments, un tableau d’ID de dispatch d’argument pour les arguments nommés et le nombre d’éléments dans les tableaux.

</dd> <dt>

*pvarResult* 
</dt> <dd>

Pointeur vers l’emplacement où le résultat doit être stocké, ou **null** si l’appelant n’attend aucun résultat.

</dd> <dt>

*pexcepinfo* 
</dt> <dd>

Pointeur vers une structure contenant des informations sur les exceptions.

</dd> <dt>

*puArgErr* 
</dt> <dd>

Pointeur vers l’index du premier argument, dans le tableau **rgvarg** de la structure **DISPPARAMS** , qui comporte une erreur. Pour plus d’informations sur **DISPPARAMS**, consultez le kit de développement Platform SDK.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la \_ valeur DISP E \_ UNKNOWNINTERFACE si *riid* n’est pas un IID \_ null. Retourne l’un des codes d’erreur de [**CMediaEvent :: GetTypeInfo**](cmediaevent-gettypeinfo.md) si l’appel échoue. Sinon, retourne le **HRESULT** de l’appel à **IDispatch :: Invoke**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaEvent, classe**](cmediaevent.md)
</dt> </dl>

 

 




