---
description: 'La méthode QueryInternalConnections récupère les broches qui sont connectées en interne à ce code confidentiel (dans le filtre). Cette méthode implémente la méthode IPin :: QueryInternalConnections.'
ms.assetid: 08344fc5-38b2-4dbe-8ef9-30d2fcd64187
title: Méthode CBasePin. QueryInternalConnections (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryInternalConnections
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 99a636295fc87347a1735ab028b6de342e887d55
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530527"
---
# <a name="cbasepinqueryinternalconnections-method"></a>Méthode CBasePin. QueryInternalConnections

La `QueryInternalConnections` méthode récupère les broches qui sont connectées en interne à ce code confidentiel (dans le filtre). Cette méthode implémente la méthode [**IPIN :: QueryInternalConnections**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryinternalconnections) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT QueryInternalConnections(
   IPin  *apPin,
   ULONG *nPin
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*apPin* 
</dt> <dd>

Adresse d’un tableau de pointeurs [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) .

</dd> <dt>

*nPin* 
</dt> <dd>

En entrée, spécifie la taille du tableau. Lorsque la méthode retourne, la valeur est définie sur le nombre de pointeurs retournés dans le tableau.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.



| Code de retour                                                                               | Description                         |
|-------------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>   | Taille de tableau insuffisante.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>      | Opération réussie.<br/>                 |
| <dl> <dt>**E \_ échec**</dt> </dl>    | Échec.<br/>                 |
| <dl> <dt>**\_NOTIMPL E**</dt> </dl> | Non implémenté.<br/>         |



 

## <a name="remarks"></a>Notes

Sur certains filtres, les broches d’entrée correspondent à des broches de sortie particulières. Pour chaque code confidentiel, cette méthode remplit un tableau avec des pointeurs vers les broches correspondantes. Si chaque broche d’entrée fournit des données pour chaque broche de sortie, retournez E \_ NOTIMPL.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePin, classe**](cbasepin.md)
</dt> </dl>

 

 




