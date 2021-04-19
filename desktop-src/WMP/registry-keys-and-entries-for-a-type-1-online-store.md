---
title: Clés et entrées de Registre pour un magasin de type 1 en ligne
description: Clés et entrées de Registre pour un magasin de type 1 en ligne
ms.assetid: cf25a004-e0c3-407c-8704-54be3601528b
keywords:
- Magasins en ligne du lecteur Windows Media, registre
- magasins en ligne, registre
- types 1 magasins en ligne, registre
- Registre, type 1 magasins en ligne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1329ad69e91ebce41b258d1e148403f62caceb96
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "106510666"
---
# <a name="registry-keys-and-entries-for-a-type-1-online-store"></a><span data-ttu-id="ab69e-107">Clés et entrées de Registre pour un magasin de type 1 en ligne</span><span class="sxs-lookup"><span data-stu-id="ab69e-107">Registry Keys and Entries for a Type 1 Online Store</span></span>

<span data-ttu-id="ab69e-108">Pour rendre un magasin en ligne de type 1 disponible dans le lecteur Windows Media, le fournisseur de la Banque d’informations en ligne doit créer les sous-clés et les entrées de Registre suivantes sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ab69e-108">To make a type 1 online store available in Windows Media Player, the online store provider must create the following registry subkeys and entries on the user's computer.</span></span>


```C++
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MediaPlayer\Subscriptions\keyName]
"Capabilities"=dword:flags
"SubscriptionObjectGUID"=clsid
"FriendlyName"=friendlyName

[HKEY_CLASSES_ROOT\AppID\appid]
@=pluginName
"DllSurrogate"=""

[HKEY_CLASSES_ROOT\CLSID\clsid]
@=className
"AppID"="appid"

[HKEY_CLASSES_ROOT\CLSID\clsid\InprocServer32]
@=moduleName
"ThreadingModel"="threading"
```



> [!Note]  
> <span data-ttu-id="ab69e-109">La définition de la valeur de DllSurrogate sur la chaîne vide indique que le runtime COM chargera le plug-in du magasin en ligne dans le substitut de la DLL par défaut, dllhost.exe.</span><span class="sxs-lookup"><span data-stu-id="ab69e-109">Setting the value of DllSurrogate to the empty string indicates that the COM runtime will load the online store's plug-in into the default DLL surrogate, dllhost.exe.</span></span>

 

<span data-ttu-id="ab69e-110">Dans la syntaxe précédente du Registre, les symboles en italique sont des espaces réservés pour les noms et les identificateurs globaux uniques (GUID) qui sont spécifiques au magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="ab69e-110">In the preceding registry syntax, the symbols in italic are placeholders for names and globally unique identifiers (GUIDs) that are specific to the online store.</span></span> <span data-ttu-id="ab69e-111">Le tableau suivant décrit ces espaces réservés.</span><span class="sxs-lookup"><span data-stu-id="ab69e-111">The following table describes those placeholders.</span></span>



| <span data-ttu-id="ab69e-112">Espace réservé</span><span class="sxs-lookup"><span data-stu-id="ab69e-112">Placeholder</span></span>    | <span data-ttu-id="ab69e-113">Description</span><span class="sxs-lookup"><span data-stu-id="ab69e-113">Description</span></span>                                                                                                                                                                                                                                                                                                                     |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab69e-114">*keyName*</span><span class="sxs-lookup"><span data-stu-id="ab69e-114">*keyName*</span></span>      | <span data-ttu-id="ab69e-115">Chaîne convenue entre Microsoft et le magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="ab69e-115">A string agreed upon between Microsoft and the online store.</span></span> <span data-ttu-id="ab69e-116">Cette chaîne identifie de façon unique le magasin en ligne. Exemple : « Proseware »</span><span class="sxs-lookup"><span data-stu-id="ab69e-116">This string uniquely identifies the online store.Example: "Proseware"</span></span><br/>                                                                                                                                                                                   |
| <span data-ttu-id="ab69e-117">*flags*</span><span class="sxs-lookup"><span data-stu-id="ab69e-117">*flags*</span></span>        | <span data-ttu-id="ab69e-118">Un or **au niveau du** bit d’une ou de plusieurs fonctionnalités de plug-in signalent que ces indicateurs spécifient si le lecteur Windows Media doit appeler des méthodes particulières de [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner).</span><span class="sxs-lookup"><span data-stu-id="ab69e-118">A bitwise **OR** of one or more plug-in capability flags These flags specify whether Windows Media Player should call particular methods of [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner).</span></span> <span data-ttu-id="ab69e-119">Pour plus d’informations sur les indicateurs pris en charge, consultez le tableau des indicateurs de capacité de plug-in qui suit ce tableau. Exemple : 00000058</span><span class="sxs-lookup"><span data-stu-id="ab69e-119">For information about supported flags, see the table of plug-in capability flags that follows this table.Example: 00000058</span></span><br/> |
| <span data-ttu-id="ab69e-120">*identificateur*</span><span class="sxs-lookup"><span data-stu-id="ab69e-120">*clsid*</span></span>        | <span data-ttu-id="ab69e-121">GUID qui est l’identificateur de classe (CLSID) de la classe qui implémente **IWMPContentPartner** dans le plug-in du magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="ab69e-121">A GUID that is the class identifier (CLSID) for the class that implements **IWMPContentPartner** in the online store's plug-in.</span></span> <span data-ttu-id="ab69e-122">Ce GUID doit être au format de Registre, avec les accolades. Format : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span><span class="sxs-lookup"><span data-stu-id="ab69e-122">This GUID must be in registry format, complete with the curly braces.Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span></span><br/>                                                                  |
| <span data-ttu-id="ab69e-123">*convivial*</span><span class="sxs-lookup"><span data-stu-id="ab69e-123">*friendlyname*</span></span> | <span data-ttu-id="ab69e-124">Nom convivial du magasin en ligne. Exemple : « Proseware Music service »</span><span class="sxs-lookup"><span data-stu-id="ab69e-124">A friendly name for the online store.Example: "Proseware Music Service"</span></span><br/>                                                                                                                                                                                                                                              |
| <span data-ttu-id="ab69e-125">*appid*</span><span class="sxs-lookup"><span data-stu-id="ab69e-125">*appid*</span></span>        | <span data-ttu-id="ab69e-126">GUID qui est l’identificateur d’application (AppID) pour le plug-in du magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="ab69e-126">A GUID that is the application identifier (AppID) for the online store's plug-in.</span></span> <span data-ttu-id="ab69e-127">Ce GUID doit être au format de Registre, avec les accolades. Format : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span><span class="sxs-lookup"><span data-stu-id="ab69e-127">This GUID must be in registry format, complete with the curly braces.Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span></span><br/>                                                                                                                |
| <span data-ttu-id="ab69e-128">*pluginName*</span><span class="sxs-lookup"><span data-stu-id="ab69e-128">*pluginName*</span></span>   | <span data-ttu-id="ab69e-129">Nom du plug-in du magasin en ligne. Exemple : « plug-in de partenaire de contenu Proseware »</span><span class="sxs-lookup"><span data-stu-id="ab69e-129">A name for the online store's plug-in.Example: "Proseware Content Partner Plug-in"</span></span><br/>                                                                                                                                                                                                                                   |
| <span data-ttu-id="ab69e-130">*ClassName*</span><span class="sxs-lookup"><span data-stu-id="ab69e-130">*className*</span></span>    | <span data-ttu-id="ab69e-131">Nom de la classe qui implémente **IWMPContentpartner** dans le plug-in du magasin en ligne. Exemple : « CProsewarePartner »</span><span class="sxs-lookup"><span data-stu-id="ab69e-131">The name of the class that implements **IWMPContentpartner** in the online store's plug-in.Example: "CProsewarePartner"</span></span><br/>                                                                                                                                                                                              |
| <span data-ttu-id="ab69e-132">*NomModule*</span><span class="sxs-lookup"><span data-stu-id="ab69e-132">*moduleName*</span></span>   | <span data-ttu-id="ab69e-133">Chemin d’accès complet à la DLL qui implémente le plug-in du magasin en ligne. Exemple : « C : \\ Program Files \\ proseware \\ProsewarePartner.dll »</span><span class="sxs-lookup"><span data-stu-id="ab69e-133">The fully qualified path to the DLL that implements the online store's plug-in.Example: "C:\\Program Files\\Proseware\\ProsewarePartner.dll"</span></span><br/>                                                                                                                                                                         |
| <span data-ttu-id="ab69e-134">*Threading*</span><span class="sxs-lookup"><span data-stu-id="ab69e-134">*threading*</span></span>    | <span data-ttu-id="ab69e-135">Type de cloisonnement dans lequel le plug-in est exécuté.</span><span class="sxs-lookup"><span data-stu-id="ab69e-135">The type of apartment the plug-in runs in.</span></span> <span data-ttu-id="ab69e-136">« ThreadingModel » = « Apartment » indique que le plug-in s’exécute dans un thread cloisonné (STA).</span><span class="sxs-lookup"><span data-stu-id="ab69e-136">"ThreadingModel"="Apartment" indicates that the plug-in runs in a single-threaded apartment (STA).</span></span> <span data-ttu-id="ab69e-137">"ThreadingModel" = "Free" indique que le plug-in s’exécute dans le cloisonnement multithread (MTA).</span><span class="sxs-lookup"><span data-stu-id="ab69e-137">"ThreadingModel"="Free" indicates that the plug-in runs in the multithreaded apartment (MTA).</span></span>                                                                                     |



 

<span data-ttu-id="ab69e-138">Le tableau suivant décrit les indicateurs de capacité de plug-in.</span><span class="sxs-lookup"><span data-stu-id="ab69e-138">The following table describes the plug-in capability flags.</span></span>



| <span data-ttu-id="ab69e-139">Indicateur</span><span class="sxs-lookup"><span data-stu-id="ab69e-139">Flag</span></span>                                    | <span data-ttu-id="ab69e-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="ab69e-140">Value</span></span> | <span data-ttu-id="ab69e-141">Description</span><span class="sxs-lookup"><span data-stu-id="ab69e-141">Description</span></span>                                                                                                                                                                                                                                                                 |
|-----------------------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab69e-142">limite d’abonnement \_ \_ BACKGROUNDPROCESSING</span><span class="sxs-lookup"><span data-stu-id="ab69e-142">SUBSCRIPTION\_CAP\_BACKGROUNDPROCESSING</span></span> | <span data-ttu-id="ab69e-143">0x8</span><span class="sxs-lookup"><span data-stu-id="ab69e-143">0x8</span></span>   | <span data-ttu-id="ab69e-144">Le lecteur Windows Media doit appeler [IWMPContentPartner :: Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-notify) pour informer le plug-in lorsqu’il doit démarrer et arrêter le traitement en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="ab69e-144">Windows Media Player should call [IWMPContentPartner::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-notify) to inform the plug-in when it should start and stop background processing.</span></span>                                                                                                     |
| <span data-ttu-id="ab69e-145">limite d’abonnement \_ \_ DEVICEAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="ab69e-145">SUBSCRIPTION\_CAP\_DEVICEAVAILABLE</span></span>      | <span data-ttu-id="ab69e-146">0x10</span><span class="sxs-lookup"><span data-stu-id="ab69e-146">0x10</span></span>  | <span data-ttu-id="ab69e-147">Le lecteur Windows Media doit appeler [IWMPContentPartner :: UpdateDevice](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-updatedevice).</span><span class="sxs-lookup"><span data-stu-id="ab69e-147">Windows Media Player should call [IWMPContentPartner::UpdateDevice](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-updatedevice).</span></span>                                                                                                                                                                   |
| <span data-ttu-id="ab69e-148">la limite d’abonnement \_ \_ est \_ CONTENTPARTNER</span><span class="sxs-lookup"><span data-stu-id="ab69e-148">SUBSCRIPTION\_CAP\_IS\_CONTENTPARTNER</span></span>   | <span data-ttu-id="ab69e-149">0x40</span><span class="sxs-lookup"><span data-stu-id="ab69e-149">0x40</span></span>  | <span data-ttu-id="ab69e-150">Informe le lecteur Windows Media que le plug-in implémente l’interface **IWMPContentPartner** .</span><span class="sxs-lookup"><span data-stu-id="ab69e-150">Informs Windows Media Player that the plug-in implements the **IWMPContentPartner** interface.</span></span> <span data-ttu-id="ab69e-151">Tous les plug-ins de magasin en ligne de type 1 doivent définir cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="ab69e-151">All type 1 online store plug-ins must set this flag.</span></span>                                                                                                                         |
| <span data-ttu-id="ab69e-152">limite d’abonnement \_ \_ ALTLOGIN</span><span class="sxs-lookup"><span data-stu-id="ab69e-152">SUBSCRIPTION\_CAP\_ALTLOGIN</span></span>             | <span data-ttu-id="ab69e-153">0x80</span><span class="sxs-lookup"><span data-stu-id="ab69e-153">0x80</span></span>  | <span data-ttu-id="ab69e-154">Informe le lecteur Windows Media que le plug-in prend en charge une autre connexion.</span><span class="sxs-lookup"><span data-stu-id="ab69e-154">Informs Windows Media Player that the plug-in supports an alternate login.</span></span> <span data-ttu-id="ab69e-155">Si le plug-in prend en charge une autre connexion, le lecteur Windows Media récupère l’URL de connexion de substitution et la légende en appelant [IWMPContentPartner :: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo).</span><span class="sxs-lookup"><span data-stu-id="ab69e-155">If the plug-in supports an alternate login, Windows Media Player retrieves the alternate login URL and caption by calling [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo).</span></span> |



 

<span data-ttu-id="ab69e-156">**Entrées de Registre pour le développement et le test**</span><span class="sxs-lookup"><span data-stu-id="ab69e-156">**Registry Entries for Development and Testing**</span></span>

<span data-ttu-id="ab69e-157">Lorsque vous commencez à développer votre boutique en ligne, Microsoft vous propose deux clés : une clé de test et une clé de production.</span><span class="sxs-lookup"><span data-stu-id="ab69e-157">When you begin developing your online store, Microsoft provides you with two keys: a test key and a production key.</span></span> <span data-ttu-id="ab69e-158">Pendant la phase de développement et de test, votre magasin en ligne s’affiche dans le lecteur Windows Media uniquement si votre clé de test ou votre clé de production se trouve dans le registre sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ab69e-158">During the development and testing phase, your online store will appear in Windows Media Player only if your test key or your production key is in the registry on the user's computer.</span></span> <span data-ttu-id="ab69e-159">Pour plus d’informations sur les clés de test et de production, consultez [clés de test et de production pour un magasin de type 1 en ligne](test-and-production-keys-for-a-type-1-online-store.md).</span><span class="sxs-lookup"><span data-stu-id="ab69e-159">For more information about the test and production keys, see [Test and Production Keys for a Type 1 Online Store](test-and-production-keys-for-a-type-1-online-store.md).</span></span>

<span data-ttu-id="ab69e-160">Placez votre clé de test ou de production à l’emplacement suivant dans le registre.</span><span class="sxs-lookup"><span data-stu-id="ab69e-160">Place your test or production key in the following location in the registry.</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Services]
"TestParameter" = "key1;key2;...;keyN"
```



<span data-ttu-id="ab69e-161">Notez que la valeur de l’entrée de Registre TestParameter peut spécifier plusieurs clés de test ou de production.</span><span class="sxs-lookup"><span data-stu-id="ab69e-161">Note that the value of the TestParameter registry entry can specify multiple test or production keys.</span></span> <span data-ttu-id="ab69e-162">Par exemple, supposons que Proseware a une clé de test de « 1234 » et que contoso a une clé de test « 2345 ».</span><span class="sxs-lookup"><span data-stu-id="ab69e-162">For example, suppose that Proseware has a test key of "1234" and Contoso has a test key of "2345".</span></span> <span data-ttu-id="ab69e-163">L’entrée de Registre suivante spécifie que les banques de test pour Proseware et contoso s’affichent dans le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="ab69e-163">The following registry entry specifies that the test stores for Proseware and Contoso will appear in Windows Media Player.</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Services]
"TestParameter" = "1234;2345"
```



<span data-ttu-id="ab69e-164">**Entrée de Registre ActiveService**</span><span class="sxs-lookup"><span data-stu-id="ab69e-164">**ActiveService Registry Entry**</span></span>

<span data-ttu-id="ab69e-165">Lorsque l’utilisateur active un magasin en ligne, le lecteur Windows Media écrit des informations dans le Registre qui identifient le magasin en ligne actif.</span><span class="sxs-lookup"><span data-stu-id="ab69e-165">When the user activates an online store, Windows Media Player writes information in the registry that identifies the active online store.</span></span> <span data-ttu-id="ab69e-166">Le lecteur Windows Media place les informations à l’emplacement suivant dans le registre sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ab69e-166">Windows Media Player places the information in the following location in the registry on the user's computer.</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Subscriptions]
"ActiveService"=serviceInfo
```



<span data-ttu-id="ab69e-167">Dans la syntaxe précédente du Registre, *serviceInfo* est un espace réservé pour une chaîne qui contient des informations descriptives sur le magasin en ligne actif.</span><span class="sxs-lookup"><span data-stu-id="ab69e-167">In the preceding registry syntax, *serviceInfo* is a placeholder for a string that contains descriptive information about the active online store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ab69e-168">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ab69e-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab69e-169">**Référence pour les magasins en ligne de type 1**</span><span class="sxs-lookup"><span data-stu-id="ab69e-169">**Reference for Type 1 Online Stores**</span></span>](reference-for-type-1-online-stores.md)
</dt> </dl>

 

 





