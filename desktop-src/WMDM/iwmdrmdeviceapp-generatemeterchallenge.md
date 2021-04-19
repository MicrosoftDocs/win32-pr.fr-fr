---
title: Méthode IWMDRMDeviceApp GenerateMeterChallenge (WMDRMDeviceApp. h)
description: La méthode GenerateMeterChallenge acquiert des données de contrôle à partir d’un appareil.
ms.assetid: 2457cab7-bd45-49a7-ba69-74ae022207ce
keywords:
- Méthode GenerateMeterChallenge Gestionnaire de périphériques Windows Media
- Méthode GenerateMeterChallenge Gestionnaire de périphériques Windows Media, interface IWMDRMDeviceApp
- Interface IWMDRMDeviceApp Windows Media Gestionnaire de périphériques, méthode GenerateMeterChallenge
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.GenerateMeterChallenge
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06a71f04a5837f09575a2f4bccf4b17e34e30d63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528510"
---
# <a name="iwmdrmdeviceappgeneratemeterchallenge-method"></a>IWMDRMDeviceApp :: GenerateMeterChallenge, méthode

La méthode **GenerateMeterChallenge** acquiert des données de contrôle à partir d’un appareil.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GenerateMeterChallenge(
  [in]  IWMDMDevice *pDevice,
  [in]  BSTR        bstrMeterCert,
  [out] BSTR        *pbstrMeterURL,
  [out] BSTR        *pbstrMeterData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDevice* \[ dans\]
</dt> <dd>

Pointeur vers une interface [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) . Si l’application transmet la **valeur null**, les informations de contrôle stockées sur l’ordinateur sont utilisées à la place des informations de contrôle d’un appareil connecté.

</dd> <dt>

*bstrMeterCert* \[ dans\]
</dt> <dd>

Le certificat de contrôle de l’application, en tant que **BSTR**. Il s’agit d’un certificat signé reçu de Microsoft.

</dd> <dt>

*pbstrMeterURL* \[ à\]
</dt> <dd>

URL à laquelle les données de contrôle doivent être envoyées. Elle est allouée par les Gestionnaire de périphériques Windows Media et doit être libérée par l’appelant à l’aide de **SysFreeString**.

</dd> <dt>

*pbstrMeterData* \[ à\]
</dt> <dd>

Données de contrôle à envoyer au service de contrôle. Elle est allouée par les Gestionnaire de périphériques Windows Media et doit être libérée par l’appelant à l’aide de **SysFreeString**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                                                      | Description                                                                   |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                             | S_OK<br/>                                              |
| <dl> <dt>**DRM \_ E \_ INVALIDARG**</dt> </dl>                | Un ou plusieurs arguments ne sont pas valides.<br/>                               |
| <dl> <dt>**\_INVALIDXMLTAG DRM E \_**</dt> </dl>             | Le format XML est incorrect.<br/>                                          |
| <dl> <dt>**\_NOXMLCLOSETAG DRM E \_**</dt> </dl>             | Le format XML est incorrect.<br/>                                          |
| <dl> <dt>**\_NOXMLOPENTAG DRM E \_**</dt> </dl>              | Le format XML est incorrect.<br/>                                          |
| <dl> <dt>**\_XMLNOTFOUND DRM E \_**</dt> </dl>               | Impossible de trouver une balise XML obligatoire.<br/>                                 |
| <dl> <dt>**Erreurs de l’appareil**</dt> </dl>            | Un certain nombre d’erreurs d’appareil.<br/>                                  |
| <dl> <dt>**Erreurs du client DRM**</dt> </dl>        | L’une des nombreuses erreurs internes du client DRM.<br/>                     |
| <dl> <dt>**appareil \_ NS \_ E \_ non \_ WMDRM \_**</dt> </dl> | L’appareil spécifié n’est pas un périphérique compatible DRM Windows Media.<br/> |



 

## <a name="remarks"></a>Notes

Avant d’appeler cette méthode, l’application doit appeler [**IWMDRMDeviceApp :: QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) ou [**IWMDRMDeviceApp2 :: QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md) pour vérifier que tous les composants DRM de l’appareil sont à jour. Cette méthode peut uniquement être appelée sur un appareil qui prend en charge Windows Media DRM 10 pour les appareils mobiles.

Le *pbstrMeterData* de données extrait doit être envoyé à l’URL spécifiée par *pbstrMeterURL*. Veillez à encoder les données récupérées par URL afin qu’elles ne soient pas modifiées pendant le transfert.

Pour plus d’informations, consultez [gestion du contenu protégé dans l’application](handling-protected-content-in-the-application.md) .

## <a name="examples"></a>Exemples

L’exemple de code C++ suivant crée un objet **WMDRMDeviceApp** , vérifie que l’appareil est un appareil Windows Media DRM 10, que son horloge est exacte, puis demande les données de contrôle.


```C++
HRESULT hr = S_OK;
// Create the WMDRMDeviceApp object.
CComPtr<IWMDRMDeviceApp> pDRM;
hr = pDRM.CoCreateInstance(CLSID_WMDRMDeviceApp, 0, CLSCTX_ALL);

// Find out first if the device is a WMDRM 10 device, and if it requires
// any clock updates.
DWORD status = 0;
hr = pDRM->QueryDeviceStatus(pDevice, &status);

if (!(WMDRM_DEVICE_ISWMDRM & status)) // Device is not WMDRM 10. Nothing can be updated,
    return E_FAIL;                   // and metering cannot be performed.
else if (status & WMDRM_DEVICE_REVOKED) // Device is revoked.
    return E_FAIL;
else if (status & WMDRM_DEVICE_NEEDCLOCK || 
    status & WMDRM_CLIENT_NEEDINDIV ||
    status & WMDRM_DEVICE_REFRESHCLOCK)
{
    // Need to update device clock. 
    // Using custom function, which is synchronous.
    hr = myAcquireDeviceData(pDRM, pDevice, this, status, &result);
    if (hr != S_OK || result != 0)    // Couldn't perform the updates.
        return E_FAIL;    
}

// Any updates have been performed. Now get the metering information from the device.
CComBSTR meterCert(METERCERT);
CComBSTR URL;
CComBSTR rawdata;
CComBSTR data;
hr = pDRM->GenerateMeterChallenge(pDevice, meterCert, &URL, &rawdata);
if (hr == S_OK)
    ..... Send to URL...
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>WMDRMDeviceApp. h (nécessite également Wmdrmdeviceapp \_ i. c, créé à partir de WMDRMDeviceApp. idl)</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>Mssachlp. lib</dt> </dl>                                                                        |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Gestion du contenu protégé dans l’application**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**Interface IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)
</dt> <dt>

[**Interface IWMDRMDeviceApp**](iwmdrmdeviceapp.md)
</dt> </dl>

 

 





