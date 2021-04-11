---
description: Les auteurs doivent exécuter la validation à chaque nouveau module de fusion, ou nouvellement modifié, avant de tenter de fusionner le module dans une base de données d’installation pour la première fois.
ms.assetid: 8d6794af-403a-416e-8ace-1af3f193414b
title: Validation des modules de fusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d8bbe7f1c1ea32baa39cadd7c729f3a8ca3ac17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113826"
---
# <a name="validating-merge-modules"></a><span data-ttu-id="31d90-103">Validation des modules de fusion</span><span class="sxs-lookup"><span data-stu-id="31d90-103">Validating Merge Modules</span></span>

<span data-ttu-id="31d90-104">Les auteurs doivent exécuter la validation à chaque nouveau module de fusion, ou nouvellement modifié, avant de tenter de fusionner le module dans une base de données d’installation pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="31d90-104">Authors should run validation on every new, or newly modified, merge module before attempting to merge the module into an installation database for the first time.</span></span> <span data-ttu-id="31d90-105">La validation du module de fusion fonctionne de la même façon que la [validation du package](package-validation.md) , mais utilise un ensemble différent d' [évaluateurs de cohérence internes](internal-consistency-evaluators-ices.md) (ICEs) spécifique aux modules de fusion.</span><span class="sxs-lookup"><span data-stu-id="31d90-105">Merge module validation works in the same way as [package validation](package-validation.md) but uses a different set of [Internal Consistency Evaluators](internal-consistency-evaluators-ices.md) (ICEs) specific to merge modules.</span></span> <span data-ttu-id="31d90-106">Pour plus d’informations sur le CIEM du module de fusion, consultez Référence de la [glace du module de fusion](merge-module-ice-reference.md).</span><span class="sxs-lookup"><span data-stu-id="31d90-106">For more information about these merge module ICEs, see [Merge Module ICE Reference](merge-module-ice-reference.md).</span></span>

<span data-ttu-id="31d90-107">Le module de fusion CIEM est stocké dans le fichier. CUB du module de fusion, Mergemod. CUB.</span><span class="sxs-lookup"><span data-stu-id="31d90-107">Merge module ICEs are stored in the merge module .cub file, Mergemod.cub.</span></span> <span data-ttu-id="31d90-108">L’installation de l’outil Orca ou de MSIVal2 fournit également les fichiers logo. CUB, Darice. CUB et Mergemod. CUB.</span><span class="sxs-lookup"><span data-stu-id="31d90-108">The installation of the Orca tool or msival2 also provides the Logo.cub, Darice.cub, and Mergemod.cub files.</span></span>

<span data-ttu-id="31d90-109">Pour plus d’informations, consultez Référence de la [glace du module de fusion](merge-module-ice-reference.md).</span><span class="sxs-lookup"><span data-stu-id="31d90-109">For more information, see [Merge Module ICE Reference](merge-module-ice-reference.md).</span></span>

 

 



