---
title: Formats de disque
description: 'IMAPi prend en charge trois formats de système de fichiers : ISO 9660, Joliet et UDF.'
ms.assetid: 9cd782c0-203b-452c-9d04-3464d39453b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af71733ec2747ae227ac412a7b49f0faa73639cf1000f1332db5ec1d1d55db9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118758601"
---
# <a name="disc-formats"></a>Formats de disque

IMAPi prend en charge trois formats de système de fichiers : [ISO 9660](#iso-9660), [Joliet](#joliet)et [UDF](#universal-disk-format-udf).

## <a name="iso-9660"></a>ISO 9660

Le format ISO 9660 est le système de fichiers standard d’origine pour les disques de données de CD. le format est reconnu sur plusieurs systèmes d’exploitation, notamment MSDOS, le Mac OS, UNIX et le système d’exploitation Windows. Le format ISO 9660 est publié par le Organisation internationale de normalisation (ISO).

Le format commence au secteur 16 avec l’en-tête volume, CD0001 ; le reste de l’en-tête suit. D’autres formats dérivés commencent également au secteur 16, mais utilisent une autre chaîne pour l’en-tête du volume. Par exemple, les disques High Sierra utilisent la chaîne CD-ROM0001 et le format interactif du CD Compact utilise CD-I0001.

L’en-tête pointe vers les zones du disque qui stockent les noms de fichiers au format ISO 9660. La Convention d’affectation de noms de fichiers et de répertoires se compose de 8 caractères, un point et 3 caractères supplémentaires. Il s’agit de la même convention d’affectation de noms que celle utilisée par le système d’exploitation MSDOS.

Des en-têtes de système de fichiers supplémentaires, pour les formats tels que Joliet et UDF, peuvent coexister sur un disque sans affecter la lisibilité du format ISO 9660. Après les index, un ensemble de fichiers de données occupe le disque. Les index de chaque système de fichiers référencent indépendamment les fichiers de données sur le disque.

La spécification ISO 9660 définit trois niveaux de format :

-   Le niveau 1 définit des noms de fichiers pour utiliser le format de caractère 8,3.
-   le niveau 2 autorise des noms de fichiers plus longs, tels qu’ils figurent sur les plateformes DOS 6. xx, MacIntosh et UNIX.
-   Le niveau 3 permet d’améliorer les performances de récupération (lecture) des données et des fichiers audio entrelacés. Ce niveau supprime également la limite de 2 Go de fichiers. Ce niveau n’est **pas** pris en charge par l’API de mastérisation d’image.

Les disques DVD peuvent également utiliser ISO 9660 ; Toutefois, le système de fichiers UDF est le système de fichiers le plus répandu utilisé avec les supports DVD.

## <a name="joliet"></a>Joliet

Le format Joliet est une dérivée de la norme ISO 9660. Ce format écrit l’index du système de fichiers Joliet sur l’image disque en plus de l’index du système de fichiers ISO 9660.

L’index Joliet offre les améliorations suivantes à l’index du système de fichiers :

-   Reconnaît les noms de fichiers longs jusqu’à 32 caractères.
-   Distingue les lettres majuscules et minuscules dans les noms de fichiers.
-   Prend en charge les caractères Unicode dans le nom de fichier.

L’en-tête de format Joliet commence au secteur 17 du disque.

Étant donné que le format Joliet conserve le système de fichiers ISO 9660 sur un disque, la compatibilité avec les appareils conformes ISO 9660 est conservée.

## <a name="universal-disk-format-udf"></a>Format UDF (Universal Disk Format)

le Format UDF (Universal Disk Format) est un système de fichiers plus récent développé pour le support optique par l’Association de technologie OSTA (optical Stockage Technology Association). UDF est un format portable reconnu par plusieurs systèmes d’exploitation. UDF remplace ISO 9660 comme nouveau standard, en particulier avec les supports de lecture/écriture.

Les fonctionnalités UDF sont les suivantes :

-   Prend en charge une taille maximale de 2 to.
-   Prend en charge les disques Flash Media, Iomega REV et CD-MRW.
-   Stocke des fichiers d’une longueur inférieure à 2 Ko dans le bloc d’entrée de fichier.
-   Prend en charge des fichiers d’une longueur maximale de 2 to avec des noms de fichiers tant que 255 caractères.
-   Prend en charge un ensemble complet d’attributs de fichier adaptés à différents systèmes d’exploitation.
-   Prend en charge un format de pont où les formats ISO 9660, Joliet et UDF résident tous sur le même disque. Cela est utilisé dans les applications vidéo, telles que DVD-Video, DVD + VR et DVD-VR.
-   Prend en charge les flux nommés et les fichiers « en temps réel ».

 

 




