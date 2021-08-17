---
description: une vérification de redondance cyclique (CRC) de fichiers est disponible avec Windows Installer.
ms.assetid: c895488b-6e60-4175-8865-4ba4b0cb2d9a
title: Vérification des CRC au cours d’une installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c81b80a9b1900abf6c294911803df155a4c75025f5ad5ef01609af7345b0431e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118379914"
---
# <a name="crc-checking-during-an-installation"></a>Vérification des CRC au cours d’une installation

une vérification de redondance cyclique (CRC) de fichiers est disponible avec Windows Installer. La vérification du CRC est un mécanisme de vérification des erreurs, similaire à une somme de contrôle, qui permet à une application de déterminer si les informations d’un fichier ont été modifiées. une fois que le Windows Installer terminé de copier un fichier, il obtient une valeur CRC des fichiers source et de destination. Le programme d’installation vérifie le CRC d’origine marqué dans le fichier et le compare au CRC calculé à partir de la copie. La vérification du CRC échoue si la valeur CRC d’origine n’est pas null et est différente du CRC calculé sur la copie. Si le CRC d’origine est null, aucune vérification n’est effectuée.

la Windows Installer effectue une vérification de CRC sur un fichier dans les cas suivants :

-   Si la [propriété MSICHECKCRCS](msicheckcrcs.md) est définie et **msidbFileAttributesChecksum** est inclus dans le champ Attributes de l’enregistrement du fichier dans la [table file](file-table.md). Le programme d’installation effectue la vérification de CRC après l’installation, la duplication ou le déplacement du fichier.
-   Si la [propriété MSICHECKCRCS](msicheckcrcs.md) est définie et que **msidbFileAttributesChecksum** est inclus dans le champ Attributes de l’enregistrement du fichier dans la [table file](file-table.md), le programme d’installation effectue une vérification des CRC après avoir appliqué un correctif au fichier.
-   Si le **msidbFileAttributesChecksum** est inclus dans le champ attributs de l’enregistrement du fichier dans la [table file](file-table.md), le programme d’installation effectue une vérification de CRC avant de lier les images.

Si la vérification échoue avant la liaison d’une image, le programme d’installation signale les deux erreurs suivantes dans le fichier journal et poursuit l’installation sans lier le fichier.



| Code | Message                                               |
|------|-------------------------------------------------------|
| 2941 | Impossible de calculer le CRC pour le fichier \[ 2 \] .             |
| 2942 | L’action BindImage n’a pas été exécutée sur \[ 2 \] fichiers. |



 

Si la vérification échoue après qu’un fichier non compressé a été copié, dupliqué ou corrigé, le programme d’installation signale l’erreur suivante. Cette erreur est également signalée si la vérification échoue après la copie d’un fichier compressé. Si le fichier a l’attribut **msidbFileAttributesVital** , le fichier est considéré comme vital pour l’installation et l’utilisateur a la possibilité de réessayer ou d’annuler l’installation. Si le fichier est marqué comme non critique dans la colonne attributs de la [table file](file-table.md), l’utilisateur peut ignorer l’erreur et continuer, réessayer ou annuler l’installation.



| Code | Message                                         |
|------|-------------------------------------------------|
| 1331 | Échec de la copie correcte du \[ \] fichier 2 : erreur CRC. |



 

Notez que seuls les fichiers non compressés sont déplacés. Si la vérification échoue après le déplacement d’un fichier non compressé, le programme d’installation affiche l’erreur suivante. Si le fichier a l’attribut **msidbFileAttributesVital** , le fichier est considéré comme vital pour l’installation et l’installation échoue. Si le fichier est marqué comme non vital dans la colonne attributs de la [table file](file-table.md), l’utilisateur a la possibilité d’annuler ou d’ignorer l’erreur et de poursuivre l’installation.



| Code | Message                                         |
|------|-------------------------------------------------|
| 1332 | Échec du déplacement du \[ \] fichier 2 : erreur CRC. |



 

Si la vérification échoue après l’application d’un correctif à un fichier non compressé, le programme d’installation affiche l’erreur suivante. Si le fichier a l’attribut **msidbFileAttributesVital** , le fichier est considéré comme vital pour l’installation et l’installation échoue. Si le fichier est marqué comme non vital dans la colonne attributs de la [table file](file-table.md), l’utilisateur a la possibilité d’annuler ou d’ignorer l’erreur et de poursuivre l’installation.



| Code | Message                                          |
|------|--------------------------------------------------|
| 1333 | Échec de la correction \[ du \] fichier 2 : erreur CRC. |



 

 

 



