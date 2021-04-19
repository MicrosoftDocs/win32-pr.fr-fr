---
description: Les ressources nécessaires à la personnalisation d’une application, telles que les modèles d’entreprise, peuvent être déployées avec l’application en incluant une transformation avec le package d’installation de l’application.
ms.assetid: 3d9328d0-4d95-449c-bf2b-5487f7ba5971
title: Utilisation des transformations pour ajouter des ressources
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c11fac7ad65601286fb550abd950bf5ac49af1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543114"
---
# <a name="using-transforms-to-add-resources"></a><span data-ttu-id="b7bb0-103">Utilisation des transformations pour ajouter des ressources</span><span class="sxs-lookup"><span data-stu-id="b7bb0-103">Using Transforms to Add Resources</span></span>

<span data-ttu-id="b7bb0-104">Les ressources nécessaires à la personnalisation d’une application, telles que les modèles d’entreprise, peuvent être déployées avec l’application en incluant une transformation avec le package d’installation de l’application.</span><span class="sxs-lookup"><span data-stu-id="b7bb0-104">Resources that are needed for the customization of an application, such as corporate templates, can be deployed with the application by including a transform with the application's installation package.</span></span> <span data-ttu-id="b7bb0-105">Les règles suivantes doivent être suivies lors du déploiement de ressources, telles que des fichiers, des clés de registre ou des raccourcis, à l’aide d’une transformation.</span><span class="sxs-lookup"><span data-stu-id="b7bb0-105">The following rules should be followed when deploying resources, such as files, registry keys, or shortcuts, using a transform.</span></span>

-   <span data-ttu-id="b7bb0-106">La transformation doit ajouter un ou plusieurs nouveaux composants à la base de données d’installation pour contenir les ressources supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="b7bb0-106">The transform should add one or more new components to the installation database to contain the additional resources.</span></span> <span data-ttu-id="b7bb0-107">La transformation ne doit pas ajouter de ressources à un composant qui existe déjà dans l’installation.</span><span class="sxs-lookup"><span data-stu-id="b7bb0-107">The transform should not add resources to a component that already exists in the installation.</span></span>
-   <span data-ttu-id="b7bb0-108">La transformation doit ajouter une ou plusieurs nouvelles fonctionnalités à la base de données d’installation pour contenir ces nouveaux composants.</span><span class="sxs-lookup"><span data-stu-id="b7bb0-108">The transform should add one or more new features to the installation database to contain these new components.</span></span> <span data-ttu-id="b7bb0-109">Ces nouvelles fonctionnalités ne doivent pas être les parents des fonctionnalités existantes, mais les nouvelles fonctionnalités parent et enfant peuvent être introduites ensemble.</span><span class="sxs-lookup"><span data-stu-id="b7bb0-109">These new features should not be the parents of any existing features, but new parent and child features may be introduced together.</span></span> <span data-ttu-id="b7bb0-110">Les nouvelles fonctionnalités doivent être attribuées à des noms uniques dans toutes les autres transformations de ce produit.</span><span class="sxs-lookup"><span data-stu-id="b7bb0-110">New features should be given names that are unique across all other transforms for this product.</span></span> <span data-ttu-id="b7bb0-111">Deux transformations ne doivent jamais ajouter une fonctionnalité à ce produit qui porte le même nom que celui figurant dans la colonne de fonctionnalités de la [table de fonctionnalités](feature-table.md) et qui contient des composants ou des ressources différents.</span><span class="sxs-lookup"><span data-stu-id="b7bb0-111">No two transforms should ever add a feature to this product that has the same name listed in the Feature column of the [Feature table](feature-table.md) and containing different components or resources.</span></span>

 

 



