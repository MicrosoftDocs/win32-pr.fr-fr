---
description: Les modules de fusion offrent une méthode standard par laquelle les développeurs fournissent des composants de Windows Installer partagés et une logique de configuration à leurs applications.
ms.assetid: 673de3ff-e58c-4153-9c8d-c3baebba5eb1
title: Modules de fusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3499368b309909bcb06da45476d43d8cac28e205
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210592"
---
# <a name="merge-modules"></a>Modules de fusion

Les modules de fusion offrent une méthode standard par laquelle les développeurs fournissent des [*composants*](c-gly.md) de Windows Installer partagés et une logique de configuration à leurs applications. Les modules de fusion sont utilisés pour distribuer du code partagé, des fichiers, des ressources, des entrées de Registre et une logique de configuration aux applications sous la forme d’un fichier composé unique. Les développeurs qui créent de nouveaux modules de fusion ou qui utilisent des modules de fusion existants doivent suivre la norme décrite dans cette section.

Un module de fusion est de structure similaire à un [*fichier Windows Installer. msi*](m-gly.md)simplifié. Toutefois, un module de fusion ne peut pas être installé seul, il doit être fusionné dans un package d’installation à l’aide d’un outil de fusion. Les développeurs souhaitant utiliser des modules de fusion doivent obtenir l’un des outils de fusion distribués librement, tels que Mergemod.dll, ou acheter un outil de fusion auprès d’un éditeur de logiciels indépendant. Les développeurs peuvent créer des modules de fusion à l’aide de nombreux outils logiciels utilisés pour créer un package d’installation Windows Installer, tel que l’éditeur de table de base de données Orca fourni avec le kit de développement logiciel (SDK) Windows Installer.

Lorsqu’un module de fusion est fusionné dans le fichier. msi d’une application, toutes les informations et ressources nécessaires à l’installation des composants fournis par le module de fusion sont incorporées dans le fichier. msi de l’application. Le module de fusion n’est alors plus nécessaire pour installer ces composants et le module de fusion n’a pas besoin d’être accessible à un utilisateur. Étant donné que toutes les informations nécessaires pour installer les composants sont fournies sous la forme d’un fichier unique, l’utilisation de modules de fusion peut éliminer de nombreuses instances de conflits de version, des entrées de Registre manquantes et des fichiers installés de manière incorrecte.

Pour plus d’informations sur les modules de fusion, consultez :

-   [À propos des modules de fusion](about-merge-modules.md)
-   [Utilisation de modules de fusion](using-merge-modules.md)
-   [Référence de module de fusion](merge-module-reference.md)

 

 



