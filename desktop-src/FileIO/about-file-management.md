---
description: Informations sur la gestion des fichiers.
ms.assetid: cf4e69b9-86dd-43a4-9011-6209fc65f550
title: À propos de la gestion de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2544d31ecb95029053987a3d64e80f4cdf8c0f3170b3a679b542e145ca262947
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766369"
---
# <a name="about-file-management"></a>À propos de la gestion de fichiers

Les rubriques suivantes contiennent plus d’informations sur la gestion des fichiers.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                                 | Description                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Comparaison des fonctionnalités du système de fichiers](filesystem-functionality-comparison.md)<br/>            | les Tables qui répertorient les fonctionnalités et les fonctionnalités prennent en charge les comparaisons pour les quatre principaux systèmes de fichiers Windows, NTFS, exFAT, UDF et FAT32.<br/>                                                                           |
| [Fichiers et clusters](files-and-clusters.md)<br/>                                               | Un *fichier* est une unité de données dans le système de fichiers qu’un utilisateur peut accéder et gérer.<br/>                                                                                                                              |
| [Création, suppression et maintenance de fichiers](creating--deleting--and-maintaining-files.md)<br/> | Fonctions à utiliser pour créer, supprimer et gérer des fichiers.<br/>                                                                                                                                                       |
| [Obtention et définition des informations de fichier](obtaining-and-setting-file-information.md)<br/>       | Fonctions à utiliser pour récupérer et définir des informations de fichier.<br/>                                                                                                                                                             |
| [Lecture et écriture dans des fichiers](reading-from-and-writing-to-files.md)<br/>                 | Une application lit et écrit dans un fichier à l’aide des fonctions [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile), [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex), [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)et [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) .<br/> |
| [Liaison de fichiers et de répertoires](file-and-directory-linking.md)<br/>                               | Il existe deux types de liens pris en charge dans le système de fichiers NTFS : les [liens physiques et les jonctions](hard-links-and-junctions.md).<br/>                                                                                     |
| [Clonage de bloc](block-cloning.md)<br/>                                                         | Une opération de *clonage de bloc* indique au système de fichiers de copier une plage d’octets de fichier pour le compte d’une application.<br/>                                                                                                |
| [Compression et décompression de fichiers](file-compression-and-decompression.md)<br/>               | Le système de fichiers NTFS utilise la compression Lempel-Ziv, qui est un algorithme de compression sans perte.<br/>                                                                                                                  |
| [Chiffrement de fichier](file-encryption.md)<br/>                                                     | Le système de fichiers EFS (Encrypted File System) fournit une protection par chiffrement des fichiers individuels sur les volumes de système de fichiers NTFS à l’aide d’un système à clé publique.<br/>                                                               |
| [Sécurité des fichiers et droits d’accès](file-security-and-access-rights.md)<br/>                     | Étant donné que les fichiers sont des [objets sécurisables](/windows/desktop/SecAuthZ/securable-objects), l’accès à ceux-ci est régi par le modèle de contrôle d’accès qui régit l’accès à tous les autres objets sécurisables dans Windows.<br/>                     |
| [Entrée et sortie (e/s)](input-and-output--i-o-.md)<br/>                                       | Windows permet d’effectuer des opérations d’entrée et de sortie (e/s) sur des composants de stockage situés sur des ordinateurs locaux et distants.<br/>                                                                        |
| [Fichiers partiellement alloués](sparse-files.md)<br/>                                                           | La compression de fichiers de fichiers qui contiennent principalement des zéros permet d’utiliser efficacement l’espace disque.<br/>                                                                                                                        |
| [Liens symboliques](symbolic-links.md)<br/>                                                       | Un lien symbolique est un objet de système de fichiers qui pointe vers un autre objet de système de fichiers. L’objet désigné est appelé la cible.<br/>                                                                          |



 

 

