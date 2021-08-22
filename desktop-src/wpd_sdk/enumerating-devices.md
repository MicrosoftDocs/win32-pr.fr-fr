---
title: Énumération des appareils (WPD)
description: Découvrez comment une application énumère les appareils à l’aide de la fonction EnumerateAllDevices, qui obtient le nombre d’appareils connectés et les informations spécifiques à l’appareil.
ms.assetid: 28ded3cf-b0c8-4c90-ab39-efc879adb6e7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6cfe1c1b4dee11383a4c36eaea43974f7e0439ae4ff2370a90e99b1702a8e0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083573"
---
# <a name="enumerating-devices-wpd"></a>Énumération des appareils (WPD)

La première tâche effectuée par la plupart des applications est l’énumération des appareils connectés à l’ordinateur. Cette tâche et la récupération des informations de l’appareil (telles que le fabricant, le nom convivial et la description) sont prises en charge par l’interface [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) .

La fonction EnumerateAllDevices dans le module DeviceEnumeration. cpp contient du code qui illustre la récupération du nombre d’appareils connectés et, une fois le nombre récupéré, la récupération des informations spécifiques à l’appareil pour chaque périphérique connecté.

La fonction EnumerateAllDevices effectue quatre tâches principales :

1.  Crée l’objet portable Device Manager.
2.  Récupère le nombre d’appareils connectés.
3.  Récupère les informations de l’appareil (pour les appareils connectés).
4.  Libère la mémoire utilisée lors de la récupération des informations de l’appareil.

Chacune de ces quatre tâches est décrite plus en détail dans les sections suivantes.

La première étape du processus d’énumération des appareils consiste à créer un objet portable Device Manager. Pour ce faire, appelez la fonction CoCreateInstance et passez l’identificateur de classe (CLSID) de l’objet, en spécifiant le contexte dans lequel le code s’exécutera, en spécifiant un identificateur de référence pour l’interface IPortableDeviceManager, puis en fournissant une variable pointeur qui reçoit le pointeur d’interface IPortableDeviceManager.


```C++
HRESULT hr = CoCreateInstance(CLSID_PortableDeviceManager,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&pPortableDeviceManager));
if (FAILED(hr))
{
    printf("! Failed to CoCreateInstance CLSID_PortableDeviceManager, hr = 0x%lx\n",hr);
}
```



Une fois que vous obtenez un pointeur d’interface [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) , vous pouvez commencer à appeler des méthodes sur cette interface. La première méthode appelée dans la fonction EnumerateAllDevices est [**IPortableDeviceManager :: GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices). Lorsque cette méthode est appelée avec le premier argument ayant la valeur **null**, elle retourne le nombre d’appareils connectés.


```C++
if (SUCCEEDED(hr))
{
    hr = pPortableDeviceManager->GetDevices(NULL, &cPnPDeviceIDs);
    if (FAILED(hr))
    {
        printf("! Failed to get number of devices on the system, hr = 0x%lx\n",hr);
    }
}

// Report the number of devices found.  NOTE: we will report 0, if an error
// occured.

printf("\n%d Windows Portable Device(s) found on the system\n\n", cPnPDeviceIDs);
```



Une fois que vous avez récupéré le nombre d’appareils connectés, vous pouvez utiliser cette valeur pour récupérer les informations de chaque appareil connecté. Ce processus commence par passer un tableau de pointeurs de chaîne comme premier argument et le nombre d’éléments que ce tableau peut conserver comme deuxième argument (ce nombre doit être au moins égal au nombre d’appareils disponibles).

Les chaînes retournées par cette méthode sont les noms Plug-and-Play des appareils connectés. Ces noms, à leur tour, sont passés à d’autres méthodes sur l’interface [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) pour récupérer des informations spécifiques à l’appareil, telles que le nom convivial, le nom du fabricant et la description de l’appareil. (Ces noms sont également utilisés pour ouvrir une connexion à l’appareil quand une application appelle la méthode [**IPortableDevice :: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) .)


```C++
if (SUCCEEDED(hr) && (cPnPDeviceIDs > 0))
{
    pPnpDeviceIDs = new (std::nothrow) PWSTR[cPnPDeviceIDs];
    if (pPnpDeviceIDs != NULL)
    {
        DWORD dwIndex = 0;

        hr = pPortableDeviceManager->GetDevices(pPnpDeviceIDs, &cPnPDeviceIDs);
        if (SUCCEEDED(hr))
        {
            // For each device found, display the devices friendly name,
            // manufacturer, and description strings.
            for (dwIndex = 0; dwIndex < cPnPDeviceIDs; dwIndex++)
            {
                printf("[%d] ", dwIndex);
                DisplayFriendlyName(pPortableDeviceManager, pPnpDeviceIDs[dwIndex]);
                printf("    ");
                DisplayManufacturer(pPortableDeviceManager, pPnpDeviceIDs[dwIndex]);
                printf("    ");
                DisplayDescription(pPortableDeviceManager, pPnpDeviceIDs[dwIndex]);
            }
        }
        else
        {
            printf("! Failed to get the device list from the system, hr = 0x%lx\n",hr);
        }
```



Une fois que vous avez récupéré les informations de l’appareil, vous devrez libérer la mémoire associée aux chaînes pointées par le tableau de pointeurs de chaîne. Vous devrez également supprimer ce tableau.


```C++
for (dwIndex = 0; dwIndex < cPnPDeviceIDs; dwIndex++)
{
    CoTaskMemFree(pPnpDeviceIDs[dwIndex]);
    pPnpDeviceIDs[dwIndex] = NULL;
}

// Delete the array of PWSTR pointers
delete [] pPnpDeviceIDs;
pPnpDeviceIDs = NULL;
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager)
</dt> <dt>

[**Guide de programmation**](programming-guide.md)
</dt> </dl>

 

 



