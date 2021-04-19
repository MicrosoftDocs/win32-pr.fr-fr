---
description: Chaque fois que vous apportez des modifications au package, les auteurs des packages de mise à niveau doivent toujours exécuter la validation sur leurs packages avant de tenter d’installer le package pour la première fois et de réexécuter la validation.
ms.assetid: c578c020-18be-47ea-8f59-c1bbd45f1260
title: Validation de la mise à niveau d’une installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cab7f45d3d5c19a71dac8c7a2d0150409b3a45f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538225"
---
# <a name="validating-an-installation-upgrade"></a><span data-ttu-id="491f9-103">Validation de la mise à niveau d’une installation</span><span class="sxs-lookup"><span data-stu-id="491f9-103">Validating an Installation Upgrade</span></span>

<span data-ttu-id="491f9-104">Chaque fois que vous apportez des modifications au package, les auteurs des packages de mise à niveau doivent toujours exécuter la validation sur leurs packages avant de tenter d’installer le package pour la première fois et de réexécuter la validation.</span><span class="sxs-lookup"><span data-stu-id="491f9-104">Whenever making any changes to the package, authors of upgrade packages should always run validation on their packages before attempting to install the package for the first time and rerun validation.</span></span> <span data-ttu-id="491f9-105">Exécutez la validation sur un package de mise à niveau de la même façon que pour un package d’installation.</span><span class="sxs-lookup"><span data-stu-id="491f9-105">Run validation on an upgrade package in the same way as for an installation package.</span></span> <span data-ttu-id="491f9-106">Pour plus d’informations, consultez [validation d’une base de données d’installation](validating-an-installation-database.md).</span><span class="sxs-lookup"><span data-stu-id="491f9-106">For details, see [Validating an Installation Database](validating-an-installation-database.md).</span></span>

<span data-ttu-id="491f9-107">Cela termine l’exemple de package de mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="491f9-107">This completes the sample upgrade package.</span></span> <span data-ttu-id="491f9-108">Pour installer la mise à niveau, installez d’abord MNP2000.msi puis installez MNP2001.msi.</span><span class="sxs-lookup"><span data-stu-id="491f9-108">To install the upgrade first install MNP2000.msi and then install MNP2001.msi.</span></span> <span data-ttu-id="491f9-109">Lorsque vous désinstallez MNP2001, les produits d’origine et de mise à niveau sont supprimés de votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="491f9-109">When you uninstall MNP2001 both the original and upgrade products are removed from your computer.</span></span>

## <a name="next-example"></a><span data-ttu-id="491f9-110">Exemple suivant</span><span class="sxs-lookup"><span data-stu-id="491f9-110">Next example</span></span>

[<span data-ttu-id="491f9-111">Exemple de transformation de personnalisation</span><span class="sxs-lookup"><span data-stu-id="491f9-111">A Customization Transform Example</span></span>](a-customization-transform-example.md)

 

 



