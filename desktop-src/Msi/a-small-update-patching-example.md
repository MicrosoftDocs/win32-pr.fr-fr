---
description: Cet exemple montre comment créer un package de correctifs qui applique une petite mise à jour de l’exemple de package d’installation abordé dans un exemple d’installation.
ms.assetid: 17dadd64-6e81-444a-985e-1b340e4f2ee5
title: Exemple de mise à jour corrective de petite taille
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36d4997a326e8fea33086a75c9cf40ecef8cb997
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527857"
---
# <a name="a-small-update-patching-example"></a><span data-ttu-id="72afa-103">Exemple de mise à jour corrective de petite taille</span><span class="sxs-lookup"><span data-stu-id="72afa-103">A Small Update Patching Example</span></span>

<span data-ttu-id="72afa-104">Cet exemple montre comment créer un package de [correctifs](patch-packages.md) qui applique une [petite mise à jour](small-updates.md) de l’exemple de package d’installation abordé dans [un exemple d’installation](an-installation-example.md).</span><span class="sxs-lookup"><span data-stu-id="72afa-104">This example illustrates how to create a [patch package](patch-packages.md) that applies a [small update](small-updates.md) to the sample installation package discussed in [An Installation Example](an-installation-example.md).</span></span> <span data-ttu-id="72afa-105">Une petite mise à jour apporte des modifications à un ou plusieurs fichiers d’application qui sont jugés trop mineurs pour justifier la modification du code du produit.</span><span class="sxs-lookup"><span data-stu-id="72afa-105">A small update makes changes to one or more application files that are judged to be too minor to warrant changing the product code.</span></span> <span data-ttu-id="72afa-106">Pour plus d’informations [, consultez Mise à jour corrective et mises à niveau](patching-and-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="72afa-106">For more information see [Patching and Upgrades](patching-and-upgrades.md).</span></span>

<span data-ttu-id="72afa-107">Cet exemple montre comment créer un package de correctifs Windows Installer qui met à jour la fonctionnalité de concert du produit hypothétique MNP2000 pour résoudre une erreur dans le produit d’origine.</span><span class="sxs-lookup"><span data-stu-id="72afa-107">This example illustrates how to create a Windows Installer patch package that updates the Concert feature of the hypothetical product MNP2000 to fix an error in the original product.</span></span> <span data-ttu-id="72afa-108">L’exemple de package correctif applique une petite mise à jour du produit qui ne nécessite pas de modification du code du produit.</span><span class="sxs-lookup"><span data-stu-id="72afa-108">The example patch package applies a small update to the product that does not require changing the product code.</span></span> <span data-ttu-id="72afa-109">Pour plus d’informations sur les principales mises à niveau, consultez la rubrique sur les [mises à niveau majeures](major-upgrades.md) dans la section [correctifs et mises à niveau](patching-and-upgrades.md) .</span><span class="sxs-lookup"><span data-stu-id="72afa-109">See the topic on [Major Upgrades](major-upgrades.md) in the [Patching and Upgrades](patching-and-upgrades.md) section for more information about major upgrades.</span></span>

<span data-ttu-id="72afa-110">L’exemple de package de mise à niveau présente les spécifications suivantes :</span><span class="sxs-lookup"><span data-stu-id="72afa-110">The sample upgrade package has the following specifications:</span></span>

-   <span data-ttu-id="72afa-111">Il corrige une erreur mineure dans la planification de concert affichée par la fonctionnalité de concert.</span><span class="sxs-lookup"><span data-stu-id="72afa-111">It corrects a minor error in the Concert schedule displayed by the Concert feature.</span></span>
-   <span data-ttu-id="72afa-112">Il met à jour le code du package pour refléter la modification du package d’installation.</span><span class="sxs-lookup"><span data-stu-id="72afa-112">It updates the package code to reflect the installation package has changed.</span></span>
-   <span data-ttu-id="72afa-113">La petite mise à jour peut être appliquée en appliquant des correctifs à l’installation locale du produit.</span><span class="sxs-lookup"><span data-stu-id="72afa-113">The small update can be applied by patching the local installation of the product.</span></span>

[<span data-ttu-id="72afa-114">Continuer</span><span class="sxs-lookup"><span data-stu-id="72afa-114">Continue</span></span>](planning-a-small-update-patch.md)

 

 



