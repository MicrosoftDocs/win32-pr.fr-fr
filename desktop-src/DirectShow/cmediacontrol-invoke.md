---
description: 'Méthode CMediaControl. Invoke : fournit l’accès aux propriétés et aux méthodes exposées par un objet.'
ms.assetid: 05006f1e-24ff-4ed2-8291-2ba48495fec0
title: CMediaControl. Invoke, méthode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.Invoke
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fe077b2c69f603eef8737cbf7ea8c514e9b90c85
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006771"
---
# <a name="cmediacontrolinvoke-method"></a>CMediaControl. Invoke, méthode

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

Identificateur du membre. Utilisez [**CMediaControl :: GetIDsOfNames**](cmediacontrol-getidsofnames.md) ou la documentation de l’objet pour obtenir l’identificateur de dispatch.

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

Indicateurs décrivant le contexte de l' `CMediaControl::Invoke` appel.

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

## <a name="return-value"></a>Valeur de retour

Retourne la \_ valeur DISP E \_ UNKNOWNINTERFACE si *riid* n’est pas un IID \_ null. Retourne l’un des codes d’erreur de [**CMediaControl :: GetTypeInfo**](cmediacontrol-gettypeinfo.md) si l’appel échoue. Sinon, retourne le **HRESULT** de l’appel à **IDispatch :: Invoke**.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaControl, classe**](cmediacontrol.md)
</dt> </dl>

 

 




