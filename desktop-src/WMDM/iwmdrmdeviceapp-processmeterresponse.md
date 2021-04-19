---
title: Méthode IWMDRMDeviceApp ProcessMeterResponse (WMDRMDeviceApp. h)
description: La méthode ProcessMeterResponse réinitialise tout ou partie des nombres de contrôle sur un appareil, une fois que les données de l’appareil ont été envoyées et traitées par le serveur.
ms.assetid: bafc4bb2-aa3c-4b2a-a818-1a78577cefc5
keywords:
- Méthode ProcessMeterResponse Gestionnaire de périphériques Windows Media
- Méthode ProcessMeterResponse Gestionnaire de périphériques Windows Media, interface IWMDRMDeviceApp
- Interface IWMDRMDeviceApp Windows Media Gestionnaire de périphériques, méthode ProcessMeterResponse
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.ProcessMeterResponse
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b57312dc2f401207e41f38f5bf75cddf69a13b1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545470"
---
# <a name="iwmdrmdeviceappprocessmeterresponse-method"></a>IWMDRMDeviceApp ::P méthode rocessMeterResponse

La méthode **ProcessMeterResponse** réinitialise tout ou partie des nombres de contrôle sur un appareil, une fois que les données de l’appareil ont été envoyées et traitées par le serveur.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ProcessMeterResponse(
  [in]  IWMDMDevice *pDevice,
  [in]  BYTE        *pbResponse,
  [in]  DWORD       cbResponse,
  [out] DWORD       *pdwFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDevice* \[ dans\]
</dt> <dd>

Pointeur vers un objet [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) .

</dd> <dt>

*pbResponse* \[ dans\]
</dt> <dd>

Réponse reçue d’un serveur de contrôle, après l’envoi des données générées à l’aide de [**GenerateMeterChallenge**](iwmdrmdeviceapp-generatemeterchallenge.md).

</dd> <dt>

*cbResponse* \[ dans\]
</dt> <dd>

Taille de *pbResponse*, en octets.

</dd> <dt>

*pdwFlags* \[ à\]
</dt> <dd>

Un **DWORD** du tableau ci-dessous, indiquant s’il y a plus de données de contrôle sur l’appareil qui doivent être traitées.



| Indicateur                            | Description                                     |
|---------------------------------|-------------------------------------------------|
| \_réponse du compteur WMDRM \_ \_ All     | Toutes les données de contrôle ont été traitées.           |
| réponse de compteur de WMDRM \_ \_ \_ partielle | Des données de contrôle supplémentaires doivent être traitées. |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                                                      | Description                                                                   |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                             | S_OK<br/>                                              |
| <dl> <dt>**DRM \_ E \_ INVALIDARG**</dt> </dl>                | Un ou plusieurs arguments ne sont pas valides.<br/>                               |
| <dl> <dt>**Erreurs de l’appareil**</dt> </dl>            | Un certain nombre d’erreurs d’appareil.<br/>                                  |
| <dl> <dt>**Erreurs du client DRM**</dt> </dl>        | L’une des nombreuses erreurs internes du client DRM.<br/>                     |
| <dl> <dt>**appareil \_ NS \_ E \_ non \_ WMDRM \_**</dt> </dl> | L’appareil spécifié n’est pas un périphérique compatible DRM Windows Media.<br/> |



 

## <a name="remarks"></a>Notes

Pour plus d’informations sur le contrôle, y compris des exemples de code, consultez le livre blanc [contrôle de l’utilisation du contenu multimédia numérique avec Windows Media DRM 10](/previous-versions//bb614723(v=vs.85)) sur le site Web MSDN.

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

 

