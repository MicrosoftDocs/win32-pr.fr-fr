---
title: Vérifier que le serveur est bien celui qu’il prétend être
description: Il est préférable d’utiliser l’authentification mutuelle et, par conséquent, de vérifier l’identité du serveur.
ms.assetid: 6636a865-0e3b-4e52-81bb-0df48285e928
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d3e16ae6a87134a9fbc783d35216a1c4df56ce2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673250"
---
# <a name="verify-the-server-is-who-it-claims-to-be"></a><span data-ttu-id="870dc-103">Vérifier que le serveur est bien celui qu’il prétend être</span><span class="sxs-lookup"><span data-stu-id="870dc-103">Verify the Server is Who it Claims to Be</span></span>

<span data-ttu-id="870dc-104">Il est préférable d’utiliser l’authentification mutuelle et, par conséquent, de vérifier l’identité du serveur.</span><span class="sxs-lookup"><span data-stu-id="870dc-104">It is best to use mutual authentication, and thereby verify the identity of the server.</span></span> <span data-ttu-id="870dc-105">Voici un exemple d’erreur courante qui ne parvient pas à effectuer cette opération : les applications qui ont un service local dans lequel les clients appellent.</span><span class="sxs-lookup"><span data-stu-id="870dc-105">An example of a common mistake that fails to do this is applications that have a local service into which clients call.</span></span> <span data-ttu-id="870dc-106">Dans certaines configurations, un administrateur peut décider que le service système n’est pas vraiment utile et peut choisir de l’arrêter.</span><span class="sxs-lookup"><span data-stu-id="870dc-106">In some configurations an administrator may decide that the system service is not really useful and may chose to stop it.</span></span> <span data-ttu-id="870dc-107">Une personne malveillante inventif sur un ordinateur Terminal Server peut lancer un processus qui écoute sur le même point de terminaison, et lorsqu’un client se connecte à un point de terminaison, autorisant l’emprunt d’identité sur le serveur sans authentification mutuelle du serveur, l’attaquant peut emprunter l’identité du client et accéder aux données du client, ou effectuer des appels réseau pour le compte du client.</span><span class="sxs-lookup"><span data-stu-id="870dc-107">An inventive attacker on a terminal server computer may launch a process that listens on the same endpoint, and when a client connects to an endpoint, allowing impersonation on the server without mutually authenticating the server, the attacker can impersonate the client and access the client's data, or make network calls on behalf of the client.</span></span> <span data-ttu-id="870dc-108">La plupart des services système s’exécutent sous un compte bien connu, tel que LocalSysyem, LocalService ou NetworkService, qui peut être vérifié à l’aide de l’authentification mutuelle.</span><span class="sxs-lookup"><span data-stu-id="870dc-108">Most system services run under a well-known account, such as LocalSysyem, LocalService, or NetworkService, which can be verified using mutual authentication.</span></span>

 

 




