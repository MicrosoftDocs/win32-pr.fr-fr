---
description: Une application lit et écrit dans un fichier à l’aide des fonctions ReadFile, ReadFileEx, WriteFile et WriteFileEx.
ms.assetid: 14ecb06c-3f80-47b8-9964-6a2c3b572300
title: Lecture et écriture dans des fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffd0e6518ce2430e18bbb11033023ee6dc274573
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529350"
---
# <a name="reading-from-and-writing-to-files"></a>Lecture et écriture dans des fichiers

Une application lit et écrit dans un fichier à l’aide des fonctions [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile), [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex), [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)et [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) . Ces fonctions requièrent un handle vers un fichier à ouvrir pour la lecture et l’écriture, respectivement. Ils lisent et écrivent un nombre spécifié d’octets à l’emplacement indiqué par le pointeur de fichier. Les données sont lues et écrites exactement comme spécifié ; les fonctions ne mettent pas en forme les données.

Quand le pointeur de fichier atteint la fin d’un fichier et que l’application tente de lire à partir du fichier, aucune erreur ne se produit, mais aucun octet n’est lu. Par conséquent, la lecture de zéro octet sans erreur signifie que l’application a atteint la fin du fichier. L’écriture de zéro octet ne fait rien.

Pour plus d'informations, consultez les rubriques ci-dessous.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                                                                           | Description                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [Positionnement d’un pointeur de fichier](positioning-a-file-pointer.md)<br/>                                                                         | Windows utilise un pointeur de fichier pour effectuer le suivi des octets lus ou écrits.<br/>                                                       |
| [Lecture ou écriture dans des fichiers à l’aide d’un schéma de Scatter-Gather](reading-from-or-writing-to-files-using-a-scatter-gather-scheme.md)<br/> | Décrit un schéma de ventilation-regroupement pour la lecture ou l’écriture de segments non contigus de données en une seule opération.<br/>                   |
| [Vidage du System-Buffered des données d’e/s sur le disque](flushing-system-buffered-i-o-data-to-disk.md)<br/>                                           | Windows stocke les données dans des opérations de lecture et d’écriture de fichiers dans des mémoires tampons de données gérées par le système pour optimiser les performances du disque.<br/> |
| [Troncation ou extension des fichiers](truncating-or-extending-files.md)<br/>                                                                   | Une application peut tronquer ou étendre un fichier en appelant [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile).<br/>                             |



 

 

 




