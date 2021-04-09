---
title: Instructions pour la sélection d’un compte d’ouverture de session de service
description: Un service Win32 peut s’exécuter dans le contexte de sécurité d’un compte d’utilisateur local, d’un compte d’utilisateur de domaine ou du compte LocalSystem.
ms.assetid: aa2b93c7-335f-4e03-9198-fe2b396e296e
ms.tgt_platform: multiple
keywords:
- Instructions pour la sélection d’un compte d’ouverture de session de service AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5bb8f5b4fe6a57863c09c9563454fc3ec09e75c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028606"
---
# <a name="guidelines-for-selecting-a-service-logon-account"></a><span data-ttu-id="b09d1-104">Instructions pour la sélection d’un compte d’ouverture de session de service</span><span class="sxs-lookup"><span data-stu-id="b09d1-104">Guidelines for Selecting a Service Logon Account</span></span>

<span data-ttu-id="b09d1-105">Un service Win32 peut s’exécuter dans le contexte de sécurité d’un compte d’utilisateur local, d’un compte d’utilisateur de domaine ou du compte LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="b09d1-105">A Win32-based service can run in the security context of a local user account, a domain user account, or the LocalSystem account.</span></span> <span data-ttu-id="b09d1-106">Pour déterminer le compte à utiliser, un administrateur doit installer le service avec le jeu d’autorisations minimal requis pour effectuer les opérations de service.</span><span class="sxs-lookup"><span data-stu-id="b09d1-106">To decide which account to use, an administrator should install the service with the minimum set of permissions required to perform the service operations.</span></span> <span data-ttu-id="b09d1-107">Dans un service standard d’annuaire, cela signifie que le programme d’installation du service doit créer un compte d’utilisateur de domaine pour le service et accorder à ce compte les droits d’accès et les privilèges spécifiques requis par le service au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="b09d1-107">In a typical directory-enabled service, this means the service installer should create a domain user account for the service and grant that account the specific access rights and privileges required by the service at run time.</span></span> <span data-ttu-id="b09d1-108">Un service ne doit s’exécuter que sous le compte LocalSystem si le service requiert des privilèges d’administrateur ou s’il doit agir en tant que partie du système d’exploitation sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="b09d1-108">A service should only run under the LocalSystem account if the service requires administrative privileges or must act as part of the operating system on the local computer.</span></span>

<span data-ttu-id="b09d1-109">N’oubliez pas que le programme d’installation du service doit, par défaut, configurer le service pour qu’il s’exécute sous un compte d’utilisateur de domaine.</span><span class="sxs-lookup"><span data-stu-id="b09d1-109">Be aware that the service installer should, by default, set up the service to run under a domain user account.</span></span> <span data-ttu-id="b09d1-110">Pour exécuter le service sous le compte LocalSystem, le programme d’installation du service doit demander à l’administrateur l’autorisation de le faire.</span><span class="sxs-lookup"><span data-stu-id="b09d1-110">To run the service under the LocalSystem account, the service installer should query the administrator for permission to do so.</span></span>

<span data-ttu-id="b09d1-111">Pour plus d’informations sur les descriptions, les avantages et les inconvénients de chaque type de compte, consultez :</span><span class="sxs-lookup"><span data-stu-id="b09d1-111">For more information about descriptions, advantages, and disadvantages of each account type, see:</span></span>

-   <span data-ttu-id="b09d1-112">[Comptes d’utilisateurs locaux](local-user-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="b09d1-112">[Local User Accounts](local-user-accounts.md).</span></span>
-   <span data-ttu-id="b09d1-113">[Comptes d’utilisateur de domaine](domain-user-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="b09d1-113">[Domain User Accounts](domain-user-accounts.md).</span></span>
-   <span data-ttu-id="b09d1-114">[Compte LocalSystem](the-localsystem-account.md).</span><span class="sxs-lookup"><span data-stu-id="b09d1-114">[The LocalSystem Account](the-localsystem-account.md).</span></span>

 

 




