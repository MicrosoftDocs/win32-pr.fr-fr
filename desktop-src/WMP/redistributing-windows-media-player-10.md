---
title: Redistribution du lecteur Windows Media 10
description: Redistribution du lecteur Windows Media 10
ms.assetid: 58d601d4-e3d4-4a29-969c-799b2819f92c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4515317e0a6714d53c147671bbb83c06c172ef6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671473"
---
# <a name="redistributing-windows-media-player-10"></a><span data-ttu-id="6ae77-103">Redistribution du lecteur Windows Media 10</span><span class="sxs-lookup"><span data-stu-id="6ae77-103">Redistributing Windows Media Player 10</span></span>

<span data-ttu-id="6ae77-104">Vous pouvez installer le lecteur Windows Media 10 sur Windows XP en utilisant le programme d’installation suivant.</span><span class="sxs-lookup"><span data-stu-id="6ae77-104">You can install Windows Media Player 10 on Windows XP by using the following setup program.</span></span>

-   <span data-ttu-id="6ae77-105">MP10Setup.exe</span><span class="sxs-lookup"><span data-stu-id="6ae77-105">MP10Setup.exe</span></span>

<span data-ttu-id="6ae77-106">Voici un exemple de ligne de commande pour l’installation sans interface utilisateur et sans invite de redémarrage ou de redémarrage.</span><span class="sxs-lookup"><span data-stu-id="6ae77-106">Here is an example of a command line for installation with no UI and no restart or restart prompt.</span></span>


```
MP10Setup.exe /q:A /c:"setup_wm.exe /Q /R:N"
```



<span data-ttu-id="6ae77-107">Le tableau suivant présente des paramètres supplémentaires que vous pouvez utiliser avec le programme d’installation de Windows Media Player 10.</span><span class="sxs-lookup"><span data-stu-id="6ae77-107">The following table shows additional parameters that you can use with the Windows Media Player 10 setup program.</span></span>



| <span data-ttu-id="6ae77-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="6ae77-108">Parameter</span></span>              | <span data-ttu-id="6ae77-109">Description</span><span class="sxs-lookup"><span data-stu-id="6ae77-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ae77-110">/NoMigrate</span><span class="sxs-lookup"><span data-stu-id="6ae77-110">/NoMigrate</span></span>             | <span data-ttu-id="6ae77-111">Empêcher la migration de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="6ae77-111">Prevent library migration.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="6ae77-112">/NestedRestore</span><span class="sxs-lookup"><span data-stu-id="6ae77-112">/NestedRestore</span></span>         | <span data-ttu-id="6ae77-113">Créez un point de restauration système imbriqué.</span><span class="sxs-lookup"><span data-stu-id="6ae77-113">Create a nested system restore point.</span></span> <span data-ttu-id="6ae77-114">Utilisez cette valeur si votre application crée un point de restauration système pour imbriquer le point de restauration du lecteur Windows Media au sein de votre point de restauration de l’application.</span><span class="sxs-lookup"><span data-stu-id="6ae77-114">Use this if your application creates a system restore point to nest the Windows Media Player restore point within your application restore point.</span></span>                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="6ae77-115">/DisallowSystemRestore</span><span class="sxs-lookup"><span data-stu-id="6ae77-115">/DisallowSystemRestore</span></span> | <span data-ttu-id="6ae77-116">Interdire la création d’un point de restauration système.</span><span class="sxs-lookup"><span data-stu-id="6ae77-116">Disallow the creation of a system restore point.</span></span> <span data-ttu-id="6ae77-117">Cet indicateur désactive la création d’un point de restauration système.</span><span class="sxs-lookup"><span data-stu-id="6ae77-117">This flag will disable the creation of a system restore point.</span></span> <span data-ttu-id="6ae77-118">Dans la plupart des cas, cet indicateur ne doit pas être utilisé pour la redistribution de logiciels générale.</span><span class="sxs-lookup"><span data-stu-id="6ae77-118">Under most circumstances this flag should not be used for general software redistribution.</span></span> <span data-ttu-id="6ae77-119">Elle doit être utilisée uniquement lorsque vous pouvez faire un choix explicite au nom de l’utilisateur final pour ne pas prendre en charge la restauration des fichiers du lecteur Windows Media vers une version antérieure du lecteur.</span><span class="sxs-lookup"><span data-stu-id="6ae77-119">This should be used only when you can make an explicit choice on behalf of the end user not to support the rollback of the Windows Media Player files to an earlier version of the Player.</span></span> <span data-ttu-id="6ae77-120">Cet indicateur doit être utilisé uniquement pour le déploiement d’entreprise ou l’installation OEM (Original Equipment Manufacturer).</span><span class="sxs-lookup"><span data-stu-id="6ae77-120">This flag should be used only for corporate deployment or original equipment manufacturer (OEM) installation.</span></span> |
| <span data-ttu-id="6ae77-121">/DefaultService</span><span class="sxs-lookup"><span data-stu-id="6ae77-121">/DefaultService</span></span>        | <span data-ttu-id="6ae77-122">Définissez le magasin en ligne initial.</span><span class="sxs-lookup"><span data-stu-id="6ae77-122">Set the initial online store.</span></span> <span data-ttu-id="6ae77-123">Pour plus d’informations, consultez [paramètres de ligne de commande du programme d’installation pour les magasins en ligne](setup-command-line-parameters-for-online-stores.md).</span><span class="sxs-lookup"><span data-stu-id="6ae77-123">For more information, see [Setup Command-line Parameters for Online Stores](setup-command-line-parameters-for-online-stores.md).</span></span>                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="6ae77-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6ae77-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ae77-125">**Redistribution du logiciel Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="6ae77-125">**Redistributing Windows Media Player Software**</span></span>](redistributing-windows-media-player-software.md)
</dt> <dt>

[<span data-ttu-id="6ae77-126">**Document ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="6ae77-126">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 




