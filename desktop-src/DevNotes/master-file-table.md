---
description: La table de fichiers maîtres (MFT) stocke les informations requises pour récupérer des fichiers à partir d’une partition NTFS.
ms.assetid: 673fb4d0-7b6f-44fe-bfd6-1962e14ccdf5
title: Table de fichiers maîtres (remarques pour les développeurs)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ae8656a44b6dadd7d4ff601ddc64623935f5881
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950415"
---
# <a name="master-file-table"></a>Table de fichiers maîtres

\[Ce document s’applique uniquement à la version 3 des volumes NTFS.\]

La table de fichiers maîtres (MFT) stocke les informations requises pour récupérer des fichiers à partir d’une partition NTFS.

Un fichier peut avoir un ou plusieurs enregistrements MFT et peut contenir un ou plusieurs attributs. Dans NTFS, une référence de fichier correspond à la référence de segment MFT de l’enregistrement de fichier de base. Pour plus d’informations, [**consultez \_ \_ référence des segments MFT**](mft-segment-reference.md).

La table MFT contient des segments d’enregistrement de fichier ; les 16 premiers sont réservés aux fichiers spéciaux, tels que les suivants :

-   0 : MFT ($Mft)
-   5 : répertoire racine ( \\ )
-   6 : fichier d’allocation de cluster de volumes ($Bitmap)
-   8 : fichier de cluster incorrect ($BadClus)

Chaque segment d’enregistrement de fichier commence par un en-tête de segment d’enregistrement de fichier. Pour plus d’informations, consultez l' [**\_ \_ \_ en-tête de segment d’enregistrement de fichier**](file-record-segment-header.md). Chaque segment d’enregistrement de fichier est suivi d’un ou plusieurs attributs. Chaque attribut commence par un en-tête d’enregistrement d’attribut. Pour plus d’informations, consultez l' [**\_ \_ en-tête d’enregistrement d’attribut**](attribute-record-header.md). L’enregistrement d’attribut comprend le type d’attribut (par exemple $DATA ou $BITMAP), un nom facultatif et la valeur de l’attribut. Le flux de données utilisateur est un attribut, comme tous les flux. La liste d’attributs se termine par 0xFFFFFFFF ($END).

Voici quelques exemples d’attributs.

-   Le fichier $Mft contient un attribut $DATA sans nom qui correspond à la séquence des segments d’enregistrement MFT, dans l’ordre.
-   Le fichier $Mft contient un attribut $BITMAP sans nom qui indique les enregistrements MFT en cours d’utilisation.
-   Le fichier $Bitmap contient un attribut $DATA sans nom qui indique quels clusters sont en cours d’utilisation.
-   Le fichier $BadClus contient un attribut $DATA nommé $BAD qui contient une entrée qui correspond à chaque cluster incorrect.

Lorsqu’il n’y a plus d’espace pour le stockage des attributs dans le segment d’enregistrement de fichier, des segments d’enregistrement de fichier supplémentaires sont alloués et insérés dans le premier segment d’enregistrement de fichier (ou de base) dans un attribut appelé liste d’attributs. La liste d’attributs indique où chaque attribut associé au fichier est trouvé. Cela comprend tous les attributs de l’enregistrement de fichier de base, à l’exception de la liste d’attributs elle-même. Pour plus d’informations, [**consultez \_ \_ entrée de liste d’attributs**](attribute-list-entry.md).

Les structures associées à la table MFT sont les suivantes :

-   [**\_entrée de liste d’attributs \_**](attribute-list-entry.md)
-   [**\_ \_ en-tête d’enregistrement d’attribut**](attribute-record-header.md)
-   [**nom du fichier \_**](file-name.md)
-   [**\_ \_ en-tête de segment d’enregistrement de fichier \_**](file-record-segment-header.md)
-   [**\_Référence du segment MFT \_**](mft-segment-reference.md)
-   [**\_ \_ en-tête multisecteur**](multi-sector-header.md)
-   [**\_informations standard**](standard-information.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence technique NTFS](/previous-versions/windows/it-pro/windows-server-2003/cc758691(v=ws.10))
</dt> </dl>

 

 
