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
# <a name="describing-devices"></a>Description des appareils

Il existe deux façons d’obtenir des objets d’appareil :

-   À l’aide de l’interface [**IUPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument) . L’interface **IUPnPDescriptionDocument** est la seule interface sécurisée pour les scripts.
-   Utilisation de l’interface [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) pour obtenir une interface [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) .

Les deux méthodes retournent des collections d’appareils. Les applications utilisent ensuite les méthodes d’appareil pour récupérer les propriétés des appareils.

Les applications sont en mesure de récupérer les types d’informations suivants :

-   Informations sur la hiérarchie des appareils, y compris les périphériques racine, les périphériques parents et les périphériques enfants.
-   Propriétés de l’appareil, y compris UDNs, les URI (Uniform Resource Identifiers) et les noms lisibles par l’utilisateur.
-   Informations sur le fabricant, y compris les noms et les pages Web associées.
-   Informations sur le modèle, y compris le nom, le nombre, le UPC, les numéros de série et les descriptions des appareils.
-   Affichez des informations, y compris l’URL pour contrôler l’appareil et les URL à partir desquelles les icônes sont téléchargées.
-   Services fournis par un appareil particulier.

Les applications obtiennent également l’URL du document de description de l’appareil à l’aide de l’interface [**IUPnPDeviceDocumentAccess**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicedocumentaccess) . L’application charge ensuite le document de description et travaille avec les propriétés de l’appareil et du service qui ne sont pas exposées par l’interface [**IUPnPDevice**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevice) . Cette interface ne peut pas être utilisée dans les scripts, car il ne s’agit pas de l’interface par défaut.

## <a name="visual-basic-example"></a>Exemple de Visual Basic

L’exemple de code suivant illustre l’utilisation de [**IUPnPDeviceDocumentAccess :: GetDocumentURL**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicedocumentaccess-getdocumenturl).


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



## <a name="c-example"></a>Exemple C++

L’exemple de code suivant illustre l’utilisation de [**IUPnPDeviceDocumentAccess :: GetDocumentURL**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicedocumentaccess-getdocumenturl).


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



 

 




