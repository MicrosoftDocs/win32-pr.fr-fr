---
title: Utilisation d’un compte d’utilisateur local en tant que compte d’ouverture de session de service
description: Un compte d’utilisateur local (format de nom \ 0034 ;. \\ Nom d’utilisateur \ 0034 ;) existe uniquement dans la base de données SAM de l’ordinateur hôte ; Il n’a pas d’objet utilisateur dans Active Directory Domain Services.
ms.assetid: a36d4d1c-3cfc-4ae1-8f1d-3f2e766f0c4b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84da502e99d2e5cd74e98e9f792e06f74f4852e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100593"
---
# <a name="using-a-local-user-account-as-a-service-logon-account"></a><span data-ttu-id="68069-103">Utilisation d’un compte d’utilisateur local en tant que compte d’ouverture de session de service</span><span class="sxs-lookup"><span data-stu-id="68069-103">Using a Local User Account as a Service Logon Account</span></span>

<span data-ttu-id="68069-104">Un compte d’utilisateur local (format de nom : ". \\ *Username*") existe uniquement dans la base de données Sam de l’ordinateur hôte ; Il n’a pas d’objet utilisateur dans Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="68069-104">A local user account (name format: ".\\*UserName*") exists only in the SAM database of the host computer; it does not have a user object in Active Directory Domain Services.</span></span> <span data-ttu-id="68069-105">Cela signifie qu’un compte local ne peut pas être authentifié par le domaine.</span><span class="sxs-lookup"><span data-stu-id="68069-105">This means that a local account cannot be authenticated by the domain.</span></span> <span data-ttu-id="68069-106">Par conséquent, un service qui s’exécute dans le contexte de sécurité d’un compte d’utilisateur local n’a pas accès aux ressources réseau (sauf s’il s’agit d’un utilisateur anonyme) et il ne peut pas prendre en charge l’authentification mutuelle Kerberos dans laquelle le service est authentifié par ses clients.</span><span class="sxs-lookup"><span data-stu-id="68069-106">Consequently, a service that runs in the security context of a local user account does not have access to network resources (except as an anonymous user), and it cannot support Kerberos mutual authentication in which the service is authenticated by its clients.</span></span> <span data-ttu-id="68069-107">Pour ces raisons, les comptes d’utilisateur locaux sont généralement inappropriés pour les services d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="68069-107">For these reasons, local user accounts are typically inappropriate for directory-enabled services.</span></span> <span data-ttu-id="68069-108">Côté plus, les bogues dans le service ne peuvent pas endommager le système.</span><span class="sxs-lookup"><span data-stu-id="68069-108">On the plus side, bugs in the service cannot damage the system.</span></span> <span data-ttu-id="68069-109">Si votre service peut s’exécuter sous ces limites, il doit le faire.</span><span class="sxs-lookup"><span data-stu-id="68069-109">If your service can run under those limitations, it should.</span></span>

 

 




