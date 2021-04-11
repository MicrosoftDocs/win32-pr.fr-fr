---
title: Utilisation des commandes de script
description: Utilisation des commandes de script
ms.assetid: be8a2d22-35cb-4b8d-ad00-e8a45bb85b39
keywords:
- Windows Media Format SDK, commandes de script
- ASF (Advanced Systems Format), commandes de script
- ASF (format des systèmes avancés), commandes de script
- scripts, commandes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad2e840a677e58a1be528e84e4ed1b4be7fe3619
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029293"
---
# <a name="using-script-commands"></a><span data-ttu-id="4b5d1-107">Utilisation des commandes de script</span><span class="sxs-lookup"><span data-stu-id="4b5d1-107">Using Script Commands</span></span>

<span data-ttu-id="4b5d1-108">Le kit de développement logiciel (SDK) Windows Media format prend en charge l’utilisation de commandes de script pour communiquer des actions d’application dans des fichiers ASF.</span><span class="sxs-lookup"><span data-stu-id="4b5d1-108">The Windows Media Format SDK supports the use of script commands to communicate application actions in ASF files.</span></span> <span data-ttu-id="4b5d1-109">Chaque commande de script est composée de deux chaînes, la première est le type de commande, la seconde est celle des données de commande.</span><span class="sxs-lookup"><span data-stu-id="4b5d1-109">Each script command is made up of two strings, the first string is the type of command, the second is the command data.</span></span> <span data-ttu-id="4b5d1-110">Par exemple, vous pouvez utiliser le type de script « URL » et transmettre une URL Internet valide en tant que données de commande.</span><span class="sxs-lookup"><span data-stu-id="4b5d1-110">For example, you can use the script type "URL" and pass a valid Internet URL as the command data.</span></span> <span data-ttu-id="4b5d1-111">Lorsqu’une application de lecture qui prend en charge les commandes de script de type « URL » reçoit cette commande, elle ouvre l’adresse spécifiée dans une fenêtre de navigateur.</span><span class="sxs-lookup"><span data-stu-id="4b5d1-111">When a reading application that supports script commands of type "URL" receives this command, it will open the specified address in a browser window.</span></span>

<span data-ttu-id="4b5d1-112">Le kit de développement logiciel (SDK) du format Windows Media offre deux options de diffusion de script dans des fichiers ASF.</span><span class="sxs-lookup"><span data-stu-id="4b5d1-112">The Windows Media Format SDK provides two options for delivering script in ASF files.</span></span> <span data-ttu-id="4b5d1-113">Vous pouvez créer un flux de script ou inclure des commandes de script dans l’en-tête du fichier.</span><span class="sxs-lookup"><span data-stu-id="4b5d1-113">You can create a script stream or you can include script commands in the header of the file.</span></span> <span data-ttu-id="4b5d1-114">Les flux de script sont utiles car les commandes de script sont fournies dans l’ordre chronologique des présentations.</span><span class="sxs-lookup"><span data-stu-id="4b5d1-114">Script streams are useful because the script commands are delivered in presentation time order.</span></span> <span data-ttu-id="4b5d1-115">Si vous utilisez des commandes de script dans l’en-tête de fichier, votre application doit récupérer toutes les commandes de script avant de commencer la lecture.</span><span class="sxs-lookup"><span data-stu-id="4b5d1-115">If you use script commands in the file header, your application will need to retrieve all of the script commands before starting playback.</span></span> <span data-ttu-id="4b5d1-116">Vous devez suivre les durées de présentation des commandes de script et y répondre au bon moment.</span><span class="sxs-lookup"><span data-stu-id="4b5d1-116">You must keep track of the presentation times of script commands and respond to them at the right time.</span></span>

<span data-ttu-id="4b5d1-117">Les sections suivantes décrivent comment inclure des commandes de script dans un fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="4b5d1-117">The following sections describe how to include script commands in an ASF file.</span></span>



| <span data-ttu-id="4b5d1-118">Section</span><span class="sxs-lookup"><span data-stu-id="4b5d1-118">Section</span></span>                                                                                                                | <span data-ttu-id="4b5d1-119">Description</span><span class="sxs-lookup"><span data-stu-id="4b5d1-119">Description</span></span>                                                  |
|------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="4b5d1-120">Pour utiliser un flux de script</span><span class="sxs-lookup"><span data-stu-id="4b5d1-120">To Use a Script Stream</span></span>](to-use-a-script-stream.md)                                                                   | <span data-ttu-id="4b5d1-121">Décrit comment inclure des commandes de script dans un flux de script.</span><span class="sxs-lookup"><span data-stu-id="4b5d1-121">Describes how to include script commands in a script stream.</span></span> |
| [<span data-ttu-id="4b5d1-122">Pour ajouter des données de script à l’en-tête</span><span class="sxs-lookup"><span data-stu-id="4b5d1-122">To Add Script Data to the Header</span></span>](to-add-script-data-to-the-header.md)                                               | <span data-ttu-id="4b5d1-123">Décrit comment inclure des commandes de script dans l’en-tête de fichier.</span><span class="sxs-lookup"><span data-stu-id="4b5d1-123">Describes how to include script commands in the file header.</span></span> |
| [<span data-ttu-id="4b5d1-124">Utilisation de commandes de script prises en charge par le lecteur Windows Media</span><span class="sxs-lookup"><span data-stu-id="4b5d1-124">Using Script Commands Supported by Windows Media Player</span></span>](using-script-commands-supported-by-windows-media-player.md) | <span data-ttu-id="4b5d1-125">Décrit les commandes de script utilisées par le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="4b5d1-125">Describes the script commands used by Windows Media Player.</span></span>  |



 

> [!Note]  
> <span data-ttu-id="4b5d1-126">Dans les versions précédentes du kit de développement logiciel (SDK) de format Windows Media, les flux de script étaient utilisés pour ouvrir des adresses Web correspondant au contenu d’un fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="4b5d1-126">In previous versions of the Windows Media Format SDK, script streams were used to open Web addresses corresponding to the content of an ASF file.</span></span> <span data-ttu-id="4b5d1-127">Vous pouvez désormais utiliser des flux Web pour travailler avec des pages Web synchronisées.</span><span class="sxs-lookup"><span data-stu-id="4b5d1-127">You can now use Web streams to work with synchronized Web pages.</span></span> <span data-ttu-id="4b5d1-128">Pour plus d’informations, consultez</span><span class="sxs-lookup"><span data-stu-id="4b5d1-128">For more information.</span></span> <span data-ttu-id="4b5d1-129">consultez [flux Web](web-streams.md).</span><span class="sxs-lookup"><span data-stu-id="4b5d1-129">see [Web Streams](web-streams.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="4b5d1-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4b5d1-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b5d1-131">**Commandes de script**</span><span class="sxs-lookup"><span data-stu-id="4b5d1-131">**Script Commands**</span></span>](script-commands.md)
</dt> <dt>

[<span data-ttu-id="4b5d1-132">**Guide de programmation**</span><span class="sxs-lookup"><span data-stu-id="4b5d1-132">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 




