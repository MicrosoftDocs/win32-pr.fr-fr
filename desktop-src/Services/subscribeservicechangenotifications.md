---
description: S’abonne aux notifications de modification de l’état du service à l’aide d’une fonction de rappel.
ms.assetid: d67113eb-2141-444c-9f09-eaa772bcad8a
title: SubscribeServiceChangeNotifications, fonction (Winsvcp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SubscribeServiceChangeNotifications
api_type:
- DllExport
api_location:
- SecHost.dll
- API-MS-Win-Service-Private-L1-1-0.dll
- API-MS-Win-Service-Private-L1-1-1.dll
- Advapi32.dll
- API-MS-Win-Service-Private-L1-1-2.dll
ms.openlocfilehash: e327a44d613b514123862b1ddcb1bf302fea63ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527234"
---
# <a name="subscribeservicechangenotifications-function"></a>SubscribeServiceChangeNotifications fonction)

S’abonne aux notifications de modification de l’état du service à l’aide d’une fonction de rappel.

## <a name="syntax"></a>Syntaxe


```C++
DWORD WINAPI SubscribeServiceChangeNotifications(
  _In_     SC_HANDLE                     hService,
  _In_     SC_EVENT_TYPE                 eEventType,
  _In_     PSC_NOTIFICATION_CALLBACK     pCallback,
  _In_opt_ PVOID                         pCallbackContext,
  _Out_    PSC_NOTIFICATION_REGISTRATION *pSubscription
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hService* \[ dans\]
</dt> <dd>

Un handle vers le service ou un handle vers le gestionnaire de contrôle des services (SCM) pour surveiller les modifications.

Les handles vers les services sont retournés par les fonctions [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) et [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) et doivent disposer du droit d’accès **\_ \_ État** de la requête de service. Les handles du gestionnaire de contrôle des services sont retournés par la fonction [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) et doivent disposer du droit d' **\_ \_ énumérer \_** l’accès au service du gestionnaire SC.

</dd> <dt>

*eEventType* \[ dans\]
</dt> <dd>

Spécifie le type de modification d’État qui doit être signalé. Ce paramètre est défini sur l’une des valeurs spécifiées dans le [**\_ \_ type d’événement SC**](sc-event-type.md). Le comportement de cette fonction est différent selon le type d’événement, comme indiqué ci-dessous.



| Valeur                                                                                                                                                                                                                                                   | Signification                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span id="SC_EVENT_DATABASE_CHANGE"></span><span id="sc_event_database_change"></span><dl> <dt>**SC \_ \_ \_ Modification de la base de données d’événements**</dt> <dt>0</dt> </dl> | Un service a été ajouté ou supprimé. Le paramètre *hService* doit être un handle vers le SCM.<br/>                  |
| <span id="SC_EVENT_PROPERTY_CHANGE"></span><span id="sc_event_property_change"></span><dl> <dt>**SC \_ \_ \_ Modification**</dt> de la propriété d’événement <dt>1</dt> </dl> | Une ou plusieurs propriétés de service ont été mises à jour. Le paramètre *hService* doit être un handle vers le service.<br/> |
| <span id="SC_EVENT_STATUS_CHANGE"></span><span id="sc_event_status_change"></span><dl> <dt>**SC \_ \_ \_ Modification**</dt> de l’état de l’événement <dt>2</dt> </dl>       | L’état d’un service a changé. Le paramètre *hService* doit être un handle vers le service.<br/>              |



 

</dd> <dt>

*pCallback* \[ dans\]
</dt> <dd>

Spécifie la fonction de rappel. Le rappel doit être défini comme ayant un type de **\_ \_ rappel de notification SC**. Pour plus d'informations, consultez la section Notes.

</dd> <dt>

*pCallbackContext* \[ dans, facultatif\]
</dt> <dd>

Pointeur représentant le contexte de ce rappel de notification.

</dd> <dt>

*pSubscription* \[ à\]
</dt> <dd>

Retourne un pointeur vers l’abonnement résultant de l’inscription du rappel de notification. L’appelant est chargé d’appeler [**UnsubscribeServiceChangeNotifications**](unsubscribeservicechangenotifications.md) pour cesser de recevoir des notifications.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est une **erreur de \_ réussite**.

Si la fonction échoue, la valeur de retour est l’un des [codes d’erreur système](/windows/desktop/Debug/system-error-codes).

## <a name="remarks"></a>Notes

La fonction de rappel est déclarée comme suit :


```C++
typedef VOID CALLBACK SC_NOTIFICATION_CALLBACK(
    _In_    DWORD                   dwNotify,
    _In_    PVOID                   pCallbackContext
);
typedef SC_NOTIFICATION_CALLBACK* PSC_NOTIFICATION_CALLBACK;
```



La fonction de rappel reçoit un pointeur vers le contexte fourni par l’appelant. Le rappel est appelé à la suite de l’événement de modification de l’état du service. Lorsque le rappel est appelé, il est fourni avec un masque de révocation de **service \_ notification \_ * xxx*** qui indique le type de modification de l’état du service. Lorsque le rappel est fourni avec zéro au lieu d’une valeur de **service \_ Notify \_ * xxx*** valide, l’application doit vérifier ce qui a été modifié.

La fonction de rappel ne doit pas bloquer l’exécution. Si vous vous attendez à ce que l’exécution de la fonction de rappel prenne du temps, déchargez le travail que vous effectuez dans la fonction de rappel vers un thread distinct en mettant en file d’attente un élément de travail vers un thread dans un pool de threads. Certains types de travail qui peuvent rendre la fonction de rappel prend du temps incluent l’exécution d’e/s de fichier, l’attente d’un événement et l’exécution d’appels de procédure distante externes.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>Winsvcp. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>SecHost.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)
</dt> <dt>

[**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea)
</dt> <dt>

[**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera)
</dt> <dt>

[**UnsubscribeServiceChangeNotifications**](unsubscribeservicechangenotifications.md)
</dt> <dt>

[**QueryServiceDynamicInformation**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicedynamicinformation)
</dt> </dl>

 

