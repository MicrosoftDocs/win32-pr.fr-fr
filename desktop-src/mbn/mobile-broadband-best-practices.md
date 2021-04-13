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
# <a name="mobile-broadband-api-best-practices"></a><span data-ttu-id="95b23-103">Meilleures pratiques pour l’API haut débit mobile</span><span class="sxs-lookup"><span data-stu-id="95b23-103">Mobile Broadband API Best Practices</span></span>

<span data-ttu-id="95b23-104">Lors de l’utilisation de l’API haut débit mobile, l’ensemble suivant de meilleures pratiques doit être utilisé pour obtenir les meilleures performances possibles.</span><span class="sxs-lookup"><span data-stu-id="95b23-104">When working with the Mobile Broadband API the following set of best practices should be used in order to achieve the best possible performance.</span></span>

## <a name="do-not-cache-functional-objects"></a><span data-ttu-id="95b23-105">Ne pas mettre en cache les objets fonctionnels</span><span class="sxs-lookup"><span data-stu-id="95b23-105">Do Not Cache Functional Objects</span></span>

<span data-ttu-id="95b23-106">Les objets fonctionnels, tels que [**IMbnInterface**](/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface) et d’autres, sont obtenus à partir d’objets Manager, tels que [**IMbnInterfaceManager**](/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfacemanager), à l’aide de la méthode d’énumération sur l’objet Manager correspondant.</span><span class="sxs-lookup"><span data-stu-id="95b23-106">Functional objects, such as [**IMbnInterface**](/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface) and others, are obtained from manager objects, like [**IMbnInterfaceManager**](/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfacemanager), using the enumeration method on the corresponding manager object.</span></span> <span data-ttu-id="95b23-107">Ne mettez pas en cache ces objets fonctionnels, car les objets fonctionnels mis en cache contiennent des données obsolètes.</span><span class="sxs-lookup"><span data-stu-id="95b23-107">Do not cache these functional objects, since cached functional objects contain stale data.</span></span> <span data-ttu-id="95b23-108">Les opérations synchrones effectuées sur ces objets fonctionnels retournent les mêmes données jusqu’à ce que les objets fonctionnels soient à nouveau obtenus.</span><span class="sxs-lookup"><span data-stu-id="95b23-108">The synchronous operations performed on these functional objects will return the same data until the functional objects are obtained again.</span></span>

<span data-ttu-id="95b23-109">Au lieu de cela, mettez en cache les objets de gestionnaire et récupérez les objets fonctionnels à partir de l’objet gestionnaire à l’aide de la méthode d’énumération sur l’objet gestionnaire correspondant pour obtenir les données les plus récentes.</span><span class="sxs-lookup"><span data-stu-id="95b23-109">Instead, cache the manager objects and obtain the functional objects from manager object using the enumeration method on the corresponding manager object again to get the latest data.</span></span>

<span data-ttu-id="95b23-110">L’exemple de code suivant illustre la manière appropriée de mettre en cache des objets de gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="95b23-110">The following code example demonstrates the proper way to cache manager objects.</span></span>


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



## <a name="handle-all-notifications"></a><span data-ttu-id="95b23-111">Gérer toutes les notifications</span><span class="sxs-lookup"><span data-stu-id="95b23-111">Handle All Notifications</span></span>

<span data-ttu-id="95b23-112">Suivez et Gérez toutes les notifications, même si elles ne sont pas déclenchées par votre application.</span><span class="sxs-lookup"><span data-stu-id="95b23-112">Follow and handle all notifications, even if they are not triggered by your application.</span></span> <span data-ttu-id="95b23-113">Cela est nécessaire pour maintenir la synchronisation de l’interface utilisateur avec l’état réel de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="95b23-113">This is required to keep the UI in sync with the actual state of the device.</span></span>

<span data-ttu-id="95b23-114">Il peut y avoir plus d’un gestionnaire de connexions en cours d’exécution sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="95b23-114">There can be more than one connection manager running on a computer.</span></span> <span data-ttu-id="95b23-115">L’interface utilisateur d’interface réseau disponible de l’affichage natif fournie par Windows 7 est un gestionnaire de connexions.</span><span class="sxs-lookup"><span data-stu-id="95b23-115">The native View Available Network Interface UI provided by Windows 7 is a connection manager.</span></span> <span data-ttu-id="95b23-116">Tous les autres gestionnaires de connexions doivent répondre à toutes les notifications pour rester dans la synchronisation de l’interface utilisateur native Windows.</span><span class="sxs-lookup"><span data-stu-id="95b23-116">Any other connection managers need to respond to all notifications to remain in sync the Windows native UI.</span></span> <span data-ttu-id="95b23-117">Un utilisateur peut choisir d’effectuer une opération sur l’un des gestionnaires de connexions, ce qui peut entraîner un changement d’état de l’appareil haut débit mobile.</span><span class="sxs-lookup"><span data-stu-id="95b23-117">A user may opt to perform some operation on one of the connection managers which may result in a state change of the Mobile Broadband device.</span></span> <span data-ttu-id="95b23-118">Toutefois, d’autres gestionnaires de connexions doivent rester mis à jour afin d’indiquer correctement l’état modifié de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="95b23-118">However, other connection managers need to remain updated in order to properly indicate the modified state of the device.</span></span>

<span data-ttu-id="95b23-119">Par exemple, si vous effectuez une connexion à l’aide de l’un des gestionnaires de connexions, l’état de l’appareil est modifié de disponible à connecté.</span><span class="sxs-lookup"><span data-stu-id="95b23-119">For example, performing a connect using one of the connection managers will change the state of the device from available to connected.</span></span> <span data-ttu-id="95b23-120">Cette modification doit être visible pour les gestionnaires de connexions qui n’ont pas initié cette action.</span><span class="sxs-lookup"><span data-stu-id="95b23-120">This change should be visible to the connection managers that didn’t initiate this action.</span></span> <span data-ttu-id="95b23-121">Tous les gestionnaires de connexions qui ont une interface utilisateur qui indique l’état de connexion de l’appareil, doivent écouter et gérer les notifications d’état de connexion afin de mettre correctement à jour leur interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="95b23-121">All connection managers that have UI that indicates the connection state of the device, need to listen to and handle the connection state notifications in order to properly update their user interface.</span></span>

## <a name="sending-and-receiving-bytes"></a><span data-ttu-id="95b23-122">Octets d’envoi et de réception</span><span class="sxs-lookup"><span data-stu-id="95b23-122">Sending And Receiving Bytes</span></span>

<span data-ttu-id="95b23-123">Utilisez les fonctions d’assistance IP [GetlfEntry](/windows/win32/api/iphlpapi/nf-iphlpapi-getifentry) et [GetlfEntry2](/windows/win32/api/netioapi/nf-netioapi-getifentry2) pour envoyer et recevoir des octets.</span><span class="sxs-lookup"><span data-stu-id="95b23-123">Use the IP Helper functions [GetlfEntry](/windows/win32/api/iphlpapi/nf-iphlpapi-getifentry) and [GetlfEntry2](/windows/win32/api/netioapi/nf-netioapi-getifentry2) to send and receive bytes.</span></span>

## <a name="using-the-pin-unblock-api"></a><span data-ttu-id="95b23-124">Utilisation de l’API débloquer le code confidentiel</span><span class="sxs-lookup"><span data-stu-id="95b23-124">Using The Pin Unblock API</span></span>

<span data-ttu-id="95b23-125">Une application cliente appelante doit être élevée pour pouvoir appeler [**IMbnPin :: Unblock**](/windows/desktop/api/mbnapi/nf-mbnapi-imbnpin-unblock).</span><span class="sxs-lookup"><span data-stu-id="95b23-125">A calling client application must be elevated in order to successfully to invoke [**IMbnPin::Unblock**](/windows/desktop/api/mbnapi/nf-mbnapi-imbnpin-unblock).</span></span> <span data-ttu-id="95b23-126">Cette méthode est la seule partie de l’API de haut débit mobile qui requiert des privilèges d’administrateur ou de NCO.</span><span class="sxs-lookup"><span data-stu-id="95b23-126">This method is the only portion of the Mobile Broadband API that requires administrator or NCO privileges.</span></span> <span data-ttu-id="95b23-127">Pour plus d’informations, consultez [la description du groupe opérateurs de configuration réseau]( https://support.microsoft.com/kb/297938/en-us) .</span><span class="sxs-lookup"><span data-stu-id="95b23-127">See [A Description of the Network Configuration Operators Group]( https://support.microsoft.com/kb/297938/en-us) for more information.</span></span>

## <a name="working-with-safearrays"></a><span data-ttu-id="95b23-128">Utilisation de SAFEARRAY</span><span class="sxs-lookup"><span data-stu-id="95b23-128">Working With SafeArrays</span></span>

-   <span data-ttu-id="95b23-129">Utilisez ZeroMemory () avant d’accéder à tous les éléments d’un SafeArray.</span><span class="sxs-lookup"><span data-stu-id="95b23-129">Use ZeroMemory() before accessing any elements in a SafeArray.</span></span>

-   <span data-ttu-id="95b23-130">Ne vérifie pas les index d’un SafeArray.</span><span class="sxs-lookup"><span data-stu-id="95b23-130">Don’t check on the indexes of a SafeArray.</span></span> <span data-ttu-id="95b23-131">Ils peuvent être négatifs.</span><span class="sxs-lookup"><span data-stu-id="95b23-131">They may be negative.</span></span>

<span data-ttu-id="95b23-132">L’exemple de code suivant montre comment gérer correctement un SafeArray.</span><span class="sxs-lookup"><span data-stu-id="95b23-132">The following code example shows how to properly handle a SafeArray.</span></span>


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



 

 
