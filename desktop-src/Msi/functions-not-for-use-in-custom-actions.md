---
description: Les fonctions de base de données suivantes ne doivent jamais être appelées à partir d’une action personnalisée.
ms.assetid: 55fdd82b-9f34-4c2c-a837-8a09f21f568a
title: Fonctions non utilisables dans les actions personnalisées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c77c4714ca65614200cf77d6b207b6eebcaf179
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519385"
---
# <a name="functions-not-for-use-in-custom-actions"></a><span data-ttu-id="a19b5-103">Fonctions non utilisables dans les actions personnalisées</span><span class="sxs-lookup"><span data-stu-id="a19b5-103">Functions Not for Use in Custom Actions</span></span>

<span data-ttu-id="a19b5-104">Les [fonctions de base de données](database-functions.md) suivantes ne doivent jamais être appelées à partir d’une action personnalisée.</span><span class="sxs-lookup"><span data-stu-id="a19b5-104">The following [Database Functions](database-functions.md) must never be called from a custom action.</span></span>

-   [<span data-ttu-id="a19b5-105">**MsiConfigureProduct**</span><span class="sxs-lookup"><span data-stu-id="a19b5-105">**MsiConfigureProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)
-   [<span data-ttu-id="a19b5-106">**MsiConfigureProductEx**</span><span class="sxs-lookup"><span data-stu-id="a19b5-106">**MsiConfigureProductEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msiconfigureproductexa)
-   [<span data-ttu-id="a19b5-107">**MsiCreateTransformSummaryInfo**</span><span class="sxs-lookup"><span data-stu-id="a19b5-107">**MsiCreateTransformSummaryInfo**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)
-   [<span data-ttu-id="a19b5-108">**MsiDatabaseApplyTransform**</span><span class="sxs-lookup"><span data-stu-id="a19b5-108">**MsiDatabaseApplyTransform**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma)
-   [<span data-ttu-id="a19b5-109">**MsiDatabaseCommit**</span><span class="sxs-lookup"><span data-stu-id="a19b5-109">**MsiDatabaseCommit**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)
-   [<span data-ttu-id="a19b5-110">**MsiDatabaseExport**</span><span class="sxs-lookup"><span data-stu-id="a19b5-110">**MsiDatabaseExport**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)
-   [<span data-ttu-id="a19b5-111">**MsiDatabaseGenerateTransform**</span><span class="sxs-lookup"><span data-stu-id="a19b5-111">**MsiDatabaseGenerateTransform**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma)
-   [<span data-ttu-id="a19b5-112">**MsiDatabaseImport**</span><span class="sxs-lookup"><span data-stu-id="a19b5-112">**MsiDatabaseImport**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)
-   [<span data-ttu-id="a19b5-113">**MsiDatabaseMerge**</span><span class="sxs-lookup"><span data-stu-id="a19b5-113">**MsiDatabaseMerge**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea)
-   [<span data-ttu-id="a19b5-114">**MsiEnableLog**</span><span class="sxs-lookup"><span data-stu-id="a19b5-114">**MsiEnableLog**</span></span>](/windows/desktop/api/Msi/nf-msi-msienableloga)
-   [<span data-ttu-id="a19b5-115">**MsiEnableUIPreview**</span><span class="sxs-lookup"><span data-stu-id="a19b5-115">**MsiEnableUIPreview**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview)
-   [<span data-ttu-id="a19b5-116">**MsiGetDatabaseState**</span><span class="sxs-lookup"><span data-stu-id="a19b5-116">**MsiGetDatabaseState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate)
-   [<span data-ttu-id="a19b5-117">**MsiOpenDatabase**</span><span class="sxs-lookup"><span data-stu-id="a19b5-117">**MsiOpenDatabase**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea)
-   [<span data-ttu-id="a19b5-118">**MsiPreviewBillboard**</span><span class="sxs-lookup"><span data-stu-id="a19b5-118">**MsiPreviewBillboard**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewbillboarda)
-   [<span data-ttu-id="a19b5-119">**MsiPreviewDialog**</span><span class="sxs-lookup"><span data-stu-id="a19b5-119">**MsiPreviewDialog**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewdialoga)
-   [<span data-ttu-id="a19b5-120">**MsiReinstallProduct**</span><span class="sxs-lookup"><span data-stu-id="a19b5-120">**MsiReinstallProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msireinstallproducta)
-   [<span data-ttu-id="a19b5-121">**MsiSetExternalUI**</span><span class="sxs-lookup"><span data-stu-id="a19b5-121">**MsiSetExternalUI**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)
-   [<span data-ttu-id="a19b5-122">**MsiSetExternalUIRecord**</span><span class="sxs-lookup"><span data-stu-id="a19b5-122">**MsiSetExternalUIRecord**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetexternaluirecord)
-   [<span data-ttu-id="a19b5-123">**MsiSetInternalUI**</span><span class="sxs-lookup"><span data-stu-id="a19b5-123">**MsiSetInternalUI**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetinternalui)

<span data-ttu-id="a19b5-124">Les [fonctions de programme d’installation](installer-function-reference.md) suivantes ne doivent jamais être appelées à partir d’une action personnalisée.</span><span class="sxs-lookup"><span data-stu-id="a19b5-124">The following [Installer Functions](installer-function-reference.md) must never be called from a custom action.</span></span>

-   [<span data-ttu-id="a19b5-125">**MsiApplyPatch**</span><span class="sxs-lookup"><span data-stu-id="a19b5-125">**MsiApplyPatch**</span></span>](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)
-   [<span data-ttu-id="a19b5-126">**MsiCollectUserInfo**</span><span class="sxs-lookup"><span data-stu-id="a19b5-126">**MsiCollectUserInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa)
-   [<span data-ttu-id="a19b5-127">**MsiConfigureFeature**</span><span class="sxs-lookup"><span data-stu-id="a19b5-127">**MsiConfigureFeature**</span></span>](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea)
-   [<span data-ttu-id="a19b5-128">**MsiConfigureProduct**</span><span class="sxs-lookup"><span data-stu-id="a19b5-128">**MsiConfigureProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)
-   [<span data-ttu-id="a19b5-129">**MsiConfigureProductEx**</span><span class="sxs-lookup"><span data-stu-id="a19b5-129">**MsiConfigureProductEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msiconfigureproductexa)
-   [<span data-ttu-id="a19b5-130">**MsiEnableLog**</span><span class="sxs-lookup"><span data-stu-id="a19b5-130">**MsiEnableLog**</span></span>](/windows/desktop/api/Msi/nf-msi-msienableloga)
-   [<span data-ttu-id="a19b5-131">**MsiGetFeatureInfo**</span><span class="sxs-lookup"><span data-stu-id="a19b5-131">**MsiGetFeatureInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfeatureinfoa)
-   [<span data-ttu-id="a19b5-132">**MsiGetProductCode**</span><span class="sxs-lookup"><span data-stu-id="a19b5-132">**MsiGetProductCode**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetproductcodea)
-   [<span data-ttu-id="a19b5-133">**MsiGetProductProperty**</span><span class="sxs-lookup"><span data-stu-id="a19b5-133">**MsiGetProductProperty**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya)
-   [<span data-ttu-id="a19b5-134">**MsiInstallMissingComponent**</span><span class="sxs-lookup"><span data-stu-id="a19b5-134">**MsiInstallMissingComponent**</span></span>](/windows/desktop/api/Msi/nf-msi-msiinstallmissingcomponenta)
-   [<span data-ttu-id="a19b5-135">**MsiInstallMissingFile**</span><span class="sxs-lookup"><span data-stu-id="a19b5-135">**MsiInstallMissingFile**</span></span>](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea)
-   [<span data-ttu-id="a19b5-136">**MsiInstallProduct**</span><span class="sxs-lookup"><span data-stu-id="a19b5-136">**MsiInstallProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msiinstallproducta)
-   [<span data-ttu-id="a19b5-137">**MsiOpenPackage**</span><span class="sxs-lookup"><span data-stu-id="a19b5-137">**MsiOpenPackage**</span></span>](/windows/desktop/api/Msi/nf-msi-msiopenpackagea)
-   [<span data-ttu-id="a19b5-138">**MsiOpenProduct**</span><span class="sxs-lookup"><span data-stu-id="a19b5-138">**MsiOpenProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msiopenproducta)
-   [<span data-ttu-id="a19b5-139">**MsiReinstallFeature**</span><span class="sxs-lookup"><span data-stu-id="a19b5-139">**MsiReinstallFeature**</span></span>](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea)
-   [<span data-ttu-id="a19b5-140">**MsiReinstallProduct**</span><span class="sxs-lookup"><span data-stu-id="a19b5-140">**MsiReinstallProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msireinstallproducta)
-   [<span data-ttu-id="a19b5-141">**MsiSetExternalUI**</span><span class="sxs-lookup"><span data-stu-id="a19b5-141">**MsiSetExternalUI**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)
-   [<span data-ttu-id="a19b5-142">**MsiSetInternalUI**</span><span class="sxs-lookup"><span data-stu-id="a19b5-142">**MsiSetInternalUI**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetinternalui)
-   [<span data-ttu-id="a19b5-143">**MsiUseFeature**</span><span class="sxs-lookup"><span data-stu-id="a19b5-143">**MsiUseFeature**</span></span>](/windows/desktop/api/Msi/nf-msi-msiusefeaturea)
-   [<span data-ttu-id="a19b5-144">**MsiUseFeatureEx**</span><span class="sxs-lookup"><span data-stu-id="a19b5-144">**MsiUseFeatureEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msiusefeatureexa)
-   [<span data-ttu-id="a19b5-145">**MsiVerifyPackage**</span><span class="sxs-lookup"><span data-stu-id="a19b5-145">**MsiVerifyPackage**</span></span>](/windows/desktop/api/Msi/nf-msi-msiverifypackagea)

<span data-ttu-id="a19b5-146">Les [fonctions de programme d’installation](installer-function-reference.md) suivantes ne doivent jamais être appelées à partir d’une action personnalisée si cela démarre une autre installation.</span><span class="sxs-lookup"><span data-stu-id="a19b5-146">The following [Installer Functions](installer-function-reference.md) must never be called from a custom action if doing so starts another installation.</span></span> <span data-ttu-id="a19b5-147">Elles peuvent être appelées à partir d’une action personnalisée qui ne démarre pas une autre installation.</span><span class="sxs-lookup"><span data-stu-id="a19b5-147">They may be called from a custom action that does not start another installation.</span></span>

-   [<span data-ttu-id="a19b5-148">**MsiProvideComponent**</span><span class="sxs-lookup"><span data-stu-id="a19b5-148">**MsiProvideComponent**</span></span>](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)
-   [<span data-ttu-id="a19b5-149">**MsiProvideQualifiedComponent**</span><span class="sxs-lookup"><span data-stu-id="a19b5-149">**MsiProvideQualifiedComponent**</span></span>](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta)
-   [<span data-ttu-id="a19b5-150">**MsiProvideQualifiedComponentEx**</span><span class="sxs-lookup"><span data-stu-id="a19b5-150">**MsiProvideQualifiedComponentEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa)

<span data-ttu-id="a19b5-151">Une action personnalisée ne doit jamais générer un nouveau thread qui utilise Windows Installer fonctions pour modifier l’état de la fonctionnalité, l’état du composant ou pour envoyer des messages à partir d’un événement de contrôle.</span><span class="sxs-lookup"><span data-stu-id="a19b5-151">A custom action should never spawn a new thread that uses Windows Installer functions to change the feature state, component state, or to send messages from a Control Event.</span></span> <span data-ttu-id="a19b5-152">Si vous tentez de le faire, l’installation échoue.</span><span class="sxs-lookup"><span data-stu-id="a19b5-152">Attempting to do this causes the installation to fail.</span></span>

 

 



