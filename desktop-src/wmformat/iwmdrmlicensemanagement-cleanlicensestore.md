---
title: Méthode IWMDRMLicenseManagement CleanLicenseStore (wmdrmsdk. h)
description: La méthode CleanLicenseStore supprime les licences inutilisables du magasin de licences temporaire et défragmente le magasin de licences local pour améliorer les performances.
ms.assetid: 07ddd6f8-a091-4c18-81d3-c4d0c6026b6b
keywords:
- Méthode CleanLicenseStore format Windows Media
- Méthode CleanLicenseStore format Windows Media, interface IWMDRMLicenseManagement
- Interface IWMDRMLicenseManagement Windows Media format, méthode CleanLicenseStore
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.CleanLicenseStore
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6010313efaca6855c403f9ee698284ff4aebb2e0ab8a5e08e5862a5890224a1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117846950"
---
# <a name="iwmdrmlicensemanagementcleanlicensestore-method"></a>IWMDRMLicenseManagement :: CleanLicenseStore, méthode

La méthode **CleanLicenseStore** supprime les licences inutilisables du magasin de licences temporaire et défragmente le magasin de licences local pour améliorer les performances.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CleanLicenseStore(
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Indicateurs spécifiant les options de nettoyage du magasin de licences à utiliser. Définissez l’une des constantes dans le tableau suivant.



| Constante                            | Description                                                                                                                                                                    |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_synchronisation du \_ magasin de licences de nettoyage WMDRM \_ \_  | L’opération de nettoyage sera exécutée de façon synchrone. Cette méthode n’est pas retournée tant que l’opération n’est pas terminée.                                                              |
| \_magasin de licences nettoyées WMDRM \_ \_ \_ asynchrone | L’opération de nettoyage sera exécutée de manière asynchrone. Cette méthode est retournée immédiatement. Une fois l’opération terminée, l’événement de média MELicenseStoreCleaned sera envoyé. |



 

</dd> <dt>

*ppunkCancelationCookie* \[ à\]
</dt> <dd>

Pointeur qui reçoit un pointeur vers l’interface **IUnknown** d’un objet qui identifie cet appel asynchrone. Ce pointeur d’interface peut être utilisé pour annuler l’appel asynchrone en appelant la méthode [**IWMDRMEventGenerator :: CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                                            | Description                                                            |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                   | S_OK<br/>                                       |
| <dl> <dt>**\_LICENSENOTFOUND DRM E \_**</dt> </dl> | Il n’existe pas de magasin de licences temporaire sur l’ordinateur client.<br/> |



 

## <a name="remarks"></a>Remarques

Cette méthode s’exécute de façon asynchrone. Elle retourne immédiatement après l’appel de, puis génère un événement **MEWMDRMLicenseStoreCleaned** lorsque le traitement est terminé.

pour plus d’informations sur l’utilisation des méthodes asynchrones des api étendues du Client Media DRM Windows, consultez [utilisation du modèle d’événement Media Foundation](using-the-media-foundation-model.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





