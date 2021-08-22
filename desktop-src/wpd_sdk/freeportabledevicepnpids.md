---
description: 'Libère les identificateurs PnP (Plug-and-Play) récupérés par les méthodes IPortableDeviceManager :: GetDevices ou IPortableDeviceServiceManager :: GetDeviceServices.'
ms.assetid: b86f7733-81a3-4b60-bb7c-840c75f8d03f
title: FreePortableDevicePnPIDs, fonction (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreePortableDevicePnPIDs
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 150796912d2796a2697d3c088963c20e1523288f5a1301e9467a6859845db68c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590312"
---
# <a name="freeportabledevicepnpids-function"></a>FreePortableDevicePnPIDs fonction)

La fonction d’assistance **FreePortableDevicePnPIDs** libère les identificateurs PnP (plug-and-Play) récupérés par les méthodes [**IPortableDeviceManager :: GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) ou [**IPortableDeviceServiceManager :: GetDeviceServices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) .

## <a name="syntax"></a>Syntaxe


```C++
void FreePortableDevicePnPIDs(
   LPWSTR *pPnPIDs,
   DWORD  cPnPIDs
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pPnPIDs* 
</dt> <dd>

Tableau d’identificateurs PnP (Plug-and-Play) à libérer.

</dd> <dt>

*cPnPIDs* 
</dt> <dd>

Nombre d’identificateurs dans le tableau spécifié par le paramètre *pPnPIDs* .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

L’application est chargée de libérer le tableau de pointeurs qu’elle alloue.

## <a name="examples"></a>Exemples


```C++
// Allocate an array of LPWSTR pointers.
    LPWSTR* pPnpDeviceIDs = new LPWSTR[cPnpDeviceIDs];
if (pPnpDeviceIDs != NULL)
{
    hr = pPortableDeviceManager->;GetDevices(pPnpDeviceIDs, &cPnpDeviceIDs);
    if (SUCCEEDED(hr))
    {
        // Free all returned PnPDeviceID strings allocated by IPortableDeviceManager::GetDevices.
     FreePortableDevicePnPIDs(pPnpDeviceIDs, cPnpDeviceIDs);
     // Application is responsible for deleting the array of LPWSTR pointers.
     delete [] pPnpDeviceIDs;
     pPnpDeviceIDs = NULL;      
 }
} 
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 \| applications UWP\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                   |
| En-tête<br/>                   | <dl> <dt>PortableDevice. h</dt> </dl> |



 

 




