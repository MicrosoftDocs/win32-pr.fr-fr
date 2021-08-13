---
description: un package d’installation contient toutes les informations dont l’Windows Installer a besoin pour installer ou désinstaller une application ou un produit et pour exécuter l’interface utilisateur du programme d’installation.
ms.assetid: 532b3492-919f-4999-b86c-e3c210876141
title: Package d'installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61daf878a7933353382a52acd9a7172e87b97b14cdf41a047279360342ca768b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118633819"
---
# <a name="installation-package"></a>Package d'installation

un package d’installation contient toutes les informations dont l’Windows Installer a besoin pour installer ou désinstaller une application ou un produit et pour exécuter l’interface utilisateur du programme d’installation. Chaque package d’installation comprend un fichier .msi, contenant une base de données d’installation, un flux d’informations de synthèse et des flux de données pour différentes parties de l’installation. Le fichier .msi peut également contenir une ou plusieurs transformations, des fichiers sources internes, des fichiers sources externes ou des fichiers CAB requis par l’installation.

Les développeurs d’applications doivent créer une installation pour utiliser le programme d’installation. Étant donné que le programme d’installation organise les installations autour du concept de [composants et de fonctionnalités](components-and-features.md), et stocke toutes les informations relatives à l’installation dans une base de données relationnelle, le processus de création d’un package d’installation implique une large part des étapes suivantes :

-   Identifiez les fonctionnalités à présenter aux utilisateurs.
-   Organisez l’application en composants.
-   Remplissez la base de données d’installation avec les informations.
-   Validez le package d’installation.

La section suivante décrit les composants et les fonctionnalités du programme d’installation. Pour plus d’informations, consultez [composants et fonctionnalités](components-and-features.md). Le choix des fonctionnalités est généralement déterminé par les fonctionnalités de l’application du point de vue de l’utilisateur.

Il est recommandé que les développeurs utilisent une procédure standard pour choisir des composants. Pour plus d’informations, consultez [Organisation des applications dans des composants](organizing-applications-into-components.md).

les auteurs de package peuvent utiliser des outils de création de packages tiers, ou un éditeur de table et le kit de développement logiciel (SDK) Windows Installer, pour remplir la base de données d’installation. Tous les packages d’installation doivent être validés pour assurer la cohérence interne. Pour plus d’informations, consultez [validation de package](package-validation.md).

 

 



