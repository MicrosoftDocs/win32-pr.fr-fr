---
description: Au cœur d’un programme d’installation se trouve l’installation réelle des fichiers.
ms.assetid: e6f6d6a5-bdb0-4866-8d2c-56313d92c94c
title: Règles de contrôle de version des fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67c6f8e59b4f15774f898217690dbb1c4d57b1bf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021743"
---
# <a name="file-versioning-rules"></a>Règles de contrôle de version des fichiers

Au cœur d’un programme d’installation se trouve l’installation réelle des fichiers. Déterminer si un fichier doit être installé est un processus complexe. Au niveau le plus élevé, cette détermination varie selon que le composant auquel appartient un fichier est marqué pour l’installation. Une fois que vous avez déterminé qu’un fichier doit être copié, le processus est compliqué s’il existe un autre fichier portant le même nom dans le dossier cible. Dans ce cas, la détermination requiert un ensemble de règles qui impliquent les propriétés suivantes :

-   Version
-   Date
-   Langage

Le programme d’installation n’utilise ces règles que lors de la tentative d’installation d’un fichier dans un emplacement qui contient déjà un fichier portant le même nom. dans ce cas, le Windows Installer utilise les règles suivantes, toutes autres étant égales, pour déterminer s’il faut installer.

La version la plus élevée gagne, le fichier ayant la version la plus élevée gagne, même si le fichier sur l’ordinateur a la version la plus récente.

Fichiers avec version Win : un fichier avec version est installé sur un fichier qui n’A pas de version.

Privilégier la langue du produit : si le fichier en cours d’installation a une langue différente de celle du fichier sur l’ordinateur, privilégiez le fichier avec la langue qui correspond au produit en cours d’installation. Les fichiers dont la langue est indépendante sont traités comme une autre langue, de sorte que le produit en cours d’installation est privilégié.

Mise en correspondance de plusieurs langues : après avoir pris en compte les langues courantes entre le fichier en cours d’installation et le fichier sur l’ordinateur, toutes les langues restantes sont privilégiées en fonction de ce qui est requis par le produit installé.

Conserver les autres langages : conservez le fichier qui prend en charge plusieurs langues, qu’il soit déjà installé ou non sur l’ordinateur ou qu’il soit en cours d’installation.

Les fichiers sans version sont des données utilisateur : si la date de modification est postérieure à la date de création du fichier sur l’ordinateur, n’installez pas le fichier, car les personnalisations de l’utilisateur sont supprimées. Si les dates de création et de modification sont identiques, installez le fichier. Si la date de création est postérieure à la date de modification, le fichier est considéré comme non modifié, installe le fichier.

L’installation d’un [fichier compagnon](companion-files.md) ne dépend pas de ses propres informations de contrôle de version de fichier, mais du contrôle de version de son parent associé. Dans le cas des fichiers auxiliaires, l’installation est ignorée uniquement si le fichier parent a une version plus récente. Notez qu’un fichier qui est le chemin d’accès de clé de son composant ne doit pas être un fichier associé, car cela entraîne la logique de contrôle de version du fichier de chemin d’accès de clé qui est déterminée par le fichier parent associé.

Fichiers sans version à l’aide des [fichiers d’accompagnement](companion-files.md): un fichier sans version qui est associé à un fichier avec version à l’aide du mécanisme d’accompagnement respecte les règles du fichier avec version. La seule exception est si le fichier avec version sur l’ordinateur et le fichier avec version en cours d’installation ont la même version et la même langue, mais que le fichier associé est manquant sur l’ordinateur. Dans ce cas, le fichier compagnon en cours d’installation est utilisé même si le fichier avec version sur l’ordinateur est utilisé. En outre, un fichier non géré à l’aide d’un fichier auxiliaire est installé si la propriété [**REINSTALLMODE**](reinstallmode.md) comprend les options remplacer les anciennes versions (« o » ou « e ») et que la version du fichier compagnon est égale à un fichier déjà présent sur l’ordinateur.

Les règles sont globales : les règles permettant de déterminer quand installer un fichier se trouvent à un emplacement unique dans le programme d’installation et sont globales, ce qui signifie qu’elles s’appliquent à tous les fichiers de manière égale.

Pour obtenir des exemples du format utilisé pour les versions de fichier, consultez le type de données [version](version.md) . Pour plus d’informations, consultez [remplacement des fichiers existants](replacing-existing-files.md) ou contrôle de [version de fichier par défaut](default-file-versioning.md).

 

 



