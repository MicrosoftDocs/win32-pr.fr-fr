---
description: Les auteurs des packages d’installation doivent toujours exécuter la validation sur leurs packages avant d’essayer d’installer le package pour la première fois et de réexécuter la validation chaque fois que vous apportez des modifications au package.
ms.assetid: 1f16a349-4919-46d2-9b78-2533b8679a73
title: Validation d’une base de données d’installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6db262a280afa1d9222696d40a6f5949d69ece0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861893"
---
# <a name="validating-an-installation-database"></a><span data-ttu-id="cd20e-103">Validation d’une base de données d’installation</span><span class="sxs-lookup"><span data-stu-id="cd20e-103">Validating an Installation Database</span></span>

<span data-ttu-id="cd20e-104">Les auteurs des packages d’installation doivent toujours exécuter la validation sur leurs packages avant d’essayer d’installer le package pour la première fois et de réexécuter la validation chaque fois que vous apportez des modifications au package.</span><span class="sxs-lookup"><span data-stu-id="cd20e-104">Authors of installation packages should always run validation on their packages before attempting to install the package for the first time and rerun validation whenever making any changes to the package.</span></span> <span data-ttu-id="cd20e-105">La validation analyse la base de données à la recherche d’erreurs qui peuvent sembler valides individuellement, mais qui entraînent un comportement incorrect dans le contexte de la base de données entière.</span><span class="sxs-lookup"><span data-stu-id="cd20e-105">Validation scans the database for errors that may appear valid individually but that cause incorrect behavior in the context of the whole database.</span></span> <span data-ttu-id="cd20e-106">Toute tentative d’installation d’un package dont la validation échoue peut endommager le système de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cd20e-106">Attempting to install a package that fails validation can damage the user's system.</span></span> <span data-ttu-id="cd20e-107">Consultez les sections [validation de package](package-validation.md) et [évaluateur de cohérence interne-ICEs-v](internal-consistency-evaluators-ices.md).</span><span class="sxs-lookup"><span data-stu-id="cd20e-107">See the sections [Package Validation](package-validation.md) and [Internal Consistency Evaluators - ICEs](internal-consistency-evaluators-ices.md).</span></span>

<span data-ttu-id="cd20e-108">Vous pouvez valider l’exemple de package à l’aide de [Orca.exe](orca-exe.md) ou [Msival2.exe](msival2-exe.md).</span><span class="sxs-lookup"><span data-stu-id="cd20e-108">You can validate the sample package using [Orca.exe](orca-exe.md) or [Msival2.exe](msival2-exe.md).</span></span> <span data-ttu-id="cd20e-109">Pour afficher l’aide de Msival2.exe modifier les répertoires et entrez sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="cd20e-109">To view the help for Msival2.exe change directories and enter on the command line.</span></span>

<span data-ttu-id="cd20e-110">Msival2 -?</span><span class="sxs-lookup"><span data-stu-id="cd20e-110">Msival2 -?</span></span>

<span data-ttu-id="cd20e-111">Le fichier. CUB Darice. CUB contient les actions personnalisées ICE requises par Msival2.exe pour effectuer la validation.</span><span class="sxs-lookup"><span data-stu-id="cd20e-111">The .cub file darice.cub contains the ICE custom actions needed by Msival2.exe to perform validation.</span></span> <span data-ttu-id="cd20e-112">Pour valider le MNP2000.msi entrée</span><span class="sxs-lookup"><span data-stu-id="cd20e-112">To validate the MNP2000.msi enter</span></span>

<span data-ttu-id="cd20e-113">MSIVal2 MNP2000.msi Darice. CUB</span><span class="sxs-lookup"><span data-stu-id="cd20e-113">msival2 MNP2000.msi Darice.cub</span></span>

<span data-ttu-id="cd20e-114">Pour obtenir une description des messages d’erreur et d’avertissement retournés par la validation, consultez la [référence Ice](ice-reference.md).</span><span class="sxs-lookup"><span data-stu-id="cd20e-114">For a description of the error and warning messages returned by validation see the [ICE Reference](ice-reference.md).</span></span> <span data-ttu-id="cd20e-115">Corrigez toutes les erreurs dans le package et réexécutez la validation si nécessaire, jusqu’à ce que le package ait réussi la validation sans erreurs.</span><span class="sxs-lookup"><span data-stu-id="cd20e-115">Correct all the errors in the package and rerun validation as necessary until the package passes validation without errors.</span></span>

<span data-ttu-id="cd20e-116">Une fois que le package a réussi la validation, vous pouvez installer l’exemple de package en cliquant sur l’icône MNP2000.msi ou sur la ligne de commande à l’aide des [options de ligne de commande](command-line-options.md).</span><span class="sxs-lookup"><span data-stu-id="cd20e-116">Once the package passes validation, you can install the sample package by clicking on the MNP2000.msi icon or from the command line using the [Command Line Options](command-line-options.md).</span></span>

<span data-ttu-id="cd20e-117">Cela termine l’installation de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="cd20e-117">This completes the sample installation.</span></span>

## <a name="next-example"></a><span data-ttu-id="cd20e-118">Exemple suivant</span><span class="sxs-lookup"><span data-stu-id="cd20e-118">Next example</span></span>

[<span data-ttu-id="cd20e-119">Exemple de mise à niveau</span><span class="sxs-lookup"><span data-stu-id="cd20e-119">An Upgrade Example</span></span>](an-upgrade-example.md)

 

 



