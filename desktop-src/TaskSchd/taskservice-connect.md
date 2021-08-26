---
title: TaskService. méthode Connecter
description: Pour les scripts, se connecte à un ordinateur distant et associe tous les appels suivants à cette interface avec une session à distance.
ms.assetid: 206087df-307c-4ba9-9e83-915f5287f281
keywords:
- méthode Connecter Planificateur de tâches
- Connecter méthode Planificateur de tâches, objet TaskService
- Planificateur de tâches de l’objet TaskService, méthode Connecter
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
ms.openlocfilehash: 1e8d9491fb66d8e79b18efed363d4eb4f21bc6c5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472345"
---
# <a name="taskserviceconnect-method"></a>TaskService. méthode Connecter

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

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

la méthode **TaskService. Connecter** doit être appelée avant d’appeler l’une des autres méthodes [**TaskService**](taskservice.md) .

si la méthode Connecter échoue, vous pouvez collecter l’identificateur d’erreur pour déterminer la signification de l’erreur. Le tableau suivant répertorie les identificateurs d’erreur et leurs descriptions.




| Identificateur d’erreur | Description | 
|------------------|-------------|
| 0x80070005 | L’accès est refusé pour la connexion au service Planificateur de tâches. | 
| 0x80041315 | Le service Planificateur de tâches n’est pas en cours d’exécution. | 
| 0x8007000e | L’application ne dispose pas de suffisamment de mémoire pour terminer l’opération ou l' <em>utilisateur</em>, le <em>mot de passe</em>ou le <em>domaine</em> a au moins une valeur null et une valeur non null. | 
| 53 | Cette erreur est retournée dans les cas suivants :<ul><li>Le nom d’ordinateur spécifié dans le paramètre <em>ServerName</em> n’existe pas.</li><li>lorsque vous essayez de vous connecter à un ordinateur Windows Server 2003 ou Windows XP, et que l’exception de pare-feu de partage de fichiers et d’imprimantes n’est pas activée sur l’ordinateur distant ou que le service d’accès à distance au registre n’est pas en cours d’exécution.</li><li>lorsque vous essayez de vous connecter à un ordinateur Windows Vista et que l’exception de pare-feu de gestion des tâches planifiées distantes n’est pas activée et que l’exception de pare-feu de partage de fichiers et d’imprimantes est activée sur l’ordinateur distant ou que le service d’accès à distance au registre n’est pas en cours d’exécution</li></ul> | 
| 50 | les paramètres <em>utilisateur</em>, <em>mot de passe</em>ou <em>domaine</em> ne peuvent pas être spécifiés lors de la connexion à un ordinateur distant Windows XP ou Windows Server 2003 à partir d’un ordinateur Windows Vista. | 




 

si vous vous connectez à un ordinateur distant Windows vista à partir d’un Windows vista, vous devez autoriser l’exception de pare-feu de gestion des tâches planifiées à distance sur l’ordinateur distant. pour autoriser cette exception, cliquez sur démarrer, panneau de configuration, sécurité, autoriser un programme via Windows pare-feu, puis activez la case à cocher gestion des tâches planifiées distantes. cliquez ensuite sur le bouton Ok dans la boîte de dialogue Windows Paramètres du pare-feu.

si vous vous connectez à un ordinateur distant Windows XP ou Windows Server 2003 à partir d’un ordinateur Windows Vista, vous devez autoriser l’exception de pare-feu de partage de fichiers et d’imprimantes sur l’ordinateur distant. pour autoriser cette exception, cliquez sur démarrer, panneau de configuration, double-cliquez sur Windows pare-feu, sélectionnez l’onglet Exceptions, puis sélectionnez l’exception pare-feu de partage de fichiers et d’imprimantes. cliquez ensuite sur le bouton OK dans la boîte de dialogue Windows le pare-feu. Le service d’accès à distance au registre doit également être en cours d’exécution sur l’ordinateur distant.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





