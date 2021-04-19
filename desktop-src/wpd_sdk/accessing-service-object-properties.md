---
description: Accès aux propriétés de l’objet de service
ms.assetid: 66d9802b-ad28-47a4-8151-9df7aff07d61
title: Accès aux propriétés de l’objet de service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 028ffc178f29f21aa60295b137b48c0fa2357a28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515638"
---
# <a name="accessing-service-object-properties"></a><span data-ttu-id="31af2-103">Accès aux propriétés de l’objet de service</span><span class="sxs-lookup"><span data-stu-id="31af2-103">Accessing Service Object Properties</span></span>

<span data-ttu-id="31af2-104">Une application peut lire et écrire des propriétés pour un objet unique sur un service, pour plusieurs objets identifiés par des identificateurs d’objets, ou pour plusieurs objets du même type.</span><span class="sxs-lookup"><span data-stu-id="31af2-104">An application can read and write properties for a single object on a service, for multiple objects identified by object identifiers, or for multiple objects of the same type.</span></span> <span data-ttu-id="31af2-105">La rubrique [récupération des propriétés](retrieving-content-object-properties.md) de l’objet décrit la lecture des propriétés d’un seul objet sur un service.</span><span class="sxs-lookup"><span data-stu-id="31af2-105">The [Retrieving Object Properties](retrieving-content-object-properties.md) topic describes reading properties for a single object on a service.</span></span> <span data-ttu-id="31af2-106">La rubrique relative à l' [écriture des propriétés](writing-content-object-properties.md) de l’objet décrit l’écriture des propriétés d’un objet unique sur un service.</span><span class="sxs-lookup"><span data-stu-id="31af2-106">The [Writing Object Properties](writing-content-object-properties.md) topic describes writing properties for a single object on a service.</span></span>

<span data-ttu-id="31af2-107">Reportez-vous à la section [tâches avancées](advanced-tasks.md) pour obtenir une description de la récupération de propriétés pour plusieurs objets.</span><span class="sxs-lookup"><span data-stu-id="31af2-107">Refer to the [Advanced Tasks](advanced-tasks.md) section for a description of property retrieval for multiple objects.</span></span>

## <a name="when-to-use-service-property-definitions"></a><span data-ttu-id="31af2-108">Quand utiliser les définitions de propriété de service</span><span class="sxs-lookup"><span data-stu-id="31af2-108">When to use Service Property Definitions</span></span>

<span data-ttu-id="31af2-109">Les appels de l’API WPD utilisés pour la récupération et la définition des propriétés d’un service sont les mêmes que ceux des appels pour la récupération des propriétés d’un appareil (par exemple, « récupération des propriétés d’un objet unique »).</span><span class="sxs-lookup"><span data-stu-id="31af2-109">The WPD API calls used for retrieving and setting object properties for a service are the same as the calls for retrieving object properties for a device (compare "Retrieving Properties for a Single Object" for an example).</span></span> <span data-ttu-id="31af2-110">La principale différence réside dans le fait qu’un autre jeu d’PROPERTYKEYs est utilisé pour interroger les propriétés de l’objet.</span><span class="sxs-lookup"><span data-stu-id="31af2-110">The key difference is that a different set of PROPERTYKEYs are used to query object properties.</span></span> <span data-ttu-id="31af2-111">Pour WpdServiceApiSample, le service de l’appareil PROPERTYKEYs est utilisé (par exemple, le **\_ \_ nom** du type d’GenericObj); pour le WpdApiSample, les PropertyKeys PropertyKeys sont utilisées (telles que le nom de l' **\_ \_ objet wpd**).</span><span class="sxs-lookup"><span data-stu-id="31af2-111">For the WpdServiceApiSample, device service PROPERTYKEYs are used (such as **PKEY\_GenericObj\_Name**); for the WpdApiSample, WPD PROPERTYKEYs are used (such as **WPD\_OBJECT\_NAME**).</span></span>

<span data-ttu-id="31af2-112">Le service d’appareil PROPERTYKEYs est défini dans BridgeDeviceServices. h (inclus par chaque fichier d’en-tête de service) et représente l’ensemble commun de PROPERTYKEYS employés par les applications de services d’appareils et l’implémentation du microprogramme sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="31af2-112">Device service PROPERTYKEYs are defined in BridgeDeviceServices.h (included by each service header file), and represent the common set of PROPERTYKEYS employed by both device services applications and the firmware implementation on the device.</span></span> <span data-ttu-id="31af2-113">Cela permet un ensemble cohérent de définitions dans la pile d’appareils avec une traduction minimale, des groupes PROPERTYKEYs basés sur le service et permet de définir de nouveaux services plus facilement sans avoir à mettre à jour le schéma WPD.</span><span class="sxs-lookup"><span data-stu-id="31af2-113">This allows a consistent set of definitions throughout the device stack with minimal translation, groups PROPERTYKEYs based on the service, and enables new services to be more easily defined without having to update the WPD schema.</span></span>

<span data-ttu-id="31af2-114">L’ensemble des PROPERTYKEYs utilisés dépend des besoins de votre application :</span><span class="sxs-lookup"><span data-stu-id="31af2-114">The set of PROPERTYKEYs used will depend on your application's needs:</span></span>

-   <span data-ttu-id="31af2-115">Si votre application communique avec l’appareil en appelant [**IPortableDevice :: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open), utilisez la fonction PROPERTYKEYs définie dans PortableDevice. h.</span><span class="sxs-lookup"><span data-stu-id="31af2-115">If your application is communicating with the device by calling [**IPortableDevice::Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open), use the PROPERTYKEYs defined in PortableDevice.h.</span></span> <span data-ttu-id="31af2-116">WpdApiSample est un exemple d’une telle application.</span><span class="sxs-lookup"><span data-stu-id="31af2-116">An example of such an application is the WpdApiSample.</span></span>
-   <span data-ttu-id="31af2-117">Si votre application communique avec les services d’appareil en appelant [**IPortableDeviceService :: Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open), utilisez la fonction PROPERTYKEYS définie dans BridgeDeviceServices. h.</span><span class="sxs-lookup"><span data-stu-id="31af2-117">If your application is communicating with device services by calling [**IPortableDeviceService::Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open), use the PROPERTYKEYS defined in BridgeDeviceServices.h.</span></span> <span data-ttu-id="31af2-118">WpdServicesApiSample est un exemple d’une telle application.</span><span class="sxs-lookup"><span data-stu-id="31af2-118">An example of such an application is the WpdServicesApiSample.</span></span>
-   <span data-ttu-id="31af2-119">Si vous écrivez une application complexe qui doit prendre en charge un hybride des services d’appareils et de l’appareil (cela signifie que votre application appelle à la fois **IPortableDevice :: Open** et **IPortableDeviceService :: Open**), vous devez utiliser l’interface wpd PropertyKeys quand vous utilisez IPortableDevice et ses interfaces dérivées, et le service d’appareil PropertyKeys quand vous utilisez [IPortableDeviceService](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) et ses interfaces dérivées.</span><span class="sxs-lookup"><span data-stu-id="31af2-119">If you are writing a complex application that needs to support a hybrid of both device services and the device (this means your application calls both **IPortableDevice::Open** and **IPortableDeviceService::Open**), you will need to use the WPD PROPERTYKEYs when using IPortableDevice and its derived interfaces, and device service PROPERTYKEYs when using [IPortableDeviceService](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) and its derived interfaces.</span></span>

<span data-ttu-id="31af2-120">La plupart des applications WPD doivent appartenir à la première ou à la deuxième catégorie.</span><span class="sxs-lookup"><span data-stu-id="31af2-120">Most WPD applications should fall into the first or second category.</span></span>

## <a name="related-topics"></a><span data-ttu-id="31af2-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="31af2-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31af2-122">**IPortableDeviceContent2**</span><span class="sxs-lookup"><span data-stu-id="31af2-122">**IPortableDeviceContent2**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)
</dt> <dt>

[<span data-ttu-id="31af2-123">**IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="31af2-123">**IPortableDeviceProperties**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="31af2-124">Récupération des propriétés de l’objet</span><span class="sxs-lookup"><span data-stu-id="31af2-124">Retrieving Object Properties</span></span>](retrieving-content-object-properties.md)
</dt> <dt>

[<span data-ttu-id="31af2-125">Écriture de propriétés d’objet</span><span class="sxs-lookup"><span data-stu-id="31af2-125">Writing Object Properties</span></span>](writing-content-object-properties.md)
</dt> <dt>

[<span data-ttu-id="31af2-126">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="31af2-126">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



