---
title: Mappage de l’interface utilisateur de l’objet de groupe
description: Cette rubrique décrit les feuilles de propriétés d’objet de groupe dans le composant logiciel enfichable utilisateurs et ordinateurs Active Directory. Propriété générale SheetMember de la propriété SheetMembers de la propriété SheetManaged par la feuille de propriétés
ms.assetid: c0cd73f0-f09f-4645-966d-6149888ce482
ms.tgt_platform: multiple
keywords:
- Objet de groupe mappage de l’interface utilisateur Active Directory
- Mappage de l’interface utilisateur, objet groupe AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe2277c24f621f8e32f46b9e9571d0d0d4de9cfc
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104031001"
---
# <a name="group-object-user-interface-mapping"></a><span data-ttu-id="c8871-105">Mappage de l’interface utilisateur de l’objet de groupe</span><span class="sxs-lookup"><span data-stu-id="c8871-105">Group Object User Interface Mapping</span></span>

<span data-ttu-id="c8871-106">Cette rubrique décrit les feuilles de propriétés d’objet de groupe dans le composant logiciel enfichable utilisateurs et ordinateurs Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c8871-106">This topic describes the Group object property sheets in the Active Directory Users and Computers snap-in.</span></span>

-   [<span data-ttu-id="c8871-107">Feuille de propriétés général</span><span class="sxs-lookup"><span data-stu-id="c8871-107">General Property Sheet</span></span>](#general-property-sheet)
-   [<span data-ttu-id="c8871-108">Membre de la feuille de propriétés</span><span class="sxs-lookup"><span data-stu-id="c8871-108">Member Of Property Sheet</span></span>](#member-of-property-sheet)
-   [<span data-ttu-id="c8871-109">Feuille de propriétés des membres</span><span class="sxs-lookup"><span data-stu-id="c8871-109">Members Property Sheet</span></span>](#members-property-sheet)
-   [<span data-ttu-id="c8871-110">Gestion par feuille de propriétés</span><span class="sxs-lookup"><span data-stu-id="c8871-110">Managed By Property Sheet</span></span>](#managed-by-property-sheet)

## <a name="general-property-sheet"></a><span data-ttu-id="c8871-111">Feuille de propriétés général</span><span class="sxs-lookup"><span data-stu-id="c8871-111">General Property Sheet</span></span>

<span data-ttu-id="c8871-112">Le tableau suivant présente les étiquettes de l’interface utilisateur de la feuille de propriétés **générales** .</span><span class="sxs-lookup"><span data-stu-id="c8871-112">The following table shows the UI labels of the **General** property sheet.</span></span>



| <span data-ttu-id="c8871-113">Étiquette d’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="c8871-113">UI label</span></span>                      | <span data-ttu-id="c8871-114">Attribut dans Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="c8871-114">Attribute in Active Directory Domain Services</span></span>     |
|-------------------------------|---------------------------------------------------|
| <span data-ttu-id="c8871-115">Nom du groupe (antérieur à Windows 2000)</span><span class="sxs-lookup"><span data-stu-id="c8871-115">Group Name (pre-Windows 2000)</span></span> | [<span data-ttu-id="c8871-116">**Nom de compte SAM**</span><span class="sxs-lookup"><span data-stu-id="c8871-116">**SAM-Account-Name**</span></span>](/windows/desktop/ADSchema/a-samaccountname) |
| <span data-ttu-id="c8871-117">Description</span><span class="sxs-lookup"><span data-stu-id="c8871-117">Description</span></span>                   | [<span data-ttu-id="c8871-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="c8871-118">**Description**</span></span>](/windows/desktop/ADSchema/a-description)         |
| <span data-ttu-id="c8871-119">Courrier électronique</span><span class="sxs-lookup"><span data-stu-id="c8871-119">E-Mail</span></span>                        | [<span data-ttu-id="c8871-120">**Adresses de messagerie**</span><span class="sxs-lookup"><span data-stu-id="c8871-120">**E-mail-Addresses**</span></span>](/windows/desktop/ADSchema/a-mail)           |
| <span data-ttu-id="c8871-121">Étendue du groupe</span><span class="sxs-lookup"><span data-stu-id="c8871-121">Group Scope</span></span>                   | [<span data-ttu-id="c8871-122">**Type de groupe**</span><span class="sxs-lookup"><span data-stu-id="c8871-122">**Group-Type**</span></span>](/windows/desktop/ADSchema/a-grouptype)            |
| <span data-ttu-id="c8871-123">Type de groupe</span><span class="sxs-lookup"><span data-stu-id="c8871-123">Group Type</span></span>                    | [<span data-ttu-id="c8871-124">**Type de groupe**</span><span class="sxs-lookup"><span data-stu-id="c8871-124">**Group-Type**</span></span>](/windows/desktop/ADSchema/a-grouptype)            |
| <span data-ttu-id="c8871-125">Notes</span><span class="sxs-lookup"><span data-stu-id="c8871-125">Notes</span></span>                         | [<span data-ttu-id="c8871-126">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="c8871-126">**Comment**</span></span>](/windows/desktop/ADSchema/a-info)                    |



 

## <a name="member-of-property-sheet"></a><span data-ttu-id="c8871-127">Membre de la feuille de propriétés</span><span class="sxs-lookup"><span data-stu-id="c8871-127">Member Of Property Sheet</span></span>

<span data-ttu-id="c8871-128">Le tableau suivant présente les étiquettes de l’interface utilisateur du **membre de** la feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="c8871-128">The following table shows the UI labels of the **Member Of** property sheet.</span></span>



| <span data-ttu-id="c8871-129">Étiquette d’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="c8871-129">UI label</span></span>  | <span data-ttu-id="c8871-130">Attribut dans Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="c8871-130">Attribute in Active Directory Domain Services</span></span> | <span data-ttu-id="c8871-131">Description</span><span class="sxs-lookup"><span data-stu-id="c8871-131">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-----------|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8871-132">Membre de</span><span class="sxs-lookup"><span data-stu-id="c8871-132">Member of</span></span> | [<span data-ttu-id="c8871-133">**Is-Member-of-DL**</span><span class="sxs-lookup"><span data-stu-id="c8871-133">**Is-Member-Of-DL**</span></span>](/windows/desktop/ADSchema/a-memberof)    | <span data-ttu-id="c8871-134">Contient les noms uniques des groupes auxquels appartient ce groupe.</span><span class="sxs-lookup"><span data-stu-id="c8871-134">Contains the distinguished names of the groups to which this group belongs.</span></span> <span data-ttu-id="c8871-135">L’attribut de membre de chacun des groupes de cette liste contient le nom unique de cet objet de groupe. L’interface utilisateur ne modifie pas directement l’attribut [**is-Member-of-DL**](/windows/desktop/ADSchema/a-memberof) .</span><span class="sxs-lookup"><span data-stu-id="c8871-135">The member attribute of each of the groups in this list contains the distinguished name of this group object.The user interface does not directly modify the [**Is-Member-Of-DL**](/windows/desktop/ADSchema/a-memberof) attribute.</span></span> <span data-ttu-id="c8871-136">Elle modifie l’attribut de [**membre**](/windows/desktop/ADSchema/a-member) sur l’objet de groupe dont cet objet est membre.</span><span class="sxs-lookup"><span data-stu-id="c8871-136">It modifies the [**Member**](/windows/desktop/ADSchema/a-member) attribute on the group object of which this object is made a member of.</span></span> <span data-ttu-id="c8871-137">Le serveur Active Directory gère l’attribut **is-Member-of-DL** .</span><span class="sxs-lookup"><span data-stu-id="c8871-137">The Active Directory server maintains the **Is-Member-Of-DL** attribute.</span></span><br/> |



 

## <a name="members-property-sheet"></a><span data-ttu-id="c8871-138">Feuille de propriétés des membres</span><span class="sxs-lookup"><span data-stu-id="c8871-138">Members Property Sheet</span></span>

<span data-ttu-id="c8871-139">Le tableau suivant présente les étiquettes de l’interface utilisateur de la feuille de propriétés des **membres** .</span><span class="sxs-lookup"><span data-stu-id="c8871-139">The following table shows the UI labels of the **Members** property sheet.</span></span>



| <span data-ttu-id="c8871-140">Étiquette d’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="c8871-140">UI label</span></span> | <span data-ttu-id="c8871-141">Attribut dans Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="c8871-141">Attribute in Active Directory Domain Services</span></span> | <span data-ttu-id="c8871-142">Description</span><span class="sxs-lookup"><span data-stu-id="c8871-142">Description</span></span>                                                           |
|----------|-----------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="c8871-143">Membres</span><span class="sxs-lookup"><span data-stu-id="c8871-143">Members</span></span>  | [<span data-ttu-id="c8871-144">**Membre**</span><span class="sxs-lookup"><span data-stu-id="c8871-144">**Member**</span></span>](/windows/desktop/ADSchema/a-member)               | <span data-ttu-id="c8871-145">Contient les noms uniques des membres de cet objet de groupe.</span><span class="sxs-lookup"><span data-stu-id="c8871-145">Contains the distinguished names of the members of this group object.</span></span> |



 

## <a name="managed-by-property-sheet"></a><span data-ttu-id="c8871-146">Gestion par feuille de propriétés</span><span class="sxs-lookup"><span data-stu-id="c8871-146">Managed By Property Sheet</span></span>

<span data-ttu-id="c8871-147">Le tableau suivant présente les étiquettes de l’interface utilisateur de la feuille de propriétés **géré par** .</span><span class="sxs-lookup"><span data-stu-id="c8871-147">The following table shows the UI labels of the **Managed By** property sheet.</span></span>



| <span data-ttu-id="c8871-148">Étiquette d’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="c8871-148">UI label</span></span>                           | <span data-ttu-id="c8871-149">Attribut dans Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="c8871-149">Attribute in Active Directory Domain Services</span></span>                                                                                   |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8871-150">Nom</span><span class="sxs-lookup"><span data-stu-id="c8871-150">Name</span></span>                               | [<span data-ttu-id="c8871-151">**Géré par**</span><span class="sxs-lookup"><span data-stu-id="c8871-151">**Managed-By**</span></span>](/windows/desktop/ADSchema/a-managedby)                                                                                          |
| <span data-ttu-id="c8871-152">Le gestionnaire peut mettre à jour la liste des membres</span><span class="sxs-lookup"><span data-stu-id="c8871-152">Manager can update membership list</span></span> | <span data-ttu-id="c8871-153">Aucun</span><span class="sxs-lookup"><span data-stu-id="c8871-153">None.</span></span> <span data-ttu-id="c8871-154">Une entrée du contrôle d’accès avec l’autorisation « autoriser-écrire des membres » est ajoutée au compte identifié par **nom**.</span><span class="sxs-lookup"><span data-stu-id="c8871-154">An ACE with the "Allow - Write Members" permission is added to the account identified by **Name**.</span></span>                        |
| <span data-ttu-id="c8871-155">Office</span><span class="sxs-lookup"><span data-stu-id="c8871-155">Office</span></span>                             | <span data-ttu-id="c8871-156">Attribut [**Physical-Delivery-Office-Name**](/windows/desktop/ADSchema/a-physicaldeliveryofficename) du compte identifié par **Name**.</span><span class="sxs-lookup"><span data-stu-id="c8871-156">The [**Physical-Delivery-Office-Name**](/windows/desktop/ADSchema/a-physicaldeliveryofficename) attribute of the account identified by **Name**.</span></span> |
| <span data-ttu-id="c8871-157">Rue</span><span class="sxs-lookup"><span data-stu-id="c8871-157">Street</span></span>                             | <span data-ttu-id="c8871-158">L’attribut [**rue-adresse**](/windows/desktop/ADSchema/a-street) du compte identifié par le **nom**.</span><span class="sxs-lookup"><span data-stu-id="c8871-158">The [**Street-Address**](/windows/desktop/ADSchema/a-street) attribute of the account identified by **Name**.</span></span>                                    |
| <span data-ttu-id="c8871-159">City</span><span class="sxs-lookup"><span data-stu-id="c8871-159">City</span></span>                               | <span data-ttu-id="c8871-160">Attribut de [**nom de localité**](/windows/desktop/ADSchema/a-l) du compte identifié par le **nom**.</span><span class="sxs-lookup"><span data-stu-id="c8871-160">The [**Locality-Name**](/windows/desktop/ADSchema/a-l) attribute of the account identified by **Name**.</span></span>                                          |
| <span data-ttu-id="c8871-161">État/Province</span><span class="sxs-lookup"><span data-stu-id="c8871-161">State/province</span></span>                     | <span data-ttu-id="c8871-162">Attribut [**State-or-province-Name**](/windows/desktop/ADSchema/a-st) du compte identifié par **nom**.</span><span class="sxs-lookup"><span data-stu-id="c8871-162">The [**State-Or-Province-Name**](/windows/desktop/ADSchema/a-st) attribute of the account identified by **Name**.</span></span>                                |
| <span data-ttu-id="c8871-163">Pays/région</span><span class="sxs-lookup"><span data-stu-id="c8871-163">Country/region</span></span>                     | <span data-ttu-id="c8871-164">Attribut [**Country-Name**](/windows/desktop/ADSchema/a-c) du compte identifié par **Name**.</span><span class="sxs-lookup"><span data-stu-id="c8871-164">The [**Country-Name**](/windows/desktop/ADSchema/a-c) attribute of the account identified by **Name**.</span></span>                                           |
| <span data-ttu-id="c8871-165">Numéro de téléphone</span><span class="sxs-lookup"><span data-stu-id="c8871-165">Telephone number</span></span>                   | <span data-ttu-id="c8871-166">Attribut de [**numéro de téléphone**](/windows/desktop/ADSchema/a-telephonenumber) du compte identifié par le **nom**.</span><span class="sxs-lookup"><span data-stu-id="c8871-166">The [**Telephone-Number**](/windows/desktop/ADSchema/a-telephonenumber) attribute of the account identified by **Name**.</span></span>                         |
| <span data-ttu-id="c8871-167">Numéro de télécopie</span><span class="sxs-lookup"><span data-stu-id="c8871-167">Fax number</span></span>                         | <span data-ttu-id="c8871-168">Attribut [**télécopie-numéro de téléphone**](/windows/desktop/ADSchema/a-facsimiletelephonenumber) du compte identifié par le **nom**.</span><span class="sxs-lookup"><span data-stu-id="c8871-168">The [**Facsimile-Telephone-Number**](/windows/desktop/ADSchema/a-facsimiletelephonenumber) attribute of the account identified by **Name**.</span></span>      |



 

 

