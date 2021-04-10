---
title: Services d’annuaire aujourd’hui
description: Il est courant de trouver plusieurs répertoires d’administration déployés au sein d’une même organisation.
ms.assetid: e6f05beb-d88d-46d5-85c7-3477a6af03c9
ms.tgt_platform: multiple
keywords:
- ADSI des services d’annuaire
- ADSI des services d’annuaire, arrière-plan pour les services d’annuaire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38e6a6e5dfd1e0f8fc3f87d407bbbce28caa0696
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104190742"
---
# <a name="directory-services-today"></a><span data-ttu-id="f8a36-105">Services d’annuaire aujourd’hui</span><span class="sxs-lookup"><span data-stu-id="f8a36-105">Directory Services Today</span></span>

<span data-ttu-id="f8a36-106">Il est courant de trouver plusieurs répertoires d’administration déployés au sein d’une même organisation.</span><span class="sxs-lookup"><span data-stu-id="f8a36-106">It is common to find multiple administrative directories deployed within a single organization.</span></span> <span data-ttu-id="f8a36-107">Ces répertoires incluent des répertoires de ressources réseau, tels que les annuaires LDAP tels que le service d’annuaire Microsoft Active Directory, le service d’annuaire de système d’exploitation Windows, ainsi que les répertoires spécifiques à l’application, tels que Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="f8a36-107">These directories include network resource directories, such as LDAP-based directories like Microsoft Active Directory directory service, Windows operating system directory service, as well as application-specific directories, such as Microsoft Exchange.</span></span>

![déploiement de plusieurs annuaires](images/ds2chal.png)

## <a name="the-directory-challenge"></a><span data-ttu-id="f8a36-109">Le défi de l’annuaire</span><span class="sxs-lookup"><span data-stu-id="f8a36-109">The Directory Challenge</span></span>

<span data-ttu-id="f8a36-110">Dans l’organisation, plusieurs annuaires présentent des défis complexes pour les utilisateurs, les administrateurs et les développeurs.</span><span class="sxs-lookup"><span data-stu-id="f8a36-110">Multiple directories in the organization pose complex challenges to users, administrators, and developers.</span></span> <span data-ttu-id="f8a36-111">Ces problèmes ont un déploiement limité de répertoires étendus.</span><span class="sxs-lookup"><span data-stu-id="f8a36-111">These problems have limited wide-directory deployment.</span></span> <span data-ttu-id="f8a36-112">Les utilisateurs sont confrontés à plusieurs ouvertures de session et à différentes interfaces pour les informations dans plusieurs annuaires.</span><span class="sxs-lookup"><span data-stu-id="f8a36-112">Users face multiple logons and a variety of interfaces to information across multiple directories.</span></span> <span data-ttu-id="f8a36-113">Les administrateurs sont confrontés à la complexité de la gestion de plusieurs annuaires.</span><span class="sxs-lookup"><span data-stu-id="f8a36-113">Administrators face the complexity of managing multiple directories.</span></span> <span data-ttu-id="f8a36-114">Les utilisateurs finaux et les administrateurs veulent que les développeurs d’applications utilisent un annuaire d’administration existant, mais les développeurs sont confrontés à un dilemme sur lequel utiliser.</span><span class="sxs-lookup"><span data-stu-id="f8a36-114">End users and administrators want application developers to use an existing administrative directory, but developers face a dilemma about which one to use.</span></span> <span data-ttu-id="f8a36-115">Chaque annuaire offre des interfaces d’application uniques.</span><span class="sxs-lookup"><span data-stu-id="f8a36-115">Each directory offers unique application interfaces.</span></span> <span data-ttu-id="f8a36-116">Un développeur doit choisir une implémentation d’annuaire spécifique ou prendre en charge plusieurs versions de son application.</span><span class="sxs-lookup"><span data-stu-id="f8a36-116">A developer must choose a specific directory implementation, or support multiple versions of their application.</span></span> <span data-ttu-id="f8a36-117">Par conséquent, les développeurs utilisent rarement des services d’annuaire existants.</span><span class="sxs-lookup"><span data-stu-id="f8a36-117">As a result, developers rarely use existing directory services.</span></span>

 

 




