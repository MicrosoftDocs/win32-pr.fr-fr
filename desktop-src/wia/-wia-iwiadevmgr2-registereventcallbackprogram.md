---
description: 'La méthode IWiaDevMgr2 :: RegisterEventCallbackProgram inscrit une application pour recevoir des événements d’appareil. il est principalement fourni pour la compatibilité descendante avec les applications qui n’ont pas été écrites pour Windows acquisition d’images (WIA) 2,0.'
ms.assetid: 6b427f19-719b-44ce-8e2c-3c44672345c8
title: 'IWiaDevMgr2 :: RegisterEventCallbackProgram, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.RegisterEventCallbackProgram
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 6ebc99e61bf038c8db2ea537a1f8a5933ad512d21ec05cf51f6f8b7af5ede2b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118441297"
---
# <a name="iwiadevmgr2registereventcallbackprogram-method"></a>IWiaDevMgr2 :: RegisterEventCallbackProgram, méthode

La méthode **IWiaDevMgr2 :: RegisterEventCallbackProgram** inscrit une application pour recevoir des événements d’appareil. il est principalement fourni pour la compatibilité descendante avec les applications qui n’ont pas été écrites pour Windows acquisition d’images (WIA) 2,0.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT RegisterEventCallbackProgram(
  [in]       LONG lFlags,
  [in]       BSTR bstrDeviceID,
  [in] const GUID *pEventGUID,
  [in]       BSTR bstrFullAppName,
  [in]       BSTR bstrCommandlineArg,
  [in]       BSTR bstrName,
  [in]       BSTR bstrDescription,
  [in]       BSTR bstrIcon
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lFlags* \[ dans\]
</dt> <dd>

Type : **long**

Indicateurs d’inscription. Peut être défini avec les valeurs suivantes.



| Valeur                                                                                                                                                                                                           | Signification                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span id="WIA_REGISTER_EVENT_CALLBACK"></span><span id="wia_register_event_callback"></span><dl> <dt>**\_rappel d' \_ événement de Registre WIA \_**</dt> </dl>       | Inscrivez-vous à l’événement.<br/>                           |
| <span id="WIA_UNREGISTER_EVENT_CALLBACK"></span><span id="wia_unregister_event_callback"></span><dl> <dt>**\_rappel d’événement d’annulation d’inscription WIA \_ \_**</dt> </dl> | Supprimez l’inscription de l’événement.<br/>            |
| <span id="WIA_SET_DEFAULT_HANDLER"></span><span id="wia_set_default_handler"></span><dl> <dt>**\_Gestionnaire WIA \_ par défaut \_**</dt> </dl>                   | Définissez l’application en tant que gestionnaire d’événements par défaut.<br/> |



 

</dd> <dt>

*bstrDeviceID* \[ dans\]
</dt> <dd>

Type : **BSTR**

Identificateur d’appareil. Transmettez la **valeur null** pour l’inscription de l’événement sur tous les appareils WIA 2,0.

</dd> <dt>

*pEventGUID* \[ dans\]
</dt> <dd>

Type : **const GUID \***

Événement pour lequel l’application est inscrite. Pour obtenir la liste des GUID d’événements valides, consultez la page [identificateurs d’événements WIA](-wia-wia-event-identifiers.md).

</dd> <dt>

*bstrFullAppName* \[ dans\]
</dt> <dd>

Type : **BSTR**

Nom de chemin d’accès complet de l’application.

</dd> <dt>

*bstrCommandlineArg* \[ dans\]
</dt> <dd>

Type : **BSTR**

Arguments de ligne de commande appropriés pour l’application.

</dd> <dt>

*bstrName* \[ dans\]
</dt> <dd>

Type : **BSTR**

Le nom de l’application. Le nom est affiché à l’utilisateur lorsque plusieurs applications s’inscrivent pour le même événement.

</dd> <dt>

*bstrDescription* \[ dans\]
</dt> <dd>

Type : **BSTR**

Description de l’application. La description est présentée à l’utilisateur lorsque plusieurs applications s’inscrivent pour le même événement.

</dd> <dt>

*bstrIcon* \[ dans\]
</dt> <dd>

Type : **BSTR**

Icône qui représente l’application. L’icône s’affiche pour l’utilisateur lorsque plusieurs applications s’inscrivent pour le même événement. La chaîne contient le nom de l’application et l’index de base zéro de l’icône, séparés par une virgule, par exemple « MyApp, 0 ». Il peut y avoir plus d’une icône qui représente une application.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

Utilisez **IWiaDevMgr2 :: RegisterEventCallbackProgram** pour vous inscrire pour les événements de périphérique matériel. Lorsqu’un événement se produit lorsqu’une application est inscrite, l’application est lancée et les informations sur l’événement sont transmises à l’application.

Utilisez la méthode [**EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) pour récupérer un pointeur vers un objet énumérateur pour les propriétés d’inscription des événements.

Utilisez la méthode **IWiaDevMgr2 :: RegisterEventCallbackProgram** uniquement pour la compatibilité descendante avec les applications non écrites pour l’architecture WIA 2,0. Utilisez les interfaces COM (Component Object Model) fournies par l’architecture WIA 2,0 pour les nouvelles applications. En particulier, appelez [**IWiaDevMgr2 :: RegisterEventCallbackInterface**](-wia-iwiadevmgr2-registereventcallbackinterface.md) ou [**IWiaDevMgr2 :: RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md) pour inscrire une nouvelle application pour les événements d’appareil.

En règle générale, cette méthode est appelée par un programme d’installation ou un script. Le programme ou le script d’installation inscrit l’application pour recevoir des événements d’appareil WIA 2,0. Lorsque l’événement se produit, l’application est démarrée par le système d’exécution WIA 2,0.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                   |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl> |



 

 




