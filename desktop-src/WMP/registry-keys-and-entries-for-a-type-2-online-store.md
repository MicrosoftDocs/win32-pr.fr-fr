---
title: Clés et entrées de Registre pour un magasin de type 2 en ligne
description: Clés et entrées de Registre pour un magasin de type 2 en ligne
ms.assetid: 17dff940-3884-488a-9016-29bb47c51caf
keywords:
- Magasins en ligne du lecteur Windows Media, registre
- magasins en ligne, registre
- type 2 magasins en ligne, registre
- Registre, type 2 magasins en ligne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 685a26514730e7c370c698cbc9c64c29366c35ee
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104101333"
---
# <a name="registry-keys-and-entries-for-a-type-2-online-store"></a><span data-ttu-id="b2aae-107">Clés et entrées de Registre pour un magasin de type 2 en ligne</span><span class="sxs-lookup"><span data-stu-id="b2aae-107">Registry Keys and Entries for a Type 2 Online Store</span></span>

> [!Note]  
> <span data-ttu-id="b2aae-108">Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="b2aae-108">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="b2aae-109">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="b2aae-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="b2aae-110">Pour rendre disponible un magasin en ligne de type 2 dans le lecteur Windows Media, le fournisseur de la Banque d’informations en ligne doit créer les sous-clés et les entrées de Registre suivantes sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b2aae-110">To make a type 2 online store available in Windows Media Player, the online store provider must create the following registry subkeys and entries on the user's computer.</span></span>


```C++
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MediaPlayer\Subscriptions\keyName]
"Capabilities"=dword:flags
"SubscriptionObjectGUID"=clsid
"FriendlyName"=friendlyName

[HKEY_CLASSES_ROOT\CLSID\clsid]
@=className

[HKEY_CLASSES_ROOT\CLSID\clsid\InprocServer32]
@=moduleName
"ThreadingModel"="Apartment"
```



<span data-ttu-id="b2aae-111">Dans la syntaxe précédente du Registre, les symboles en italique sont des espaces réservés pour les noms et les identificateurs globaux uniques (GUID) qui sont spécifiques au magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="b2aae-111">In the preceding registry syntax, the symbols in italic are placeholders for names and globally unique identifiers (GUIDs) that are specific to the online store.</span></span> <span data-ttu-id="b2aae-112">Le tableau suivant décrit ces espaces réservés.</span><span class="sxs-lookup"><span data-stu-id="b2aae-112">The following table describes those placeholders.</span></span>



| <span data-ttu-id="b2aae-113">Espace réservé</span><span class="sxs-lookup"><span data-stu-id="b2aae-113">Placeholder</span></span>    | <span data-ttu-id="b2aae-114">Description</span><span class="sxs-lookup"><span data-stu-id="b2aae-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                            |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2aae-115">*keyName*</span><span class="sxs-lookup"><span data-stu-id="b2aae-115">*keyName*</span></span>      | <span data-ttu-id="b2aae-116">Chaîne convenue entre Microsoft et le magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="b2aae-116">A string agreed upon between Microsoft and the online store.</span></span> <span data-ttu-id="b2aae-117">Cette chaîne identifie de façon unique le magasin en ligne. Exemple : « Proseware »</span><span class="sxs-lookup"><span data-stu-id="b2aae-117">This string uniquely identifies the online store.Example: "Proseware"</span></span><br/>                                                                                                                                                                                                                                                          |
| <span data-ttu-id="b2aae-118">*flags*</span><span class="sxs-lookup"><span data-stu-id="b2aae-118">*flags*</span></span>        | <span data-ttu-id="b2aae-119">Un or **au niveau du** bit d’une ou de plusieurs fonctionnalités de plug-in signalent que ces indicateurs spécifient si le lecteur Windows Media doit appeler des méthodes particulières de [IWMPSubscriptionService](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice) et [IWMPSubscriptionService2](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2).</span><span class="sxs-lookup"><span data-stu-id="b2aae-119">A bitwise **OR** of one or more plug-in capability flags These flags specify whether Windows Media Player should call particular methods of [IWMPSubscriptionService](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice) and [IWMPSubscriptionService2](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2).</span></span> <span data-ttu-id="b2aae-120">Pour plus d’informations sur les indicateurs pris en charge, consultez le tableau des indicateurs de capacité de plug-in qui suit ce tableau. Exemple : 00000037</span><span class="sxs-lookup"><span data-stu-id="b2aae-120">For information about supported flags, see the table of plug-in capability flags that follows this table.Example: 00000037</span></span><br/> |
| <span data-ttu-id="b2aae-121">*identificateur*</span><span class="sxs-lookup"><span data-stu-id="b2aae-121">*clsid*</span></span>        | <span data-ttu-id="b2aae-122">GUID qui est l’identificateur de classe (CLSID) de la classe qui implémente **IWMPSubscriptionService** dans le plug-in du magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="b2aae-122">A GUID that is the class identifier (CLSID) for the class that implements **IWMPSubscriptionService** in the online store's plug-in.</span></span> <span data-ttu-id="b2aae-123">Ce GUID doit être au format de Registre, avec les accolades. Format : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span><span class="sxs-lookup"><span data-stu-id="b2aae-123">This GUID must be in registry format, complete with the curly braces.Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span></span><br/>                                                                                                                                    |
| <span data-ttu-id="b2aae-124">*convivial*</span><span class="sxs-lookup"><span data-stu-id="b2aae-124">*friendlyname*</span></span> | <span data-ttu-id="b2aae-125">Nom convivial du magasin en ligne. Exemple : « Proseware Music service »</span><span class="sxs-lookup"><span data-stu-id="b2aae-125">A friendly name for the online store.Example: "Proseware Music Service"</span></span><br/>                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="b2aae-126">*pluginName*</span><span class="sxs-lookup"><span data-stu-id="b2aae-126">*pluginName*</span></span>   | <span data-ttu-id="b2aae-127">Nom du plug-in du magasin en ligne. Exemple : « plug-in de service Proseware »</span><span class="sxs-lookup"><span data-stu-id="b2aae-127">A name for the online store's plug-in.Example: "Proseware Service Plug-in"</span></span><br/>                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="b2aae-128">*ClassName*</span><span class="sxs-lookup"><span data-stu-id="b2aae-128">*className*</span></span>    | <span data-ttu-id="b2aae-129">Nom de la classe qui implémente **IWMPSubscriptionService** dans le plug-in du magasin en ligne. Exemple : « CProsewareService »</span><span class="sxs-lookup"><span data-stu-id="b2aae-129">The name of the class that implements **IWMPSubscriptionService** in the online store's plug-in.Example: "CProsewareService"</span></span><br/>                                                                                                                                                                                                                                                                |
| <span data-ttu-id="b2aae-130">*NomModule*</span><span class="sxs-lookup"><span data-stu-id="b2aae-130">*moduleName*</span></span>   | <span data-ttu-id="b2aae-131">Chemin d’accès complet à la DLL qui implémente le plug-in du magasin en ligne. Exemple : « C : \\ Program Files \\ proseware \\ProsewareService.dll »</span><span class="sxs-lookup"><span data-stu-id="b2aae-131">The fully qualified path to the DLL that implements the online store's plug-in.Example: "C:\\Program Files\\Proseware\\ProsewareService.dll"</span></span><br/>                                                                                                                                                                                                                                                |



 

<span data-ttu-id="b2aae-132">Le tableau suivant décrit les indicateurs de capacité de plug-in.</span><span class="sxs-lookup"><span data-stu-id="b2aae-132">The following table describes the plug-in capability flags.</span></span>



| <span data-ttu-id="b2aae-133">Indicateur</span><span class="sxs-lookup"><span data-stu-id="b2aae-133">Flag</span></span>                                    | <span data-ttu-id="b2aae-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="b2aae-134">Value</span></span> | <span data-ttu-id="b2aae-135">Description</span><span class="sxs-lookup"><span data-stu-id="b2aae-135">Description</span></span>                                                                                                                                                                                                                        |
|-----------------------------------------|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2aae-136">limite d’abonnement \_ \_ ALLOWPLAY</span><span class="sxs-lookup"><span data-stu-id="b2aae-136">SUBSCRIPTION\_CAP\_ALLOWPLAY</span></span>            | <span data-ttu-id="b2aae-137">0X1</span><span class="sxs-lookup"><span data-stu-id="b2aae-137">0X1</span></span>   | <span data-ttu-id="b2aae-138">Le lecteur Windows Media doit appeler [IWMPSubscriptionService :: allowPlay](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay).</span><span class="sxs-lookup"><span data-stu-id="b2aae-138">Windows Media Player should call [IWMPSubscriptionService::allowPlay](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay).</span></span>                                                                                                                      |
| <span data-ttu-id="b2aae-139">limite d’abonnement \_ \_ ALLOWCDBURN</span><span class="sxs-lookup"><span data-stu-id="b2aae-139">SUBSCRIPTION\_CAP\_ALLOWCDBURN</span></span>          | <span data-ttu-id="b2aae-140">0X2</span><span class="sxs-lookup"><span data-stu-id="b2aae-140">0X2</span></span>   | <span data-ttu-id="b2aae-141">Le lecteur Windows Media doit appeler [IWMPSubscriptionService :: allowCDBurn](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowcdburn).</span><span class="sxs-lookup"><span data-stu-id="b2aae-141">Windows Media Player should call [IWMPSubscriptionService::allowCDBurn](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowcdburn).</span></span>                                                                                                                  |
| <span data-ttu-id="b2aae-142">limite d’abonnement \_ \_ ALLOWPDATRANSFER</span><span class="sxs-lookup"><span data-stu-id="b2aae-142">SUBSCRIPTION\_CAP\_ALLOWPDATRANSFER</span></span>     | <span data-ttu-id="b2aae-143">0X4</span><span class="sxs-lookup"><span data-stu-id="b2aae-143">0X4</span></span>   | <span data-ttu-id="b2aae-144">Le lecteur Windows Media doit appeler [IWMPSubscriptionService :: allowPDATransfer](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowpdatransfer).</span><span class="sxs-lookup"><span data-stu-id="b2aae-144">Windows Media Player should call [IWMPSubscriptionService::allowPDATransfer](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowpdatransfer).</span></span>                                                                                                        |
| <span data-ttu-id="b2aae-145">limite d’abonnement \_ \_ BACKGROUNDPROCESSING</span><span class="sxs-lookup"><span data-stu-id="b2aae-145">SUBSCRIPTION\_CAP\_BACKGROUNDPROCESSING</span></span> | <span data-ttu-id="b2aae-146">0X8</span><span class="sxs-lookup"><span data-stu-id="b2aae-146">0X8</span></span>   | <span data-ttu-id="b2aae-147">Le lecteur Windows Media doit appeler [IWMPSubscriptionService :: startBackgroundProcessing](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-startbackgroundprocessing).</span><span class="sxs-lookup"><span data-stu-id="b2aae-147">Windows Media Player should call [IWMPSubscriptionService::startBackgroundProcessing](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-startbackgroundprocessing).</span></span>                                                                                      |
| <span data-ttu-id="b2aae-148">limite d’abonnement \_ \_ DEVICEAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="b2aae-148">SUBSCRIPTION\_CAP\_DEVICEAVAILABLE</span></span>      | <span data-ttu-id="b2aae-149">0X10</span><span class="sxs-lookup"><span data-stu-id="b2aae-149">0X10</span></span>  | <span data-ttu-id="b2aae-150">Le lecteur Windows Media doit appeler [IWMPSubscriptionService2 ::D eviceavailable](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-deviceavailable).</span><span class="sxs-lookup"><span data-stu-id="b2aae-150">Windows Media Player should call [IWMPSubscriptionService2::deviceAvailable](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-deviceavailable).</span></span>                                                                                                        |
| <span data-ttu-id="b2aae-151">limite d’abonnement \_ \_ PREPAREFORSYNC</span><span class="sxs-lookup"><span data-stu-id="b2aae-151">SUBSCRIPTION\_CAP\_PREPAREFORSYNC</span></span>       | <span data-ttu-id="b2aae-152">0X20</span><span class="sxs-lookup"><span data-stu-id="b2aae-152">0X20</span></span>  | <span data-ttu-id="b2aae-153">Le lecteur Windows Media doit appeler [IWMPSubscriptionService2 ::P repareforsync](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-prepareforsync).</span><span class="sxs-lookup"><span data-stu-id="b2aae-153">Windows Media Player should call [IWMPSubscriptionService2::prepareForSync](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-prepareforsync).</span></span>                                                                                                          |
| <span data-ttu-id="b2aae-154">ABONNEMENTs \_ v1 \_</span><span class="sxs-lookup"><span data-stu-id="b2aae-154">SUBSCRIPTION\_V1\_CAPS</span></span>                  | <span data-ttu-id="b2aae-155">0XF</span><span class="sxs-lookup"><span data-stu-id="b2aae-155">0XF</span></span>   | <span data-ttu-id="b2aae-156">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="b2aae-156">Default.</span></span> <span data-ttu-id="b2aae-157">Cette valeur est utilisée si aucun n’est inscrit.</span><span class="sxs-lookup"><span data-stu-id="b2aae-157">This value is used if none is registered.</span></span> <span data-ttu-id="b2aae-158">Cela équivaut à la combinaison de la limite d’abonnement ALLOWPLAY, de l’abonnement Cap ALLOWCDBURN, de la limite d’abonnement \_ \_ \_ ALLOWPDATRANSFER et de la limite d' \_ \_ \_ abonnement \_ \_ BACKGROUNDPROCESSING.</span><span class="sxs-lookup"><span data-stu-id="b2aae-158">This is equivalent to combining SUBSCRIPTION\_CAP\_ALLOWPLAY, SUBSCRIPTION\_CAP\_ALLOWCDBURN, SUBSCRIPTION\_CAP\_ALLOWPDATRANSFER, and SUBSCRIPTION\_CAP\_BACKGROUNDPROCESSING.</span></span> |



 

<span data-ttu-id="b2aae-159">**Entrées de Registre pour le développement et le test**</span><span class="sxs-lookup"><span data-stu-id="b2aae-159">**Registry Entries for Development and Testing**</span></span>

<span data-ttu-id="b2aae-160">Lorsque vous commencez à développer votre boutique en ligne, Microsoft vous propose deux clés : une clé de test et une clé de production.</span><span class="sxs-lookup"><span data-stu-id="b2aae-160">When you begin developing your online store, Microsoft provides you with two keys: a test key and a production key.</span></span> <span data-ttu-id="b2aae-161">Pendant la phase de développement et de test, votre magasin en ligne s’affiche dans le lecteur Windows Media uniquement si votre clé de test ou votre clé de production se trouve dans le registre sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b2aae-161">During the development and testing phase, your online store will appear in Windows Media Player only if your test key or your production key is in the registry on the user's computer.</span></span> <span data-ttu-id="b2aae-162">Pour plus d’informations sur les clés de test et de production, consultez [clés de test et de production pour un magasin de type 2 en ligne](test-and-production-keys-for-a-type-2-online-store.md).</span><span class="sxs-lookup"><span data-stu-id="b2aae-162">For more information about the test and production keys, see [Test and Production Keys for a Type 2 Online Store](test-and-production-keys-for-a-type-2-online-store.md).</span></span>

<span data-ttu-id="b2aae-163">Placez votre clé de test ou de production à l’emplacement suivant dans le registre.</span><span class="sxs-lookup"><span data-stu-id="b2aae-163">Place your test or production key in the following location in the registry.</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Services]
"TestParameter" = "key1;key2;...;keyN"
```



<span data-ttu-id="b2aae-164">Notez que la valeur de l’entrée de Registre TestParameter peut spécifier plusieurs clés de test ou de production.</span><span class="sxs-lookup"><span data-stu-id="b2aae-164">Note that the value of the TestParameter registry entry can specify multiple test or production keys.</span></span> <span data-ttu-id="b2aae-165">Par exemple, supposons que Proseware a une clé de test de « 1234 » et que contoso a une clé de test « 2345 ».</span><span class="sxs-lookup"><span data-stu-id="b2aae-165">For example, suppose that Proseware has a test key of "1234" and Contoso has a test key of "2345".</span></span> <span data-ttu-id="b2aae-166">L’entrée de Registre suivante spécifie que les banques de test pour Proseware et contoso s’affichent dans le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b2aae-166">The following registry entry specifies that the test stores for Proseware and Contoso will appear in Windows Media Player.</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Services]
"TestParameter" = "1234;2345"
```



<span data-ttu-id="b2aae-167">**Entrée de Registre ActiveService**</span><span class="sxs-lookup"><span data-stu-id="b2aae-167">**ActiveService Registry Entry**</span></span>

<span data-ttu-id="b2aae-168">Lorsque l’utilisateur active un magasin en ligne, le lecteur Windows Media écrit des informations dans le Registre qui identifient le magasin en ligne actif.</span><span class="sxs-lookup"><span data-stu-id="b2aae-168">When the user activates an online store, Windows Media Player writes information in the registry that identifies the active online store.</span></span> <span data-ttu-id="b2aae-169">Le lecteur Windows Media place les informations à l’emplacement suivant dans le registre sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b2aae-169">Windows Media Player places the information in the following location in the registry on the user's computer.</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Subscriptions]
"ActiveService"=serviceInfo
```



<span data-ttu-id="b2aae-170">Dans la syntaxe précédente du Registre, *serviceInfo* est un espace réservé pour une chaîne qui contient des informations descriptives sur le magasin en ligne actif.</span><span class="sxs-lookup"><span data-stu-id="b2aae-170">In the preceding registry syntax, *serviceInfo* is a placeholder for a string that contains descriptive information about the active online store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b2aae-171">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b2aae-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2aae-172">**Référence pour les magasins en ligne de type 2**</span><span class="sxs-lookup"><span data-stu-id="b2aae-172">**Reference for Type 2 Online Stores**</span></span>](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 





