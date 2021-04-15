---
description: WMI s’appuie sur les descripteurs de sécurité Windows standard pour contrôler et protéger l’accès aux objets sécurisables tels que les espaces de noms WMI, les imprimantes, les services et les applications DCOM.
ms.assetid: 5893457d-3fc2-4d64-a6c2-0f410052ce52
ms.tgt_platform: multiple
title: Accès aux objets sécurisables WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad4ea78cd45d57856b0909283e7c2624fb26bd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210220"
---
# <a name="access-to-wmi-securable-objects"></a><span data-ttu-id="8db0d-103">Accès aux objets sécurisables WMI</span><span class="sxs-lookup"><span data-stu-id="8db0d-103">Access to WMI Securable Objects</span></span>

<span data-ttu-id="8db0d-104">WMI s’appuie sur les [*descripteurs de sécurité*](/windows/desktop/SecGloss/s-gly) Windows standard pour contrôler et protéger l’accès aux objets sécurisables tels que les espaces de noms WMI, les imprimantes, les services et les applications DCOM.</span><span class="sxs-lookup"><span data-stu-id="8db0d-104">WMI relies on standard Windows [*security descriptors*](/windows/desktop/SecGloss/s-gly) to control and protect access to securable objects like WMI namespaces, printers, services, and DCOM applications.</span></span> <span data-ttu-id="8db0d-105">Pour plus d’informations, consultez [accès aux espaces de noms WMI](access-to-wmi-namespaces.md).</span><span class="sxs-lookup"><span data-stu-id="8db0d-105">For more information, see [Access to WMI Namespaces](access-to-wmi-namespaces.md).</span></span>

<span data-ttu-id="8db0d-106">Les rubriques suivantes sont présentées dans cette section :</span><span class="sxs-lookup"><span data-stu-id="8db0d-106">The following topics are discussed in this section:</span></span>

-   [<span data-ttu-id="8db0d-107">Descripteurs de sécurité et sid</span><span class="sxs-lookup"><span data-stu-id="8db0d-107">Security Descriptors and SIDs</span></span>](#security-descriptors-and-sids)
-   [<span data-ttu-id="8db0d-108">Contrôle d’accès</span><span class="sxs-lookup"><span data-stu-id="8db0d-108">Access Control</span></span>](#access-control)
-   [<span data-ttu-id="8db0d-109">Modification de la sécurité d’accès</span><span class="sxs-lookup"><span data-stu-id="8db0d-109">Changing Access Security</span></span>](#changing-access-security)
-   [<span data-ttu-id="8db0d-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8db0d-110">Related topics</span></span>](#related-topics)

## <a name="security-descriptors-and-sids"></a><span data-ttu-id="8db0d-111">Descripteurs de sécurité et sid</span><span class="sxs-lookup"><span data-stu-id="8db0d-111">Security Descriptors and SIDs</span></span>

<span data-ttu-id="8db0d-112">WMI maintient la sécurité d’accès en comparant le [*jeton d’accès*](/windows/desktop/SecGloss/a-gly) de l’utilisateur qui tente d’accéder à un objet sécurisable avec le descripteur de sécurité de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8db0d-112">WMI maintains access security by comparing the [*access token*](/windows/desktop/SecGloss/a-gly) of the user that attempts to access a securable object with the security descriptor of the object.</span></span>

<span data-ttu-id="8db0d-113">Lorsqu’un utilisateur ou un groupe est créé sur un système, le SID s’assure [*qu’un compte*](/windows/desktop/SecGloss/s-gly) créé avec le même nom qu’un compte supprimé précédemment n’hérite pas des paramètres de sécurité précédents.</span><span class="sxs-lookup"><span data-stu-id="8db0d-113">When a user or group is created on a system, the account is given a [*security identifier (SID)*](/windows/desktop/SecGloss/s-gly) The SID ensures that an account created with the same name as a previously deleted account does not inherit the previous security settings.</span></span> <span data-ttu-id="8db0d-114">Un jeton d’accès est créé en combinant le SID, la liste des groupes dont l’utilisateur est membre et la liste des privilèges activés ou désactivés.</span><span class="sxs-lookup"><span data-stu-id="8db0d-114">An access token is created by combining the SID, the list of groups of which the user is a member, and the list of enabled or disabled privileges.</span></span> <span data-ttu-id="8db0d-115">Ces jetons sont affectés à tous les processus et threads appartenant à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8db0d-115">These tokens are assigned to all processes and threads owned by the user.</span></span>

## <a name="access-control"></a><span data-ttu-id="8db0d-116">Contrôle d’accès</span><span class="sxs-lookup"><span data-stu-id="8db0d-116">Access Control</span></span>

<span data-ttu-id="8db0d-117">Lorsque l’utilisateur souhaite utiliser un objet sécurisé, le jeton d’accès est comparé à la [*liste de contrôle d’accès discrétionnaire (DACL, Discretionary Access Control List)*](/windows/desktop/SecGloss/d-gly) dans le descripteur de sécurité de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8db0d-117">When the user wants to use a secured object, the access token is compared with the [*discretionary access control list (DACL)*](/windows/desktop/SecGloss/d-gly) in the security descriptor on the object.</span></span> <span data-ttu-id="8db0d-118">La liste DACL contient des autorisations appelées [*entrées de contrôle d’accès (ACE)*](/windows/desktop/SecGloss/a-gly).</span><span class="sxs-lookup"><span data-stu-id="8db0d-118">The DACL contains permissions called [*access control entries (ACE)*](/windows/desktop/SecGloss/a-gly).</span></span> <span data-ttu-id="8db0d-119">Les [*listes de contrôle d’accès système (SACL)*](/windows/desktop/SecGloss/s-gly) font la même chose que les DACL, mais elles peuvent générer des événements d’audit de sécurité.</span><span class="sxs-lookup"><span data-stu-id="8db0d-119">[*System access control lists (SACL)*](/windows/desktop/SecGloss/s-gly) do the same thing as DACLs, but can generate security audit events.</span></span> <span data-ttu-id="8db0d-120">À compter de Windows Vista, WMI peut créer des entrées d’audit dans le journal de sécurité Windows.</span><span class="sxs-lookup"><span data-stu-id="8db0d-120">Starting with Windows Vista, WMI can make auditing entries in the Windows Security Log.</span></span> <span data-ttu-id="8db0d-121">Pour plus d’informations sur l’audit dans WMI, consultez [accès aux espaces de noms WMI](access-to-wmi-namespaces.md).</span><span class="sxs-lookup"><span data-stu-id="8db0d-121">For more information about auditing in WMI, see [Access to WMI Namespaces](access-to-wmi-namespaces.md).</span></span>

<span data-ttu-id="8db0d-122">Les listes DACL et SACL se composent toutes deux d’une liste d’entrées de contrôle d’accès qui décrivent les utilisateurs ayant des droits d’accès spécifiques, y compris l’écriture dans le référentiel WMI, l’accès et l’exécution à distance et les autorisations d’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="8db0d-122">Both the DACL and the SACL consist of a list of ACEs that describe which users have specific access rights, including writing to the WMI repository, remote access and execution, and logon permissions.</span></span> <span data-ttu-id="8db0d-123">WMI stocke ces listes de contrôle d’accès dans l’espace de stockage WMI.</span><span class="sxs-lookup"><span data-stu-id="8db0d-123">WMI stores these ACLs in the WMI repository.</span></span>

<span data-ttu-id="8db0d-124">Les ACE contiennent trois types de niveaux d’accès ou des droits accord/refus : autoriser, refuser pour DACL et audit système (pour les listes SACL).</span><span class="sxs-lookup"><span data-stu-id="8db0d-124">ACEs hold three types of access levels or grant/deny rights: allow, deny for DACL, and system audit (for SACLs).</span></span> <span data-ttu-id="8db0d-125">Les ACE de refus précèdent les ACE Allow dans la liste DACL ou SACL.</span><span class="sxs-lookup"><span data-stu-id="8db0d-125">Deny ACEs precede allow ACEs in the DACL or SACL.</span></span> <span data-ttu-id="8db0d-126">Lors de la vérification des droits d’accès utilisateur, WMI s’exécute de manière consécutive via la liste de contrôle d’accès jusqu’à ce qu’il trouve un ACE Allow qui s’applique au jeton d’accès demandeur.</span><span class="sxs-lookup"><span data-stu-id="8db0d-126">When checking the user access rights, WMI runs consecutively through the access control list until it finds an allow ACE that applies to the requesting access token.</span></span> <span data-ttu-id="8db0d-127">Les ACE restantes ne sont pas vérifiées après ce point.</span><span class="sxs-lookup"><span data-stu-id="8db0d-127">The remaining ACEs are not checked after this point.</span></span> <span data-ttu-id="8db0d-128">Si aucun ACE allow approprié n’est trouvé, l’accès est refusé.</span><span class="sxs-lookup"><span data-stu-id="8db0d-128">If no appropriate allow ACE is found, then access is denied.</span></span> <span data-ttu-id="8db0d-129">Pour plus d’informations, consultez [ordre des entrées de commande dans une liste DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl) et [création d’une liste DACL](/windows/desktop/SecBP/creating-a-dacl).</span><span class="sxs-lookup"><span data-stu-id="8db0d-129">For more information, see [Order of ACEs in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl) and [Creating a DACL](/windows/desktop/SecBP/creating-a-dacl).</span></span>

## <a name="changing-access-security"></a><span data-ttu-id="8db0d-130">Modification de la sécurité d’accès</span><span class="sxs-lookup"><span data-stu-id="8db0d-130">Changing Access Security</span></span>

<span data-ttu-id="8db0d-131">Avec les autorisations appropriées, vous pouvez modifier la sécurité sur un objet sécurisable à l’aide d’un script ou d’une application.</span><span class="sxs-lookup"><span data-stu-id="8db0d-131">With appropriate permissions, you can change the security on a securable object with a script or application.</span></span> <span data-ttu-id="8db0d-132">Vous pouvez également modifier les paramètres de sécurité sur les espaces de noms WMI à l’aide du [*contrôle WMI*](gloss-w.md) ou en ajoutant une chaîne [SDDL (Security Descriptor Definition Language)](/windows/desktop/SecAuthZ/security-descriptor-definition-language) dans le fichier [*format MOF (MOF)*](gloss-m.md) qui définit les classes de l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="8db0d-132">You can also change the security settings on WMI namespaces using the [*WMI Control*](gloss-w.md) or by adding a [Security Descriptor Definition Language (SDDL)](/windows/desktop/SecAuthZ/security-descriptor-definition-language) string in the [*Managed Object Format (MOF)*](gloss-m.md) file that defines classes for the namespace.</span></span> <span data-ttu-id="8db0d-133">Pour plus d’informations, consultez [accès aux espaces de noms WMI](access-to-wmi-namespaces.md), [sécurisation des espaces de noms WMI](securing-wmi-namespaces.md)et [modification de la sécurité d’accès sur les objets sécurisables](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="8db0d-133">For more information, see [Access to WMI Namespaces](access-to-wmi-namespaces.md), [Securing WMI Namespaces](securing-wmi-namespaces.md), and [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8db0d-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8db0d-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8db0d-135">Objets descripteurs de sécurité WMI</span><span class="sxs-lookup"><span data-stu-id="8db0d-135">WMI Security Descriptor Objects</span></span>](wmi-security-descriptor-objects.md)
</dt> <dt>

[<span data-ttu-id="8db0d-136">Constantes de sécurité WMI</span><span class="sxs-lookup"><span data-stu-id="8db0d-136">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="8db0d-137">Contrôle de compte d’utilisateur et WMI</span><span class="sxs-lookup"><span data-stu-id="8db0d-137">User Account Control and WMI</span></span>](user-account-control-and-wmi.md)
</dt> <dt>

[<span data-ttu-id="8db0d-138">Objets descripteurs de sécurité WMI</span><span class="sxs-lookup"><span data-stu-id="8db0d-138">WMI Security Descriptor Objects</span></span>](wmi-security-descriptor-objects.md)
</dt> <dt>

[<span data-ttu-id="8db0d-139">Accès aux espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="8db0d-139">Access to WMI Namespaces</span></span>](access-to-wmi-namespaces.md)
</dt> </dl>

 

 
