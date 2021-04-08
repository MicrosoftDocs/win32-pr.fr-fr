---
title: TaskService. Connect, méthode
description: Pour les scripts, se connecte à un ordinateur distant et associe tous les appels suivants à cette interface avec une session à distance.
ms.assetid: 206087df-307c-4ba9-9e83-915f5287f281
keywords:
- Méthode Connect Planificateur de tâches
- Méthode Connect Planificateur de tâches, objet TaskService
- Planificateur de tâches objet TaskService, méthode Connect
topic_type:
- apiref
api_name:
- TaskService.Connect
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1db5f13e20da825cbdaf45ae399279687f6ff4aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941891"
---
# <a name="taskserviceconnect-method"></a>TaskService. Connect, méthode

Pour les scripts, se connecte à un ordinateur distant et associe tous les appels suivants à cette interface avec une session à distance. Si le paramètre serverName est vide, cette méthode s’exécute sur l’ordinateur local. Si le userId n’est pas spécifié, le jeton actuel est utilisé.

## <a name="syntax"></a>Syntaxe


```VB
TaskService.Connect( _
  [ ByVal serverName ], _
  [ ByVal user ], _
  [ ByVal domain ], _
  [ ByVal password ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*nom du serveur* \[ dans, facultatif\]
</dt> <dd>

Nom de l’ordinateur auquel vous souhaitez vous connecter. Si le paramètre serverName est vide, cette méthode s’exécute sur l’ordinateur local.

</dd> <dt>

*utilisateur* \[ dans, facultatif\]
</dt> <dd>

Nom d’utilisateur utilisé lors de la connexion à l’ordinateur. Si l’utilisateur n’est pas spécifié, le jeton actuel est utilisé.

</dd> <dt>

*domaine* \[ dans, facultatif\]
</dt> <dd>

Domaine de l’utilisateur spécifié dans le paramètre *User* .

</dd> <dt>

*mot de passe* \[ dans, facultatif\]
</dt> <dd>

Mot de passe utilisé pour se connecter à l’ordinateur. Si le nom d’utilisateur et le mot de passe ne sont pas spécifiés, le jeton actuel est utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

La méthode **TaskService. Connect** doit être appelée avant d’appeler l’une des autres méthodes [**TaskService**](taskservice.md) .

Si la méthode Connect échoue, vous pouvez collecter l’identificateur d’erreur pour déterminer la signification de l’erreur. Le tableau suivant répertorie les identificateurs d’erreur et leurs descriptions.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Identificateur d’erreur</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0x80070005</td>
<td>L’accès est refusé pour la connexion au service Planificateur de tâches.</td>
</tr>
<tr class="even">
<td>0x80041315</td>
<td>Le service Planificateur de tâches n’est pas en cours d’exécution.</td>
</tr>
<tr class="odd">
<td>0x8007000e</td>
<td>L’application ne dispose pas de suffisamment de mémoire pour terminer l’opération ou l' <em>utilisateur</em>, le <em>mot de passe</em>ou le <em>domaine</em> a au moins une valeur null et une valeur non null.</td>
</tr>
<tr class="even">
<td>53</td>
<td>Cette erreur est retournée dans les cas suivants :
<ul>
<li>Le nom d’ordinateur spécifié dans le paramètre <em>ServerName</em> n’existe pas.</li>
<li>Lorsque vous essayez de vous connecter à un ordinateur Windows Server 2003 ou Windows XP, et que l’exception de pare-feu de partage de fichiers et d’imprimantes n’est pas activée sur l’ordinateur distant ou que le service d’accès à distance au registre n’est pas en cours d’exécution.</li>
<li>Lorsque vous essayez de vous connecter à un ordinateur Windows Vista et que l’exception de pare-feu de gestion des tâches planifiées distantes n’est pas activée pour l’ordinateur distant et que l’exception de pare-feu de partage de fichiers et d’imprimantes est activée ou que le service d’accès à distance au registre n’est pas en cours d’exécution</li>
</ul></td>
</tr>
<tr class="odd">
<td>50</td>
<td>Les paramètres <em>utilisateur</em>, <em>mot de passe</em>ou <em>domaine</em> ne peuvent pas être spécifiés lors de la connexion à un ordinateur Windows XP ou Windows Server 2003 distant à partir d’un ordinateur Windows Vista.</td>
</tr>
</tbody>
</table>



 

Si vous vous connectez à un ordinateur Windows Vista distant à partir de Windows Vista, vous devez autoriser l’exception de pare-feu de gestion des tâches planifiées à distance sur l’ordinateur distant. Pour autoriser cette exception, cliquez sur Démarrer, panneau de configuration, sécurité, autoriser un programme via le pare-feu Windows, puis activez la case à cocher gestion des tâches planifiées distantes. Cliquez ensuite sur le bouton OK dans la boîte de dialogue Paramètres du pare-feu Windows.

Si vous vous connectez à un ordinateur Windows XP ou Windows Server 2003 distant à partir d’un ordinateur Windows Vista, vous devez autoriser l’exception de pare-feu de partage de fichiers et d’imprimantes sur l’ordinateur distant. Pour autoriser cette exception, cliquez sur Démarrer, panneau de configuration, double-cliquez sur pare-feu Windows, sélectionnez l’onglet exceptions, puis sélectionnez l’exception pare-feu de partage de fichiers et d’imprimantes. Cliquez ensuite sur le bouton OK dans la boîte de dialogue pare-feu Windows. Le service d’accès à distance au registre doit également être en cours d’exécution sur l’ordinateur distant.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





