---
description: Normalement, les informations de débogage sont stockées dans un fichier de symboles distinct de l’exécutable.
ms.assetid: 610e5cd3-9dc3-462c-98f8-6a63874464f8
title: Fichiers de symboles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 610e289a64ed807a26086f12780b45bc35ea65464946ec81a07e4169515d1132
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642179"
---
# <a name="symbol-files"></a>Fichiers de symboles

Normalement, les informations de débogage sont stockées dans un fichier de symboles distinct de l’exécutable. L’implémentation de ces informations de débogage a changé au cours des années, et la documentation suivante fournit des conseils sur ces différentes implémentations.

## <a name="pdb-files"></a>fichiers PDB

Toutes les versions modernes des compilateurs Microsoft stockent les informations de débogage relatives à un exécutable compilé dans un fichier *de base de données du programme* (. pdb) distinct. Ce fichier est communément appelé *PDB*. Les données sont stockées dans un fichier distinct de l’exécutable pour limiter la taille de l’exécutable, ce qui permet d’économiser de l’espace de stockage sur disque et de réduire le temps nécessaire au chargement des données. Cette méthode permet également de distribuer l’exécutable sans divulguer ces informations importantes, ce qui peut rendre le programme plus facile à rétroconcevoir.

Pour créer un fichier PDB, générez votre fichier exécutable avec des informations de débogage en fonction des instructions de vos outils de génération.

L’API DbgHelp peut utiliser des fichiers PDB pour obtenir les informations suivantes.

-   public et exportations
-   symboles globaux
-   symboles locaux
-   données de type
-   fichiers sources
-   numéros de ligne

## <a name="dbg-files-and-embedded-debug-information"></a>Fichiers DBG et informations de débogage incorporés

Les versions précédentes de l’ensemble d’outils Microsoft utilisaient pour incorporer les informations de débogage dans le fichier exécutable, mais il serait normalement éliminé dans un fichier distinct avec une extension. dbg. C’est ce qu’on appelle communément un fichier *dbg* . Les fichiers DBG utilisent le même format de fichier PE que les exécutables.

La prise en charge de l’API DbgHelp pour DBGs et les informations de débogage intégrées est limitée et comprend les éléments suivants.

-   public et exportations
-   symboles globaux

 

 



