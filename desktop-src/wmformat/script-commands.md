---
title: Commandes de script
description: Commandes de script
ms.assetid: b8d7d4d3-c0d3-4b09-b5dd-1c6bbc3f2020
keywords:
- Windows Media Format SDK, commandes de script
- ASF (Advanced Systems Format), commandes de script
- ASF (format des systèmes avancés), commandes de script
- Windows Media Format SDK, flux de scripts
- ASF (Advanced Systems Format), flux de scripts
- ASF (format de systèmes avancés), flux de script
- Windows Media Format SDK, flux
- ASF (Advanced Systems Format), flux
- ASF (format de systèmes avancés), flux
- scripts, commandes
- scripts, flux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e57ab446a216624dc8f844f54298aeeaee358ac3
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104032062"
---
# <a name="script-commands"></a><span data-ttu-id="70685-114">Commandes de script</span><span class="sxs-lookup"><span data-stu-id="70685-114">Script Commands</span></span>

<span data-ttu-id="70685-115">Les commandes de script prises en charge par le kit de développement logiciel (SDK) Windows Media format sont des paires de chaînes nom et valeur simples.</span><span class="sxs-lookup"><span data-stu-id="70685-115">The script commands supported by the Windows Media Format SDK are simple name and value string pairs.</span></span> <span data-ttu-id="70685-116">Par exemple, une commande de script courante est « URL », qui est utilisée par le lecteur Windows Media et d’autres applications en cours d’exécution pour ouvrir des pages Web.</span><span class="sxs-lookup"><span data-stu-id="70685-116">For example, a common script command is "URL", which is used by Windows Media Player and other playing applications to open Web pages.</span></span> <span data-ttu-id="70685-117">L’autre moitié de la paire de scripts pour la commande « URL » contient une URL (Uniform Resource Locator) valide, telle que `https://www.adatum.com` .</span><span class="sxs-lookup"><span data-stu-id="70685-117">The other half of the script pair for "URL" command contains a valid uniform resource locator (URL), such as `https://www.adatum.com`.</span></span> <span data-ttu-id="70685-118">Aucune prise en charge n’est fournie par les objets de ce kit de développement logiciel (SDK) pour des commandes spécifiques. votre application doit inclure une logique pour gérer les commandes que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="70685-118">No support is provided by the objects of this SDK for any specific commands; your application must include logic to handle whatever commands you use.</span></span> <span data-ttu-id="70685-119">Vous pouvez utiliser les commandes prises en charge par le lecteur Windows Media pour assurer la compatibilité avec la plupart des joueurs.</span><span class="sxs-lookup"><span data-stu-id="70685-119">You can use the commands supported by Windows Media Player to maintain compatibility with most players.</span></span>

<span data-ttu-id="70685-120">Les commandes de script peuvent être remises de deux manières : dans un flux de script ou dans l’en-tête de fichier.</span><span class="sxs-lookup"><span data-stu-id="70685-120">Script commands can be delivered in one of two ways: in a script stream or in the file header.</span></span>

## <a name="script-streams"></a><span data-ttu-id="70685-121">Flux de script</span><span class="sxs-lookup"><span data-stu-id="70685-121">Script Streams</span></span>

<span data-ttu-id="70685-122">Vous pouvez fournir des commandes de script dans leur propre flux dans un fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="70685-122">You can deliver script commands in their own stream in an ASF file.</span></span> <span data-ttu-id="70685-123">Chaque échantillon dans un flux de script contient les deux chaînes de la paire nom/valeur.</span><span class="sxs-lookup"><span data-stu-id="70685-123">Each sample in a script stream contains the two strings of the name/value pair.</span></span> <span data-ttu-id="70685-124">L’avantage de l’utilisation d’un flux de script est que les commandes sont remises à l’heure de présentation correcte.</span><span class="sxs-lookup"><span data-stu-id="70685-124">The advantage of using a script stream is that the commands will be delivered at the correct presentation time.</span></span>

## <a name="script-commands-in-the-file-header"></a><span data-ttu-id="70685-125">Commandes de script dans l’en-tête de fichier</span><span class="sxs-lookup"><span data-stu-id="70685-125">Script Commands in the File Header</span></span>

<span data-ttu-id="70685-126">Les commandes de script peuvent être incluses dans l’en-tête de fichier pour être récupérées au moment de la lecture.</span><span class="sxs-lookup"><span data-stu-id="70685-126">Script commands can be included in the file header for retrieval at the time of playback.</span></span> <span data-ttu-id="70685-127">L’application en cours d’exécution est chargée d’exécuter les commandes de script au moment opportun.</span><span class="sxs-lookup"><span data-stu-id="70685-127">The playing application is responsible for executing the script commands at the proper time.</span></span> <span data-ttu-id="70685-128">L’avantage de l’utilisation de commandes de script dans l’en-tête de fichier est que toutes les commandes de script sont disponibles avant de commencer à recevoir des exemples.</span><span class="sxs-lookup"><span data-stu-id="70685-128">The advantage of using script commands in the file header is that all of the script commands are available before beginning to receive samples.</span></span>

## <a name="related-topics"></a><span data-ttu-id="70685-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="70685-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70685-130">**Fonctionnalités des fichiers ASF**</span><span class="sxs-lookup"><span data-stu-id="70685-130">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="70685-131">**Utilisation des commandes de script**</span><span class="sxs-lookup"><span data-stu-id="70685-131">**Using Script Commands**</span></span>](using-script-commands.md)
</dt> </dl>

 

 




