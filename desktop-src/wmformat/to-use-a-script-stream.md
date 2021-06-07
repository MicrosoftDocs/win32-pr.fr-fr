---
title: Pour utiliser un flux de script
description: Pour utiliser un flux de script
ms.assetid: 502b1f66-213d-41d8-992a-9bef4f6209f9
keywords:
- Windows Media Format SDK, flux de scripts
- ASF (Advanced Systems Format), flux de scripts
- ASF (format de systèmes avancés), flux de script
- flux de script, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09782855bd3000d711f134c5889733e49e020c44
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444730"
---
# <a name="to-use-a-script-stream"></a><span data-ttu-id="3da4c-107">Pour utiliser un flux de script</span><span class="sxs-lookup"><span data-stu-id="3da4c-107">To Use a Script Stream</span></span>

<span data-ttu-id="3da4c-108">Cette section décrit comment envoyer des données de script à l’enregistreur pour les inclure dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="3da4c-108">This section describes how to send script data to the writer for inclusion in a file.</span></span> <span data-ttu-id="3da4c-109">Pour plus d’informations sur l’inclusion de flux de script dans des profils, consultez [configuration de types de flux arbitraires](configuring-arbitrary-stream-types.md).</span><span class="sxs-lookup"><span data-stu-id="3da4c-109">For information about including script streams in profiles, see [Configuring Arbitrary Stream Types](configuring-arbitrary-stream-types.md).</span></span>

<span data-ttu-id="3da4c-110">Chaque script se compose de deux chaînes, d’une chaîne de *type* et d’une chaîne d' *argument* .</span><span class="sxs-lookup"><span data-stu-id="3da4c-110">Each script consists of two strings, a *type* string and an *argument* string.</span></span>

<span data-ttu-id="3da4c-111">Les données du script doivent être mises en forme avant d’être envoyées au writer.</span><span class="sxs-lookup"><span data-stu-id="3da4c-111">The script data must be formatted before it is sent to the writer.</span></span> <span data-ttu-id="3da4c-112">Les chaînes doivent être concaténées, séparées par un caractère **null** et se terminant par un caractère **null** .</span><span class="sxs-lookup"><span data-stu-id="3da4c-112">The strings should be concatenated, separated by a **NULL** character, and terminated with a **NULL** character.</span></span> <span data-ttu-id="3da4c-113">L’exemple suivant montre un script légitime :</span><span class="sxs-lookup"><span data-stu-id="3da4c-113">The following example shows a legitimate script:</span></span>



| &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; |   &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp;  | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp;  | &nbsp; |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="3da4c-114">U</span><span class="sxs-lookup"><span data-stu-id="3da4c-114">U</span></span>   | <span data-ttu-id="3da4c-115">R</span><span class="sxs-lookup"><span data-stu-id="3da4c-115">R</span></span>   | <span data-ttu-id="3da4c-116">L</span><span class="sxs-lookup"><span data-stu-id="3da4c-116">L</span></span>   | &nbsp; | <span data-ttu-id="3da4c-117">h</span><span class="sxs-lookup"><span data-stu-id="3da4c-117">h</span></span>   | <span data-ttu-id="3da4c-118">t</span><span class="sxs-lookup"><span data-stu-id="3da4c-118">t</span></span>   | <span data-ttu-id="3da4c-119">t</span><span class="sxs-lookup"><span data-stu-id="3da4c-119">t</span></span>   | <span data-ttu-id="3da4c-120">p</span><span class="sxs-lookup"><span data-stu-id="3da4c-120">p</span></span>   | <span data-ttu-id="3da4c-121">:</span><span class="sxs-lookup"><span data-stu-id="3da4c-121">:</span></span>   | /   | /   | <span data-ttu-id="3da4c-122">w</span><span class="sxs-lookup"><span data-stu-id="3da4c-122">w</span></span>   | <span data-ttu-id="3da4c-123">w</span><span class="sxs-lookup"><span data-stu-id="3da4c-123">w</span></span>   | <span data-ttu-id="3da4c-124">w</span><span class="sxs-lookup"><span data-stu-id="3da4c-124">w</span></span>   | <span data-ttu-id="3da4c-125">.</span><span class="sxs-lookup"><span data-stu-id="3da4c-125">.</span></span>   | <span data-ttu-id="3da4c-126">a</span><span class="sxs-lookup"><span data-stu-id="3da4c-126">a</span></span>   | <span data-ttu-id="3da4c-127">d</span><span class="sxs-lookup"><span data-stu-id="3da4c-127">d</span></span>   | <span data-ttu-id="3da4c-128">a</span><span class="sxs-lookup"><span data-stu-id="3da4c-128">a</span></span>   | <span data-ttu-id="3da4c-129">t</span><span class="sxs-lookup"><span data-stu-id="3da4c-129">t</span></span>   | <span data-ttu-id="3da4c-130">u</span><span class="sxs-lookup"><span data-stu-id="3da4c-130">u</span></span>   | <span data-ttu-id="3da4c-131">m</span><span class="sxs-lookup"><span data-stu-id="3da4c-131">m</span></span>   | <span data-ttu-id="3da4c-132">.</span><span class="sxs-lookup"><span data-stu-id="3da4c-132">.</span></span>   | <span data-ttu-id="3da4c-133">c</span><span class="sxs-lookup"><span data-stu-id="3da4c-133">c</span></span>   | <span data-ttu-id="3da4c-134">o</span><span class="sxs-lookup"><span data-stu-id="3da4c-134">o</span></span>   | <span data-ttu-id="3da4c-135">m</span><span class="sxs-lookup"><span data-stu-id="3da4c-135">m</span></span>   | &nbsp; |



 

<span data-ttu-id="3da4c-136">Chaque paire de commandes de script doit être écrite en tant qu’exemple dans le writer.</span><span class="sxs-lookup"><span data-stu-id="3da4c-136">Each pair of script commands should be written as a sample to the writer.</span></span> <span data-ttu-id="3da4c-137">Pour plus d’informations sur l’écriture d’exemples, consultez [pour écrire des exemples](to-write-samples.md).</span><span class="sxs-lookup"><span data-stu-id="3da4c-137">For more information about writing samples, see [To Write Samples](to-write-samples.md).</span></span>

<span data-ttu-id="3da4c-138">Lorsque le fichier ASF est lu, les commandes de script sont remises par le lecteur (ou lecteur synchrone) dans l’ordre de la durée de la présentation.</span><span class="sxs-lookup"><span data-stu-id="3da4c-138">When the ASF file is played, the script commands will be delivered by the reader (or synchronous reader) in presentation time order.</span></span> <span data-ttu-id="3da4c-139">Il est de la responsabilité de l’application d’analyser les deux chaînes et de répondre à la commande de script.</span><span class="sxs-lookup"><span data-stu-id="3da4c-139">It is the responsibility of the application to parse the two strings and respond to the script command.</span></span>

> [!Note]  
> <span data-ttu-id="3da4c-140">Lorsque vous utilisez DRM pour chiffrer un fichier, aucune commande de script ne peut avoir une heure de présentation de 0.</span><span class="sxs-lookup"><span data-stu-id="3da4c-140">When using DRM to encrypt a file, no script command can have a presentation time of 0.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="3da4c-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3da4c-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3da4c-142">**Utilisation des commandes de script**</span><span class="sxs-lookup"><span data-stu-id="3da4c-142">**Using Script Commands**</span></span>](using-script-commands.md)
</dt> </dl>

 

 




