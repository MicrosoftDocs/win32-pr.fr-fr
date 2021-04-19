---
description: Les services linguistiques étendus (ELS) sont implémentés sous la forme d’une bibliothèque de liens dynamiques (DLL) qui fournit diverses fonctionnalités de prise en charge linguistique pour le texte que l’application spécifie.
ms.assetid: 23d4e42a-a5bb-467c-a8b9-6a57ae39daa0
title: À propos des services linguistiques étendus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a6594fcfe67954a56cb09e239221b2b529d4d01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541844"
---
# <a name="about-extended-linguistic-services"></a><span data-ttu-id="1be29-103">À propos des services linguistiques étendus</span><span class="sxs-lookup"><span data-stu-id="1be29-103">About Extended Linguistic Services</span></span>

<span data-ttu-id="1be29-104">Les services linguistiques étendus (ELS) sont implémentés sous la forme d’une bibliothèque de liens dynamiques (DLL) qui fournit diverses fonctionnalités de prise en charge linguistique pour le texte que l’application spécifie.</span><span class="sxs-lookup"><span data-stu-id="1be29-104">Extended Linguistic Services (ELS) is implemented as a dynamic-link library (DLL) that provides a variety of linguistic support functionality for text that the application specifies.</span></span> <span data-ttu-id="1be29-105">La technologie comprend la plateforme et les plug-ins ELS pour plusieurs types de service linguistiques prédéfinis accessibles à l’application via la plateforme.</span><span class="sxs-lookup"><span data-stu-id="1be29-105">The technology includes the ELS platform and plug-ins for several predefined linguistic service types accessible to the application through the platform.</span></span>

> [!Note]  
> <span data-ttu-id="1be29-106">Le module ELS est installé automatiquement avec Windows 7 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="1be29-106">The ELS module is installed automatically with Windows 7 and later.</span></span>

 

## <a name="els-platform"></a><span data-ttu-id="1be29-107">Plateforme ELS</span><span class="sxs-lookup"><span data-stu-id="1be29-107">ELS Platform</span></span>

<span data-ttu-id="1be29-108">La plateforme ELS est l’interface entre votre application et les services ELS.</span><span class="sxs-lookup"><span data-stu-id="1be29-108">The ELS platform is the interface between your application and the ELS services.</span></span> <span data-ttu-id="1be29-109">Il offre un moyen simple d’implémenter plusieurs types de fonctionnalités linguistiques via la même API, ce qui permet à l’application d’accéder à des services spécifiques et de les utiliser.</span><span class="sxs-lookup"><span data-stu-id="1be29-109">It provides a simple way to implement several kinds of linguistic functionality through the same API, which allows the application to access and use specific services.</span></span> <span data-ttu-id="1be29-110">Pour plus d’informations sur l’API, consultez [référence des services linguistiques étendus.](extended-linguistic-services-reference.md)</span><span class="sxs-lookup"><span data-stu-id="1be29-110">For more information about the API, see [Extended Linguistic Services Reference.](extended-linguistic-services-reference.md)</span></span>

> [!Note]  
> <span data-ttu-id="1be29-111">Lorsque l’application appelle l’une des fonctions de l’API ELS, la plateforme alloue la mémoire et les ressources nécessaires pour la communication avec les services.</span><span class="sxs-lookup"><span data-stu-id="1be29-111">When the application calls any of the ELS API functions, the platform allocates memory and resources as needed for communication with the services.</span></span> <span data-ttu-id="1be29-112">L’application est responsable de l’appel de la plateforme pour libérer ces ressources.</span><span class="sxs-lookup"><span data-stu-id="1be29-112">The application is responsible for calling the platform again to free these resources.</span></span>

 

<span data-ttu-id="1be29-113">La plateforme s’exécute dans l’espace mémoire virtuelle de l’application, et toute la mémoire allouée fait partie de cet espace.</span><span class="sxs-lookup"><span data-stu-id="1be29-113">The platform runs inside the application virtual memory space, and all allocated memory is part of this space.</span></span> <span data-ttu-id="1be29-114">Par conséquent, votre application doit uniquement être liée à la DLL du composant ELS (Elscore.dll) en établissant une liaison à Elscore. lib ou en chargeant dynamiquement Elscore.dll.</span><span class="sxs-lookup"><span data-stu-id="1be29-114">Thus your application only needs to link to the ELS component DLL (Elscore.dll) by linking to Elscore.lib or by dynamically loading Elscore.dll.</span></span>

## <a name="els-services"></a><span data-ttu-id="1be29-115">Services ELS</span><span class="sxs-lookup"><span data-stu-id="1be29-115">ELS Services</span></span>

<span data-ttu-id="1be29-116">Pour Windows 7 et versions ultérieures, la plateforme ELS prend en charge uniquement les services prédéfinis suivants.</span><span class="sxs-lookup"><span data-stu-id="1be29-116">For Windows 7 and later, the ELS platform supports only the following predefined services.</span></span>

-   [<span data-ttu-id="1be29-117">Détection de langue Microsoft</span><span class="sxs-lookup"><span data-stu-id="1be29-117">Microsoft Language Detection</span></span>](microsoft-language-detection.md)
-   [<span data-ttu-id="1be29-118">Détection de scripts Microsoft</span><span class="sxs-lookup"><span data-stu-id="1be29-118">Microsoft Script Detection</span></span>](microsoft-script-detection.md)
-   [<span data-ttu-id="1be29-119">Services de translittération</span><span class="sxs-lookup"><span data-stu-id="1be29-119">Transliteration services</span></span>](transliteration-services.md)

> [!Note]  
> <span data-ttu-id="1be29-120">Les futures versions d’ELS prendront en charge des services supplémentaires fournis par Microsoft ou des fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="1be29-120">Future versions of ELS will support additional services provided by Microsoft or service providers.</span></span>

 

<span data-ttu-id="1be29-121">Chaque service est associé à une catégorie de service décrivant ce que fait le service.</span><span class="sxs-lookup"><span data-stu-id="1be29-121">Each service is associated with a service category describing what the service does.</span></span> <span data-ttu-id="1be29-122">La catégorie est représentée par une chaîne non localisable.</span><span class="sxs-lookup"><span data-stu-id="1be29-122">The category is represented by a nonlocalizable string.</span></span> <span data-ttu-id="1be29-123">Elle est utilisée par les applications pour énumérer les services disponibles.</span><span class="sxs-lookup"><span data-stu-id="1be29-123">It is used by applications to enumerate available services.</span></span> <span data-ttu-id="1be29-124">Les catégories de service actuelles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="1be29-124">The current service categories are:</span></span>

-   <span data-ttu-id="1be29-125">« Détection de langue »</span><span class="sxs-lookup"><span data-stu-id="1be29-125">"Language Detection"</span></span>
-   <span data-ttu-id="1be29-126">« Détection de script »</span><span class="sxs-lookup"><span data-stu-id="1be29-126">"Script Detection"</span></span>
-   <span data-ttu-id="1be29-127">Translittér</span><span class="sxs-lookup"><span data-stu-id="1be29-127">"Transliteration"</span></span>

<span data-ttu-id="1be29-128">La plateforme utilise des métadonnées de service pour énumérer les services demandés par l’application.</span><span class="sxs-lookup"><span data-stu-id="1be29-128">The platform uses service metadata to enumerate the services requested by the application.</span></span> <span data-ttu-id="1be29-129">Les propriétés telles que l’identificateur global unique (GUID) du service, les langues et les scripts d’entrée et de sortie pris en charge et la catégorie de service peuvent être utilisées par l’application pour énumérer les services ELS souhaités.</span><span class="sxs-lookup"><span data-stu-id="1be29-129">Properties such as the service globally unique identifier (GUID), supported input and output languages and scripts, and the service category can be used by the application to enumerate the desired ELS services.</span></span>

<span data-ttu-id="1be29-130">Chaque service ELS est implémenté en tant que plug-in pris en charge par une DLL qui peut être installée sur le système d’exploitation afin que la plateforme ELS puisse le détecter et l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="1be29-130">Each ELS service is implemented as a plug-in supported by a DLL that can be installed on the operating system so that the ELS platform can detect and use it.</span></span> <span data-ttu-id="1be29-131">Les services peuvent exposer leurs propres sous-services, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="1be29-131">Services can expose their own subservices, if required.</span></span>

## <a name="main-els-operations"></a><span data-ttu-id="1be29-132">Opérations ELS principales</span><span class="sxs-lookup"><span data-stu-id="1be29-132">Main ELS Operations</span></span>

<span data-ttu-id="1be29-133">Cette section décrit les principales opérations prises en charge par la plateforme ELS.</span><span class="sxs-lookup"><span data-stu-id="1be29-133">This section describes the main operations supported by the ELS platform.</span></span> <span data-ttu-id="1be29-134">La plateforme prend en charge les modes d’appel synchrones et asynchrones.</span><span class="sxs-lookup"><span data-stu-id="1be29-134">The platform supports both synchronous and asynchronous calling modes.</span></span> <span data-ttu-id="1be29-135">Le mode d’appel asynchrone utilise un pool de threads d’application pour planifier les threads de traitement des demandes.</span><span class="sxs-lookup"><span data-stu-id="1be29-135">The asynchronous calling mode uses an application thread pool to schedule threads for processing requests.</span></span>

> [!Note]  
> <span data-ttu-id="1be29-136">Étant donné que la plateforme prend en charge un mode asynchrone, les services ELS n’ont pas à implémenter ce type de fonctionnalité de manière autonome.</span><span class="sxs-lookup"><span data-stu-id="1be29-136">Since the platform supports an asynchronous mode, ELS services do not have to implement this type of functionality on their own.</span></span>

 

### <a name="service-enumeration"></a><span data-ttu-id="1be29-137">Énumération de service</span><span class="sxs-lookup"><span data-stu-id="1be29-137">Service Enumeration</span></span>

<span data-ttu-id="1be29-138">La plateforme ELS charge et gère tous les services ELS, ce qui rend l’opération transparente pour l’application.</span><span class="sxs-lookup"><span data-stu-id="1be29-138">The ELS platform loads and manages all ELS services, making operation transparent to the application.</span></span> <span data-ttu-id="1be29-139">L’application énumère les services disponibles en appelant [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices).</span><span class="sxs-lookup"><span data-stu-id="1be29-139">The application enumerates the available services by calling [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices).</span></span> <span data-ttu-id="1be29-140">Pour obtenir des instructions de programmation, consultez [énumération et libération de services](enumerating-and-freeing-services.md).</span><span class="sxs-lookup"><span data-stu-id="1be29-140">For programming instructions, see [Enumerating and Freeing Services](enumerating-and-freeing-services.md).</span></span>

> [!Note]  
> <span data-ttu-id="1be29-141">Pour des raisons de performances, il est recommandé de faire en sorte que votre application n’énumère les services disponibles qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="1be29-141">It is advisable for performance reasons to have your application enumerate the available services only once.</span></span> <span data-ttu-id="1be29-142">La plateforme ELS vérifie à nouveau les services sur l’énumération suivante pour s’assurer que les résultats de leur énumération sont toujours à jour.</span><span class="sxs-lookup"><span data-stu-id="1be29-142">The ELS platform checks the services again on the next enumeration to ensure that its enumeration results are always current.</span></span>

 

### <a name="text-recognition"></a><span data-ttu-id="1be29-143">Reconnaissance de texte</span><span class="sxs-lookup"><span data-stu-id="1be29-143">Text Recognition</span></span>

<span data-ttu-id="1be29-144">Après l’énumération de service, l’application appelle la fonction [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) pour utiliser un service Els particulier afin de mapper une plage de texte de texte d’entrée au texte de sortie.</span><span class="sxs-lookup"><span data-stu-id="1be29-144">After service enumeration, the application calls the [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) function to use a particular ELS service to map any text range of input text to output text.</span></span> <span data-ttu-id="1be29-145">Un exemple de reconnaissance de texte est l’utilisation d’un service de détection de langage qui reçoit un segment de texte et détecte son langage le plus probable.</span><span class="sxs-lookup"><span data-stu-id="1be29-145">An example of text recognition is the use of a language detection service that receives a text segment and detects its most probable language.</span></span>

<span data-ttu-id="1be29-146">Une fois que le service a reconnu le texte, [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) retourne avec une structure de [**\_ \_ jeu**](/windows/desktop/api/Elscore/ns-elscore-mapping_property_bag) de propriétés de mappage remplie avec les données de sortie et les propriétés produites par le service.</span><span class="sxs-lookup"><span data-stu-id="1be29-146">After the service has recognized the text, [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) returns with a [**MAPPING\_PROPERTY\_BAG**](/windows/desktop/api/Elscore/ns-elscore-mapping_property_bag) structure populated with output data and properties produced by the service.</span></span> <span data-ttu-id="1be29-147">Pour éviter les fuites de mémoire, l’application doit libérer le conteneur de propriétés en appelant [**MappingFreePropertyBag**](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag) pour chaque fois que le [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1be29-147">To avoid memory leaks, the application must free the property bag by calling [**MappingFreePropertyBag**](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag) for each time that the [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) returns S\_OK.</span></span> <span data-ttu-id="1be29-148">En règle générale, l’application effectue cette opération lorsqu’elle a terminé d’utiliser les données de sortie ou lorsque les données de sortie ne sont plus pertinentes, car la région d’entrée du texte a été modifiée, par exemple, modifiée ou supprimée.</span><span class="sxs-lookup"><span data-stu-id="1be29-148">Usually the application does this either when it finishes using the output data or when the output data is no longer relevant because the input region of text has been modified, for example, edited or deleted.</span></span> <span data-ttu-id="1be29-149">Lorsque le jeu de propriétés est relâché, **MappingFreePropertyBag** retourne.</span><span class="sxs-lookup"><span data-stu-id="1be29-149">When the property bag is released, **MappingFreePropertyBag** returns.</span></span>

<span data-ttu-id="1be29-150">Des instructions de programmation pour la reconnaissance de texte sont fournies dans [demande de reconnaissance de texte](requesting-text-recognition.md).</span><span class="sxs-lookup"><span data-stu-id="1be29-150">Programming instructions for text recognition are provided in [Requesting Text Recognition](requesting-text-recognition.md).</span></span>

### <a name="service-termination"></a><span data-ttu-id="1be29-151">Arrêt du service</span><span class="sxs-lookup"><span data-stu-id="1be29-151">Service Termination</span></span>

<span data-ttu-id="1be29-152">Lorsque votre application n’a plus besoin de services ELS, elle appelle [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) avant qu’elle ne se termine.</span><span class="sxs-lookup"><span data-stu-id="1be29-152">When your application no longer requires ELS services, it calls [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) before it terminates.</span></span> <span data-ttu-id="1be29-153">Pour plus d’informations, consultez [énumération et libération de services](enumerating-and-freeing-services.md).</span><span class="sxs-lookup"><span data-stu-id="1be29-153">For more information, see [Enumerating and Freeing Services](enumerating-and-freeing-services.md).</span></span>

### <a name="versioning"></a><span data-ttu-id="1be29-154">Contrôle de version</span><span class="sxs-lookup"><span data-stu-id="1be29-154">Versioning</span></span>

<span data-ttu-id="1be29-155">Les futures versions d’ELS autorisent la mise à jour des services ELS.</span><span class="sxs-lookup"><span data-stu-id="1be29-155">Future versions of ELS will allow the ELS services to be updated.</span></span> <span data-ttu-id="1be29-156">L’application sera en mesure de vérifier les numéros de version de la structure d' [**\_ \_ informations de service de mappage**](/windows/desktop/api/Elscore/ns-elscore-mapping_service_info) pour détecter les modifications apportées aux services.</span><span class="sxs-lookup"><span data-stu-id="1be29-156">The application will be able to check the version numbers of the [**MAPPING\_SERVICE\_INFO**](/windows/desktop/api/Elscore/ns-elscore-mapping_service_info) structure to detect any changes in the services.</span></span>

> [!Note]  
> <span data-ttu-id="1be29-157">Votre application ELS ne doit pas supposer que les différentes versions du même service peuvent récupérer exactement les mêmes résultats.</span><span class="sxs-lookup"><span data-stu-id="1be29-157">Your ELS application should not make the assumption that different versions of the same service can retrieve exactly the same results.</span></span>

 

 

 



