---
title: Interfaces du plug-in DSP
description: Interfaces du plug-in DSP
ms.assetid: 4660f928-2e92-468f-9e2b-b411931dfded
keywords:
- Plug-ins du lecteur Windows Media, interfaces DSP
- Plug-ins du lecteur Windows Media, interfaces
- plug-ins, interfaces DSP
- plug-ins, interfaces
- plug-ins de traitement de signal numérique, interfaces
- plug-ins de traitement de signal numérique, interface ISpecifyPropertyPage
- Plug-ins DSP, interfaces
- Plug-ins DSP, interface ISpecifyPropertyPage
- interfaces, plug-ins DSP
- ISpecifyPropertyPage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5458ab945b24f8646d986ab7d5d44e12ef3249d
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/21/2020
ms.locfileid: "104381675"
---
# <a name="dsp-plug-in-interfaces"></a><span data-ttu-id="961cc-113">Interfaces du plug-in DSP</span><span class="sxs-lookup"><span data-stu-id="961cc-113">DSP Plug-in Interfaces</span></span>

<span data-ttu-id="961cc-114">Les interfaces de plug-in Digital Signal Processing (DSP) sont utilisées pour gérer le transfert de données entre le lecteur Windows Media et le plug-in.</span><span class="sxs-lookup"><span data-stu-id="961cc-114">The digital signal processing (DSP) plug-in interfaces are used to manage data transfer between Windows Media Player and the plug-in.</span></span> <span data-ttu-id="961cc-115">Tous les plug-ins DSP peuvent éventuellement implémenter l’interface **ISpecifyPropertyPage** pour fournir une implémentation de page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="961cc-115">All DSP plug-ins may optionally implement the **ISpecifyPropertyPage** interface to provide a property page implementation.</span></span>

<span data-ttu-id="961cc-116">Les interfaces suivantes sont requises pour la création de plug-ins DSP.</span><span class="sxs-lookup"><span data-stu-id="961cc-116">The following interfaces are required for creating DSP plug-ins.</span></span>



| <span data-ttu-id="961cc-117">Interface</span><span class="sxs-lookup"><span data-stu-id="961cc-117">Interface</span></span>                                                | <span data-ttu-id="961cc-118">Description</span><span class="sxs-lookup"><span data-stu-id="961cc-118">Description</span></span>                                                                                                                                            |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="961cc-119">**IMediaObject**</span><span class="sxs-lookup"><span data-stu-id="961cc-119">**IMediaObject**</span></span>                                         | <span data-ttu-id="961cc-120">Gère l’échange de données avec le lecteur Windows Media et effectue des tâches de traitement de signal numérique.</span><span class="sxs-lookup"><span data-stu-id="961cc-120">Manages data exchange with Windows Media Player and performs digital signal processing tasks.</span></span> <span data-ttu-id="961cc-121">La documentation détaillée est incluse dans le kit de développement logiciel (SDK) DirectX.</span><span class="sxs-lookup"><span data-stu-id="961cc-121">Detailed documentation is included with the DirectX SDK.</span></span> |
| [<span data-ttu-id="961cc-122">IWMPMediaPluginRegistrar</span><span class="sxs-lookup"><span data-stu-id="961cc-122">IWMPMediaPluginRegistrar</span></span>](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpmediapluginregistrar) | <span data-ttu-id="961cc-123">Gère l’inscription du plug-in.</span><span class="sxs-lookup"><span data-stu-id="961cc-123">Manages plug-in registration.</span></span>                                                                                                                          |
| [<span data-ttu-id="961cc-124">IWMPPlugin</span><span class="sxs-lookup"><span data-stu-id="961cc-124">IWMPPlugin</span></span>](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpplugin)                             | <span data-ttu-id="961cc-125">Gère la connexion au lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="961cc-125">Manages the connection to Windows Media Player.</span></span>                                                                                                        |
| [<span data-ttu-id="961cc-126">IWMPPluginEnable</span><span class="sxs-lookup"><span data-stu-id="961cc-126">IWMPPluginEnable</span></span>](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmppluginenable)                 | <span data-ttu-id="961cc-127">Stocke si le plug-in est actuellement activé par le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="961cc-127">Stores whether the plug-in is currently enabled by Windows Media Player.</span></span>                                                                               |
| [<span data-ttu-id="961cc-128">IWMPServices</span><span class="sxs-lookup"><span data-stu-id="961cc-128">IWMPServices</span></span>](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpservices)                         | <span data-ttu-id="961cc-129">Récupère des informations à partir du lecteur sur le temps de flux actuel et l’état du flux.</span><span class="sxs-lookup"><span data-stu-id="961cc-129">Retrieves information from the Player about the current stream time and stream state.</span></span>                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="961cc-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="961cc-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="961cc-131">**Référence de programmation de plug-ins DSP**</span><span class="sxs-lookup"><span data-stu-id="961cc-131">**DSP Plug-ins Programming Reference**</span></span>](dsp-plug-ins-programming-reference.md)
</dt> </dl>

 

 




