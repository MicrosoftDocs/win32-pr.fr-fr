---
title: Mise à jour des plug-ins DSP existants
description: Mise à jour des plug-ins DSP existants
ms.assetid: 0525030e-eb30-41a0-8191-4a5727736857
keywords:
- Plug-ins du lecteur Windows Media, DSP (Digital Signal Processing)
- plug-ins, traitement des signaux numériques (DSP)
- plug-ins de traitement de signal numérique, mise à jour
- Plug-ins DSP, mise à jour
- versions du lecteur Windows Media, les plug-ins DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 393cde356e0d86bb920825e731bb12ee0b7c2818
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723474"
---
# <a name="updating-existing-dsp-plug-ins"></a><span data-ttu-id="a2a40-108">Mise à jour des plug-ins DSP existants</span><span class="sxs-lookup"><span data-stu-id="a2a40-108">Updating Existing DSP Plug-ins</span></span>

<span data-ttu-id="a2a40-109">Les plug-ins DSP créés avant le lancement du kit de développement logiciel (SDK) du lecteur Windows Media 11 peuvent ne pas fonctionner comme prévu avec le lecteur Windows Media 11 s’exécutant sur Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a2a40-109">DSP plug-ins created before the release of the Windows Media Player 11 SDK might not work as expected with Windows Media Player 11 running on Windows Vista.</span></span> <span data-ttu-id="a2a40-110">Pour vous assurer que les clients qui exécutent le lecteur Windows Media 11 sur Windows Vista peuvent utiliser vos plug-ins, vous devez apporter des modifications à votre code de plug-in DSP, recompiler votre projet et distribuer le plug-in mis à jour à vos clients.</span><span class="sxs-lookup"><span data-stu-id="a2a40-110">To ensure that customers who run Windows Media Player 11 on Windows Vista can use your plug-ins, you must make some changes to your DSP plug-in code, recompile your project, and distribute the updated plug-in to your customers.</span></span>

<span data-ttu-id="a2a40-111">Les projets créés à l’aide de la version la plus récente de l’Assistant de plug-in du lecteur Windows Media contiennent les mises à jour requises.</span><span class="sxs-lookup"><span data-stu-id="a2a40-111">Projects created using the latest version of the Windows Media Player plug-in wizard will contain the required updates.</span></span> <span data-ttu-id="a2a40-112">Consultez [mises à jour de l’Assistant de plug-in DSP pour le lecteur Windows Media 11](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md).</span><span class="sxs-lookup"><span data-stu-id="a2a40-112">See [Updates to the DSP Plug-in Wizard for Windows Media Player 11](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md).</span></span> <span data-ttu-id="a2a40-113">(Il est judicieux d’exécuter l’Assistant pour créer un exemple de projet, puis d’utiliser un outil comme Windiff.exe, fourni avec Visual Studio, pour inspecter les différences entre l’exemple de code et votre code de production.)</span><span class="sxs-lookup"><span data-stu-id="a2a40-113">(It is a good idea to run the wizard to create a new sample project and then use a tool like Windiff.exe, which comes with Visual Studio, to inspect the differences between the sample code and your production code.)</span></span>

<span data-ttu-id="a2a40-114">Trois modifications principales doivent être apportées à tous les plug-ins DSP existants :</span><span class="sxs-lookup"><span data-stu-id="a2a40-114">There are three main changes you will need to make to any existing DSP plug-ins:</span></span>

-   <span data-ttu-id="a2a40-115">Modifiez la façon dont le plug-in s’inscrit.</span><span class="sxs-lookup"><span data-stu-id="a2a40-115">Change the way the plug-in registers.</span></span> <span data-ttu-id="a2a40-116">Votre plug-in existant inscrit probablement le modèle de thread en tant que « cloisonnement ».</span><span class="sxs-lookup"><span data-stu-id="a2a40-116">Your existing plug-in probably registers the threading model as "Apartment".</span></span> <span data-ttu-id="a2a40-117">Le lecteur Windows Media 11 s’exécutant sur Windows Vista exige que les plug-ins DSP inscrivent le modèle de thread comme « les deux ».</span><span class="sxs-lookup"><span data-stu-id="a2a40-117">Windows Media Player 11 running on Windows Vista requires that DSP plug-ins register the threading model as "Both".</span></span> <span data-ttu-id="a2a40-118">Vous pouvez résoudre ce problème en modifiant la valeur du modèle de thread dans votre fichier *ProjectName*. RGS, comme suit :</span><span class="sxs-lookup"><span data-stu-id="a2a40-118">You can fix this by changing the threading model value in your *projectname*.rgs file, as follows:</span></span>

    ```C++
    val ThreadingModel = s 'Both'
    
    ```

    

    > [!Note]  
    > <span data-ttu-id="a2a40-119">La spécification du modèle de thread comme « both » supprime toute sérialisation fournie par COM pour les appels à des interfaces personnalisées.</span><span class="sxs-lookup"><span data-stu-id="a2a40-119">Specifying the threading model as "Both" removes any serialization that COM provides for calls to custom interfaces.</span></span> <span data-ttu-id="a2a40-120">Si vous effectuez des appels à vos interfaces personnalisées à partir de plusieurs threads, vous devez fournir cette sérialisation vous-même.</span><span class="sxs-lookup"><span data-stu-id="a2a40-120">If you make calls to your custom interfaces from multiple threads, you must provide this serialization yourself.</span></span>

     

    <span data-ttu-id="a2a40-121">Le lecteur Windows Media 11 garantit que les appels aux interfaces DMO sont correctement sérialisés.</span><span class="sxs-lookup"><span data-stu-id="a2a40-121">Windows Media Player 11 ensures that calls to DMO interfaces are properly serialized.</span></span>

    1.  <span data-ttu-id="a2a40-122">Ajoutez des appels à [IWMPMediaPluginRegistrar :: WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) et [IWMPMediaPluginRegistrar :: WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) avec un nouveau type de plug-in : WMP \_ PLUGINTYPE \_ DSP \_ OUTOFPROC dans DllRegisterServer et DllUnregisterServer dans votre fichier *projectnamedll*. cpp.</span><span class="sxs-lookup"><span data-stu-id="a2a40-122">Add calls to [IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) and [IWMPMediaPluginRegistrar::WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) with a new plug-in type: WMP\_PLUGINTYPE\_DSP\_OUTOFPROC in DllRegisterServer and DllUnregisterServer in your *projectnamedll*.cpp file.</span></span> <span data-ttu-id="a2a40-123">Pour plus d’informations, consultez les pages de référence pour ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="a2a40-123">See the reference pages for these methods for details.</span></span>
    2.  <span data-ttu-id="a2a40-124">Créez et distribuez une DLL proxy/stub pour activer le marshaling COM de toute interface personnalisée implémentée ou créée par la classe de plug-in.</span><span class="sxs-lookup"><span data-stu-id="a2a40-124">Create and distribute a proxy/stub DLL to enable COM marshaling of any custom interface implemented on or created by the plug-in class.</span></span> <span data-ttu-id="a2a40-125">Une interface personnalisée est toute interface propriétaire que vous définissez et implémentez pour une utilisation par l’objet de plug-in.</span><span class="sxs-lookup"><span data-stu-id="a2a40-125">A custom interface is any proprietary interface that you define and implement for use by the plug-in object.</span></span> <span data-ttu-id="a2a40-126">Cela inclut l’interface personnalisée utilisée par votre page de propriétés, si vous en avez fourni une, mais peut également inclure des interfaces qui se connectent aux plug-ins d’interface utilisateur, par exemple.</span><span class="sxs-lookup"><span data-stu-id="a2a40-126">This includes the custom interface used by your property page, if you provided one, but might also include interfaces that connect to UI plug-ins, for example.</span></span> <span data-ttu-id="a2a40-127">*Iprojectname* est un exemple d’interface personnalisée créée par l’Assistant de plug-in.</span><span class="sxs-lookup"><span data-stu-id="a2a40-127">An example of a custom interface created by the plug-in wizard is *Iprojectname*.</span></span> <span data-ttu-id="a2a40-128">**IMediaObject** et **IWMPPluginEnable** sont des exemples d’interfaces qui ne sont pas des interfaces personnalisées.</span><span class="sxs-lookup"><span data-stu-id="a2a40-128">Examples of interfaces that are not custom interfaces include **IMediaObject** and **IWMPPluginEnable**.</span></span>

<span data-ttu-id="a2a40-129">Si votre plug-in DSP traite le son, vous devez également ajouter la prise en charge des nouveaux formats audio suivants :</span><span class="sxs-lookup"><span data-stu-id="a2a40-129">If your DSP plug-in processes audio, you must also add support for the following new audio formats:</span></span>

-   <span data-ttu-id="a2a40-130">\_format Wave \_ IEEE \_ float</span><span class="sxs-lookup"><span data-stu-id="a2a40-130">WAVE\_FORMAT\_IEEE\_FLOAT</span></span>
-   <span data-ttu-id="a2a40-131">\_Format Wave \_ extensible avec SUBformat KSDATAFORMAT sous- \_ type \_ IEEE \_ float.</span><span class="sxs-lookup"><span data-stu-id="a2a40-131">WAVE\_FORMAT\_EXTENSIBLE with subformat KSDATAFORMAT\_SUBTYPE\_IEEE\_FLOAT.</span></span>

<span data-ttu-id="a2a40-132">Si votre plug-in DSP traite une vidéo, vous devez ajouter la prise en charge du format vidéo NV12.</span><span class="sxs-lookup"><span data-stu-id="a2a40-132">If your DSP plug-in processes video, you must add support for the NV12 video format.</span></span>

<span data-ttu-id="a2a40-133">Pour obtenir un exemple de traitement de ces types de format, consultez l’exemple de plug-in DSP audio ou Video créé par l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="a2a40-133">See the sample audio or video DSP plug-in that the wizard creates for an example of how to process these format types.</span></span>

## <a name="about-the-proxystub-project"></a><span data-ttu-id="a2a40-134">À propos du projet proxy/stub</span><span class="sxs-lookup"><span data-stu-id="a2a40-134">About the Proxy/Stub Project</span></span>

<span data-ttu-id="a2a40-135">La façon la plus simple de créer un projet DLL proxy/stub pour votre plug-in DSP consiste à exécuter l’Assistant de plug-in DSP.</span><span class="sxs-lookup"><span data-stu-id="a2a40-135">Perhaps the simplest way to create a proxy/stub DLL project for your DSP plug-in is to run the DSP plug-in wizard.</span></span> <span data-ttu-id="a2a40-136">Cela permet de créer un exemple de projet de proxy/stub que vous pouvez modifier pour utiliser votre code existant.</span><span class="sxs-lookup"><span data-stu-id="a2a40-136">This will create a sample proxy/stub project that you can modify to work with your existing code.</span></span> <span data-ttu-id="a2a40-137">Vous devrez apporter les modifications suivantes :</span><span class="sxs-lookup"><span data-stu-id="a2a40-137">You will need to make the following changes:</span></span>

1.  <span data-ttu-id="a2a40-138">Supprimez les définitions existantes de vos interfaces personnalisées de votre code.</span><span class="sxs-lookup"><span data-stu-id="a2a40-138">Remove any existing definitions for your custom interfaces from your code.</span></span> <span data-ttu-id="a2a40-139">Par exemple, l’Assistant de plug-in DSP du kit de développement logiciel (SDK) du lecteur Windows Media 10 a créé la définition de l’interface *Iprojectname* dans le fichier *ProjectName*. h à l’aide du mot clé **interface** .</span><span class="sxs-lookup"><span data-stu-id="a2a40-139">For example, the DSP plug-in wizard from the Windows Media Player 10 SDK created the *Iprojectname* interface definition in the *projectname*.h file by using the **interface** keyword.</span></span>
2.  <span data-ttu-id="a2a40-140">Définissez vos interfaces personnalisées dans le fichier IDL du projet proxy/stub.</span><span class="sxs-lookup"><span data-stu-id="a2a40-140">Define your custom interfaces in the proxy/stub project's IDL file.</span></span>
3.  <span data-ttu-id="a2a40-141">Générez le projet proxy/stub avant votre projet principal.</span><span class="sxs-lookup"><span data-stu-id="a2a40-141">Build the proxy/stub project before your main project.</span></span> <span data-ttu-id="a2a40-142">Vous pouvez configurer Visual Studio pour effectuer cette opération automatiquement si les deux projets font partie de la même solution.</span><span class="sxs-lookup"><span data-stu-id="a2a40-142">You can configure Visual Studio to do this automatically if both projects are part of the same solution.</span></span>
4.  <span data-ttu-id="a2a40-143">Le compilateur MIDL crée un nouveau fichier d’en-tête dont le nom est au format *ProjectName* \_ h.h.</span><span class="sxs-lookup"><span data-stu-id="a2a40-143">The MIDL compiler will create a new header file having a name in the format *projectname*\_h.h.</span></span> <span data-ttu-id="a2a40-144">Vous devez inclure cet en-tête dans votre projet principal (dans *nom_projet*. h).</span><span class="sxs-lookup"><span data-stu-id="a2a40-144">You must include this header in your main project (in *projectname*.h).</span></span> <span data-ttu-id="a2a40-145">Elle contient les définitions de vos interfaces personnalisées.</span><span class="sxs-lookup"><span data-stu-id="a2a40-145">It contains the definitions for your custom interfaces.</span></span>

## <a name="distributing-the-updated-plug-in"></a><span data-ttu-id="a2a40-146">Distribution du plug-in mis à jour</span><span class="sxs-lookup"><span data-stu-id="a2a40-146">Distributing the Updated Plug-in</span></span>

<span data-ttu-id="a2a40-147">Vous pouvez installer le plug-in mis à jour sur les ordinateurs de vos utilisateurs exactement comme vous l’avez déjà passé.</span><span class="sxs-lookup"><span data-stu-id="a2a40-147">You can install the updated plug-in on your users' computers exactly as you have in the past.</span></span> <span data-ttu-id="a2a40-148">Toutefois, vous devez maintenant également distribuer et inscrire la DLL proxy/stub.</span><span class="sxs-lookup"><span data-stu-id="a2a40-148">However, you must now also distribute and register the proxy/stub DLL.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a2a40-149">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a2a40-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2a40-150">**Vue d’ensemble des développeurs de plug-ins DSP**</span><span class="sxs-lookup"><span data-stu-id="a2a40-150">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




