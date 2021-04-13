---
description: Lors de l’utilisation de l’API haut débit mobile, l’ensemble suivant de meilleures pratiques doit être utilisé pour obtenir les meilleures performances possibles.
ms.assetid: 523e3ea4-1d4e-45d1-bc24-93aa2fb14390
title: Meilleures pratiques pour l’API haut débit mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 399c2ebc40a357eac9686bc3c2c9f471e3b853f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201539"
---
# <a name="mobile-broadband-api-best-practices"></a>Meilleures pratiques pour l’API haut débit mobile

Lors de l’utilisation de l’API haut débit mobile, l’ensemble suivant de meilleures pratiques doit être utilisé pour obtenir les meilleures performances possibles.

## <a name="do-not-cache-functional-objects"></a>Ne pas mettre en cache les objets fonctionnels

Les objets fonctionnels, tels que [**IMbnInterface**](/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface) et d’autres, sont obtenus à partir d’objets Manager, tels que [**IMbnInterfaceManager**](/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfacemanager), à l’aide de la méthode d’énumération sur l’objet Manager correspondant. Ne mettez pas en cache ces objets fonctionnels, car les objets fonctionnels mis en cache contiennent des données obsolètes. Les opérations synchrones effectuées sur ces objets fonctionnels retournent les mêmes données jusqu’à ce que les objets fonctionnels soient à nouveau obtenus.

Au lieu de cela, mettez en cache les objets de gestionnaire et récupérez les objets fonctionnels à partir de l’objet gestionnaire à l’aide de la méthode d’énumération sur l’objet gestionnaire correspondant pour obtenir les données les plus récentes.

L’exemple de code suivant illustre la manière appropriée de mettre en cache des objets de gestionnaire.


```C++
#include <atlbase.h>
#include "mbnapi.h"
#include <tchar.h>

int main()
{
    HRESULT hr = E_FAIL;
    int returnVal = 0;

    do
    {
        hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);    
        if (FAILED(hr))
        {
            returnVal = hr; 
            break;
        }

        CComPtr<IMbnInterfaceManager>  g_InterfaceMgr = NULL;

        //Do the below once(cache the manager objects)
        hr = CoCreateInstance(CLSID_MbnInterfaceManager,
            NULL, 
            CLSCTX_ALL, 
            IID_IMbnInterfaceManager, 
            (void**)&g_InterfaceMgr);
        if (FAILED(hr))
        {
            returnVal = hr; 
            break;
        }

        SAFEARRAY *psa = NULL;

        //Do the below each time(do not cache functional objects)
        hr = g_InterfaceMgr->GetInterfaces(&psa);
        if (FAILED(hr))
        {
            returnVal = hr; 
            break;
        }

        LONG lLower;
        LONG lUpper;

        hr = SafeArrayGetLBound(psa, 1, &lLower);
        if (FAILED(hr))
        {
            returnVal = hr; 
            break;
        }

        hr = SafeArrayGetUBound(psa, 1, &lUpper);
        if (FAILED(hr))
        {
            returnVal = hr; 
            break;
        }

        CComPtr<IMbnInterface>  pInf = NULL;
        MBN_READY_STATE readyState;

        for (LONG l = lLower; l <= lUpper; l++)
        {
            hr = SafeArrayGetElement(psa, &l, (void*)(&pInf));
            if (FAILED(hr))
            {
                returnVal = hr; 
                break;
            }

            hr = pInf->GetReadyState(&readyState);
            if (FAILED(hr))
            {
                returnVal = hr; 
                break;
            }

            _tprintf(_T("Ready State = %d"), readyState); 
        }

        if (FAILED(hr))
        {
            break;
        }
    } while (FALSE);


    CoUninitialize();
    return returnVal;
}
```



## <a name="handle-all-notifications"></a>Gérer toutes les notifications

Suivez et Gérez toutes les notifications, même si elles ne sont pas déclenchées par votre application. Cela est nécessaire pour maintenir la synchronisation de l’interface utilisateur avec l’état réel de l’appareil.

Il peut y avoir plus d’un gestionnaire de connexions en cours d’exécution sur un ordinateur. L’interface utilisateur d’interface réseau disponible de l’affichage natif fournie par Windows 7 est un gestionnaire de connexions. Tous les autres gestionnaires de connexions doivent répondre à toutes les notifications pour rester dans la synchronisation de l’interface utilisateur native Windows. Un utilisateur peut choisir d’effectuer une opération sur l’un des gestionnaires de connexions, ce qui peut entraîner un changement d’état de l’appareil haut débit mobile. Toutefois, d’autres gestionnaires de connexions doivent rester mis à jour afin d’indiquer correctement l’état modifié de l’appareil.

Par exemple, si vous effectuez une connexion à l’aide de l’un des gestionnaires de connexions, l’état de l’appareil est modifié de disponible à connecté. Cette modification doit être visible pour les gestionnaires de connexions qui n’ont pas initié cette action. Tous les gestionnaires de connexions qui ont une interface utilisateur qui indique l’état de connexion de l’appareil, doivent écouter et gérer les notifications d’état de connexion afin de mettre correctement à jour leur interface utilisateur.

## <a name="sending-and-receiving-bytes"></a>Octets d’envoi et de réception

Utilisez les fonctions d’assistance IP [GetlfEntry](/windows/win32/api/iphlpapi/nf-iphlpapi-getifentry) et [GetlfEntry2](/windows/win32/api/netioapi/nf-netioapi-getifentry2) pour envoyer et recevoir des octets.

## <a name="using-the-pin-unblock-api"></a>Utilisation de l’API débloquer le code confidentiel

Une application cliente appelante doit être élevée pour pouvoir appeler [**IMbnPin :: Unblock**](/windows/desktop/api/mbnapi/nf-mbnapi-imbnpin-unblock). Cette méthode est la seule partie de l’API de haut débit mobile qui requiert des privilèges d’administrateur ou de NCO. Pour plus d’informations, consultez [la description du groupe opérateurs de configuration réseau]( https://support.microsoft.com/kb/297938/en-us) .

## <a name="working-with-safearrays"></a>Utilisation de SAFEARRAY

-   Utilisez ZeroMemory () avant d’accéder à tous les éléments d’un SafeArray.

-   Ne vérifie pas les index d’un SafeArray. Ils peuvent être négatifs.

L’exemple de code suivant montre comment gérer correctement un SafeArray.


```C++
#include <atlbase.h>
#include "mbnapi.h"

void CreateVisibleProviderList(LPCWSTR interfaceID)
{
    CComPtr<IMbnInterfaceManager>  g_InterfaceMgr = NULL;
    SAFEARRAY *visibleProviders = NULL;
    long visibleLower = 0;
    long visibleUpper = 0;
    MBN_PROVIDER *pProvider = NULL;
    CComPtr<IMbnInterface> pInterface = NULL;

    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);

    if (FAILED(hr))
    {
        goto ERROR_0;
    }

    hr = CoCreateInstance(CLSID_MbnInterfaceManager,
            NULL, 
            CLSCTX_ALL, 
            IID_IMbnInterfaceManager, 
            (void**)&g_InterfaceMgr);
    
    if (FAILED(hr))
    {
        goto ERROR_0;
    }

    hr = g_InterfaceMgr->GetInterface(interfaceID, & pInterface);
    if (FAILED(hr)) 
    {
        goto ERROR_0;
    }

    ULONG age;

    hr = pInterface->GetVisibleProviders(&age, &visibleProviders);
    if (FAILED(hr)) 
    {
        goto ERROR_0;
    }

    hr = SafeArrayGetLBound(visibleProviders, 1, &visibleLower);
    if (FAILED(hr)) 
    {
        goto ERROR_0;
    }

    hr = SafeArrayGetUBound(visibleProviders, 1, &visibleUpper);
    if (FAILED(hr)) 
    {
        goto ERROR_0;
    }

    //don't check on the indexes of safearray to be positive
    if (visibleLower > visibleUpper) 
    {
        // There are no visible providers in this case.
        hr = HRESULT_FROM_WIN32(ERROR_NOT_FOUND);
        goto ERROR_0;
    }

    DWORD size = (visibleUpper - visibleLower + 1) * sizeof(BOOL);
    DBG_UNREFERENCED_LOCAL_VARIABLE(size); 
    
    pProvider = (MBN_PROVIDER *)CoTaskMemAlloc(sizeof(MBN_PROVIDER));
    if (!pProvider) 
    {
        hr = E_OUTOFMEMORY;
        goto ERROR_0;
    }

    for (LONG vIndex = visibleLower; vIndex <= visibleUpper; vIndex++) 
    {
        //use zeromemory before accessing any elements in a safearray
        ZeroMemory(pProvider, sizeof(MBN_PROVIDER));
        hr = SafeArrayGetElement(visibleProviders, &vIndex, (void *)pProvider);
        if (FAILED(hr)) 
        {
            continue;
        }
    }

ERROR_0:
    if (visibleProviders) 
    {
        SafeArrayDestroy(visibleProviders);
        visibleProviders = NULL;
    }

    CoUninitialize();
}
```



 

 
