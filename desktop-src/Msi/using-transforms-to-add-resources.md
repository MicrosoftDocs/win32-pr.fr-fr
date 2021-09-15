---
description: Les ressources nécessaires à la personnalisation d’une application, telles que les modèles d’entreprise, peuvent être déployées avec l’application en incluant une transformation avec le package d’installation de l’application.
ms.assetid: 3d9328d0-4d95-449c-bf2b-5487f7ba5971
title: Utilisation des transformations pour ajouter des ressources
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c11fac7ad65601286fb550abd950bf5ac49af1f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413915"
---
# <a name="using-transforms-to-add-resources"></a>Utilisation des transformations pour ajouter des ressources

Les ressources nécessaires à la personnalisation d’une application, telles que les modèles d’entreprise, peuvent être déployées avec l’application en incluant une transformation avec le package d’installation de l’application. Les règles suivantes doivent être suivies lors du déploiement de ressources, telles que des fichiers, des clés de registre ou des raccourcis, à l’aide d’une transformation.

-   La transformation doit ajouter un ou plusieurs nouveaux composants à la base de données d’installation pour contenir les ressources supplémentaires. La transformation ne doit pas ajouter de ressources à un composant qui existe déjà dans l’installation.
-   La transformation doit ajouter une ou plusieurs nouvelles fonctionnalités à la base de données d’installation pour contenir ces nouveaux composants. Ces nouvelles fonctionnalités ne doivent pas être les parents des fonctionnalités existantes, mais les nouvelles fonctionnalités parent et enfant peuvent être introduites ensemble. Les nouvelles fonctionnalités doivent être attribuées à des noms uniques dans toutes les autres transformations de ce produit. Deux transformations ne doivent jamais ajouter une fonctionnalité à ce produit qui porte le même nom que celui figurant dans la colonne de fonctionnalités de la [table de fonctionnalités](feature-table.md) et qui contient des composants ou des ressources différents.

 

 



