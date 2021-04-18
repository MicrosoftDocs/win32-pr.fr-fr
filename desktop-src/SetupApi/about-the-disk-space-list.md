---
description: La liste espace disque vous permet de calculer l’espace disque requis pour effectuer les opérations d’installation.
ms.assetid: 6514cbdd-2f23-4ab8-9e34-86d3837503dc
title: À propos de la liste Disk-Space
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b092d73c00f426fe5c0ab298e4b6a53c19131c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106542897"
---
# <a name="about-the-disk-space-list"></a><span data-ttu-id="9ba4a-103">À propos de la liste Disk-Space</span><span class="sxs-lookup"><span data-stu-id="9ba4a-103">About the Disk-Space List</span></span>

<span data-ttu-id="9ba4a-104">La liste espace disque vous permet de calculer l’espace disque requis pour effectuer les opérations d’installation.</span><span class="sxs-lookup"><span data-stu-id="9ba4a-104">The disk-space list enables you to calculate the disk space required to complete the installation operations.</span></span> <span data-ttu-id="9ba4a-105">Après avoir créé une liste d’espace disque et y avoir ajouté des opérations de fichier, vous pouvez interroger la liste pour déterminer les lecteurs cibles spécifiés par les opérations de fichier et l’espace disque requis sur chaque lecteur.</span><span class="sxs-lookup"><span data-stu-id="9ba4a-105">After you create a disk-space list and add file operations to it, you can query the list to determine the target drives specified by the file operations, and the disk space required on each drive.</span></span>

<span data-ttu-id="9ba4a-106">En comparant l’espace nécessaire à l’espace disponible sur les disques cibles, vous pouvez déterminer par programme si un espace suffisant est disponible pour l’installation actuelle.</span><span class="sxs-lookup"><span data-stu-id="9ba4a-106">By comparing the space required to the space available on the target disks, you can programmatically determine whether sufficient space is available for the current installation.</span></span>

<span data-ttu-id="9ba4a-107">Vous pouvez ajouter ou supprimer des opérations de fichier dans la liste espace disque et recalculer l’espace disque requis.</span><span class="sxs-lookup"><span data-stu-id="9ba4a-107">You can add or remove file operations to the disk-space list and recalculate the disk space required.</span></span> <span data-ttu-id="9ba4a-108">Cette fonctionnalité vous permet, par exemple, d’écrire un programme qui interagit avec l’utilisateur, ce qui lui permet de choisir les composants qu’il souhaite installer en fonction de l’espace disque requis.</span><span class="sxs-lookup"><span data-stu-id="9ba4a-108">This functionality enables you to, for example, write a program that interacts with the user, allowing him or her to choose what components they want to install based on the disk space required.</span></span>

<span data-ttu-id="9ba4a-109">Les fonctions de liste d’espace disque vérifient automatiquement les copies préexistantes des fichiers sur le disque cible.</span><span class="sxs-lookup"><span data-stu-id="9ba4a-109">The disk-space list functions automatically check for preexisting copies of files on the target disk.</span></span> <span data-ttu-id="9ba4a-110">Si une version précédente du fichier est trouvée, les fonctions de liste d’espace disque calculent l’espace supplémentaire requis pour effectuer les opérations de fichier.</span><span class="sxs-lookup"><span data-stu-id="9ba4a-110">If a previous version of the file is found, the disk-space list functions calculate the additional space required to complete the file operations.</span></span>

<span data-ttu-id="9ba4a-111">Par exemple, si une opération de copie spécifie qu’un fichier de 6000 octets doit être copié sur le lecteur C, et qu’une version de 2000 octets de ce fichier existe déjà sur le lecteur C, les fonctions d’espace disque retourneraient un espace requis de 4000 octets.</span><span class="sxs-lookup"><span data-stu-id="9ba4a-111">For example, if a copy operation specifies that a 6000-byte file be copied to drive C, and a 2000-byte version of that file already exists on the drive C, the disk space functions would return a required space of 4000 bytes.</span></span> <span data-ttu-id="9ba4a-112">L’espace supplémentaire est utilisé pour remplacer l’ancienne version du fichier par la version la plus récente.</span><span class="sxs-lookup"><span data-stu-id="9ba4a-112">The additional space is used to replace the older version of the file with the newer version.</span></span>

<span data-ttu-id="9ba4a-113">La liste d’espace disque permet d’arrondir les tailles de fichiers aux limites du cluster de disque.</span><span class="sxs-lookup"><span data-stu-id="9ba4a-113">The disk-space list functions round file sizes to the disk cluster boundaries.</span></span>

 

 



