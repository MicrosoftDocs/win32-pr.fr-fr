---
title: Méthode IWMDRMDeviceApp QueryDeviceStatus (WMDRMDeviceApp. h)
description: La méthode QueryDeviceStatus interroge l’État et les fonctionnalités DRM actuelles sur un appareil.
ms.assetid: cd5a75d5-d7f8-4077-a9fc-6e7ddd7c796b
keywords:
- Méthode QueryDeviceStatus Gestionnaire de périphériques Windows Media
- Méthode QueryDeviceStatus Gestionnaire de périphériques Windows Media, interface IWMDRMDeviceApp
- Interface IWMDRMDeviceApp Windows Media Gestionnaire de périphériques, méthode QueryDeviceStatus
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.QueryDeviceStatus
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8e0f4fad5ff9026ce70fc21712506eb4796d76b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533056"
---
# <a name="iwmdrmdeviceappquerydevicestatus-method"></a>IWMDRMDeviceApp :: QueryDeviceStatus, méthode

La méthode **QueryDeviceStatus** interroge l’État et les fonctionnalités DRM actuelles sur un appareil.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT QueryDeviceStatus(
  [in]  IWMDMDevice *pDevice,
  [out] DWORD       *pdwStatus
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDevice* \[ dans\]
</dt> <dd>

Pointeur vers un objet [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) .

</dd> <dt>

*pdwStatus* \[ à\]
</dt> <dd>

Zéro, une ou plusieurs des valeurs **DWORD** suivantes décrivant les aspects DRM de l’appareil, combinés avec **une opération or** au niveau du bit. Consultez la section Notes.



| Statut                      | Description                                  |
|-----------------------------|----------------------------------------------|
| \_ISWMDRM d’appareil WMDRM \_      | L’appareil prend en charge Windows Media DRM.       |
| \_NEEDCLOCK d’appareil WMDRM \_    | L’appareil n’a pas d’horloge sécurisée.     |
| \_appareil WMDRM \_ révoqué      | L’appareil a été révoqué.                 |
| \_NEEDINDIV du client WMDRM \_    | La sécurité DRM doit être individualisée. |
| \_REFRESHCLOCK d’appareil WMDRM \_ | L’horloge doit être actualisée.             |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                                                              | Description                                                               |
|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                                     | S_OK<br/>                                          |
| <dl> <dt>**DRM \_ E \_ INVALIDARG**</dt> </dl>                        | L’argument d’entrée n’est pas valide.<br/>                               |
| <dl> <dt>**\_ \_ \_ certificat non valide NS E DRM \_**</dt> </dl>          | Le certificat d’appareil récupéré à partir de l’appareil n’est pas valide.<br/> |
| <dl> <dt>**NS \_ E \_ DRM- \_ Impossible \_ d' \_ accéder au \_ \_ certificat de l’appareil**</dt> </dl> | Impossible de récupérer le certificat de l’appareil à partir de l’appareil.<br/>     |



 

## <a name="remarks"></a>Notes

Cette méthode doit être appelée avant d’effectuer des actions restreintes sur du contenu DRM, telles que le transfert de contenu DRM sur l’appareil ou l’obtention d’informations de contrôle. Si les valeurs récupérées par *pdwStatus* indiquent qu’une action doit être effectuée (par exemple, une individualisation pour le bureau ou l’acquisition d’une horloge pour l’appareil), l’application doit appeler [**AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) et transmettre la valeur *pdwStatus* Récupérée de cette fonction au paramètre *dwFlags* dans **AcquireDeviceData**. Si la valeur zéro est retournée, l’appareil ne prend pas en charge Windows Media DRM 10 pour les appareils mobiles et aucune action n’est nécessaire. Pour plus d’informations, consultez [gestion du contenu protégé dans l’application](handling-protected-content-in-the-application.md) .

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

[**Interface IWMDRMDeviceApp**](iwmdrmdeviceapp.md)
</dt> <dt>

[**IWMDRMDeviceApp2::QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md)
</dt> </dl>

 

 





