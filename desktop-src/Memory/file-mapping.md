---
description: Le mappage de fichier est l’Association du contenu d’un fichier avec une partie de l’espace d’adressage virtuel d’un processus.
ms.assetid: 86a8bc81-914d-46a2-99fd-65dfd03bbcdd
title: Mappage de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7f49162a4545d0e087e6b291e429d89049dbf57
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094153"
---
# <a name="file-mapping"></a>Mappage de fichiers

Le *mappage de fichier* est l’Association du contenu d’un fichier avec une partie de l’espace d’adressage virtuel d’un processus. Le système crée un *objet de mappage de fichier* (également appelé *objet de section*) pour maintenir cette association. Un *affichage des fichiers* est la partie de l’espace d’adressage virtuel utilisée par un processus pour accéder au contenu du fichier. Le mappage de fichiers permet au processus d’utiliser à la fois les entrées et sorties aléatoires (e/s) et les e/s séquentielles. Il permet également au processus de fonctionner efficacement avec un fichier de données volumineux, tel qu’une base de données, sans avoir à mapper l’ensemble du fichier en mémoire. Plusieurs processus peuvent également utiliser des fichiers mappés en mémoire pour partager des données.

Les processus lisent et écrivent dans la vue de fichier à l’aide de pointeurs, exactement comme ils le font avec la mémoire allouée dynamiquement. L’utilisation du mappage de fichiers améliore l’efficacité, car le fichier réside sur le disque, mais la vue de fichier réside en mémoire. Les processus peuvent également manipuler la vue de fichier avec la fonction [**VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect) .

L’illustration suivante montre la relation entre le fichier sur le disque, un objet de mappage de fichier et un affichage des fichiers.

![relation entre le fichier sur le disque, un objet de mappage de fichier et un affichage des fichiers.](images/fmap.png)

Le fichier sur le disque peut être n’importe quel fichier que vous souhaitez mapper en mémoire, ou il peut s’agir du fichier d’échange de pages système. L’objet de mappage de fichier peut être constitué de tout ou partie du fichier. Elle est sauvegardée par le fichier sur le disque. Cela signifie que lorsque le système permute des pages de l’objet de mappage de fichier, toutes les modifications apportées à l’objet de mappage de fichier sont écrites dans le fichier. Lorsque les pages de l’objet de mappage de fichier sont à nouveau échangées, elles sont restaurées à partir du fichier.

Une vue de fichier peut être constituée de tout ou partie de l’objet de mappage de fichier. Un processus manipule le fichier par le biais des vues de fichiers. Un processus peut créer plusieurs vues pour un objet de mappage de fichier. Les vues de fichiers créées par chaque processus résident dans l’espace d’adressage virtuel de ce processus. Quand le processus a besoin de données provenant d’une partie du fichier autre que celle de l’affichage des fichiers en cours, il peut annuler le mappage de l’affichage des fichiers en cours, puis créer une nouvelle vue de fichier.

Lorsque plusieurs processus utilisent le même objet de mappage de fichier pour créer des vues pour un fichier local, les données sont cohérentes. Autrement dit, les vues contiennent des copies identiques du fichier sur le disque. Le fichier ne peut pas résider sur un ordinateur distant si vous souhaitez partager la mémoire entre plusieurs processus.

Pour plus d'informations, voir les rubriques suivantes :

-   [Création d’un objet de mappage de fichier](creating-a-file-mapping-object.md)
-   [Création d’un affichage des fichiers](creating-a-file-view.md)
-   [Partage de fichiers et de mémoire](sharing-files-and-memory.md)
-   [Lecture et écriture à partir d’un affichage des fichiers](reading-and-writing-from-a-file-view.md)
-   [Fermeture d’un objet de mappage de fichier](closing-a-file-mapping-object.md)
-   [Sécurité du mappage de fichiers et droits d’accès](file-mapping-security-and-access-rights.md)
-   [Utilisation du mappage de fichiers](using-file-mapping.md)

 

 
