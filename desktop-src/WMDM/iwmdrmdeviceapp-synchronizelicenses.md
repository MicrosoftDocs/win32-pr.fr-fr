---
title: Méthode IWMDRMDeviceApp SynchronizeLicenses (WMDRMDeviceApp. h)
description: La méthode SynchronizeLicenses met à jour les licences sur un appareil lorsque celles-ci arrivent à expiration.
ms.assetid: 352378c1-7432-476c-98e9-d811165c020e
keywords:
- Méthode SynchronizeLicenses Gestionnaire de périphériques Windows Media
- Méthode SynchronizeLicenses Gestionnaire de périphériques Windows Media, interface IWMDRMDeviceApp
- Interface IWMDRMDeviceApp Windows Media Gestionnaire de périphériques, méthode SynchronizeLicenses
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.SynchronizeLicenses
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91ec48743bf52d990c64ce1aecf30897a7ee2f51664e88695a181f9d4f758140
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031739"
---
# <a name="iwmdrmdeviceappsynchronizelicenses-method"></a>IWMDRMDeviceApp :: SynchronizeLicenses, méthode

La méthode **SynchronizeLicenses** met à jour les licences sur un appareil lorsque celles-ci arrivent à expiration.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SynchronizeLicenses(
  [in] IWMDMDevice    *pDevice,
  [in] IWMDMProgress3 *pProgressCallback,
  [in] DWORD          cMinCountThreshold,
  [in] DWORD          cMinHoursThreshold
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDevice* \[ dans\]
</dt> <dd>

Pointeur vers un objet [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) .

</dd> <dt>

*pProgressCallback* \[ dans\]
</dt> <dd>

Rappel de progression qui reçoit la progression de toutes les étapes qu’il peut être amené à effectuer. L’étape est identifiée par le paramètre *eventID* de la méthode [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3) appelée.

</dd> <dt>

*cMinCountThreshold* \[ dans\]
</dt> <dd>

Nombre minimal de jeux de lecture restant facultatif sur une licence d’appareil.

</dd> <dt>

*cMinHoursThreshold* \[ dans\]
</dt> <dd>

Heures restantes minimales facultatives sur une licence d’appareil.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                                                         | Description                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                                | S_OK<br/>                                                                                                                            |
| <dl> <dt>**DRM \_ E \_ INVALIDARG**</dt> </dl>                   | Un ou plusieurs arguments ne sont pas valides.<br/>                                                                                                             |
| <dl> <dt>**\_INVALIDXMLTAG DRM E \_**</dt> </dl>                | Le format XML est incorrect.<br/>                                                                                                                        |
| <dl> <dt>**\_NOTIMPL DRM E \_**</dt> </dl>                      | Cette fonctionnalité n’est pas implémentée pour le moment. (SyncLicenses w/ *pDevice* = null)<br/>                                                               |
| <dl> <dt>**\_NOXMLCLOSETAG DRM E \_**</dt> </dl>                | Le code XML de la licence est incorrect.<br/>                                                                                                           |
| <dl> <dt>**\_NOXMLOPENTAG DRM E \_**</dt> </dl>                 | Le code XML de la licence est incorrect.<br/>                                                                                                           |
| <dl> <dt>**\_OUTOFMEMORY DRM E \_**</dt> </dl>                  | Mémoire insuffisante.<br/>                                                                                                                                   |
| <dl> <dt>**\_XMLNOTFOUND DRM E \_**</dt> </dl>                  | Impossible de trouver une balise XML obligatoire dans la licence.<br/>                                                                                                |
| <dl> <dt>**appareil \_ NS \_ E \_ non \_ WMDRM \_**</dt> </dl>    | l’appareil spécifié n’est pas un appareil compatible avec DRM Windows Media.<br/>                                                                               |
| <dl> <dt>**l' \_ \_ individualisation des droits de l’utilisateur NS E \_ a besoin \_**</dt> </dl> | La DRM requiert une boîte noire individualisée pour exécuter cette fonction. en d’autres termes, le kit de développement logiciel (SDK) Windows Media Format requiert une mise à niveau de sécurité.<br/> |



 

## <a name="remarks"></a>Remarques

cet appel ne peut être effectué que sur un appareil qui prend en charge Windows Media DRM 10 pour les appareils mobiles. Vous devez spécifier au moins un paramètre de seuil.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>WMDRMDeviceApp. h (nécessite également Wmdrmdeviceapp \_ i. c, créé à partir de WMDRMDeviceApp. idl)</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>Mssachlp. lib</dt> </dl>                                                                        |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Gestion du contenu protégé dans l’application**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**Interface IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)
</dt> <dt>

[**Interface IWMDRMDeviceApp**](iwmdrmdeviceapp.md)
</dt> </dl>

 

 





