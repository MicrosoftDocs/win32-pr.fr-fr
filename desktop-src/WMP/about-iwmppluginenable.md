---
title: À propos de IWMPPluginEnable
description: À propos de IWMPPluginEnable
ms.assetid: 7611a197-f404-4cfb-88b0-05348a41ac42
keywords:
- Plug-ins du lecteur Windows Media, interfaces
- plug-ins, interfaces
- plug-ins de traitement de signal numérique, interfaces
- Plug-ins DSP, interfaces
- interfaces, plug-ins DSP
- Plug-ins du lecteur Windows Media, interface IWMPPluginEnable
- plug-ins, interface IWMPPluginEnable
- plug-ins de traitement de signal numérique, interface IWMPPluginEnable
- Plug-ins DSP, interface IWMPPluginEnable
- Interface IWMPPluginEnable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce7bf0f58be1d2623539cc5ac1329838246c8697
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939689"
---
# <a name="about-iwmppluginenable"></a><span data-ttu-id="84b4a-113">À propos de IWMPPluginEnable</span><span class="sxs-lookup"><span data-stu-id="84b4a-113">About IWMPPluginEnable</span></span>

<span data-ttu-id="84b4a-114">L’interface **IWMPPluginEnable** est requise pour les plug-ins du lecteur Windows Media DSP. **IWMPPluginEnable** contient deux méthodes qui stockent si le lecteur Windows Media a activé le plug-in DSP.</span><span class="sxs-lookup"><span data-stu-id="84b4a-114">The **IWMPPluginEnable** interface is required for Windows Media Player DSP plug-ins. **IWMPPluginEnable** contains two methods that store whether Windows Media Player has enabled the DSP plug-in.</span></span> <span data-ttu-id="84b4a-115">Le lecteur Windows Media appelle **IWMPPluginEnable :: SetEnable** lorsqu’il crée une instance du plug-in DSP, en passant la valeur **true** s’il a activé le plug-in ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="84b4a-115">Windows Media Player calls **IWMPPluginEnable::SetEnable** when it creates an instance of the DSP plug-in, passing a value of **TRUE** if it has enabled the plug-in or **FALSE** otherwise.</span></span>

<span data-ttu-id="84b4a-116">Les plug-ins DSP peuvent rester chargés même lorsque l’utilisateur choisit de les désactiver.</span><span class="sxs-lookup"><span data-stu-id="84b4a-116">DSP plug-ins may remain loaded even when the user chooses to disable them.</span></span> <span data-ttu-id="84b4a-117">Lorsqu’il est désactivé, un plug-in doit copier les données de la mémoire tampon d’entrée vers la mémoire tampon de sortie, en effectuant uniquement le traitement de la conversion de format, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="84b4a-117">When disabled, a plug-in must copy data from the input buffer to the output buffer, performing only format conversion processing, if applicable.</span></span>

<span data-ttu-id="84b4a-118">Le lecteur Windows Media appelle également cette méthode avant de libérer une instance du plug-in DSP.</span><span class="sxs-lookup"><span data-stu-id="84b4a-118">Windows Media Player also calls this method before it releases an instance of the DSP plug-in.</span></span> <span data-ttu-id="84b4a-119">Cela est utile pour permettre aux clients du plug-in de vérifier si le plug-in est actuellement activé.</span><span class="sxs-lookup"><span data-stu-id="84b4a-119">This is useful to allow clients of the plug-in to check whether the plug-in is currently enabled.</span></span> <span data-ttu-id="84b4a-120">Par exemple, un plug-in d’interface utilisateur peut modifier l’apparence de ses contrôles pour alerter l’utilisateur que le plug-in DSP n’est pas connecté.</span><span class="sxs-lookup"><span data-stu-id="84b4a-120">For instance, a user interface plug-in might change the appearance of its controls to alert the user that the DSP plug-in is not connected.</span></span>

## <a name="related-topics"></a><span data-ttu-id="84b4a-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="84b4a-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84b4a-122">**Interfaces requises**</span><span class="sxs-lookup"><span data-stu-id="84b4a-122">**Required Interfaces**</span></span>](required-interfaces.md)
</dt> </dl>

 

 




