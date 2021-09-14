---
title: EmailAction. Server, propriété
description: Pour les scripts, obtient ou définit le nom du serveur SMTP que vous utilisez pour envoyer des messages électroniques à partir de.
ms.assetid: a6e03144-ae3e-4c4c-aad8-884be5ab324f
keywords:
- Planificateur de tâches de propriétés de serveur
- Planificateur de tâches de propriétés de serveur, objet EmailAction
- Planificateur de tâches objet EmailAction, propriété de serveur
topic_type:
- apiref
api_name:
- EmailAction.Server
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fefcc5e33727d6b4ad0bcd60e48432c68422105
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414666"
---
# <a name="emailactionserver-property"></a>EmailAction. Server, propriété

\[Cet objet n’est plus pris en charge. Utilisez IExecAction avec l’applet de commande PowerShell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) comme solution de contournement.\]

Pour les scripts, obtient ou définit le nom du serveur SMTP que vous utilisez pour envoyer des messages électroniques à partir de.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
EmailAction.Server As String
```



## <a name="property-value"></a>Valeur de la propriété

Nom du serveur que vous utilisez pour envoyer des messages électroniques.

## <a name="remarks"></a>Notes

Assurez-vous que le serveur SMTP qui envoie l’e-mail est correctement configuré. le courrier électronique est envoyé à l’aide de l’authentification NTLM pour Windows serveurs smtp, ce qui signifie que les informations d’identification de sécurité utilisées pour l’exécution de la tâche doivent également avoir des privilèges sur le serveur smtp pour envoyer un message électronique. si le serveur SMTP est un serveur non Windows, le courrier électronique est envoyé si le serveur autorise l’accès anonyme. Pour plus d’informations sur la configuration du serveur SMTP, consultez [installation du serveur SMTP](https://www.microsoft.com/technet/prodtechnol/WindowsServer2003/Library/IIS/e4cf06f5-9a36-474b-ba78-3f287a2b88f2.mspx?mfr=true)et pour plus d’informations sur la gestion des paramètres du serveur SMTP, consultez [administration SMTP](/previous-versions/windows/it-pro/windows-server-2003/cc758258(v=ws.10)).

## <a name="requirements"></a>Spécifications



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

 

