---
description: La classe CBaseDispatch est une classe de base pour l’implémentation de l’interface IDispatch dans un filtre DirectShow.
ms.assetid: 33a989be-d059-4ad7-99f8-715c55a128a2
title: CBaseDispatch, classe (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d115412b2b668f640834d5a3fa3b134f7a8d9c01
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106524007"
---
# <a name="cbasedispatch-class"></a>CBaseDispatch, classe

![hiérarchie de la classe cbasedispatch](images/cutil01.png)

La classe **CBaseDispatch** est une classe de base pour l’implémentation de l’interface **IDispatch** dans un filtre DirectShow.

Cette classe est limitée à la prise en charge des interfaces compatibles Automation exportées par la bibliothèque de types DirectShow, QuartzTypeLib. Par exemple, les classes [**CMediaControl**](cmediacontrol.md) et [**CMediaPosition**](cmediaposition.md) utilisent **CBaseDispatch** pour implémenter [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) et [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), respectivement. En raison de cette limitation, il n’y a probablement aucune raison d’utiliser **CBaseDispatch** directement dans vos propres filtres.

Pour utiliser cette classe, procédez comme suit :

-   Déclarez une nouvelle classe qui prend en charge **IDispatch**.
-   Donnez à votre nouvelle classe une variable membre privée de type **CBaseDispatch**.
-   Implémentez les méthodes **IDispatch** .
-   Dans vos méthodes **IDispatch** , appelez les méthodes **CBaseDispatch** .

Pour plus d’informations, reportez-vous au code source de l’un des exemples de classes déclarés dans Ctlutil. h.



| M&#233;thodes publiques                                             | Description                                                                                                         |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**CBaseDispatch**](cbasedispatch-cbasedispatch.md)       | Méthode de constructeur.                                                                                                 |
| [**~ CBaseDispatch**](cbasedispatch--cbasedispatch.md)     | Méthode de destructeur.                                                                                                  |
| [**GetIDsOfNames**](cbasedispatch-getidsofnames.md)       | Mappe un ensemble de noms à un ensemble correspondant de DISPID.                                                              |
| [**GetTypeInfo**](cbasedispatch-gettypeinfo.md)           | Récupère les informations de type de l’objet, qui peuvent ensuite être utilisées pour obtenir les informations de type d’une interface. |
| [**GetTypeInfoCount**](cbasedispatch-gettypeinfocount.md) | Récupère le nombre d’interfaces d’informations de type fourni par l’objet.                                            |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Classes de base DirectShow](directshow-base-classes.md)
</dt> </dl>

 

 




