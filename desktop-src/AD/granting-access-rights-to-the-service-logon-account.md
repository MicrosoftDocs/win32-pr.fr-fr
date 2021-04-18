---
title: Octroi de droits d’accès au compte d’ouverture de session du service
description: L’un des principaux points à prendre en compte lors de l’installation d’une instance de service est de s’assurer que le service installé peut accéder aux ressources nécessaires.
ms.assetid: 5b756318-f621-4fce-af2b-71ccccbb4e3c
ms.tgt_platform: multiple
keywords:
- Octroi de droits d’accès à l’AD du compte d’ouverture de session du service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f4ea5b85e6158109338b881eeb3f59d74a3910
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "106511886"
---
# <a name="granting-access-rights-to-the-service-logon-account"></a><span data-ttu-id="a48c9-104">Octroi de droits d’accès au compte d’ouverture de session du service</span><span class="sxs-lookup"><span data-stu-id="a48c9-104">Granting Access Rights to the Service Logon Account</span></span>

<span data-ttu-id="a48c9-105">L’un des principaux points à prendre en compte lors de l’installation d’une instance de service est de s’assurer que le service installé peut accéder aux ressources nécessaires.</span><span class="sxs-lookup"><span data-stu-id="a48c9-105">A primary consideration of installing a service instance is to ensure that the installed service can access the necessary resources.</span></span> <span data-ttu-id="a48c9-106">Pour ce faire, définissez les ACE dans les descripteurs de sécurité des objets auxquels le service doit accéder.</span><span class="sxs-lookup"><span data-stu-id="a48c9-106">To do this, set ACEs in the security descriptors of objects that the service must access.</span></span> <span data-ttu-id="a48c9-107">Un ACE peut accorder ou refuser des droits d’accès à un principal de sécurité spécifié, tel que le compte d’utilisateur du service, ou le compte d’ordinateur pour un service LocalSystem, ou un groupe auquel appartient le compte du service.</span><span class="sxs-lookup"><span data-stu-id="a48c9-107">An ACE can grant or deny access rights to a specified security principal, such as the service user account, or the computer account for a LocalSystem service, or a group to which the service's account belongs.</span></span> <span data-ttu-id="a48c9-108">Pour plus d’informations sur les ACE, les descripteurs de sécurité et le contrôle d’accès, consultez [contrôle de l’accès aux objets dans Active Directory Domain Services](controlling-access-to-objects-in-active-directory-domain-services.md) et [Access Control](/windows/desktop/SecAuthZ/access-control).</span><span class="sxs-lookup"><span data-stu-id="a48c9-108">For more information about ACEs, security descriptors, and access control, see [Controlling Access to objects in Active Directory Domain Services](controlling-access-to-objects-in-active-directory-domain-services.md) and [Access Control](/windows/desktop/SecAuthZ/access-control).</span></span>

<span data-ttu-id="a48c9-109">Pour plus d’informations et pour obtenir un exemple de code qui peut être utilisé pour définir une entrée du contrôle d’accès qui permet au service de modifier son point de connexion de service, consultez [activation du compte de service pour accéder aux propriétés SCP](enabling-service-account-to-access-scp-properties.md).</span><span class="sxs-lookup"><span data-stu-id="a48c9-109">For more information and a code example that can be used to set an ACE that enables the service to modify its service connection point, see [Enabling Service Account to Access SCP Properties](enabling-service-account-to-access-scp-properties.md).</span></span>

<span data-ttu-id="a48c9-110">Dans certains cas, vous devez ajouter votre compte d’utilisateur de service en tant que membre d’un ou de plusieurs groupes de sécurité.</span><span class="sxs-lookup"><span data-stu-id="a48c9-110">In some cases, you must add your service user account as a member of one or more security groups.</span></span> <span data-ttu-id="a48c9-111">Par exemple, si vous créez un groupe administrateurs pour votre service, vous pouvez faire en sorte que le service soit membre du groupe.</span><span class="sxs-lookup"><span data-stu-id="a48c9-111">For example, if you create an administrators group for your service, you might make the service a member of the group.</span></span> <span data-ttu-id="a48c9-112">Vous pouvez ensuite accorder des droits d’accès au groupe plutôt que de les accorder explicitement au compte de service.</span><span class="sxs-lookup"><span data-stu-id="a48c9-112">You can then grant access rights to the group rather than granting them explicitly to the service account.</span></span> <span data-ttu-id="a48c9-113">Pour plus d’informations sur les groupes de sécurité, consultez [gestion des groupes](managing-groups.md).</span><span class="sxs-lookup"><span data-stu-id="a48c9-113">For more information about security groups, see [Managing Groups](managing-groups.md).</span></span>

 

 