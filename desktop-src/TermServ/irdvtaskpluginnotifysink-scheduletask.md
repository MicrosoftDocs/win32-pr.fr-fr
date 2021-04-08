---
title: IRDVTaskPluginNotifySink ScheduleTask, méthode
description: Appelé par l’agent de tâche pour planifier une tâche.
ms.assetid: 06793439-cf16-40ca-8a91-08acc22c73ed
ms.tgt_platform: multiple
keywords:
- ScheduleTask, méthode Services Bureau à distance
- ScheduleTask, méthode Services Bureau à distance, IRDVTaskPluginNotifySink, interface
- IRDVTaskPluginNotifySink interface Services Bureau à distance, ScheduleTask, méthode
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.ScheduleTask
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c9bde92992eec9c4ab3d4151c59e6d687ec2f3fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844278"
---
# <a name="irdvtaskpluginnotifysinkscheduletask-method"></a>IRDVTaskPluginNotifySink :: ScheduleTask, méthode

Appelé par l’agent de tâche pour planifier une tâche.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ScheduleTask(
  [in] FILETIME        ftStartTime,
  [in] FILETIME        ftEndTime,
  [in] FILETIME        ftDeadline,
  [in] BSTR            bstrLabel,
  [in] BSTR            bstrIdentifier,
  [in] SAFEARRAY(BYTE) saContext
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ftStartTime* \[ dans\]
</dt> <dd>

Type : **[ **fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**

Heure de début de la première tâche, en UTC.

</dd> <dt>

*ftEndTime* \[ dans\]
</dt> <dd>

Type : **[ **fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**

Heure de fin de la tâche, en heure UTC. Passe un [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) défini à tous les zéros si aucune heure de fin n’est spécifiée.

</dd> <dt>

*ftDeadline* \[ dans\]
</dt> <dd>

Type : **[ **fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**

Date d’échéance de la tâche, en UTC. Cette valeur est utilisée pour définir la priorité de plusieurs tâches qui se trouvent dans leur fenêtre de démarrage. Si plusieurs tâches doivent être démarrées, celle avec l’échéance la plus proche est démarrée en premier.

</dd> <dt>

*bstrLabel* \[ dans\]
</dt> <dd>

Type : **BSTR**

Étiquette de la tâche. Cette valeur est transmise à la méthode [**StartTask**](irdvtaskplugin-starttask.md) .

</dd> <dt>

*bstrIdentifier* \[ dans\]
</dt> <dd>

Type : **BSTR**

Identificateur de la tâche. Cette valeur est transmise à la méthode [**StartTask**](irdvtaskplugin-starttask.md) .

</dd> <dt>

*Sacontext* \[ dans\]
</dt> <dd>

Type : **SAFEARRAY (Byte)**

Données facultatives pour la tâche. Cette valeur est transmise à la méthode [**StartTask**](irdvtaskplugin-starttask.md) .

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

[**IRDVTaskPluginNotifySink**](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

