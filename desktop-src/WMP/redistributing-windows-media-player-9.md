---
title: Redistribution du lecteur Windows Media série 9
description: Redistribution du lecteur Windows Media série 9
ms.assetid: 812e3fc7-e23d-489c-a486-62c7602cf46e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62f48da20123255ae08a0993d361a95deb8ed335
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029753"
---
# <a name="redistributing-windows-media-player-9-series"></a><span data-ttu-id="3a27f-103">Redistribution du lecteur Windows Media série 9</span><span class="sxs-lookup"><span data-stu-id="3a27f-103">Redistributing Windows Media Player 9 Series</span></span>

<span data-ttu-id="3a27f-104">Vous pouvez installer le lecteur Windows Media 9 sur Windows XP en utilisant l’un des programmes d’installation suivants.</span><span class="sxs-lookup"><span data-stu-id="3a27f-104">You can install Windows Media Player 9 Series on Windows XP by using one of the following setup programs.</span></span>

-   <span data-ttu-id="3a27f-105">MPSetupXP.exe</span><span class="sxs-lookup"><span data-stu-id="3a27f-105">MPSetupXP.exe</span></span>
-   <span data-ttu-id="3a27f-106">MPSetup.exe</span><span class="sxs-lookup"><span data-stu-id="3a27f-106">MPSetup.exe</span></span>

> [!Note]  
> <span data-ttu-id="3a27f-107">MPSetup.exe est un sur-ensemble du programme d’installation de MPSetupXP.exe.</span><span class="sxs-lookup"><span data-stu-id="3a27f-107">MPSetup.exe is a superset of the MPSetupXP.exe setup program.</span></span> <span data-ttu-id="3a27f-108">Il contient les fichiers nécessaires aux systèmes d’exploitation antérieurs à Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3a27f-108">It contains files that are needed by operating systems released before Windows XP.</span></span> <span data-ttu-id="3a27f-109">MPSetup.exe est fonctionnellement équivalente à MPSetupXP.exe lorsqu’il est exécuté sur Windows XP, mais la taille du fichier du programme d’installation est plus importante car elle n’a pas été optimisée pour l’installation sur les systèmes d’exploitation Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3a27f-109">MPSetup.exe is functionally equivalent to MPSetupXP.exe when run on Windows XP, but the setup program file size is larger because it has not been optimized for installation on Windows XP operating systems.</span></span>

 

<span data-ttu-id="3a27f-110">Vous pouvez installer le lecteur Windows Media 9 sur Windows 98 Deuxième édition, Windows Millennium Edition ou Windows 2000 à l’aide du programme d’installation suivant.</span><span class="sxs-lookup"><span data-stu-id="3a27f-110">You can install Windows Media Player 9 Series on Windows 98 Second Edition, Windows Millennium Edition or Windows 2000 by using the following setup program.</span></span>

-   <span data-ttu-id="3a27f-111">MPSetup.exe</span><span class="sxs-lookup"><span data-stu-id="3a27f-111">MPSetup.exe</span></span>

<span data-ttu-id="3a27f-112">Voici un exemple de ligne de commande pour l’installation sans interface utilisateur et sans invite de redémarrage ou de redémarrage.</span><span class="sxs-lookup"><span data-stu-id="3a27f-112">Here is an example of a command line for installation with no UI and no restart or restart prompt.</span></span>


```
MPSetup.exe /q:A /c:"setup_wm.exe /Q /R:N /P:#e"
```



> [!Note]  
> <span data-ttu-id="3a27f-113">Le paramètre/P : \# e spécifie que le package d’installation du lecteur Windows Media doit être mis en cache lors de l’installation du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="3a27f-113">The /P:\#e parameter specifies that the Windows Media Player installation package should be cached during Windows Media Player setup.</span></span> <span data-ttu-id="3a27f-114">Cette commande est utilisée pour gérer les futures mises à niveau du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="3a27f-114">This command is used to handle future upgrades of the operating system.</span></span> <span data-ttu-id="3a27f-115">Cette commande ne doit être omise que par les administrateurs informatiques de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="3a27f-115">This command should be omitted only by corporate IT administrators.</span></span> <span data-ttu-id="3a27f-116">Le seul cas où/P : \# e ne doit pas être inclus sur la ligne de commande est lorsque vous êtes propriétaire du système cible et que vous savez que le système cible ne sera jamais mis à niveau vers un système d’exploitation ultérieur.</span><span class="sxs-lookup"><span data-stu-id="3a27f-116">The only case where /P:\#e should not be included on the command line is when you own the target system and know that the target system will never be upgraded to a later operating system.</span></span> <span data-ttu-id="3a27f-117">Par exemple, si vous installez le lecteur Windows Media 9 sur Windows 2000 et que l’ordinateur a peut-être été mis à niveau vers Windows XP, vous devez utiliser/P : \# e sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="3a27f-117">For example, if you are installing Windows Media Player 9 Series on Windows 2000 and the computer may someday be upgraded to Windows XP, you must use /P:\#e on the command line.</span></span> <span data-ttu-id="3a27f-118">Dans le cas contraire, après l’installation de Windows XP, les fichiers du lecteur Windows Media seront remplacés par les fichiers du lecteur Windows Media pour Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3a27f-118">Otherwise, after the Windows XP installation, the Windows Media Player files will be overwritten with the files for Windows Media Player for Windows XP.</span></span>

 

<span data-ttu-id="3a27f-119">Le tableau suivant présente des paramètres supplémentaires que vous pouvez utiliser avec le programme d’installation de Windows Media Player 9 Series.</span><span class="sxs-lookup"><span data-stu-id="3a27f-119">The following table shows additional parameters that you can use with the Windows Media Player 9 Series setup program.</span></span>



| <span data-ttu-id="3a27f-120">Paramètre</span><span class="sxs-lookup"><span data-stu-id="3a27f-120">Parameter</span></span>              | <span data-ttu-id="3a27f-121">Description</span><span class="sxs-lookup"><span data-stu-id="3a27f-121">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a27f-122">/NoMigrate</span><span class="sxs-lookup"><span data-stu-id="3a27f-122">/NoMigrate</span></span>             | <span data-ttu-id="3a27f-123">Empêcher la migration de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="3a27f-123">Prevent library migration.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="3a27f-124">/NestedRestore</span><span class="sxs-lookup"><span data-stu-id="3a27f-124">/NestedRestore</span></span>         | <span data-ttu-id="3a27f-125">Créez un point de restauration système imbriqué.</span><span class="sxs-lookup"><span data-stu-id="3a27f-125">Create a nested system restore point.</span></span> <span data-ttu-id="3a27f-126">Utilisez cette valeur si votre application crée un point de restauration système pour imbriquer le point de restauration du lecteur Windows Media au sein de votre point de restauration de l’application.</span><span class="sxs-lookup"><span data-stu-id="3a27f-126">Use this if your application creates a system restore point to nest the Windows Media Player restore point within your application restore point.</span></span>                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="3a27f-127">/DisallowSystemRestore</span><span class="sxs-lookup"><span data-stu-id="3a27f-127">/DisallowSystemRestore</span></span> | <span data-ttu-id="3a27f-128">Interdire la création d’un point de restauration système.</span><span class="sxs-lookup"><span data-stu-id="3a27f-128">Disallow the creation of a system restore point.</span></span> <span data-ttu-id="3a27f-129">Cet indicateur désactive la création d’un point de restauration système.</span><span class="sxs-lookup"><span data-stu-id="3a27f-129">This flag will disable the creation of a system restore point.</span></span> <span data-ttu-id="3a27f-130">Dans la plupart des cas, cet indicateur ne doit pas être utilisé pour la redistribution de logiciels générale.</span><span class="sxs-lookup"><span data-stu-id="3a27f-130">Under most circumstances this flag should not be used for general software redistribution.</span></span> <span data-ttu-id="3a27f-131">Elle doit être utilisée uniquement lorsque vous pouvez faire un choix explicite au nom de l’utilisateur final pour ne pas prendre en charge la restauration des fichiers du lecteur Windows Media vers une version antérieure du lecteur.</span><span class="sxs-lookup"><span data-stu-id="3a27f-131">This should be used only when you can make an explicit choice on behalf of the end user not to support the rollback of the Windows Media Player files to an earlier version of the Player.</span></span> <span data-ttu-id="3a27f-132">Cet indicateur doit être utilisé uniquement pour le déploiement d’entreprise ou l’installation OEM (Original Equipment Manufacturer).</span><span class="sxs-lookup"><span data-stu-id="3a27f-132">This flag should be used only for corporate deployment or original equipment manufacturer (OEM) installation.</span></span> |



 

## <a name="notes"></a><span data-ttu-id="3a27f-133">Notes</span><span class="sxs-lookup"><span data-stu-id="3a27f-133">Notes</span></span>

-   <span data-ttu-id="3a27f-134">Les paramètres de ligne de commande respectent la casse.</span><span class="sxs-lookup"><span data-stu-id="3a27f-134">The command-line parameters are case-sensitive.</span></span>
-   <span data-ttu-id="3a27f-135">Lorsque vous supprimez l’invite de redémarrage, vous devez vérifier la clé de Registre InstallResult et gérer la notification de redémarrage dans l’application d’installation appelante.</span><span class="sxs-lookup"><span data-stu-id="3a27f-135">When suppressing the restart prompt, you must check the InstallResult registry key and handle restart notification in the calling setup application.</span></span>
-   <span data-ttu-id="3a27f-136">Le lecteur Windows Media 9 installe également le runtime Windows Media format. il n’est donc pas nécessaire d’inclure à la fois le package de distribution du lecteur Windows Media et le package de distribution du format d’exécution Windows Media dans le même package de redistribution de logiciels.</span><span class="sxs-lookup"><span data-stu-id="3a27f-136">Windows Media Player 9 Series also installs the Windows Media Format runtime, so there is no need to include both the Windows Media Player distribution package and the Windows Media Format runtime distribution package in the same software redistribution package.</span></span> <span data-ttu-id="3a27f-137">Par conséquent, si vous incluez des MPSetup.exe ou des MPSetupXP.exe dans votre installation, vous n’avez pas besoin d’inclure de WMFdist.exe.</span><span class="sxs-lookup"><span data-stu-id="3a27f-137">Therefore, if you include MPSetup.exe or MPSetupXP.exe in your installation, you do not need to include WMFdist.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3a27f-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3a27f-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a27f-139">**Redistribution du logiciel Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="3a27f-139">**Redistributing Windows Media Player Software**</span></span>](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




