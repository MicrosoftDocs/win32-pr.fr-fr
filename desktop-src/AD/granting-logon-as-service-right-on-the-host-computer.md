---
title: Octroi du droit d’ouverture de session en tant que service sur l’ordinateur hôte
description: Lors de l’installation d’un service pour qu’il s’exécute sous un compte d’utilisateur de domaine, le compte doit disposer du droit d’ouvrir une session en tant que service sur l’ordinateur local.
ms.assetid: 1b217650-4397-4e28-b53e-8b03f3caf903
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95ef2bb87c3cf461e67cb7da20f36d9ac07fb362
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671274"
---
# <a name="granting-logon-as-service-right-on-the-host-computer"></a><span data-ttu-id="30d59-103">Octroi du droit d’ouverture de session en tant que service sur l’ordinateur hôte</span><span class="sxs-lookup"><span data-stu-id="30d59-103">Granting Logon as Service Right on the Host Computer</span></span>

<span data-ttu-id="30d59-104">Lors de l’installation d’un service pour qu’il s’exécute sous un compte d’utilisateur de domaine, le compte doit disposer du droit d’ouvrir une session en tant que service sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="30d59-104">When installing a service to run under a domain user account, the account must have the right to logon as a service on the local computer.</span></span> <span data-ttu-id="30d59-105">N’oubliez pas que ce droit d’ouverture de session s’applique uniquement à l’ordinateur local et doit être accordé dans la stratégie LSA locale de chaque ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="30d59-105">Be aware that this logon right applies only to the local computer and must be granted in the local LSA policy of each host computer.</span></span> <span data-ttu-id="30d59-106">Cette étape n’est pas requise si votre service s’exécute en tant que LocalSystem, qui, par défaut, reçoit ce droit.</span><span class="sxs-lookup"><span data-stu-id="30d59-106">This step is not required if your service runs as LocalSystem, which, by default, is granted this right.</span></span>

<span data-ttu-id="30d59-107">Pour plus d’informations sur la façon d’accorder un droit d’ouverture de session en tant que service par programmation, consultez l' [exemple de code LSAPrivs](https://www.google.com/#q=LSAPrivs).</span><span class="sxs-lookup"><span data-stu-id="30d59-107">For more information on how to programmatically grant logon as a service right, see the [LSAPrivs sample code](https://www.google.com/#q=LSAPrivs).</span></span>

 

 




