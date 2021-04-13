---
title: Connexion au lecteur Windows Media
description: Connexion au lecteur Windows Media
ms.assetid: c6afbd95-bcf8-438a-b854-776c543a5d51
keywords:
- Plug-ins du lecteur Windows Media, entrées de Registre
- plug-ins, entrées de Registre
- Plug-ins du lecteur Windows Media, connexion
- plug-ins, connexion
- plug-ins de traitement de signal numérique, connexion
- Plug-ins DSP, connexion
- plug-ins de traitement de signal numérique, entrées de Registre
- Plug-ins DSP, entrées de Registre
- Registre, plug-ins DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8fa0851e271631e2c37bf716c427b5af34ade14
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104381474"
---
# <a name="connecting-to-windows-media-player"></a><span data-ttu-id="f379d-112">Connexion au lecteur Windows Media</span><span class="sxs-lookup"><span data-stu-id="f379d-112">Connecting to Windows Media Player</span></span>

<span data-ttu-id="f379d-113">Le lecteur Windows Media se connecte automatiquement aux plug-ins DSP qui ont été installés et correctement inscrits.</span><span class="sxs-lookup"><span data-stu-id="f379d-113">Windows Media Player automatically connects to DSP plug-ins that have been installed and properly registered.</span></span> <span data-ttu-id="f379d-114">Les plug-ins DSP doivent appeler [IWMPMediaPluginRegistrar :: WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) pour créer les entrées de Registre nécessaires pour permettre au lecteur Windows Media de reconnaître le plug-in et de le répertorier sous l’onglet **plug-ins** de la boîte de dialogue Options.</span><span class="sxs-lookup"><span data-stu-id="f379d-114">DSP plug-ins must call [IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) to create the registry entries necessary to allow Windows Media Player to recognize the plug-in and to list it on the **Plug-ins** tab of the Options dialog box.</span></span> <span data-ttu-id="f379d-115">Pour supprimer les entrées de Registre créées par **IWMPMediaPluginRegistrar :: WMPRegisterPlayerPlugin**, le plug-in appelle [IWMPMediaPluginRegistrar :: WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin).</span><span class="sxs-lookup"><span data-stu-id="f379d-115">To remove the registry entries created by **IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin**, the plug-in calls [IWMPMediaPluginRegistrar::WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f379d-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f379d-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f379d-117">**Vue d’ensemble des développeurs de plug-ins DSP**</span><span class="sxs-lookup"><span data-stu-id="f379d-117">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




