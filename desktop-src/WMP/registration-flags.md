---
title: Indicateurs d’inscription
description: Indicateurs d’inscription
ms.assetid: ba1709c2-0fe5-4168-9aed-613d01eff21f
keywords:
- Plug-ins du lecteur Windows Media, indicateurs d’inscription
- plug-ins, indicateurs d’inscription
- plug-ins d’interface utilisateur, indicateurs d’inscription
- Plug-ins d’interface utilisateur, indicateurs d’inscription
- indicateurs, plug-ins d’interface utilisateur
- Registre, plug-ins d’interface utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac609b45866cd5f18edf61dffc2d3b7ac3c397ac
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104030815"
---
# <a name="registration-flags"></a><span data-ttu-id="7b24d-109">Indicateurs d’inscription</span><span class="sxs-lookup"><span data-stu-id="7b24d-109">Registration Flags</span></span>

<span data-ttu-id="7b24d-110">Lorsque l’Assistant de plug-in du lecteur Windows Media crée un projet de plug-in d’interface utilisateur, il crée une clé dans le Registre qui contient des informations sur le plug-in.</span><span class="sxs-lookup"><span data-stu-id="7b24d-110">When the Windows Media Player Plug-in Wizard creates a new UI plug-in project, it creates a key in the registry that contains information about the plug-in.</span></span> <span data-ttu-id="7b24d-111">Cette clé est créée à l’emplacement suivant :</span><span class="sxs-lookup"><span data-stu-id="7b24d-111">This key is created in the following location:</span></span>


```C++
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MediaPlayer\UIPlugins\{ClassId}
```



<span data-ttu-id="7b24d-112">*ClassID* est l’ID de classe du plug-in.</span><span class="sxs-lookup"><span data-stu-id="7b24d-112">*ClassId* is the class id of the plug-in.</span></span>

<span data-ttu-id="7b24d-113">Cette clé comprend les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="7b24d-113">This key includes the following values.</span></span>



| <span data-ttu-id="7b24d-114">Nom</span><span class="sxs-lookup"><span data-stu-id="7b24d-114">Name</span></span>                     | <span data-ttu-id="7b24d-115">Type</span><span class="sxs-lookup"><span data-stu-id="7b24d-115">Type</span></span>       | <span data-ttu-id="7b24d-116">Description</span><span class="sxs-lookup"><span data-stu-id="7b24d-116">Description</span></span>                                                                                                                                                                               |
|--------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b24d-117">Fonctions</span><span class="sxs-lookup"><span data-stu-id="7b24d-117">Capabilities</span></span>             | <span data-ttu-id="7b24d-118">\_valeur DWORD reg</span><span class="sxs-lookup"><span data-stu-id="7b24d-118">REG\_DWORD</span></span> | <span data-ttu-id="7b24d-119">Valeur DWORD qui se compose d’au moins un indicateur de type de plug-in qui peut être combiné avec un ou plusieurs indicateurs de fonctionnalités de plug-in à l’aide de binaires ou d’opérations.</span><span class="sxs-lookup"><span data-stu-id="7b24d-119">A DWORD value that consists of at least one plug-in type flag that may be combined with one or more plug-in capabilities flags by using binary OR operations.</span></span>                             |
| <span data-ttu-id="7b24d-120">Description</span><span class="sxs-lookup"><span data-stu-id="7b24d-120">Description</span></span>              | <span data-ttu-id="7b24d-121">SZ de REG \_</span><span class="sxs-lookup"><span data-stu-id="7b24d-121">REG\_SZ</span></span>    | <span data-ttu-id="7b24d-122">Chaîne qui contient la description du plug-in.</span><span class="sxs-lookup"><span data-stu-id="7b24d-122">A string that contains the description of the plug-in.</span></span> <span data-ttu-id="7b24d-123">L’Assistant de plug-in crée une ressource de type chaîne et fournit l’URL de la ressource (à l’aide du protocole res) pour cette valeur.</span><span class="sxs-lookup"><span data-stu-id="7b24d-123">The plug-in wizard creates a string resource and provides the URL of the resource (using the res protocol) for this value.</span></span>         |
| <span data-ttu-id="7b24d-124">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="7b24d-124">FriendlyName</span></span>             | <span data-ttu-id="7b24d-125">SZ de REG \_</span><span class="sxs-lookup"><span data-stu-id="7b24d-125">REG\_SZ</span></span>    | <span data-ttu-id="7b24d-126">Chaîne qui contient le nom lisible par l’utilisateur pour le plug-in.</span><span class="sxs-lookup"><span data-stu-id="7b24d-126">A string that contains the user-readable name for the plug-in.</span></span> <span data-ttu-id="7b24d-127">L’Assistant de plug-in crée une ressource de type chaîne et fournit l’URL de la ressource (à l’aide du protocole res) pour cette valeur.</span><span class="sxs-lookup"><span data-stu-id="7b24d-127">The plug-in wizard creates a string resource and provides the URL of the resource (using the res protocol) for this value.</span></span> |
| <span data-ttu-id="7b24d-128">UninstallPath (facultatif)</span><span class="sxs-lookup"><span data-stu-id="7b24d-128">UninstallPath (optional)</span></span> | <span data-ttu-id="7b24d-129">SZ de REG \_</span><span class="sxs-lookup"><span data-stu-id="7b24d-129">REG\_SZ</span></span>    | <span data-ttu-id="7b24d-130">Chaîne qui contient le chemin d’accès à un fichier exécutable qui désinstalle le plug-in.</span><span class="sxs-lookup"><span data-stu-id="7b24d-130">A string that contains the path to an executable file that uninstalls the plug-in.</span></span>                                                                                                        |



 

<span data-ttu-id="7b24d-131">Pour plus d’informations sur le protocole res, consultez le kit de développement logiciel (SDK) Internet Development.</span><span class="sxs-lookup"><span data-stu-id="7b24d-131">For more information about the res protocol, see the Internet Development SDK.</span></span>

<span data-ttu-id="7b24d-132">Le tableau suivant détaille les indicateurs de type de plug-in.</span><span class="sxs-lookup"><span data-stu-id="7b24d-132">The following table details the plug-in type flags.</span></span>



| <span data-ttu-id="7b24d-133">Indicateur de type de plug-in</span><span class="sxs-lookup"><span data-stu-id="7b24d-133">Plug-in Type Flag</span></span>                | <span data-ttu-id="7b24d-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="7b24d-134">Value</span></span> | <span data-ttu-id="7b24d-135">Description</span><span class="sxs-lookup"><span data-stu-id="7b24d-135">Description</span></span>                                       |
|----------------------------------|-------|---------------------------------------------------|
| <span data-ttu-id="7b24d-136">**\_arrière-plan du type de plug \_ -in**</span><span class="sxs-lookup"><span data-stu-id="7b24d-136">**PLUGIN\_TYPE\_BACKGROUND**</span></span>     | <span data-ttu-id="7b24d-137">0x1</span><span class="sxs-lookup"><span data-stu-id="7b24d-137">0x1</span></span>   | <span data-ttu-id="7b24d-138">Le plug-in d’interface utilisateur n’affiche pas d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7b24d-138">The UI plug-in does not display a user interface.</span></span> |
| <span data-ttu-id="7b24d-139">**TYPE de plug-in \_ \_ SEPARATEWINDOW**</span><span class="sxs-lookup"><span data-stu-id="7b24d-139">**PLUGIN\_TYPE\_SEPARATEWINDOW**</span></span> | <span data-ttu-id="7b24d-140">0x2</span><span class="sxs-lookup"><span data-stu-id="7b24d-140">0x2</span></span>   | <span data-ttu-id="7b24d-141">Le plug-in d’interface utilisateur est un plug-in de fenêtre distinct.</span><span class="sxs-lookup"><span data-stu-id="7b24d-141">The UI plug-in is a separate window plug-in.</span></span>      |
| <span data-ttu-id="7b24d-142">**TYPE de plug-in \_ \_ DISPLAYAREA**</span><span class="sxs-lookup"><span data-stu-id="7b24d-142">**PLUGIN\_TYPE\_DISPLAYAREA**</span></span>    | <span data-ttu-id="7b24d-143">0x3</span><span class="sxs-lookup"><span data-stu-id="7b24d-143">0x3</span></span>   | <span data-ttu-id="7b24d-144">Le plug-in d’interface utilisateur est un plug-in de zone d’affichage.</span><span class="sxs-lookup"><span data-stu-id="7b24d-144">The UI plug-in is a display area plug-in.</span></span>         |
| <span data-ttu-id="7b24d-145">**TYPE de plug-in \_ \_ SETTINGSAREA**</span><span class="sxs-lookup"><span data-stu-id="7b24d-145">**PLUGIN\_TYPE\_SETTINGSAREA**</span></span>   | <span data-ttu-id="7b24d-146">0x4</span><span class="sxs-lookup"><span data-stu-id="7b24d-146">0x4</span></span>   | <span data-ttu-id="7b24d-147">Le plug-in d’interface utilisateur est un plug-in de zone de paramètres.</span><span class="sxs-lookup"><span data-stu-id="7b24d-147">The UI plug-in is a settings area plug-in.</span></span>        |
| <span data-ttu-id="7b24d-148">**TYPE de plug-in \_ \_ METADATAAREA**</span><span class="sxs-lookup"><span data-stu-id="7b24d-148">**PLUGIN\_TYPE\_METADATAAREA**</span></span>   | <span data-ttu-id="7b24d-149">0x5</span><span class="sxs-lookup"><span data-stu-id="7b24d-149">0x5</span></span>   | <span data-ttu-id="7b24d-150">Le plug-in d’interface utilisateur est un plug-in de zone de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="7b24d-150">The UI plug-in is a metadata area plug-in.</span></span>        |



 

<span data-ttu-id="7b24d-151">Le tableau suivant détaille les indicateurs de fonctionnalités de plug-in.</span><span class="sxs-lookup"><span data-stu-id="7b24d-151">The following table details the plug-in capabilities flags.</span></span>



| <span data-ttu-id="7b24d-152">Indicateur de fonctionnalités de plug-in</span><span class="sxs-lookup"><span data-stu-id="7b24d-152">Plug-in Capabilities Flag</span></span>             | <span data-ttu-id="7b24d-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="7b24d-153">Value</span></span>      | <span data-ttu-id="7b24d-154">Description</span><span class="sxs-lookup"><span data-stu-id="7b24d-154">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b24d-155">**indicateurs de plug-in \_ \_ ACCEPTSMEDIA**</span><span class="sxs-lookup"><span data-stu-id="7b24d-155">**PLUGIN\_FLAGS\_ACCEPTSMEDIA**</span></span>       | <span data-ttu-id="7b24d-156">0x10000000</span><span class="sxs-lookup"><span data-stu-id="7b24d-156">0x10000000</span></span> | <span data-ttu-id="7b24d-157">Le plug-in d’interface utilisateur peut accepter des tableaux de pointeurs d’objets **multimédias** quand le lecteur Windows Media appelle [**IWMPPluginUI :: SetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty) .</span><span class="sxs-lookup"><span data-stu-id="7b24d-157">The UI plug-in can accept **Media** object pointer arrays when Windows Media Player calls [**IWMPPluginUI::SetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty) .</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="7b24d-158">**indicateurs de plug-in \_ \_ ACCEPTSPLAYLISTS**</span><span class="sxs-lookup"><span data-stu-id="7b24d-158">**PLUGIN\_FLAGS\_ACCEPTSPLAYLISTS**</span></span>   | <span data-ttu-id="7b24d-159">0x8000000</span><span class="sxs-lookup"><span data-stu-id="7b24d-159">0x8000000</span></span>  | <span data-ttu-id="7b24d-160">Le plug-in d’interface utilisateur peut accepter des tableaux de pointeurs d’objets de **sélection** lorsque le lecteur Windows Media appelle [**IWMPPluginUI :: SetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty) .</span><span class="sxs-lookup"><span data-stu-id="7b24d-160">The UI plug-in can accept **Playlist** object pointer arrays when Windows Media Player calls [**IWMPPluginUI::SetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty) .</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="7b24d-161">**indicateurs de plug-in \_ \_ HASPRESETS**</span><span class="sxs-lookup"><span data-stu-id="7b24d-161">**PLUGIN\_FLAGS\_HASPRESETS**</span></span>         | <span data-ttu-id="7b24d-162">0x4000000</span><span class="sxs-lookup"><span data-stu-id="7b24d-162">0x4000000</span></span>  | <span data-ttu-id="7b24d-163">Le plug-in d’interface utilisateur utilise des présélections.</span><span class="sxs-lookup"><span data-stu-id="7b24d-163">The UI plug-in uses presets.</span></span> <span data-ttu-id="7b24d-164">Si le plug-in spécifie cet indicateur, le lecteur Windows Media interroge le plug-in pour obtenir des informations prédéfinies en appelant [**IWMPPluginUI :: GetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-getproperty) .</span><span class="sxs-lookup"><span data-stu-id="7b24d-164">If the plug-in specifies this flag, Windows Media Player will query the plug-in for preset information by calling [**IWMPPluginUI::GetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-getproperty) .</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="7b24d-165">**indicateurs de plug-in \_ \_ HASPROPERTYPAGE**</span><span class="sxs-lookup"><span data-stu-id="7b24d-165">**PLUGIN\_FLAGS\_HASPROPERTYPAGE**</span></span>    | <span data-ttu-id="7b24d-166">0x80000000</span><span class="sxs-lookup"><span data-stu-id="7b24d-166">0x80000000</span></span> | <span data-ttu-id="7b24d-167">Le plug-in d’interface utilisateur fournit une boîte de dialogue de page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="7b24d-167">The UI plug-in provides a property page dialog.</span></span> <span data-ttu-id="7b24d-168">Le lecteur Windows Media appellera [**IWMPPluginUI ::D isplaypropertypage**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage) si cet indicateur est défini lors de l’appel de la page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="7b24d-168">Windows Media Player will call [**IWMPPluginUI::DisplayPropertyPage**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage) if this flag is set when the property page is invoked.</span></span>                                                                                                                                                                                                 |
| <span data-ttu-id="7b24d-169">**indicateurs de plug-in \_ \_ masqués**</span><span class="sxs-lookup"><span data-stu-id="7b24d-169">**PLUGIN\_FLAGS\_HIDDEN**</span></span>             | <span data-ttu-id="7b24d-170">0x02000000</span><span class="sxs-lookup"><span data-stu-id="7b24d-170">0x02000000</span></span> | <span data-ttu-id="7b24d-171">Le plug-in IU d’arrière-plan n’apparaît pas dans le menu **plug-ins** accessible à partir des menus **affichage** ou **Outils** ou du bouton **Sélectionner les options de diffusion** en cours.</span><span class="sxs-lookup"><span data-stu-id="7b24d-171">The background UI plug-in does not appear on the **Plug-ins** menu that is accessed from the **View** or **Tools** menus or the **Select Now Playing options** button in Now Playing.</span></span> <span data-ttu-id="7b24d-172">Il apparaît dans l’onglet **plug-ins** de la boîte de dialogue Options.</span><span class="sxs-lookup"><span data-stu-id="7b24d-172">It does appear on the **Plug-ins** tab of the Options dialog.</span></span> <span data-ttu-id="7b24d-173">L’icône d’exécution du plug-in en arrière-plan s’affiche alors dans la barre d’État. Cet indicateur n’a aucun effet sur les plug-ins autres que les plug-ins d’IU d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="7b24d-173">It does cause the Background Plug-in Running icon to appear in the status bar.This flag has no effect on plug-ins other than background UI plug-ins.</span></span><br/> |
| <span data-ttu-id="7b24d-174">**indicateurs de plug-in \_ \_ INSTALLAUTORUN**</span><span class="sxs-lookup"><span data-stu-id="7b24d-174">**PLUGIN\_FLAGS\_INSTALLAUTORUN**</span></span>     | <span data-ttu-id="7b24d-175">0x40000000</span><span class="sxs-lookup"><span data-stu-id="7b24d-175">0x40000000</span></span> | <span data-ttu-id="7b24d-176">Le lecteur Windows Media exécute automatiquement le plug-in d’interface utilisateur lors de l’installation du plug-in.</span><span class="sxs-lookup"><span data-stu-id="7b24d-176">Windows Media Player runs the UI plug-in automatically when the plug-in is installed.</span></span>                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="7b24d-177">**indicateurs de plug-in \_ \_ LAUNCHPROPERTYPAGE**</span><span class="sxs-lookup"><span data-stu-id="7b24d-177">**PLUGIN\_FLAGS\_LAUNCHPROPERTYPAGE**</span></span> | <span data-ttu-id="7b24d-178">0x20000000</span><span class="sxs-lookup"><span data-stu-id="7b24d-178">0x20000000</span></span> | <span data-ttu-id="7b24d-179">Le lecteur Windows Media appelle [**IWMPPluginUI ::D isplaypropertypage**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage) lorsque le plug-in d’interface utilisateur s’exécute pour la première fois. Si cet indicateur est spécifié, les **indicateurs de plug-in \_ \_ HASPROPERTYPAGE** doivent également être spécifiés.</span><span class="sxs-lookup"><span data-stu-id="7b24d-179">Windows Media Player calls [**IWMPPluginUI::DisplayPropertyPage**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage) when the UI plug-in runs for the first time.If this flag is specified, **PLUGIN\_FLAGS\_HASPROPERTYPAGE** should be specified also.</span></span><br/>                                                                                                                                                             |



 

<span data-ttu-id="7b24d-180">Les constantes suivantes sont définies dans wmpplug. h.</span><span class="sxs-lookup"><span data-stu-id="7b24d-180">The following constants are defined in wmpplug.h.</span></span> <span data-ttu-id="7b24d-181">Ne modifiez pas les valeurs associées à ces constantes.</span><span class="sxs-lookup"><span data-stu-id="7b24d-181">Do not change the values associated with these constants.</span></span>



| <span data-ttu-id="7b24d-182">Nom</span><span class="sxs-lookup"><span data-stu-id="7b24d-182">Name</span></span>                                    | <span data-ttu-id="7b24d-183">Description</span><span class="sxs-lookup"><span data-stu-id="7b24d-183">Description</span></span>                               |
|-----------------------------------------|-------------------------------------------|
| <span data-ttu-id="7b24d-184">**PLUG-in \_ INSTALLREGKEY**</span><span class="sxs-lookup"><span data-stu-id="7b24d-184">**PLUGIN\_INSTALLREGKEY**</span></span>               | <span data-ttu-id="7b24d-185">Emplacement de la clé de registre de plug-in.</span><span class="sxs-lookup"><span data-stu-id="7b24d-185">The location of the plug-in registry key.</span></span> |
| <span data-ttu-id="7b24d-186">**PLUG-in \_ INSTALLREGKEY \_ FRIENDLYNAME**</span><span class="sxs-lookup"><span data-stu-id="7b24d-186">**PLUGIN\_INSTALLREGKEY\_FRIENDLYNAME**</span></span> | <span data-ttu-id="7b24d-187">Nom de la valeur de nom convivial.</span><span class="sxs-lookup"><span data-stu-id="7b24d-187">The name of the friendly name value.</span></span>      |
| <span data-ttu-id="7b24d-188">**Description du plug-in \_ INSTALLREGKEY \_**</span><span class="sxs-lookup"><span data-stu-id="7b24d-188">**PLUGIN\_INSTALLREGKEY\_DESCRIPTION**</span></span>  | <span data-ttu-id="7b24d-189">Nom de la valeur de description.</span><span class="sxs-lookup"><span data-stu-id="7b24d-189">The name of the description value.</span></span>        |
| <span data-ttu-id="7b24d-190">**\_fonctionnalités INSTALLREGKEY du plug-in \_**</span><span class="sxs-lookup"><span data-stu-id="7b24d-190">**PLUGIN\_INSTALLREGKEY\_CAPABILITIES**</span></span> | <span data-ttu-id="7b24d-191">Nom de la valeur des fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="7b24d-191">The name of the capabilities value.</span></span>       |
| <span data-ttu-id="7b24d-192">**désinstaller le plug-in \_ INSTALLREGKEY \_**</span><span class="sxs-lookup"><span data-stu-id="7b24d-192">**PLUGIN\_INSTALLREGKEY\_UNINSTALL**</span></span>    | <span data-ttu-id="7b24d-193">Nom de la valeur du chemin d’accès de désinstallation.</span><span class="sxs-lookup"><span data-stu-id="7b24d-193">The name of the uninstall path value.</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="7b24d-194">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7b24d-194">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b24d-195">**IWMPPluginUI ::D isplayPropertyPage**</span><span class="sxs-lookup"><span data-stu-id="7b24d-195">**IWMPPluginUI::DisplayPropertyPage**</span></span>](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage)
</dt> <dt>

[<span data-ttu-id="7b24d-196">**IWMPPluginUI :: GetProperty**</span><span class="sxs-lookup"><span data-stu-id="7b24d-196">**IWMPPluginUI::GetProperty**</span></span>](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-getproperty)
</dt> <dt>

[<span data-ttu-id="7b24d-197">**IWMPPluginUI :: SetProperty**</span><span class="sxs-lookup"><span data-stu-id="7b24d-197">**IWMPPluginUI::SetProperty**</span></span>](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty)
</dt> <dt>

[<span data-ttu-id="7b24d-198">**Informations de référence sur la programmation de plug-ins d’interface utilisateur**</span><span class="sxs-lookup"><span data-stu-id="7b24d-198">**User Interface Plug-ins Programming Reference**</span></span>](user-interface-plug-ins-programming-reference.md)
</dt> </dl>

 

 





