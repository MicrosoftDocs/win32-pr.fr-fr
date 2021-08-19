---
description: arrête le mode récepteur Miracast, désactive la détectabilité et annule l’inscription du rappel.
ms.assetid: 38AE60CB-F601-4C03-A725-9B802341B84B
title: WFDDisplaySinkStop, fonction (Wfdsink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFDStopDisplaySink
api_type:
- DllExport
api_location:
- wifidisplay.dll
ms.openlocfilehash: a5e2da91e29535c1e2fd9553a2b6ec2bb0008e61f33cd55ebcda2746b93eb657
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117797929"
---
# <a name="wfddisplaysinkstop-function"></a>WFDDisplaySinkStop fonction)

arrête le mode récepteur Miracast, désactive la détectabilité et annule l’inscription du rappel. Votre application doit l’appeler une fois à l’arrêt.

## <a name="syntax"></a>Syntaxe


```C++
DWORD WINAPI WFDStopDisplaySink(void);
```



## <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.

## <a name="remarks"></a>Remarques

Il est prévu que votre application ait débloqué tous les rappels en cours avant d’appeler **WFDStopDisplaySink**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[Applications de bureau R2 uniquement\]<br/>                                    |
| Fin de la prise en charge des clients<br/>    | Windows 10<br/>                                                                      |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2016<br/>                                                             |
| En-tête<br/>                   | <dl> <dt>Wfdsink. h</dt> </dl>       |
| Bibliothèque<br/>                  | <dl> <dt>Wifidisplay. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wifidisplay.dll</dt> </dl> |



 

 




