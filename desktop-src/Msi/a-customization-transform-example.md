---
description: Cet exemple montre comment une transformation de personnalisation peut être utilisée pour désactiver des fonctionnalités et ajouter de nouvelles ressources.
ms.assetid: 028b1d01-3b66-4640-98f9-ca33f90ca516
title: Exemple de transformation de personnalisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26ea655d1187b0271aba7ea56a46bacf95f5fb40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519068"
---
# <a name="a-customization-transform-example"></a>Exemple de transformation de personnalisation

Cet exemple montre comment une transformation de personnalisation peut être utilisée pour désactiver des fonctionnalités et ajouter de nouvelles ressources.

Un administrateur peut désactiver définitivement une fonctionnalité à l’aide d’une transformation de personnalisation pour entrer 0 dans la colonne de niveau de la [table des fonctionnalités](feature-table.md). L’application de la transformation de personnalisation empêche l’installation et l’affichage de cette fonctionnalité, même si l’utilisateur sélectionne une installation complète à l’aide de l’interface utilisateur ou en affectant à la propriété [**addlocal**](addlocal.md) la valeur All sur la ligne de commande. Pour plus d’informations sur le niveau d’installation, consultez [table des fonctionnalités](feature-table.md) et propriété [**INSTALLLEVEL**](installlevel.md) .

Les ressources nécessaires pour personnaliser une application peuvent être déployées à l’aide d’une transformation de personnalisation pour ajouter un ou plusieurs nouveaux composants. La transformation doit ajouter une ou plusieurs nouvelles fonctionnalités pour contenir ces nouveaux composants. Pour connaître les règles qui doivent être suivies lors du déploiement de ressources, telles que des fichiers, des clés de registre ou des raccourcis, consultez [utilisation de transformations pour ajouter des ressources](using-transforms-to-add-resources.md).

Cet exemple montre comment créer une [transformation](transforms.md) pour personnaliser l’installation de l’application décrite dans [un exemple d’installation](an-installation-example.md). Le package d’installation d’origine installe toutes les fonctionnalités de l’exemple d’application, y compris la porte de fonctionnalités, qui permet aux utilisateurs d’afficher les informations d’admission pour le parc de parcs rouge. Certains groupes d’utilisateurs ont uniquement besoin des fonctionnalités d’application qui fournissent des informations sur la planification des événements et n’ont pas besoin de la fonctionnalité de porte. Ces groupes doivent également obtenir une liste de numéros de téléphone spéciale. La transformation doit donc faire deux choses : 1) personnaliser l’installation afin que ce groupe ne reçoive que les fonctionnalités d’application dont il a besoin et 2) fournisse les ressources nécessaires pour la nouvelle liste téléphonique.

Un exemple d’interface utilisateur minimale pour cet exemple est fourni dans les [composants SDK Windows pour Windows Installer les développeurs](platform-sdk-components-for-windows-installer-developers.md) comme Uisample.msi de fichier. Si vous avez le kit de développement logiciel (SDK), vous avez accès à tous les outils et données nécessaires pour reproduire l’exemple de package d’installation, l’interface utilisateur et la transformation de personnalisation.

La transformation de personnalisation présente les spécifications suivantes :

-   La transformation de personnalisation est incorporée dans le fichier MNP2000.msi pour garantir qu’elle est toujours disponible avec la base de données d’installation.
-   L’installation de MNP2000.msi à l’aide de la transformation de personnalisation n’installe pas la fonctionnalité porte, les fonctionnalités enfants de la fonctionnalité porte ou l’un des composants de la fonctionnalité de porte, même si l’utilisateur sélectionne le type complet d’installation.
-   D’autres applications peuvent partager certains ou l’ensemble des composants de la fonctionnalité de la porte. Les packages d’installation de ces applications peuvent installer tous leurs composants sur l’ordinateur de l’utilisateur.
-   La suppression de MNP2000.msi à l’aide de la transformation de personnalisation ne supprime pas les composants de la porte qui ont été installés par d’autres applications.
-   L’installation de MNP2000.msi avec la transformation de personnalisation installe également une nouvelle fonctionnalité de niveau supérieur, une \_ Liste téléphonique et un nouveau composant, téléphone, qui nécessite l’installation de la ressource, Phone.txt. L’utilisateur accède à la \_ fonctionnalité de liste téléphonique à l’aide d’un raccourci dans le répertoire menu.

[Continuer](customizing-an-original-database.md)

 

 



