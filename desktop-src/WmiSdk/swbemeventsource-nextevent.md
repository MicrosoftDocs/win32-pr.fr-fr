---
description: Si un événement est disponible, la méthode NextEvent de l’objet SWbemEventSource récupère l’événement à partir d’une requête d’événement.
ms.assetid: ff2d54d4-b8ee-4bb8-b6f7-081a1ca20489
ms.tgt_platform: multiple
title: Méthode SWbemEventSource. NextEvent (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemEventSource.NextEvent
- ISWbemEventSource.NextEvent
- ISWbemEventSource.NextEvent
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 02fbc32557ab29c66849a4249d26cc2ca41564e6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292830"
---
# <a name="swbemeventsourcenextevent-method"></a>Méthode SWbemEventSource. NextEvent

Si un événement est disponible, la méthode **NextEvent** de l’objet [**SWbemEventSource**](swbemeventsource.md) récupère l’événement à partir d’une requête d’événement.

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntaxe


```VB
objWbemObject = .NextEvent( _
  [ ByVal iTimeoutMs ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*iTimeoutMs* \[ dans, facultatif\]
</dt> <dd>

Nombre de millisecondes pendant lesquelles l’appel attend un événement avant de retourner une erreur de délai d’attente. La valeur par défaut de ce paramètre est **wbemTimeoutInfinite** (-1), qui indique à l’appel d’attendre indéfiniment.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la méthode **NextEvent** réussit, elle retourne un objet [**SWbemObject**](swbemobject.md) qui contient l’événement demandé. Si l’appel expire, l’objet retourné est **null** et une erreur est générée.

## <a name="error-codes"></a>Codes d’erreur

À la fin de la méthode **NextEvent** , l’objet **Err** peut contenir le code d’erreur figurant dans la liste suivante.

<dl> <dt>

**wbemErrTimedOut** -0x80043001
</dt> <dd>

L’événement demandé n’est pas arrivé dans le laps de temps spécifié dans *iTimeoutMs.*

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemEventSource<br/>                                                      |
| IID<br/>                      | IID \_ ISWbemEventSource<br/>                                                       |



 

 




