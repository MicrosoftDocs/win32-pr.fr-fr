---
title: Méthode IWMDRMDeviceApp2 QueryDeviceStatus2 (WMDRMDeviceApp. h)
description: La méthode QueryDeviceStatus2 interroge un appareil pour obtenir un État ou une fonctionnalité DRM spécifique.
ms.assetid: f7e95fb7-5929-4a70-8580-a443e152e6d1
keywords:
- Méthode QueryDeviceStatus2 Gestionnaire de périphériques Windows Media
- Méthode QueryDeviceStatus2 Gestionnaire de périphériques Windows Media, interface IWMDRMDeviceApp2
- Interface IWMDRMDeviceApp2 Windows Media Gestionnaire de périphériques, méthode QueryDeviceStatus2
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp2.QueryDeviceStatus2
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 338d1f03f8d1e63086bb260c9854c7dcf3e88514
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520980"
---
# <a name="iwmdrmdeviceapp2querydevicestatus2-method"></a>IWMDRMDeviceApp2 :: QueryDeviceStatus2, méthode

La méthode **QueryDeviceStatus2** interroge un appareil pour obtenir un État ou une fonctionnalité DRM spécifique.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT QueryDeviceStatus2(
  [in]  IWMDMDevice *pDevice,
  [in]  DWORD       dwFlags,
  [out] DWORD       *pdwStatus
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDevice* \[ dans\]
</dt> <dd>

Pointeur vers un objet [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) .

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Une ou plusieurs des valeurs **DWORD** suivantes spécifiant les fonctionnalités à demander, combinées avec une **opération or** au niveau du bit.



| Indicateur                              | Description                                                                  |
|-----------------------------------|------------------------------------------------------------------------------|
| \_INDIVSTATUS du \_ client de requête WMDRM \_ | Demander si les composants DRM de l’ordinateur doivent être individualisés.       |
| CLOCKSTATUS de l' \_ appareil de requête WMDRM \_ \_ | Demander si l’horloge sécurisée de l’appareil doit être ajoutée ou mise à jour.        |
| ISREVOKED de l' \_ appareil de requête WMDRM \_ \_   | Demander si l’appareil est révoqué.                                         |
| ISWMDRM de l' \_ appareil de requête WMDRM \_ \_     | Demander si l’appareil prend en charge Windows Media DRM 10 pour les appareils mobiles. |



 

</dd> <dt>

*pdwStatus* \[ à\]
</dt> <dd>

Zéro, une ou plusieurs des valeurs **DWORD** suivantes spécifiant l’état de l’appareil demandé, combiné avec **une opération or** au niveau du bit.



| Statut                      | Description                                              |
|-----------------------------|----------------------------------------------------------|
| \_ISWMDRM d’appareil WMDRM \_      | L’appareil prend en charge Windows Media DRM.                   |
| \_NEEDCLOCK d’appareil WMDRM \_    | L’appareil n’a pas d’horloge sécurisée.                 |
| \_appareil WMDRM \_ révoqué      | L’appareil a été révoqué.                             |
| \_NEEDINDIV du client WMDRM \_    | Les composants DRM de l’ordinateur doivent être individualisés. |
| \_REFRESHCLOCK d’appareil WMDRM \_ | L’horloge doit être actualisée.                         |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                                                              | Description                                                               |
|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                                     | S_OK<br/>                                          |
| <dl> <dt>**DRM \_ E \_ INVALIDARG**</dt> </dl>                        | Un ou plusieurs arguments ne sont pas valides.<br/>                           |
| <dl> <dt>**\_ \_ \_ certificat non valide NS E DRM \_**</dt> </dl>          | Le certificat d’appareil récupéré à partir de l’appareil n’est pas valide.<br/> |
| <dl> <dt>**NS \_ E \_ DRM- \_ Impossible \_ d' \_ accéder au \_ \_ certificat de l’appareil**</dt> </dl> | Impossible de récupérer le certificat de l’appareil à partir de l’appareil.<br/>     |



 

## <a name="remarks"></a>Notes

Cette méthode doit être appelée avant d’effectuer des actions restreintes sur du contenu DRM, telles que le transfert de contenu DRM sur l’appareil ou l’obtention d’informations de contrôle. Si les valeurs récupérées par *pdwStatus* indiquent qu’une action doit être exécutée (par exemple, une individualisation pour le bureau ou l’acquisition d’une horloge pour l’appareil), l’application doit appeler [**IWMDRMDeviceApp :: AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) et transmettre la valeur *pdwStatus* Récupérée de cette fonction au paramètre *dwFlags* dans **AcquireDeviceData**. Si la valeur zéro est retournée, l’appareil ne prend pas en charge Windows Media DRM 10 pour les appareils mobiles et aucune action n’est nécessaire. Pour plus d’informations, consultez [gestion du contenu protégé dans l’application](handling-protected-content-in-the-application.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>WMDRMDeviceApp. h (nécessite également Wmdrmdeviceapp \_ i. c, créé à partir de WMDRMDeviceApp. idl)</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>Mssachlp. lib</dt> </dl>                                                                        |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Gestion du contenu protégé dans l’application**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**IWMDRMDeviceApp::QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md)
</dt> <dt>

[**Interface IWMDRMDeviceApp2**](iwmdrmdeviceapp2.md)
</dt> </dl>

 

 





