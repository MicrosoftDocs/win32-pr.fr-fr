---
description: Lors de l’installation d’un assembly dans un emplacement isolé pour une application spécifique, l’application doit être spécifiée dans la \_ colonne application de fichier de la table MsiAssembly.
ms.assetid: 8d7fc09c-1017-4a30-be00-b7b0e5f2a057
title: Installation et suppression d’assemblys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f44dee05940ab3c05e97a7145f9b2363226bb07c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210787"
---
# <a name="installing-and-removing-assemblies"></a><span data-ttu-id="4c9f5-103">Installation et suppression d’assemblys</span><span class="sxs-lookup"><span data-stu-id="4c9f5-103">Installing and Removing Assemblies</span></span>

<span data-ttu-id="4c9f5-104">Lors de l’installation d’un assembly dans un emplacement isolé pour une application spécifique, l’application doit être spécifiée dans la \_ colonne application de fichier de la [table MsiAssembly](msiassembly-table.md).</span><span class="sxs-lookup"><span data-stu-id="4c9f5-104">When installing an assembly to an isolated location for a specific application, the application must be specified in the File\_Application column of the [MsiAssembly table](msiassembly-table.md).</span></span> <span data-ttu-id="4c9f5-105">Ce champ est une clé de la [table de fichiers](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="4c9f5-105">This field is a key into the [File table](file-table.md).</span></span> <span data-ttu-id="4c9f5-106">Le programme d’installation utilise la structure de répertoires spécifiée dans la [table de répertoires](directory-table.md) pour installer l’assembly dans le même répertoire que le composant qui contient ce fichier.</span><span class="sxs-lookup"><span data-stu-id="4c9f5-106">The installer uses the directory structure that is specified in the [Directory table](directory-table.md) to install the assembly into the same directory as the component that contains this file.</span></span>

<span data-ttu-id="4c9f5-107">Lors de l’installation d’un assembly dans le Global Assembly Cache, la valeur dans la \_ colonne application de fichier de la [table MsiAssembly](msiassembly-table.md) doit être null.</span><span class="sxs-lookup"><span data-stu-id="4c9f5-107">When installing an assembly to the global assembly cache, the value in the File\_Application column of the [MsiAssembly Table](msiassembly-table.md) must be Null.</span></span>

<span data-ttu-id="4c9f5-108">Les sections suivantes décrivent l’installation des assemblys Win32 et common language runtime :</span><span class="sxs-lookup"><span data-stu-id="4c9f5-108">The following sections describe the installation of Win32 and common language runtime assemblies:</span></span>

-   [<span data-ttu-id="4c9f5-109">Installation d’assemblys Win32</span><span class="sxs-lookup"><span data-stu-id="4c9f5-109">Installation of Win32 Assemblies</span></span>](installation-of-win32-assemblies.md)
-   [<span data-ttu-id="4c9f5-110">Installation d’assemblys Common Language Runtime</span><span class="sxs-lookup"><span data-stu-id="4c9f5-110">Installation of Common Language Runtime Assemblies</span></span>](installation-of-common-language-runtime-assemblies.md)

 

 



