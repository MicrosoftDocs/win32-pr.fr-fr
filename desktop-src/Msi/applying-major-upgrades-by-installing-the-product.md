---
description: Une mise à niveau majeure peut être appliquée en installant le nouveau package d’installation pour le produit mis à niveau.
ms.assetid: f4fb28be-5ec0-4eac-9d4d-eccf5bd61ac4
title: Application de mises à niveau majeures en installant le produit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7619b2ae2b8e1f10cac2fcfae61dde0c6dbba5d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529799"
---
# <a name="applying-major-upgrades-by-installing-the-product"></a><span data-ttu-id="4c005-103">Application de mises à niveau majeures en installant le produit</span><span class="sxs-lookup"><span data-stu-id="4c005-103">Applying Major Upgrades by Installing the Product</span></span>

<span data-ttu-id="4c005-104">Une mise à niveau majeure peut être appliquée en installant le nouveau package d’installation pour le produit mis à niveau.</span><span class="sxs-lookup"><span data-stu-id="4c005-104">A major upgrade can be applied by installing the new installation package for the upgraded product.</span></span> <span data-ttu-id="4c005-105">Les mises à niveau majeures obtenant un code de produit différent de celui du produit d’origine, l’installation de la mise à niveau doit être traitée comme une installation d’un nouveau produit.</span><span class="sxs-lookup"><span data-stu-id="4c005-105">Because major upgrades get a different product code than the original product, installing the upgrade must be treated as an installation of a new product.</span></span> <span data-ttu-id="4c005-106">La mise à niveau peut simplement être installée comme un autre produit.</span><span class="sxs-lookup"><span data-stu-id="4c005-106">The upgrade can simply be installed like another product.</span></span> <span data-ttu-id="4c005-107">Vous pouvez faire en sorte que le nouveau package d’installation traite la suppression de l’ancien produit en incluant la [table de mise à niveau](upgrade-table.md) et l’action [FindRelatedProducts](findrelatedproducts-action.md) et l' [action RemoveExistingProducts](removeexistingproducts-action.md).</span><span class="sxs-lookup"><span data-stu-id="4c005-107">You can have the new installation package handle the removal of the old product by including the [Upgrade table](upgrade-table.md) and the [FindRelatedProducts action](findrelatedproducts-action.md) and [RemoveExistingProducts action](removeexistingproducts-action.md).</span></span>

<span data-ttu-id="4c005-108">**Pour propager une mise à niveau majeure aux utilisateurs actuels à partir de la ligne de commande**</span><span class="sxs-lookup"><span data-stu-id="4c005-108">**To propagate a major upgrade to current users from the command line**</span></span>

-   <span data-ttu-id="4c005-109">À partir de la ligne de commande, utilisez : **msiexec \[ /i** _chemin d’accès au fichier msi mis à jour_*_\]_*</span><span class="sxs-lookup"><span data-stu-id="4c005-109">From the command line, use: **msiexec /i \[**_path to updated msi file_*_\]_*</span></span>

<span data-ttu-id="4c005-110">**Pour propager une mise à niveau majeure à des utilisateurs actuels à partir d’un programme**</span><span class="sxs-lookup"><span data-stu-id="4c005-110">**To propagate a major upgrade to current users from a program**</span></span>

-   <span data-ttu-id="4c005-111">À partir d’un programme, appelez [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) et spécifiez le chemin d’accès au fichier msi mis à jour.</span><span class="sxs-lookup"><span data-stu-id="4c005-111">From a program, call [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) and specify the path to the updated msi file.</span></span>

 

 



