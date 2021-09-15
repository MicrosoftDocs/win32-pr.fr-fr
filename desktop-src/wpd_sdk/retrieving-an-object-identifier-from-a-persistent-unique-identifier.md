---
description: Récupération d’un identificateur d’objet à partir d’un identificateur unique persistant
ms.assetid: 146f8943-d4e1-4b87-a812-e534082a4f14
title: Récupération d’un ID d’objet à partir d’un ID unique persistant
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4f997f0faf586a374e5a83c6f96b6508f02eb41
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127522028"
---
# <a name="retrieving-an-object-id-from-a-persistent-unique-id"></a>Récupération d’un ID d’objet à partir d’un ID unique persistant

L’unicité des identificateurs d’objets n’est garantie que pour une session d’appareil donnée ; Si l’utilisateur établit une nouvelle connexion, les identificateurs d’une session précédente peuvent ne pas correspondre aux identificateurs de la session active. Pour résoudre ce problème, l’API WPD prend en charge les identificateurs uniques persistants (PUID), qui persistent sur les sessions de l’appareil.

Certains appareils stockent leurs PUID en mode natif avec un objet donné. D’autres peuvent générer le PUID en se basant sur le hachage des données de l’objet sélectionné. D’autres peuvent traiter les identificateurs d’objets comme des PUID (car ils peuvent garantir que ces identificateurs ne changent jamais).

La fonction GetObjectIdentifierFromPersistentUniqueIdentifier dans le module ContentProperties. cpp illustre la récupération d’un identificateur d’objet pour un PUID donné.

Votre application peut récupérer un identificateur d’objet pour un PUID correspondant à l’aide des interfaces décrites dans le tableau suivant.



| Interface                                                                                      | Description                                                                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**Interface IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | Fournit l’accès à la méthode de récupération.                                                            |
| [**Interface IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) | Utilisé pour stocker l’identificateur d’objet et l’identificateur unique persistant (PUID) correspondant. |



 

La première tâche que l’exemple d’application effectue est d’obtenir un PUID auprès de l’utilisateur.


```C++
// Prompt user to enter an unique identifier to convert to an object idenifier.
printf("Enter the Persistant Unique Identifier of the object you wish to convert into an object identifier.\n>");
hr = StringCbGetsW(szSelection,sizeof(szSelection));
if (FAILED(hr))
{
    printf("An invalid persistent object identifier was specified, aborting the query operation\n");
}
```



Après cela, l’exemple d’application récupère un objet [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) , qu’il utilisera pour appeler la méthode [**GetObjectIDsFromPersistentUniqueIDs**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-getobjectidsfrompersistentuniqueids) .


```C++
if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}
```



Ensuite, il crée un objet [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) qui contiendra le PUID fourni par l’utilisateur.


```C++
hr = CoCreateInstance(CLSID_PortableDevicePropVariantCollection,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&pPersistentUniqueIDs));
```



Une fois les trois étapes précédentes effectuées, l’exemple est prêt à récupérer l’identificateur d’objet qui correspond au PUID fourni par l’utilisateur. Pour ce faire, vous devez appeler la méthode [**IPortableDeviceContent :: GetObjectIDsFromPersistentUniqueIDs**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-getobjectidsfrompersistentuniqueids) . Avant d’appeler cette méthode, l’exemple Initialise une structure PROPVARIANT, écrit le PUID fourni par l’utilisateur dans cette structure, puis l’ajoute à l’objet IPortableDevicePropVariantCollection à partir duquel pPersistentUniqueIDs pointe. Ce pointeur est passé comme premier argument à la méthode GetObjectIDsFromPersistentUniqueIDs. Le deuxième argument de GetObjectIDsFromPersistentUniqueIDs est un objet IPortableDevicePropVariantCollection qui reçoit l’identificateur d’objet correspondant.


```C++
if (SUCCEEDED(hr))
{
    if (pPersistentUniqueIDs != NULL)
    {
        PROPVARIANT pv = {0};
        PropVariantInit(&pv);

        // Initialize a PROPVARIANT structure with the object identifier string
        // that the user selected above. Notice we are allocating memory for the
        // PWSTR value.  This memory will be freed when PropVariantClear() is
        // called below.
        pv.vt      = VT_LPWSTR;
        pv.pwszVal = AtlAllocTaskWideString(szSelection);
        if (pv.pwszVal != NULL)
        {
            // Add the object identifier to the objects-to-delete list
            // (We are only deleting 1 in this example)
            hr = pPersistentUniqueIDs->Add(&pv);
            if (SUCCEEDED(hr))
            {
                // 3) Attempt to get the unique idenifier for the object from the device
                hr = pContent->GetObjectIDsFromPersistentUniqueIDs(pPersistentUniqueIDs,
                                                                   &pObjectIDs);
                if (SUCCEEDED(hr))
                {
                    PROPVARIANT pvId = {0};
                    hr = pObjectIDs->GetAt(0, &pvId);
                    if (SUCCEEDED(hr))
                    {
                        printf("The persistent unique identifier '%ws' relates to object identifier '%ws' on the device.\n", szSelection, pvId.pwszVal);
                    }
                    else
                    {
                        printf("! Failed to get the object identifier for '%ws' from the IPortableDevicePropVariantCollection, hr = 0x%lx\n",szSelection, hr);
                    }

                    // Free the returned allocated string from the GetAt() call
                    PropVariantClear(&pvId);
                }
                else
                {
                    printf("! Failed to get the object identifier from persistent object idenifier '%ws', hr = 0x%lx\n",szSelection, hr);
                }
            }
            else
            {
                printf("! Failed to get the object identifier from persistent object idenifier because we could no add the persistent object identifier string to the IPortableDevicePropVariantCollection, hr = 0x%lx\n",hr);
            }
        }
        else
        {
            hr = E_OUTOFMEMORY;
            printf("! Failed to get the object identifier because we could no allocate memory for the persistent object identifier string, hr = 0x%lx\n",hr);
        }

        // Free any allocated values in the PROPVARIANT before exiting
        PropVariantClear(&pv);
    }
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Interface IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**Interface IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**Guide de programmation**](programming-guide.md)
</dt> </dl>

 

 



