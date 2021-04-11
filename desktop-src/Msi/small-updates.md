---
description: Une petite mise à jour apporte des modifications à un ou plusieurs fichiers d’application qui sont trop mineurs pour justifier la modification du code du produit.
ms.assetid: c74ef2bd-9cf5-4ec0-bfff-1fad0e17ba98
title: Petites mises à jour
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ca87e825f462a98cc7fc80ad42d2b09b7931d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112255"
---
# <a name="small-updates"></a><span data-ttu-id="a4ca2-103">Petites mises à jour</span><span class="sxs-lookup"><span data-stu-id="a4ca2-103">Small Updates</span></span>

<span data-ttu-id="a4ca2-104">Une petite mise à jour apporte des modifications à un ou plusieurs fichiers d’application qui sont trop mineurs pour justifier la modification du code du produit.</span><span class="sxs-lookup"><span data-stu-id="a4ca2-104">A small update makes changes to one or more application files that are too minor to warrant changing the product code.</span></span> <span data-ttu-id="a4ca2-105">Une petite mise à jour est également communément appelée mise à jour QFE (Quick Fix Engineering).</span><span class="sxs-lookup"><span data-stu-id="a4ca2-105">A small update is also commonly referred to as a quick fix engineering (QFE) update.</span></span> <span data-ttu-id="a4ca2-106">Une petite mise à jour n’autorise pas la réorganisation de l’arborescence des composants de fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="a4ca2-106">A small update does not permit reorganization of the feature-component tree.</span></span>

<span data-ttu-id="a4ca2-107">Une petite mise à jour classique ne modifie qu’un ou deux fichiers ou une clé de registre.</span><span class="sxs-lookup"><span data-stu-id="a4ca2-107">A typical small update changes only one or two files or a registry key.</span></span> <span data-ttu-id="a4ca2-108">Étant donné qu’une petite mise à jour modifie les informations dans le fichier. msi, le code du package d’installation doit être modifié.</span><span class="sxs-lookup"><span data-stu-id="a4ca2-108">Because a small update changes the information in the .msi file, the installation package code must be changed.</span></span> <span data-ttu-id="a4ca2-109">Le code du package est stocké dans la propriété [**Résumé du numéro de révision**](revision-number-summary.md) du flux d’informations de [synthèse](summary-information-stream.md).</span><span class="sxs-lookup"><span data-stu-id="a4ca2-109">The package code is stored in the [**Revision Number Summary**](revision-number-summary.md) property of the [Summary Information Stream](summary-information-stream.md).</span></span>

<span data-ttu-id="a4ca2-110">Le code du produit n’est jamais modifié avec une petite mise à jour. par conséquent, toutes les modifications introduites par une petite mise à jour doivent être cohérentes avec les instructions décrites dans [modification du code du produit](changing-the-product-code.md).</span><span class="sxs-lookup"><span data-stu-id="a4ca2-110">The product code is never changed with a small update, so all of the changes introduced by a small update have to be consistent with the guidelines described in [Changing the Product Code](changing-the-product-code.md).</span></span> <span data-ttu-id="a4ca2-111">Une mise à jour requiert une [mise à niveau majeure](major-upgrades.md) pour modifier la valeur [**ProductCode**](productcode.md).</span><span class="sxs-lookup"><span data-stu-id="a4ca2-111">An update requires a [major upgrade](major-upgrades.md) to change the [**ProductCode**](productcode.md).</span></span> <span data-ttu-id="a4ca2-112">S’il est nécessaire de faire la différence entre les produits sans modifier le code du produit, utilisez une [mise à niveau mineure](minor-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="a4ca2-112">If it is necessary to differentiate between products without changing the product code, use a [minor upgrade](minor-upgrades.md).</span></span>

<span data-ttu-id="a4ca2-113">Pour plus d’informations sur l’application d’un package de correctifs de mise à jour à un package de Windows Installer, consultez [création d’un correctif logiciel](creating-a-small-update-patch.md)de petite mise à jour, [application de petites mises à jour en corrigeant l’installation locale du produit](applying-small-updates-by-patching-the-local-installation-of-the-product.md), [application de petites mises à jour en réinstallant le produit](applying-small-updates-by-reinstalling-the-product.md)et [application de petites mises à jour en corrigeant une image administrative](applying-small-updates-by-patching-an-administrative-image.md).</span><span class="sxs-lookup"><span data-stu-id="a4ca2-113">For information on how to apply a small update patch package to a Windows Installer package, see [Creating a Small Update Patch](creating-a-small-update-patch.md), [Applying Small Updates by Patching the Local Installation of the Product](applying-small-updates-by-patching-the-local-installation-of-the-product.md), [Applying Small Updates by Reinstalling the Product](applying-small-updates-by-reinstalling-the-product.md), and [Applying Small Updates by Patching an Administrative Image](applying-small-updates-by-patching-an-administrative-image.md).</span></span>

 

 



