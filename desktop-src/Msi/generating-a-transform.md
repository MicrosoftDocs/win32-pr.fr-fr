---
description: La procédure suivante décrit un scénario permettant de générer une transformation qui masque définitivement une fonctionnalité.
ms.assetid: 43f36866-a9df-4035-a8ae-5ccbcb628a90
title: Génération d’une transformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0543ae74f71155e6fcd504ebee677558f21bbfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034793"
---
# <a name="generating-a-transform"></a><span data-ttu-id="035c0-103">Génération d’une transformation</span><span class="sxs-lookup"><span data-stu-id="035c0-103">Generating a Transform</span></span>

<span data-ttu-id="035c0-104">La procédure suivante décrit un scénario permettant de générer une transformation qui masque définitivement une fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="035c0-104">The following procedure describes a scenario to generate a transform that permanently hides a feature.</span></span>

<span data-ttu-id="035c0-105">**Pour masquer définitivement une fonctionnalité de produit**</span><span class="sxs-lookup"><span data-stu-id="035c0-105">**To permanently hide a product feature**</span></span>

1.  <span data-ttu-id="035c0-106">Copiez le package d’installation d’origine.</span><span class="sxs-lookup"><span data-stu-id="035c0-106">Copy the original installation package.</span></span>
2.  <span data-ttu-id="035c0-107">Modifiez la copie en affectant à la colonne d’affichage de la [table de fonctionnalités](feature-table.md) la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="035c0-107">Alter the copy by setting the value of the Display column in the [Feature table](feature-table.md) to zero.</span></span> <span data-ttu-id="035c0-108">Cela permet de masquer la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="035c0-108">This specifies hiding the feature.</span></span>
3.  <span data-ttu-id="035c0-109">Créez une transformation à partir du package d’installation d’origine vers les nouveaux packages d’installation en appelant [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma).</span><span class="sxs-lookup"><span data-stu-id="035c0-109">Create a transform from the original installation package to the new installation packages by calling [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma).</span></span>
4.  <span data-ttu-id="035c0-110">Créez les informations de résumé dans la transformation en appelant [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).</span><span class="sxs-lookup"><span data-stu-id="035c0-110">Create the summary information in the transform by calling [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).</span></span>

<span data-ttu-id="035c0-111">La transformation est ensuite prête à être appliquée lors de l’installation.</span><span class="sxs-lookup"><span data-stu-id="035c0-111">The transform is then ready to be applied during installation.</span></span> <span data-ttu-id="035c0-112">Pour plus d’informations, consultez [application de transformations](applying-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="035c0-112">For more information, see [Applying Transforms](applying-transforms.md).</span></span>

 

 



