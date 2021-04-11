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
# <a name="using-logical-sensors"></a>Utilisation de capteurs logiques

Pour instancier un nœud d’appareil pour un capteur logique, ou pour se reconnecter à un nœud de périphérique de capteur logique existant, une application ou un service doit appeler [**ILogicalSensorManager :: Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)). Le paramètre *pPropertyStore* de cette méthode nécessite un pointeur vers une interface [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) qui contient les ID des pilotes de capteur auxquels se connecter. Cela signifie que vous devez créer une banque de propriétés et ajouter ces données au magasin avant d’appeler cette méthode.

### <a name="connecting-to-the-logical-sensor"></a>Connexion au capteur logique

Pour vous connecter à un capteur logique, vous devez spécifier, au minimum, un ID matériel, tel qu’il est défini dans le fichier. inf du pilote de capteur et un **GUID** logique qui identifie le capteur. La plateforme utilise ce **GUID** pour identifier le capteur lorsque vous choisissez de vous déconnecter d’un nœud de périphérique capteur ou de le désinstaller.

L’exemple de code suivant crée une méthode d’assistance qui se connecte à un capteur logique spécifié. Les paramètres de méthode reçoivent l’ID de matériel de capteur et un **GUID** unique pour identifier le capteur.


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



### <a name="disconnecting-from-a-logical-sensor"></a>Déconnexion d’un capteur logique

Pour vous déconnecter d’un capteur logique, vous devez fournir le même ID logique que celui que vous avez utilisé lorsque vous avez appelé [**Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)).

L’exemple de code suivant crée une fonction d’assistance qui se déconnecte d’un capteur logique.


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



### <a name="uninstalling-a-logical-sensor"></a>Désinstallation d’un capteur logique

Pour désinstaller un capteur logique, vous devez fournir le même ID logique que celui que vous avez utilisé lorsque vous avez appelé [**Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)).

L’exemple de code suivant crée une fonction d’assistance qui désinstalle un capteur logique.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos des capteurs logiques](about-logical-sensors.md)
</dt> </dl>

 

 
