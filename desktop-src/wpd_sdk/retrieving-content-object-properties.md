---
title: Récupération des propriétés de l’objet WPD
description: L’application WpdServiceApiSample montre comment une application peut récupérer les propriétés de Content-Object prises en charge par un service de contacts donné.
ms.assetid: 7fbd6f65-366a-49ea-a680-be77ca0d64f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b56b164980249911ce267050143611dc599520fc841e33157bd6ac84718c1728
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806689"
---
# <a name="retrieving-wpd-object-properties"></a>Récupération des propriétés de l’objet WPD

Les services contiennent souvent des objets enfants qui appartiennent à l’un des formats pris en charge par chaque service. Par exemple, un service de contacts peut prendre en charge plusieurs objets de contact du format de contact abstrait. Chaque objet contact est décrit par des propriétés associées (nom de contact, numéro de téléphone, adresse de messagerie, etc.).

L’application WpdServiceApiSample comprend du code qui montre comment une application peut récupérer les propriétés Content-Object prises en charge par un service de contacts donné. Cet exemple utilise les interfaces suivantes.



| Interface | Description    |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)             | Récupère l’interface **IPortableDeviceContent2** pour accéder aux méthodes de service prises en charge. |
| [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)           | Fournit l’accès aux méthodes spécifiques au contenu.                                             |
| [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)       | Récupère les valeurs de propriété de l’objet.                                                        |
| [**IPortableDeviceValues**](iportabledevicevalues.md)               | Contient les valeurs de propriété qui ont été lues pour cet objet.                                    |
| [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) | Contient les paramètres pour une méthode donnée.                                                  |



 

Quand l’utilisateur choisit l’option « 7 » sur la ligne de commande, l’application appelle la méthode **ReadContentProperties** qui se trouve dans le module ContentProperties. cpp.

Cette méthode récupère les quatre propriétés suivantes pour l’objet contact spécifié.



| Propriété                     | Description                                                                                                                                                                                                      | Services d’appareil PROPERTYKEY     | WPD \_ PROPERTYKEY équivalent         |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------|-------------------------------------|
| Identificateur de l’objet parent     | Chaîne qui spécifie l’identificateur pour le parent de l’objet donné.                                                                                                                                            | \_GenericObj, \_ ParentId      | \_ \_ ID parent de l’objet wpd \_             |
| Nom d’objet                  | Chaîne qui spécifie le nom de l’objet donné.                                                                                                                                                             | Nom du GenericObj de la \_ \_          | nom de l' \_ objet wpd \_                   |
| Identificateur unique persistant | Chaîne qui spécifie un identificateur unique pour l’objet donné. Cet identificateur est persistant entre les sessions, contrairement à l’identificateur d’objet. Pour les services, il doit s’agir d’une représentation sous forme de chaîne d’un GUID. | \_GenericObj \_ PersistentUID | \_ \_ \_ ID unique persistant de l’objet wpd \_ |
| Format de l’objet                | Identificateur global unique (GUID) qui spécifie le format du fichier correspondant à un objet donné                                                                                                        | \_GenericObj \_ ObjectFormat  | \_format d’objet wpd \_                 |



 

-   ID parent
-   Name
-   PersistentUID
-   Format

Notez qu’avant de récupérer les propriétés de contenu, l’exemple d’application ouvre un service de contacts sur un appareil connecté.

Le code suivant pour la méthode **ReadContentProperties** montre comment l’application utilise l’interface [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) pour récupérer une interface [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) . En passant les PROPERTYKEYS des propriétés demandées à la méthode [**IPortableDeviceProperties :: GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) , **ReadContentProperties** récupère les valeurs demandées, puis les affiche dans la fenêtre de console.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)
</dt> <dt>

[**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[WpdServicesApiSample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



