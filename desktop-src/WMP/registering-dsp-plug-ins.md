---
title: Inscription des plug-ins DSP
description: Inscription des plug-ins DSP
ms.assetid: af264ff7-702b-4a49-a14d-ab8563a40c4e
keywords:
- Plug-ins du lecteur Windows Media, entrées de Registre
- plug-ins, entrées de Registre
- plug-ins de traitement de signal numérique, entrées de Registre
- Plug-ins DSP, entrées de Registre
- Registre, plug-ins DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64e7afd43cf242d57c0a9375c4cbda56e457ef1
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103940689"
---
# <a name="registering-dsp-plug-ins"></a><span data-ttu-id="be82a-108">Inscription des plug-ins DSP</span><span class="sxs-lookup"><span data-stu-id="be82a-108">Registering DSP Plug-ins</span></span>

<span data-ttu-id="be82a-109">Pour que votre plug-in DSP soit disponible dans le lecteur Windows Media, vous devez créer les sous-clés et les entrées de Registre suivantes sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="be82a-109">To make your DSP plug-in available in Windows Media Player you must create the following registry subkeys and entries on the user's computer.</span></span>


```C++
[HKEY_CLASSES_ROOT\CLSID\PluginClsid]
@=PluginClassFriendlyName

[HKEY_CLASSES_ROOT\CLSID\PluginClsid\InprocServer32]
@=PluginModuleName
"ThreadingModel"="Threading"
```



<span data-ttu-id="be82a-110">Dans la syntaxe précédente du Registre, les symboles en italique sont des espaces réservés pour les noms et les identificateurs globaux uniques (GUID) qui sont spécifiques au plug-in DSP.</span><span class="sxs-lookup"><span data-stu-id="be82a-110">In the preceding registry syntax, the symbols in italic are placeholders for names and globally unique identifiers (GUIDs) that are specific to the DSP plug-in.</span></span> <span data-ttu-id="be82a-111">Le tableau suivant décrit ces espaces réservés.</span><span class="sxs-lookup"><span data-stu-id="be82a-111">The following table describes those placeholders.</span></span>



| <span data-ttu-id="be82a-112">Espace réservé</span><span class="sxs-lookup"><span data-stu-id="be82a-112">Placeholder</span></span>               | <span data-ttu-id="be82a-113">Description</span><span class="sxs-lookup"><span data-stu-id="be82a-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be82a-114">*PluginClsid*</span><span class="sxs-lookup"><span data-stu-id="be82a-114">*PluginClsid*</span></span>             | <span data-ttu-id="be82a-115">GUID qui est l’identificateur de classe de la classe principale du plug-in DSP.</span><span class="sxs-lookup"><span data-stu-id="be82a-115">A GUID that is the class identifier for the DSP plug-in's primary class.</span></span> <span data-ttu-id="be82a-116">Il s’agit de la classe qui implémente **IMediaObject**, **IPluginEnable** et éventuellement **ISpecifyPropertyPages**.</span><span class="sxs-lookup"><span data-stu-id="be82a-116">This is the class that implements **IMediaObject**, **IPluginEnable**, and possibly **ISpecifyPropertyPages**.</span></span> <span data-ttu-id="be82a-117">Dans un plug-in en mode double, cette classe implémente également **IMFTransform** et **IMFGetService**. Ce GUID doit être au format de Registre, avec les accolades.</span><span class="sxs-lookup"><span data-stu-id="be82a-117">In a dual-mode plug-in, this class also implements **IMFTransform** and **IMFGetService**.This GUID must be in registry format, complete with the curly braces.</span></span><br/> <span data-ttu-id="be82a-118">Format : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span><span class="sxs-lookup"><span data-stu-id="be82a-118">Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span></span><br/> |
| <span data-ttu-id="be82a-119">*PluginClassFriendlyName*</span><span class="sxs-lookup"><span data-stu-id="be82a-119">*PluginClassFriendlyName*</span></span> | <span data-ttu-id="be82a-120">Nom convivial de la classe principale du plug-in DSP. Exemple : « ProsewareDSP Class »</span><span class="sxs-lookup"><span data-stu-id="be82a-120">A friendly name for the DSP plug-in's primary class.Example: "ProsewareDSP Class"</span></span><br/>                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="be82a-121">*PluginModuleName*</span><span class="sxs-lookup"><span data-stu-id="be82a-121">*PluginModuleName*</span></span>        | <span data-ttu-id="be82a-122">Chemin d’accès qualifié complet à la DLL qui implémente le plug-in DSP. Exemple : « C : \\ Program Files \\ proseware \\ProsewareDsp.dll »</span><span class="sxs-lookup"><span data-stu-id="be82a-122">The fully qualified path to the DLL that implements the DSP plug-in.Example: "C:\\Program Files\\Proseware\\ProsewareDsp.dll"</span></span><br/>                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="be82a-123">*Threads*</span><span class="sxs-lookup"><span data-stu-id="be82a-123">*Threading*</span></span>               | <span data-ttu-id="be82a-124">Chaîne qui spécifie le modèle de thread pour le plug-in.</span><span class="sxs-lookup"><span data-stu-id="be82a-124">A string that specifies the threading model for the plug-in.</span></span> <span data-ttu-id="be82a-125">Si le plug-in va s’exécuter avec le lecteur Windows Media 11 sur Windows Vista, cette entrée de registre doit être égale à « both ».</span><span class="sxs-lookup"><span data-stu-id="be82a-125">If the plug-in is going to run with Windows Media Player 11 on Windows Vista, this registry entry must be equal to "Both".</span></span> <span data-ttu-id="be82a-126">Si le plug-in va s’exécuter sur Windows XP ou des systèmes d’exploitation antérieurs, cette entrée de Registre peut être égale à « Apartment » ou « Both ».</span><span class="sxs-lookup"><span data-stu-id="be82a-126">If the plug-in is going to run on Windows XP or older operating systems, this registry entry can be equal to either "Apartment" or "Both".</span></span>                                                                                           |



 

<span data-ttu-id="be82a-127">Si votre plug-in DSP implémente une interface personnalisée et si votre plug-in va s’exécuter dans le lecteur Windows Media 11 sur Windows Vista, vous devez créer les sous-clés et les entrées de Registre suivantes sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="be82a-127">If your DSP plug-in implements a custom interface and if your plug-in is going to run in Windows Media Player 11 on Windows Vista, you must create the following registry subkeys and entries on the user's computer.</span></span>


```C++
[HKEY_CLASSES_ROOT\CLSID\ProxyStubClsid]
@=PSFactoryBuffer

[HKEY_CLASSES_ROOT\CLSID\ProxyStubClsid\InprocServer32]
@=ProxyStubModuleName
"ThreadingModel"="Apartment"

[HKEY_CLASSES_ROOT\Interfaces\CustomInterfaceId]
@=CustomInterfaceName

[HKEY_CLASSES_ROOT\Interfaces\CustomInterfaceId\NumMethods]
@=NumberOfMethods

[HKEY_CLASSES_ROOT\Interfaces\CustomInterfaceId\ProxyStubClsid32]
@=ProxyStubClsid
```



<span data-ttu-id="be82a-128">Dans la syntaxe précédente du Registre, les symboles en italique sont des espaces réservés pour les noms, les valeurs numériques et les identificateurs globaux uniques (GUID) qui sont spécifiques au plug-in DSP.</span><span class="sxs-lookup"><span data-stu-id="be82a-128">In the preceding registry syntax, the symbols in italic are placeholders for names, numeric values, and globally unique identifiers (GUIDs) that are specific to the DSP plug-in.</span></span> <span data-ttu-id="be82a-129">Le tableau suivant décrit ces espaces réservés.</span><span class="sxs-lookup"><span data-stu-id="be82a-129">The following table describes those placeholders.</span></span>



| <span data-ttu-id="be82a-130">Espace réservé</span><span class="sxs-lookup"><span data-stu-id="be82a-130">Placeholder</span></span>           | <span data-ttu-id="be82a-131">Description</span><span class="sxs-lookup"><span data-stu-id="be82a-131">Description</span></span>                                                                                                                                                                                                                                                                |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be82a-132">*ProxyStubClsid*</span><span class="sxs-lookup"><span data-stu-id="be82a-132">*ProxyStubClsid*</span></span>      | <span data-ttu-id="be82a-133">GUID qui est l’identificateur de classe de la classe qui implémente les proxies et les stubs pour les interfaces personnalisées du plug-in DSP. Ce GUID doit être au format de Registre, avec les accolades.</span><span class="sxs-lookup"><span data-stu-id="be82a-133">A GUID that is the class identifier for the class that implements the proxies and stubs for the DSP plug-in's custom interfaces.This GUID must be in registry format, complete with the curly braces.</span></span><br/> <span data-ttu-id="be82a-134">Format : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span><span class="sxs-lookup"><span data-stu-id="be82a-134">Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span></span><br/> |
| <span data-ttu-id="be82a-135">*ProxyStubModuleName*</span><span class="sxs-lookup"><span data-stu-id="be82a-135">*ProxyStubModuleName*</span></span> | <span data-ttu-id="be82a-136">Le chemin d’accès complet à la DLL qui implémente les interfaces de proxy et stub pour le plug-in DSP. Exemple : « C : \\ Program Files \\ proseware \\ProsewareDspPS.dll »</span><span class="sxs-lookup"><span data-stu-id="be82a-136">The fully qualified path to the DLL that implements the proxy and stub interfaces for the DSP plug-in.Example: "C:\\Program Files\\Proseware\\ProsewareDspPS.dll"</span></span><br/>                                                                                               |
| <span data-ttu-id="be82a-137">*CustomInterfaceId*</span><span class="sxs-lookup"><span data-stu-id="be82a-137">*CustomInterfaceId*</span></span>   | <span data-ttu-id="be82a-138">GUID qui est l’identificateur d’interface d’une interface personnalisée qui est implémentée par le plug-in DSP. Ce GUID doit être au format de Registre, avec les accolades.</span><span class="sxs-lookup"><span data-stu-id="be82a-138">A GUID that is the interface identifier for a custom interface that is implemented by the DSP plug-in.This GUID must be in registry format, complete with the curly braces.</span></span><br/> <span data-ttu-id="be82a-139">Format : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span><span class="sxs-lookup"><span data-stu-id="be82a-139">Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span></span><br/>                           |
| <span data-ttu-id="be82a-140">*CustomInterfaceName*</span><span class="sxs-lookup"><span data-stu-id="be82a-140">*CustomInterfaceName*</span></span> | <span data-ttu-id="be82a-141">Nom d’une interface personnalisée qui est implémentée par le plug-in DSP. Exemple : « IProsewareDsp »</span><span class="sxs-lookup"><span data-stu-id="be82a-141">The name of a custom interface that is implemented by the DSP plug-in.Example: "IProsewareDsp"</span></span><br/>                                                                                                                                                                  |
| <span data-ttu-id="be82a-142">*NumberOfMethods*</span><span class="sxs-lookup"><span data-stu-id="be82a-142">*NumberOfMethods*</span></span>     | <span data-ttu-id="be82a-143">Nombre de méthodes, y compris les méthodes héritées, définies par une interface personnalisée. Exemple : « 5 »</span><span class="sxs-lookup"><span data-stu-id="be82a-143">The number of methods, including inherited methods, defined by a custom interface.Example: "5"</span></span><br/>                                                                                                                                                                  |



 

<span data-ttu-id="be82a-144">Si votre plug-in DSP fournit une page de propriétés, vous devez créer les sous-clés et les entrées de Registre suivantes sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="be82a-144">If your DSP plug-in provides a property page, you must create the following registry subkeys and entries on the user's computer.</span></span>


```C++
[HKEY_CLASSES_ROOT\CLSID\PropPageClsid]
@=PropPageClassFriendlyName

[HKEY_CLASSES_ROOT\CLSID\PropPageClsid\InprocServer32]
@=PluginModuleName
"ThreadingModel"="Apartment"
```



<span data-ttu-id="be82a-145">Dans la syntaxe précédente du Registre, les symboles en italique sont des espaces réservés pour les noms et les identificateurs globaux uniques (GUID) qui sont spécifiques au plug-in DSP.</span><span class="sxs-lookup"><span data-stu-id="be82a-145">In the preceding registry syntax, the symbols in italic are placeholders for names and globally unique identifiers (GUIDs) that are specific to the DSP plug-in.</span></span> <span data-ttu-id="be82a-146">Le tableau suivant décrit ces espaces réservés.</span><span class="sxs-lookup"><span data-stu-id="be82a-146">The following table describes those placeholders.</span></span>



| <span data-ttu-id="be82a-147">Espace réservé</span><span class="sxs-lookup"><span data-stu-id="be82a-147">Placeholder</span></span>                 | <span data-ttu-id="be82a-148">Description</span><span class="sxs-lookup"><span data-stu-id="be82a-148">Description</span></span>                                                                                                                                                                                                                            |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be82a-149">*PropPageClsid*</span><span class="sxs-lookup"><span data-stu-id="be82a-149">*PropPageClsid*</span></span>             | <span data-ttu-id="be82a-150">GUID qui est l’identificateur de classe pour la classe de page de propriétés fournie par le plug-in DSP. Ce GUID doit être au format de Registre, avec les accolades.</span><span class="sxs-lookup"><span data-stu-id="be82a-150">A GUID that is the class identifier for the property page class provided by the DSP plug-in.This GUID must be in registry format, complete with the curly braces.</span></span><br/> <span data-ttu-id="be82a-151">Format : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span><span class="sxs-lookup"><span data-stu-id="be82a-151">Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span></span><br/> |
| <span data-ttu-id="be82a-152">*PropPageClassFriendlyName*</span><span class="sxs-lookup"><span data-stu-id="be82a-152">*PropPageClassFriendlyName*</span></span> | <span data-ttu-id="be82a-153">Nom convivial de la classe de la page de propriétés. Exemple : « ProsewareDSP Property page Class »</span><span class="sxs-lookup"><span data-stu-id="be82a-153">A friendly name for the property page class.Example: "ProsewareDSP Property Page Class"</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="be82a-154">*PluginModuleName*</span><span class="sxs-lookup"><span data-stu-id="be82a-154">*PluginModuleName*</span></span>          | <span data-ttu-id="be82a-155">Chemin d’accès qualifié complet à la DLL qui implémente le plug-in DSP. Exemple : « C : \\ Program Files \\ proseware \\ProsewareDsp.dll »</span><span class="sxs-lookup"><span data-stu-id="be82a-155">The fully qualified path to the DLL that implements the DSP plug-in.Example: "C:\\Program Files\\Proseware\\ProsewareDsp.dll"</span></span><br/>                                                                                               |



 

<span data-ttu-id="be82a-156">**Appel de IWMPPluginRegistrar**</span><span class="sxs-lookup"><span data-stu-id="be82a-156">**Calling IWMPPluginRegistrar**</span></span>

<span data-ttu-id="be82a-157">Outre les sous-clés et les entrées de Registre décrites dans les listes et les tables précédentes, vous devez créer des clés et des entrées de registre en appelant [IWMPMediaPluginRegistrar :: WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin).</span><span class="sxs-lookup"><span data-stu-id="be82a-157">In addition to the registry subkeys and entries described in the preceding lists and tables, you must create some registry keys and entries by calling [IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin).</span></span> <span data-ttu-id="be82a-158">Cette méthode effectue l’inscription nécessaire pour permettre au lecteur Windows Media de reconnaître votre plug-in et de le présenter en tant qu’option à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="be82a-158">This method performs the necessary registration to enable Windows Media Player to recognize your plug-in and present it as an option to the user.</span></span>

<span data-ttu-id="be82a-159">Appelez **IWMPMediaPluginRegistrar :: WMPRegisterPlayerPlugin** dans la fonction **DllRegisterServer** de votre plug-in, puis appelez [IWMPMediaPluginRegistrar :: WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) dans la fonction **DllUnregisterServer** de votre plug-in.</span><span class="sxs-lookup"><span data-stu-id="be82a-159">Call **IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin** in your plug-in's **DllRegisterServer** function, and call [IWMPMediaPluginRegistrar::WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) in your plug-in's **DllUnregisterServer** function.</span></span> <span data-ttu-id="be82a-160">Pour obtenir un pointeur vers une interface **IWMPMediaPluginRegistrar** , appelez **CoCreateInstance**, en passant \_ le CLSID WMPMediaPluginRegistrar en tant qu’ID de classe.</span><span class="sxs-lookup"><span data-stu-id="be82a-160">To get a pointer to an **IWMPMediaPluginRegistrar** interface, call **CoCreateInstance**, passing CLSID\_WMPMediaPluginRegistrar as the Class ID.</span></span> <span data-ttu-id="be82a-161">Le CLSID \_ de constante WMPMediaPluginRegistrar est défini dans wmpservices. h.</span><span class="sxs-lookup"><span data-stu-id="be82a-161">The constant CLSID\_WMPMediaPluginRegistrar is defined in wmpservices.h.</span></span>

<span data-ttu-id="be82a-162">**Inscription dans l’Assistant de plug-in DSP**</span><span class="sxs-lookup"><span data-stu-id="be82a-162">**Registration in the DSP Plug-in Wizard**</span></span>

<span data-ttu-id="be82a-163">L’Assistant de plug-in DSP, qui est inclus dans le SDK Windows, génère un exemple de code basé sur Active Template Library (ATL).</span><span class="sxs-lookup"><span data-stu-id="be82a-163">The DSP plug-in wizard, which is included in the Windows SDK, generates sample code that is based on Active Template Library (ATL).</span></span> <span data-ttu-id="be82a-164">L’exemple de fonction **DllRegisterServer** du plug-in appelle la fonction **RegisterServer** de la bibliothèque ATL, qui crée des sous-clés et des entrées de registre en fonction de deux fichiers de script du Registre dans le projet Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="be82a-164">The sample plug-in's **DllRegisterServer** function calls ATL's **RegisterServer** function, which creates registry subkeys and entries according to two registry script files in the Visual Studio project.</span></span> <span data-ttu-id="be82a-165">Le fichier *ProjectName*. RGS contient le script d’enregistrement de la classe principale du plug-in, et le fichier *nom_projet* PropPage. RGS contient le script d’enregistrement de la classe de la page de propriétés du plug-in.</span><span class="sxs-lookup"><span data-stu-id="be82a-165">The file *ProjectName*.rgs contains the script for registering the plug-in's main class, and the file *ProjectName* PropPage.rgs contains the script for registering the plug-in's property page class.</span></span> <span data-ttu-id="be82a-166">L’exemple de fonction **DllRegisterServer** du plug-in appelle également **IWMPPluginRegistrar :: WMPRegisterPlayerPlugin**.</span><span class="sxs-lookup"><span data-stu-id="be82a-166">The sample plug-in's **DllRegisterServer** function also calls **IWMPPluginRegistrar::WMPRegisterPlayerPlugin**.</span></span>

<span data-ttu-id="be82a-167">L’Assistant de plug-in DSP génère également du code pour un composant proxy-stub qui est un fichier. dll à inscription automatique.</span><span class="sxs-lookup"><span data-stu-id="be82a-167">The DSP plug-in wizard also generates code for a proxy-stub component that is a self-registering .dll file.</span></span> <span data-ttu-id="be82a-168">Le code d’inscription de ce fichier se trouve dans dlldata. cpp.</span><span class="sxs-lookup"><span data-stu-id="be82a-168">The registration code for that file is in dlldata.cpp.</span></span> <span data-ttu-id="be82a-169">La macro **DLLDATA \_ routines** se développe pour inclure une implémentation de **DllRegisterServer**.</span><span class="sxs-lookup"><span data-stu-id="be82a-169">The macro **DLLDATA\_ROUTINES** expands to include an implementation of **DllRegisterServer**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="be82a-170">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="be82a-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be82a-171">**Vue d’ensemble des développeurs de plug-ins DSP**</span><span class="sxs-lookup"><span data-stu-id="be82a-171">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> <dt>

[<span data-ttu-id="be82a-172">**IWMPMediaPluginRegistrar**</span><span class="sxs-lookup"><span data-stu-id="be82a-172">**IWMPMediaPluginRegistrar**</span></span>](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpmediapluginregistrar)
</dt> </dl>

 

 





