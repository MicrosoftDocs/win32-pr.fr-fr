---
title: États de connexion
description: Pendant le processus de connexion à un serveur distant, le gestionnaire de connexions d’accès à distance et le serveur RAS sur l’ordinateur distant exécutent plusieurs étapes pour établir la connexion.
ms.assetid: 7a8b0086-308b-47d2-888e-69ff473c6015
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df4488cc020a8a1b2a7da93384a4a5be1edb5182
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842514"
---
# <a name="connection-states"></a><span data-ttu-id="f1ae2-103">États de connexion</span><span class="sxs-lookup"><span data-stu-id="f1ae2-103">Connection States</span></span>

<span data-ttu-id="f1ae2-104">Pendant le processus de connexion à un serveur distant, le gestionnaire de connexions d’accès à distance et le serveur RAS sur l’ordinateur distant exécutent plusieurs étapes pour établir la connexion.</span><span class="sxs-lookup"><span data-stu-id="f1ae2-104">During the process of connecting to a remote server, the Remote Access Connection Manager and the RAS server on the remote computer perform several steps to establish the connection.</span></span> <span data-ttu-id="f1ae2-105">Chacune de ces étapes est identifiée par un état de connexion.</span><span class="sxs-lookup"><span data-stu-id="f1ae2-105">Each of these steps is identified by a connection state.</span></span> <span data-ttu-id="f1ae2-106">L’énumération [**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)) est un ensemble de valeurs qui correspondent à ces États de connexion.</span><span class="sxs-lookup"><span data-stu-id="f1ae2-106">The [**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)) enumeration is a set of values that correspond to these connection states.</span></span> <span data-ttu-id="f1ae2-107">Les États de connexion peuvent être répartis dans les trois groupes suivants :</span><span class="sxs-lookup"><span data-stu-id="f1ae2-107">The connection states can be divided into the following three groups:</span></span>

<dl> <dt>

<span data-ttu-id="f1ae2-108"><span id="Running_states"></span><span id="running_states"></span><span id="RUNNING_STATES"></span>États en cours d’exécution</span><span class="sxs-lookup"><span data-stu-id="f1ae2-108"><span id="Running_states"></span><span id="running_states"></span><span id="RUNNING_STATES"></span>Running states</span></span>
</dt> <dd>

<span data-ttu-id="f1ae2-109">Les États en cours d’exécution sont les parties de l’opération de connexion que RAS gère automatiquement, par exemple la connexion aux appareils nécessaires, l’authentification de l’utilisateur et l’attente d’un rappel du serveur distant.</span><span class="sxs-lookup"><span data-stu-id="f1ae2-109">The running states are the parts of the connection operation that RAS handles automatically, such as connecting to the necessary devices, authenticating the user, and waiting for a callback from the remote server.</span></span> <span data-ttu-id="f1ae2-110">À moins qu’une erreur ne se produise, le client RAS ne doit effectuer aucune action que pour transmettre la notification à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f1ae2-110">Unless an error occurs, the RAS client need take no action other than to pass the notification on to the user.</span></span>

</dd> <dt>

<span data-ttu-id="f1ae2-111"><span id="Paused_states"></span><span id="paused_states"></span><span id="PAUSED_STATES"></span>États suspendus</span><span class="sxs-lookup"><span data-stu-id="f1ae2-111"><span id="Paused_states"></span><span id="paused_states"></span><span id="PAUSED_STATES"></span>Paused states</span></span>
</dt> <dd>

<span data-ttu-id="f1ae2-112">Les [États suspendus](paused-states.md) se produisent lorsque le serveur distant interrompt l’opération de connexion pour obtenir des informations supplémentaires de la part de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f1ae2-112">The [paused states](paused-states.md) occur when the remote server pauses the connection operation to get additional input from the user.</span></span> <span data-ttu-id="f1ae2-113">Pendant un état suspendu, l’utilisateur peut taper un numéro de [rappel](callback-connections.md) , un nom d’utilisateur et un mot de passe différents en cas d’échec de l’authentification de l’utilisateur ou un nouveau mot de passe si l’ancien est arrivé à expiration.</span><span class="sxs-lookup"><span data-stu-id="f1ae2-113">During a paused state, the user can type a [callback](callback-connections.md) number, a different user name and password if the user authentication fails, or a new password if the old one has expired.</span></span>

</dd> <dt>

<span data-ttu-id="f1ae2-114"><span id="Terminal_states"></span><span id="terminal_states"></span><span id="TERMINAL_STATES"></span>États des terminaux</span><span class="sxs-lookup"><span data-stu-id="f1ae2-114"><span id="Terminal_states"></span><span id="terminal_states"></span><span id="TERMINAL_STATES"></span>Terminal states</span></span>
</dt> <dd>

<span data-ttu-id="f1ae2-115">Les États des terminaux se produisent lorsque la connexion a été établie avec succès, que l’opération de connexion a échoué ou que la connexion a été interrompue par un appel [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) .</span><span class="sxs-lookup"><span data-stu-id="f1ae2-115">The terminal states occur when the connection has been successfully established, the connection operation has failed, or the connection has been broken by a [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) call.</span></span>

</dd> </dl>

<span data-ttu-id="f1ae2-116">Un client RAS peut utiliser plusieurs mécanismes pour déterminer l’état actuel d’une opération de connexion.</span><span class="sxs-lookup"><span data-stu-id="f1ae2-116">There are several mechanisms that a RAS client can use to determine the current state of a connection operation.</span></span> <span data-ttu-id="f1ae2-117">Lorsqu’un client RAS exécute la fonction [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) de manière asynchrone, le gestionnaire de connexions d’accès à distance envoie des notifications de progression au [Gestionnaire de notification](notification-handlers.md) du client chaque fois que l’état de la connexion change.</span><span class="sxs-lookup"><span data-stu-id="f1ae2-117">When a RAS client executes the [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) function asynchronously, the Remote Access Connection Manager sends progress notifications to the client's [notification handler](notification-handlers.md) whenever the connection state changes.</span></span> <span data-ttu-id="f1ae2-118">En outre, le client peut utiliser la fonction [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) pour connaître l’état actuel de toute opération de connexion RAS.</span><span class="sxs-lookup"><span data-stu-id="f1ae2-118">In addition, the client can use the [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) function to get the current state of any RAS connection operation.</span></span>

 

 