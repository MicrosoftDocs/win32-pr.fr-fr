---
title: Extensions de schéma
description: L’architecture du schéma ADSI fournit que de nouvelles classes de schéma peuvent être ajoutées au conteneur de classe de schéma et de nouvelles propriétés à un objet de classe de schéma existant au moment de l’exécution.
ms.assetid: 935d39ca-cfb9-4aa3-aa0e-b614f7b359f2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b86491966e2bfddbef72d68d7a96869448c38188
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100557"
---
# <a name="schema-extensions"></a>Extensions de schéma

L’architecture du schéma ADSI fournit que de nouvelles classes de schéma peuvent être ajoutées au conteneur de classe de schéma et de nouvelles propriétés à un objet de classe de schéma existant au moment de l’exécution. La dernière possibilité ne requiert pas de nouveau code. Il s’agit d’une fonctionnalité importante pour les espaces de noms qui autorisent les services d’annuaire extensibles. Le composant fournisseur doit autoriser cette extensibilité et savoir où accéder et stocker l’instance de classe et les valeurs de ses propriétés. Dans un service d’annuaire extensible classique, ces informations sont stockées dans la base de données du service d’annuaire de la même manière que toute autre classe de schéma et définition de propriété.

> [!Note]  
> Dans la terminologie de l’interface COM, seules les propriétés peuvent être ajoutées à une classe de schéma existante, et non à des méthodes. L’ajout d’une nouvelle méthode nécessite l’ajout d’une nouvelle implémentation de cette méthode et nécessite donc du code supplémentaire.

 

Pour obtenir un exemple de schéma de fournisseur spécifique, consultez [gestion des schémas](schema-management.md).

 

 




