---
description: Tous les utilisateurs ont un accès en lecture à la liste des processus du système et il existe plusieurs fonctions différentes qui énumèrent les processus actifs. La fonction que vous devez utiliser dépend de facteurs tels que la prise en charge de plateforme souhaitée.
ms.assetid: 4c73fb10-7ee8-4d8a-9cdb-a2ae59aef5bd
title: Énumération des processus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a05caa13d0f53fc87828669b2e19eba126c62c28f492b2f41d09caf2377321a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081319"
---
# <a name="process-enumeration"></a>Énumération des processus

Tous les utilisateurs ont un accès en lecture à la liste des processus du système et il existe plusieurs fonctions différentes qui énumèrent les processus actifs. La fonction que vous devez utiliser dépend de facteurs tels que la prise en charge de plateforme souhaitée.

Les fonctions suivantes sont utilisées pour énumérer les processus.



| Fonction                                                    | Description                                                                        |
|-------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses)                     | Récupère l’identificateur de processus pour chaque objet de processus dans le système.            |
| [**Process32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first)                   | Récupère des informations sur le premier processus rencontré dans un instantané système.    |
| [**Process32Next**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32next)                     | Récupère des informations sur le processus suivant enregistré dans un instantané système.        |
| [**WTSEnumerateProcesses**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumerateprocessesa) | Récupère des informations sur les processus actifs sur le serveur Terminal Server spécifié. |



 

Les fonctions toolhelp et [**EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses) énumèrent tous les processus. Pour répertorier les processus qui s’exécutent dans un compte d’utilisateur spécifique, utilisez [**WTSEnumerateProcesses**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumerateprocessesa) et filtrez sur le SID de l’utilisateur. Vous pouvez filtrer sur l’ID de session pour masquer les processus qui s’exécutent dans d’autres sessions Terminal Server.

Vous pouvez également filtrer les processus par compte d’utilisateur, quelle que soit la fonction d’énumération, en appelant [**OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess), [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken)et [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) avec **TokenUser**. Toutefois, vous ne pouvez pas ouvrir un processus qui est protégé par un descripteur de sécurité, sauf si vous avez reçu l’autorisation d’accès.

 

 
