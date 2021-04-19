---
description: Une entrée de contrôle d’accès (ACE) est un élément dans une liste de contrôle d’accès (ACL).
ms.assetid: 9cf4d796-3955-456b-9db9-ae9fa83752f6
title: Entrées Access Control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49fe98cf1c1c4d5fb23091a6539564ff964202cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527432"
---
# <a name="access-control-entries"></a><span data-ttu-id="ad49e-103">Entrées Access Control</span><span class="sxs-lookup"><span data-stu-id="ad49e-103">Access Control Entries</span></span>

<span data-ttu-id="ad49e-104">Une [*entrée de contrôle*](/windows/desktop/SecGloss/a-gly) d’accès (ACE) est un élément dans une [*liste de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACL).</span><span class="sxs-lookup"><span data-stu-id="ad49e-104">An [*access control entry*](/windows/desktop/SecGloss/a-gly) (ACE) is an element in an [*access control list*](/windows/desktop/SecGloss/a-gly) (ACL).</span></span> <span data-ttu-id="ad49e-105">Une liste de contrôle d’accès peut avoir zéro ou plusieurs entrées de contrôle d’accès.</span><span class="sxs-lookup"><span data-stu-id="ad49e-105">An ACL can have zero or more ACEs.</span></span> <span data-ttu-id="ad49e-106">Chaque ACE contrôle ou surveille l’accès à un objet par un tiers de confiance spécifié.</span><span class="sxs-lookup"><span data-stu-id="ad49e-106">Each ACE controls or monitors access to an object by a specified trustee.</span></span> <span data-ttu-id="ad49e-107">Pour plus d’informations sur l’ajout, la suppression ou la modification des entrées du contrôle d’accès dans les listes de contrôle d’accès d’un objet, consultez [modification des listes de contrôle d’accès d’un objet en C++](modifying-the-acls-of-an-object-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="ad49e-107">For information about adding, removing, or changing the ACEs in an object's ACLs, see [Modifying the ACLs of an Object in C++](modifying-the-acls-of-an-object-in-c--.md).</span></span>

<span data-ttu-id="ad49e-108">Il existe six types d’ACE, dont trois sont pris en charge par tous les objets sécurisables.</span><span class="sxs-lookup"><span data-stu-id="ad49e-108">There are six types of ACEs, three of which are supported by all securable objects.</span></span> <span data-ttu-id="ad49e-109">Les trois autres types sont des [ACE spécifiques](object-specific-aces.md) aux objets pris en charge par les objets de service d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="ad49e-109">The other three types are [Object-specific ACEs](object-specific-aces.md) supported by directory service objects.</span></span>

<span data-ttu-id="ad49e-110">Tous les types d’ACE contiennent les informations de contrôle d’accès suivantes :</span><span class="sxs-lookup"><span data-stu-id="ad49e-110">All types of ACEs contain the following access control information:</span></span>

-   <span data-ttu-id="ad49e-111">[Identificateur de sécurité](security-identifiers.md) (SID) qui identifie le [tiers de confiance](trustees.md) auquel l’entrée du contrôle d’accès s’applique.</span><span class="sxs-lookup"><span data-stu-id="ad49e-111">A [security identifier](security-identifiers.md) (SID) that identifies the [trustee](trustees.md) to which the ACE applies.</span></span>
-   <span data-ttu-id="ad49e-112">[*Masque d’accès*](/windows/desktop/SecGloss/a-gly) qui spécifie les [droits d’accès](access-rights-and-access-masks.md) contrôlés par l’entrée du contrôle d’accès.</span><span class="sxs-lookup"><span data-stu-id="ad49e-112">An [*access mask*](/windows/desktop/SecGloss/a-gly) that specifies the [access rights](access-rights-and-access-masks.md) controlled by the ACE.</span></span>
-   <span data-ttu-id="ad49e-113">Indicateur qui spécifie le type d’entrée du contrôle d’accès.</span><span class="sxs-lookup"><span data-stu-id="ad49e-113">A flag that indicates the type of ACE.</span></span>
-   <span data-ttu-id="ad49e-114">Jeu d’indicateurs de bits qui déterminent si les conteneurs enfants ou les objets peuvent hériter de l’entrée du contrôle d’accès de l’objet principal auquel la liste ACL est attachée.</span><span class="sxs-lookup"><span data-stu-id="ad49e-114">A set of bit flags that determine whether child containers or objects can inherit the ACE from the primary object to which the ACL is attached.</span></span>

<span data-ttu-id="ad49e-115">Le tableau suivant répertorie les trois types d’entrées du contrôle d’accès pris en charge par tous les objets sécurisables.</span><span class="sxs-lookup"><span data-stu-id="ad49e-115">The following table lists the three ACE types supported by all securable objects.</span></span>



| <span data-ttu-id="ad49e-116">Type</span><span class="sxs-lookup"><span data-stu-id="ad49e-116">Type</span></span>               | <span data-ttu-id="ad49e-117">Description</span><span class="sxs-lookup"><span data-stu-id="ad49e-117">Description</span></span>                                                                                                                                                                                                                                      |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad49e-118">ACE accès refusé</span><span class="sxs-lookup"><span data-stu-id="ad49e-118">Access-denied ACE</span></span>  | <span data-ttu-id="ad49e-119">Utilisé dans une [*liste de contrôle d’accès discrétionnaire*](/windows/desktop/SecGloss/d-gly) (DACL) pour refuser les droits d’accès à un tiers de confiance.</span><span class="sxs-lookup"><span data-stu-id="ad49e-119">Used in a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) to deny access rights to a trustee.</span></span>                                       |
| <span data-ttu-id="ad49e-120">Accès-ACE autorisé</span><span class="sxs-lookup"><span data-stu-id="ad49e-120">Access-allowed ACE</span></span> | <span data-ttu-id="ad49e-121">Utilisé dans une liste DACL pour autoriser les droits d’accès à un tiers de confiance.</span><span class="sxs-lookup"><span data-stu-id="ad49e-121">Used in a DACL to allow access rights to a trustee.</span></span>                                                                                                                                                                                              |
| <span data-ttu-id="ad49e-122">ACE système-audit</span><span class="sxs-lookup"><span data-stu-id="ad49e-122">System-audit ACE</span></span>   | <span data-ttu-id="ad49e-123">Utilisé dans une [*liste de contrôle d’accès système*](/windows/desktop/SecGloss/s-gly) (SACL) pour générer un enregistrement d’audit lorsque le tiers de confiance tente d’exercer les droits d’accès spécifiés.</span><span class="sxs-lookup"><span data-stu-id="ad49e-123">Used in a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL) to generate an audit record when the trustee attempts to exercise the specified access rights.</span></span> |



 

<span data-ttu-id="ad49e-124">Pour obtenir une table des ACE spécifiques aux objets, consultez [ACE spécifiques aux objets](object-specific-aces.md).</span><span class="sxs-lookup"><span data-stu-id="ad49e-124">For a table of object-specific ACEs, see [Object-specific ACEs](object-specific-aces.md).</span></span>

> [!Note]  
> <span data-ttu-id="ad49e-125">Les ACE de l’objet System-Alarm ne sont pas prises en charge actuellement.</span><span class="sxs-lookup"><span data-stu-id="ad49e-125">System-alarm object ACEs are not currently supported.</span></span>

 

 

 
