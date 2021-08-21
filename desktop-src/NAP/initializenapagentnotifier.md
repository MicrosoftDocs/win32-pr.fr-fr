---
title: InitializeNapAgentNotifier, fonction (NapUtil. h)
description: Abonne le processus appelant aux notifications de modification d’État NapAgent et aux notifications de modification d’état de quarantaine.
ms.assetid: 24180194-50d7-4f54-845d-25402af9cf9a
keywords:
- InitializeNapAgentNotifier fonction NAP
topic_type:
- apiref
api_name:
- InitializeNapAgentNotifier
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ac2d874f6138bcc1fbc97952d4464e56e05b0a497c7b0ff98e9c05e8c8434e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118133454"
---
# <a name="initializenapagentnotifier-function"></a>InitializeNapAgentNotifier fonction)

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La fonction **InitializeNapAgentNotifier** abonne le processus appelant aux notifications de modification d’État NapAgent et aux notifications de modification d’état de quarantaine. Ces notifications sont fournies par le service NapAgent.

## <a name="syntax"></a>Syntaxe


```C++
NAPAPI HRESULT WINAPI InitializeNapAgentNotifier(
  _In_ NapNotifyType type,
  _In_ HANDLE        hNotifyEvent
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*type* \[ dans\]
</dt> <dd>

Valeur [**NapNotifyType**](/windows/win32/api/naptypes/ne-naptypes-napnotifytype) qui spécifie le type de notifications de service à recevoir.

</dd> <dt>

*hNotifyEvent* \[ dans\]
</dt> <dd>

Handle d’événement utilisé pour la notification. L’appelant doit passer un handle ouvert au paramètre *hNotifyEvent* . L’appelant doit également fermer le descripteur d’événement lorsqu’il n’est plus nécessaire.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée



| Code de retour                                                                                                | Description                                                                                               |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                       | L’initialisation s’est terminée avec succès.<br/>                                                         |
| <dl> <dt>**E \_ échec**</dt> </dl>                     | Échec de l'initialisation.<br/>                                                                         |
| <dl> <dt>**ERREUR \_ déjà \_ initialisée**</dt> </dl> | Le processus s’est déjà abonné aux notifications du service NapAgent du *type* spécifié. <br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>               | Un argument non valide a été passé. <br/>                                                               |



 

## <a name="remarks"></a>Remarques

Cette fonction n’est pas thread-safe.

Chaque processus qui requiert un abonnement aux notifications de service NapAgent du *type* spécifié doit appeler **InitializeNapAgentNotifier** pour s’abonner aux notifications. Si un processus doit s’abonner à plusieurs types de notifications, il doit appeler **InitializeNapAgentNotifier** une fois pour chaque type de notification.

Une fois qu’un processus ne nécessite pas d’autres notifications, le processus doit appeler [**UninitializeNapAgentNotifier**](uninitializenapagentnotifier.md) pour le *type* spécifié.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>NapUtil. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**UninitializeNapAgentNotifier**](uninitializenapagentnotifier.md)
</dt> </dl>

 

 





