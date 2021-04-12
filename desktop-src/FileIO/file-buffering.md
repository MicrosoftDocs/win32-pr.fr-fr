---
description: Décrit les éléments à prendre en considération pour le contrôle d’application de la mise en mémoire tampon des fichiers, également appelée entrée/sortie (e/s) de fichiers non mis en mémoire tampon.
ms.assetid: ae1e5d0f-9b55-4aae-8402-b9c8e33d9363
title: Mise en mémoire tampon du fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a44f6724622b2c3116fa24a6109efb6c0d9f1d9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210262"
---
# <a name="file-buffering"></a>Mise en mémoire tampon du fichier

Cette rubrique couvre les différents éléments à prendre en considération pour le contrôle d’application de la mise en mémoire tampon des fichiers, également appelée entrée/sortie de fichier non mis en mémoire tampon. La mise en mémoire tampon des fichiers est généralement gérée par le système en arrière-plan et est considérée comme faisant partie de la [mise en cache des fichiers](file-caching.md) au sein du système d’exploitation Windows, sauf indication contraire. Bien que les conditions de *mise en cache* et de mise en *mémoire tampon* soient parfois utilisées de manière interchangeable, cette rubrique utilise le terme de *mise en mémoire tampon* , spécifiquement dans le contexte de l’interaction avec les données qui ne sont pas mises en cache (mises en mémoire tampon) par le système, dans le cas contraire du contrôle direct des applications en mode utilisateur.

Lors de l’ouverture ou de la création d’un fichier avec la fonction [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) , l’indicateur de **fichier aucun indicateur de mise en \_ \_ \_ mémoire tampon** peut être spécifié pour désactiver la mise en cache du système des données lues ou écrites dans le fichier. Bien que cela offre un contrôle complet et direct sur la mise en mémoire tampon des e/s des données, dans le cas de fichiers et d’appareils similaires, des exigences d’alignement des données doivent être prises en compte.

> [!Note]  
> Ces informations d’alignement s’appliquent aux e/s sur les appareils tels que les fichiers qui prennent en charge la recherche et le concept de pointeurs (ou de *décalages*) de position de fichier. Pour les appareils qui ne recherchent pas, tels que les canaux nommés ou les appareils de communication, la désactivation de la mise en mémoire tampon peut ne pas nécessiter d’alignement particulier. Les limitations ou les gains d’efficacité qui peuvent être obtenus par l’alignement dans ce cas dépendent de la technologie sous-jacente.

 

Dans un exemple simple, l’application ouvre un fichier pour l’accès en écriture avec l’indicateur de **fichier aucun indicateur de \_ mise en \_ \_ mémoire tampon** , puis effectue un appel à la fonction [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) à l’aide d’une mémoire tampon de données définie dans l’application. Cette mémoire tampon locale est, dans ces cas, la seule mémoire tampon de fichier qui existe pour cette opération. En raison de la disposition du disque physique, de la disposition du stockage du système de fichiers et du suivi de position du pointeur de fichier au niveau système, cette opération d’écriture échoue, sauf si les tampons de données définis localement répondent à certains critères d’alignement, décrits dans la section suivante.

> [!Note]  
> La discussion sur la mise en cache ne tient pas compte de la mise en cache matérielle sur le disque physique lui-même, ce qui n’est pas garanti dans le contrôle direct du système dans tous les cas. Cela n’a aucun effet sur les spécifications spécifiées dans cette rubrique.

 

Pour plus d’informations sur la façon dont l' **indicateur de fichier \_ \_ sans \_ mise en mémoire tampon** interagit avec d’autres indicateurs liés au cache, consultez [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea).

## <a name="alignment-and-file-access-requirements"></a>Exigences d’alignement et d’accès aux fichiers

Comme indiqué précédemment, une application doit répondre à certaines exigences lors de l’utilisation de fichiers ouverts avec l' **indicateur de fichier \_ \_ sans \_ mise en mémoire tampon**. Les caractéristiques suivantes s’appliquent :

-   Les tailles d’accès aux fichiers, y compris l’offset de fichier facultatif dans la structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) , s’ils sont spécifiés, doivent être pour un nombre d’octets qui est un entier multiple de la taille du secteur du volume. Par exemple, si la taille de secteur est de 512 octets, une application peut demander des lectures et des écritures de 512, 1 024, 1 536 ou 2 048 octets, mais pas de 335, 981 ou 7 171 octets.
-   Les adresses de mémoire tampon d’accès aux fichiers pour les opérations de lecture et d’écriture doivent être alignées sur un secteur physique, ce qui signifie qu’elles sont alignées sur les adresses en mémoire qui sont des nombres entiers de la taille de secteur physique du volume. Selon le disque, cette exigence ne peut pas être appliquée.

Les développeurs d’applications doivent prendre note de nouveaux types de périphériques de stockage introduits sur le marché avec une taille de secteur de média physique de 4 096 octets. Le nom du secteur pour ces appareils est « format avancé ». Comme il peut y avoir des problèmes de compatibilité avec l’introduction directe de 4 096 octets comme unité d’adressage pour le support, une solution de compatibilité temporaire consiste à introduire des appareils qui émulent un périphérique de stockage de secteur de 512 octets standard, mais qui proposent des informations sur la taille réelle de secteur par le biais de commandes ATA et SCSI standard.

À la suite de cette émulation, il y a deux tailles de secteur que les développeurs devront comprendre :

-   Secteur logique : unité utilisée pour l’adressage de bloc logique pour le média. Nous pouvons également considérer qu’il s’agit de la plus petite unité d’écriture que le stockage peut accepter. Il s’agit de l' « émulation ».
-   Secteur physique : l’unité pour laquelle les opérations de lecture et d’écriture sur l’appareil sont effectuées en une seule opération. Il s’agit de l’unité d’écriture atomique et de l’alignement des e/s non mises en mémoire tampon sur afin d’obtenir des caractéristiques de performances et de fiabilité optimales.

La plupart des API Windows actuelles, comme [**IOCTL \_ Disk obtiennent un \_ \_ lecteur \_ Geometry**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_disk_get_drive_geometry) et [**GetDiskFreeSpace**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespacea), retournent la taille de secteur logique, mais la taille de secteur physique peut être récupérée par le biais du code de contrôle de propriété de  [**\_ \_ requête \_ de stockage IOCTL**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) , avec les informations pertinentes contenues dans le membre BytesPerPhysicalSector dans la structure du [**\_ \_ \_ descripteur d’alignement de l’accès au stockage**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_access_alignment_descriptor) . Pour obtenir un exemple, consultez l’exemple de code du [**\_ \_ \_ descripteur d’alignement**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_access_alignment_descriptor)de l’accès au stockage. Microsoft recommande vivement aux développeurs d’aligner les e/s non mises en mémoire tampon sur la taille de secteur physique comme indiqué par le code de contrôle de la **\_ propriété de \_ requête \_ de stockage IOCTL** pour garantir que leurs applications sont préparées pour cette transition de taille de secteur.

**Windows Server 2003 et Windows XP :** La structure du [**\_ \_ \_ descripteur d’alignement de l’accès au stockage**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_access_alignment_descriptor) n’est pas disponible. Il a été introduit avec Windows Vista et Windows Server 2008.

Étant donné que les adresses de mémoire tampon pour les opérations de lecture et d’écriture doivent être alignées sur les secteurs, l’application doit contrôler directement la manière dont ces mémoires tampons sont allouées. L’une des façons d’aligner les mémoires tampons consiste à utiliser la fonction [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc) pour allouer les mémoires tampons. Tenez compte des éléments suivants :

-   [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc) alloue de la mémoire qui est alignée sur les adresses qui sont des multiples de type entier de la taille de page du système. La taille de la page est de 4 096 octets sur x64 et x86 ou 8 192 octets pour les systèmes Itanium. Pour plus d’informations, consultez la fonction [**GetSystemInfo**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) .
-   La taille du secteur est généralement de 512 à 4 096 octets pour les périphériques de stockage à accès direct (disques durs) et de 2 048 octets pour les CD-ROM.
-   Les tailles des pages et des secteurs sont les puissances de 2.

Par conséquent, dans la plupart des cas, la mémoire alignée sur la page est également alignée sur les secteurs, car le cas où la taille du secteur est plus grande que la taille de la page est rare.

Une autre façon d’obtenir des tampons de mémoire alignés manuellement consiste à utiliser la fonction [ \_ \_ malloc alignée](/cpp/c-runtime-library/reference/aligned-malloc?view=vs-2019) à partir de la bibliothèque de Run-Time C. Pour obtenir un exemple de la façon de contrôler manuellement l’alignement de la mémoire tampon, consultez l’exemple de code du langage C++ dans la section exemple de code de [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile).

 

 
