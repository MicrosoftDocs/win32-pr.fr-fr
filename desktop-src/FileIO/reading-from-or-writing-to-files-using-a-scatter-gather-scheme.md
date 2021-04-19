---
description: Décrit un schéma de ventilation-regroupement pour la lecture ou l’écriture de segments non contigus de données en une seule opération.
ms.assetid: ae5d83ca-f219-4fcc-ad06-bc242ba95372
title: Lecture ou écriture dans des fichiers à l’aide d’un schéma de Scatter-Gather
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a7db31dd73dd0b498436548a867dd92ff248805
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545015"
---
# <a name="reading-from-or-writing-to-files-using-a-scatter-gather-scheme"></a><span data-ttu-id="49641-103">Lecture ou écriture dans des fichiers à l’aide d’un schéma de Scatter-Gather</span><span class="sxs-lookup"><span data-stu-id="49641-103">Reading From or Writing To Files Using a Scatter-Gather Scheme</span></span>

<span data-ttu-id="49641-104">Un schéma de ventilation-regroupement utilise le système d’exploitation pour fournir en une seule opération des blocs de données discrets (tels que les enregistrements de base de données) à partir d’un fichier pour séparer les mémoires tampons non contiguës en mémoire.</span><span class="sxs-lookup"><span data-stu-id="49641-104">A scatter-gather scheme uses the operating system to deliver in one operation multiple discrete chunks of data (such as database records) from a file to separate, noncontiguous buffers in memory.</span></span> <span data-ttu-id="49641-105">Un schéma de ventilation-regroupement écrit également les données à partir de mémoires tampons non contiguës en une seule opération.</span><span class="sxs-lookup"><span data-stu-id="49641-105">A scatter-gather scheme also writes the data from noncontiguous buffers in one operation.</span></span>

<span data-ttu-id="49641-106">Une application peut implémenter un schéma de ventilation-regroupement à l’aide des fonctions [**ReadFileScatter**](/windows/desktop/api/FileAPI/nf-fileapi-readfilescatter) et [**WriteFileGather**](/windows/desktop/api/FileAPI/nf-fileapi-writefilegather) .</span><span class="sxs-lookup"><span data-stu-id="49641-106">An application can implement a scatter-gather scheme by using the [**ReadFileScatter**](/windows/desktop/api/FileAPI/nf-fileapi-readfilescatter) and [**WriteFileGather**](/windows/desktop/api/FileAPI/nf-fileapi-writefilegather) functions.</span></span>

 

 



