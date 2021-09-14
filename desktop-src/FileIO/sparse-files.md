---
description: La compression de fichiers de fichiers qui contiennent principalement des zéros permet d’utiliser efficacement l’espace disque.
ms.assetid: 7326041d-f11e-4b80-ac4e-07173e418ce7
title: Fichiers partiellement alloués
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21c282ca89c9dc9e44800a2a7fc969c3f883006b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009838"
---
# <a name="sparse-files"></a>Fichiers partiellement alloués

Un fichier dans lequel la plupart des données est égale à zéro est dit qu’il contient un *jeu de données éparses*. Les fichiers comme ceux-ci sont généralement très volumineux par exemple, un fichier qui contient des données d’image à traiter ou une matrice au sein d’une base de données à haut débit. Le problème avec les fichiers qui contiennent des jeux de données éparses est que la majorité du fichier ne contient pas de données utiles et, pour cette raison, il s’agit d’une utilisation inefficace de l’espace disque.

La compression de fichiers dans le système de fichiers NTFS est une solution partielle au problème. Toutes les données du fichier qui ne sont pas écrites explicitement sont explicitement définies à zéro. La compression de fichiers compacte ces plages de zéros. Toutefois, l’inconvénient de la compression de fichiers est que le temps d’accès peut augmenter en raison de la compression et de la décompression des données.

La prise en charge des fichiers partiellement alloués est introduite dans le système de fichiers NTFS pour une utilisation plus efficace de l’espace disque. Lorsque la fonctionnalité de fichier partiellement alloué est activée, le système n’alloue pas d’espace disque dur à un fichier, sauf dans les régions où il contient des données différentes de zéro. Lorsqu’une opération d’écriture est tentée alors qu’une grande quantité de données dans la mémoire tampon est égale à zéro, les zéros ne sont pas écrits dans le fichier. Au lieu de cela, le système de fichiers crée une liste interne qui contient les emplacements des zéros dans le fichier, et cette liste est consultée pendant toutes les opérations de lecture. Lorsqu’une opération de lecture est effectuée dans des zones du fichier où des zéros se trouvent, le système de fichiers retourne le nombre approprié de zéros dans la mémoire tampon allouée pour l’opération de lecture. De cette façon, la maintenance du fichier partiellement alloué est transparente pour tous les processus qui y accèdent et est plus efficace que la compression pour ce scénario particulier.

La valeur de données par défaut d’un fichier partiellement alloué est zéro ; Toutefois, il peut être défini sur d’autres valeurs.

Pour plus d’informations sur les fichiers partiellement alloués, consultez les rubriques suivantes.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                     | Description                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Opérations sur les fichiers partiellement alloués](sparse-file-operations.md)<br/>                           | Déterminez si un système de fichiers prend en charge les fichiers partiellement alloués en appelant la fonction GetVolumeInformation.<br/>                                                                                |
| [Obtention de la taille d’un fichier partiellement alloué](obtaining-the-size-of-a-sparse-file.md)<br/> | Obtenir la taille allouée ou la taille totale d’un fichier à l’aide de la fonction [**GetCompressedFileSize**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea) ou [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) .<br/> |
| [Fichiers partiellement alloués et quotas de disque](sparse-files-and-disk-quota.md)<br/>                | Un fichier partiellement alloué affecte les quotas de l’utilisateur par la taille nominale du fichier, et non par la quantité réelle d’espace disque allouée.<br/>                                                                  |



 

 

 




