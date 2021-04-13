---
title: Méthode IRDVTaskPlugin StartTask
description: Appelé pour démarrer la tâche de mise à jour sur la machine virtuelle.
ms.assetid: c1e9f18b-1e83-4a29-8646-8adde94e8c14
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode StartTask
- Méthode StartTask Services Bureau à distance, interface IRDVTaskPlugin
- Services Bureau à distance de l’interface IRDVTaskPlugin, méthode StartTask
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.StartTask
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 51c499549378700a90d8fc78d075bc07c1f874cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465782"
---
# <a name="irdvtaskpluginstarttask-method"></a>IRDVTaskPlugin :: StartTask, méthode

Appelé pour démarrer la tâche de mise à jour sur la machine virtuelle.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT StartTask(
  [in] BSTR            Label,
  [in] BSTR            Identifier,
  [in] SAFEARRAY(BYTE) *Context
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Étiquette* \[ dans\]
</dt> <dd>

Étiquette de la tâche. Il s’agit de l’étiquette qui a été transmise à l’agent déclencheur dans la méthode [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) .

</dd> <dt>

*Identificateur* \[ dans\]
</dt> <dd>

Identificateur de la tâche. Il s’agit de l’identificateur qui a été passé à l’agent déclencheur dans la méthode [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) .

</dd> <dt>

*Contexte* \[ dans\]
</dt> <dd>

Données facultatives pour la tâche. Il s’agit des données qui ont été passées à l’agent déclencheur dans la méthode [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

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

 

 





