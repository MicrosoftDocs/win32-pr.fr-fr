---
title: Méthode IRDVTaskPluginNotifySink OnTerminated (Sbtsv. h)
description: Appelée par l’agent de tâche pour demander que l’agent de tâche soit arrêté.
ms.assetid: 163e0ce5-f4ee-4242-bdbb-977c5ede3451
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnTerminated
- Méthode OnTerminated Services Bureau à distance, interface IRDVTaskPluginNotifySink
- Services Bureau à distance de l’interface IRDVTaskPluginNotifySink, méthode OnTerminated
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.OnTerminated
api_location:
- sbtsv.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29ab2a3e8ddea5999b6d63322dbeb9fca07983e591e849f22a3e98e27c67609a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129131"
---
# <a name="irdvtaskpluginnotifysinkonterminated-method"></a>IRDVTaskPluginNotifySink :: OnTerminated, méthode

Appelée par l’agent de tâche pour demander que l’agent de tâche soit arrêté.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT OnTerminated(
  [in] HRESULT hr
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*RH* \[ dans\]
</dt> <dd>

Indique si l’arrêt est dû à un arrêt normal ou à un échec. Si l’arrêt est normal, cela indique que **est \_ OK**. Sinon, elle contient un code d’erreur **HRESULT** .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 7 Entreprise<br/>                                                    |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2<br/>                                                  |
| En-tête<br/>                   | <dl> <dt>Sbtsv. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IRDVTaskPluginNotifySink**](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

 





