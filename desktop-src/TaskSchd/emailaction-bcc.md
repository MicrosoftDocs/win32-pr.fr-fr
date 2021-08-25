---
title: EmailAction. BCC, propriété
description: Pour les scripts, obtient ou définit l’adresse e-mail ou les adresses que vous souhaitez voir dans le message électronique.
ms.assetid: ab340cd7-d6ce-4dce-8474-fdbbc02bd65b
keywords:
- Planificateur de tâches de propriété BCC
- Planificateur de tâches de propriété BCC, objet EmailAction
- Objet EmailAction Planificateur de tâches, BCC, propriété
topic_type:
- apiref
api_name:
- EmailAction.Bcc
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 268aece8d6433d07b06d856c266d1e26c096104f0456856ac383253faaf4e976
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100389"
---
# <a name="emailactionbcc-property"></a>EmailAction. BCC, propriété

\[Cet objet n’est plus pris en charge. Utilisez IExecAction avec l’applet de commande PowerShell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) comme solution de contournement.\]

Pour les scripts, obtient ou définit l’adresse e-mail ou les adresses que vous souhaitez voir dans le message électronique.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
EmailAction.Bcc As String
```



## <a name="property-value"></a>Valeur de la propriété

L’adresse ou les adresses de messagerie que vous souhaitez voir CCI dans le message électronique.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                    |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2008 R2<br/>                                                       |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**EmailAction**](emailaction.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

