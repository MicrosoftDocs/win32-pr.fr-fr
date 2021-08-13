---
description: Récupère le suivant d’un ou plusieurs objets IPortableDeviceConnector dans la séquence d’énumération.
ms.assetid: 5aed563a-5ecc-49c0-8a0c-622405453896
title: 'IEnumPortableDeviceConnectors :: Next, méthode (Devpkey. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPortableDeviceConnectors.Next
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 868f13f220dbd5d5867e5ee2bbb54c1ef946e267d87e9ea0aa625108b945d537
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118697294"
---
# <a name="ienumportabledeviceconnectorsnext-method"></a>IEnumPortableDeviceConnectors :: Next, méthode

La méthode **suivante** récupère le suivant d’un ou plusieurs objets [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) dans la séquence d’énumération.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Next(
  [in]      UINT32                   cRequested,
  [out]     IPortableDeviceConnector **pConnectors,
  [in, out] UINT32                   *pcFetched
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*cRequested* \[ dans\]
</dt> <dd>

Nombre d’appareils demandés. Cette valeur indique également le nombre d’éléments dans le tableau alloué par l’appelant spécifié par le paramètre *pConnectors* .

</dd> <dt>

*pConnectors* \[ à\]
</dt> <dd>

tableau de pointeurs [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) , chacun spécifiant un appareil Bluetooth MTP jumelé. L’appelant doit allouer un tableau de pointeurs **IPortableDeviceConnector** avec la longueur de tableau spécifiée par le paramètre *cRequested* . En cas de retour réussi, l’appelant doit libérer à la fois le tableau et les pointeurs retournés. Les interfaces **IPortableDeviceConnector** sont libérées en appelant la méthode **IUnknown :: Release** .

</dd> <dt>

*pcFetched* \[ in, out\]
</dt> <dd>

Nombre d’interfaces [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) réellement récupérées. Si aucune interface **IPortableDeviceConnector** n’est récupérée et que la valeur de retour est **\_ false**, il n’y a plus d’interfaces **IPortableDeviceConnector** à énumérer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                             | Description                                                      |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>    | S_OK<br/>                                 |
| <dl> <dt>**S \_ false**</dt> </dl> | il n’y a plus d’appareils de Bluetooth MTP à énumérer.<br/> |



 

## <a name="examples"></a>Exemples

l’exemple suivant illustre l’utilisation de cette méthode pour énumérer les appareils MTP/Bluetooth associés et pour envoyer une demande de connexion asynchrone à chacun.


```C++
IEnumPortableDeviceConnectors* pEnum = NULL;
    HRESULT hrEnum = S_OK;
 HRESULT hr = CoCreateInstance(CLSID_EnumBthMtpConnectors, NULL, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pEnum));
    if (SUCCEEDED(hr))
{
  while (S_OK == hrEnum)
    {
       UINT32  uFetched        = 0;
       LPWSTR  wszDevicePnPID  = NULL;
       IPortableDeviceConnector* pDevice = NULL;
       hrEnum = pEnum->Next(1, &spDevice, &uFetched);
       if (hrEnum == S_OK && uFetched == 1)
        {
          // Send an asynchronous connect request.  
          hr = pDevice ->Connect(NULL);
          // Release the device when done
          pDevice->Release();
          pDevice = NULL;
        }
     }  // while S_OK == hrEnum
  // Release the enumerator when done
    if (pEnum)
    {
     pEnum->Release();
     pEnum = NULL;
   }
    }
       
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                                                                                             |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                                                                              |
| En-tête<br/>                   | <dl> <dt>Devpkey. h ; </dt> <dt>PortableDeviceConnectApi. h</dt> </dl> |
| MIDL<br/>                      | <dl> <dt>PortableDeviceConnectApi. idl</dt> </dl>                                                                |
| Bibliothèque<br/>                  | <dl> <dt>PortableDeviceGuids. lib</dt> </dl>                                                                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IEnumPortableDeviceConnectors**](ienumportabledeviceconnectors.md)
</dt> </dl>

 

 




