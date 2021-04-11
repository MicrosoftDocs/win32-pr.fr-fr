---
description: Utilisation de capteurs logiques
ms.assetid: 97f4c44e-27dd-4f2a-b987-060bb2d9bc00
title: Utilisation de capteurs logiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb0493cfe8ff3a489e926792f9a101eb5d9db6b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112622"
---
# <a name="using-logical-sensors"></a><span data-ttu-id="5853f-103">Utilisation de capteurs logiques</span><span class="sxs-lookup"><span data-stu-id="5853f-103">Using Logical Sensors</span></span>

<span data-ttu-id="5853f-104">Pour instancier un nœud d’appareil pour un capteur logique, ou pour se reconnecter à un nœud de périphérique de capteur logique existant, une application ou un service doit appeler [**ILogicalSensorManager :: Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5853f-104">To instantiate a device node for a logical sensor, or to reconnect to an existing logical sensor device node, an application or service must call [**ILogicalSensorManager::Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)).</span></span> <span data-ttu-id="5853f-105">Le paramètre *pPropertyStore* de cette méthode nécessite un pointeur vers une interface [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) qui contient les ID des pilotes de capteur auxquels se connecter.</span><span class="sxs-lookup"><span data-stu-id="5853f-105">The *pPropertyStore* parameter for this method requires a pointer to an [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface that contains the IDs for the sensor drivers to connect to.</span></span> <span data-ttu-id="5853f-106">Cela signifie que vous devez créer une banque de propriétés et ajouter ces données au magasin avant d’appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="5853f-106">This means that you must create a property store and add this data to the store before calling this method.</span></span>

### <a name="connecting-to-the-logical-sensor"></a><span data-ttu-id="5853f-107">Connexion au capteur logique</span><span class="sxs-lookup"><span data-stu-id="5853f-107">Connecting to the Logical Sensor</span></span>

<span data-ttu-id="5853f-108">Pour vous connecter à un capteur logique, vous devez spécifier, au minimum, un ID matériel, tel qu’il est défini dans le fichier. inf du pilote de capteur et un **GUID** logique qui identifie le capteur.</span><span class="sxs-lookup"><span data-stu-id="5853f-108">To connect to a logical sensor, you must provide, at a minimum, a hardware ID, as defined in the sensor driver's .inf file, and a logical **GUID** that identifies the sensor.</span></span> <span data-ttu-id="5853f-109">La plateforme utilise ce **GUID** pour identifier le capteur lorsque vous choisissez de vous déconnecter d’un nœud de périphérique capteur ou de le désinstaller.</span><span class="sxs-lookup"><span data-stu-id="5853f-109">The platform uses this **GUID** to identify the sensor when you choose to disconnect from, or uninstall, the sensor device node.</span></span>

<span data-ttu-id="5853f-110">L’exemple de code suivant crée une méthode d’assistance qui se connecte à un capteur logique spécifié.</span><span class="sxs-lookup"><span data-stu-id="5853f-110">The following example code creates a helper method that connects to a specified logical sensor.</span></span> <span data-ttu-id="5853f-111">Les paramètres de méthode reçoivent l’ID de matériel de capteur et un **GUID** unique pour identifier le capteur.</span><span class="sxs-lookup"><span data-stu-id="5853f-111">The method parameters receive the sensor hardware ID and a unique **GUID** to identify the sensor.</span></span>


```C++
HRESULT ConnectToLogicalSensor(PCWSTR* wszHardwareID, GUID guidLogicalID)
{
    HRESULT hr = S_OK;
    
    ILogicalSensorManager* pLSM = NULL;
    IPropertyStore* pStore = NULL;
    PROPVARIANT pv = {};

    // Create the property store.
    hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&pStore));

    if(SUCCEEDED(hr))
    {
        // Create the logical sensor manager.
        hr = CoCreateInstance(CLSID_LogicalSensorManager, 
                                NULL, 
                                CLSCTX_INPROC_SERVER, 
                                IID_PPV_ARGS(&pLSM));
    }

    // Fill in the values.
    if(SUCCEEDED(hr))
    {
        hr = InitPropVariantFromStringVector(wszHardwareID, 1, &pv);
    }

    if(SUCCEEDED(hr))
    {
        hr = pStore->SetValue(PKEY_Device_HardwareIds, pv);
    }

    if(SUCCEEDED(hr))
    {
        hr = pStore->SetValue(PKEY_Device_CompatibleIds, pv);
    }

    if(SUCCEEDED(hr))
    {
        // Connect to the logical sensor.
        hr = pLSM->Connect(guidLogicalID, pStore);
    }

    SafeRelease(&pStore);
    SafeRelease(&pLSM);

    return hr;
}
```



### <a name="disconnecting-from-a-logical-sensor"></a><span data-ttu-id="5853f-112">Déconnexion d’un capteur logique</span><span class="sxs-lookup"><span data-stu-id="5853f-112">Disconnecting from a Logical Sensor</span></span>

<span data-ttu-id="5853f-113">Pour vous déconnecter d’un capteur logique, vous devez fournir le même ID logique que celui que vous avez utilisé lorsque vous avez appelé [**Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5853f-113">To disconnect from a logical sensor, you must provide the same logical ID that you used when you called [**Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)).</span></span>

<span data-ttu-id="5853f-114">L’exemple de code suivant crée une fonction d’assistance qui se déconnecte d’un capteur logique.</span><span class="sxs-lookup"><span data-stu-id="5853f-114">The following example code creates a helper function that disconnects from a logical sensor.</span></span>


```C++
HRESULT DisconnectFromLogicalSensor(GUID guidLogicalID)
{
    HRESULT hr = S_OK;

    ILogicalSensorManager* pLSM = NULL;
 
    if(SUCCEEDED(hr))
    {
        // Create the logical sensor manager.
        hr = CoCreateInstance(CLSID_LogicalSensorManager, 
                                NULL, 
                                CLSCTX_INPROC_SERVER, 
                                IID_PPV_ARGS(&pLSM));
    }

    if(SUCCEEDED(hr))
    {
        hr = pLSM->Disconnect(guidLogicalID);
    }

    SafeRelease(&pLSM);

    return hr;
}
```



### <a name="uninstalling-a-logical-sensor"></a><span data-ttu-id="5853f-115">Désinstallation d’un capteur logique</span><span class="sxs-lookup"><span data-stu-id="5853f-115">Uninstalling a Logical Sensor</span></span>

<span data-ttu-id="5853f-116">Pour désinstaller un capteur logique, vous devez fournir le même ID logique que celui que vous avez utilisé lorsque vous avez appelé [**Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5853f-116">To uninstall a logical sensor, you must provide the same logical ID that you used when you called [**Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)).</span></span>

<span data-ttu-id="5853f-117">L’exemple de code suivant crée une fonction d’assistance qui désinstalle un capteur logique.</span><span class="sxs-lookup"><span data-stu-id="5853f-117">The following example code creates a helper function that uninstalls a logical sensor.</span></span>


```C++
HRESULT UninstallLogicalSensor(REFGUID guidLogicalID)
{
    HRESULT hr = S_OK;

    ILogicalSensorManager* pLSM;
 
    // Create the logical sensor manager.
    hr = CoCreateInstance(CLSID_LogicalSensorManager, 
                            NULL, 
                            CLSCTX_INPROC_SERVER, 
                            IID_PPV_ARGS(&pLSM));
 
    if(SUCCEEDED(hr))
    {
        hr = pLSM->Uninstall(guidLogicalID);
    }

    SafeRelease(&pLSM);

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="5853f-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5853f-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5853f-119">À propos des capteurs logiques</span><span class="sxs-lookup"><span data-stu-id="5853f-119">About Logical Sensors</span></span>](about-logical-sensors.md)
</dt> </dl>

 

 
