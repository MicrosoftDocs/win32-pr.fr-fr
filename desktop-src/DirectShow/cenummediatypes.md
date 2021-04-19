---
description: La classe CEnumMediaTypes implémente un énumérateur pour les types de média préférés.
ms.assetid: 50a90926-0bc7-4204-8000-81894bd154ac
title: CEnumMediaTypes, classe (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ad5e1de9eb2edbdb63eb6f476391ae8387c8d01e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530990"
---
# <a name="cenummediatypes-class"></a>CEnumMediaTypes, classe

![hiérarchie de la classe cenummediatypes](images/filter04.png)

La `CEnumMediaTypes` classe implémente un énumérateur pour les types de média préférés.

Cette classe implémente l’interface [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) . Il appelle les méthodes [**CBasePin**](cbasepin.md) suivantes :

-   [**CBasePin :: GetMediaType**](cbasepin-getmediatype.md): récupère un type de média, référencé par un index de base zéro.
-   [**CBasePin :: GetMediaTypeVersion**](cbasepin-getmediatypeversion.md): détermine si l’ensemble de types préférés a changé.

Chaque fois qu’un code PIN modifie sa liste de types de médias préférés, le code PIN incrémente le numéro de version du type de média. Dans ce cas, l’objet énumérateur n’est plus synchronisé avec le code confidentiel, et les méthodes de la classe retournent VFW \_ E \_ enum non \_ \_ \_ synchronisé. Appelez la méthode [**CEnumMediaTypes :: Reset**](cenummediatypes-reset.md) pour resynchroniser l’énumérateur.



| M&#233;thodes publiques                                               | Description                                                     |
|--------------------------------------------------------------|-----------------------------------------------------------------|
| [**CEnumMediaTypes**](cenummediatypes-cenummediatypes.md)   | Méthode de constructeur.                                             |
| [**~ CEnumMediaTypes**](cenummediatypes--cenummediatypes.md) | Méthode de destructeur. Virtuels.                                     |
| Méthodes IEnumMediaTypes                                      | Description                                                     |
| [**Répliqué**](cenummediatypes-clone.md)                       | Fait une copie de l’énumérateur avec le même état d’énumération. |
| [**Suivant**](cenummediatypes-next.md)                         | Récupère un nombre spécifié de types de médias.                    |
| [**Réinitialiser**](cenummediatypes-reset.md)                       | Réinitialise la séquence d'énumération au début.               |
| [**Saut**](cenummediatypes-skip.md)                         | Ignore un nombre spécifié de types de médias.                   |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




