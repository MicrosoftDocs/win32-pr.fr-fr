---
title: Méthode IWMDRMLicenseManagement BackupLicenses (wmdrmsdk. h)
description: La méthode BackupLicenses crée une sauvegarde des licences dans le magasin de licences local.
ms.assetid: f265254d-b240-4a9f-9c67-de9c92e8a14d
keywords:
- Méthode BackupLicenses format Windows Media
- Méthode BackupLicenses format Windows Media, interface IWMDRMLicenseManagement
- Interface IWMDRMLicenseManagement Windows Media format, méthode BackupLicenses
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.BackupLicenses
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61c7f676b532353c839a428571f6d28540851bee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543795"
---
# <a name="iwmdrmlicensemanagementbackuplicenses-method"></a>IWMDRMLicenseManagement :: BackupLicenses, méthode

La méthode **BackupLicenses** crée une sauvegarde des licences dans le magasin de licences local.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT BackupLicenses(
  [in]  BSTR     bstrBackupDirectory,
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrBackupDirectory* \[ dans\]
</dt> <dd>

Chemin d’accès UNC de l’emplacement vers lequel les licences seront sauvegardées.

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Indicateurs spécifiant les options de sauvegarde à utiliser. Le seul indicateur actuellement pris en charge est le \_ remplacement de la sauvegarde WMDRM \_ , qui configure la méthode pour remplacer les fichiers de sauvegarde existants dans le répertoire.

</dd> <dt>

*ppunkCancelationCookie* \[ à\]
</dt> <dd>

Pointeur qui reçoit un pointeur vers l’interface **IUnknown** d’un objet qui identifie cet appel asynchrone. Ce pointeur d’interface peut être utilisé pour annuler l’appel asynchrone en appelant la méthode [**IWMDRMEventGenerator :: CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="remarks"></a>Notes

Cette méthode s’exécute de façon asynchrone. Elle retourne immédiatement après l’appel de, puis génère une série d’événements **MEWMDRMLicenseBackupProgress** suivie d’un événement **MEWMDRMLicenseBackupCompleted** lorsque le traitement est terminé. La valeur de chacun des événements **MEWMDRMLicenseBackupProgress** obtenus en appelant **IMFMediaEvent :: GetValue** est un pointeur **IUnknown** . Vous pouvez appeler la méthode **QueryInterface** de l’interface **IUnknown** Récupérée pour récupérer une instance de l’interface [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) .

Pour plus d’informations sur l’utilisation des méthodes asynchrones des API étendues du client Windows Media DRM, consultez [utilisation du modèle d’événement Media Foundation](using-the-media-foundation-model.md).

Toutes les licences ne sont pas autorisées à être sauvegardées. Cette méthode sauvegarde uniquement les licences qui l’autorisent.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





