---
title: États de connexion
description: Pendant le processus de connexion à un serveur distant, le gestionnaire de connexions d’accès à distance et le serveur RAS sur l’ordinateur distant exécutent plusieurs étapes pour établir la connexion.
ms.assetid: 7a8b0086-308b-47d2-888e-69ff473c6015
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d9e52e1e4ea4a071f6606681aa2dc2fc15e88df659f8fd16746abf2d84727d2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074219"
---
# <a name="connection-states"></a>États de connexion

Pendant le processus de connexion à un serveur distant, le gestionnaire de connexions d’accès à distance et le serveur RAS sur l’ordinateur distant exécutent plusieurs étapes pour établir la connexion. Chacune de ces étapes est identifiée par un état de connexion. L’énumération [**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)) est un ensemble de valeurs qui correspondent à ces États de connexion. Les États de connexion peuvent être répartis dans les trois groupes suivants :

<dl> <dt>

<span id="Running_states"></span><span id="running_states"></span><span id="RUNNING_STATES"></span>États en cours d’exécution
</dt> <dd>

Les États en cours d’exécution sont les parties de l’opération de connexion que RAS gère automatiquement, par exemple la connexion aux appareils nécessaires, l’authentification de l’utilisateur et l’attente d’un rappel du serveur distant. À moins qu’une erreur ne se produise, le client RAS ne doit effectuer aucune action que pour transmettre la notification à l’utilisateur.

</dd> <dt>

<span id="Paused_states"></span><span id="paused_states"></span><span id="PAUSED_STATES"></span>États suspendus
</dt> <dd>

Les [États suspendus](paused-states.md) se produisent lorsque le serveur distant interrompt l’opération de connexion pour obtenir des informations supplémentaires de la part de l’utilisateur. Pendant un état suspendu, l’utilisateur peut taper un numéro de [rappel](callback-connections.md) , un nom d’utilisateur et un mot de passe différents en cas d’échec de l’authentification de l’utilisateur ou un nouveau mot de passe si l’ancien est arrivé à expiration.

</dd> <dt>

<span id="Terminal_states"></span><span id="terminal_states"></span><span id="TERMINAL_STATES"></span>États des terminaux
</dt> <dd>

Les États des terminaux se produisent lorsque la connexion a été établie avec succès, que l’opération de connexion a échoué ou que la connexion a été interrompue par un appel [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) .

</dd> </dl>

Un client RAS peut utiliser plusieurs mécanismes pour déterminer l’état actuel d’une opération de connexion. Lorsqu’un client RAS exécute la fonction [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) de manière asynchrone, le gestionnaire de connexions d’accès à distance envoie des notifications de progression au [Gestionnaire de notification](notification-handlers.md) du client chaque fois que l’état de la connexion change. En outre, le client peut utiliser la fonction [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) pour connaître l’état actuel de toute opération de connexion RAS.

 

 