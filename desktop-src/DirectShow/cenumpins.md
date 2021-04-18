---
description: La classe CEnumPins implémente un énumérateur pour les codes confidentiels.
ms.assetid: 8729f294-c76d-404f-9f51-7565470eced8
title: CEnumPins, classe (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5dde02c31ed0ef72e6df36a6cf0364b7f184304e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533365"
---
# <a name="cenumpins-class"></a>CEnumPins, classe

![hiérarchie de la classe cenumpins](images/filter03.png)

La `CEnumPins` classe implémente un énumérateur pour les codes confidentiels.

Cette classe implémente l’interface [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) . Il appelle les méthodes [**CBaseFilter**](cbasefilter.md) suivantes :

-   [**CBaseFilter :: GetPin**](cbasefilter-getpin.md): récupère un code confidentiel sur le filtre, référencé par un index de base zéro.
-   [**CBaseFilter :: GetPinCount**](cbasefilter-getpincount.md): récupère le nombre total de broches sur le filtre.
-   [**CBaseFilter :: GetPinVersion**](cbasefilter-getpinversion.md): détermine si les broches ont changé.

Si le filtre crée ou détruit dynamiquement des broches, il incrémente la version du code confidentiel chaque fois que les codes confidentiels changent. Si le numéro de version change, l’objet énumérateur n’est plus synchronisé avec le filtre. Une fois l’énumérateur désynchronisé, les méthodes de `CEnumPins` retournent \_ les \_ enums VFW E non \_ \_ \_ synchronisés. Appelez la méthode [**CEnumPins :: Reset**](cenumpins-reset.md) pour resynchroniser l’énumérateur.



| M&#233;thodes publiques                             | Description                                                     |
|--------------------------------------------|-----------------------------------------------------------------|
| [**CEnumPins**](cenumpins-cenumpins.md)   | Méthode de constructeur.                                             |
| [**~ CEnumPins**](cenumpins--cenumpins.md) | Méthode de destructeur. Virtuels.                                     |
| Méthodes IEnumPins                          | Description                                                     |
| [**Répliqué**](cenumpins-clone.md)           | Fait une copie de l’énumérateur avec le même état d’énumération. |
| [**Suivant**](cenumpins-next.md)             | Récupère un nombre spécifié de broches.                           |
| [**Réinitialiser**](cenumpins-reset.md)           | Réinitialise la séquence d'énumération au début.               |
| [**Saut**](cenumpins-skip.md)             | Ignore un nombre spécifié de broches.                          |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




