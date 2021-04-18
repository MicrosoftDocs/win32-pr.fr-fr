---
description: Windows Installer les packages de mise à niveau peuvent être créés pour que les mises à niveau majeures ne soient pas installées si une version plus récente est déjà installée sur un utilisateur.
ms.assetid: f46e82bd-70b3-46a2-8246-a1eadfdc589d
title: Empêcher l’installation d’un ancien package sur une version plus récente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 320ab062c4ffbc740d85c59ece3d3baaa63f4209
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519865"
---
# <a name="preventing-an-old-package-from-installing-over-a-newer-version"></a><span data-ttu-id="7a8ac-103">Empêcher l’installation d’un ancien package sur une version plus récente</span><span class="sxs-lookup"><span data-stu-id="7a8ac-103">Preventing an Old Package from Installing Over a Newer Version</span></span>

<span data-ttu-id="7a8ac-104">Windows Installer les packages de mise à niveau peuvent être créés pour que les mises à niveau majeures ne soient pas installées si une version plus récente est déjà installée sur un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7a8ac-104">Windows Installer upgrade packages can be authored to have major upgrades not install if a user already has a newer version installed.</span></span> <span data-ttu-id="7a8ac-105">La procédure décrite dans cette rubrique peut uniquement empêcher les rétrogradations qui peuvent être provoquées par l’exécution d’un package de mise à niveau majeur.</span><span class="sxs-lookup"><span data-stu-id="7a8ac-105">The procedure in this topic can only prevent downgrades that might be caused by running a major upgrade package.</span></span> <span data-ttu-id="7a8ac-106">Cette procédure s’appuie sur l' [action FindRelatedProducts](findrelatedproducts-action.md), qui s’exécute uniquement lors d’une première installation et qui ne s’exécute pas en mode maintenance (réinstallation).</span><span class="sxs-lookup"><span data-stu-id="7a8ac-106">This procedure relies on the [FindRelatedProducts Action](findrelatedproducts-action.md), which only runs during a first-time installation and does not run in maintenance mode (reinstallation).</span></span> <span data-ttu-id="7a8ac-107">Étant donné que les mises à niveau mineures sont effectuées à l’aide de la réinstallation, cette procédure ne peut pas être utilisée pour déterminer si un package de mise à niveau mineure tente de rétrograder une application.</span><span class="sxs-lookup"><span data-stu-id="7a8ac-107">Because minor upgrades are performed using reinstallation, this procedure cannot be used to determine whether a minor upgrade package is attempting to downgrade an application.</span></span> <span data-ttu-id="7a8ac-108">Pour plus d’informations, consultez [préparation d’une application pour les futures mises à niveau majeures](preparing-an-application-for-future-major-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="7a8ac-108">For more information, see [Preparing an Application for Future Major Upgrades](preparing-an-application-for-future-major-upgrades.md).</span></span>

<span data-ttu-id="7a8ac-109">**Pour empêcher l’installation d’un ancien package sur une version plus récente**</span><span class="sxs-lookup"><span data-stu-id="7a8ac-109">**To prevent an old package from installing over a newer version**</span></span>

1.  <span data-ttu-id="7a8ac-110">Entrez la propriété [**UpgradeCode**](upgradecode.md) du groupe de produits connexes pouvant être éligibles pour recevoir cette mise à niveau dans la colonne UpgradeCode de la [table de mise à niveau](upgrade-table.md).</span><span class="sxs-lookup"><span data-stu-id="7a8ac-110">Enter the [**UpgradeCode**](upgradecode.md) Property for the group of related products that may be eligible to receive this upgrade into the UpgradeCode column of the [Upgrade Table](upgrade-table.md).</span></span>
2.  <span data-ttu-id="7a8ac-111">Entrez l’indicateur de bit **msidbUpgradeAttributesOnlyDetect** dans la colonne attributs de la [table de mise à niveau](upgrade-table.md).</span><span class="sxs-lookup"><span data-stu-id="7a8ac-111">Enter the **msidbUpgradeAttributesOnlyDetect** bit flag in the Attributes column of the [Upgrade Table](upgrade-table.md).</span></span>
3.  <span data-ttu-id="7a8ac-112">Entrez la version de la mise à niveau fournie par ce package dans la colonne VersionMin de la [table de mise à niveau](upgrade-table.md).</span><span class="sxs-lookup"><span data-stu-id="7a8ac-112">Enter the version of the upgrade provided by this package into the VersionMin column of the [Upgrade Table](upgrade-table.md).</span></span> <span data-ttu-id="7a8ac-113">Laissez la colonne VersionMax vide.</span><span class="sxs-lookup"><span data-stu-id="7a8ac-113">Leave the VersionMax column blank.</span></span>
4.  <span data-ttu-id="7a8ac-114">Entrez le nom de la propriété qui doit être définie par l' [action FindRelatedProducts](findrelatedproducts-action.md) dans la colonne ActionProperty de la [table de mise à niveau](upgrade-table.md).</span><span class="sxs-lookup"><span data-stu-id="7a8ac-114">Enter the name of the property that is to be set by the [FindRelatedProducts Action](findrelatedproducts-action.md) into the ActionProperty column of the [Upgrade Table](upgrade-table.md).</span></span>
5.  <span data-ttu-id="7a8ac-115">Ajoutez la propriété [**SecureCustomProperties**](securecustomproperties.md) et la propriété nommée dans la colonne ActionProperty de la [table de mise à niveau](upgrade-table.md) à la [table de propriétés](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="7a8ac-115">Add the [**SecureCustomProperties**](securecustomproperties.md) property and the property named in the ActionProperty column of the [Upgrade Table](upgrade-table.md) to the [Property Table](property-table.md).</span></span>
6.  <span data-ttu-id="7a8ac-116">Ajoutez un [type d’action personnalisé 19](custom-action-type-19.md) après l’action FindRelatedProducts dans la [table InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="7a8ac-116">Add a [Custom Action Type 19](custom-action-type-19.md) after the FindRelatedProducts action in the [InstallExecuteSequence Table](installexecutesequence-table.md).</span></span> <span data-ttu-id="7a8ac-117">Incluez un enregistrement dans la [table CustomAction](customaction-table.md) pour cette action et entrez le texte à afficher dans la colonne cible.</span><span class="sxs-lookup"><span data-stu-id="7a8ac-117">Include a record in the [CustomAction Table](customaction-table.md) for this action and enter the text to be displayed in the Target column.</span></span> <span data-ttu-id="7a8ac-118">L’action personnalisée de type 19 étant intégrée au programme d’installation, il n’y a aucun code à écrire.</span><span class="sxs-lookup"><span data-stu-id="7a8ac-118">The type 19 custom action is built into the installer, so there is no code to write.</span></span>
7.  <span data-ttu-id="7a8ac-119">Entrez le nom du ActionProperty dans la colonne condition de l’enregistrement dans la [table InstallExecuteSequence](installexecutesequence-table.md) qui contient le [type d’action personnalisé 19](custom-action-type-19.md).</span><span class="sxs-lookup"><span data-stu-id="7a8ac-119">Enter the name of the ActionProperty into the Condition column of the record in [InstallExecuteSequence Table](installexecutesequence-table.md) that contains the [Custom Action Type 19](custom-action-type-19.md).</span></span> <span data-ttu-id="7a8ac-120">Cette condition permet d’exécuter l’action personnalisée uniquement lorsque la [table de mise à niveau](upgrade-table.md) détecte qu’une version plus récente est déjà installée.</span><span class="sxs-lookup"><span data-stu-id="7a8ac-120">This conditions the custom action to only be executed when the [Upgrade Table](upgrade-table.md) detects that a newer version is already installed.</span></span>

    <span data-ttu-id="7a8ac-121">Par exemple, un package Windows Installer qui met à niveau un groupe de produits associés vers la version 3,0 peut inclure les enregistrements suivants dans ses tables de [mise à niveau](upgrade-table.md), [CustomAction](customaction-table.md), [InstallExecuteSequence](installexecutesequence-table.md)et [propriété](property-table.md) .</span><span class="sxs-lookup"><span data-stu-id="7a8ac-121">For example, a Windows Installer package that upgrades a group of related products to version 3.0 may include the following records in its [Upgrade](upgrade-table.md), [CustomAction](customaction-table.md), [InstallExecuteSequence](installexecutesequence-table.md), and [Property](property-table.md) tables.</span></span> <span data-ttu-id="7a8ac-122">Tous les produits associés au groupe ont le même UpgradeCode, mais le programme d’installation n’installe pas ce package de mise à niveau si une version ultérieure à la version 3,0 est déjà installée sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="7a8ac-122">All the related products in the group have the same UpgradeCode, but the installer does not install this upgrade package if a version later than 3.0 is already installed on the computer.</span></span> <span data-ttu-id="7a8ac-123">Dans ce cas, le programme d’installation affiche un message d’erreur et l’installation échoue.</span><span class="sxs-lookup"><span data-stu-id="7a8ac-123">In this case, the Installer presents an error message and the installation fails.</span></span> <span data-ttu-id="7a8ac-124">Le package de mise à niveau de la version 3,0 s’installe sur les versions 1,0 et 2,0.</span><span class="sxs-lookup"><span data-stu-id="7a8ac-124">The version 3.0 upgrade package installs over versions 1.0 and 2.0.</span></span>

    [<span data-ttu-id="7a8ac-125">Mettre à niveau la table</span><span class="sxs-lookup"><span data-stu-id="7a8ac-125">Upgrade Table</span></span>](upgrade-table.md)

    

    | <span data-ttu-id="7a8ac-126">UpgradeCode</span><span class="sxs-lookup"><span data-stu-id="7a8ac-126">UpgradeCode</span></span>                            | <span data-ttu-id="7a8ac-127">VersionMin</span><span class="sxs-lookup"><span data-stu-id="7a8ac-127">VersionMin</span></span> | <span data-ttu-id="7a8ac-128">VersionMax</span><span class="sxs-lookup"><span data-stu-id="7a8ac-128">VersionMax</span></span> | <span data-ttu-id="7a8ac-129">Language</span><span class="sxs-lookup"><span data-stu-id="7a8ac-129">Language</span></span> | <span data-ttu-id="7a8ac-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="7a8ac-130">Attributes</span></span>                                | <span data-ttu-id="7a8ac-131">Supprimer</span><span class="sxs-lookup"><span data-stu-id="7a8ac-131">Remove</span></span> | <span data-ttu-id="7a8ac-132">ActionProperty</span><span class="sxs-lookup"><span data-stu-id="7a8ac-132">ActionProperty</span></span>  |
    |----------------------------------------|------------|------------|----------|-------------------------------------------|--------|-----------------|
    | <span data-ttu-id="7a8ac-133">{E7BE6D45-49FF-4701-A17E-BDCC98CE180D}</span><span class="sxs-lookup"><span data-stu-id="7a8ac-133">{E7BE6D45-49FF-4701-A17E-BDCC98CE180D}</span></span> | <span data-ttu-id="7a8ac-134">3.0</span><span class="sxs-lookup"><span data-stu-id="7a8ac-134">3.0</span></span>        |            |          | <span data-ttu-id="7a8ac-135">msidbUpgradeAttributesOnlyDetect</span><span class="sxs-lookup"><span data-stu-id="7a8ac-135">msidbUpgradeAttributesOnlyDetect</span></span>          |        | <span data-ttu-id="7a8ac-136">NEWPRODUCTFOUND</span><span class="sxs-lookup"><span data-stu-id="7a8ac-136">NEWPRODUCTFOUND</span></span> |
    | <span data-ttu-id="7a8ac-137">{E7BE6D45-49FF-4701-A17E-BDCC98CE180D}</span><span class="sxs-lookup"><span data-stu-id="7a8ac-137">{E7BE6D45-49FF-4701-A17E-BDCC98CE180D}</span></span> | <span data-ttu-id="7a8ac-138">1.0</span><span class="sxs-lookup"><span data-stu-id="7a8ac-138">1.0</span></span>        | <span data-ttu-id="7a8ac-139">3.0</span><span class="sxs-lookup"><span data-stu-id="7a8ac-139">3.0</span></span>        |          | <span data-ttu-id="7a8ac-140">msidbUpgradeAttributesVersionMinInclusive</span><span class="sxs-lookup"><span data-stu-id="7a8ac-140">msidbUpgradeAttributesVersionMinInclusive</span></span> |        | <span data-ttu-id="7a8ac-141">UPGRADEFOUND</span><span class="sxs-lookup"><span data-stu-id="7a8ac-141">UPGRADEFOUND</span></span>    |

    

     

    [<span data-ttu-id="7a8ac-142">Table CustomAction</span><span class="sxs-lookup"><span data-stu-id="7a8ac-142">CustomAction Table</span></span>](customaction-table.md)

    

    | <span data-ttu-id="7a8ac-143">Action</span><span class="sxs-lookup"><span data-stu-id="7a8ac-143">Action</span></span> | <span data-ttu-id="7a8ac-144">Type</span><span class="sxs-lookup"><span data-stu-id="7a8ac-144">Type</span></span> | <span data-ttu-id="7a8ac-145">Source</span><span class="sxs-lookup"><span data-stu-id="7a8ac-145">Source</span></span> | <span data-ttu-id="7a8ac-146">Cible</span><span class="sxs-lookup"><span data-stu-id="7a8ac-146">Target</span></span>                                 |
    |--------|------|--------|----------------------------------------|
    | <span data-ttu-id="7a8ac-147">AC1</span><span class="sxs-lookup"><span data-stu-id="7a8ac-147">CA1</span></span>    | <span data-ttu-id="7a8ac-148">19</span><span class="sxs-lookup"><span data-stu-id="7a8ac-148">19</span></span>   |        | <span data-ttu-id="7a8ac-149">Une mise à niveau plus élevée est déjà installée.</span><span class="sxs-lookup"><span data-stu-id="7a8ac-149">A higher upgrade is already installed.</span></span> |

    

     

    [<span data-ttu-id="7a8ac-150">Table InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="7a8ac-150">InstallExecuteSequence Table</span></span>](installexecutesequence-table.md)

    

    | <span data-ttu-id="7a8ac-151">Action</span><span class="sxs-lookup"><span data-stu-id="7a8ac-151">Action</span></span>              | <span data-ttu-id="7a8ac-152">Condition</span><span class="sxs-lookup"><span data-stu-id="7a8ac-152">Condition</span></span>       | <span data-ttu-id="7a8ac-153">Séquence</span><span class="sxs-lookup"><span data-stu-id="7a8ac-153">Sequence</span></span> |
    |---------------------|-----------------|----------|
    | <span data-ttu-id="7a8ac-154">FindRelatedProducts</span><span class="sxs-lookup"><span data-stu-id="7a8ac-154">FindRelatedProducts</span></span> |                 | <span data-ttu-id="7a8ac-155">200</span><span class="sxs-lookup"><span data-stu-id="7a8ac-155">200</span></span>      |
    | <span data-ttu-id="7a8ac-156">AC1</span><span class="sxs-lookup"><span data-stu-id="7a8ac-156">CA1</span></span>                 | <span data-ttu-id="7a8ac-157">NEWPRODUCTFOUND</span><span class="sxs-lookup"><span data-stu-id="7a8ac-157">NEWPRODUCTFOUND</span></span> | <span data-ttu-id="7a8ac-158">201</span><span class="sxs-lookup"><span data-stu-id="7a8ac-158">201</span></span>      |

    

     

    [<span data-ttu-id="7a8ac-159">Table de propriétés</span><span class="sxs-lookup"><span data-stu-id="7a8ac-159">Property Table</span></span>](property-table.md)

    

    | <span data-ttu-id="7a8ac-160">Propriété</span><span class="sxs-lookup"><span data-stu-id="7a8ac-160">Property</span></span>                                                 | <span data-ttu-id="7a8ac-161">Valeur</span><span class="sxs-lookup"><span data-stu-id="7a8ac-161">Value</span></span>                        |
    |----------------------------------------------------------|------------------------------|
    | [<span data-ttu-id="7a8ac-162">**SecureCustomProperties**</span><span class="sxs-lookup"><span data-stu-id="7a8ac-162">**SecureCustomProperties**</span></span>](securecustomproperties.md) | <span data-ttu-id="7a8ac-163">NEWPRODUCTFOUND; UPGRADEFOUND</span><span class="sxs-lookup"><span data-stu-id="7a8ac-163">NEWPRODUCTFOUND;UPGRADEFOUND</span></span> |

    

     

 

 



