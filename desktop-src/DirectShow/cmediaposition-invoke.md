---
description: La méthode Invoke fournit l’accès aux propriétés et aux méthodes exposées par l’objet.
ms.assetid: 3c03751d-239b-4cc5-bfab-8d1aed1074b8
title: CMediaPosition. Invoke, méthode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.Invoke
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3955848bf2a87e0983ddd7dc3bef48f157ae6648
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537119"
---
# <a name="cmediapositioninvoke-method"></a>CMediaPosition. Invoke, méthode

La `Invoke` méthode fournit l’accès aux propriétés et aux méthodes exposées par l’objet.

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

Identificateur du membre. Utilisez [**CMediaPosition :: GetIDsOfNames**](cmediaposition-getidsofnames.md) pour obtenir l’identificateur de dispatch.

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

Indicateurs décrivant le contexte de l'appel.

</dd> <dt>

*pdispparams* 
</dt> <dd>

Pointeur vers une structure **DIPPARAMS** qui contient les arguments.

</dd> <dt>

*pvarResult* 
</dt> <dd>

Pointeur vers un **Variant** qui reçoit le résultat, ou **null** si l’appelant n’attend aucun résultat.

</dd> <dt>

*pexcepinfo* 
</dt> <dd>

Pointeur vers une structure qui reçoit des informations sur l’exception.

</dd> <dt>

*puArgErr* 
</dt> <dd>

Pointeur vers une variable qui reçoit l’index du premier argument qui génère une erreur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes.



| Code de retour                                                                                              | Description                                      |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                     | Opération réussie.<br/>                              |
| <dl> <dt>**\_UNKNOWNINTERFACE DISP \_**</dt> </dl> | Le paramètre *riid* n’est pas une valeur d’IID \_ null<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaPosition, classe**](cmediaposition.md)
</dt> </dl>

 

 




