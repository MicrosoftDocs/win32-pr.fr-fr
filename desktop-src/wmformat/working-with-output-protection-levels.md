---
title: Utilisation des niveaux de protection de sortie
description: Utilisation des niveaux de protection de sortie
ms.assetid: ec5982cd-0b87-4081-98e2-ab2d102a36d8
keywords:
- Windows Media Format SDK, niveaux de protection de sortie (OPL)
- Windows Media Format SDK, niveaux de protection
- ASF (Advanced Systems Format), niveaux de protection de sortie (OPL)
- ASF (format des systèmes avancés), niveaux de protection de la sortie (OPL)
- ASF (Advanced Systems Format), niveaux de protection
- ASF (format des systèmes avancés), niveaux de protection
- ASF (Advanced Systems Format), plusieurs licences
- ASF (Advanced Systems Format), plusieurs licences
- gestion des droits numériques (DRM), niveaux de protection de sortie (OPL)
- DRM (gestion des droits numériques), niveaux de protection de sortie (OPL)
- gestion des droits numériques (DRM), niveaux de protection
- DRM (gestion des droits numériques), niveaux de protection
- gestion des droits numériques (DRM), évaluation des niveaux de protection de sortie (OPL)
- DRM (Digital Rights Management), évaluation des niveaux de protection de sortie (OPL)
- gestion des droits numériques (DRM), plusieurs licences
- DRM (gestion des droits numériques), plusieurs licences
- niveaux de protection de sortie (OPL)
- OPL (niveaux de protection de sortie)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aab7023cc8285e5f3993aac69c57deca9675d9dd
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314221"
---
# <a name="working-with-output-protection-levels"></a><span data-ttu-id="c2756-121">Utilisation des niveaux de protection de sortie</span><span class="sxs-lookup"><span data-stu-id="c2756-121">Working with Output Protection Levels</span></span>

<span data-ttu-id="c2756-122">Les licences créées à l’aide du kit de développement logiciel (SDK) Windows Media Rights Manager 10 peuvent spécifier des restrictions d’action à l’aide des niveaux de protection de sortie (OPLs).</span><span class="sxs-lookup"><span data-stu-id="c2756-122">Licenses created by using the Windows Media Rights Manager 10 SDK can specify action restrictions using output protection levels (OPLs).</span></span> <span data-ttu-id="c2756-123">OPLs permet à un créateur de licence d’autoriser certaines actions uniquement sur des appareils avec des technologies spécifiques.</span><span class="sxs-lookup"><span data-stu-id="c2756-123">OPLs enable a license creator to allow some actions only on devices with specific technologies.</span></span> <span data-ttu-id="c2756-124">Les avantages de l’utilisation de OPLs sont que vous bénéficiez d’une plus grande flexibilité pour créer des restrictions de licence que les versions précédentes.</span><span class="sxs-lookup"><span data-stu-id="c2756-124">The benefits of using OPLs is that you get more flexibility in creating license restrictions than previous versions.</span></span> <span data-ttu-id="c2756-125">En outre, les OPLs sont extensibles pour s’adapter aux futures technologies.</span><span class="sxs-lookup"><span data-stu-id="c2756-125">In addition, OPLs are expandable to accommodate future technologies.</span></span> <span data-ttu-id="c2756-126">Vous pouvez prendre en charge ces licences dans vos applications à l’aide des méthodes de l’interface [**IWMDRMReader2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2) .</span><span class="sxs-lookup"><span data-stu-id="c2756-126">You can support such licenses in your applications by using the methods of the [**IWMDRMReader2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2) interface.</span></span>

<span data-ttu-id="c2756-127">Pour lire les fichiers qui sont protégés par une licence qui spécifie OPLs, vous devez vérifier la OPL de l’action souhaitée.</span><span class="sxs-lookup"><span data-stu-id="c2756-127">To read files that are protected by a license that specifies OPLs, you must check the OPL for the desired action.</span></span> <span data-ttu-id="c2756-128">La technologie de sortie utilisée par votre application doit être autorisée par le OPL dans la licence.</span><span class="sxs-lookup"><span data-stu-id="c2756-128">The output technology your application is using must be allowed by the OPL in the license.</span></span> <span data-ttu-id="c2756-129">Par exemple, certaines licences pour le contenu audio protégé peuvent nécessiter l’utilisation d’un chemin d’accès audio sécurisé pour le lire.</span><span class="sxs-lookup"><span data-stu-id="c2756-129">For example, some licenses for protected audio may require that you use secure audio path to play it.</span></span>

## <a name="configuring-the-reader-to-evaluate-output-protection-levels"></a><span data-ttu-id="c2756-130">Configuration du lecteur pour évaluer les niveaux de protection de sortie</span><span class="sxs-lookup"><span data-stu-id="c2756-130">Configuring the Reader to Evaluate Output Protection Levels</span></span>

<span data-ttu-id="c2756-131">Avant de pouvoir vérifier OPLs pour les fichiers chargés dans le lecteur, vous devez appeler la méthode [**IWMDRMReader2 :: SetEvaluateOutputLevelLicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-setevaluateoutputlevellicenses) , en passant **true** pour le paramètre *fEvaluate* .</span><span class="sxs-lookup"><span data-stu-id="c2756-131">Before you can check OPLs for files loaded in the reader, you must call the [**IWMDRMReader2::SetEvaluateOutputLevelLicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-setevaluateoutputlevellicenses) method, passing **TRUE** for the *fEvaluate* parameter.</span></span> <span data-ttu-id="c2756-132">Si vous n’appelez pas cette méthode, les licences qui requièrent des OPLs ne sont pas visibles par votre application.</span><span class="sxs-lookup"><span data-stu-id="c2756-132">If you do not call this method, licenses that require OPLs are not visible to your application.</span></span>

## <a name="evaluating-copy-output-protection-levels"></a><span data-ttu-id="c2756-133">Évaluation des niveaux de protection de copie de sortie</span><span class="sxs-lookup"><span data-stu-id="c2756-133">Evaluating Copy Output Protection Levels</span></span>

<span data-ttu-id="c2756-134">Pour obtenir les niveaux de protection de sortie de l’action de copie, appelez la méthode [**IWMDRMReader2 :: GetCopyOutputLevels**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-getcopyoutputlevels) .</span><span class="sxs-lookup"><span data-stu-id="c2756-134">To get output protection levels for the copy action, call the [**IWMDRMReader2::GetCopyOutputLevels**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-getcopyoutputlevels) method.</span></span> <span data-ttu-id="c2756-135">Les données que vous recevez de l’appel sont stockées dans une structure [**\_ \_ OPL de copie DRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_copy_opl) .</span><span class="sxs-lookup"><span data-stu-id="c2756-135">The data you receive from the call is stored in a [**DRM\_COPY\_OPL**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_copy_opl) structure.</span></span> <span data-ttu-id="c2756-136">La structure contient un niveau de protection de sortie de base, qui spécifie le niveau de sortie minimal pour l’action de copie dans la licence.</span><span class="sxs-lookup"><span data-stu-id="c2756-136">The structure contains a base output protection level, which specifies the minimum output level for the copy action in the license.</span></span> <span data-ttu-id="c2756-137">Toutefois, la \_ structure OPL de la copie DRM \_ contient également deux listes d’identificateurs de technologie : une pour les technologies autorisées qui sont évaluées à un OPL inférieur à la base et une pour les technologies évaluées égales ou supérieures à celles du OPL de base, mais qui sont limitées par la licence.</span><span class="sxs-lookup"><span data-stu-id="c2756-137">However, the DRM\_COPY\_OPL structure also contains two lists of technology identifiers: one for allowed technologies that are rated at a lower OPL than the base, and one for technologies that are rated equal to or higher than the base OPL but that are restricted by the license.</span></span> <span data-ttu-id="c2756-138">Vous devez vérifier les inclusions et les exclusions pour vous assurer que la technologie utilisée par votre application est autorisée par la licence.</span><span class="sxs-lookup"><span data-stu-id="c2756-138">You must check the inclusions and exclusions to ensure that the technology your application is using is allowed by the license.</span></span>

## <a name="evaluating-play-output-protection-levels"></a><span data-ttu-id="c2756-139">Évaluation des niveaux de protection de sortie de lecture</span><span class="sxs-lookup"><span data-stu-id="c2756-139">Evaluating Play Output Protection Levels</span></span>

<span data-ttu-id="c2756-140">Pour obtenir les niveaux de protection de sortie de l’action Play, appelez la méthode [**IWMDRMReader2 :: GetPlayOutputLevels**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-getplayoutputlevels) .</span><span class="sxs-lookup"><span data-stu-id="c2756-140">To get output protection levels for the play action, call the [**IWMDRMReader2::GetPlayOutputLevels**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-getplayoutputlevels) method.</span></span> <span data-ttu-id="c2756-141">Les données que vous recevez de l’appel sont stockées dans une structure de [**\_ lecture DRM \_ OPL**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_play_opl) .</span><span class="sxs-lookup"><span data-stu-id="c2756-141">The data you receive from the call is stored in a [**DRM\_PLAY\_OPL**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_play_opl) structure.</span></span> <span data-ttu-id="c2756-142">La structure contient plusieurs autres structures.</span><span class="sxs-lookup"><span data-stu-id="c2756-142">The structure contains several other structures.</span></span> <span data-ttu-id="c2756-143">Les niveaux de protection de sortie de base pour l’action de lecture sont stockés dans une structure de [**niveaux de protection de \_ \_ sortie \_ \_ DRM minimum**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_minimum_output_protection_levels) (le membre **minOPL** de **DRM \_ Play \_ OPL**), qui définit le OPL minimal requis pour lire le contenu dans divers formats.</span><span class="sxs-lookup"><span data-stu-id="c2756-143">The base output protection levels for the play action are stored in a [**DRM\_MINIMUM\_OUTPUT\_PROTECTION\_LEVELS**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_minimum_output_protection_levels) structure (the **minOPL** member of **DRM\_PLAY\_OPL**), which defines the minimum OPL required to play content in a variety of formats.</span></span> <span data-ttu-id="c2756-144">Vous devez vérifier le type des formats de sortie fournis par votre application.</span><span class="sxs-lookup"><span data-stu-id="c2756-144">You must check the member for the type of output formats that your application delivers.</span></span>

<span data-ttu-id="c2756-145">La **structure \_ \_ OPL de la lecture DRM** définit deux types de restrictions : les identificateurs d’échantillonnage et de protection de sortie vidéo autorisés.</span><span class="sxs-lookup"><span data-stu-id="c2756-145">The **DRM\_PLAY\_OPL** structure defines two kinds of restrictions: required down-sampling and allowed video output protection identifiers.</span></span>

<span data-ttu-id="c2756-146">L’échantillonnage obligatoire est défini sous la forme d’une liste d’identificateurs de technologie de sortie (le membre **oplIdDownsample** de la fonction **DRM \_ Play \_ OPL**) qui, s’il est utilisé, peut recevoir le contenu pour lecture uniquement si le contenu est d’abord abaissé à une vitesse de transmission inférieure.</span><span class="sxs-lookup"><span data-stu-id="c2756-146">Required down-sampling is defined as a list of output technology identifiers (the **oplIdDownsample** member of **DRM\_PLAY\_OPL**) that, if used, can receive the content for playback only if the content is first down-sampled to a lower bit rate.</span></span>

<span data-ttu-id="c2756-147">Les identificateurs de protection de sortie vidéo autorisés sont définis comme une liste de technologies de sortie vidéo avec les informations de configuration de chacune.</span><span class="sxs-lookup"><span data-stu-id="c2756-147">Allowed video output protection identifiers are defined as a list of video output technologies with configuration information for each.</span></span>

## <a name="handling-multiple-licenses"></a><span data-ttu-id="c2756-148">Gestion de plusieurs licences</span><span class="sxs-lookup"><span data-stu-id="c2756-148">Handling Multiple Licenses</span></span>

<span data-ttu-id="c2756-149">Certains fichiers peuvent être associés à plusieurs licences dans le magasin de licences local.</span><span class="sxs-lookup"><span data-stu-id="c2756-149">Some files may have multiple licenses associated with them in the local license store.</span></span> <span data-ttu-id="c2756-150">Lorsque vous évaluez OPLs pour un fichier que vous lisez, vous pouvez rechercher d’autres licences en appelant la méthode [**IWMDRMReader2 :: TryNextLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-trynextlicense) .</span><span class="sxs-lookup"><span data-stu-id="c2756-150">When you evaluate OPLs for a file that you are reading, you can check for additional licenses by calling the [**IWMDRMReader2::TryNextLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-trynextlicense) method.</span></span> <span data-ttu-id="c2756-151">Vous devez continuer à essayer les licences jusqu’à ce que vous en trouviez une qui autorise l’action que vous voulez effectuer ou jusqu’à ce que TryNextLicense retourne DRM \_ S \_ false, ce qui indique qu’il n’y a plus de licences.</span><span class="sxs-lookup"><span data-stu-id="c2756-151">You should continue trying licenses until you find one that allows the action you want to perform or until TryNextLicense returns DRM\_S\_FALSE, which indicates that there are no more licenses.</span></span>

<span data-ttu-id="c2756-152">Dans certains cas, un fichier peut avoir une licence associée qui requiert un OPL que votre application ne peut pas prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="c2756-152">In some cases, a file might have an associated license that requires an OPL that your application cannot support.</span></span> <span data-ttu-id="c2756-153">Dans ce cas, il est important de vérifier la présence de licences supplémentaires, car il existe une licence qui ne spécifie pas OPLs.</span><span class="sxs-lookup"><span data-stu-id="c2756-153">In such a case it is important to check for additional licenses because a license may exist that does not specify OPLs.</span></span>

<span data-ttu-id="c2756-154">**Remarque** DRM n’est pas pris en charge par la version x64 de ce kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="c2756-154">**Note** DRM is not supported by the x64-based version of this SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c2756-155">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c2756-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2756-156">**Activation de la prise en charge de DRM**</span><span class="sxs-lookup"><span data-stu-id="c2756-156">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> <dt>

[<span data-ttu-id="c2756-157">**Interface IWMDRMReader2**</span><span class="sxs-lookup"><span data-stu-id="c2756-157">**IWMDRMReader2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2)
</dt> </dl>

 

 




