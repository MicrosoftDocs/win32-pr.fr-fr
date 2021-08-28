---
description: 'Méthode CMediaControl. GetTypeInfo : récupère un objet d’informations de type, qui peut récupérer les informations de type pour une interface.'
ms.assetid: 2014485f-d937-415d-a2fc-0c69269b5237
title: Méthode CMediaControl. GetTypeInfo (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.GetTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6355876c2237ec62813366c0a4fa32ffaff3d3c745a11ffde83fca81356edb00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055175"
---
# <a name="cmediacontrolgettypeinfo-method"></a>Méthode CMediaControl. GetTypeInfo

Récupère un objet d’informations de type, qui peut récupérer les informations de type pour une interface.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetTypeInfo(
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*itinfo* 
</dt> <dd>

Informations de type à retourner. Passe zéro pour récupérer les informations de type pour l’implémentation **IDispatch** .

</dd> <dt>

*lcid* 
</dt> <dd>

ID de paramètres régionaux pour les informations de type. Pour les classes qui prennent en charge les noms de membres localisés, un objet peut être en mesure de retourner des informations de type différentes pour différentes langues. Pour les classes qui ne prennent pas en charge les noms de membres localisés, ce paramètre peut être ignoré.

</dd> <dt>

*ppTInfo* 
</dt> <dd>

Adresse d’un pointeur vers l’objet d’informations de type demandé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne un \_ pointeur E si *ppTInfo* n’est pas valide. Retourne le TYPE \_ E \_ ELEMENTNOTFOUND si *iTInfo* n’est pas égal à zéro. Retourne S \_ OK si réussit. Sinon, retourne un **HRESULT** de l’un des appels pour récupérer le type.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaControl, classe**](cmediacontrol.md)
</dt> </dl>

 

 




