---
title: Classes auxiliaires liées de manière dynamique
description: Une classe auxiliaire liée de manière dynamique est une classe qui est attachée à un objet individuel, plutôt qu’à une classe d’objet.
ms.assetid: 10530a3c-89fc-4ff0-a0b7-1c9a27659003
ms.tgt_platform: multiple
keywords:
- Active Directory des classes auxiliaires liées de manière dynamique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd0cacb09d3aef05bcaf0ef729411c2e023469be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104190771"
---
# <a name="dynamically-linked-auxiliary-classes"></a>Classes auxiliaires liées de manière dynamique

Une classe auxiliaire liée de manière dynamique est une classe qui est attachée à un objet individuel, plutôt qu’à une classe d’objet. La liaison dynamique vous permet de stocker des attributs supplémentaires avec un objet individuel sans l’impact à l’échelle de la forêt de l’extension de la définition de schéma pour une classe entière. Par exemple, une entreprise peut utiliser la liaison dynamique pour attacher une classe auxiliaire spécifique aux ventes aux objets utilisateur de ses commerciaux, ainsi qu’à d’autres classes auxiliaires spécifiques au département, aux objets utilisateur des employés d’autres services.

La liaison dynamique n’est pas complexe : ajoutez le nom de la classe auxiliaire aux valeurs de l’attribut **objectClass** d’un objet. Si la classe auxiliaire possède des attributs obligatoires (**musthave** ou **systemMustHave**), vous devez les définir en même temps. Pour plus d’informations et pour obtenir un exemple de code, consultez [Ajout d’une classe auxiliaire à une instance d’objet](adding-an-auxiliary-class-to-an-object-instance.md).

Pour supprimer une classe auxiliaire liée de manière dynamique, effacez les valeurs de tous les attributs de la classe auxiliaire, puis supprimez le nom de la classe auxiliaire de l’attribut **objectClass** de l’objet.

Si vous ajoutez dynamiquement une classe auxiliaire qui est une sous-classe d’une autre classe auxiliaire, les deux classes auxiliaires sont ajoutées à l’objet cible. Toutefois, la suppression de la classe auxiliaire enfant ne supprime pas son parent ; chaque classe doit être supprimée explicitement.

 

 




