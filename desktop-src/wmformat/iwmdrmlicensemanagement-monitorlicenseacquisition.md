---
title: Méthode IWMDRMLicenseManagement MonitorLicenseAcquisition (wmdrmsdk. h)
description: La méthode MonitorLicenseAcquisition lance la surveillance d’un processus d’acquisition de licence.
ms.assetid: 725cd51a-a50b-4ff5-a880-7f551f6dba8f
keywords:
- Méthode MonitorLicenseAcquisition format Windows Media
- Méthode MonitorLicenseAcquisition format Windows Media, interface IWMDRMLicenseManagement
- Interface IWMDRMLicenseManagement Windows Media format, méthode MonitorLicenseAcquisition
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.MonitorLicenseAcquisition
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7ab3188425decca614ae104989fdc2f07930ac0de463e492be630a3fb54556e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027577"
---
# <a name="iwmdrmlicensemanagementmonitorlicenseacquisition-method"></a>IWMDRMLicenseManagement :: MonitorLicenseAcquisition, méthode

La méthode **MonitorLicenseAcquisition** lance la surveillance d’un processus d’acquisition de licence.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT MonitorLicenseAcquisition(
  [in]  BSTR     bstrKID,
  [in]  BSTR     bstrHeader,
  [in]  BSTR     bstrActions,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrKID* \[ dans\]
</dt> <dd>

ID de clé (KID) de la licence acquise.

</dd> <dt>

*bstrHeader* \[ dans\]
</dt> <dd>

En-tête de contenu qui a été utilisé dans l’appel à la méthode [**AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) .

</dd> <dt>

*bstrActions* \[ dans\]
</dt> <dd>

Chaîne contenant les actions demandées dans l’appel à la méthode **AcquireLicense** .

</dd> <dt>

*ppunkCancelationCookie* \[ à\]
</dt> <dd>

Pointeur qui reçoit un pointeur vers l’interface **IUnknown** d’un objet qui identifie cet appel asynchrone. Ce pointeur d’interface peut être utilisé pour annuler l’appel asynchrone en appelant la méthode [**IWMDRMEventGenerator :: CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="remarks"></a>Notes

Aucun.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





