---
description: Le Windows Installer réduit le coût total de possession (TCO) de vos applications en renforçant la capacité de vos clients à gérer et à gérer les composants de l’application lors de l’installation et de l’exécution.
ms.assetid: fbb139e3-c81b-44fc-9e92-bada0be02862
title: Gestion des composants
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aeff6c25556879429330170ec8190b1296576517
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545831"
---
# <a name="component-management"></a>Gestion des composants

Le Windows Installer réduit le coût total de possession (TCO) de vos applications en renforçant la capacité de vos clients à gérer et à gérer les composants de l’application lors de l’installation et de l’exécution. La base de données d’installation effectue le suivi des applications qui nécessitent un composant particulier, des fichiers qui composent chaque composant, où chaque fichier est installé sur le système et où se trouvent les sources des composants. Cela permet aux développeurs de créer des packages qui offrent les avantages suivants :

-   Résilience accrue des applications. Utilisez le programme d’installation pour détecter et réinstaller les composants endommagés sans avoir à réexécuter l’installation. Le programme d’installation vérifie le chemin d’accès d’un composant au moment de l’exécution. Cela permet de libérer des applications de la dépendance sur les chemins d’accès de fichiers statiques qui diffèrent généralement entre les ordinateurs et peuvent pointer vers des composants manquants. Pour plus d’informations, consultez [résilience](resiliency.md).
-   Installation à la demande. Ce jeu de fonctionnalités n’est pas installé lors de l’installation, mais il est spécifié dans la base de données à installer juste-à-temps pour une utilisation si l’application l’exige à l’avenir. Les utilisateurs n’ont pas besoin de réexécuter l’installation. Pour plus d’informations, consultez [installation-à la demande](installation-on-demand.md).
-   Publication de raccourcis vers des fonctionnalités, des applications ou des produits entiers dans l’interface utilisateur. Les utilisateurs peuvent les installer à la demande à l’aide des raccourcis. Les utilisateurs peuvent également supprimer des fonctionnalités, des applications ou des produits entiers à la demande. Pour plus d’informations, consultez [publication](advertisement.md).
-   Personnalisation de l’installation. Un administrateur peut appliquer des transformations à la base de données afin de personnaliser l’installation d’un groupe d’utilisateurs particulier. Pour plus d'informations, consultez [Personnalisation](customization.md).
-   Déploiement plus facile des mises à jour des applications. Utilisez le programme d’installation pour mettre à jour vos produits. Pour plus d’informations, consultez [mise à jour corrective et mises à niveau](patching-and-upgrades.md).
-   Affichage du raccourci de fonctionnalité. Le programme d’installation affiche des raccourcis vers des fonctionnalités qui s’exécutent localement avec des raccourcis vers des fonctionnalités qui s’exécutent à distance. Étant donné que la base de données d’installation spécifie le contexte d’exécution de chaque fonctionnalité, les points d’entrée visibles peuvent être présentés aux utilisateurs en fonction des besoins.
-   Conserver les métriques d’utilisation sur les fonctionnalités. Les développeurs peuvent fournir un package d’installation qui conserve le nombre d’utilisations d’une fonctionnalité par toutes les applications clientes et supprime les composants qui ne sont pas utilisés.
-   Incorporez les installations. Les développeurs peuvent incorporer les fonctionnalités de gestion des composants du programme d’installation dans leurs applications en créant un package d’installation et en utilisant les [fonctions du programme](installer-functions.md) d’installation dans leur code d’application. La figure suivante illustre une application demandant l’installation d’une fonctionnalité.

    ![application demandant l’installation des fonctionnalités. ](images/over1.png)

 

 



