---
description: ICE58 vérifie que votre table des médias ne contient pas plus de 80 lignes.
ms.assetid: 693b195e-1e69-4895-87dd-59714646cff9
title: ICE58
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 152e3a528506861107bfc3c2d64c48935ea7320e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952595"
---
# <a name="ice58"></a><span data-ttu-id="28f01-103">ICE58</span><span class="sxs-lookup"><span data-stu-id="28f01-103">ICE58</span></span>

<span data-ttu-id="28f01-104">ICE58 vérifie que votre [table des médias](media-table.md) ne contient pas plus de 80 lignes.</span><span class="sxs-lookup"><span data-stu-id="28f01-104">ICE58 checks that your [Media table](media-table.md) does not have more than 80 rows.</span></span>

## <a name="result"></a><span data-ttu-id="28f01-105">Résultats</span><span class="sxs-lookup"><span data-stu-id="28f01-105">Result</span></span>

<span data-ttu-id="28f01-106">Les avertissements signalés par ICE58 provoquent l’échec de l’installation, à moins que le package ne soit installé avec Windows Installer 2,0 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="28f01-106">Warnings reported by ICE58 cause the installation to fail unless the package is installed with Windows Installer 2.0 or later.</span></span> <span data-ttu-id="28f01-107">À partir de Windows Installer 2,0, la restriction à plus de 80 entrées de table multimédia est supprimée.</span><span class="sxs-lookup"><span data-stu-id="28f01-107">Beginning with Windows Installer 2.0, the restriction to more than 80 media table entries is removed.</span></span> <span data-ttu-id="28f01-108">Aucun avertissement n’est émis si la propriété de [**Résumé du nombre de pages**](page-count-summary.md) du package est supérieure ou égale à 150.</span><span class="sxs-lookup"><span data-stu-id="28f01-108">No warning is issued if the package's [**Page Count Summary**](page-count-summary.md) Property is greater than or equal to 150.</span></span> <span data-ttu-id="28f01-109">Les packages de schéma 200 ou version ultérieure peuvent uniquement être installés par Windows Installer 2,0 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="28f01-109">Packages of schema 200 or higher can only be installed by Windows Installer 2.0 or later.</span></span>

## <a name="example"></a><span data-ttu-id="28f01-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="28f01-110">Example</span></span>

<span data-ttu-id="28f01-111">ICE58 signale les erreurs et avertissements suivants pour l’exemple indiqué.</span><span class="sxs-lookup"><span data-stu-id="28f01-111">ICE58 reports the following errors and warnings for the example shown.</span></span>

``` syntax
This package has 81 media entries. Packages are limited to 80 entries in the media table.
```

<span data-ttu-id="28f01-112">Pour corriger cette erreur, supprimez toutes les entrées de table de média inutilisées, consolidez les entrées de table de média qui font référence au même support et reconditionnez votre application pour réduire le support requis.</span><span class="sxs-lookup"><span data-stu-id="28f01-112">To fix this error, eliminate any unused media table entries, consolidate media table entries that refer to the same media, and repackage your application to reduce the media required.</span></span>

<span data-ttu-id="28f01-113">[Table des médias](media-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="28f01-113">[Media Table](media-table.md) (partial)</span></span>



| <span data-ttu-id="28f01-114">DiskId</span><span class="sxs-lookup"><span data-stu-id="28f01-114">DiskId</span></span> | <span data-ttu-id="28f01-115">LastSequence\_</span><span class="sxs-lookup"><span data-stu-id="28f01-115">LastSequence\_</span></span> |
|--------|----------------|
| <span data-ttu-id="28f01-116">1</span><span class="sxs-lookup"><span data-stu-id="28f01-116">1</span></span>      | <span data-ttu-id="28f01-117">10</span><span class="sxs-lookup"><span data-stu-id="28f01-117">10</span></span>             |
| <span data-ttu-id="28f01-118">2</span><span class="sxs-lookup"><span data-stu-id="28f01-118">2</span></span>      | <span data-ttu-id="28f01-119">20</span><span class="sxs-lookup"><span data-stu-id="28f01-119">20</span></span>             |
| <span data-ttu-id="28f01-120">...</span><span class="sxs-lookup"><span data-stu-id="28f01-120">...</span></span>    | <span data-ttu-id="28f01-121">...</span><span class="sxs-lookup"><span data-stu-id="28f01-121">...</span></span>            |
| <span data-ttu-id="28f01-122">81</span><span class="sxs-lookup"><span data-stu-id="28f01-122">81</span></span>     | <span data-ttu-id="28f01-123">810</span><span class="sxs-lookup"><span data-stu-id="28f01-123">810</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="28f01-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="28f01-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28f01-125">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="28f01-125">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



