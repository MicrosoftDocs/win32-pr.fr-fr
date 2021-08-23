---
description: La classe CMediaPosition gère les méthodes IDispatch de l’interface double IMediaPosition.
ms.assetid: 5e84a2b6-39d4-47a4-93b4-690df12e2d19
title: CMediaPosition, classe (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7305d5eded589e167352ce7ff13194b52965b939daf907e8381b64684a03d1bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634849"
---
# <a name="cmediaposition-class"></a>CMediaPosition, classe

![hiérarchie de la classe cmediaposition](images/cutil14.png)

La classe **CMediaPosition** gère les méthodes **IDispatch** de l’interface double [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) .

Cette classe hérite de l’interface [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) , mais ne l’implémente pas. il implémente **IDispatch** par le biais de la classe [**CBaseDispatch**](cbasedispatch.md) et de la bibliothèque de types DirectShow. N’utilisez pas cette classe directement. Utilisez plutôt l’une des classes suivantes :

-   Filtres sources : utilisez la classe de base [**CSourceSeeking**](csourceseeking.md) pour implémenter la recherche.
-   Filtres de transformation : utilisez la classe [**CPosPassThru**](cpospassthru.md) pour transmettre les commandes de recherche en amont.
-   Convertisseurs : utilisez la classe [**CRendererPosPassThru**](crendererpospassthru.md) pour transmettre les commandes de recherche en amont.



| M&#233;thodes publiques                                              | Description                                                                                                         |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**CMediaPosition**](cmediaposition-cmediaposition.md)     | Méthode de constructeur.                                                                                                 |
| Méthodes IDispatch                                           | Description                                                                                                         |
| [**GetIDsOfNames**](cmediaposition-getidsofnames.md)       | Cartes un ensemble de noms à un ensemble correspondant de dispid.                                                              |
| [**GetTypeInfo**](cmediaposition-gettypeinfo.md)           | Récupère les informations de type de l’objet, qui peuvent ensuite être utilisées pour obtenir les informations de type d’une interface. |
| [**GetTypeInfoCount**](cmediaposition-gettypeinfocount.md) | Récupère le nombre d’interfaces d’informations de type fourni par l’objet.                                            |
| [**Appeler**](cmediaposition-invoke.md)                     | Fournit l’accès aux propriétés et aux méthodes exposées par l’objet.                                                    |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[DirectShow Classes de base](directshow-base-classes.md)
</dt> </dl>

 

 




