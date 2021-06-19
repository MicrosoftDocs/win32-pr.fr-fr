---
title: Récupération des propriétés de l’objet WPD
description: L’application WpdServiceApiSample montre comment une application peut récupérer les propriétés de Content-Object prises en charge par un service de contacts donné.
ms.assetid: 7fbd6f65-366a-49ea-a680-be77ca0d64f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98e57258993d0a81f68042195db2caf338c97c53
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404312"
---
# <a name="retrieving-wpd-object-properties"></a><span data-ttu-id="14ee8-103">Récupération des propriétés de l’objet WPD</span><span class="sxs-lookup"><span data-stu-id="14ee8-103">Retrieving WPD object properties</span></span>

<span data-ttu-id="14ee8-104">Les services contiennent souvent des objets enfants qui appartiennent à l’un des formats pris en charge par chaque service.</span><span class="sxs-lookup"><span data-stu-id="14ee8-104">Services often contain child objects that belong to one of the formats that each service supports.</span></span> <span data-ttu-id="14ee8-105">Par exemple, un service de contacts peut prendre en charge plusieurs objets de contact du format de contact abstrait.</span><span class="sxs-lookup"><span data-stu-id="14ee8-105">For example, a Contacts service may support multiple contact objects of the Abstract Contact format.</span></span> <span data-ttu-id="14ee8-106">Chaque objet contact est décrit par des propriétés associées (nom de contact, numéro de téléphone, adresse de messagerie, etc.).</span><span class="sxs-lookup"><span data-stu-id="14ee8-106">Each contact object is described by related properties (contact name, phone number, email address, and so on).</span></span>

<span data-ttu-id="14ee8-107">L’application WpdServiceApiSample comprend du code qui montre comment une application peut récupérer les propriétés Content-Object prises en charge par un service de contacts donné.</span><span class="sxs-lookup"><span data-stu-id="14ee8-107">The WpdServiceApiSample application includes code that demonstrates how an application can retrieve the content-object properties supported by a given Contacts service.</span></span> <span data-ttu-id="14ee8-108">Cet exemple utilise les interfaces suivantes.</span><span class="sxs-lookup"><span data-stu-id="14ee8-108">This sample uses the following interfaces.</span></span>



| <span data-ttu-id="14ee8-109">Interface</span><span class="sxs-lookup"><span data-stu-id="14ee8-109">Interface</span></span> | <span data-ttu-id="14ee8-110">Description</span><span class="sxs-lookup"><span data-stu-id="14ee8-110">Description</span></span>    |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="14ee8-111">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="14ee8-111">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)             | <span data-ttu-id="14ee8-112">Récupère l’interface **IPortableDeviceContent2** pour accéder aux méthodes de service prises en charge.</span><span class="sxs-lookup"><span data-stu-id="14ee8-112">Retrieves the **IPortableDeviceContent2** interface to access the supported service methods.</span></span> |
| [<span data-ttu-id="14ee8-113">**IPortableDeviceContent2**</span><span class="sxs-lookup"><span data-stu-id="14ee8-113">**IPortableDeviceContent2**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)           | <span data-ttu-id="14ee8-114">Fournit l’accès aux méthodes spécifiques au contenu.</span><span class="sxs-lookup"><span data-stu-id="14ee8-114">Provides access to the content-specific methods.</span></span>                                             |
| [<span data-ttu-id="14ee8-115">**IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="14ee8-115">**IPortableDeviceProperties**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)       | <span data-ttu-id="14ee8-116">Récupère les valeurs de propriété de l’objet.</span><span class="sxs-lookup"><span data-stu-id="14ee8-116">Retrieves the object property values.</span></span>                                                        |
| [<span data-ttu-id="14ee8-117">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="14ee8-117">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)               | <span data-ttu-id="14ee8-118">Contient les valeurs de propriété qui ont été lues pour cet objet.</span><span class="sxs-lookup"><span data-stu-id="14ee8-118">Holds the property values that were read for that object.</span></span>                                    |
| [<span data-ttu-id="14ee8-119">**IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="14ee8-119">**IPortableDeviceKeyCollection**</span></span>](iportabledevicekeycollection.md) | <span data-ttu-id="14ee8-120">Contient les paramètres pour une méthode donnée.</span><span class="sxs-lookup"><span data-stu-id="14ee8-120">Contains the parameters for a given method.</span></span>                                                  |



 

<span data-ttu-id="14ee8-121">Quand l’utilisateur choisit l’option « 7 » sur la ligne de commande, l’application appelle la méthode **ReadContentProperties** qui se trouve dans le module ContentProperties. cpp.</span><span class="sxs-lookup"><span data-stu-id="14ee8-121">When the user chooses option "7" at the command line, the application invokes the **ReadContentProperties** method that is found in the ContentProperties.cpp module.</span></span>

<span data-ttu-id="14ee8-122">Cette méthode récupère les quatre propriétés suivantes pour l’objet contact spécifié.</span><span class="sxs-lookup"><span data-stu-id="14ee8-122">This method retrieves the following four properties for the specified contact object.</span></span>



| <span data-ttu-id="14ee8-123">Propriété</span><span class="sxs-lookup"><span data-stu-id="14ee8-123">Property</span></span>                     | <span data-ttu-id="14ee8-124">Description</span><span class="sxs-lookup"><span data-stu-id="14ee8-124">Description</span></span>                                                                                                                                                                                                      | <span data-ttu-id="14ee8-125">Services d’appareil PROPERTYKEY</span><span class="sxs-lookup"><span data-stu-id="14ee8-125">Device Services PROPERTYKEY</span></span>     | <span data-ttu-id="14ee8-126">WPD \_ PROPERTYKEY équivalent</span><span class="sxs-lookup"><span data-stu-id="14ee8-126">Equivalent WPD\_PROPERTYKEY</span></span>         |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------|-------------------------------------|
| <span data-ttu-id="14ee8-127">Identificateur de l’objet parent</span><span class="sxs-lookup"><span data-stu-id="14ee8-127">Parent-object identifier</span></span>     | <span data-ttu-id="14ee8-128">Chaîne qui spécifie l’identificateur pour le parent de l’objet donné.</span><span class="sxs-lookup"><span data-stu-id="14ee8-128">A string that specifies the identifier for the given object's parent.</span></span>                                                                                                                                            | <span data-ttu-id="14ee8-129">\_GenericObj, \_ ParentId</span><span class="sxs-lookup"><span data-stu-id="14ee8-129">PKEY\_GenericObj\_ParentID</span></span>      | <span data-ttu-id="14ee8-130">\_ \_ ID parent de l’objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="14ee8-130">WPD\_OBJECT\_PARENT\_ID</span></span>             |
| <span data-ttu-id="14ee8-131">Nom d’objet</span><span class="sxs-lookup"><span data-stu-id="14ee8-131">Object name</span></span>                  | <span data-ttu-id="14ee8-132">Chaîne qui spécifie le nom de l’objet donné.</span><span class="sxs-lookup"><span data-stu-id="14ee8-132">A string that specifies the name of the given object</span></span>                                                                                                                                                             | <span data-ttu-id="14ee8-133">Nom du GenericObj de la \_ \_</span><span class="sxs-lookup"><span data-stu-id="14ee8-133">PKEY\_GenericObj\_Name</span></span>          | <span data-ttu-id="14ee8-134">nom de l' \_ objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="14ee8-134">WPD\_OBJECT\_NAME</span></span>                   |
| <span data-ttu-id="14ee8-135">Identificateur unique persistant</span><span class="sxs-lookup"><span data-stu-id="14ee8-135">Persistent unique identifier</span></span> | <span data-ttu-id="14ee8-136">Chaîne qui spécifie un identificateur unique pour l’objet donné.</span><span class="sxs-lookup"><span data-stu-id="14ee8-136">A string that specifies a unique identifier for the given object.</span></span> <span data-ttu-id="14ee8-137">Cet identificateur est persistant entre les sessions, contrairement à l’identificateur d’objet.</span><span class="sxs-lookup"><span data-stu-id="14ee8-137">This identifier is persistent across sessions, unlike the object identifier.</span></span> <span data-ttu-id="14ee8-138">Pour les services, il doit s’agir d’une représentation sous forme de chaîne d’un GUID.</span><span class="sxs-lookup"><span data-stu-id="14ee8-138">For services, this needs to be a string-representation of a GUID.</span></span> | <span data-ttu-id="14ee8-139">\_GenericObj \_ PersistentUID</span><span class="sxs-lookup"><span data-stu-id="14ee8-139">PKEY\_GenericObj\_PersistentUID</span></span> | <span data-ttu-id="14ee8-140">\_ \_ \_ ID unique persistant de l’objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="14ee8-140">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span> |
| <span data-ttu-id="14ee8-141">Format de l’objet</span><span class="sxs-lookup"><span data-stu-id="14ee8-141">Object format</span></span>                | <span data-ttu-id="14ee8-142">Identificateur global unique (GUID) qui spécifie le format du fichier correspondant à un objet donné</span><span class="sxs-lookup"><span data-stu-id="14ee8-142">A globally unique identifier (GUID) that specifies the format of the file corresponding to a given object</span></span>                                                                                                        | <span data-ttu-id="14ee8-143">\_GenericObj \_ ObjectFormat</span><span class="sxs-lookup"><span data-stu-id="14ee8-143">PKEY\_GenericObj\_ObjectFormat</span></span>  | <span data-ttu-id="14ee8-144">\_format d’objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="14ee8-144">WPD\_OBJECT\_FORMAT</span></span>                 |



 

-   <span data-ttu-id="14ee8-145">ID parent</span><span class="sxs-lookup"><span data-stu-id="14ee8-145">Parent ID</span></span>
-   <span data-ttu-id="14ee8-146">Nom</span><span class="sxs-lookup"><span data-stu-id="14ee8-146">Name</span></span>
-   <span data-ttu-id="14ee8-147">PersistentUID</span><span class="sxs-lookup"><span data-stu-id="14ee8-147">PersistentUID</span></span>
-   <span data-ttu-id="14ee8-148">Format</span><span class="sxs-lookup"><span data-stu-id="14ee8-148">Format</span></span>

<span data-ttu-id="14ee8-149">Notez qu’avant de récupérer les propriétés de contenu, l’exemple d’application ouvre un service de contacts sur un appareil connecté.</span><span class="sxs-lookup"><span data-stu-id="14ee8-149">Note that prior to retrieving the content properties, the sample application opens a Contacts service on a connected device.</span></span>

<span data-ttu-id="14ee8-150">Le code suivant pour la méthode **ReadContentProperties** montre comment l’application utilise l’interface [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) pour récupérer une interface [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) .</span><span class="sxs-lookup"><span data-stu-id="14ee8-150">The following code for the **ReadContentProperties** method demonstrates how the application uses the [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) interface to retrieve an [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) interface.</span></span> <span data-ttu-id="14ee8-151">En passant les PROPERTYKEYS des propriétés demandées à la méthode [**IPortableDeviceProperties :: GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) , **ReadContentProperties** récupère les valeurs demandées, puis les affiche dans la fenêtre de console.</span><span class="sxs-lookup"><span data-stu-id="14ee8-151">By passing the PROPERTYKEYS of the requested properties to the [**IPortableDeviceProperties::GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) method, **ReadContentProperties** retrieves the requested values, and then displays them to the console window.</span></span>


```C++
// Reads properties for the user specified object.
void ReadContentProperties(
    IPortableDeviceService*    pService)
{
    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    HRESULT                               hr              = S_OK;
    WCHAR                                 szSelection[81] = {0};
    CComPtr<IPortableDeviceProperties>    pProperties;
    CComPtr<IPortableDeviceValues>        pObjectProperties;
    CComPtr<IPortableDeviceContent2>      pContent;
    CComPtr<IPortableDeviceKeyCollection> pPropertiesToRead;

    // Prompt user to enter an object identifier on the device to read properties from.
    printf("Enter the identifer of the object you wish to read properties from.\n>");
    hr = StringCbGetsW(szSelection,sizeof(szSelection));
    if (FAILED(hr))
    {
        printf("An invalid object identifier was specified, aborting property reading\n");
    }

    // 1) Get an IPortableDeviceContent2 interface from the IPortableDeviceService interface to
    // access the content-specific methods.
    if (SUCCEEDED(hr))
    {
        hr = pService->Content(&pContent);
        if (FAILED(hr))
        {
            printf("! Failed to get IPortableDeviceContent2 from IPortableDeviceService, hr = 0x%lx\n",hr);
        }
    }

    // 2) Get an IPortableDeviceProperties interface from the IPortableDeviceContent2 interface
    // to access the property-specific methods.
    if (SUCCEEDED(hr))
    {
        hr = pContent->Properties(&pProperties);
        if (FAILED(hr))
        {
            printf("! Failed to get IPortableDeviceProperties from IPortableDeviceContent2, hr = 0x%lx\n",hr);
        }
    }

    // 3) CoCreate an IPortableDeviceKeyCollection interface to hold the property keys
    // we wish to read.
    hr = CoCreateInstance(CLSID_PortableDeviceKeyCollection,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_PPV_ARGS(&pPropertiesToRead));
    if (SUCCEEDED(hr))
    {
        // 4) Populate the IPortableDeviceKeyCollection with the keys we wish to read.
        // NOTE: We are not handling any special error cases here so we can proceed with
        // adding as many of the target properties as we can.
        if (pPropertiesToRead != NULL)
        {
            HRESULT hrTemp = S_OK;
            hrTemp = pPropertiesToRead->Add(PKEY_GenericObj_ParentID);
            if (FAILED(hrTemp))
            {
                printf("! Failed to add PKEY_GenericObj_ParentID to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
            }

            hrTemp = pPropertiesToRead->Add(PKEY_GenericObj_Name);
            if (FAILED(hrTemp))
            {
                printf("! Failed to add PKEY_GenericObj_Name to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
            }

            hrTemp = pPropertiesToRead->Add(PKEY_GenericObj_PersistentUID);
            if (FAILED(hrTemp))
            {
                printf("! Failed to add PKEY_GenericObj_PersistentUID to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
            }

            hrTemp = pPropertiesToRead->Add(PKEY_GenericObj_ObjectFormat);
            if (FAILED(hrTemp))
            {
                printf("! Failed to add PKEY_GenericObj_ObjectFormat to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
            }

        }
    }

    // 5) Call GetValues() passing the collection of specified PROPERTYKEYs.
    if (SUCCEEDED(hr))
    {
        hr = pProperties->GetValues(szSelection,         // The object whose properties we are reading
                                    pPropertiesToRead,   // The properties we want to read
                                    &pObjectProperties); // Driver supplied property values for the specified object
        if (FAILED(hr))
        {
            printf("! Failed to get all properties for object '%ws', hr= 0x%lx\n", szSelection, hr);
        }
    }

    // 6) Display the returned property values to the user
    if (SUCCEEDED(hr))
    {
        DisplayStringProperty(pObjectProperties, PKEY_GenericObj_ParentID,        NAME_GenericObj_ParentID);
        DisplayStringProperty(pObjectProperties, PKEY_GenericObj_Name,            NAME_GenericObj_Name);
        DisplayStringProperty(pObjectProperties, PKEY_GenericObj_PersistentUID,   NAME_GenericObj_PersistentUID);
        DisplayGuidProperty  (pObjectProperties, PKEY_GenericObj_ObjectFormat,    NAME_GenericObj_ObjectFormat);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="14ee8-152">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="14ee8-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14ee8-153">**IPortableDeviceContent2**</span><span class="sxs-lookup"><span data-stu-id="14ee8-153">**IPortableDeviceContent2**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)
</dt> <dt>

[<span data-ttu-id="14ee8-154">**IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="14ee8-154">**IPortableDeviceProperties**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="14ee8-155">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="14ee8-155">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



