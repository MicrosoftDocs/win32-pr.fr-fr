---
description: L’objectif de la règle de stratégie d’autorisation centrale (CAPR) est de fournir une définition à l’ensemble du domaine d’un aspect isolé de la stratégie d’autorisation des organisations.
ms.assetid: 51436332-F06A-4929-B3C1-AD2F66C3273B
title: Règle de stratégie d’autorisation centrale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cda6279b2bf28f80f99a0e2608b5bf209855a76a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042878"
---
# <a name="central-authorization-policy-rule"></a><span data-ttu-id="74c22-103">Règle de stratégie d’autorisation centrale</span><span class="sxs-lookup"><span data-stu-id="74c22-103">Central Authorization Policy Rule</span></span>

<span data-ttu-id="74c22-104">L’objectif de la règle de stratégie d’autorisation centrale (CAPR) est de fournir une définition à l’ensemble du domaine d’un aspect isolé de la stratégie d’autorisation de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="74c22-104">The purpose of the Central Authorization Policy Rule (CAPR) is to provide a domain-wide definition of an isolated aspect of the organization's authorization policy.</span></span> <span data-ttu-id="74c22-105">L’administrateur définit le CAPR pour appliquer l’une des exigences d’autorisation spécifiques.</span><span class="sxs-lookup"><span data-stu-id="74c22-105">The administrator defines the CAPR to enforce one of the specific authorization requirements.</span></span> <span data-ttu-id="74c22-106">Étant donné que le CAPR définit une seule exigence spécifique souhaitée de la stratégie d’autorisation, il peut être plus simplement défini et interprété que si toutes les exigences de la stratégie d’autorisation de l’organisation sont compilées dans une définition de stratégie unique.</span><span class="sxs-lookup"><span data-stu-id="74c22-106">Since the CAPR defines only one specific desired requirement of the authorization policy it can be more simply defined and understood than if all the authorization policy requirements of the organization are compiled into a single policy definition.</span></span>

<span data-ttu-id="74c22-107">CAPR a les attributs suivants :</span><span class="sxs-lookup"><span data-stu-id="74c22-107">The CAPR has the following attributes:</span></span>

-   <span data-ttu-id="74c22-108">Nom : identifie le CAPR pour les administrateurs.</span><span class="sxs-lookup"><span data-stu-id="74c22-108">Name – identifies the CAPR to the administrators.</span></span>
-   <span data-ttu-id="74c22-109">Description : définit l’objectif du CAPR et toutes les informations qui peuvent être nécessaires aux consommateurs du CAPR.</span><span class="sxs-lookup"><span data-stu-id="74c22-109">Description – defines the purpose of the CAPR and any information that may be needed by consumers of the CAPR.</span></span>
-   <span data-ttu-id="74c22-110">Expression d’applicabilité : définit les ressources ou situations dans lesquelles la stratégie sera appliquée.</span><span class="sxs-lookup"><span data-stu-id="74c22-110">Applicability Expression – defines the resources or situations in which the policy will be applied.</span></span>
-   <span data-ttu-id="74c22-111">ID : identificateur à utiliser pour l’audit des modifications apportées au CAPR.</span><span class="sxs-lookup"><span data-stu-id="74c22-111">ID – identifier for use in auditing of changes to the CAPR.</span></span>
-   <span data-ttu-id="74c22-112">Stratégie de Access Control effective : descripteur de sécurité Windows contenant une liste DACL qui définit la stratégie d’autorisation effective.</span><span class="sxs-lookup"><span data-stu-id="74c22-112">Effective Access Control Policy – a Windows security descriptor containing a DACL that defines the effective authorization policy.</span></span>
-   <span data-ttu-id="74c22-113">Expression d’exception : une ou plusieurs expressions qui fournissent un moyen de remplacer la stratégie et d’accorder l’accès à un principal d’après l’évaluation de l’expression.</span><span class="sxs-lookup"><span data-stu-id="74c22-113">Exception Expression – one or more expressions that provide a means to override the policy and grant access to a principal according to the evaluation of the expression.</span></span>
-   <span data-ttu-id="74c22-114">Stratégie de préproduction : descripteur de sécurité Windows facultatif contenant une liste DACL qui définit une stratégie d’autorisation proposée (liste des entrées de contrôle d’accès) qui sera testée par rapport à la stratégie effective, mais non appliquée.</span><span class="sxs-lookup"><span data-stu-id="74c22-114">Staging Policy – an optional Windows security descriptor containing a DACL that defines a proposed authorization policy (list of access control entries) that will be tested against the effective policy but not enforced.</span></span> <span data-ttu-id="74c22-115">S’il existe une différence entre les résultats de la stratégie effective et la stratégie de mise en lots, la différence est enregistrée dans le journal des événements d’audit.</span><span class="sxs-lookup"><span data-stu-id="74c22-115">If there is a difference between the results of the effective policy and the staging policy the difference will be recorded in the audit event log.</span></span>
    -   <span data-ttu-id="74c22-116">Étant donné que la mise en lots peut avoir un effet imprévisible sur les performances du système, un administrateur de stratégie de groupe doit être en mesure de sélectionner des ordinateurs spécifiques sur lesquels la mise en œuvre intermédiaire sera en vigueur.</span><span class="sxs-lookup"><span data-stu-id="74c22-116">Since staging can have an unpredictable effect on system performance, a Group Policy administrator must be able to select specific machines on which staging will be in effect.</span></span> <span data-ttu-id="74c22-117">Cela permet à la stratégie existante d’être en place sur la plupart des ordinateurs d’une unité d’organisation pendant que la mise en lots se produit sur un sous-ensemble de machines.</span><span class="sxs-lookup"><span data-stu-id="74c22-117">This allows the existing policy to be in place on most machines in an OU while staging is happening on a subset of the machines.</span></span>
    -   <span data-ttu-id="74c22-118">P2 : un administrateur local sur un ordinateur particulier doit être en mesure de désactiver la mise en lots si la mise en lots de cet ordinateur entraîne une dégradation des performances.</span><span class="sxs-lookup"><span data-stu-id="74c22-118">P2 – A local administrator on a particular machine should be able to disable staging if staging on that machine is causing too much of a performance degradation.</span></span>
-   <span data-ttu-id="74c22-119">Lien secondaire à CAP : liste des liens vers les liens vers toutes les majuscules qui peuvent faire référence à ce CAPR.</span><span class="sxs-lookup"><span data-stu-id="74c22-119">Backlink to CAP – A list of backlinks to any CAPs that may be referring to this CAPR.</span></span>

<span data-ttu-id="74c22-120">Au cours de la vérification de l’accès, l’applicabilité du CAPR est évaluée en fonction de l’expression d’applicabilité.</span><span class="sxs-lookup"><span data-stu-id="74c22-120">During access check, the CAPR is be evaluated for applicability based on the applicability expression.</span></span> <span data-ttu-id="74c22-121">Si un CAPR est applicable, il est évalué pour déterminer s’il fournit à l’utilisateur demandeur l’accès demandé à la ressource identifiée.</span><span class="sxs-lookup"><span data-stu-id="74c22-121">If a CAPR is applicable, it is evaluated for whether it provides the requesting user the requested access to the identified resource.</span></span> <span data-ttu-id="74c22-122">Les résultats de l’évaluation du Cap sont ensuite joints logiquement par **et** avec les résultats de la liste DACL sur la ressource et les autres CAPRs applicables en vigueur sur la ressource.</span><span class="sxs-lookup"><span data-stu-id="74c22-122">The results of the CAPE evaluation is then logically joined by **AND** with the results of the DACL on the resource and any other applicable CAPRs in effect on the resource.</span></span>

<span data-ttu-id="74c22-123">Exemple de CAPRs :</span><span class="sxs-lookup"><span data-stu-id="74c22-123">Example CAPRs:</span></span>

``` syntax
[HBI-POLICY]
APPLIES-TO="(@resource.confidentiality == HBI"
SD ="D:(A;;FA;;;AU;(@memberOf("Smartcard Logon")))"
StagingSD = "D:(A;;FA;;;AU;(@memberOf("Smartcard Logon") AND memberOfAny(Resource.ProjectGroups)))"
description="Control access to sensitive information"
 
[RETENTION-POLICY]
Applies-To="@resource.retention == true"
SD ="D:(A;;;FA;;BA)(A;;FR;;;WD)"
description="If the document is marked for retention, then it is read-only for everyone however Local Admins have 
full control to them to put them out of retention when the time comes"
 
[TEST-FINANCE-POLICY]
Applies-To="@resource.label == 'finance'"
SD="D:(A;;FA;;;AU;(member_of(FinanceGroup))"
description="Department: Only employees of the finance department should be able to read documents labeled as finance"
```

## <a name="deny-aces-in-capes"></a><span data-ttu-id="74c22-124">Refuser les ACE dans CAPEs</span><span class="sxs-lookup"><span data-stu-id="74c22-124">Deny ACEs in CAPEs</span></span>

<span data-ttu-id="74c22-125">Dans Windows 8, les ACE de refus ne sont pas prises en charge dans un CAPR.</span><span class="sxs-lookup"><span data-stu-id="74c22-125">In Windows 8 deny ACEs will not be supported in a CAPR.</span></span> <span data-ttu-id="74c22-126">L’expérience utilisateur de création de CAPR n’autorise pas la création d’une entrée du contrôle d’accès.</span><span class="sxs-lookup"><span data-stu-id="74c22-126">The CAPR authoring UX will not allow creation of a deny ACE.</span></span> <span data-ttu-id="74c22-127">En outre, lorsque l’autorité LSA récupère le CAP à partir de Active Directory, LSA vérifie qu’aucun CAPRs n’a de refus d’entrées de contrôle d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="74c22-127">Additionally, when the LSA retrieves the CAP from Active Directory, LSA will verify that no CAPRs have deny ACEs.</span></span> <span data-ttu-id="74c22-128">Si une entrée du contrôle d’accès est détectée dans un CAPR, la limite est traitée comme étant non valide et ne sera pas copiée dans le registre ou le SRM.</span><span class="sxs-lookup"><span data-stu-id="74c22-128">If a deny ACE is found in a CAPR then the CAP will be treated as invalid and not be copied to the registry or SRM.</span></span>

> [!Note]  
> <span data-ttu-id="74c22-129">La vérification de l’accès n’impose pas l’absence d’ACE de refus.</span><span class="sxs-lookup"><span data-stu-id="74c22-129">The access check will not enforce that no deny ACEs are present.</span></span> <span data-ttu-id="74c22-130">Les ACE de refus dans un CAPR seront appliqués.</span><span class="sxs-lookup"><span data-stu-id="74c22-130">Deny ACEs in a CAPR will be applied.</span></span> <span data-ttu-id="74c22-131">Il est prévu que les outils de création empêchent cela de se produire.</span><span class="sxs-lookup"><span data-stu-id="74c22-131">It is expected that authoring tools will prevent this from happening.</span></span>

 

## <a name="cape-definition"></a><span data-ttu-id="74c22-132">Définition du Cap</span><span class="sxs-lookup"><span data-stu-id="74c22-132">CAPE Definition</span></span>

<span data-ttu-id="74c22-133">Les CAPRs sont créés par le biais d’une nouvelle expérience utilisateur fournie dans Centre d’administration Active Directory (le centre.) Dans le centre, une nouvelle option de tâche est fournie pour créer un CAPR.</span><span class="sxs-lookup"><span data-stu-id="74c22-133">CAPRs are created though a new UX provided in Active Directory Administrative Center (ADAC.) In ADAC a new task option is provided to create a CAPR.</span></span> <span data-ttu-id="74c22-134">Lorsque cette tâche est sélectionnée, le centre invite l’utilisateur à fournir un nom de CAPR et une description à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="74c22-134">When this task is selected, ADAC will prompt the user with a dialog asking the user for a CAPR name and a description.</span></span> <span data-ttu-id="74c22-135">Lorsqu’ils sont fournis, les contrôles permettant de définir les autres éléments CAPR sont activés.</span><span class="sxs-lookup"><span data-stu-id="74c22-135">When these are provided, the controls to define any of the remaining CAPR elements become enabled.</span></span> <span data-ttu-id="74c22-136">Pour chacun des éléments restants de CAPR, l’expérience utilisateur appellera la liste de contrôle d’accès (ACL) pour permettre la définition de l’expression et/ou des ACL.</span><span class="sxs-lookup"><span data-stu-id="74c22-136">For each of the remaining CAPR elements, the UX will call out to the ACL-UI to allow definition of expression and/or ACLs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="74c22-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="74c22-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74c22-138">**AccessCheck**</span><span class="sxs-lookup"><span data-stu-id="74c22-138">**AccessCheck**</span></span>](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck)
</dt> <dt>

[<span data-ttu-id="74c22-139">Scénario de Access Control dynamique (DAC)</span><span class="sxs-lookup"><span data-stu-id="74c22-139">Dynamic Access Control (DAC) scenario</span></span>](/previous-versions/windows/desktop/dacx/dynamic-access-control-developer-extensibility-roadmap)
</dt> </dl>

 

 
