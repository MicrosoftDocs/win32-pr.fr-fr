---
description: La défragmentation est le processus qui consiste à déplacer des parties de fichiers sur un disque pour défragmenter des fichiers, c’est-à-dire le processus de déplacement de clusters de fichiers sur un disque afin de les rendre contigus.
ms.assetid: 27ccaab7-ec89-489b-80dc-df9beb7969bc
title: Défragmentation des fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b2d079f58ec98f320356a477531616788f84ccb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863885"
---
# <a name="defragmenting-files"></a>Défragmentation des fichiers

Lorsqu’un fichier est écrit sur un disque, il se peut que le fichier ne puisse pas être écrit dans des clusters contigus. Les clusters non contigus ralentissent le processus de lecture et d’écriture d’un fichier. Plus la valeur est éloignée sur un disque les clusters non contigus, moins le problème est grave en raison du temps nécessaire pour déplacer la tête de lecture/écriture d’un lecteur de disque dur. Un fichier avec des clusters non contigus est *fragmenté*. Pour optimiser l’accès aux fichiers, un volume peut être défragmenté.

La *défragmentation* est le processus qui consiste à déplacer des parties de fichiers sur un disque pour défragmenter des fichiers, c’est-à-dire le processus de déplacement de clusters de fichiers sur un disque afin de les rendre contigus. Pour plus d'informations, consultez les sections suivantes :

-   [Défragmentation d’un fichier](#defragmenting-a-file)
-   [Minimisation des interactions entre la défragmentation et les clichés instantanés](#minimizing-interactions-between-defragmentation-and-shadow-copies)
-   [Fichiers, flux et types de flux pris en charge pour la défragmentation](#files-streams-and-stream-types-supported-for-defragmentation)

## <a name="defragmenting-a-file"></a>Défragmentation d’un fichier

Dans un système d’exploitation simple à tâche unique, le logiciel de défragmentation est la seule tâche, et il n’y a aucun autre processus à lire ou à écrire sur le disque. Toutefois, dans un système d’exploitation multitâche, certains processus peuvent lire et écrire sur un lecteur de disque dur, tandis qu’un autre processus est en train de défragmenter ce disque dur. L’astuce consiste à éviter les écritures dans un fichier qui est défragmenté sans arrêter le processus d’écriture pendant très longtemps. La résolution de ce problème n’est pas simple, mais cela est possible.

Pour permettre la défragmentation sans avoir besoin d’une connaissance détaillée de la structure d’un disque de système de fichiers, un ensemble de trois codes de contrôle est fourni. Les codes de contrôle offrent les fonctionnalités suivantes :

-   Autoriser les applications à localiser des clusters vides
-   Déterminer l’emplacement du disque des clusters de fichiers
-   Déplacer des clusters sur un disque

Les codes de contrôle gèrent également en toute transparence le problème de l’inhibition et de permettre à d’autres processus de lire et d’écrire dans des fichiers pendant les déplacements.

Ces opérations peuvent être effectuées sans empêcher l’exécution d’autres processus. Toutefois, les autres processus ont des temps de réponse plus lents lors de la défragmentation d’un lecteur de disque.

**Pour défragmenter un fichier**

1.  Utilisez le code de contrôle [**FSCTL \_ obtenir le \_ volume \_ bitmap**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_volume_bitmap) pour rechercher un emplacement sur le volume suffisamment grand pour accepter un fichier entier.
    > [!Note]  
    > Si nécessaire, déplacez d’autres fichiers pour créer un emplacement suffisamment grand. Dans l’idéal, il y a suffisamment de clusters non alloués après la première extension du fichier, vous pouvez déplacer les extensions suivantes dans l’espace après la première extension.

     

2.  Utilisez le code de contrôle [**FSCTL \_ obtenir des \_ \_ pointeurs de récupération**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_retrieval_pointers) pour obtenir une carte de la disposition actuelle du fichier sur le disque.
3.  Parcourez la structure de [**\_ \_ mémoire tampon des pointeurs de récupération**](/windows/desktop/api/WinIoCtl/ns-winioctl-retrieval_pointers_buffer) retournée par [**FSCTL \_ obtient les \_ \_ pointeurs de récupération**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_retrieval_pointers).
4.  Utilisez le code de contrôle de [**\_ déplacement de \_ fichier FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_move_file) pour déplacer chaque cluster au fur et à mesure que vous parcourez la structure.
    > [!Note]  
    > Vous devrez peut-être renouveler le bitmap ou la structure de récupération, ou les deux à la fois à mesure que d’autres processus écrivent sur le disque.

     

Deux des opérations utilisées dans le processus de défragmentation nécessitent un handle vers un volume. Seuls les administrateurs peuvent obtenir un descripteur d’un volume, de sorte que seuls les administrateurs peuvent défragmenter un volume. Une application doit vérifier les droits d’un utilisateur qui tente d’exécuter un logiciel de défragmentation, et elle ne doit pas autoriser un utilisateur à défragmenter un volume si l’utilisateur ne dispose pas des droits appropriés.

Si vous utilisez [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) pour ouvrir un répertoire lors de la défragmentation d’un volume de système de fichiers FAT ou FAT32, spécifiez la valeur du masque d’accès **\_ en lecture générique** . Ne spécifiez pas la valeur **maximale \_ autorisée** pour le masque d’accès. L’accès au répertoire est refusé si cela est fait.

N’essayez pas de déplacer les clusters alloués dans un système de fichiers NTFS qui s’étend au-delà de la taille de fichier arrondie du cluster, car le résultat est une erreur.

Les points d’analyse, les bitmaps et les listes d’attributs des volumes du système de fichiers NTFS peuvent être défragmentés, ouverts pour la lecture et la synchronisation et nommés à l’aide de la syntaxe *file*:*Name*:*type* ; par exemple, *dirname*: $i 30 : $index \_ allocation, *MRP*:: $DATA, *MRP*:: $REPARSE \_ point et *MRP*:: $attribute \_ liste.

Lors de la défragmentation des volumes du système de fichiers NTFS, la défragmentation d’un cluster virtuel au-delà de la taille d’allocation d’un fichier est autorisée.

## <a name="minimizing-interactions-between-defragmentation-and-shadow-copies"></a>Minimisation des interactions entre la défragmentation et les clichés instantanés

Lorsque cela est possible, déplacez les données des blocs alignés les uns par rapport aux autres en incréments de 16 kilo-octets (Ko). Cela réduit la surcharge de copie sur écriture lorsque les clichés instantanés sont activés, car l’espace de cliché instantané est augmenté et les performances sont réduites lorsque les conditions suivantes sont remplies :

-   La taille du bloc de la demande de déplacement est inférieure ou égale à 16 Ko.
-   Le delta de déplacement n’est pas par incréments de 16 Ko.

Le delta de déplacement est le nombre d’octets entre le début du bloc source et le début du bloc cible. En d’autres termes, un bloc commençant à l’offset X (on-Disk) peut être déplacé vers l’offset de départ Y si la valeur absolue de X moins Y est un multiple pair de 16 Ko. Par conséquent, en supposant que les clusters de 4 Ko, le passage du cluster 3 au cluster 27 est optimisé, mais pas le passage du cluster 18 au cluster 24. Notez que mod (3, 4) = 3 = mod (27, 4). Mod 4 est choisi, car quatre clusters à 4 Ko chacun sont équivalents à 16 Ko. Par conséquent, un volume formaté sur une taille de cluster de 16 Ko entraîne l’optimisation de tous les fichiers de déplacement.

Pour plus d’informations sur les clichés instantanés, consultez [service VSS](/windows/desktop/VSS/about-the-volume-shadow-copy-service).

## <a name="files-streams-and-stream-types-supported-for-defragmentation"></a>Fichiers, flux et types de flux pris en charge pour la défragmentation

Alors que la plupart des fichiers peuvent être déplacés à l’aide du code de contrôle de [**\_ déplacement du \_ fichier FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_move_file) , ils ne peuvent pas tous être déplacés. Voici la liste des fichiers, des flux et des types de flux (également appelés codes de type d’attribut) pris en charge par **FSCTL \_ Move \_ file**. Les autres fichiers, flux et types de flux ne sont pas pris en charge par **FSCTL \_ Move \_ file**.

Types de flux pris en charge pour tout fichier ou répertoire.

-   :: $DATA
-   :: $ATTRIBUTE \_ liste
-   :: $REPARSE \_ point
-   :: $EA
-   :: $LOGGED \_ flux de l’utilitaire \_

* * Windows 7, Windows Server 2008 R2, Windows Server 2008, Windows Vista, Windows Server 2003 et Windows XP : * * :: $EA et :: $LOGGED \_ flux de l’utilitaire ne \_ sont pas pris en charge avant Windows 8 et windows server 2012

Types de flux pris en charge pour n’importe quel répertoire.

-   :: $BITMAP
-   :: $INDEX \_ allocation

Voici les types de fichiers système, de flux et de flux pris en charge par [**FSCTL \_ Move \_ file**](/windows/win32/api/winioctl/ni-winioctl-fsctl_move_file) dans le format «*nom_fichier*:*StreamName*: $*TypeName*».

-   $MFT :: $DATA
-   $MFT :: $ATTRIBUTE \_ liste
-   $MFT :: $BITMAP
-   $AttrDef :: $DATA
-   $AttrDef :: $ATTRIBUTE \_ liste
-   $Secure : $SDS : $DATA
-   $Secure :: $ATTRIBUTE \_ liste
-   $Secure : $SDH : allocation de $INDEX \_
-   $Secure : $SDH : $BITMAP
-   $Secure : $SII : allocation de $INDEX \_
-   $Secure : $SII : $BITMAP
-   $UpCase :: $DATA
-   $UpCase :: $ATTRIBUTE \_ liste
-   $Extend : $I 30 : allocation de $INDEX \_
-   $Extend :: $ATTRIBUTE \_ liste
-   $Extend : $I 30 : $BITMAP
-   $Extend \\ $UsnJrnl : $J : $Data
-   $Extend \\ $UsnJrnl :: $attribute, \_ liste
-   $Extend \\ $UsnJrnl : $max : $Data
-   $Extend \\ $quota : $Q : allocation de $index \_
-   $Extend \\ $quota :: $attribute, \_ liste
-   $Extend \\ $quota : $Q : $bitmap
-   $Extend \\ $quota : $O : allocation de $index \_
-   $Extend \\ $quota : $O : $bitmap
-   $Extend \\ $objID : $O : allocation de $index \_
-   $Extend \\ $objID :: $attribute, \_ liste
-   $Extend \\ $objID : $O : $bitmap
-   $Extend \\ $reparse : $R : allocation de $index \_
-   $Extend \\ $reparse :: $attribute, \_ liste
-   $Extend \\ $reparse : $R : $bitmap
-   $Extend \\ $RmMetadata : $I 30 : allocation de $index \_
-   $Extend \\ $RmMetadata : $I 30 : $bitmap
-   $Extend \\ $RmMetadata :: $attribute, \_ liste
-   $Extend \\ $RmMetadata \\ $Repair :: $Data
-   $Extend \\ $RmMetadata \\ $Repair :: $attribute \_
-   $Extend \\ $RmMetadata \\ $Repair : $Config : $Data
-   $Extend \\ $RmMetadata \\ $Txf : $I 30 : ALLOCATION de $index \_
-   $Extend \\ $RmMetadata \\ $TxF :: $attribute \_
-   $Extend \\ $RmMetadata \\ $Txf : $I 30 : $bitmap
-   $Extend \\ $RmMetadata \\ $Txf : $TxF \_ Data : $logged \_ \_ flux de l’utilitaire
-   $Extend \\ $RmMetadata \\ $TxfLog : $I 30 : ALLOCATION de $index \_
-   $Extend \\ $RmMetadata \\ $txflog :: $attribute \_
-   $Extend \\ $RmMetadata \\ $TxfLog : $I 30 : $bitmap
-   $Extend \\ $RmMetadata \\ $txflog \\ $Tops :: $Data
-   $Extend \\ $RmMetadata \\ $txflog \\ $Tops :: $attribute \_
-   $Extend \\ $RmMetadata \\ $txflog \\ $Tops : $T : $Data
-   $Extend \\ $RmMetadata \\ $txflog \\ $txflog. flambt :: $Data
-   $Extend \\ $RmMetadata \\ $txflog \\ $txflog. flambage :: $attribute \_ liste

 

 
