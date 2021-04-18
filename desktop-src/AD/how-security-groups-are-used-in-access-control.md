---
title: Utilisation des groupes de sécurité dans les Access Control
description: L’identificateur de sécurité (SID) est l’identificateur d’objet de l’utilisateur ou du groupe de sécurité lorsque l’utilisateur ou le groupe est utilisé à des fins de sécurité.
ms.assetid: 3236c51f-21c1-4c07-9b76-2668ae72a42f
ms.tgt_platform: multiple
keywords:
- Utilisation des groupes de sécurité dans les Access Control
- contrôle d’accès, groupes de sécurité utilisés dans
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf7096e32c64fe420ca6625378725ce8e4864beb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512019"
---
# <a name="how-security-groups-are-used-in-access-control"></a><span data-ttu-id="78928-105">Utilisation des groupes de sécurité dans les Access Control</span><span class="sxs-lookup"><span data-stu-id="78928-105">How Security Groups are Used in Access Control</span></span>

<span data-ttu-id="78928-106">L’identificateur de sécurité (SID) est l’identificateur d’objet de l’utilisateur ou du groupe de sécurité lorsque l’utilisateur ou le groupe est utilisé à des fins de sécurité.</span><span class="sxs-lookup"><span data-stu-id="78928-106">The security identifier (SID) is the object identifier of the user or security group when the user or group is used for security purposes.</span></span> <span data-ttu-id="78928-107">Le nom de l’utilisateur ou du groupe n’est pas utilisé en tant qu’identificateur unique dans le système.</span><span class="sxs-lookup"><span data-stu-id="78928-107">The name of the user or group is not used as the unique identifier within the system.</span></span> <span data-ttu-id="78928-108">Le SID est stocké dans l’attribut **objectSID** des objets utilisateur et groupe de sécurité.</span><span class="sxs-lookup"><span data-stu-id="78928-108">The SID is stored in the **objectSid** attribute of user objects and security group objects.</span></span> <span data-ttu-id="78928-109">Le serveur Active Directory génère l' **objectSID** lorsque l’utilisateur ou le groupe est créé.</span><span class="sxs-lookup"><span data-stu-id="78928-109">The Active Directory server generates the **objectSid** when the user or group is created.</span></span> <span data-ttu-id="78928-110">Le système garantit que les SID sont uniques dans une forêt.</span><span class="sxs-lookup"><span data-stu-id="78928-110">The system ensures that the SIDs are unique across a forest.</span></span> <span data-ttu-id="78928-111">N’oubliez pas que l' **objectGUID** est l’identificateur unique d’un utilisateur, d’un groupe ou d’un autre objet annuaire.</span><span class="sxs-lookup"><span data-stu-id="78928-111">Be aware that the **objectGuid** is the unique identifier of a user, group, or any other directory object.</span></span> <span data-ttu-id="78928-112">Le SID change si un utilisateur ou un groupe est déplacé vers un autre domaine. l' **objectGUID** reste le même.</span><span class="sxs-lookup"><span data-stu-id="78928-112">The SID changes if a user or group is moved to another domain; the **objectGuid** remains the same.</span></span>

<span data-ttu-id="78928-113">Lorsqu’un utilisateur ou un groupe a l’autorisation d’accéder à une ressource, telle qu’une imprimante ou un partage de fichiers, le SID de l’utilisateur ou du groupe est ajouté à l’entrée de contrôle d’accès (ACE) définissant l’autorisation accordée dans la liste de contrôle d’accès discrétionnaire (DACL) de la ressource.</span><span class="sxs-lookup"><span data-stu-id="78928-113">When a user or group is given permission to access a resource, such as a printer or a file share, the SID of the user or group is added to the access control entry (ACE) defining the granted permission in the resource's discretionary access control list (DACL).</span></span> <span data-ttu-id="78928-114">Dans Active Directory Domain Services, chaque objet a un attribut **ntSecurityDescriptor** qui stocke une liste DACL définissant l’accès à cet objet ou aux attributs particuliers sur cet objet.</span><span class="sxs-lookup"><span data-stu-id="78928-114">In Active Directory Domain Services, each object has an **nTSecurityDescriptor** attribute that stores a DACL defining the access to that particular object or attributes on that object.</span></span> <span data-ttu-id="78928-115">Pour plus d’informations sur la définition du contrôle d’accès sur des objets dans Active Directory Domain Services, consultez [contrôle de l’accès aux objets dans Active Directory Domain Services](controlling-access-to-objects-in-active-directory-domain-services.md).</span><span class="sxs-lookup"><span data-stu-id="78928-115">For more information about setting access control on objects in Active Directory Domain Services, see [Controlling Access to Objects in Active Directory Domain Services](controlling-access-to-objects-in-active-directory-domain-services.md).</span></span>

<span data-ttu-id="78928-116">Lorsqu’un utilisateur se connecte à un domaine Windows 2000, le système d’exploitation génère un jeton d’accès.</span><span class="sxs-lookup"><span data-stu-id="78928-116">When a user logs on to a Windows 2000 domain, the operating system generates an access token.</span></span> <span data-ttu-id="78928-117">Ce jeton d’accès est utilisé pour déterminer les ressources auxquelles l’utilisateur peut accéder.</span><span class="sxs-lookup"><span data-stu-id="78928-117">This access token is used to determine which resources the user may access.</span></span> <span data-ttu-id="78928-118">Le jeton d’accès utilisateur contient les données suivantes :</span><span class="sxs-lookup"><span data-stu-id="78928-118">The user access token includes the following data:</span></span>

-   <span data-ttu-id="78928-119">SID de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="78928-119">User SID.</span></span>
-   <span data-ttu-id="78928-120">SID de tous les groupes de sécurité globaux et universels dont l’utilisateur est membre.</span><span class="sxs-lookup"><span data-stu-id="78928-120">SIDs of all global and universal security groups that the user is a member of.</span></span>
-   <span data-ttu-id="78928-121">SID de tous les groupes de sécurité globaux et universels imbriqués.</span><span class="sxs-lookup"><span data-stu-id="78928-121">SIDs of all nested global and universal security groups.</span></span>

<span data-ttu-id="78928-122">Chaque processus exécuté pour le compte de cet utilisateur dispose d’une copie de ce jeton d’accès.</span><span class="sxs-lookup"><span data-stu-id="78928-122">Every process executed on behalf of this user has a copy of this access token.</span></span>

<span data-ttu-id="78928-123">Lorsque l’utilisateur tente d’accéder à des ressources sur un ordinateur, le service par le biais duquel l’utilisateur accède à la ressource empruntera l’identité de l’utilisateur en créant un nouveau jeton d’accès basé sur le jeton d’accès créé au moment de l’ouverture de session de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="78928-123">When the user attempts to access resources on a computer, the service through which the user accesses the resource will impersonate the user by creating a new access token based on the access token created at user logon time.</span></span> <span data-ttu-id="78928-124">Ce nouveau jeton d’accès contient également les SID suivants :</span><span class="sxs-lookup"><span data-stu-id="78928-124">This new access token will also contain the following SIDs:</span></span>

-   <span data-ttu-id="78928-125">Sid pour tous les groupes locaux de domaine dans le domaine cible dont l’utilisateur est membre.</span><span class="sxs-lookup"><span data-stu-id="78928-125">SIDs for all domain local groups in the target domain that the user is a member of.</span></span>
-   <span data-ttu-id="78928-126">Sid pour tous les groupes locaux de l’ordinateur sur l’ordinateur cible dont l’utilisateur est membre.</span><span class="sxs-lookup"><span data-stu-id="78928-126">SIDs for all machine local groups on the target computer that the user is a member of.</span></span>

<span data-ttu-id="78928-127">Le service utilise ce nouveau jeton d’accès pour évaluer l’accès à la ressource.</span><span class="sxs-lookup"><span data-stu-id="78928-127">The service uses this new access token to evaluate access to the resource.</span></span> <span data-ttu-id="78928-128">Si un SID dans le jeton d’accès apparaît dans des ACE dans la liste DACL, le service accorde à l’utilisateur les autorisations spécifiées dans ces entrées de du texte.</span><span class="sxs-lookup"><span data-stu-id="78928-128">If a SID in the access token appears in any ACEs in the DACL, the service gives the user the permissions specified in those ACEs.</span></span>

 

 




