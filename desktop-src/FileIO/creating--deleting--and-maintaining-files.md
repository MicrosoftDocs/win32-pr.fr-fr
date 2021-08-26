---
description: Fonctions à utiliser pour créer, supprimer et gérer des fichiers.
ms.assetid: b9cf0ddf-efda-4997-bcc3-3056026c1264
title: Création, suppression et maintenance de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff20362e2ff5f1d8b01b515c7cbbb9fae250d930b2610c49c5e8aaeeabe7b401
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982119"
---
# <a name="creating-deleting-and-maintaining-files"></a>Création, suppression et maintenance de fichiers

Les rubriques suivantes décrivent comment créer, supprimer et gérer des fichiers.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                   | Description                                                                                                                                                                                                                                                                 |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Nommage des fichiers, chemins d’accès et espaces de noms](naming-a-file.md)<br/>     | Règles, conventions et limitations des noms de fichiers et de répertoires, notamment les conventions d’affectation de noms, les noms de fichiers courts et les noms de fichiers longs, les chemins d’accès complets et les chemins d’accès relatifs, la limite de longueur maximale du chemin d’accès, les noms de fichiers 8,3 et les espaces de noms.<br/>            |
| [Création et ouverture de fichiers](creating-and-opening-files.md)<br/> | Considérations relatives à la création ou à l’ouverture d’un fichier à l’aide de la fonction [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) .<br/>                                                                                                                                                            |
| [Déplacement et remplacement de fichiers](moving-and-replacing-files.md)<br/> | Considérations relatives au déplacement et au remplacement de fichiers à l’aide des fonctions CopyFileEx, CreateFile, ReplaceFile et MoveFileEx.<br/>                                                                                                                                        |
| [Fermeture et suppression de fichiers](closing-and-deleting-files.md)<br/> | Pour utiliser efficacement les ressources du système d’exploitation, une application doit fermer les fichiers lorsqu’ils ne sont plus nécessaires à l’aide de la fonction [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) . Si un fichier est ouvert lorsqu’une application se termine, le système le ferme automatiquement.<br/> |
| [Défragmentation des fichiers](defragmenting-files.md)<br/>               | La *défragmentation* est le processus qui consiste à déplacer des parties de fichiers sur un disque pour défragmenter des fichiers, c’est-à-dire le processus de déplacement de clusters de fichiers sur un disque afin de les rendre contigus.<br/>                                                                               |



 

 

