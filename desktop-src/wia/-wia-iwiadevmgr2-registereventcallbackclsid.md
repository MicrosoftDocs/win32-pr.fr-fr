---
description: 'La méthode IWiaDevMgr2 :: RegisterEventCallbackCLSID inscrit une application pour recevoir des événements même si l’application n’est pas en cours d’exécution.'
ms.assetid: e0d421a7-ef49-4e27-9661-c358ac819712
title: 'IWiaDevMgr2 :: RegisterEventCallbackCLSID, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.RegisterEventCallbackCLSID
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 9137fdd33f59eb841a54e84a6d12bb0b08968ac29c8737afbf56f66c57176c20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965647"
---
# <a name="iwiadevmgr2registereventcallbackclsid-method"></a>IWiaDevMgr2 :: RegisterEventCallbackCLSID, méthode

La méthode **IWiaDevMgr2 :: RegisterEventCallbackCLSID** inscrit une application pour recevoir des événements même si l’application n’est pas en cours d’exécution.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT RegisterEventCallbackCLSID(
  [in]               LONG lFlags,
  [in]               BSTR bstrDeviceID,
  [in]         const GUID *pEventGUID,
  [in, unique] const GUID *pClsID,
  [in]               BSTR bstrName,
  [in]               BSTR bstrDescription,
  [in]               BSTR bstrIcon
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lFlags* \[ dans\]
</dt> <dd>

Type : **long**

Spécifie les indicateurs d’inscription. Peut être défini avec les valeurs suivantes :



| Indicateur d’inscription                | Signification                                           |
|----------------------------------|---------------------------------------------------|
| \_rappel d' \_ événement de Registre WIA \_   | Inscrivez-vous à l’événement.                           |
| \_rappel d’événement d’annulation d’inscription WIA \_ \_ | Supprimez l’inscription de l’événement.            |
| \_Gestionnaire WIA \_ par défaut \_       | Définissez l’application en tant que gestionnaire d’événements par défaut. |



 

</dd> <dt>

*bstrDeviceID* \[ dans\]
</dt> <dd>

Type : **BSTR**

Spécifie un identificateur d’appareil. Transmettez la **valeur null** pour l’inscription de l’événement sur tous les appareils WIA 2,0.

</dd> <dt>

*pEventGUID* \[ dans\]
</dt> <dd>

Type : **const GUID \***

Spécifie l’événement pour lequel l’application est inscrite. Pour obtenir la liste des événements standard, consultez la page [identificateurs d’événements WIA](-wia-wia-event-identifiers.md).

</dd> <dt>

*pClsID* \[ dans\]
</dt> <dd>

Type : **const GUID \***

Pointeur vers l’ID de classe d’application (**CLSID**). Le système d’exécution WIA 2,0 utilise le **CLSID** de l’application pour démarrer l’application quand un événement s’est produit pour lequel il est enregistré.

</dd> <dt>

*bstrName* \[ dans\]
</dt> <dd>

Type : **BSTR**

Spécifie le nom de l’application qui s’inscrit pour l’événement.

</dd> <dt>

*bstrDescription* \[ dans\]
</dt> <dd>

Type : **BSTR**

Spécifie une description textuelle de l’application qui s’inscrit pour l’événement.

</dd> <dt>

*bstrIcon* \[ dans\]
</dt> <dd>

Type : **BSTR**

Spécifie le nom d’un fichier image à utiliser pour l’icône de l’application qui s’inscrit pour l’événement.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

Les applications WIA 2,0 utilisent cette méthode pour s’inscrire afin de recevoir des événements de périphérique matériel. Après l’appel de **IWiaDevMgr2 :: RegisterEventCallbackCLSID** , l’application est inscrite pour recevoir des événements d’appareil WIA 2,0, même s’il n’est pas en cours d’exécution.

Lorsque l’événement se produit, le système WIA 2,0 détermine quelle application est inscrite pour recevoir l’événement. Elle utilise la fonction [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) et le CLSID spécifiés dans le paramètre *pClsID* pour créer une instance de l’application, puis appelle la méthode [**ImageEventCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback) pour transmettre les informations d’événement à l’application.

Une application peut appeler la méthode [**EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) pour énumérer les informations d’inscription des événements.

Si l’application n’est pas un composant COM (Component Object Model) inscrit et n’est pas compatible avec l’architecture WIA 2,0, utilisez la méthode [**IWiaDevMgr2 :: RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md) pour inscrire une application pour les événements d’appareil.

> [!Note]  
> Dans une application multithread, il n’y a aucune garantie que le rappel de notification d’événement soit retourné sur le thread qui a inscrit le rappel.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                   |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl> |



 

 
