---
description: Récupération des méthodes de service prises en charge
ms.assetid: 783a6552-9b22-4af4-9252-b443e2624687
title: Récupération des méthodes de service prises en charge
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b021aa868ffaa95df23a729e94d62eae8a0c632e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127525116"
---
# <a name="retrieving-supported-service-methods"></a>Récupération des méthodes de service prises en charge

Les méthodes de service encapsulent les fonctionnalités que chaque service définit et implémente. Elles sont spécifiques à chaque type de service et sont représentées par un GUID unique.

Par exemple, le service contacts définit une méthode **BeginSync** que les applications appellent pour préparer l’appareil à la synchronisation des objets contact, et une méthode **EndSync** pour informer l’appareil que la synchronisation est terminée.

Les applications peuvent interroger par programme les méthodes prises en charge et accéder à ces méthodes et à leurs attributs à l’aide de l’interface [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) .

Les méthodes de service ne doivent pas être confondues avec les commandes WPD. Les commandes WPD font partie de l’interface de pilote de périphérique WPD standard (DDI) et constituent le mécanisme de communication entre une application WPD et le pilote. Les commandes sont prédéfinies, regroupées par catégories, par exemple \_ , \_ la catégorie wpd commun et sont représentées par une structure PROPERTYKEY. Pour plus d’informations, consultez la rubrique [**commandes**](commands.md) .

L’application WpdServicesApiSample comprend du code qui montre comment une application peut récupérer les méthodes prises en charge par un service de contacts donné en utilisant les interfaces du tableau suivant.



| Interface      | Description         |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                             | Utilisé pour récupérer l’interface **IPortableDeviceServiceCapabilities** pour accéder aux méthodes de service prises en charge. |
| [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)     | Fournit l’accès aux méthodes prises en charge, aux attributs de méthode et aux paramètres de méthode.                             |
| [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) | Contient la liste des méthodes prises en charge.                                                                        |
| [**IPortableDeviceValues**](iportabledevicevalues.md)                               | Contient les attributs pour une méthode et pour les paramètres d’une méthode donnée.                                      |
| [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md)                 | Contient les paramètres pour une méthode donnée.                                                                    |



 

Quand l’utilisateur choisit l’option « 5 » sur la ligne de commande, l’application appelle la méthode **ListSupportedMethods** qui se trouve dans le module ServiceMethods. cpp.

Notez qu’avant de récupérer la liste des événements, l’exemple d’application ouvre un service de contacts sur un appareil connecté.

Dans WPD, une méthode est décrite par son nom, ses droits d’accès, ses paramètres et ses données associées. L’exemple d’application affiche un nom convivial, par exemple « CustomMethod », ou un GUID. Le nom ou le GUID de la méthode est suivi des données d’accès (« lecture/écriture »), du nom de tout format associé et des données de paramètre. Ces données incluent le nom du paramètre, l’utilisation, le VARTYPE et le formulaire.

Cinq méthodes dans le module ServiceMethods. cpp prennent en charge la récupération des méthodes (et des données associées) pour le service de contacts donné : **ListSupportedMethods**, **DisplayMethod**, **DisplayMethodAccess**, **displayFormat** et **DisplayMethodParameters**. La méthode **ListSupportedMethods** récupère le nombre de méthodes prises en charge et l’identificateur GUID pour chaque ; Il appelle ensuite la méthode **DisplayMethod** . La méthode **DisplayMethod** appelle la méthode [**IPortableDeviceServiceCapapbilities :: GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) pour récupérer les options, les paramètres, etc. de la méthode donnée. Une fois que le **DisplayMethod** a récupéré les données de la méthode, il restitue le nom (ou le GUID), les restrictions d’accès, le format associé (le cas échéant) et les descriptions des paramètres. **DisplayMethodAccess**, **displayFormat** et **DisplayMethodParameters** sont des fonctions d’assistance qui restituent leurs champs de données respectifs.

La méthode **ListSupportedMethods** appelle la méthode [**IPortableDeviceService :: Capabilities**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) pour récupérer une interface [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) . À l’aide de cette interface, elle récupère les méthodes prises en charge en appelant la méthode [**IPortableDeviceServiceCapabilities :: GetSupportedMethods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedmethods) . La méthode **GetSupportedMethods** récupère les GUID pour chaque méthode prise en charge par le service et copie ce GUID dans un objet [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) .

Le code suivant utilise la méthode **ListSupportedMethods** .


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



Une fois que la méthode **ListSupportedMethods** a récupéré le GUID pour chaque événement pris en charge par le service donné, elle appelle la méthode **DisplayMethod** pour récupérer les attributs spécifiques à la méthode. Ces attributs sont notamment : le nom convivial du script de la méthode, les restrictions d’accès requises, tout format associé et la liste de paramètres.

La méthode **DisplayMethod** appelle la méthode [**IPortableDeviceServiceCapabilities :: GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) pour récupérer une collection d’attributs pour la méthode donnée. Il appelle ensuite la méthode [**IPortableDeviceValues :: GetStringValue**](iportabledevicevalues-getstringvalue.md) pour récupérer le nom de la méthode. **DisplayMethod** appelle [**IPortableDeviceValues :: GetUnsignedIntegerValue**](iportabledevicevalues-getunsignedintegervalue.md) pour récupérer le restrctions d’accès. Après cela, il appelle [**IPortableDeviceValues :: GetGuidValue**](iportabledevicevalues-getguidvalue.md) pour récupérer tout format associé. Enfin, **DisplayMethod** appelle [**IPortableDeviceValues :: GetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md) pour récupérer les données de paramètre. Il passe les données retournées par ces méthodes aux fonctions d’assistance **DisplayMethodAccess**, **displayFormat** et **DisplayMethodParameters** , qui restituent les informations pour la méthode donnée.

Le code suivant utilise la méthode **DisplayMethod** .


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



La fonction d’assistance **DisplayMethodAccess** reçoit une valeur DWORD qui contient les options d’accès de la méthode. Elle compare cette valeur à \_ la commande wpd Access \_ \_ Read et wpd \_ Command \_ Access \_ ReadWrite pour déterminer le privilège d’accès à la méthode. À l’aide du résultat, il restitue une chaîne indiquant la restriction d’accès pour la méthode donnée.

Le code suivant utilise la fonction d’assistance **DisplayMethodAccess** .


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



La fonction d’assistance **DisplayMethod** reçoit un objet [**IPORTABLEDEVICESERVICECAPABILITIES**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) et le GUID de la méthode en tant que paramètres. À l’aide de l’objet **IPortableDeviceServiceCapabilities** , il appelle la méthode [**IPortableDeviceServiceCapabilities :: GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) pour récupérer les attributs de méthode et les restituer dans la fenêtre de console de l’application.

La fonction d’assistance **DisplayMethodParameters** reçoit un objet [**IPORTABLEDEVICESERVICECAPABILITIES**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) , le GUID de la méthode et un objet IPortableDeviceKeyCollection contenant les paramètres de la méthode. À l’aide de l’objet [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) , elle appelle la méthode [**IPortableDeviceServiceCapabilities :: GetMethodParameterAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodparameterattributes) pour récupérer le nom, l’utilisation, le VarType et le formulaire du paramètre. Elle affiche ces informations dans la fenêtre de console de l’application.

Le code suivant utilise la fonction d’assistance **DisplayMethodParameters** .


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md)
</dt> <dt>

[**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)
</dt> <dt>

[**IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[WpdServicesApiSample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



