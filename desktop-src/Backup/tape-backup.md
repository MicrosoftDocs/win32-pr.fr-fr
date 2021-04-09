---
title: Sauvegarde sur bande
description: Un volume de bande se compose d’un support d’enregistrement et de son opérateur physique. Chaque volume de bande possède une ou plusieurs partitions. Les partitions sont généralement divisées en sections par des marques de setmarks. Il existe trois types de marques de marques.
ms.assetid: 2057e6e4-b674-4151-b3b6-bde5d87d10c1
keywords:
- sauvegarde de sauvegarde, bande
- Sauvegarde sur bande
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2820e512646642046059cb151061e3f605d56cd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028752"
---
# <a name="tape-backup"></a>Sauvegarde sur bande

Un *volume de bande* se compose d’un support d’enregistrement et de son opérateur physique. La longueur totale de la bande dans un volume n’est pas disponible pour l’enregistrement des données. Des sections courtes au début et à la fin de la bande sont réservées à l’attachement de la bande aux hubs du transporteur. La première position sur la bande où les données peuvent être enregistrées est le *marqueur de début de support*, et la dernière position est appelée *marqueur de fin de support*.

Chaque volume de bande possède une ou plusieurs partitions. Une partition est une partie du volume, contenant ses propres points de début et de fin, qui ne se chevauchent pas avec une autre partie du volume. Chaque partition comporte trois positions prédéfinies. La première position dans une partition où vous pouvez enregistrer des données est appelée *marqueur de début de partition* et le dernier est appelé *marqueur de fin de partition*. Le *marqueur d’avertissement anticipé* est situé juste avant le marqueur de fin de partition. La position d’avertissement précoce indique aux applications sur bande de transférer les données mises en mémoire tampon sur la bande avant d’atteindre le marqueur de fin de partition.

La zone entre les points de début et de fin d’une partition est généralement divisée en sections par des *marques* de *setmarks*. Les marques et les setmarks sont des éléments enregistrés spéciaux qui ne contiennent pas de données utilisateur ; Ils divisent simplement la partition en zones plus petites pour fournir un schéma d’adresse. Les marques de setmarks et les points de vue sont similaires, mais setmarks fournissent un positionnement plus rapide sur les lecteurs de bande haute capacité.

En règle générale, les périphériques à bandes prennent en charge les marques et les setmarks. La prise en charge des deux permet la mise en forme des données sur bande, de telle sorte que setmarks des données distinctes des différents volumes de disque et des marques de données séparent les données des fichiers individuels sur un volume de disque.

Un autre élément enregistré qui désigne les emplacements sur la bande est un *écart d’effacement*, une zone de bande effacée ou un motif que l’appareil ne reconnaît pas comme une marque ou des données utilisateur.

Il existe trois types de marques de marques. Une *petite* marque de service contient un écart d’effacement bref qui ne peut pas être remplacé à moins que l’opération d’écriture soit effectuée depuis le début de la partition ou à partir d’une marque de service longue antérieure. Une rencontre *longue* contient un écart d’effacement long qui permet à une application de positionner la bande au début de la marque de fin et de remplacer la marque de fin et l’écart d’effacement. Une marque de rencontre *normale* ne contient pas d’écart d’effacement. Les périphériques à bandes qui utilisent des marques de service prennent en charge des marques courtes et longues ou des marques de caractères ordinaires, mais pas les trois.

La zone sur une partition entre les setmarks ou les marques est disponible pour l’enregistrement des données. Une unité de données écrites ou lues à partir d’une bande est appelée un bloc.

Pour plus d'informations, voir les rubriques suivantes :

-   [Initialisation de la bande](tape-initialization.md)
-   [Entrée et sortie sur bande](tape-input-and-output.md)
-   [Création d’une application de sauvegarde](creating-a-backup-application.md)
-   [Sauvegarde et restauration des liens physiques](backing-up-and-restoring-hard-links.md)

 

 




