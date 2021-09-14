---
title: UninitializeNapAgentNotifier, fonction (NapUtil. h)
description: Désabonne le processus appelant des notifications de changement d’État NapAgent et des notifications de changement d’état de quarantaine.
ms.assetid: b676ee33-caf6-48f0-acf8-5be1b23c62fe
keywords:
- UninitializeNapAgentNotifier fonction NAP
topic_type:
- apiref
api_name:
- UninitializeNapAgentNotifier
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5d68b43fba64be82908d73803113f871b08c93c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127110545"
---
# <a name="uninitializenapagentnotifier-function"></a>UninitializeNapAgentNotifier fonction)

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La fonction **UninitializeNapAgentNotifier** désabonne le processus appelant des notifications de changement d’État NapAgent et des notifications de changement d’état de quarantaine. Ces notifications sont fournies par le service NapAgent.

## <a name="syntax"></a>Syntaxe


```C++
NAPAPI VOID WINAPI UninitializeNapAgentNotifier(
  _In_ NapNotifyType type
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*type* \[ dans\]
</dt> <dd>

Valeur [**NapNotifyType**](/windows/win32/api/naptypes/ne-naptypes-napnotifytype) qui spécifie le type de notifications de service dont l’abonnement doit être annulé.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette fonction n’a pas de valeur de retour.

## <a name="remarks"></a>Notes

Cette fonction n’est pas thread-safe.

Chaque processus abonné aux notifications de service NapAgent du *type* spécifié doit appeler **UninitializeNapAgentNotifier** pour se désabonner des notifications. Si un processus est abonné à plusieurs types de notifications, il doit appeler **UninitializeNapAgentNotifier** une fois pour chaque type de notification.

Cette fonction échoue en silence si le processus n’a pas précédemment appelé [**InitializeNapAgentNotifier**](initializenapagentnotifier.md) pour le type de notification.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>NapUtil. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**InitializeNapAgentNotifier**](initializenapagentnotifier.md)
</dt> </dl>

 

 





