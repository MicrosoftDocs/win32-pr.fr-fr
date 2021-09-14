---
description: Déterminez si un système de fichiers prend en charge les fichiers partiellement alloués en appelant la fonction GetVolumeInformation.
ms.assetid: a08f6bbc-c139-4396-8964-4aa63285f3f5
title: Opérations sur les fichiers partiellement alloués
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c23d26fc1c52db32ca7674aec2fc487a826e9a6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009845"
---
# <a name="sparse-file-operations"></a>Opérations sur les fichiers partiellement alloués

Pour déterminer si un système de fichiers prend en charge les fichiers partiellement alloués, appelez la fonction [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) et examinez le fichier prend en charge l’indicateur de bit de **\_ \_ \_ fichiers éparpillés** retourné via le paramètre *lpFileSystemFlags* .

La plupart des applications ne prennent pas en charge les fichiers partiellement alloués et ne créent pas de fichiers partiellement alloués. Le fait qu’une application lise un fichier partiellement alloué est transparent pour l’application. Une application qui prend en charge les fichiers partiellement alloués doit déterminer si son jeu de données est apte à être conservé dans un fichier partiellement alloué. Une fois cette détermination effectuée, l’application doit déclarer explicitement un fichier comme fragmenté, à l’aide du code de contrôle [**\_ \_ Sparse FSCTL Set**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_sparse) .

Une fois qu’une application a défini un fichier comme étant épars, l’application peut utiliser le code de contrôle de [**FSCTL \_ défini \_ zéro \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data) pour définir une région du fichier sur zéro. En outre, l’application peut utiliser le code de contrôle des [**\_ \_ \_ plages allouées par la requête FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_allocated_ranges) pour accélérer les recherches de données autres que zéro dans le fichier partiellement alloué.

Lorsque vous effectuez une opération d’écriture (avec une fonction ou une opération autre que [**FSCTL ne \_ définissant \_ aucune \_ donnée**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data)) dont les données se composent de zéro, mais des zéros, les zéros sont écrits sur le disque pendant toute la durée de l’écriture. Pour mettre à zéro une plage du fichier et conserver la plus faible, utilisez **FSCTL \_ définir \_ zéro \_ données**.

Une application qui prend en charge les géofaibles peut également définir un fichier existant de façon à ce qu’il soit fragmenté. Si une application définit un fichier existant comme étant fragmenté, elle doit ensuite analyser le fichier pour rechercher les régions qui contiennent des zéros, et utiliser FSCTL pour réinitialiser les régions, ce qui peut entraîner la désallocation de stockage sur disque physique. [**\_ \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data) Une application mise à niveau vers la reconnaissance des fichiers éparpillés doit effectuer cette conversion.

Lorsque vous effectuez une opération de lecture à partir d’une partie zéro d’un fichier partiellement alloué, le système d’exploitation peut ne pas lire à partir du disque dur. Au lieu de cela, le système reconnaît que la partie du fichier à lire contient des zéros et retourne une mémoire tampon pleine de zéros sans lire réellement sur le disque.

Comme pour tout autre fichier, le système peut écrire des données ou les lire à partir de n’importe quelle position dans un fichier partiellement alloué. Les données non null écrites dans une partie précédemment nulle du fichier peuvent entraîner une allocation d’espace disque. Les zéros écrits sur des données non nulles (uniquement avec [**FSCTL \_ défini sur \_ zéro \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data)) peuvent entraîner une désallocation de l’espace disque.

> [!Note]  
> C’est à l’application de préserver la plus faible en écrivant des zéros avec FSCTL, sans [**\_ définir de \_ \_ données zéro**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data).

 

Les outils de défragmentation qui gèrent des fichiers compressés sur des systèmes de fichiers NTFS gèrent correctement les fichiers partiellement alloués sur les volumes NTFS. Les fichiers partiellement alloués volumineux et très fragmentés peuvent dépasser la limite NTFS sur les étendues de disque avant l’utilisation de l’espace disponible. Pour plus d’informations, consultez l' [extension d’un fichier peut échouer avec l’erreur « disque plein », même si le volume dispose d’espace libre](https://support.microsoft.com/default.aspx/kb/957180).

 

 
