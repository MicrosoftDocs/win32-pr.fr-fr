---
title: Méthode IWMDRMLicenseManagement RestoreLicenses (wmdrmsdk. h)
description: La méthode RestoreLicenses restaure les licences à partir d’une sauvegarde de licence créée en appelant la méthode BackupLicenses.
ms.assetid: 83e4b748-0f69-4a9e-b531-047c9a2be1fe
keywords:
- Méthode RestoreLicenses format Windows Media
- Méthode RestoreLicenses format Windows Media, interface IWMDRMLicenseManagement
- Interface IWMDRMLicenseManagement Windows Media format, méthode RestoreLicenses
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.RestoreLicenses
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2a35fdd33df2387bb59dfac64f554dd8b5953fa3015afec6ca643725b9bd58f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117846937"
---
# <a name="iwmdrmlicensemanagementrestorelicenses-method"></a>IWMDRMLicenseManagement :: RestoreLicenses, méthode

La méthode **RestoreLicenses** restaure les licences à partir d’une sauvegarde de licence créée en appelant la méthode [**BackupLicenses**](iwmdrmlicensemanagement-backuplicenses.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT RestoreLicenses(
  [in]  BSTR     bstrBackupDirectory,
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrBackupDirectory* \[ dans\]
</dt> <dd>

Chemin d’accès UNC de l’emplacement à partir duquel les licences seront restaurées.

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Indicateurs spécifiant les options de restauration à utiliser. Le seul indicateur actuellement pris en charge est l' \_ \_ élément de restauration WMDRM, qui configure la méthode pour effectuer l’individualisation dans le cadre de la restauration, si nécessaire.

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



 

## <a name="remarks"></a>Remarques

Cette méthode s’exécute de façon asynchrone. Elle retourne immédiatement après l’appel de, puis génère une série d’événements **MEWMDRMLicenseRestoreProgress** suivie d’un événement **MEWMDRMLicenseRestoreCompleted** lorsque le traitement est terminé. La valeur de chacun des événements **MEWMDRMLicenseRestoreProgress** obtenus en appelant **IMFMediaEvent :: GetValue** est un pointeur **IUnknown** . Vous pouvez appeler la méthode **QueryInterface** de l’interface **IUnknown** Récupérée pour récupérer une instance de l’interface [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) .

pour plus d’informations sur l’utilisation des méthodes asynchrones des api étendues du Client Media DRM Windows, consultez [utilisation du modèle d’événement Media Foundation](using-the-media-foundation-model.md).

La sauvegarde peut être à partir de l’ordinateur local ou d’un autre ordinateur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





