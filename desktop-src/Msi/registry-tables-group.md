---
description: Le groupe de registres de Windows Installer tables contient des informations sur les entrées de registre.
ms.assetid: 31a75c20-79e4-4bcf-bcc1-34a7d191fa90
title: Groupe de tables de Registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8ba14bdc2bc5668ce2de3ec66172c75c176ab41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864837"
---
# <a name="registry-tables-group"></a>Groupe de tables de Registre

![Groupe de tables de Registre](images/registry.png)

Pour plus d’informations sur ce diagramme, consultez la [légende diagramme de relation d’entité](entity-relationship-diagram-legend.md).

Le programme d’installation a des tables spécifiques pour les différents types d’entrées de registre. Lors du remplissage du groupe de tables de Registre, il est important d’essayer de réduire le nombre d’entrées placées dans la [table de Registre](registry-table.md) et d’optimiser l’utilisation des autres tables de Registre spécifiques. Cela est dû au fait que le programme d’installation ne peut pas faire la distinction entre les différents types d’entrées de Registre dans la table du Registre et ne peut pas utiliser la logique interne nécessaire pour tirer pleinement parti de toutes les fonctionnalités du programme d’installation, telles que la [*publication*](a-gly.md). La création d’entrées de Registre liées à COM et à l’interpréteur de commandes permet également d’obtenir une organisation plus logique et peut aider à minimiser l’inscription erronée des informations du serveur COM.

La figure illustre le groupe d’entrées de registre des tables ainsi que la table des [composants](component-table.md), la [table des fonctionnalités](feature-table.md)et la [table des fichiers](file-table.md). Bien que ces derniers ne soient pas directement impliqués dans le remplissage du Registre, ils sont inclus dans la figure car ils sont essentiels à la logique du groupe d’entrées du Registre.

Le groupe d’entrées de registre contient les tables suivantes d’entrées de Registre spécifiques.

-   La [table d’extension](extension-table.md) contient toutes les extensions de nom de fichier utilisées par votre application, ainsi que les fonctionnalités et composants associés.
-   La [table de verbes](verb-table.md) associe les informations de verbe de commande aux extensions de nom de fichier figurant dans la [table d’extension](extension-table.md). Cela fournit un lien indirect entre le verbe et la table de fonctionnalités requis pour la publication de fonctionnalités.
-   La [table Typelib](typelib-table.md) fournit des informations que le programme d’installation place dans le registre pour l’inscription des bibliothèques de types. Les entrées de la bibliothèque de types ne sont pas écrites au moment de la publication. Le programme d’installation écrit les entrées de la bibliothèque de types au moment de l’installation des composants associés à la bibliothèque.
-   La [table MIME](mime-table.md) associe un type de contexte MIME à un CLSID ou à une extension de nom de fichier. Cela fournit un chemin d’accès entre le MIME et le tableau de fonctionnalités requis pour la publication de fonctionnalités.
-   La [table Selfreg](selfreg-table.md) fournit les informations nécessaires pour auto-inscrire les modules. L’inscription automatique est fournie par le programme d’installation uniquement pour la compatibilité descendante et n’est pas recommandée comme méthode de remplissage du Registre. Toutefois, si des modules de votre application doivent s’inscrire eux-mêmes, utilisez la table SelfReg.
-   La [table de classe](class-table.md) est utilisée pour inscrire des ID de classe et d’autres informations pour les objets com. Ce tableau contient des informations relatives au serveur COM qui doivent être générées dans le cadre de la publication du produit.
-   La [table ProgID](progid-table.md) associe les ID de programme aux ID de classe.
-   La [table AppID](appid-table.md) est utilisée pour enregistrer les paramètres de configuration et de sécurité courants pour les objets DCOM.
-   La [table d’environnement](environment-table.md) est utilisée pour définir les valeurs des variables d’environnement, et dans Windows 2000, la table d’environnement écrit également dans le registre.
-   La [table de Registre](registry-table.md) contient toutes les autres informations que l’application doit placer dans le registre système. Cela inclut les paramètres par défaut, les informations utilisateur ou les données, ou l’inscription COM non prise en charge par les tables ci-dessus.
-   La [table RemoveRegistry](removeregistry-table.md) contient les informations de registre que l’application doit supprimer du Registre système au moment de l’installation.

 

 



