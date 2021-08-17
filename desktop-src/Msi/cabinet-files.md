---
description: Un fichier cab est un fichier unique, généralement avec une extension de .cab, qui stocke les fichiers compressés dans une bibliothèque de fichiers.
ms.assetid: df240302-b875-49bf-8e62-7a35204c35fb
title: Fichiers CAB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2331b60c42bf975856987d1e13d67c95bc01fa685f99f49543650c48347cac49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118380716"
---
# <a name="cabinet-files"></a>Fichiers CAB

Un fichier cab est un fichier unique, généralement avec une extension de .cab, qui stocke les fichiers compressés dans une bibliothèque de fichiers. Le format cab est un moyen efficace d’empaqueter plusieurs fichiers, car la compression est effectuée à travers les limites de fichiers, ce qui améliore considérablement le taux de compression.

Les développeurs peuvent utiliser un outil de création de fichier CAB comme Makecab.exe pour créer des fichiers CAB à utiliser avec des packages d’installation. l’utilitaire Makecab.exe est inclus dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md).

Les développeurs peuvent également utiliser un outil de création de fichier CAB comme Cabarc.exe pour créer des fichiers CAB à utiliser avec des packages d’installation. Cet outil écrit dans la structure de l’armoire Diamond.

Les clés de fichier des fichiers stockés dans un fichier cab doivent correspondre à celles de la colonne file de la [table file](file-table.md) et la séquence de fichiers dans le fichier cab doit correspondre à la séquence de fichiers spécifiée dans la colonne Sequence. Pour plus d’informations, consultez [utilisation d’armoires et de sources compressées](using-cabinets-and-compressed-sources.md).

Les fichiers volumineux peuvent être fractionnés entre deux fichiers CAB ou plus. Il ne peut pas y avoir plus de 15 fichiers dans un fichier CAB qui s’étend au fichier CAB suivant. Par exemple, si vous avez trois fichiers CAB, le premier fichier CAB peut avoir 15 fichiers qui s’étendent au deuxième fichier CAB et le second peut avoir 15 fichiers qui s’étendent au troisième fichier CAB.

Le programme d’installation extrait les fichiers d’un fichier CAB lorsqu’ils sont nécessaires à l’installation et les installe dans le même ordre que celui dans lequel ils sont stockés dans le fichier CAB. L’espace requis pour l’installation d’un fichier stocké dans un fichier CAB n’est pas différent de celui de l’installation d’un fichier non compressé.

Un fichier CAB peut se trouver à l’intérieur ou à l’extérieur du fichier .msi. à compter de Windows Installer 5,0 s’exécutant sur Windows 7 ou Windows Server 2008 R2, le programme d’installation enregistre les armoires incorporées dans le fichier .msi avant la mise en cache du package d’installation.

**[Windows Installer 4,5 ou version antérieure](not-supported-in-windows-installer-4-5.md):** Pour économiser de l’espace disque, le programme d’installation supprime toujours toutes les armoires incorporées dans le fichier .msi avant la mise en cache du package d’installation sur l’ordinateur de l’utilisateur.

 

 



