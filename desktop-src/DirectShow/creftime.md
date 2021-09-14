---
description: La classe CRefTime est une classe d’assistance pour la gestion des temps de référence.
ms.assetid: 4be0fc23-77fb-4c45-a899-c1dfc6ee89b9
title: CRefTime, classe (reftime. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 01e83520943abafd814425b6ff3fb53f48775627
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999702"
---
# <a name="creftime-class"></a>CRefTime, classe

![hiérarchie de la classe creftime](images/cutil05.png)

La `CRefTime` classe est une classe d’assistance pour la gestion des temps de référence.

Une *heure de référence* est une unité de temps représentée en unités de 100 nanosecondes. Cette classe partage la même disposition des données que le type de données de [**\_ temps de référence**](reference-time.md) , mais ajoute des méthodes et des opérateurs qui fournissent des fonctions de comparaison, de conversion et arithmétiques. Pour plus d’informations sur les temps de référence, consultez [temps et horloges dans DirectShow](time-and-clocks-in-directshow.md).



| Variables membres publiques                                                 | Description                                           |
|-------------------------------------------------------------------------|-------------------------------------------------------|
| [**m \_ heure**](creftime-m-time.md)                                      | Spécifie la valeur de **\_ temps de référence** .              |
| M&#233;thodes publiques                                                          | Description                                           |
| [**CRefTime**](creftime-creftime.md)                                   | Méthode de constructeur.                                   |
| [**GetUnits**](creftime-getunits.md)                                   | Récupère le temps de référence en unités de 100 nanosecondes. |
| [**Millisecondes**](creftime-millisecs.md)                                 | Convertit la durée de référence en millisecondes.          |
| Opérateurs                                                               | Description                                           |
| [**\_temps de référence de l’opérateur ()**](creftime-operator-reference-time-.md) | Convertit l’objet en un type de données de **\_ temps de référence** .  |
| [**opérateur =**](creftime-operator-assign.md)                           | Affecte une nouvelle heure de référence.                         |
| [**opérateur + =**](creftime-operator-plus-assign.md)                     | Ajoute deux heures de référence.                             |
| [**opérateur =**](creftime-operator-minus-assign.md)                    | Soustrait une heure de référence d’une autre.            |



 

## <a name="remarks"></a>Notes

L’utilisation de cette classe présente un inconvénient potentiel. Si vous appliquez l’opérateur + = avec un objet **CRefTime** comme opérande de gauche et une variable de type **long** comme opérande de droite, le compilateur convertit implicitement l’opérande de droite en objet **CRefTime** . Cette contrainte utilise le constructeur **CRefTime** qui convertit les millisecondes en unités de temps de référence \_ ; par conséquent, l’opérande droit est multiplié par 10 000 :


```
CRefTime rt;   // rt.m_time is 0.
LONG val = 20;
rt += val;    // Coerce val to CRefTime, rt.m_time is now 200,000.
```



Toutefois, le même élément ne se produit pas à l’aide de l’opérateur + :


```
CRefTime rt;   // rt.m_time is 0.
LONG val = 20;
rt = rt + val; // CRefTime, rt.m_time is 20.
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Reftime. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




