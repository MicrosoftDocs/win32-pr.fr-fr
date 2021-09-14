---
title: Récupération des attributs de l’appareil
description: Récupération des attributs de l’appareil
ms.assetid: c553d495-d8fc-4483-a3dc-6679c6b9d1f1
keywords:
- Lecteur Windows Media, appareils mobiles
- modèle objet Lecteur Windows Media, appareils mobiles
- modèle objet, appareils mobiles
- contrôle de ActiveX Lecteur Windows Media, appareils mobiles
- contrôle de ActiveX, appareils mobiles
- Lecteur Windows Media contrôle Mobile ActiveX, appareils mobiles
- Lecteur Windows Media Mobile, appareils mobiles
- périphériques portables, récupération d’attributs
- attributs, appareils mobiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f486b94fe6a9a5c78f238d78a7f79dec9df3376
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416190"
---
# <a name="retrieving-device-attributes"></a>Récupération des attributs de l’appareil

Lecteur Windows Media stocke des informations sur les appareils qui se sont connectés au lecteur. Certains attributs sont disponibles en appelant des méthodes individuelles de **IWMPSyncDevice**, certaines peuvent être récupérées à l’aide de **IWMPSyncDevice :: getItemInfo**, et certaines peuvent être récupérées à l’aide de l’une ou l’autre technique.

L’exemple de code suivant remplit un contrôle de zone de liste avec les attributs disponibles pour l’appareil spécifié. La première partie de la fonction récupère les propriétés disponibles à l’aide de méthodes spécifiques. La deuxième partie de la fonction récupère les valeurs d’attribut à l’aide de **IWMPSyncDevice :: getItemInfo**. Le paramètre de fonction, *Lindex*, est l’index de l’appareil dans votre tableau d’appareils personnalisé pointé par m \_ ppWMPDevices.


```C++
STDMETHODIMP CMainDlg::ShowDeviceAttributes(long lIndex)
{
    HRESULT hr = S_OK;

    if(!m_ppWMPDevices)
        return S_FALSE;

    // Array of attribute names for devices.
    const TCHAR *szDeviceAttributeNames[16] = {
    _T("Connected"),
    _T("FreeSpace"),
    _T("FriendlyName"),
    _T("LastSyncErrorCount"),
    _T("LastSyncNoFitCount"),
    _T("LastSyncTime"),
    _T("Name"),
    _T("SerialNumber"),
    _T("SupportsAudio"),
    _T("SupportsPhoto"),
    _T("SupportsVideo"),
    _T("SyncIndex"),
    _T("SyncItemCount"),
    _T("SyncPercentComplete"),
    _T("SyncRelationship"),
    _T("TotalSpace")};
    
    // Array of device status strings.
    static const TCHAR *szDeviceStatus[6] = {
    _T("Unknown"),
    _T("Partnership exists"),
    _T("Partnership declined by the user"),
    _T("Partnership with another computer or user"),
    _T("Device only supports manual transfer"),
    _T("New device")};

    // Handle to the list box that displays the information.
    HWND hwndStats = GetDlgItem(IDC_STATS);
    CComBSTR bstrStatistics;  // Contains the display string for each property.
    CComBSTR bstrTemp; // Contains the retrieved value for each property.
    // Retrieve a pointer to the current device.
    CComPtr<IWMPSyncDevice> spDevice(m_ppWMPDevices[GetSelectedDeviceIndex()]);
    VARIANT_BOOL vbIsConnected = VARIANT_FALSE;
    WMPDeviceStatus  wmpDS = wmpdsUnknown;
    
    SendMessage(hwndStats, LB_RESETCONTENT, 0, 0);

    if(NULL == spDevice.p)
    {
        return E_POINTER;
    }
 
    // Status
    spDevice->get_status(&wmpDS);
    bstrStatistics = "Status: ";
    bstrTemp = szDeviceStatus[wmpDS];
    bstrStatistics += bstrTemp;
    SendMessage(hwndStats, LB_ADDSTRING, 0,(LPARAM)(LPCTSTR)COLE2T(bstrStatistics)); 
    bstrTemp.Empty();
    
    // Connected?
    spDevice->get_connected(&vbIsConnected);
    bstrStatistics = "Connected: ";
    bstrTemp = (vbIsConnected == VARIANT_TRUE)?"True":"False";
    bstrStatistics += bstrTemp;
    SendMessage(hwndStats, LB_ADDSTRING, 0,(LPARAM)(LPCTSTR)COLE2T(bstrStatistics));
    bstrTemp.Empty();
    
    // Device ID
    spDevice->get_deviceId(&bstrTemp);
    bstrStatistics = "Device ID: ";
    bstrStatistics += bstrTemp;

    // Calculate the list box width based on text metrics.
    // This assumes Device ID is likely to be the longest string.
    HDC hDC = GetDC();
    SIZE sizeText = {0, 0};
    GetTextExtentPoint32(hDC, (LPCTSTR)COLE2T(bstrStatistics), bstrStatistics.Length(), &sizeText);
    ReleaseDC(hDC);

    SendMessage(hwndStats, LB_ADDSTRING, 0,(LPARAM)(LPCTSTR)COLE2T(bstrStatistics)); 
    SendMessage(hwndStats, LB_SETHORIZONTALEXTENT, sizeText.cx, 0);
    bstrTemp.Empty();

    // Friendly name
    spDevice->get_friendlyName(&bstrTemp);
    bstrStatistics = "Friendly name: ";
    bstrStatistics += bstrTemp;
    SendMessage(hwndStats, LB_ADDSTRING, 0,(LPARAM)(LPCTSTR)COLE2T(bstrStatistics)); 
    bstrTemp.Empty();

    // Skip a line and label the getItemInfo attributes.
    bstrStatistics = "";
    SendMessage(hwndStats, LB_ADDSTRING, 0,(LPARAM)(LPCTSTR)COLE2T(bstrStatistics)); 
    bstrStatistics = "--getItemInfo Attributes--";
    SendMessage(hwndStats, LB_ADDSTRING, 0,(LPARAM)(LPCTSTR)COLE2T(bstrStatistics)); 

    // Show the getItemInfo attributes.
    int iArrayBound = sizeof szDeviceAttributeNames / sizeof szDeviceAttributeNames[0];
    for(int i = 0; i < iArrayBound; i++)
    {
        CComBSTR bstrName(szDeviceAttributeNames[i]);
        CComBSTR bstrVal;
        CComBSTR bstrDisplayString;
       
        hr = spDevice->getItemInfo(bstrName, &bstrVal);
  
        if(FAILED(hr))
        {
             bstrVal.Append("Error");
        }  
        
        bstrName.Append(L": ");
        bstrDisplayString.AppendBSTR(bstrName);
        bstrDisplayString += bstrVal;  
 
        SendMessage(hwndStats, LB_ADDSTRING, 0, (LPARAM)(LPCTSTR)COLE2T(bstrDisplayString));
    }    

    return hr;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Énumération des appareils**](enumerating-devices.md)
</dt> <dt>

[**Interface IWMPSyncDevice**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
</dt> <dt>

[**IWMPSyncDevice :: getItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-getiteminfo)
</dt> <dt>

[**Utilisation d’appareils mobiles**](working-with-portable-devices.md)
</dt> </dl>

 

 




