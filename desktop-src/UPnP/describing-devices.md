---
title: Description des appareils
description: Il existe deux façons d’obtenir des objets d’appareil.
ms.assetid: a83fbf21-586e-4b92-9875-476d820c377d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5abc84f15f6b52328585e05abfd95503087124b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840529"
---
# <a name="describing-devices"></a><span data-ttu-id="58c6c-103">Description des appareils</span><span class="sxs-lookup"><span data-stu-id="58c6c-103">Describing Devices</span></span>

<span data-ttu-id="58c6c-104">Il existe deux façons d’obtenir des objets d’appareil :</span><span class="sxs-lookup"><span data-stu-id="58c6c-104">There are two ways to obtain device objects:</span></span>

-   <span data-ttu-id="58c6c-105">À l’aide de l’interface [**IUPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument) .</span><span class="sxs-lookup"><span data-stu-id="58c6c-105">Using the [**IUPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument) interface.</span></span> <span data-ttu-id="58c6c-106">L’interface **IUPnPDescriptionDocument** est la seule interface sécurisée pour les scripts.</span><span class="sxs-lookup"><span data-stu-id="58c6c-106">The **IUPnPDescriptionDocument** interface is the only interface that is safe for scripting.</span></span>
-   <span data-ttu-id="58c6c-107">Utilisation de l’interface [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) pour obtenir une interface [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) .</span><span class="sxs-lookup"><span data-stu-id="58c6c-107">Using the [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) interface to obtain an [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) interface.</span></span>

<span data-ttu-id="58c6c-108">Les deux méthodes retournent des collections d’appareils.</span><span class="sxs-lookup"><span data-stu-id="58c6c-108">Both methods return Devices collections.</span></span> <span data-ttu-id="58c6c-109">Les applications utilisent ensuite les méthodes d’appareil pour récupérer les propriétés des appareils.</span><span class="sxs-lookup"><span data-stu-id="58c6c-109">Applications then use the Device methods to retrieve properties about devices.</span></span>

<span data-ttu-id="58c6c-110">Les applications sont en mesure de récupérer les types d’informations suivants :</span><span class="sxs-lookup"><span data-stu-id="58c6c-110">Applications are able to retrieve the following types of information:</span></span>

-   <span data-ttu-id="58c6c-111">Informations sur la hiérarchie des appareils, y compris les périphériques racine, les périphériques parents et les périphériques enfants.</span><span class="sxs-lookup"><span data-stu-id="58c6c-111">Device hierarchy information, including root devices, parent devices, and child devices.</span></span>
-   <span data-ttu-id="58c6c-112">Propriétés de l’appareil, y compris UDNs, les URI (Uniform Resource Identifiers) et les noms lisibles par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="58c6c-112">Device properties, including UDNs, uniform resource identifiers (URIs), and user-readable names.</span></span>
-   <span data-ttu-id="58c6c-113">Informations sur le fabricant, y compris les noms et les pages Web associées.</span><span class="sxs-lookup"><span data-stu-id="58c6c-113">Manufacturer information, including names and related Web pages.</span></span>
-   <span data-ttu-id="58c6c-114">Informations sur le modèle, y compris le nom, le nombre, le UPC, les numéros de série et les descriptions des appareils.</span><span class="sxs-lookup"><span data-stu-id="58c6c-114">Model information, including the name, number, UPC, serial numbers and device descriptions.</span></span>
-   <span data-ttu-id="58c6c-115">Affichez des informations, y compris l’URL pour contrôler l’appareil et les URL à partir desquelles les icônes sont téléchargées.</span><span class="sxs-lookup"><span data-stu-id="58c6c-115">Display information, including the URL to control the device, and URLs from which icons are downloaded.</span></span>
-   <span data-ttu-id="58c6c-116">Services fournis par un appareil particulier.</span><span class="sxs-lookup"><span data-stu-id="58c6c-116">Services provided by a particular device.</span></span>

<span data-ttu-id="58c6c-117">Les applications obtiennent également l’URL du document de description de l’appareil à l’aide de l’interface [**IUPnPDeviceDocumentAccess**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicedocumentaccess) .</span><span class="sxs-lookup"><span data-stu-id="58c6c-117">Applications also obtain the URL of the device description document using the [**IUPnPDeviceDocumentAccess**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicedocumentaccess) interface.</span></span> <span data-ttu-id="58c6c-118">L’application charge ensuite le document de description et travaille avec les propriétés de l’appareil et du service qui ne sont pas exposées par l’interface [**IUPnPDevice**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevice) .</span><span class="sxs-lookup"><span data-stu-id="58c6c-118">The application then load the description document and work with device and service properties that are not exposed by the [**IUPnPDevice**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevice) interface.</span></span> <span data-ttu-id="58c6c-119">Cette interface ne peut pas être utilisée dans les scripts, car il ne s’agit pas de l’interface par défaut.</span><span class="sxs-lookup"><span data-stu-id="58c6c-119">This interface cannot be used in scripting, because it is not the default interface.</span></span>

## <a name="visual-basic-example"></a><span data-ttu-id="58c6c-120">Exemple de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="58c6c-120">Visual Basic Example</span></span>

<span data-ttu-id="58c6c-121">L’exemple de code suivant illustre l’utilisation de [**IUPnPDeviceDocumentAccess :: GetDocumentURL**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicedocumentaccess-getdocumenturl).</span><span class="sxs-lookup"><span data-stu-id="58c6c-121">The following sample code shows the usage of [**IUPnPDeviceDocumentAccess::GetDocumentURL**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicedocumentaccess-getdocumenturl).</span></span>


```VB
Sub GetDocumentURL()
Dim pDescDoc As IUPnPDeviceDocumentAccess
Dim strDescDocURL As String

'currentDevice is UPnPDevice object containing the current UPnP Device 
'We are trying to get IUPnPDeviceDocumentAccess interface in the UPnP Device object
Set pDescDoc = currentDevice

If Not (pDescDoc is Nothing) Then
  'Description Document URL is got from device
  strDescDocURL = pDescDoc.GetDocumentURL 
End If
```



## <a name="c-example"></a><span data-ttu-id="58c6c-122">Exemple C++</span><span class="sxs-lookup"><span data-stu-id="58c6c-122">C++ Example</span></span>

<span data-ttu-id="58c6c-123">L’exemple de code suivant illustre l’utilisation de [**IUPnPDeviceDocumentAccess :: GetDocumentURL**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicedocumentaccess-getdocumenturl).</span><span class="sxs-lookup"><span data-stu-id="58c6c-123">The following sample code shows the usage of [**IUPnPDeviceDocumentAccess::GetDocumentURL**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicedocumentaccess-getdocumenturl).</span></span>


```C++
#include <windows.h>
#include <upnp.h>
#include <stdio.h>

#pragma comment(lib, "ole32.lib")
#pragma comment(lib, "oleaut32.lib")

int GetDeviceDocumentUrl () 
{
  HRESULT hr = S_OK;
  // List of interfaces needed
  IUPnPDeviceFinder *pDevFinder=NULL;
  IUPnPDevice *pDevice =NULL;
  IUPnPDeviceDocumentAccess* pDeviceDocument=NULL;
  BSTR bstrDeviceUDN =NULL;
  BSTR bstrDeviceDocumentURL = NULL; 

  bstrDeviceUDN = SysAllocString(L"uuid:234324234324");
  if(bstrDeviceUDN == NULL){
    printf("ERROR: Could not allocate memory\n");
    return -1;
  }  

  //CoInitialize the program so that we can create COM objects
  CoInitializeEx(NULL, COINIT_MULTITHREADED);

  //now try to instantiate the DeviceFinder object
  hr = CoCreateInstance(  CLSID_UPnPDeviceFinder, 
              NULL,
              CLSCTX_INPROC_SERVER,
              IID_IUPnPDeviceFinder,
              (LPVOID *) &pDevFinder); 

  if(!SUCCEEDED(hr)){
    printf("\nERROR: CoCreateInstance on IUPnPDeviceFinder returned HRESULT %x",hr);
    goto cleanup;
  }

  printf("\nGot a pointer to the IUPnPDeviceFinder Interface");

  printf("\n Finding the device of given UDN\n");
  hr =pDevFinder->FindByUDN(bstrDeviceUDN, &pDevice);
  if(hr!=S_OK)
  {
    printf("\nERROR: FindByUDN for %S returned HRESULT %x", bstrDeviceUDN, hr);
    goto cleanup;
  }

  printf("\n\tFindByUDN for device of UDN %S succeeded", bstrDeviceUDN);
  //Now query pDevice for IUPnPDeviceDocumentAccess
  hr = pDevice->QueryInterface(IID_IUPnPDeviceDocumentAccess, (VOID **)&pDeviceDocument);
  if(SUCCEEDED(hr)){
    // We have got a pointer to the IUPnPDeviceDocumentAccess interface.
    // GetDocumentURL is available only in Windows XP. 
    hr = pDeviceDocument->GetDocumentURL(&bstrDeviceDocumentURL);
    if(SUCCEEDED(hr))
      printf("\nThe Device Document URL is %S \n", bstrDeviceDocumentURL);
  }
    
cleanup:
  //release references to all interfaces 
  if(pDevFinder)
    pDevFinder->Release();
  if(pDevice)
    pDevice->Release();
  if(pDeviceDocument)
    pDeviceDocument->Release();
  
  // Free the bstr strings
  if(bstrDeviceDocumentURL)
    SysFreeString(bstrDeviceDocumentURL);
  if(bstrDeviceUDN)
    SysFreeString(bstrDeviceUDN);
  CoUninitialize();
  return 0;
}
```



 

 




