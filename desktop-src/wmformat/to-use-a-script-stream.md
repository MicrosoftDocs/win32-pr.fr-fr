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
ms.openlocfilehash: 82dee2c4a9789406c21b18c58a5f281a768fc713
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311446"
---
# <a name="to-use-a-script-stream"></a><span data-ttu-id="f3650-107">Pour utiliser un flux de script</span><span class="sxs-lookup"><span data-stu-id="f3650-107">To Use a Script Stream</span></span>

<span data-ttu-id="f3650-108">Cette section décrit comment envoyer des données de script à l’enregistreur pour les inclure dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="f3650-108">This section describes how to send script data to the writer for inclusion in a file.</span></span> <span data-ttu-id="f3650-109">Pour plus d’informations sur l’inclusion de flux de script dans des profils, consultez [configuration de types de flux arbitraires](configuring-arbitrary-stream-types.md).</span><span class="sxs-lookup"><span data-stu-id="f3650-109">For information about including script streams in profiles, see [Configuring Arbitrary Stream Types](configuring-arbitrary-stream-types.md).</span></span>

<span data-ttu-id="f3650-110">Chaque script se compose de deux chaînes, d’une chaîne de *type* et d’une chaîne d' *argument* .</span><span class="sxs-lookup"><span data-stu-id="f3650-110">Each script consists of two strings, a *type* string and an *argument* string.</span></span>

<span data-ttu-id="f3650-111">Les données du script doivent être mises en forme avant d’être envoyées au writer.</span><span class="sxs-lookup"><span data-stu-id="f3650-111">The script data must be formatted before it is sent to the writer.</span></span> <span data-ttu-id="f3650-112">Les chaînes doivent être concaténées, séparées par un caractère **null** et se terminant par un caractère **null** .</span><span class="sxs-lookup"><span data-stu-id="f3650-112">The strings should be concatenated, separated by a **NULL** character, and terminated with a **NULL** character.</span></span> <span data-ttu-id="f3650-113">L’exemple suivant montre un script légitime :</span><span class="sxs-lookup"><span data-stu-id="f3650-113">The following example shows a legitimate script:</span></span>



|     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="f3650-114">U</span><span class="sxs-lookup"><span data-stu-id="f3650-114">U</span></span>   | <span data-ttu-id="f3650-115">R</span><span class="sxs-lookup"><span data-stu-id="f3650-115">R</span></span>   | <span data-ttu-id="f3650-116">L</span><span class="sxs-lookup"><span data-stu-id="f3650-116">L</span></span>   | <span data-ttu-id="f3650-117">\\0</span><span class="sxs-lookup"><span data-stu-id="f3650-117">\\0</span></span> | <span data-ttu-id="f3650-118">h</span><span class="sxs-lookup"><span data-stu-id="f3650-118">h</span></span>   | <span data-ttu-id="f3650-119">t</span><span class="sxs-lookup"><span data-stu-id="f3650-119">t</span></span>   | <span data-ttu-id="f3650-120">t</span><span class="sxs-lookup"><span data-stu-id="f3650-120">t</span></span>   | <span data-ttu-id="f3650-121">p</span><span class="sxs-lookup"><span data-stu-id="f3650-121">p</span></span>   | <span data-ttu-id="f3650-122">:</span><span class="sxs-lookup"><span data-stu-id="f3650-122">:</span></span>   | /   | /   | <span data-ttu-id="f3650-123">w</span><span class="sxs-lookup"><span data-stu-id="f3650-123">w</span></span>   | <span data-ttu-id="f3650-124">w</span><span class="sxs-lookup"><span data-stu-id="f3650-124">w</span></span>   | <span data-ttu-id="f3650-125">w</span><span class="sxs-lookup"><span data-stu-id="f3650-125">w</span></span>   | <span data-ttu-id="f3650-126">.</span><span class="sxs-lookup"><span data-stu-id="f3650-126">.</span></span>   | <span data-ttu-id="f3650-127">a</span><span class="sxs-lookup"><span data-stu-id="f3650-127">a</span></span>   | <span data-ttu-id="f3650-128">d</span><span class="sxs-lookup"><span data-stu-id="f3650-128">d</span></span>   | <span data-ttu-id="f3650-129">a</span><span class="sxs-lookup"><span data-stu-id="f3650-129">a</span></span>   | <span data-ttu-id="f3650-130">t</span><span class="sxs-lookup"><span data-stu-id="f3650-130">t</span></span>   | <span data-ttu-id="f3650-131">u</span><span class="sxs-lookup"><span data-stu-id="f3650-131">u</span></span>   | <span data-ttu-id="f3650-132">m</span><span class="sxs-lookup"><span data-stu-id="f3650-132">m</span></span>   | <span data-ttu-id="f3650-133">.</span><span class="sxs-lookup"><span data-stu-id="f3650-133">.</span></span>   | <span data-ttu-id="f3650-134">c</span><span class="sxs-lookup"><span data-stu-id="f3650-134">c</span></span>   | <span data-ttu-id="f3650-135">o</span><span class="sxs-lookup"><span data-stu-id="f3650-135">o</span></span>   | <span data-ttu-id="f3650-136">m</span><span class="sxs-lookup"><span data-stu-id="f3650-136">m</span></span>   | <span data-ttu-id="f3650-137">\\0</span><span class="sxs-lookup"><span data-stu-id="f3650-137">\\0</span></span> |



 

<span data-ttu-id="f3650-138">Chaque paire de commandes de script doit être écrite en tant qu’exemple dans le writer.</span><span class="sxs-lookup"><span data-stu-id="f3650-138">Each pair of script commands should be written as a sample to the writer.</span></span> <span data-ttu-id="f3650-139">Pour plus d’informations sur l’écriture d’exemples, consultez [pour écrire des exemples](to-write-samples.md).</span><span class="sxs-lookup"><span data-stu-id="f3650-139">For more information about writing samples, see [To Write Samples](to-write-samples.md).</span></span>

<span data-ttu-id="f3650-140">Lorsque le fichier ASF est lu, les commandes de script sont remises par le lecteur (ou lecteur synchrone) dans l’ordre de la durée de la présentation.</span><span class="sxs-lookup"><span data-stu-id="f3650-140">When the ASF file is played, the script commands will be delivered by the reader (or synchronous reader) in presentation time order.</span></span> <span data-ttu-id="f3650-141">Il est de la responsabilité de l’application d’analyser les deux chaînes et de répondre à la commande de script.</span><span class="sxs-lookup"><span data-stu-id="f3650-141">It is the responsibility of the application to parse the two strings and respond to the script command.</span></span>

> [!Note]  
> <span data-ttu-id="f3650-142">Lorsque vous utilisez DRM pour chiffrer un fichier, aucune commande de script ne peut avoir une heure de présentation de 0.</span><span class="sxs-lookup"><span data-stu-id="f3650-142">When using DRM to encrypt a file, no script command can have a presentation time of 0.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f3650-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f3650-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3650-144">**Utilisation des commandes de script**</span><span class="sxs-lookup"><span data-stu-id="f3650-144">**Using Script Commands**</span></span>](using-script-commands.md)
</dt> </dl>

 

 




