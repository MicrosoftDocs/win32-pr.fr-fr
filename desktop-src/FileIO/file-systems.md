---
description: Gérer les répertoires avec la table d’entrée de répertoire, les handles de répertoire, les points d’analyse.
title: Systèmes de fichiers locaux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92f624ef1999b81adb63ba1d5b7e349259cabd53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755157"
---
# <a name="local-file-systems"></a>Systèmes de fichiers locaux

Un *système de fichiers* permet aux applications de stocker et de récupérer des fichiers sur les périphériques de stockage. Les fichiers sont placés dans une structure hiérarchique. Le système de fichiers spécifie les conventions d’affectation de noms des fichiers et le format de spécification du chemin d’accès à un fichier dans l’arborescence.

Chaque système de fichiers se compose d’un ou de plusieurs pilotes et bibliothèques de liens dynamiques qui définissent les formats de données et les fonctionnalités du système de fichiers. Les systèmes de fichiers peuvent exister sur différents types de périphériques de stockage, y compris les disques durs, les juke-boxes, les disques optiques amovibles, les unités de sauvegarde sur bande et les cartes mémoire.

Tous les systèmes de fichiers pris en charge par Windows disposent des composants de stockage suivants :

-   Volumes. Un *volume* est un ensemble de répertoires et de fichiers.
-   Répertoires. Un *répertoire* est une collection hiérarchique de répertoires et de fichiers.
-   Fichiers. Un *fichier* est un regroupement logique de données associées.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                | Description                                                                                                                                                                                                                                |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Gestion de répertoires](directory-management.md)<br/>          | Un *répertoire* est une collection hiérarchique de répertoires et de fichiers. La seule contrainte sur le nombre de fichiers pouvant être contenus dans un répertoire unique est la taille physique du disque sur lequel se trouve le répertoire.<br/> |
| [Gestion des disques](disk-management.md)<br/>                    | Un *disque dur* est un disque rigide à l’intérieur d’un ordinateur qui stocke et fournit un accès relativement rapide à de grandes quantités de données. C’est le type de stockage le plus souvent utilisé avec Windows. Le système prend également en charge les supports amovibles.<br/>    |
| [Gestion des fichiers](file-management.md)<br/>                    | Un *objet fichier* fournit une représentation d’une ressource (un appareil physique ou une ressource située sur un appareil physique) qui peut être gérée par le système d’e/s.<br/>                                                            |
| [NTFS transactionnel (TxF)](transactional-ntfs-portal.md)<br/> | Le NTFS transactionnel (TxF) autorise l’exécution d’opérations de fichiers sur un volume de système de fichiers NTFS dans une transaction.<br/>                                                                                                                 |
| [Gestion des volumes](volume-management.md)<br/>                | Le niveau le plus élevé de l’organisation dans le système de fichiers est le *volume*. Un système de fichiers réside sur un volume.<br/>                                                                                                                        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Informations techniques de référence sur FAT](/previous-versions/windows/it-pro/windows-server-2003/cc758586(v=ws.10))
</dt> <dt>

[Technologies de systèmes de fichiers](/previous-versions/windows/it-pro/windows-server-2003/cc778296(v=ws.10))
</dt> <dt>

[Référence technique NTFS](/previous-versions/windows/it-pro/windows-server-2003/cc758691(v=ws.10))
</dt> </dl>

 

