---
title: Classes structurelles, abstraites et auxiliaires
description: L’attribut objectClassCategory d’un objet classSchema peut avoir une valeur, comme indiqué dans le tableau suivant, qui indique si la classe est structurelle, abstraite ou auxiliaire.
ms.assetid: 5af740cb-b292-4d80-abe5-3e3d194758f3
ms.tgt_platform: multiple
keywords:
- Classes structurelles, abstraites et auxiliaires AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 561bc836794b45b6c028fe8da772b0b38d0936a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028586"
---
# <a name="structural-abstract-and-auxiliary-classes"></a>Classes structurelles, abstraites et auxiliaires

L’attribut **objectClassCategory** d’un objet **classSchema** peut avoir une valeur, comme indiqué dans le tableau suivant, qui indique si la classe est structurelle, abstraite ou auxiliaire.



| Valeur | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | Classe structurelle, qui est le seul type de classe qui peut avoir des instances dans Active Directory Domain Services. Une classe structurelle peut être une sous-classe d’une classe abstraite ou structurelle. Une classe structurelle peut inclure n’importe quel nombre de classes auxiliaires dans sa définition.                                                                                                                                                                                                                                           |
| 2     | Classe abstraite, qui est un modèle utilisé pour dériver de nouvelles classes abstraites, auxiliaires et structurelles. Une classe abstraite ne peut être qu’une sous-classe d’une classe abstraite. Les classes abstraites ne peuvent pas être instanciées dans Active Directory Domain Services. Une classe abstraite peut inclure n’importe quel nombre de classes auxiliaires dans sa définition.                                                                                                                                                                                   |
| 3     | Classe auxiliaire, qui peut être incluse dans la définition d’une classe structurelle, abstraite ou auxiliaire, auquel cas les valeurs **mustContain**, **systemMustContain**, **mayContain** et **systemMayContain** de la classe auxiliaire sont ajoutées à celles de la classe. Une classe auxiliaire peut être une sous-classe d’une classe abstraite ou auxiliaire. Les classes auxiliaires ne peuvent pas être instanciées dans Active Directory Domain Services. Une classe auxiliaire peut inclure n’importe quel nombre de classes auxiliaires dans sa définition. |



 

Ne confondez pas le **objectClassCategory** avec une [catégorie d’objet](object-class-and-object-category.md).

 

 




