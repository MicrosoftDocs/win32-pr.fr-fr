---
title: Mappage de l’interface utilisateur de l’objet ordinateur
description: Les tableaux suivants répertorient les éléments des feuilles de propriétés de l’objet ordinateur dans le composant logiciel enfichable utilisateurs et ordinateurs Active Directory.
ms.assetid: e2a7a42d-e854-43fc-a36b-f3031c1685a7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de2a2b3ed4ec8cbf3c1af59e024fc5e04bc68ae8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724613"
---
# <a name="computer-object-user-interface-mapping"></a><span data-ttu-id="c6690-103">Mappage de l’interface utilisateur de l’objet ordinateur</span><span class="sxs-lookup"><span data-stu-id="c6690-103">Computer Object User Interface Mapping</span></span>

<span data-ttu-id="c6690-104">Les tableaux suivants répertorient les éléments des feuilles de propriétés de l’objet ordinateur dans le composant logiciel enfichable utilisateurs et ordinateurs Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c6690-104">The following tables list elements of the Computer object property sheets in the Active Directory Users and Computers snap-in.</span></span>

## <a name="general-property-sheet"></a><span data-ttu-id="c6690-105">Feuille de propriétés général</span><span class="sxs-lookup"><span data-stu-id="c6690-105">General Property Sheet</span></span>

<span data-ttu-id="c6690-106">Le tableau suivant répertorie les étiquettes de l’interface utilisateur de la feuille de propriétés **générales** .</span><span class="sxs-lookup"><span data-stu-id="c6690-106">The following table lists the UI labels of the **General** property sheet.</span></span>



| <span data-ttu-id="c6690-107">Étiquette d’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="c6690-107">UI label</span></span>                         | <span data-ttu-id="c6690-108">Attribut Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="c6690-108">Active Directory Domain Services attribute</span></span> | <span data-ttu-id="c6690-109">Commentaires</span><span class="sxs-lookup"><span data-stu-id="c6690-109">Comments</span></span>                                         |
|----------------------------------|--------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="c6690-110">Nom de l’ordinateur (antérieur à Windows 2000)</span><span class="sxs-lookup"><span data-stu-id="c6690-110">Computer Name (pre-Windows 2000)</span></span> | <span data-ttu-id="c6690-111">sAMAccountName</span><span class="sxs-lookup"><span data-stu-id="c6690-111">sAMAccountName</span></span>                             |                                                  |
| <span data-ttu-id="c6690-112">Nom DNS</span><span class="sxs-lookup"><span data-stu-id="c6690-112">DNS Name</span></span>                         | <span data-ttu-id="c6690-113">dNSHostName</span><span class="sxs-lookup"><span data-stu-id="c6690-113">dNSHostName</span></span>                                |                                                  |
| <span data-ttu-id="c6690-114">Role</span><span class="sxs-lookup"><span data-stu-id="c6690-114">Role</span></span>                             | <span data-ttu-id="c6690-115">userAccountControl</span><span class="sxs-lookup"><span data-stu-id="c6690-115">userAccountControl</span></span>                         | <span data-ttu-id="c6690-116">Bascule un bit dans le masque de bits userAccountControl.</span><span class="sxs-lookup"><span data-stu-id="c6690-116">Toggles a bit in the userAccountControl bitmask.</span></span> |
| <span data-ttu-id="c6690-117">Description</span><span class="sxs-lookup"><span data-stu-id="c6690-117">Description</span></span>                      | <span data-ttu-id="c6690-118">description</span><span class="sxs-lookup"><span data-stu-id="c6690-118">description</span></span>                                |                                                  |
| <span data-ttu-id="c6690-119">Approuver l’ordinateur pour la délégation</span><span class="sxs-lookup"><span data-stu-id="c6690-119">Trust Computer for delegation</span></span>    | <span data-ttu-id="c6690-120">userAccountControl</span><span class="sxs-lookup"><span data-stu-id="c6690-120">userAccountControl</span></span>                         | <span data-ttu-id="c6690-121">Bascule un bit dans le masque de bits userAccountControl.</span><span class="sxs-lookup"><span data-stu-id="c6690-121">Toggles a bit in the userAccountControl bitmask.</span></span> |



 

## <a name="location-property-sheet"></a><span data-ttu-id="c6690-122">Feuille de propriétés de l’emplacement</span><span class="sxs-lookup"><span data-stu-id="c6690-122">Location Property Sheet</span></span>

<span data-ttu-id="c6690-123">Le tableau suivant répertorie les étiquettes de l’interface utilisateur de la feuille de propriétés d' **emplacement** .</span><span class="sxs-lookup"><span data-stu-id="c6690-123">The following table lists the UI labels of the **Location** property sheet.</span></span>



| <span data-ttu-id="c6690-124">Étiquette d’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="c6690-124">UI label</span></span> | <span data-ttu-id="c6690-125">Attribut Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="c6690-125">Active Directory Domain Services attribute</span></span> |
|----------|--------------------------------------------|
| <span data-ttu-id="c6690-126">Emplacement</span><span class="sxs-lookup"><span data-stu-id="c6690-126">Location</span></span> | <span data-ttu-id="c6690-127">location</span><span class="sxs-lookup"><span data-stu-id="c6690-127">location</span></span>                                   |



 

## <a name="member-of-property-sheet"></a><span data-ttu-id="c6690-128">Membre de la feuille de propriétés</span><span class="sxs-lookup"><span data-stu-id="c6690-128">Member Of Property Sheet</span></span>

<span data-ttu-id="c6690-129">Le tableau suivant répertorie les étiquettes de l’interface utilisateur du **membre de** la feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="c6690-129">The following table lists the UI labels of the **Member Of** property sheet.</span></span>



| <span data-ttu-id="c6690-130">Étiquette d’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="c6690-130">UI label</span></span>          | <span data-ttu-id="c6690-131">Attribut Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="c6690-131">Active Directory Domain Services attribute</span></span> | <span data-ttu-id="c6690-132">Commentaires</span><span class="sxs-lookup"><span data-stu-id="c6690-132">Comments</span></span>                                                                                                                                                                   |
|-------------------|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6690-133">Membre de</span><span class="sxs-lookup"><span data-stu-id="c6690-133">Member of</span></span>         | <span data-ttu-id="c6690-134">memberOf</span><span class="sxs-lookup"><span data-stu-id="c6690-134">memberOf</span></span>                                   | <span data-ttu-id="c6690-135">Comprend tous les groupes de la liste des interfaces utilisateur, à l’exception du groupe principal, qui est représenté dans la publicité via l’attribut [**primaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid) .</span><span class="sxs-lookup"><span data-stu-id="c6690-135">Includes all of the groups in the UI list, except the primary group, which is represented in the AD through the [**primaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid) attribute.</span></span> |
| <span data-ttu-id="c6690-136">Définir le groupe principal</span><span class="sxs-lookup"><span data-stu-id="c6690-136">Set Primary Group</span></span> | <span data-ttu-id="c6690-137">primaryGroupID</span><span class="sxs-lookup"><span data-stu-id="c6690-137">primaryGroupID</span></span>                             | <span data-ttu-id="c6690-138">LDAP : lié à [**primaryGroupToken**](/windows/desktop/ADSchema/a-primarygrouptoken) du groupe principal.</span><span class="sxs-lookup"><span data-stu-id="c6690-138">LDAP: Tied to [**primaryGroupToken**](/windows/desktop/ADSchema/a-primarygrouptoken) of the primary group.</span></span>                                                                                  |



 

## <a name="operating-system-property-sheet"></a><span data-ttu-id="c6690-139">Feuille de propriétés du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="c6690-139">Operating System Property Sheet</span></span>

<span data-ttu-id="c6690-140">Le tableau suivant répertorie les étiquettes de l’interface utilisateur de la feuille de propriétés du **système d’exploitation** .</span><span class="sxs-lookup"><span data-stu-id="c6690-140">The following table lists the UI labels of the **Operating System** property sheet.</span></span>



| <span data-ttu-id="c6690-141">Étiquette d’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="c6690-141">UI label</span></span>     | <span data-ttu-id="c6690-142">Attribut Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="c6690-142">Active Directory Domain Services attribute</span></span> |
|--------------|--------------------------------------------|
| <span data-ttu-id="c6690-143">Nom</span><span class="sxs-lookup"><span data-stu-id="c6690-143">Name</span></span>         | <span data-ttu-id="c6690-144">operatingSystem</span><span class="sxs-lookup"><span data-stu-id="c6690-144">operatingSystem</span></span>                            |
| <span data-ttu-id="c6690-145">Version</span><span class="sxs-lookup"><span data-stu-id="c6690-145">Version</span></span>      | <span data-ttu-id="c6690-146">operatingSystemVersion</span><span class="sxs-lookup"><span data-stu-id="c6690-146">operatingSystemVersion</span></span>                     |
| <span data-ttu-id="c6690-147">Service Pack</span><span class="sxs-lookup"><span data-stu-id="c6690-147">Service Pack</span></span> | <span data-ttu-id="c6690-148">operatingSystemServicePack</span><span class="sxs-lookup"><span data-stu-id="c6690-148">operatingSystemServicePack</span></span>                 |



 

 

 