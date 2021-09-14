---
description: La classe COARefTime convertit les temps de référence entre les secondes et les unités de 100 nanosecondes.
ms.assetid: 724420fc-9252-468f-9516-174be0a82999
title: COARefTime, classe (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 851495d69a1e34bd1723c20f88dc4bb86b7a8025
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010077"
---
# <a name="coareftime-class"></a>COARefTime, classe

![hiérarchie de la classe coareftime](images/cutil05.png)

La `COARefTime` classe convertit les temps de référence entre les secondes et les unités de 100 nanosecondes.

Cette classe effectue une conversion entre les temps de référence qui sont compatibles avec l’automatisation et les temps de référence compatibles avec C/C++. Les interfaces compatibles Automation utilisent des valeurs **double** pour représenter le temps en secondes. Les autres interfaces utilisent des valeurs **LongLong** bits 64 pour représenter le temps en unités de 100 nanosecondes. Les types suivants sont définis pour ces valeurs :

``` syntax
typedef LONGLONG  REFERENCE_TIME;
typedef double    REFTIME;
```

Les filtres peuvent utiliser la `COARefTime` classe pour effectuer une conversion entre les deux formats. Cette classe est dérivée de la classe [**CRefTime**](creftime.md) .



| M&#233;thodes publiques                                          | Description                                                           |
|---------------------------------------------------------|-----------------------------------------------------------------------|
| [**COARefTime**](coareftime-coareftime.md)             | Méthode de constructeur.                                                   |
| Opérateurs                                               | Description                                                           |
| [**double**](coareftime-double.md)                     | Convertit le temps de référence en valeur **double** .                    |
| [**temps de référence \_**](coareftime-reference-time.md)    | Convertit l’objet en valeur de **\_ temps de référence** .                      |
| [**opérateur =**](coareftime-operator-assign.md)        | Affecte une nouvelle heure de référence.                                         |
| [**opérateur = =**](coareftime-operator-eq.md)           | Teste l’égalité entre deux heures de référence.                       |
| [**opérateur ! =**](cmediatype-operator-neq.md)          | Teste l’inégalité entre deux heures de référence.                     |
| [**<d’opérateur**](coareftime-operator-lt.md)         | Teste si une heure de référence est inférieure à une autre.                     |
| [**>d’opérateur**](coareftime-operator-gt.md)         | Teste si une heure de référence est supérieure à une autre.                  |
| [**<opérateur =**](coareftime-operator-lteq.md)      | Teste si une heure de référence est inférieure ou égale à une autre.         |
| [**>opérateur =**](coareftime-operator-gteq.md)      | Teste si une heure de référence est supérieure ou égale à une autre.      |
| [**opérateur +**](coareftime-operator-plus.md)          | Ajoute deux heures de référence.                                             |
| [* * opérateur * *](coareftime-operator-minus.md)         | Soustrait une heure de référence d’une autre.                            |
| [**opérateur + =**](coareftime-operator-plus-assign.md)  | Ajoute deux heures de référence et assigne le résultat à cet objet.      |
| [**opérateur =**](coareftime-operator-minus-assign.md) | Soustrait deux heures de référence et assigne le résultat à cet objet. |
| [**and \***](coareftime-operator-mult.md)         | Multiplie une heure de référence par une valeur.                               |
| [**and**](coareftime-operator-div.md)           | Divise une heure de référence par une valeur.                                  |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




