---
description: Récupération des méthodes de service prises en charge
ms.assetid: 783a6552-9b22-4af4-9252-b443e2624687
title: Récupération des méthodes de service prises en charge
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6029af655a8835a4eee887d919c534856062ff13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866502"
---
# <a name="retrieving-supported-service-methods"></a><span data-ttu-id="a6e2c-103">Récupération des méthodes de service prises en charge</span><span class="sxs-lookup"><span data-stu-id="a6e2c-103">Retrieving Supported Service Methods</span></span>

<span data-ttu-id="a6e2c-104">Les méthodes de service encapsulent les fonctionnalités que chaque service définit et implémente.</span><span class="sxs-lookup"><span data-stu-id="a6e2c-104">Service methods encapsulate functionality that each service defines and implements.</span></span> <span data-ttu-id="a6e2c-105">Elles sont spécifiques à chaque type de service et sont représentées par un GUID unique.</span><span class="sxs-lookup"><span data-stu-id="a6e2c-105">They are specific to each type of service type and are represented by a unique GUID.</span></span>

<span data-ttu-id="a6e2c-106">Par exemple, le service contacts définit une méthode **BeginSync** que les applications appellent pour préparer l’appareil à la synchronisation des objets contact, et une méthode **EndSync** pour informer l’appareil que la synchronisation est terminée.</span><span class="sxs-lookup"><span data-stu-id="a6e2c-106">For example, the Contacts service defines a **BeginSync** method that applications call to prepare the device for synchronizing Contact objects, and an **EndSync** method to notify the device that synchronization has completed.</span></span>

<span data-ttu-id="a6e2c-107">Les applications peuvent interroger par programme les méthodes prises en charge et accéder à ces méthodes et à leurs attributs à l’aide de l’interface [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) .</span><span class="sxs-lookup"><span data-stu-id="a6e2c-107">Applications can programmatically query the supported methods and access these methods and their attributes by using the [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) interface.</span></span>

<span data-ttu-id="a6e2c-108">Les méthodes de service ne doivent pas être confondues avec les commandes WPD.</span><span class="sxs-lookup"><span data-stu-id="a6e2c-108">Service methods should not be confused with WPD commands.</span></span> <span data-ttu-id="a6e2c-109">Les commandes WPD font partie de l’interface de pilote de périphérique WPD standard (DDI) et constituent le mécanisme de communication entre une application WPD et le pilote.</span><span class="sxs-lookup"><span data-stu-id="a6e2c-109">WPD commands are part of the standard WPD Device Driver Interface (DDI), and are the mechanism for communication between a WPD application and the driver.</span></span> <span data-ttu-id="a6e2c-110">Les commandes sont prédéfinies, regroupées par catégories, par exemple \_ , \_ la catégorie wpd commun et sont représentées par une structure PROPERTYKEY.</span><span class="sxs-lookup"><span data-stu-id="a6e2c-110">Commands are predefined, grouped by categories, for example, WPD\_CATEGORY\_COMMON, and are represented by a PROPERTYKEY structure.</span></span> <span data-ttu-id="a6e2c-111">Pour plus d’informations, consultez la rubrique [**commandes**](commands.md) .</span><span class="sxs-lookup"><span data-stu-id="a6e2c-111">For more information, see the [**Commands**](commands.md) topic.</span></span>

<span data-ttu-id="a6e2c-112">L’application WpdServicesApiSample comprend du code qui montre comment une application peut récupérer les méthodes prises en charge par un service de contacts donné en utilisant les interfaces du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="a6e2c-112">The WpdServicesApiSample application includes code that demonstrates how an application can retrieve the methods supported by a given Contacts service by using the interfaces in the following table.</span></span>



|                                                                                      |                                                                                                                |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6e2c-113">Interface</span><span class="sxs-lookup"><span data-stu-id="a6e2c-113">Interface</span></span>                                                                            | <span data-ttu-id="a6e2c-114">Description</span><span class="sxs-lookup"><span data-stu-id="a6e2c-114">Description</span></span>                                                                                                    |
| [<span data-ttu-id="a6e2c-115">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="a6e2c-115">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                             | <span data-ttu-id="a6e2c-116">Utilisé pour récupérer l’interface **IPortableDeviceServiceCapabilities** pour accéder aux méthodes de service prises en charge.</span><span class="sxs-lookup"><span data-stu-id="a6e2c-116">Used to retrieve the **IPortableDeviceServiceCapabilities** interface to access the supported service methods.</span></span> |
| [<span data-ttu-id="a6e2c-117">**IPortableDeviceServiceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="a6e2c-117">**IPortableDeviceServiceCapabilities**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)     | <span data-ttu-id="a6e2c-118">Fournit l’accès aux méthodes prises en charge, aux attributs de méthode et aux paramètres de méthode.</span><span class="sxs-lookup"><span data-stu-id="a6e2c-118">Provides access to the supported methods, method attributes and method parameters.</span></span>                             |
| [<span data-ttu-id="a6e2c-119">**IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="a6e2c-119">**IPortableDevicePropVariantCollection**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="a6e2c-120">Contient la liste des méthodes prises en charge.</span><span class="sxs-lookup"><span data-stu-id="a6e2c-120">Contains the list of supported methods.</span></span>                                                                        |
| [<span data-ttu-id="a6e2c-121">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="a6e2c-121">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)                               | <span data-ttu-id="a6e2c-122">Contient les attributs pour une méthode et pour les paramètres d’une méthode donnée.</span><span class="sxs-lookup"><span data-stu-id="a6e2c-122">Contains the attributes for a method and for a given method's parameters.</span></span>                                      |
| [<span data-ttu-id="a6e2c-123">**IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="a6e2c-123">**IPortableDeviceKeyCollection**</span></span>](iportabledevicekeycollection.md)                 | <span data-ttu-id="a6e2c-124">Contient les paramètres pour une méthode donnée.</span><span class="sxs-lookup"><span data-stu-id="a6e2c-124">Contains the parameters for a given method.</span></span>                                                                    |



 

<span data-ttu-id="a6e2c-125">Quand l’utilisateur choisit l’option « 5 » sur la ligne de commande, l’application appelle la méthode **ListSupportedMethods** qui se trouve dans le module ServiceMethods. cpp.</span><span class="sxs-lookup"><span data-stu-id="a6e2c-125">When the user chooses option "5" at the command line, the application invokes the **ListSupportedMethods** method that is found in the ServiceMethods.cpp module.</span></span>

<span data-ttu-id="a6e2c-126">Notez qu’avant de récupérer la liste des événements, l’exemple d’application ouvre un service de contacts sur un appareil connecté.</span><span class="sxs-lookup"><span data-stu-id="a6e2c-126">Note that prior to retrieving the list of events, the sample application opens a Contacts service on a connected device.</span></span>

<span data-ttu-id="a6e2c-127">Dans WPD, une méthode est décrite par son nom, ses droits d’accès, ses paramètres et ses données associées.</span><span class="sxs-lookup"><span data-stu-id="a6e2c-127">In WPD, a method is described by its name, access rights, parameters, and related data.</span></span> <span data-ttu-id="a6e2c-128">L’exemple d’application affiche un nom convivial, par exemple « CustomMethod », ou un GUID.</span><span class="sxs-lookup"><span data-stu-id="a6e2c-128">The sample application displays a user-friendly name, for example, "CustomMethod", or a GUID.</span></span> <span data-ttu-id="a6e2c-129">Le nom ou le GUID de la méthode est suivi des données d’accès (« lecture/écriture »), du nom de tout format associé et des données de paramètre.</span><span class="sxs-lookup"><span data-stu-id="a6e2c-129">The method name or GUID is followed by access data ("Read/Write"), the name of any associated format, and the parameter data.</span></span> <span data-ttu-id="a6e2c-130">Ces données incluent le nom du paramètre, l’utilisation, le VARTYPE et le formulaire.</span><span class="sxs-lookup"><span data-stu-id="a6e2c-130">This data includes the parameter name, usage, VARTYPE, and form.</span></span>

<span data-ttu-id="a6e2c-131">Cinq méthodes dans le module ServiceMethods. cpp prennent en charge la récupération des méthodes (et des données associées) pour le service de contacts donné : **ListSupportedMethods**, **DisplayMethod**, **DisplayMethodAccess**, **displayFormat** et **DisplayMethodParameters**.</span><span class="sxs-lookup"><span data-stu-id="a6e2c-131">Five methods in the ServiceMethods.cpp module support the retrieval of methods (and related data) for the given Contacts service: **ListSupportedMethods**, **DisplayMethod**, **DisplayMethodAccess**, **DisplayFormat**, and **DisplayMethodParameters**.</span></span> <span data-ttu-id="a6e2c-132">La méthode **ListSupportedMethods** récupère le nombre de méthodes prises en charge et l’identificateur GUID pour chaque ; Il appelle ensuite la méthode **DisplayMethod** .</span><span class="sxs-lookup"><span data-stu-id="a6e2c-132">The **ListSupportedMethods** method retrieves a count of supported methods and the GUID identifier for each; it then calls the **DisplayMethod** method.</span></span> <span data-ttu-id="a6e2c-133">La méthode **DisplayMethod** appelle la méthode [**IPortableDeviceServiceCapapbilities :: GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) pour récupérer les options, les paramètres, etc. de la méthode donnée.</span><span class="sxs-lookup"><span data-stu-id="a6e2c-133">The **DisplayMethod** method calls the [**IPortableDeviceServiceCapapbilities::GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) method to retrieve the given method's options, parameters, and so on.</span></span> <span data-ttu-id="a6e2c-134">Une fois que le **DisplayMethod** a récupéré les données de la méthode, il restitue le nom (ou le GUID), les restrictions d’accès, le format associé (le cas échéant) et les descriptions des paramètres.</span><span class="sxs-lookup"><span data-stu-id="a6e2c-134">After the **DisplayMethod** retrieves the method data, it renders the name (or GUID), the access restrictions, the associated format (if any), and the parameter descriptions.</span></span> <span data-ttu-id="a6e2c-135">**DisplayMethodAccess**, **displayFormat** et **DisplayMethodParameters** sont des fonctions d’assistance qui restituent leurs champs de données respectifs.</span><span class="sxs-lookup"><span data-stu-id="a6e2c-135">The **DisplayMethodAccess**, **DisplayFormat**, and **DisplayMethodParameters** are helper functions that render their respective fields of data.</span></span>

<span data-ttu-id="a6e2c-136">La méthode **ListSupportedMethods** appelle la méthode [**IPortableDeviceService :: Capabilities**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) pour récupérer une interface [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) .</span><span class="sxs-lookup"><span data-stu-id="a6e2c-136">The **ListSupportedMethods** method invokes the [**IPortableDeviceService::Capabilities**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) method to retrieve an [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) interface.</span></span> <span data-ttu-id="a6e2c-137">À l’aide de cette interface, elle récupère les méthodes prises en charge en appelant la méthode [**IPortableDeviceServiceCapabilities :: GetSupportedMethods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedmethods) .</span><span class="sxs-lookup"><span data-stu-id="a6e2c-137">Using this interface, it retrieves the supported methods by calling the [**IPortableDeviceServiceCapabilities::GetSupportedMethods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedmethods) method.</span></span> <span data-ttu-id="a6e2c-138">La méthode **GetSupportedMethods** récupère les GUID pour chaque méthode prise en charge par le service et copie ce GUID dans un objet [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="a6e2c-138">The **GetSupportedMethods** method retrieves the GUIDs for each method supported by the service and copies that GUID into an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object.</span></span>

<span data-ttu-id="a6e2c-139">Le code suivant utilise la méthode **ListSupportedMethods** .</span><span class="sxs-lookup"><span data-stu-id="a6e2c-139">The following code uses the **ListSupportedMethods** method.</span></span>


```C++
// List all supported methods on the service
void ListSupportedMethods(IPortableDeviceService* pService)
{
    HRESULT hr              = S_OK;
    DWORD   dwNumMethods    = 0;
    CComPtr<IPortableDeviceServiceCapabilities>     pCapabilities;
    CComPtr<IPortableDevicePropVariantCollection>   pMethods;

    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceServiceCapabilities interface from the IPortableDeviceService interface to
    // access the service capabilities-specific methods.
    hr = pService->Capabilities(&pCapabilities);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceServiceCapabilities from IPortableDeviceService, hr = 0x%lx\n",hr);
    }

    // Get all methods supported by the service.
    if (SUCCEEDED(hr))
    {
        hr = pCapabilities->GetSupportedMethods(&pMethods);
        if (FAILED(hr))
        {
            printf("! Failed to get supported methods from the service, hr = 0x%lx\n",hr);
        }
    }

    // Get the number of supported methods found on the service.
    if (SUCCEEDED(hr))
    {
        hr = pMethods->GetCount(&dwNumMethods);
        if (FAILED(hr))
        {
            printf("! Failed to get number of supported methods, hr = 0x%lx\n",hr);
        }
    }

    printf("\n%d Supported Methods Found on the service\n\n", dwNumMethods);

    // Loop through each method and display it
    if (SUCCEEDED(hr))
    {
        for (DWORD dwIndex = 0; dwIndex < dwNumMethods; dwIndex++)
        {
            PROPVARIANT pv = {0};
            PropVariantInit(&pv);
            hr = pMethods->GetAt(dwIndex, &pv);

            if (SUCCEEDED(hr))
            {
                // We have a method.  It is assumed that
                // methods are returned as VT_CLSID VarTypes.
                if (pv.puuid != NULL)
                {
                    DisplayMethod(pCapabilities, *pv.puuid);
                    printf("\n");
                }
            }

            PropVariantClear(&pv);
        }
    }    
}
```



<span data-ttu-id="a6e2c-140">Une fois que la méthode **ListSupportedMethods** a récupéré le GUID pour chaque événement pris en charge par le service donné, elle appelle la méthode **DisplayMethod** pour récupérer les attributs spécifiques à la méthode.</span><span class="sxs-lookup"><span data-stu-id="a6e2c-140">After the **ListSupportedMethods** method retrieves the GUID for each event supported by the given service, it invokes the **DisplayMethod** method to retrieve the method-specific attributes.</span></span> <span data-ttu-id="a6e2c-141">Ces attributs sont notamment : le nom convivial du script de la méthode, les restrictions d’accès requises, tout format associé et la liste de paramètres.</span><span class="sxs-lookup"><span data-stu-id="a6e2c-141">These attributes include: the method's script-friendly name , required access restrictions, any associated format, and list of parameters.</span></span>

<span data-ttu-id="a6e2c-142">La méthode **DisplayMethod** appelle la méthode [**IPortableDeviceServiceCapabilities :: GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) pour récupérer une collection d’attributs pour la méthode donnée.</span><span class="sxs-lookup"><span data-stu-id="a6e2c-142">The **DisplayMethod** method invokes the [**IPortableDeviceServiceCapabilities::GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) method to retrieve a collection of attributes for the given method.</span></span> <span data-ttu-id="a6e2c-143">Il appelle ensuite la méthode [**IPortableDeviceValues :: GetStringValue**](iportabledevicevalues-getstringvalue.md) pour récupérer le nom de la méthode.</span><span class="sxs-lookup"><span data-stu-id="a6e2c-143">It then calls the [**IPortableDeviceValues::GetStringValue**](iportabledevicevalues-getstringvalue.md) method to retrieve the method's name.</span></span> <span data-ttu-id="a6e2c-144">**DisplayMethod** appelle [**IPortableDeviceValues :: GetUnsignedIntegerValue**](iportabledevicevalues-getunsignedintegervalue.md) pour récupérer le restrctions d’accès.</span><span class="sxs-lookup"><span data-stu-id="a6e2c-144">The **DisplayMethod** calls the [**IPortableDeviceValues::GetUnsignedIntegerValue**](iportabledevicevalues-getunsignedintegervalue.md) to retrieve the access restrctions.</span></span> <span data-ttu-id="a6e2c-145">Après cela, il appelle [**IPortableDeviceValues :: GetGuidValue**](iportabledevicevalues-getguidvalue.md) pour récupérer tout format associé.</span><span class="sxs-lookup"><span data-stu-id="a6e2c-145">After this, it calls [**IPortableDeviceValues::GetGuidValue**](iportabledevicevalues-getguidvalue.md) to retrieve any associated format.</span></span> <span data-ttu-id="a6e2c-146">Enfin, **DisplayMethod** appelle [**IPortableDeviceValues :: GetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md) pour récupérer les données de paramètre.</span><span class="sxs-lookup"><span data-stu-id="a6e2c-146">And, finally, the **DisplayMethod** calls the [**IPortableDeviceValues::GetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md) to retrieve the parameter data.</span></span> <span data-ttu-id="a6e2c-147">Il passe les données retournées par ces méthodes aux fonctions d’assistance **DisplayMethodAccess**, **displayFormat** et **DisplayMethodParameters** , qui restituent les informations pour la méthode donnée.</span><span class="sxs-lookup"><span data-stu-id="a6e2c-147">It passes the data returned by these methods to the **DisplayMethodAccess**, **DisplayFormat**, and **DisplayMethodParameters** helper functions, which render the information for the given method.</span></span>

<span data-ttu-id="a6e2c-148">Le code suivant utilise la méthode **DisplayMethod** .</span><span class="sxs-lookup"><span data-stu-id="a6e2c-148">The following code uses the **DisplayMethod** method.</span></span>


```C++
// Display basic information about a method
void DisplayMethod(
    IPortableDeviceServiceCapabilities* pCapabilities,
    REFGUID                             Method)
{
    CComPtr<IPortableDeviceValues> pAttributes;

    // Get the method attributes which describe the method
    HRESULT hr = pCapabilities->GetMethodAttributes(Method, &pAttributes);
    if (FAILED(hr))
    {
        printf("! Failed to get the method attributes, hr = 0x%lx\n",hr);
    }

    if (SUCCEEDED(hr))
    {
        PWSTR   pszMethodName  = NULL;
        DWORD   dwMethodAccess = WPD_COMMAND_ACCESS_READ;
        GUID    guidFormat     = GUID_NULL;

        CComPtr<IPortableDeviceValues>          pOptions;
        CComPtr<IPortableDeviceKeyCollection>   pParameters;

        // Display the name of the method if available. Otherwise, fall back to displaying the GUID.
        hr = pAttributes->GetStringValue(WPD_METHOD_ATTRIBUTE_NAME, &pszMethodName);
        if (SUCCEEDED(hr))
        {
            printf("%ws", pszMethodName);
        }
        else
        {
            printf("%ws", (PWSTR)CGuidToString(Method));
        }       

        // Display the method access if available, otherwise default to WPD_COMMAND_ACCESS_READ access
        hr = pAttributes->GetUnsignedIntegerValue(WPD_METHOD_ATTRIBUTE_ACCESS, &dwMethodAccess);
        if (FAILED(hr))
        {
            dwMethodAccess = WPD_COMMAND_ACCESS_READ;
            hr = S_OK;
        }
        printf("\n\tAccess: ");
        DisplayMethodAccess(dwMethodAccess);

        // Display the associated format if specified.
        // Methods that have an associated format may only be supported for that format.
        // Methods that don't have associated formats generally apply to the entire service.
        hr = pAttributes->GetGuidValue(WPD_METHOD_ATTRIBUTE_ASSOCIATED_FORMAT, &guidFormat);
        if (SUCCEEDED(hr))
        {
            printf("\n\tAssociated Format: ");
            DisplayFormat(pCapabilities, guidFormat);
        }

        // Display the method parameters, if available
        hr = pAttributes->GetIPortableDeviceKeyCollectionValue(WPD_METHOD_ATTRIBUTE_PARAMETERS, &pParameters);
        if (SUCCEEDED(hr))
        {
            DisplayMethodParameters(pCapabilities, Method, pParameters);
        }
        
        CoTaskMemFree(pszMethodName);
        pszMethodName = NULL;

    }
}
```



<span data-ttu-id="a6e2c-149">La fonction d’assistance **DisplayMethodAccess** reçoit une valeur DWORD qui contient les options d’accès de la méthode.</span><span class="sxs-lookup"><span data-stu-id="a6e2c-149">The **DisplayMethodAccess** helper function receives a DWORD value that contains the method's access options.</span></span> <span data-ttu-id="a6e2c-150">Elle compare cette valeur à \_ la commande wpd Access \_ \_ Read et wpd \_ Command \_ Access \_ ReadWrite pour déterminer le privilège d’accès à la méthode.</span><span class="sxs-lookup"><span data-stu-id="a6e2c-150">It compares this value to WPD\_COMMAND\_ACCESS\_READ and WPD\_COMMAND\_ACCESS\_READWRITE to determine the method's access privilege.</span></span> <span data-ttu-id="a6e2c-151">À l’aide du résultat, il restitue une chaîne indiquant la restriction d’accès pour la méthode donnée.</span><span class="sxs-lookup"><span data-stu-id="a6e2c-151">Using the result, it renders a string indicating the access restriction for the given method.</span></span>

<span data-ttu-id="a6e2c-152">Le code suivant utilise la fonction d’assistance **DisplayMethodAccess** .</span><span class="sxs-lookup"><span data-stu-id="a6e2c-152">The following code uses the **DisplayMethodAccess** helper function.</span></span>


```C++
void DisplayMethodAccess(
    DWORD   dwAccess)
{
    switch(static_cast<WPD_COMMAND_ACCESS_TYPES>(dwAccess))
    {
        case WPD_COMMAND_ACCESS_READ:
            printf("Read");
            break;
            
        case WPD_COMMAND_ACCESS_READWRITE:
            printf("Read/Write");
            break;

        default:
            printf("Unknown Access");
            break;
    }
}
```



<span data-ttu-id="a6e2c-153">La fonction d’assistance **DisplayMethod** reçoit un objet [**IPORTABLEDEVICESERVICECAPABILITIES**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) et le GUID de la méthode en tant que paramètres.</span><span class="sxs-lookup"><span data-stu-id="a6e2c-153">The **DisplayMethod** helper function receives an [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) object and the method's GUID as parameters.</span></span> <span data-ttu-id="a6e2c-154">À l’aide de l’objet **IPortableDeviceServiceCapabilities** , il appelle la méthode [**IPortableDeviceServiceCapabilities :: GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) pour récupérer les attributs de méthode et les restituer dans la fenêtre de console de l’application.</span><span class="sxs-lookup"><span data-stu-id="a6e2c-154">Using the **IPortableDeviceServiceCapabilities** object, it invokes the [**IPortableDeviceServiceCapabilities::GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) method to retrieve the method attributes and render them in the application's console window.</span></span>

<span data-ttu-id="a6e2c-155">La fonction d’assistance **DisplayMethodParameters** reçoit un objet [**IPORTABLEDEVICESERVICECAPABILITIES**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) , le GUID de la méthode et un objet IPortableDeviceKeyCollection contenant les paramètres de la méthode.</span><span class="sxs-lookup"><span data-stu-id="a6e2c-155">The **DisplayMethodParameters** helper function receives an [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) object, the method's GUID, and an IPortableDeviceKeyCollection object containing the method parameters.</span></span> <span data-ttu-id="a6e2c-156">À l’aide de l’objet [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) , elle appelle la méthode [**IPortableDeviceServiceCapabilities :: GetMethodParameterAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodparameterattributes) pour récupérer le nom, l’utilisation, le VarType et le formulaire du paramètre.</span><span class="sxs-lookup"><span data-stu-id="a6e2c-156">Using the [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) object, it invokes the [**IPortableDeviceServiceCapabilities::GetMethodParameterAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodparameterattributes) method to retrieve the parameter's name, usage, VARTYPE, and form.</span></span> <span data-ttu-id="a6e2c-157">Elle affiche ces informations dans la fenêtre de console de l’application.</span><span class="sxs-lookup"><span data-stu-id="a6e2c-157">It renders this information in the application's console window.</span></span>

<span data-ttu-id="a6e2c-158">Le code suivant utilise la fonction d’assistance **DisplayMethodParameters** .</span><span class="sxs-lookup"><span data-stu-id="a6e2c-158">The following code uses the **DisplayMethodParameters** helper function.</span></span>


```C++
// Display the method parameters.
void DisplayMethodParameters(
    IPortableDeviceServiceCapabilities* pCapabilities,
    REFGUID                             Method,
    IPortableDeviceKeyCollection*       pParameters)
{
    DWORD   dwNumParameters = 0;

    // Get the number of parameters for this event.
    HRESULT hr = pParameters->GetCount(&dwNumParameters);
    if (FAILED(hr))
    {
        printf("! Failed to get number of parameters, hr = 0x%lx\n",hr);
    }

    printf("\n\t%d Method Parameters:\n", dwNumParameters);

    // Loop through each parameter and display it
    if (SUCCEEDED(hr))
    {
        for (DWORD dwIndex = 0; dwIndex < dwNumParameters; dwIndex++)
        {
            PROPERTYKEY parameter;
            hr = pParameters->GetAt(dwIndex, &parameter);

            if (SUCCEEDED(hr))
            {
                CComPtr<IPortableDeviceValues> pAttributes;

                // Display the parameter's Name, Usage, Vartype, and Form
                hr = pCapabilities->GetMethodParameterAttributes(Method, parameter, &pAttributes);
                if (FAILED(hr))
                {
                    printf("! Failed to get the method parameter attributes, hr = 0x%lx\n",hr);
                }

                if (SUCCEEDED(hr))
                {
                    PWSTR   pszParameterName    = NULL;
                    DWORD   dwAttributeVarType  = 0;
                    DWORD   dwAttributeForm     = WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED;
                    DWORD   dwAttributeUsage    = (DWORD)-1;

                    hr = pAttributes->GetStringValue(WPD_PARAMETER_ATTRIBUTE_NAME, &pszParameterName);
                    if (SUCCEEDED(hr))
                    {
                        printf("\t\tName: %ws\n", pszParameterName);
                    }
                    else
                    {
                        printf("! Failed to get the method parameter name, hr = 0x%lx\n",hr);
                    }

                    // Read the WPD_PARAMETER_ATTRIBUTE_USAGE value, if specified. 
                    hr = pAttributes->GetUnsignedIntegerValue(WPD_PARAMETER_ATTRIBUTE_USAGE, &dwAttributeUsage);
                    if (SUCCEEDED(hr))
                    {
                        printf("\t\tUsage: ");
                        DisplayParameterUsage(dwAttributeUsage);
                        printf("\n");
                    }
                    else
                    {
                        printf("! Failed to get the method parameter usage, hr = 0x%lx\n",hr);
                    }

                    hr = pAttributes->GetUnsignedIntegerValue(WPD_PARAMETER_ATTRIBUTE_VARTYPE, &dwAttributeVarType);
                    if (SUCCEEDED(hr))
                    {
                        printf("\t\tVARTYPE: ");
                        DisplayVarType(static_cast<VARTYPE>(dwAttributeVarType));
                        printf("\n");
                    }
                    else
                    {
                        printf("! Failed to get the method parameter VARTYPE, hr = 0x%lx\n",hr);
                    }

                    // Read the WPD_PARAMETER_ATTRIBUTE_FORM value.
                    hr = pAttributes->GetUnsignedIntegerValue(WPD_PARAMETER_ATTRIBUTE_FORM, &dwAttributeForm);
                    if (FAILED(hr))
                    {
                        // If the read fails, assume WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED
                        dwAttributeForm = WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED;
                        hr = S_OK;
                    }

                    printf("\t\tForm: ");
                    DisplayParameterForm(dwAttributeForm);
                    printf("\n");

                    CoTaskMemFree(pszParameterName);
                    pszParameterName = NULL;
                }
                
                printf("\n");
            }
        }
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="a6e2c-159">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a6e2c-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6e2c-160">**IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="a6e2c-160">**IPortableDeviceKeyCollection**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="a6e2c-161">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="a6e2c-161">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[<span data-ttu-id="a6e2c-162">**IPortableDeviceServiceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="a6e2c-162">**IPortableDeviceServiceCapabilities**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)
</dt> <dt>

[<span data-ttu-id="a6e2c-163">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="a6e2c-163">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="a6e2c-164">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="a6e2c-164">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



