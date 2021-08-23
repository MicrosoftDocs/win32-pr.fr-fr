---
description: La méthode OnFrames doit être implémentée par le moniteur. Le MCSVC appelle cette méthode lorsque la mémoire tampon de capture est pleine ou que l’heure de mise à jour est passée.
ms.assetid: 243bd35b-2527-463e-b3d2-4bd840fe9c3f
title: 'IMonitor :: OnFrames, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.OnFrames
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: a4138c35384753c8df79728a61decf78bf302d0dc9c0a71ca9f787d76a70a620
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779169"
---
# <a name="imonitoronframes-method"></a>IMonitor :: OnFrames, méthode

La méthode **OnFrames** doit être implémentée par le moniteur. Le MCSVC appelle cette méthode lorsque la mémoire tampon de capture est pleine ou que l’heure de mise à jour est passée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT OnFrames(
  [in] UPDATE_EVENT Event
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Événement* \[ dans\]
</dt> <dd>

[Mettre à jour \_ ](update-event.md) Structure d’événement qui contient les informations de frame utilisées pour mettre à jour les événements.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode réussit, la valeur de retour est S \_ OK (ce qui est identique à la valeur de l’erreur). MCSVC renvoie la valeur retournée au NPP pour traitement.

Si la méthode échoue, la valeur de retour est un code d’erreur. MCSVC renvoie la valeur retournée au NPP pour traitement.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




