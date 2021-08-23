---
title: Méthode IWMDRMDeviceApp AcquireDeviceData (WMDRMDeviceApp. h)
description: La méthode AcquireDeviceData Initialise ou réinitialise une horloge sécurisée d’appareil.
ms.assetid: 2f1cfdb9-0f07-4bee-94aa-b33b039453d0
keywords:
- Méthode AcquireDeviceData Gestionnaire de périphériques Windows Media
- Méthode AcquireDeviceData Gestionnaire de périphériques Windows Media, interface IWMDRMDeviceApp
- Interface IWMDRMDeviceApp Windows Media Gestionnaire de périphériques, méthode AcquireDeviceData
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.AcquireDeviceData
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9280a358c7124a3f16e3d303026f36506610b6dc6fe0453fdf3e7b2432682719
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055641"
---
# <a name="iwmdrmdeviceappacquiredevicedata-method"></a>IWMDRMDeviceApp :: AcquireDeviceData, méthode

La méthode **AcquireDeviceData** Initialise ou réinitialise une horloge sécurisée d’appareil.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT AcquireDeviceData(
  [in]  IWMDMDevice    *pDevice,
  [in]  IWMDMProgress3 *pProgressCallback,
  [in]  DWORD          dwFlags,
  [out] DWORD          *pdwStatus
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDevice* \[ dans\]
</dt> <dd>

Pointeur vers une interface [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) pour l’appareil qui signale les données de contrôle.

</dd> <dt>

*pProgressCallback* \[ dans\]
</dt> <dd>

Rappel de progression via lequel l’application peut suivre la progression de l’événement ou annuler l’événement. La progression est identifiée par le paramètre *eventID* des méthodes [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3) .

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

**Or** logique de l’un des indicateurs suivants, en spécifiant l’action à effectuer. Cette valeur est extraite du paramètre *pdwStatus* de [**IWMDRMDeviceApp :: QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) ou [**IWMDRMDeviceApp2 :: QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md). Vous pouvez utiliser l’indicateur *pdwStatus* directement.



| Indicateur                        | Description                                   |
|-----------------------------|-----------------------------------------------|
| \_NEEDCLOCK d’appareil WMDRM \_    | Acquérir une horloge à partir d’un serveur d’horloge sécurisé.   |
| \_REFRESHCLOCK d’appareil WMDRM \_ | Actualisez l’horloge à partir d’un serveur d’horloge sécurisé. |



 

</dd> <dt>

*pdwStatus* \[ à\]
</dt> <dd>

Une des valeurs **DWORD** suivantes spécifiant l’état retourné par l’appareil.



| État | Description                                                     |
|--------|-----------------------------------------------------------------|
| 0      | L’action n’est pas prise en charge.                                    |
| 1      | L’horloge sécurisée de l’appareil n’a pas pu être acquise auprès du service. |
| 2      | L’horloge sécurisée de l’appareil n’a pas pu être définie.                     |
| 3      | L’horloge sécurisée de l’appareil a été définie.                              |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                                                                             | Description                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                                                    | S_OK<br/>                                                                                                    |
| <dl> <dt>**DRM \_ E \_ INVALIDARG**</dt> </dl>                                       | Un ou plusieurs arguments ne sont pas valides.<br/>                                                                                     |
| <dl> <dt>**appareil \_ NS \_ E \_ non \_ WMDRM \_**</dt> </dl>                        | l’appareil spécifié n’est pas un appareil compatible avec DRM Windows Media.<br/>                                                       |
| <dl> <dt>**la \_ \_ protection d’accès du service d’E/DRM \_ ne peut pas \_ obtenir un \_ \_ \_ réveil sécurisé**</dt> </dl>               | Impossible de récupérer le challenge d’horloge sécurisée à partir de l’appareil ou de récupérer l’URL d’horloge sécurisée à partir de la demande.<br/> |
| <dl> <dt>**NS \_ E \_ DRM \_ ne peut pas \_ \_ obtenir une \_ horloge sécurisée \_ \_ à partir du \_ serveur**</dt> </dl> | Échec de la récupération de la réponse d’horloge sécurisée à partir du serveur d’horloge sécurisé.<br/>                                               |
| <dl> <dt>**NS \_ E \_ DRM \_ ne peut pas \_ \_ définir l' \_ horloge sécurisée \_**</dt> </dl>               | Impossible d’envoyer le challenge d’horloge sécurisée à l’appareil, ou l’appareil n’a pas pu définir l’horloge.<br/>                          |



 

## <a name="remarks"></a>Remarques

Il s’agit d’une méthode asynchrone ; l’appareil doit attendre le rappel [**IWMDMProgress :: end**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmprogress-end) pour cette opération avant de tenter de lire un contenu sous licence.

Une application peut déterminer si l’horloge de l’appareil doit être réinitialisée ou mise à jour en appelant [**IWMDRMDeviceApp :: QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) ou [**IWMDRMDeviceApp2 :: QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md).

Votre application doit disposer d’une connexion Internet pour lui permettre d’acquérir ou de réinitialiser une horloge sécurisée.

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

[**Interface IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)
</dt> <dt>

[**Interface IWMDRMDeviceApp**](iwmdrmdeviceapp.md)
</dt> </dl>

 

 





