---
description: Définit la fonction de rappel&\# 8212 ; que vous implémentez dans votre application&\# 8212 ; qui a été spécifié pour la fonction WFDStartDisplaySink.
ms.assetid: 0D4C00FD-4ED6-4F0F-BB72-0A1FCC05DB37
title: WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK fonction de rappel (Wfdsink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK
api_type:
- UserDefined
api_location:
- wfdsink.h
ms.openlocfilehash: c576f88a5b7f97484647c4c06f44522a5c3c379f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529162"
---
# <a name="wfd_display_sink_notification_callback-callback-function"></a>\_Fonction de \_ rappel de rappel de \_ notification du récepteur d’affichage WFD \_

La fonction de **rappel de notification du \_ récepteur d’affichage \_ \_ \_ WFD** définit la fonction de rappel, que vous implémentez dans votre application, qui a été spécifiée pour la fonction [**WFDStartDisplaySink**](wfdstartdisplaysink.md) .

## <a name="syntax"></a>Syntaxe


```C++
DWORD CALLBACK WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK(
  _In_opt_          PVOID                                 pvContext,
  _In_        const PWFD_DISPLAY_SINK_NOTIFICATION        pNotification,
  _Inout_opt_       PWFD_DISPLAY_SINK_NOTIFICATION_RESULT pNotificationResult
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pvContext* \[ dans, facultatif\]
</dt> <dd>

Pointeur de contexte facultatif passé à la fonction de rappel.

</dd> <dt>

*pNotification* \[ dans\]
</dt> <dd>

Pointeur vers un struct contenant les données relatives à la notification du récepteur d’affichage.

</dd> <dt>

*pNotificationResult* \[ in, out, facultatif\]
</dt> <dd>

Pointeur vers un struct contenant les données que votre application peut éventuellement définir pour indiquer le résultat du traitement de la notification du récepteur d’affichage.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 R2 \[ uniquement\]<br/>                              |
| En-tête<br/>                   | <dl> <dt>Wfdsink. h</dt> </dl> |



 

 




