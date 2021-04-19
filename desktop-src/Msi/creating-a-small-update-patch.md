---
description: Respectez les consignes suivantes lors de la création d’un correctif pour une Windows Installer petite mise à jour.
ms.assetid: 0e57c2aa-e86a-4161-9749-c7963182a6d5
title: Création d’un correctif de mise à jour de petite taille
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d948c871baed7fbc15545ed9669c9864ce954799
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529436"
---
# <a name="creating-a-small-update-patch"></a><span data-ttu-id="78200-103">Création d’un correctif de mise à jour de petite taille</span><span class="sxs-lookup"><span data-stu-id="78200-103">Creating a Small Update Patch</span></span>

<span data-ttu-id="78200-104">Lors de la création d’un correctif pour les [petites mises à jour](small-updates.md), les auteurs doivent respecter les instructions suivantes :</span><span class="sxs-lookup"><span data-stu-id="78200-104">When creating a patch for [small updates](small-updates.md), authors should adhere to the following guidelines:</span></span>

-   <span data-ttu-id="78200-105">Les correctifs de petite mise à jour doivent être conçus pour une installation cible unique.</span><span class="sxs-lookup"><span data-stu-id="78200-105">Small update patches must be designed for a single, target installation.</span></span>
-   <span data-ttu-id="78200-106">Les correctifs de petite mise à jour doivent utiliser la version la plus ancienne comme installation cible.</span><span class="sxs-lookup"><span data-stu-id="78200-106">Small update patches should use the earliest version as the target installation.</span></span>
-   <span data-ttu-id="78200-107">Un correctif logiciel de petite mise à jour doit remplacer et rendre obsolète les correctifs de mise à jour antérieurs.</span><span class="sxs-lookup"><span data-stu-id="78200-107">A small update patch should replace and make obsolete any earlier small update patches.</span></span>

<span data-ttu-id="78200-108">Le scénario suivant illustre le meilleur choix d’un correctif de mise à jour de petite taille.</span><span class="sxs-lookup"><span data-stu-id="78200-108">The following scenario illustrates when a small update patch is best.</span></span>

<span data-ttu-id="78200-109">Votre société livre la version 1,0 de Myproduct.msi.</span><span class="sxs-lookup"><span data-stu-id="78200-109">Your company ships version 1.0 of Myproduct.msi.</span></span> <span data-ttu-id="78200-110">Nous vous fournissons bientôt un correctif de [mise à jour de petite taille](small-updates.md) pour Myproduct.msi appelé qfe1.</span><span class="sxs-lookup"><span data-stu-id="78200-110">Shortly thereafter, you ship a [small update](small-updates.md) patch for Myproduct.msi called QFE1.</span></span> <span data-ttu-id="78200-111">Cela ne modifie pas la propriété [**ProductCode**](productcode.md) ou [**ProductVersion**](productversion.md) .</span><span class="sxs-lookup"><span data-stu-id="78200-111">This does not change the [**ProductCode**](productcode.md) property or the [**ProductVersion**](productversion.md) property.</span></span>

<span data-ttu-id="78200-112">Plus tard, vous créerez un deuxième correctif de [mise à jour](small-updates.md) pour Myproduct.msi appelé QFE2.</span><span class="sxs-lookup"><span data-stu-id="78200-112">Later, you author a second [small update](small-updates.md) patch for Myproduct.msi called QFE2.</span></span> <span data-ttu-id="78200-113">Ce deuxième correctif doit cibler la version 1,0 de Myproduct.msi.</span><span class="sxs-lookup"><span data-stu-id="78200-113">This second patch must target Myproduct.msi version 1.0.</span></span> <span data-ttu-id="78200-114">Ce deuxième correctif ne doit pas cibler à la fois Myproduct.msi version 1,0 et Myproduct.msi version 1,0 + QFE1.</span><span class="sxs-lookup"><span data-stu-id="78200-114">This second patch must not target both Myproduct.msi version 1.0 and Myproduct.msi version 1.0 + QFE1.</span></span> <span data-ttu-id="78200-115">Lorsque QFE2 est appliqué, il doit supprimer QFE1.</span><span class="sxs-lookup"><span data-stu-id="78200-115">When QFE2 is applied it should remove QFE1.</span></span>

 

 



