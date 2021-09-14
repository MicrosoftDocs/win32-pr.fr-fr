---
description: Décrit un schéma de ventilation-regroupement pour la lecture ou l’écriture de segments non contigus de données en une seule opération.
ms.assetid: ae5d83ca-f219-4fcc-ad06-bc242ba95372
title: Lecture ou écriture dans des fichiers à l’aide d’un schéma de Scatter-Gather
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a7db31dd73dd0b498436548a867dd92ff248805
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009863"
---
# <a name="reading-from-or-writing-to-files-using-a-scatter-gather-scheme"></a>Lecture ou écriture dans des fichiers à l’aide d’un schéma de Scatter-Gather

Un schéma de ventilation-regroupement utilise le système d’exploitation pour fournir en une seule opération des blocs de données discrets (tels que les enregistrements de base de données) à partir d’un fichier pour séparer les mémoires tampons non contiguës en mémoire. Un schéma de ventilation-regroupement écrit également les données à partir de mémoires tampons non contiguës en une seule opération.

Une application peut implémenter un schéma de ventilation-regroupement à l’aide des fonctions [**ReadFileScatter**](/windows/desktop/api/FileAPI/nf-fileapi-readfilescatter) et [**WriteFileGather**](/windows/desktop/api/FileAPI/nf-fileapi-writefilegather) .

 

 



