---
title: EmailAction. Subject, propriété
description: Pour les scripts, obtient ou définit l’objet du message électronique.
ms.assetid: ea398af1-9ae6-4bcf-9618-bb840b15127e
keywords:
- Planificateur de tâches de la propriété Subject
- Propriété Subject Planificateur de tâches, objet EmailAction
- Objet EmailAction Planificateur de tâches, propriété Subject
topic_type:
- apiref
api_name:
- EmailAction.Subject
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7474fa4b7a6de59fd59a98c27a4877ab10c1acb6beac3c1682fccd05702aa275
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117943786"
---
# <a name="emailactionsubject-property"></a>EmailAction. Subject, propriété

\[Cet objet n’est plus pris en charge. Utilisez IExecAction avec l’applet de commande PowerShell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage?view=powershell-7&preserve-view=true) comme solution de contournement.\]

Pour les scripts, obtient ou définit l’objet du message électronique.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
EmailAction.Subject As String
```



## <a name="property-value"></a>Valeur de la propriété

Objet du message électronique.

## <a name="remarks"></a>Remarques

Lors de la définition de cette valeur de propriété, la valeur peut être un texte récupéré à partir d’une ressource .dll fichier. Une chaîne spécialisée est utilisée pour référencer le texte à partir du fichier de ressources. Le format de la chaîne est $ (@ \[ dll \] , \[ ResourceId \] ), où \[ dll \] est le chemin d’accès au fichier .dll qui contient la ressource et \[ ResourceId \] est l’identificateur du texte de la ressource. Par exemple, si vous affectez la valeur $ (@% SystemRoot% \\ System32 \\ResourceName.dll,-101) à cette propriété, vous affectez à la propriété la valeur du texte de la ressource avec un identificateur égal à-101 dans le fichier% systemroot% \\ system32 \\ResourceName.dll.

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

 

