---
title: Mises à jour de l’Assistant de plug-in DSP pour le lecteur Windows Media 11
description: Mises à jour de l’Assistant de plug-in DSP pour le lecteur Windows Media 11
ms.assetid: 975c18d5-06d7-4db2-a558-bc6557963425
keywords:
- Plug-ins du lecteur Windows Media, Assistant plug-in
- plug-ins, Assistant de plug-in
- plug-ins de traitement de signal numérique, Assistant plug-in
- Plug-ins DSP, Assistant plug-in
- Assistant de plug-in
- Visual Studio, Assistant de plug-in DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a8efe798a3c324f9ecfac0a5b6021db4ea5abdf
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104381514"
---
# <a name="updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11"></a><span data-ttu-id="2eb18-109">Mises à jour de l’Assistant de plug-in DSP pour le lecteur Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="2eb18-109">Updates to the DSP Plug-in Wizard for Windows Media Player 11</span></span>

<span data-ttu-id="2eb18-110">Le kit de développement logiciel (SDK) du lecteur Windows Media 11 introduit les modifications suivantes dans l’Assistant de plug-in DSP :</span><span class="sxs-lookup"><span data-stu-id="2eb18-110">The Windows Media Player 11 SDK introduces the following changes to the DSP plug-in wizard:</span></span>

-   <span data-ttu-id="2eb18-111">Les plug-ins inscrivent le modèle de thread comme « les deux ».</span><span class="sxs-lookup"><span data-stu-id="2eb18-111">Plug-ins register the threading model as "Both".</span></span> <span data-ttu-id="2eb18-112">Cela permet au plug-in de s’exécuter dans le pipeline Media Foundation sous Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2eb18-112">This enables the plug-in to run in the Media Foundation pipeline on Windows Vista.</span></span> <span data-ttu-id="2eb18-113">Consultez le fichier *ProjectName*. RGS.</span><span class="sxs-lookup"><span data-stu-id="2eb18-113">See the *projectname*.rgs file.</span></span>

    -   <span data-ttu-id="2eb18-114">Les plug-ins audio DSP prennent en charge les deux formats supplémentaires suivants :</span><span class="sxs-lookup"><span data-stu-id="2eb18-114">Audio DSP plug-ins have support for the following two additional formats:</span></span>

    <!-- -->

    -   <span data-ttu-id="2eb18-115">\_format Wave \_ IEEE \_ float</span><span class="sxs-lookup"><span data-stu-id="2eb18-115">WAVE\_FORMAT\_IEEE\_FLOAT</span></span>
    -   <span data-ttu-id="2eb18-116">\_Format Wave \_ extensible avec SUBformat KSDATAFORMAT sous- \_ type \_ IEEE \_ float.</span><span class="sxs-lookup"><span data-stu-id="2eb18-116">WAVE\_FORMAT\_EXTENSIBLE with subformat KSDATAFORMAT\_SUBTYPE\_IEEE\_FLOAT.</span></span>

    <span data-ttu-id="2eb18-117">Consultez le fichier *ProjectName*. cpp.</span><span class="sxs-lookup"><span data-stu-id="2eb18-117">See the *projectname*.cpp file.</span></span>

    1.  <span data-ttu-id="2eb18-118">Les plug-ins de vidéo DSP prennent en charge le format vidéo NV12.</span><span class="sxs-lookup"><span data-stu-id="2eb18-118">Video DSP plug-ins have support for the NV12 video format.</span></span>
    2.  <span data-ttu-id="2eb18-119">Les plug-ins effectuent des appels supplémentaires à [IWMPMediaPluginRegistrar :: WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) et [IWMPMediaPluginRegistrar :: WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) avec un nouveau type de plug-in : WMP \_ PLUGINTYPE \_ DSP \_ OUTOFPROC.</span><span class="sxs-lookup"><span data-stu-id="2eb18-119">Plug-ins make additional calls to [IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) and [IWMPMediaPluginRegistrar::WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) with a new plug-in type: WMP\_PLUGINTYPE\_DSP\_OUTOFPROC.</span></span> <span data-ttu-id="2eb18-120">Consultez le fichier *projectnamedll*. cpp du projet.</span><span class="sxs-lookup"><span data-stu-id="2eb18-120">See the project's *projectnamedll*.cpp file.</span></span>
    3.  <span data-ttu-id="2eb18-121">Un projet supplémentaire dans chaque solution crée une DLL proxy/stub pour l’interface personnalisée des paramètres de page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="2eb18-121">An additional project in each solution creates a proxy/stub DLL for the property page settings custom interface.</span></span> <span data-ttu-id="2eb18-122">Consultez le projet *projectnamePS* .</span><span class="sxs-lookup"><span data-stu-id="2eb18-122">See the *projectnamePS* project.</span></span>
    4.  <span data-ttu-id="2eb18-123">Les appels aux méthodes déconseillées ont été modifiés pour utiliser les versions les plus récentes.</span><span class="sxs-lookup"><span data-stu-id="2eb18-123">Calls to deprecated methods have been changed to use the newest versions.</span></span>
    5.  <span data-ttu-id="2eb18-124">L’Assistant peut générer un plug-in en mode double qui fonctionne à la fois en tant qu’DMO, en implémentant **IMediaObject** et en tant que MFT, en implémentant **IMFTransform**.</span><span class="sxs-lookup"><span data-stu-id="2eb18-124">The wizard can generate a dual-mode plug-in that functions both as a DMO, by implementing **IMediaObject**, and as an MFT, by implementing **IMFTransform**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2eb18-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2eb18-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2eb18-126">**Assistant de plug-in DSP**</span><span class="sxs-lookup"><span data-stu-id="2eb18-126">**DSP Plug-in Wizard**</span></span>](dsp-plug-in-wizard.md)
</dt> </dl>

 

 




