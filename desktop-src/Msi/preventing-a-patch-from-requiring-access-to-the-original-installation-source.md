---
description: Il n’est pas possible d’éliminer toutes les circonstances dans lesquelles l’application d’un correctif peut nécessiter l’accès à la source d’installation d’origine.
ms.assetid: f7028c55-e4a5-4596-af7a-728c9f4f367e
title: Empêcher un correctif d’avoir accès à la source d’installation d’origine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baee8b261ff0a3f6bb94fb141ee765726ffa2ced
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864386"
---
# <a name="preventing-a-patch-from-requiring-access-to-the-original-installation-source"></a>Empêcher un correctif d’avoir accès à la source d’installation d’origine

Il n’est pas possible d’éliminer toutes les circonstances dans lesquelles l’application d’un correctif peut nécessiter l’accès à la source d’installation d’origine.

Respectez les points suivants pour réduire la possibilité que votre correctif nécessite l’accès à la source d’origine :

-   Utilisez uniquement des correctifs de fichiers complets. Cela élimine la nécessité de créer des correctifs binaires pour toutes les versions antérieures du fichier. Notez que les correctifs de fichiers entiers ont généralement une taille supérieure à celle des correctifs binaires. Vous pouvez facilement définir un patch en tant que correctif de fichier complet en créant la propriété IncludeWholeFilesOnly avec la valeur 1 (un) dans le fichier des propriétés de création de correctif (PCP).
-   Assurez-vous qu’aucune de vos actions personnalisées n’accède à l’emplacement source d’origine.
-   Assurez-vous que l’action ResolveSource est soumise à une condition de manière à ce qu’elle s’exécute uniquement si nécessaire ou qu’elle n’est pas présente du tout.
-   Remplissez la [table MsiFileHash](msifilehash-table.md) pour tous les fichiers dont la version n’est pas distante. L’outil du kit de développement logiciel (SDK) Windows Installer, Msifiler.exe, peut facilement le faire pour vous.
-   Vérifiez que les informations de version et de langue de tous les fichiers sont correctes. L’outil du kit de développement logiciel (SDK) Windows Installer, Msifiler.exe, peut facilement le faire pour vous.

## <a name="source-requirements-when-patching"></a>Configuration requise pour la mise à jour corrective

L’accès aux sources d’installation d’origine peut être nécessaire pour appliquer le correctif dans les cas suivants :

-   Le correctif s’applique à une fonctionnalité qui est actuellement exécutée à partir de la source. Dans ce cas, la fonctionnalité passe de l’état d’exécution à partir de la source à l’état local.
-   Le correctif s’applique à un composant pour lequel un fichier est manquant ou endommagé.
-   Le correctif s’applique à un fichier dans un composant qui contient également des fichiers sans version sans aucune entrée MsiFileHash. Une [table MsiFileHash](msifilehash-table.md) remplie est requise pour empêcher la recopie inutile de fichiers non distants à partir de l’emplacement source.
-   Le correctif a été appliqué avec un REINSTALLMODE de amuser ou d’Emu. Cette option est dangereuse en ce qu’elle effectue des opérations de copie de fichiers, quelle que soit la version du fichier. Cela peut entraîner un reving des fichiers et nécessite presque toujours la source. La valeur REINSTALLMODE recommandée est omus.
-   Le package mis en cache pour le produit est manquant. Le package mis en cache est nécessaire pour l’application d’un correctif. Le package mis en cache est stocké dans le dossier% windir% \\ installer.
-   Le package est créé pour appeler l' [action ResolveSource](resolvesource-action.md). En général, cette action doit être évitée ou conditionnellement, car son exécution donne toujours accès à la source.
-   Le package a une action personnalisée qui tente d’accéder à la source d’une certaine manière. L’exemple le plus courant est une action personnalisée d’installation simultanée de type 23.
    > [!Note]  
    > Les installations simultanées ne sont pas recommandées pour l’installation d’applications destinées à être communiquées au public. Pour plus d’informations sur les installations simultanées, consultez [installations simultanées](concurrent-installations.md).

     

-   Le package de correctifs se compose de correctifs binaires qui ne s’appliquent pas à la version actuelle du fichier sur l’ordinateur.

Prenons l’exemple suivant, dans lequel Windows Installer nécessite l’accès à la source d’origine lors de l’application d’un correctif :

1.  Installez la version RTM de l’exemple de produit.
2.  Appliquez le correctif Qfe1. msp à l’ordinateur. Cette version de patch 1,0 de Example.dll à la version 1,1.
3.  Un nouveau correctif, Qfe2. msp, est fourni, qui met à jour Example.dll vers la version 1,2 et obsolètes Qfe1. msp. Toutefois, le correctif a été créé uniquement pour cibler la version 1,0 de Example.dll, car il a été généré à l’aide de la version RTM du produit. Example.dll version 1,2 comprend le correctif contenu dans Example.dll version 1,1, mais le fichier. msp a été généré entre les images RTM et QFE2. Ainsi, quand Qfe2. msp est appliqué à l’ordinateur, Windows Installer doit accéder à la source d’origine. Le correctif binaire pour Example.dll ne peut pas s’appliquer à la version 1,1 ; elle ne peut s’appliquer qu’à la version 1,0. Ainsi, le programme d’installation recopie la version 1,0 de Example.dll à partir de l’emplacement source d’origine afin que le correctif puisse être appliqué avec succès.

## <a name="source-requirements-when-removing-a-patch"></a>Spécifications de la source lors de la suppression d’un correctif

L’accès aux sources d’installation d’origine peut être nécessaire pour supprimer un correctif si le Windows Installer n’a pas stocké les informations de référence sur le correctif. À partir de Windows Installer 3,0, le programme d’installation enregistre de manière sélective les informations de référence sur les fichiers lorsqu’ils sont mis à jour. Pour plus d’informations sur le cache de base, consultez réduction de la [taille des correctifs](reducing-patch-size.md) .

 

 



