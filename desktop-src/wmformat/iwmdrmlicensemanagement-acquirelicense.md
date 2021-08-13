---
title: IWMDRMLicenseManagement AcquireLicense, méthode (wmdrmsdk. h)
description: La méthode AcquireLicense acquiert de manière asynchrone une licence à partir d’une URL spécifiée.
ms.assetid: 2e134f39-1f45-4d3a-b7c7-460aa0a250d0
keywords:
- Méthode AcquireLicense format Windows Media
- Méthode AcquireLicense format Windows Media, interface IWMDRMLicenseManagement
- Interface IWMDRMLicenseManagement Windows Media format, AcquireLicense, méthode
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.AcquireLicense
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ad8251650c8a7e16c6eb2fc957df5e70459239c0cd6cf1184b5209ae51b6aaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118701125"
---
# <a name="iwmdrmlicensemanagementacquirelicense-method"></a>IWMDRMLicenseManagement :: AcquireLicense, méthode

La méthode **AcquireLicense** acquiert de manière asynchrone une licence à partir d’une URL spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT AcquireLicense(
  [in]  BSTR     bstrURL,
  [in]  BSTR     bstrHeaderData,
  [in]  BSTR     bstrActions,
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*du bstrURL* \[ dans\]
</dt> <dd>

URL du serveur de licences à partir duquel acquérir la licence. Transmettez la **valeur null** pour que la méthode analyse l’URL à partir de l’en-tête de contenu.

</dd> <dt>

*bstrHeaderData* \[ dans\]
</dt> <dd>

En-tête de contenu à transmettre au serveur de licences. Si *du bstrURL* a la **valeur null**, la méthode analyse l’URL à partir de cet en-tête. Si *dwFlags* est défini sur WMDRM \_ Acquire la \_ licence \_ héritée \_ non silencieuse, définissez cette valeur sur l’ID de clé au lieu de l’en-tête de contenu entier.

</dd> <dt>

*bstrActions* \[ dans\]
</dt> <dd>

Chaîne contenant zéro, une ou plusieurs actions pour lesquelles une autorisation doit être demandée dans la licence. La chaîne doit être mise en forme de la façon suivante :

-   Chaque action doit être définie dans un élément ACTION. Les données de l’élément sont la chaîne d’action.
-   Tous les éléments ACTION doivent être contenus dans un élément ACTIONLIST.

    Par exemple, la chaîne permettant de demander une licence pour lire du contenu est au format suivant :

    ```C++
    <ACTIONLIST><ACTION></ACTION></ACTIONLIST>
    ```

    

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Indicateurs d’option d’acquisition de licence. Définissez l’une des constantes dans le tableau suivant.



| Constante                                   | Description                                                                                                              |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| licence d’acquisition WMDRM en \_ \_ \_ mode silencieux            | La licence sera émise directement sur Internet sans aucune confirmation de la part de l’application cliente.              |
| licence d’acquisition WMDRM sans \_ \_ \_ silence         | Le sous-système DRM crée une demande de licence qui est renvoyée de manière asynchrone pour la publication sur le serveur de licences. |
| l’héritage de la licence d’acquisition WMDRM n’est pas \_ \_ \_ \_ silencieux | Identique à la \_ licence d’acquisition WMDRM sans \_ \_ silence, sauf qu’une demande de licence DRM version 1 sera créée.           |



 

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

Cette méthode s’exécute de façon asynchrone. Elle retourne immédiatement après l’appel de, puis génère un événement **MEWMDRMLicenseAcquisitionCompleted** lorsque le traitement est terminé. Pour les opérations d’acquisition de licence non silencieuses, la valeur de l’événement obtenu en appelant **IMFMediaEvent :: GetValue** est un pointeur **IUnknown** . Vous pouvez appeler la méthode **QueryInterface** de l’interface **IUnknown** Récupérée pour récupérer une instance de l’interface [**IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md) .

pour plus d’informations sur l’utilisation des méthodes asynchrones des api étendues du Client Media DRM Windows, consultez [utilisation du modèle d’événement Media Foundation](using-the-media-foundation-model.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)
</dt> <dt>

[**Acquisition de licence en mode silencieux**](silent-license-acquisition.md)
</dt> </dl>

 

 





