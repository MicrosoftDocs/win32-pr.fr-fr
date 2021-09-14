---
title: L’évolution des systèmes de fichiers
description: Avant le développement des ordinateurs pour fonctionner sur les systèmes d’exploitation de disque, chaque ordinateur a été conçu pour exécuter une seule application propriétaire, qui avait un contrôle complet et exclusif de l’ordinateur entier.
ms.assetid: 46d497b5-c325-4395-8512-1ed4b88441de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dc34dc699488b5952d52dfd13f49ea63aaa85aa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127237246"
---
# <a name="the-evolution-of-file-systems"></a>L’évolution des systèmes de fichiers

Avant le développement des ordinateurs pour fonctionner sur les systèmes d’exploitation de disque, chaque ordinateur a été conçu pour exécuter une seule application propriétaire, qui avait un contrôle complet et exclusif de l’ordinateur entier. L’application écrira ses données persistantes directement sur un disque, ou un tambour, en envoyant directement des commandes au contrôleur de disque. L’application était responsable de la gestion des emplacements absolus de données sur le disque, en veillant à ce qu’elle ne remplace pas les données déjà existantes. Étant donné qu’une seule application était en cours d’exécution sur l’ordinateur à tout moment, cette tâche était trop difficile.

L’avènement des systèmes informatiques qui pouvaient exécuter plusieurs applications nécessitait un mécanisme pour s’assurer que les applications n’écrivaient pas les données de l’autre. Les développeurs d’applications ont résolu ce problème en adoptant une norme unique pour distinguer les secteurs de disque utilisés de ceux qui étaient libres en les marquant en conséquence. Dans le temps, ces normes sont fusionnées pour devenir un système d’exploitation de disque, qui fournissait différents services aux applications, y compris un système de fichiers pour la gestion du stockage persistant. Avec l’avènement d’un système de fichiers, les applications n’ont plus à traiter directement le support de stockage physique. Au lieu de cela, ils ont simplement indiqué au système de fichiers d’écrire des blocs de données sur le disque et de faire en sorte que le système de fichiers se soucie de la façon de le faire. En outre, le système de fichiers permettait aux applications de créer des hiérarchies de données par le biais d’une abstraction connue sous le nom d’annuaire. Un répertoire peut contenir non seulement des fichiers, mais aussi d’autres répertoires, qui peuvent à leur tour contenir leurs propres fichiers et répertoires, et ainsi de suite.

Le système de fichiers a fourni un seul niveau d’indirection entre les applications et le disque, et le résultat était que chaque application a vu un fichier comme un flux contigu unique d’octets sur le disque, même si le système de fichiers stockait effectivement le fichier dans des secteurs non contigus. L’indirection a libéré aux applications d’avoir à effectuer le suivi de la position absolue des données sur un périphérique de stockage.

Aujourd’hui, presque toutes les API système pour les entrées et sorties de fichier fournissent des applications pour l’écriture d’informations dans un fichier plat. Les applications voient ce fichier sous la forme d’un flux d’octets unique qui peut croître jusqu’à ce que le disque soit plein. Pendant longtemps, ces API sont suffisantes pour permettre aux applications de stocker leurs informations persistantes. Les applications ont fait des innovations importantes quant à la façon dont elles gèrent un seul flux d’informations pour fournir des fonctionnalités telles que des enregistrements incrémentiels « rapides ».

Toutefois, dans un monde d’objets de composant, le stockage de données dans un seul fichier plat n’est plus efficace. Tout comme les systèmes de fichiers n’ont pas été en mesure de partager le même support de stockage, les objets de composants nécessitent donc un système qui leur permet de partager le stockage au sein de l’infrastructure conceptuelle d’un fichier unique. Même s’il est possible de stocker des objets distincts à l’aide du stockage de fichiers plats conventionnels, si la taille de l’un des objets augmente, ou si vous ajoutez simplement un autre objet, il est nécessaire de charger l’intégralité du fichier en mémoire, d’insérer le nouvel objet, puis d’enregistrer l’intégralité du fichier. Ce processus peut être très long.

La solution fournie par COM consiste à implémenter un deuxième niveau d’indirection : un système de fichiers dans un fichier. Le stockage de fichiers plats exige qu’une grande séquence contiguë d’octets sur le disque soit manipulée par le biais d’un seul descripteur de fichier avec un seul pointeur de recherche. En revanche, le stockage structuré COM définit comment traiter une entité de système de fichiers unique comme une collection structurée de deux types d’objets (stockages et flux) qui agissent comme des répertoires et des fichiers.

 

 




