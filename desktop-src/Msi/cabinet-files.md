---
description: Un fichier cab est un fichier unique, généralement avec une extension. cab, qui stocke les fichiers compressés dans une bibliothèque de fichiers.
ms.assetid: df240302-b875-49bf-8e62-7a35204c35fb
title: Fichiers CAB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c7b54ae737785abc33edd46c9e53edc93fcd288
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533634"
---
# <a name="cabinet-files"></a><span data-ttu-id="c2dfc-103">Fichiers CAB</span><span class="sxs-lookup"><span data-stu-id="c2dfc-103">Cabinet Files</span></span>

<span data-ttu-id="c2dfc-104">Un fichier cab est un fichier unique, généralement avec une extension. cab, qui stocke les fichiers compressés dans une bibliothèque de fichiers.</span><span class="sxs-lookup"><span data-stu-id="c2dfc-104">A cabinet is a single file, usually with a .cab extension, that stores compressed files in a file library.</span></span> <span data-ttu-id="c2dfc-105">Le format cab est un moyen efficace d’empaqueter plusieurs fichiers, car la compression est effectuée à travers les limites de fichiers, ce qui améliore considérablement le taux de compression.</span><span class="sxs-lookup"><span data-stu-id="c2dfc-105">The cabinet format is an efficient way to package multiple files because compression is performed across file boundaries, which significantly improves the compression ratio.</span></span>

<span data-ttu-id="c2dfc-106">Les développeurs peuvent utiliser un outil de création de fichier CAB comme Makecab.exe pour créer des fichiers CAB à utiliser avec des packages d’installation.</span><span class="sxs-lookup"><span data-stu-id="c2dfc-106">Developers can use a cabinet file creation tool such as Makecab.exe to make cabinet files for use with installer packages.</span></span> <span data-ttu-id="c2dfc-107">L’utilitaire Makecab.exe est inclus dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="c2dfc-107">The Makecab.exe utility is included in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

<span data-ttu-id="c2dfc-108">Les développeurs peuvent également utiliser un outil de création de fichier CAB comme Cabarc.exe pour créer des fichiers CAB à utiliser avec des packages d’installation.</span><span class="sxs-lookup"><span data-stu-id="c2dfc-108">Developers can also use a cabinet file creation tool such as Cabarc.exe to make cabinet files for use with installer packages.</span></span> <span data-ttu-id="c2dfc-109">Cet outil écrit dans la structure de l’armoire Diamond.</span><span class="sxs-lookup"><span data-stu-id="c2dfc-109">This tool writes to the Diamond cabinet structure.</span></span>

<span data-ttu-id="c2dfc-110">Les clés de fichier des fichiers stockés dans un fichier cab doivent correspondre à celles de la colonne file de la [table file](file-table.md) et la séquence de fichiers dans le fichier cab doit correspondre à la séquence de fichiers spécifiée dans la colonne Sequence.</span><span class="sxs-lookup"><span data-stu-id="c2dfc-110">The file keys of the files stored inside of a cabinet file must match the entries in the File column of the [File table](file-table.md) and the sequence of files in the cabinet must match the file sequence specified in the Sequence column.</span></span> <span data-ttu-id="c2dfc-111">Pour plus d’informations, consultez [utilisation d’armoires et de sources compressées](using-cabinets-and-compressed-sources.md).</span><span class="sxs-lookup"><span data-stu-id="c2dfc-111">For more information, see [Using Cabinets and Compressed Sources](using-cabinets-and-compressed-sources.md).</span></span>

<span data-ttu-id="c2dfc-112">Les fichiers volumineux peuvent être fractionnés entre deux fichiers CAB ou plus.</span><span class="sxs-lookup"><span data-stu-id="c2dfc-112">Large files can be split between two or more cabinet files.</span></span> <span data-ttu-id="c2dfc-113">Il ne peut pas y avoir plus de 15 fichiers dans un fichier CAB qui s’étend au fichier CAB suivant.</span><span class="sxs-lookup"><span data-stu-id="c2dfc-113">There can be no more than 15 files in any one cabinet file that spans to the next cabinet file.</span></span> <span data-ttu-id="c2dfc-114">Par exemple, si vous avez trois fichiers CAB, le premier fichier CAB peut avoir 15 fichiers qui s’étendent au deuxième fichier CAB et le second peut avoir 15 fichiers qui s’étendent au troisième fichier CAB.</span><span class="sxs-lookup"><span data-stu-id="c2dfc-114">For example, if you have three cabinet files the first cabinet can have 15 files that span to the second cabinet file and the second cabinet file can have 15 files that span to the third cabinet file.</span></span>

<span data-ttu-id="c2dfc-115">Le programme d’installation extrait les fichiers d’un fichier CAB lorsqu’ils sont nécessaires à l’installation et les installe dans le même ordre que celui dans lequel ils sont stockés dans le fichier CAB.</span><span class="sxs-lookup"><span data-stu-id="c2dfc-115">The installer extracts files from a cabinet as they are needed by the installation and installs them in the same order as they are stored in the cabinet file.</span></span> <span data-ttu-id="c2dfc-116">L’espace requis pour l’installation d’un fichier stocké dans un fichier CAB n’est pas différent de celui de l’installation d’un fichier non compressé.</span><span class="sxs-lookup"><span data-stu-id="c2dfc-116">The space requirements for installing a file stored in a cabinet are no different than for installing an uncompressed file.</span></span>

<span data-ttu-id="c2dfc-117">Un fichier CAB peut se trouver à l’intérieur ou à l’extérieur du fichier. msi.</span><span class="sxs-lookup"><span data-stu-id="c2dfc-117">A cabinet file can be located inside or outside of the .msi file.</span></span> <span data-ttu-id="c2dfc-118">À compter de Windows Installer 5,0 s’exécutant sur Windows 7 ou Windows Server 2008 R2, le programme d’installation enregistre les armoires incorporées dans le fichier. msi avant la mise en cache du package d’installation.</span><span class="sxs-lookup"><span data-stu-id="c2dfc-118">Beginning with Windows Installer 5.0 running on Windows 7 or Windows Server 2008 R2 the installer saves any cabinets that are embedded in the .msi file before caching the installation package.</span></span>

<span data-ttu-id="c2dfc-119">**[Windows Installer 4,5 ou version antérieure](not-supported-in-windows-installer-4-5.md):** Pour économiser de l’espace disque, le programme d’installation supprime toujours toutes les armoires incorporées dans le fichier. msi avant la mise en cache du package d’installation sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c2dfc-119">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** To conserve disk space, the installer always removes any cabinets that are embedded in the .msi file before caching the installation package on the user's computer.</span></span>

 

 



