---
title: Redistribution du lecteur Windows Media 11
description: Redistribution du lecteur Windows Media 11
ms.assetid: 3348821f-6d72-40c2-954b-0046ce502401
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 674da0298196f0749a549670bf9bd7c4095b6e7a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028984"
---
# <a name="redistributing-windows-media-player-11"></a><span data-ttu-id="d7b94-103">Redistribution du lecteur Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="d7b94-103">Redistributing Windows Media Player 11</span></span>

<span data-ttu-id="d7b94-104">Vous pouvez installer le lecteur Windows Media 11 sur Windows XP en utilisant l’un des programmes d’installation suivants, où *LocaleID* est un identificateur de paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="d7b94-104">You can install Windows Media Player 11 on Windows XP by using one of the following setup programs, where *localeId* is a locale identifier.</span></span>

-   <span data-ttu-id="d7b94-105">WMP11-WindowsXP-x86-*LocaleID*. exe</span><span class="sxs-lookup"><span data-stu-id="d7b94-105">wmp11-windowsxp-x86-*localeId*.exe</span></span>
-   <span data-ttu-id="d7b94-106">WMP11-WindowsXP-x64-*LocaleID*. exe</span><span class="sxs-lookup"><span data-stu-id="d7b94-106">wmp11-windowsxp-x64-*localeId*.exe</span></span>

<span data-ttu-id="d7b94-107">Voici un exemple de ligne de commande pour l’installation sans interface utilisateur et sans invite de redémarrage ou de redémarrage.</span><span class="sxs-lookup"><span data-stu-id="d7b94-107">Here is an example of a command line for installation with no UI and no restart or restart prompt.</span></span>


```
wmp11-windowsxp-x86-enu.exe /q:A /c:"setup_wm.exe /Q /R:N"
```



<span data-ttu-id="d7b94-108">Le tableau suivant présente des paramètres supplémentaires que vous pouvez utiliser avec le programme d’installation du lecteur Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="d7b94-108">The following table shows additional parameters that you can use with the Windows Media Player 11 setup program.</span></span>



| <span data-ttu-id="d7b94-109">Paramètre</span><span class="sxs-lookup"><span data-stu-id="d7b94-109">Parameter</span></span>              | <span data-ttu-id="d7b94-110">Description</span><span class="sxs-lookup"><span data-stu-id="d7b94-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7b94-111">/NoMigrate</span><span class="sxs-lookup"><span data-stu-id="d7b94-111">/NoMigrate</span></span>             | <span data-ttu-id="d7b94-112">Empêcher la migration de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="d7b94-112">Prevent library migration.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="d7b94-113">/NestedRestore</span><span class="sxs-lookup"><span data-stu-id="d7b94-113">/NestedRestore</span></span>         | <span data-ttu-id="d7b94-114">Créez un point de restauration système imbriqué.</span><span class="sxs-lookup"><span data-stu-id="d7b94-114">Create a nested system restore point.</span></span> <span data-ttu-id="d7b94-115">Utilisez cette valeur si votre application crée un point de restauration système pour imbriquer le point de restauration du lecteur Windows Media au sein de votre point de restauration de l’application.</span><span class="sxs-lookup"><span data-stu-id="d7b94-115">Use this if your application creates a system restore point to nest the Windows Media Player restore point within your application restore point.</span></span>                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="d7b94-116">/DisallowSystemRestore</span><span class="sxs-lookup"><span data-stu-id="d7b94-116">/DisallowSystemRestore</span></span> | <span data-ttu-id="d7b94-117">Interdire la création d’un point de restauration système.</span><span class="sxs-lookup"><span data-stu-id="d7b94-117">Disallow the creation of a system restore point.</span></span> <span data-ttu-id="d7b94-118">Cet indicateur désactive la création d’un point de restauration système.</span><span class="sxs-lookup"><span data-stu-id="d7b94-118">This flag will disable the creation of a system restore point.</span></span> <span data-ttu-id="d7b94-119">Dans la plupart des cas, cet indicateur ne doit pas être utilisé pour la redistribution de logiciels générale.</span><span class="sxs-lookup"><span data-stu-id="d7b94-119">Under most circumstances this flag should not be used for general software redistribution.</span></span> <span data-ttu-id="d7b94-120">Elle doit être utilisée uniquement lorsque vous pouvez faire un choix explicite au nom de l’utilisateur final pour ne pas prendre en charge la restauration des fichiers du lecteur Windows Media vers une version antérieure du lecteur.</span><span class="sxs-lookup"><span data-stu-id="d7b94-120">This should be used only when you can make an explicit choice on behalf of the end user not to support the rollback of the Windows Media Player files to an earlier version of the Player.</span></span> <span data-ttu-id="d7b94-121">Cet indicateur doit être utilisé uniquement pour le déploiement d’entreprise ou l’installation OEM (Original Equipment Manufacturer).</span><span class="sxs-lookup"><span data-stu-id="d7b94-121">This flag should be used only for corporate deployment or original equipment manufacturer (OEM) installation.</span></span> |
| <span data-ttu-id="d7b94-122">/DefaultService</span><span class="sxs-lookup"><span data-stu-id="d7b94-122">/DefaultService</span></span>        | <span data-ttu-id="d7b94-123">Définissez le magasin en ligne initial.</span><span class="sxs-lookup"><span data-stu-id="d7b94-123">Set the initial online store.</span></span> <span data-ttu-id="d7b94-124">Pour plus d’informations, consultez [paramètres de ligne de commande du programme d’installation pour les magasins en ligne](setup-command-line-parameters-for-online-stores.md).</span><span class="sxs-lookup"><span data-stu-id="d7b94-124">For more information, see [Setup Command-line Parameters for Online Stores](setup-command-line-parameters-for-online-stores.md).</span></span>                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="d7b94-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d7b94-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7b94-126">**Redistribution du logiciel Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="d7b94-126">**Redistributing Windows Media Player Software**</span></span>](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




