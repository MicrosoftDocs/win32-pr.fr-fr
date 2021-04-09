---
description: Pour appliquer une mise à niveau majeure à l’aide de Windows Installer, le package d’installation du produit d’origine doit spécifier une propriété UpgradeCode, décrite dans préparation d’une application pour les futures mises à niveau majeures, et le package de mise à niveau doit avoir une table de mise à niveau.
ms.assetid: 041f5bab-cb13-4e17-8465-484bcd3c6957
title: Mise à jour de la table de mise à niveau pour une mise à niveau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1b4c2cc2b650d49fb4ba40f97d69ed84911273
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115079"
---
# <a name="updating-upgrade-table-for-an-upgrade"></a><span data-ttu-id="d9da0-103">Mise à jour de la table de mise à niveau pour une mise à niveau</span><span class="sxs-lookup"><span data-stu-id="d9da0-103">Updating Upgrade Table for an Upgrade</span></span>

<span data-ttu-id="d9da0-104">Pour appliquer une mise à niveau majeure à l’aide de Windows Installer, le package d’installation du produit d’origine doit spécifier une propriété [**UpgradeCode**](upgradecode.md) , décrite dans [préparation d’une application pour les futures mises à niveau majeures](preparing-an-application-for-future-major-upgrades.md), et le package de mise à niveau doit avoir une [table de mise](upgrade-table.md)à niveau.</span><span class="sxs-lookup"><span data-stu-id="d9da0-104">To apply a major upgrade using Windows Installer, the original product installation package must specify an [**UpgradeCode**](upgradecode.md) Property, described in [Preparing an Application for Future Major Upgrades](preparing-an-application-for-future-major-upgrades.md), and the upgrade package must have an [Upgrade table](upgrade-table.md).</span></span>

<span data-ttu-id="d9da0-105">Pour plus d’informations sur les mises à niveau majeures, consultez [mises à niveau majeures](major-upgrades.md) dans [correctifs et mises à niveau](patching-and-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="d9da0-105">For more information about major upgrades, see [Major Upgrades](major-upgrades.md) in [Patching and Upgrades](patching-and-upgrades.md).</span></span>

<span data-ttu-id="d9da0-106">La propriété [**UpgradeCode**](upgradecode.md) du package d’installation de MNP2000.msi a été affectée, comme décrit dans la section [spécification des propriétés](specifying-properties.md).</span><span class="sxs-lookup"><span data-stu-id="d9da0-106">The installation package of MNP2000.msi was assigned an [**UpgradeCode**](upgradecode.md) property, as described in the section [Specifying Properties](specifying-properties.md).</span></span>

<span data-ttu-id="d9da0-107">Windows Installer applique la mise à niveau si l’utilisateur a déjà installé les versions 1,0 à 1,4 (inclusives) de la langue anglaise MNP2000.</span><span class="sxs-lookup"><span data-stu-id="d9da0-107">Windows Installer applies the upgrade if the user has already installed the 1.0 to 1.4 versions (inclusive) of English language MNP2000.</span></span> <span data-ttu-id="d9da0-108">Windows Installer migre tous les paramètres de fonctionnalité du produit d’origine vers le produit mis à niveau.</span><span class="sxs-lookup"><span data-stu-id="d9da0-108">Windows Installer migrates all of the original product's feature settings to the upgraded product.</span></span> <span data-ttu-id="d9da0-109">Le programme d’installation supprime les fichiers appartenant aux produits originaux qui ne sont pas utilisés par la mise à niveau du produit.</span><span class="sxs-lookup"><span data-stu-id="d9da0-109">The installer removes the files belonging to the original products not being used by the product's upgrade.</span></span>

<span data-ttu-id="d9da0-110">Si votre copie de MNP2001.msi n’inclut pas de [table de mise à niveau](upgrade-table.md), utilisez Orca ou un autre éditeur de table pour importer une table de mise à niveau vide dans la base de données à partir de Schema.msi.</span><span class="sxs-lookup"><span data-stu-id="d9da0-110">If your copy of MNP2001.msi does not include an [Upgrade table](upgrade-table.md), use Orca, or another table editor, to import an empty Upgrade table into the database from Schema.msi.</span></span> <span data-ttu-id="d9da0-111">Le kit de développement logiciel (SDK) fournit une copie de Schema.msi.</span><span class="sxs-lookup"><span data-stu-id="d9da0-111">The SDK provides a copy of Schema.msi.</span></span> <span data-ttu-id="d9da0-112">Utilisez votre éditeur de base de données pour ouvrir MNP2001.msi et entrez les données suivantes dans la table de mise à niveau vide.</span><span class="sxs-lookup"><span data-stu-id="d9da0-112">Use your database editor to open MNP2001.msi and enter the following data into the empty Upgrade table.</span></span>



| <span data-ttu-id="d9da0-113">UpgradeCode</span><span class="sxs-lookup"><span data-stu-id="d9da0-113">UpgradeCode</span></span>                            | <span data-ttu-id="d9da0-114">VersionMin</span><span class="sxs-lookup"><span data-stu-id="d9da0-114">VersionMin</span></span> | <span data-ttu-id="d9da0-115">VersionMax</span><span class="sxs-lookup"><span data-stu-id="d9da0-115">VersionMax</span></span> | <span data-ttu-id="d9da0-116">Language</span><span class="sxs-lookup"><span data-stu-id="d9da0-116">Language</span></span> | <span data-ttu-id="d9da0-117">Attributs</span><span class="sxs-lookup"><span data-stu-id="d9da0-117">Attributes</span></span> | <span data-ttu-id="d9da0-118">Supprimer</span><span class="sxs-lookup"><span data-stu-id="d9da0-118">Remove</span></span> | <span data-ttu-id="d9da0-119">ActionProperty</span><span class="sxs-lookup"><span data-stu-id="d9da0-119">ActionProperty</span></span> |
|----------------------------------------|------------|------------|----------|------------|--------|----------------|
| <span data-ttu-id="d9da0-120">{908E378A-9551-4772-BF1D-5CFAF6FD9CB4}</span><span class="sxs-lookup"><span data-stu-id="d9da0-120">{908E378A-9551-4772-BF1D-5CFAF6FD9CB4}</span></span> | <span data-ttu-id="d9da0-121">01.00.0000</span><span class="sxs-lookup"><span data-stu-id="d9da0-121">01.00.0000</span></span> | <span data-ttu-id="d9da0-122">01.40.0000</span><span class="sxs-lookup"><span data-stu-id="d9da0-122">01.40.0000</span></span> | <span data-ttu-id="d9da0-123">1033</span><span class="sxs-lookup"><span data-stu-id="d9da0-123">1033</span></span>     | <span data-ttu-id="d9da0-124">769</span><span class="sxs-lookup"><span data-stu-id="d9da0-124">769</span></span>        |        | <span data-ttu-id="d9da0-125">OLDAPPFOUND</span><span class="sxs-lookup"><span data-stu-id="d9da0-125">OLDAPPFOUND</span></span>    |



 

[<span data-ttu-id="d9da0-126">Continuer</span><span class="sxs-lookup"><span data-stu-id="d9da0-126">Continue</span></span>](updating-properties-for-an-upgrade.md)

 

 



