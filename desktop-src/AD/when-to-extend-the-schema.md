---
title: Quand étendre le schéma
description: Étendez le schéma uniquement si aucune classe d’objet existante ne répond aux besoins de votre application. L’extension du schéma est une opération complexe. les modifications de schéma sont répliquées sur chaque contrôleur de domaine de la forêt d’entreprise. Envisagez cette considération avec prudence.
ms.assetid: 92231f31-d2af-4c3b-981e-e55cc478899d
ms.tgt_platform: multiple
keywords:
- Quand étendre l’AD du schéma
- schéma Active Directory, quand étendre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18c182b346fd1e31bc549325260d9b57d75bbb63
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511614"
---
# <a name="when-to-extend-the-schema"></a>Quand étendre le schéma

Étendez le schéma uniquement si aucune classe d’objet existante ne répond aux besoins de votre application. L’extension du schéma est une opération complexe. les modifications de schéma sont répliquées sur chaque contrôleur de domaine de la forêt d’entreprise. Envisagez cette considération avec prudence.

Le schéma peut être étendu de trois façons :

-   Dérivez une nouvelle sous-classe d’une classe existante-la sous-classe possède tous les attributs de la superclasse et les attributs que vous spécifiez. Dérivation à partir d’une classe existante :
    -   Lorsque la classe existante requiert des attributs supplémentaires, mais dans le cas contraire.
    -   Lorsque la possibilité de transformer des objets existants de la classe en une nouvelle classe n’est pas obligatoire. Il n’est pas possible d’ajouter une sous-classe à un objet existant.
    -   Pour utiliser le composant logiciel enfichable Gestionnaire de répertoire existant pour gérer les attributs étendus des objets.
-   Ajoutez des attributs à une classe existante et/ou ajoutez des objets parents pour la classe. Lors de l’ajout de plusieurs attributs, effectuez cette opération de manière structurée en définissant une classe auxiliaire et en ajoutant cette classe auxiliaire à la classe existante.
-   La modification d’une classe existante est requise lorsqu’une application nécessite la possibilité d’étendre des objets existants de la classe. Par exemple, pour ajouter des données spécifiques à l’application à l’objet utilisateur, étendez l’utilisateur de la classe normalement, car vous devez gérer les utilisateurs existants et pas seulement les utilisateurs spéciaux créés par votre application.
-   Créez une nouvelle classe avec les attributs requis. Créez une nouvelle classe. autrement dit, une classe dérivée de « Top » quand aucune classe existante ne répond aux spécifications opérationnelles.

Quand vous sous-classez une classe existante, les éléments d’interface utilisateur associés à la classe d’origine ne sont pas hérités par la sous-classe. Par exemple, si vous sous-classez un objet utilisateur, les pages de propriétés et les éléments de menu associés à l’utilisateur ne sont pas hérités. Pour cette raison, il est préférable d’étendre un objet existant ou de créer une classe auxiliaire au lieu de créer une sous-classe.

Si vous sous-classez une classe existante ou modifiez une classe existante, vous devez étendre les outils tels que le composant logiciel enfichable utilisateurs et ordinateurs Active Directory pour gérer les attributs étendus des objets. Pour plus d’informations, consultez [extension de l’interface utilisateur pour les objets d’annuaire](extending-the-user-interface-for-directory-objects.md).

 

 




