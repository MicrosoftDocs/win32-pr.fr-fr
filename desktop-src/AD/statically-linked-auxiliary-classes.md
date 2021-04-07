---
title: Classes auxiliaires liées statiquement
description: Une classe auxiliaire liée de manière statique est une classe qui est incluse dans l’attribut auxiliaryClass ou systemAuxiliaryClass de la définition de l’objet classSchema d’une classe d’objets dans le schéma.
ms.assetid: 24765001-7a60-4654-a23a-bf0326b59096
ms.tgt_platform: multiple
keywords:
- Active Directory des classes auxiliaires liées statiquement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d1ef6191834687fc2b7741f097f6bfe75b5ef31
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671225"
---
# <a name="statically-linked-auxiliary-classes"></a>Classes auxiliaires liées statiquement

Une classe auxiliaire liée de manière statique est une classe qui est incluse dans l’attribut **auxiliaryClass** ou **systemAuxiliaryClass** de la définition de l’objet **classSchema** d’une classe d’objets dans le schéma. Cela signifie que la classe auxiliaire fait partie de chaque instance de la classe à laquelle elle est associée.

Une classe auxiliaire peut être liée de manière statique à une classe d’objet lorsque la classe est définie, autrement dit, quand son objet **classSchema** est ajouté au conteneur de schéma. Il s’agit de la seule fois où le **systemAuxiliaryClass** peut être utilisé ; après la création d’un objet **classSchema** , son attribut **systemAuxiliaryClass** ne peut pas être modifié. Une classe auxiliaire liée de manière statique à ce moment peut avoir des attributs obligatoires (**musthave**) et/ou facultatifs (**mayHave**).

Un utilisateur privilégié disposant des autorisations nécessaires pour étendre le schéma peut ajouter ou supprimer des classes auxiliaires de l’attribut **systemAuxiliaryClass** d’un objet **classSchema** existant. Cela permet d’ajouter ou de supprimer la classe auxiliaire de chaque instance existante de la classe d’objet. Une classe auxiliaire liée de manière statique à ce moment peut avoir des attributs facultatifs, mais elle ne peut pas avoir d’attributs obligatoires. Cela est dû au fait qu’il peut y avoir des instances existantes de la classe d’objet, auquel cas l’ajout d’un nouvel attribut obligatoire créerait des problèmes. Un utilisateur privilégié peut supprimer par la suite une classe auxiliaire de l’attribut **auxiliaryClass** d’un objet **classSchema** .

 

 




