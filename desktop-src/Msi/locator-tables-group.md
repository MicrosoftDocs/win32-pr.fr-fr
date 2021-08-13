---
description: Le groupe tables de localisateur est utilisé pour rechercher des fichiers et des applications.
ms.assetid: 44ab770b-1a7f-4590-9681-8f6bd343bf86
title: Groupe de tables de localisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ad0cf5b2d28d01b6e10cf796dc9653c82feb8ffb63adc57c7a7bc244e7ccfcb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118629166"
---
# <a name="locator-tables-group"></a>Groupe de tables de localisateur

Le groupe tables de localisateur est utilisé pour rechercher des fichiers et des applications. Pour rechercher un fichier, commencez par déterminer la signature du fichier, puis recherchez le fichier. Les tables de localisateur permettent d’effectuer des recherches dans le registre, les données de configuration du programme d’installation, l’arborescence des répertoires ou les fichiers de .ini pour la signature unique d’un fichier. La signature de fichier peut ensuite être vérifiée dans la [table de signatures](signature-table.md) pour s’assurer qu’un fichier particulier est bien le fichier recherché et pas un autre fichier portant le même nom. Si un enregistrement d’une table de localisateur ne contient pas de clé dans la table de signature, l’enregistrement fait référence à un répertoire, et non pas à un fichier.

Le composant contrôlant un fichier se trouve dans la [table de fichiers](file-table.md) via la clé externe de la table des [composants](component-table.md). Le programme d’installation résout l’emplacement d’un fichier par le biais de la table des composants, car chaque fichier appartient à un composant. L’emplacement d’un composant se trouve dans la table de [répertoires](directory-table.md)via une clé externe dans la table des composants.

L’emplacement d’une application est trouvé en recherchant des fichiers qui composent l’application. Le programme d’installation fournit également deux tables pour rechercher les versions antérieures d’une application : la [table AppSearch](appsearch-table.md) et la [table CCPSearch](ccpsearch-table.md).

Les tableaux suivants composent le groupe de tables de localisateur et sont utilisés pour déterminer la signature de fichier.

-   La [table RegLocator](reglocator-table.md) contient les informations nécessaires à la recherche d’un fichier ou d’un répertoire dans le registre.
-   La [table IniLocator](inilocator-table.md) contient les informations nécessaires à la recherche d’un fichier .ini. le fichier .ini doit être présent dans le répertoire Microsoft Windows par défaut.
-   La [table CompLocator](complocator-table.md) contient les informations nécessaires à la recherche d’un fichier ou d’un répertoire à l’aide des données de configuration du programme d’installation.
-   La [table DrLocator](drlocator-table.md) contient les informations nécessaires à la recherche d’un fichier ou d’un répertoire dans l’arborescence de répertoires.
-   La [table AppSearch](appsearch-table.md) contient les propriétés qui doivent être définies sur le résultat de la recherche d’une signature de fichier correspondante.
-   La [table CCPSearch](ccpsearch-table.md) contient la liste des signatures de fichiers, au moins l’une d’entre elles devant être présentes sur l’ordinateur d’un utilisateur pour le programme de vérification de la conformité (CCP).

 

 



