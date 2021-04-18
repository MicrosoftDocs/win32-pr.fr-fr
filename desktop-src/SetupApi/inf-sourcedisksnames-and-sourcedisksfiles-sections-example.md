---
description: La section SourceDisksNames d’un fichier INF identifie les disques qui contiennent les fichiers sources en cours d’installation.
ms.assetid: af4bc466-f0a3-4f83-adb7-6bfc276f7764
title: Exemple de sections INF SourceDisksNames et SourceDisksFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f991727a8a2ca9cce2bd2d7161dfbf27b62ce74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519434"
---
# <a name="inf-sourcedisksnames-and-sourcedisksfiles-sections-example"></a><span data-ttu-id="5e654-103">Exemple de sections INF SourceDisksNames et SourceDisksFiles</span><span class="sxs-lookup"><span data-stu-id="5e654-103">INF SourceDisksNames and SourceDisksFiles Sections Example</span></span>

<span data-ttu-id="5e654-104">La section **SourceDisksNames** d’un fichier INF identifie les disques qui contiennent les fichiers sources en cours d’installation.</span><span class="sxs-lookup"><span data-stu-id="5e654-104">The **SourceDisksNames** section of an INF file identifies the disks that contain the source files being installed.</span></span> <span data-ttu-id="5e654-105">La section **SourceDisksFiles** identifie les fichiers sources et les disques sources qui les contiennent.</span><span class="sxs-lookup"><span data-stu-id="5e654-105">The **SourceDisksFiles** section identifies the source files and the source disks that contain them.</span></span> <span data-ttu-id="5e654-106">Notez que les plateformes MIPS, alpha et PPC ne sont pas prises en charge par Windows 2000 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5e654-106">Note that MIPS, Alpha, and PPC platforms are not supported by Windows 2000 or Windows XP.</span></span>

<span data-ttu-id="5e654-107">À partir de Windows XP, une section **SourceDisksNames** peut spécifier une balise et un fichier CAB.</span><span class="sxs-lookup"><span data-stu-id="5e654-107">Beginning with Windows XP, a **SourceDisksNames** section may specify a tag as well as cabinet file.</span></span> <span data-ttu-id="5e654-108">Par exemple, la section **SourceDisksNames** suivante peut être utilisée avec un média fixe ou amovible.</span><span class="sxs-lookup"><span data-stu-id="5e654-108">For example, the following **SourceDisksNames** section may be used with removable or fixed media.</span></span> <span data-ttu-id="5e654-109">Si vous utilisez un support amovible, la section exemple vérifie la présence du média en vérifiant d’abord la présence de la balise.</span><span class="sxs-lookup"><span data-stu-id="5e654-109">If using removable media, the example section verifies the presence of the media by first checking for the presence of the tag.</span></span> <span data-ttu-id="5e654-110">Si vous utilisez un média fixe, la section exemple vérifie la présence du média en vérifiant d’abord la présence du fichier CAB.</span><span class="sxs-lookup"><span data-stu-id="5e654-110">If using fixed media, the example section verifies the presence of the media by first checking for the presence of the cabinet.</span></span> <span data-ttu-id="5e654-111">Après vérification de la présence d’un fichier CAB, le système tente de copier les fichiers en dehors de l’armoire et demande tous les fichiers qu’il n’a pas pu copier.</span><span class="sxs-lookup"><span data-stu-id="5e654-111">After verifying the presence of a cabinet, the system attempts to copy files out of the cabinet and prompts for any files it was unable to copy.</span></span>

``` syntax
[SourceDisksNames]
1="Dajava" , "Dajava.cab",,, 0x10,"Dajava.tag"
```

<span data-ttu-id="5e654-112">Pour plus d’informations sur **SourceDisksNames** ou **SourceDisksFiles**, consultez les sections « instructions générales pour le fichier INF » et « sections et directives du fichier INF » du kit de développement de pilotes Microsoft Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="5e654-112">For more information about **SourceDisksNames** or **SourceDisksFiles**, see the "General Guidelines for INF File" and "INF File Sections and Directives" sections of the Microsoft Windows 2000 Driver Development Kit.</span></span>

 

 



