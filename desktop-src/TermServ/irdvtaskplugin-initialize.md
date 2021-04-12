---
title: IRDVTaskPlugin Initialize, méthode
description: Appelé pour initialiser l’agent de tâche.
ms.assetid: eef813e6-ecca-400a-a9f3-efca6bd81161
ms.tgt_platform: multiple
keywords:
- Initialize, méthode Services Bureau à distance
- Initialize, méthode Services Bureau à distance, IRDVTaskPlugin, interface
- Services Bureau à distance de l’interface IRDVTaskPlugin, méthode Initialize
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.Initialize
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9530be7334e1f3fefa7f73007334e448362a95ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384156"
---
# <a name="irdvtaskplugininitialize-method"></a>IRDVTaskPlugin :: Initialize, méthode

Appelé pour initialiser l’agent de tâche.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Initialize(
  [in] IRDVTaskPluginNotifySink *pNotifySink
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pNotifySink* \[ dans\]
</dt> <dd>

Tapez : **[**IRDVTaskPluginNotifySink**](irdvtaskpluginnotifysink.md) \** _

Pointeur vers une interface [_ *IRDVTaskPluginNotifySink* *](irdvtaskpluginnotifysink.md) que l’agent de tâche utilise pour communiquer avec l’agent déclencheur. Vous devez libérer cette interface lorsqu’elle n’est plus nécessaire.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------|
| Client minimal pris en charge<br/> | Windows 7 Entreprise<br/>   |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IRDVTaskPlugin**](irdvtaskplugin.md)
</dt> </dl>

 

 





