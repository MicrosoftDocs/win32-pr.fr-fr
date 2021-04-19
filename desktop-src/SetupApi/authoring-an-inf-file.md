---
description: Lors de la création d’un fichier INF pour une application d’installation, vous devez également vous reporter au format de fichier INF documenté dans instructions générales pour les fichiers INF et les sections et directives du fichier INF du kit de développement de pilotes Microsoft Windows 2000.
ms.assetid: f9df95bb-345d-4a70-a27e-0b1bc2a27ada
title: Création d’un fichier INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73807f919a016f414a248f47e53f27d5b079bb33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517253"
---
# <a name="authoring-an-inf-file"></a>Création d’un fichier INF

Lors de la création d’un fichier INF pour une application d’installation, vous devez également vous reporter au format de fichier INF documenté dans *instructions générales pour les fichiers INF* et les *sections et directives du fichier* INF du kit de développement de pilotes Microsoft Windows 2000.

Lors de la création de fichiers INF pour une application d’installation, respectez les règles suivantes.

-   Une section **version** est requise dans chaque fichier INF.
-   Les sections doivent commencer par le nom de la section entre crochets ( \[ \] ).
-   Les noms des sections **DestinationDirs**, **SourceDisksFiles**, **SourceDisksNames**, **Strings** et **version** doivent être identiques au type de section. Par exemple \[ , utilisez DestinationDirs \] . Les auteurs peuvent spécifier les noms d’autres types de sections.
-   Les noms des sections **SourceDisksNames** et **SourceDisksFiles** peuvent être ajoutés avec un suffixe spécifique à la plateforme. Par exemple, pour afficher une section **SourceDisksNames** spécifique à Intel, utilisez \[ SourceDisksNames. x86 \] . Si les fonctions d’installation recherchent des sections **SourceDisksNames** et **SourceDisksFiles** spécifiques à la plateforme correspondant à la plate-forme de l’utilisateur, les fonctions utilisent les sections spécifiques à la plateforme. Dans le cas contraire, les fonctions d’installation utilisent les sections **SourceDisksNames** et **SourceDisksFiles** sans suffixe. Les fonctions d’installation peuvent déterminer par programme le système de l’utilisateur. Consultez l' [exemple de sections INF SourceDisksNames et SourceDisksFiles](inf-sourcedisksnames-and-sourcedisksfiles-sections-example.md).
-   Les valeurs peuvent être exprimées sous forme de chaînes remplaçables au format%*strKey*%. Pour utiliser un caractère% dans la chaîne, utilisez%%. StrKey doit être défini dans une section **Strings** du fichier INF.

 

 



