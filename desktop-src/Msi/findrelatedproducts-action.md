---
description: L’action FindRelatedProducts s’exécute dans l’ordre de chaque enregistrement de la table de mise à niveau et compare le code de mise à niveau, la version du produit et la langue de chaque ligne aux produits installés sur le système.
ms.assetid: 7efcb767-9bdf-43a4-83b8-61b6fc84adf6
title: Action FindRelatedProducts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a87973631e51315df17a156bc8c57aa9facd84f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319842"
---
# <a name="findrelatedproducts-action"></a><span data-ttu-id="67643-103">Action FindRelatedProducts</span><span class="sxs-lookup"><span data-stu-id="67643-103">FindRelatedProducts Action</span></span>

<span data-ttu-id="67643-104">L’action FindRelatedProducts s’exécute dans l’ordre de chaque enregistrement de la [table de mise à niveau](upgrade-table.md) et compare le code de mise à niveau, la version du produit et la langue de chaque ligne aux produits installés sur le système.</span><span class="sxs-lookup"><span data-stu-id="67643-104">The FindRelatedProducts action runs through each record of the [Upgrade table](upgrade-table.md) in sequence and compares the upgrade code, product version, and language in each row to products installed on the system.</span></span> <span data-ttu-id="67643-105">Quand FindRelatedProducts détecte une correspondance entre les informations de mise à niveau et un produit installé, il ajoute le code de produit à la propriété spécifiée dans la colonne ActionProperty de UpgradeTable.</span><span class="sxs-lookup"><span data-stu-id="67643-105">When FindRelatedProducts detects a correspondence between the upgrade information and an installed product, it appends the product code to the property specified in the ActionProperty column of the UpgradeTable.</span></span>

<span data-ttu-id="67643-106">L’action FindRelatedProducts s’exécute uniquement lors de la première installation du produit.</span><span class="sxs-lookup"><span data-stu-id="67643-106">The FindRelatedProducts action only runs the first time the product is installed.</span></span> <span data-ttu-id="67643-107">L’action FindRelatedProducts ne s’exécute pas en mode maintenance ni en cours de désinstallation.</span><span class="sxs-lookup"><span data-stu-id="67643-107">The FindRelatedProducts action does not run during maintenance mode or uninstallation.</span></span>

## <a name="database-tables-queried"></a><span data-ttu-id="67643-108">Tables de base de données interrogées</span><span class="sxs-lookup"><span data-stu-id="67643-108">Database Tables Queried</span></span>

<span data-ttu-id="67643-109">Cette action interroge le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="67643-109">This action queries the following table:</span></span>

[<span data-ttu-id="67643-110">Mettre à niveau la table</span><span class="sxs-lookup"><span data-stu-id="67643-110">Upgrade Table</span></span>](upgrade-table.md)

## <a name="properties-used"></a><span data-ttu-id="67643-111">Propriétés utilisées</span><span class="sxs-lookup"><span data-stu-id="67643-111">Properties Used</span></span>

<span data-ttu-id="67643-112">L’action FindRelatedProducts utilise la propriété [**UpgradeCode**](upgradecode.md) et les informations sur la version et la langue que vous avez créées dans la table de mise à niveau pour détecter les produits installés affectés par la mise à niveau en attente.</span><span class="sxs-lookup"><span data-stu-id="67643-112">The FindRelatedProducts action uses the [**UpgradeCode**](upgradecode.md) property and the version and language information authored into the Upgrade table to detect installed products affected by the pending upgrade.</span></span> <span data-ttu-id="67643-113">Il ajoute le code de produit des produits détectés à la propriété dans la colonne ActionProperty de UpgradeTable.</span><span class="sxs-lookup"><span data-stu-id="67643-113">It appends the product code of detected products to the property in the ActionProperty column of the UpgradeTable.</span></span>

<span data-ttu-id="67643-114">FindRelatedProducts reconnaît uniquement les produits existants qui ont été installés à l’aide de l’Windows Installer avec un fichier. msi qui définit une propriété [**UpgradeCode**](upgradecode.md) , une propriété [**ProductVersion**](productversion.md) et une valeur pour la propriété [**ProductLanguage**](productlanguage.md) qui est l’une des langues listées dans la propriété [**Résumé du modèle**](template-summary.md) .</span><span class="sxs-lookup"><span data-stu-id="67643-114">FindRelatedProducts only recognizes existing products that have been installed using the Windows Installer with an .msi that defines an [**UpgradeCode**](upgradecode.md) property, a [**ProductVersion**](productversion.md) property, and a value for the [**ProductLanguage**](productlanguage.md) property that is one of the languages listed in the [**Template Summary**](template-summary.md) Property.</span></span>

<span data-ttu-id="67643-115">Notez que FindRelatedProducts utilise la langue retournée par [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa).</span><span class="sxs-lookup"><span data-stu-id="67643-115">Note that FindRelatedProducts uses the language returned by [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa).</span></span> <span data-ttu-id="67643-116">Pour que FindRelatedProducts fonctionne correctement, l’auteur du package doit être certain que la propriété [**ProductLanguage**](productlanguage.md) de la [table de propriétés](property-table.md) est définie sur une langue qui est également indiquée dans la propriété Résumé du [**modèle**](template-summary.md) .</span><span class="sxs-lookup"><span data-stu-id="67643-116">For FindRelatedProducts to work correctly, the package author must be sure that the [**ProductLanguage**](productlanguage.md) property in the [Property table](property-table.md) is set to a language that is also listed in the [**Template Summary**](template-summary.md) Property.</span></span> <span data-ttu-id="67643-117">Consultez [préparation d’une application pour les futures mises à niveau majeures](preparing-an-application-for-future-major-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="67643-117">See [Preparing an Application for Future Major Upgrades](preparing-an-application-for-future-major-upgrades.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="67643-118">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="67643-118">Sequence Restrictions</span></span>

<span data-ttu-id="67643-119">FindRelatedProducts doit être créé dans la [table InstallUISequence](installuisequence-table.md) et les tables [InstallExecuteSequence](installexecutesequence-table.md) .</span><span class="sxs-lookup"><span data-stu-id="67643-119">FindRelatedProducts should be authored into the [InstallUISequence table](installuisequence-table.md) and [InstallExecuteSequence](installexecutesequence-table.md) tables.</span></span> <span data-ttu-id="67643-120">Le programme d’installation empêche les produits FindRelated de s’exécuter dans InstallExecuteSequence si l’action a déjà été exécutée dans InstallUISequence.</span><span class="sxs-lookup"><span data-stu-id="67643-120">The installer prevents FindRelated Products from running in InstallExecuteSequence if the action has already run in InstallUISequence.</span></span> <span data-ttu-id="67643-121">L’action FindRelatedProducts doit précéder l’action [MigrateFeatureStates](migratefeaturestates-action.md) et l’action [RemoveExistingProducts](removeexistingproducts-action.md).</span><span class="sxs-lookup"><span data-stu-id="67643-121">The FindRelatedProducts action must come before the [MigrateFeatureStates action](migratefeaturestates-action.md) and the [RemoveExistingProducts action](removeexistingproducts-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="67643-122">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="67643-122">ActionData Messages</span></span>

<span data-ttu-id="67643-123">FindRelatedProducts envoie un message de données d’action pour chaque produit associé détecté sur le système.</span><span class="sxs-lookup"><span data-stu-id="67643-123">FindRelatedProducts sends an action data message for each related product it detects on the system.</span></span>

 

 



