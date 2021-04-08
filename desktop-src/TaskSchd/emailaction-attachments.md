---
title: EmailAction. Attachments, propriété
description: Pour les scripts, obtient ou définit un tableau de pièces jointes envoyées avec le message électronique.
ms.assetid: 59bcb8c4-8b8c-4f09-94d6-3a65f1e8c0a8
keywords:
- Planificateur de tâches de propriétés des pièces jointes
- Propriété Attachments Planificateur de tâches, objet EmailAction
- Objet EmailAction Planificateur de tâches, propriété Attachments
topic_type:
- apiref
api_name:
- EmailAction.Attachments
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae620321f9dca7a5c38decf7de661d713989c88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741901"
---
# <a name="emailactionattachments-property"></a>EmailAction. Attachments, propriété

\[Cet objet n’est plus pris en charge. Utilisez IExecAction avec l’applet de commande PowerShell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) comme solution de contournement.\]

Pour les scripts, obtient ou définit un tableau de pièces jointes envoyées avec le message électronique.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
EmailAction.Attachments As String
```



## <a name="property-value"></a>Valeur de la propriété

Tableau de pièces jointes qui est envoyé avec le message électronique.

## <a name="remarks"></a>Notes

Un maximum de huit pièces jointes peuvent se trouver dans le tableau des pièces jointes.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
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

 

