---
description: La méthode QueryId récupère un identificateur pour le code confidentiel.
ms.assetid: 6050292e-6203-4a79-87bf-47394624cb32
title: Méthode CSourceStream. QueryId (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1bd8582d16022c9d5dfd60eb87847d564ef69203e329ff37eaa9c2964a11794c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119317509"
---
# <a name="csourcestreamqueryid-method"></a>CSourceStream. QueryId, méthode

La `QueryId` méthode récupère un identificateur pour le code confidentiel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT QueryId(
   LPWSTR *Id
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Id* 
</dt> <dd>

Pointeur vers une variable qui reçoit une chaîne contenant l’identificateur de code confidentiel.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                                       | Description                                 |
|---------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>              | Réussite.<br/>                         |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl>     | Mémoire insuffisante.<br/>             |
| <dl> <dt>**\_pointeur E**</dt> </dl>         | Argument de pointeur **null** .<br/>       |
| <dl> <dt>**VFW \_ E \_ \_ introuvable**</dt> </dl> | Le code PIN est introuvable dans le filtre.<br/> |



 

## <a name="remarks"></a>Remarques

Cette méthode implémente la méthode [**IPIN :: QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) . Pour construire une chaîne d’identification, le code PIN appelle la méthode [**CSource :: FindPinNumber**](csource-findpinnumber.md) avec lui-même comme paramètre. La méthode **FindPinNumber** retourne le numéro de code confidentiel, indexé à partir de zéro. `QueryId` incrémente la valeur de retour d’une unité et convertit le résultat en une chaîne. Par exemple, la première broche devient « 1 ». la deuxième broche devient « 2 ». et ainsi de suite.

Si cette méthode retourne VFW \_ E \_ \_ introuvable, cela indique que le tableau de codes confidentiels du filtre n’est pas valide, vraisemblablement dû à un bogue dans le filtre.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Source. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSourceStream, classe**](csourcestream.md)
</dt> </dl>

 

 




