---
title: Propriété principal. RunLevel
description: Pour les scripts, obtient ou définit l’identificateur qui est utilisé pour spécifier le niveau de privilège requis pour exécuter les tâches associées au principal.
ms.assetid: 2ec3d93e-9eef-4590-842c-edfc9232bcdf
keywords:
- Planificateur de tâches de la propriété RunLevel
- Planificateur de tâches de la propriété RunLevel, objet principal
- Planificateur de tâches de l’objet principal, propriété RunLevel
topic_type:
- apiref
api_name:
- Principal.RunLevel
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9acb6c4c86215312b2df73f7bf85847ef61a4b96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508661"
---
# <a name="principalrunlevel-property"></a>Propriété principal. RunLevel

Pour les scripts, obtient ou définit l’identificateur qui est utilisé pour spécifier le niveau de privilège requis pour exécuter les tâches associées au principal.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
Principal.RunLevel As Integer
```



## <a name="property-value"></a>Valeur de la propriété

Identificateur utilisé pour spécifier le niveau de privilège requis pour exécuter les tâches qui sont associées au principal.



| Valeur                                                                                                                                                                                                                                         | Signification                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="TASK_RUNLEVEL_LUA"></span><span id="task_runlevel_lua"></span><dl> <dt>**Tâche \_ RUNLEVEL \_ LUA**</dt> <dt>0</dt> </dl>             | Les tâches sont exécutées avec les privilèges minimum (LUA).<br/> |
| <span id="TASK_RUNLEVEL_HIGHEST"></span><span id="task_runlevel_highest"></span><dl> <dt>**Tâche \_ RUNLEVEL \_ le plus élevé**</dt> <dt>1</dt> </dl> | Les tâches sont exécutées avec les privilèges les plus élevés.<br/>     |



 

## <a name="remarks"></a>Notes

Si une tâche est inscrite à l’aide du \\ compte administrateur intégré ou des comptes système local ou service local, la propriété **runlevel** est ignorée. La valeur de propriété sera également ignorée si le contrôle de compte d’utilisateur (UAC) est désactivé.

Si une tâche est inscrite à l’aide du groupe administrateurs pour le contexte de sécurité de la tâche, vous devez également définir la propriété [**runlevel**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) sur la **tâche \_ runlevel la \_ plus élevée** si vous souhaitez exécuter la tâche. Pour plus d’informations, consultez [contextes de sécurité pour les tâches](security-contexts-for-running-tasks.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Directeur**](principal.md)
</dt> </dl>

 

 





