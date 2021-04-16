---
description: API d’encodeur
ms.assetid: 3d19152f-17a3-4576-a2a2-5b827d9ca8d1
title: API d’encodeur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 386b964f44dc4dc69896ead34bbe0d0177b198a1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392772"
---
# <a name="encoder-api"></a><span data-ttu-id="56ee5-103">API d’encodeur</span><span class="sxs-lookup"><span data-stu-id="56ee5-103">Encoder API</span></span>

<span data-ttu-id="56ee5-104">L’API d’encodeur fournit une interface uniforme pour la configuration des encodeurs logiciels et matériels.</span><span class="sxs-lookup"><span data-stu-id="56ee5-104">The Encoder API provides a uniform interface for configuring software and hardware encoders.</span></span> <span data-ttu-id="56ee5-105">Les applications peuvent utiliser l’API d’encodeur pour configurer un encodeur et stocker les paramètres de configuration.</span><span class="sxs-lookup"><span data-stu-id="56ee5-105">Applications can use the Encoder API to configure an encoder and to store the configuration settings.</span></span> <span data-ttu-id="56ee5-106">Les fournisseurs d’encodeurs peuvent utiliser l’API d’encodeur pour exposer les fonctionnalités d’un encodeur.</span><span class="sxs-lookup"><span data-stu-id="56ee5-106">Encoder vendors can use the Encoder API to expose the capabilities of an encoder.</span></span> <span data-ttu-id="56ee5-107">Bien que l’API d’encodeur soit principalement conçue pour les encodeurs, il est assez général que les décodeurs puissent également le prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="56ee5-107">Although the Encoder API is designed primarily for encoders, it is general enough that decoders can support it as well.</span></span>

<span data-ttu-id="56ee5-108">L’API d’encodeur est exposée aux applications via l’interface [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) , qui est exposée par le filtre d’encodeur.</span><span class="sxs-lookup"><span data-stu-id="56ee5-108">The Encoder API is exposed to applications through the [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) interface, which is exposed by the encoder filter.</span></span> <span data-ttu-id="56ee5-109">Le filtre d’encodeur peut être un filtre DirectShow natif, un encodeur matériel ou un objet de média DirectX (DMO).</span><span class="sxs-lookup"><span data-stu-id="56ee5-109">The encoder filter may be a native DirectShow filter, a hardware encoder, or a DirectX Media Object (DMO).</span></span>

-   <span data-ttu-id="56ee5-110">Filtres logiciels : un encodeur qui est implémenté en tant que filtre DirectShow natif doit exposer l' [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) directement.</span><span class="sxs-lookup"><span data-stu-id="56ee5-110">Software filters: An encoder that is implemented as a native DirectShow filter should expose the [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) directly.</span></span>
-   <span data-ttu-id="56ee5-111">Encodeurs matériels : l’appareil d’encodage est exposé via un ou plusieurs AVStream minipilotes, qui sont représentés en mode utilisateur par KSProxy.</span><span class="sxs-lookup"><span data-stu-id="56ee5-111">Hardware encoders: The encoding device is exposed through one or more AVStream minidrivers, which are represented in user mode by KSProxy.</span></span> <span data-ttu-id="56ee5-112">KSProxy convertit les appels de méthode [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) en jeux de propriétés KS.</span><span class="sxs-lookup"><span data-stu-id="56ee5-112">KSProxy translates [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) method calls into KS property sets.</span></span> <span data-ttu-id="56ee5-113">Pour plus d’informations, consultez la documentation du DDK.</span><span class="sxs-lookup"><span data-stu-id="56ee5-113">For more information, see the DDK documentation.</span></span>
-   <span data-ttu-id="56ee5-114">DMOs : DMO doit exposer l’interface [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) .</span><span class="sxs-lookup"><span data-stu-id="56ee5-114">DMOs: The DMO should expose the [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) interface.</span></span> <span data-ttu-id="56ee5-115">Les applications DirectShow peuvent interroger le filtre de wrappers DMO, qui expose l’interface en regroupant les DMO.</span><span class="sxs-lookup"><span data-stu-id="56ee5-115">DirectShow applications can query the DMO Wrapper filter, which exposes the interface by aggregating the DMO.</span></span> <span data-ttu-id="56ee5-116">Les applications non basées sur DirectShow peuvent interroger directement le DMO.</span><span class="sxs-lookup"><span data-stu-id="56ee5-116">Applications not based on DirectShow can query the DMO directly.</span></span>

### <a name="encoder-capabilties"></a><span data-ttu-id="56ee5-117">Fonctionnalité encodeur</span><span class="sxs-lookup"><span data-stu-id="56ee5-117">Encoder Capabilties</span></span>

<span data-ttu-id="56ee5-118">Un encodeur peut inscrire une liste de fonctionnalités de haut niveau en les stockant dans le registre système.</span><span class="sxs-lookup"><span data-stu-id="56ee5-118">An encoder can register a list of high-level capabilities by storing them in the system registry.</span></span> <span data-ttu-id="56ee5-119">Chaque fonctionnalité est identifiée par un GUID.</span><span class="sxs-lookup"><span data-stu-id="56ee5-119">Each capability is identified by a GUID.</span></span> <span data-ttu-id="56ee5-120">Pour énumérer les fonctionnalités d’un encodeur particulier, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="56ee5-120">To enumerate the capabilities of a particular encoder, do the following:</span></span>

1.  <span data-ttu-id="56ee5-121">Créez le moniker qui représente le filtre de l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="56ee5-121">Create the moniker that represents the encoder filter.</span></span> <span data-ttu-id="56ee5-122">(Consultez [utilisation de l’énumérateur de périphérique système](using-the-system-device-enumerator.md).)</span><span class="sxs-lookup"><span data-stu-id="56ee5-122">(See [Using the System Device Enumerator](using-the-system-device-enumerator.md).)</span></span>
2.  <span data-ttu-id="56ee5-123">Interrogez le moniker de filtre de l’interface [**IGetCapabilitiesKey**](/windows/desktop/api/Strmif/nn-strmif-igetcapabilitieskey) .</span><span class="sxs-lookup"><span data-stu-id="56ee5-123">Query the filter moniker for the [**IGetCapabilitiesKey**](/windows/desktop/api/Strmif/nn-strmif-igetcapabilitieskey) interface.</span></span>
3.  <span data-ttu-id="56ee5-124">Appelez [**IGetCapabilitiesKey :: GetCapabilitiesKey**](/windows/desktop/api/Strmif/nf-strmif-igetcapabilitieskey-getcapabilitieskey).</span><span class="sxs-lookup"><span data-stu-id="56ee5-124">Call [**IGetCapabilitiesKey::GetCapabilitiesKey**](/windows/desktop/api/Strmif/nf-strmif-igetcapabilitieskey-getcapabilitieskey).</span></span> <span data-ttu-id="56ee5-125">La méthode retourne un handle vers la clé de Registre qui contient la liste des fonctionnalités du filtre.</span><span class="sxs-lookup"><span data-stu-id="56ee5-125">The method returns a handle to the registry key that contains the filter's capabilities list.</span></span>
4.  <span data-ttu-id="56ee5-126">Appelez la fonction **RegEnumValue** pour énumérer les valeurs de la clé retournée.</span><span class="sxs-lookup"><span data-stu-id="56ee5-126">Call the **RegEnumValue** function to enumerate the values for the returned key.</span></span>

<span data-ttu-id="56ee5-127">Si vous devloping un encodeur, créez les entrées de Registre pour les fonctionnalités lorsque le filtre est inscrit.</span><span class="sxs-lookup"><span data-stu-id="56ee5-127">If you are devloping an encoder, create the registry entries for the capabilities when the filter is registered.</span></span> <span data-ttu-id="56ee5-128">Pour les filtres logiciels, créez une clé nommée **fonctionnalités** qui est adjacente aux clés **FilterData** et **FriendlyName** .</span><span class="sxs-lookup"><span data-stu-id="56ee5-128">For software filters, create a key named **Capabilities** that is adjacent to the **FilterData** and **FriendlyName** keys.</span></span> <span data-ttu-id="56ee5-129">En règle générale, vous ajoutez ces informations après avoir appelé [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) pour enregistrer les données de filtre standard.</span><span class="sxs-lookup"><span data-stu-id="56ee5-129">Typically, you would add this information after calling [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) to register the standard filter data.</span></span> <span data-ttu-id="56ee5-130">Pour plus d’informations, consultez [comment inscrire des filtres DirectShow](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="56ee5-130">For more information, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span> <span data-ttu-id="56ee5-131">Vous pouvez également créer une clé **CapabilitiesLocation** qui contient une chaîne indiquant l’emplacement de la clé de **fonctionnalités** dans le registre.</span><span class="sxs-lookup"><span data-stu-id="56ee5-131">Alternatively, you can create a **CapabilitiesLocation** key that contains a string giving the location of the **Capabilities** key in the registry.</span></span> <span data-ttu-id="56ee5-132">La chaîne doit commencer par « HKLM \\ », « HKCR \\ » ou « HKCU \\ » pour indiquer la sous-arborescence du Registre.</span><span class="sxs-lookup"><span data-stu-id="56ee5-132">The string should start with "HKLM\\", "HKCR\\", or "HKCU\\" to indicate the registry subtree.</span></span> <span data-ttu-id="56ee5-133">Pour les appareils Plug-and-Play, les fichiers d’installation du pilote doivent créer une clé de **fonctionnalités** adjacente à la clé **FriendlyName** du filtre, ou utiliser une clé **CapabilitiesLocation** comme décrit pour les filtres logiciels.</span><span class="sxs-lookup"><span data-stu-id="56ee5-133">For Plug and Play devices, the driver's setup files should create a **Capabilities** key adjacent to the filter's **FriendlyName** key, or it can use a **CapabilitiesLocation** key as described for software filters.</span></span>

<span data-ttu-id="56ee5-134">Une fois que vous avez créé la clé de **fonctionnalités** , créez une valeur pour chaque GUID de fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="56ee5-134">Once you have created the **Capabilities** key, create a value for each capability GUID.</span></span> <span data-ttu-id="56ee5-135">Le nom de la valeur doit être la forme de chaîne du GUID, sous la forme `{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}` .</span><span class="sxs-lookup"><span data-stu-id="56ee5-135">The name of the value should be the string form of the GUID, in the form `{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}`.</span></span> <span data-ttu-id="56ee5-136">Chaque type de valeur doit être l’un des suivants :</span><span class="sxs-lookup"><span data-stu-id="56ee5-136">Each value type should be one of the following:</span></span>

-   <span data-ttu-id="56ee5-137">Valeur numérique unique.</span><span class="sxs-lookup"><span data-stu-id="56ee5-137">Single numerical value.</span></span> <span data-ttu-id="56ee5-138">Utilisez une valeur **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="56ee5-138">Use a **DWORD** value.</span></span>
-   <span data-ttu-id="56ee5-139">GUID (identificateur global unique).</span><span class="sxs-lookup"><span data-stu-id="56ee5-139">GUID.</span></span> <span data-ttu-id="56ee5-140">Utilisez la forme de chaîne du GUID.</span><span class="sxs-lookup"><span data-stu-id="56ee5-140">Use the string form of the GUID.</span></span>
-   <span data-ttu-id="56ee5-141">Paires numériques.</span><span class="sxs-lookup"><span data-stu-id="56ee5-141">Numeric pairs.</span></span> <span data-ttu-id="56ee5-142">Utilisez une chaîne sous la forme « a, b » pour représenter des paires de valeurs, telles que la largeur et la hauteur, ou le numérateur et le dénominateur pour les fractions.</span><span class="sxs-lookup"><span data-stu-id="56ee5-142">Use a string with the form "a,b" to represent pairs of values, such as width and height, or numerator and denominator for fractions.</span></span>
-   <span data-ttu-id="56ee5-143">Tableaux de valeurs.</span><span class="sxs-lookup"><span data-stu-id="56ee5-143">Arrays of values.</span></span> <span data-ttu-id="56ee5-144">Utilisez des chaînes multiples (**reg \_ SZ \_ multi**) pour représenter plusieurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="56ee5-144">Use multi-strings (**REG\_SZ\_MULTI**) to represent more than one value.</span></span>

<span data-ttu-id="56ee5-145">L’exemple suivant illustre la disposition du Registre pour un filtre logiciel :</span><span class="sxs-lookup"><span data-stu-id="56ee5-145">The following example shows the registry layout for a software filter:</span></span>


```C++
\HKCR\CLSID\Filter Category\Instance\Filter CLSID\Capabilities\
    
Values: 
    
    guid1: 1234 (REG_DWORD)   
    
    guid2: "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}" (REG_SZ)
    
    guid3: "2","4","6" (REG_SZ_MULTI)
    
    guid4: "720,480" (REG_SZ) 
```



### <a name="encoder-profiles"></a><span data-ttu-id="56ee5-146">Profils d’encodeur</span><span class="sxs-lookup"><span data-stu-id="56ee5-146">Encoder Profiles</span></span>

<span data-ttu-id="56ee5-147">Un *profil d’encodeur* est une liste fixe de paramètres de configuration qui peuvent être appliqués à un encodeur au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="56ee5-147">An *encoder profile* is a fixed list of configuration settings that can be applied to an encoder at run time.</span></span> <span data-ttu-id="56ee5-148">Les profils sont indépendants de l’encodeur ; une application peut sélectionner un encodeur, puis sélectionner un profil et appliquer les paramètres de profil à l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="56ee5-148">Profiles are independent of the encoder; an application can select an encoder, then select a profile and apply the profile settings to the encoder.</span></span> <span data-ttu-id="56ee5-149">Les profils sont identifiés par un GUID et doivent être stockés à l’emplacement suivant dans le registre :</span><span class="sxs-lookup"><span data-stu-id="56ee5-149">Profiles are identified by GUID and should be stored in the following location in the registry:</span></span>


```C++
\HKLM\Software\Microsoft\EncoderProfiles\Profile GUID\
```



<span data-ttu-id="56ee5-150">*GUID du profil* de l’emplacement</span><span class="sxs-lookup"><span data-stu-id="56ee5-150">where *Profile GUID*</span></span>

<span data-ttu-id="56ee5-151">forme de chaîne du GUID qui identifie le profil.</span><span class="sxs-lookup"><span data-stu-id="56ee5-151">is the string form of the GUID that identifies the profile.</span></span> <span data-ttu-id="56ee5-152">Créez des valeurs pour chaque paramètre.</span><span class="sxs-lookup"><span data-stu-id="56ee5-152">Create values for each setting.</span></span> <span data-ttu-id="56ee5-153">Créez également une valeur de chaîne nommée « FriendlyName » dont les données identifient le profil (par exemple, « LowBandwidthVideo »).</span><span class="sxs-lookup"><span data-stu-id="56ee5-153">Also create a string value named "FriendlyName" whose data identifies the profile (such as "LowBandwidthVideo").</span></span>

## <a name="related-topics"></a><span data-ttu-id="56ee5-154">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="56ee5-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56ee5-155">Développement d’encodeur et de décodeur</span><span class="sxs-lookup"><span data-stu-id="56ee5-155">Encoder and Decoder Development</span></span>](encoder-and-decoder-development.md)
</dt> </dl>

 

 



