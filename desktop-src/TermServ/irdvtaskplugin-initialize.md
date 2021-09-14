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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127118625"
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

Type : **[ **IRDVTaskPluginNotifySink**](irdvtaskpluginnotifysink.md)\***

Pointeur vers une interface [**IRDVTaskPluginNotifySink**](irdvtaskpluginnotifysink.md) que l’agent de tâche utilise pour communiquer avec l’agent déclencheur. Vous devez libérer cette interface lorsqu’elle n’est plus nécessaire.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------|
| Client minimal pris en charge<br/> | Windows 7 Entreprise<br/>   |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IRDVTaskPlugin**](irdvtaskplugin.md)
</dt> </dl>

 

 





