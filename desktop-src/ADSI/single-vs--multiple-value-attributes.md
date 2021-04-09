---
title: Attributs Single et multiple value
description: Les attributs qui peuvent exister dans un répertoire sont généralement définis dans le schéma de l’annuaire.
ms.assetid: ea06ca66-6407-448f-8238-c8de5353663b
ms.tgt_platform: multiple
keywords:
- les attributs de valeur unique ou multiple sont des attributs ADSI
- attributs ADSI, valeurs uniques et attributs à valeurs multiples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cdfabd985be3446e4f104d300d75f891ef0ce60
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028547"
---
# <a name="single-vs-multiple-value-attributes"></a>Attributs Single et multiple value

Les attributs qui peuvent exister dans un répertoire sont généralement définis dans le schéma de l’annuaire. La définition de schéma d’un attribut spécifie un certain nombre de caractéristiques de l’attribut, telles que le type de données et si une instance de l’attribut peut avoir plusieurs valeurs.

Une instance d’un attribut à valeur unique peut contenir une seule valeur. Une instance d’un attribut à valeurs multiples peut contenir une ou plusieurs valeurs. Active Directory ne crée pas d’attributs avec des valeurs vides, soit l’attribut contient une valeur valide, soit il n’existe pas sur l’objet.

> [!Note]  
> Dans Active Directory et la plupart des autres serveurs LDAP, l’ordre des valeurs dans un attribut à valeurs multiples n’est pas défini. En outre, chaque valeur d’un attribut à valeurs multiples doit être unique.

 

ADSI charge normalement les données de schéma si votre annuaire prend en charge un schéma, comme le fait Active Directory. ADSI connaissant la syntaxe des attributs du schéma, vous n’êtes pas obligé de spécifier le type d’attribut lors de l’accès à celui-ci. ADSI marshale les valeurs d’attribut vers le type de données approprié, tel que défini dans le schéma.

Si votre répertoire n’a pas de schéma, fournissez le type de données lors de l’accès à un attribut.

> [!Note]  
> Active Directory, Exchange, Windows NT 4,0 et le serveur de site ont tous un schéma. En outre, Active Directory a un schéma extensible.

 

 

 




