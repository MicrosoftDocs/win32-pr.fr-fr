---
description: Nettoie l’état de la session en cours d’ouverture, ou la session actuellement ouverte.
ms.assetid: 8247AFA9-F471-4CCD-972D-D0C827E86880
title: WFDDisplaySinkCloseSession, fonction (Wfdsink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFDCloseDisplaySinkSession
api_type:
- DllExport
api_location:
- wifidisplay.dll
ms.openlocfilehash: 7697bc7ff1aa42569cf954b3f0b037f66ec67ded
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413742"
---
# <a name="wfddisplaysinkclosesession-function"></a>WFDDisplaySinkCloseSession fonction)

Nettoie l’état de la session en cours d’ouverture, ou la session actuellement ouverte.

## <a name="syntax"></a>Syntaxe


```C++
DWORD WINAPI WFDCloseDisplaySinkSession(
  _In_ HANDLE hSessionHandle
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hSessionHandle* \[ dans\]
</dt> <dd>

Le descripteur reçu via l’appel de [**rappel de notification du \_ récepteur d’affichage \_ \_ \_ WFD**](wfd-display-sink-notification-callback.md) le plus récent qui en comprenait un.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.

## <a name="remarks"></a>Notes

votre application peut appeler cette fonction pour mettre fin à la session Miracast pour une raison quelconque. Votre application n’est pas obligée de l’appeler quand elle reçoit le type **DisconnectedNotification** dans son rappel.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[Applications de bureau R2 uniquement\]<br/>                                    |
| Fin de la prise en charge des clients<br/>    | Windows 10<br/>                                                                      |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2016<br/>                                                             |
| En-tête<br/>                   | <dl> <dt>Wfdsink. h</dt> </dl>       |
| Bibliothèque<br/>                  | <dl> <dt>Wifidisplay. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wifidisplay.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_rappel de \_ notification du récepteur d’affichage WFD \_ \_**](wfd-display-sink-notification-callback.md)
</dt> </dl>

 

 




