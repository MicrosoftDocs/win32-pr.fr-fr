---
description: Comment le navigateur de DVD Microsoft sélectionne la région du DVD
ms.assetid: 407619c6-2d4b-4f7f-a861-42ee0f462ecd
title: Comment le navigateur de DVD Microsoft sélectionne la région du DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f8a2898725ad187946b50e567f7daa7e72a9886
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515522"
---
# <a name="how-microsoft-dvd-navigator-selects-the-dvd-region"></a><span data-ttu-id="a2e2b-103">Comment le navigateur de DVD Microsoft sélectionne la région du DVD</span><span class="sxs-lookup"><span data-stu-id="a2e2b-103">How Microsoft DVD Navigator Selects the DVD Region</span></span>

<span data-ttu-id="a2e2b-104">Le navigateur DVD Microsoft utilise l’algorithme suivant pour déterminer la correspondance de la région tout en lisant des disques DVD sur un PC :</span><span class="sxs-lookup"><span data-stu-id="a2e2b-104">The Microsoft DVD Navigator uses the following algorithm to determine region match while playing DVD discs on a PC:</span></span>

1.  <span data-ttu-id="a2e2b-105">Le navigateur DVD obtient la région du disque, la région du lecteur et la région du décodeur.</span><span class="sxs-lookup"><span data-stu-id="a2e2b-105">The DVD Navigator gets the disc region, drive region, and decoder region.</span></span>
2.  <span data-ttu-id="a2e2b-106">Si la région du disque est « toutes les régions », le navigateur DVD lit le disque.</span><span class="sxs-lookup"><span data-stu-id="a2e2b-106">If the disc region is "all regions," the DVD Navigator plays the disc.</span></span>
3.  <span data-ttu-id="a2e2b-107">Si le disque n’est pas marqué pour toutes les régions, le navigateur DVD vérifie si le décodeur a une région prédéfinie.</span><span class="sxs-lookup"><span data-stu-id="a2e2b-107">If the disc is not marked for all regions, the DVD Navigator checks whether the decoder has a preset region.</span></span>
4.  <span data-ttu-id="a2e2b-108">Si le décodeur a une région prédéfinie et qu’il ne correspond pas à la région du disque, le navigateur DVD renvoie une erreur indiquant qu’il ne peut pas lire le disque sur la configuration actuelle du DVD.</span><span class="sxs-lookup"><span data-stu-id="a2e2b-108">If the decoder has a preset region and it does not match the disc region, the DVD Navigator returns an error indicating that it cannot play the disc on the current DVD configuration.</span></span> <span data-ttu-id="a2e2b-109">Terminer</span><span class="sxs-lookup"><span data-stu-id="a2e2b-109">(Exit)</span></span>
5.  <span data-ttu-id="a2e2b-110">Si la région du décodeur n’est pas définie ou est identique à la région du disque, le navigateur DVD vérifie si la région du lecteur est la même que la région du disque.</span><span class="sxs-lookup"><span data-stu-id="a2e2b-110">If the decoder region is not set, or is the same as the disc region, the DVD Navigator checks whether the drive region is the same as the disc region.</span></span>
6.  <span data-ttu-id="a2e2b-111">Si la région du lecteur correspond à la région du disque, le navigateur DVD lit le titre.</span><span class="sxs-lookup"><span data-stu-id="a2e2b-111">If the drive region matches the disc region, the DVD Navigator plays the title.</span></span>
7.  <span data-ttu-id="a2e2b-112">Dans le cas contraire, si la région du pilote ne correspond pas à la région du disque, le navigateur DVD appelle le code pour modifier la région du lecteur.</span><span class="sxs-lookup"><span data-stu-id="a2e2b-112">Otherwise, if the driver region does not match the disc region, the DVD Navigator invokes the code to change the drive's region.</span></span> <span data-ttu-id="a2e2b-113">Si le nombre autorisé de modifications de région est épuisé, la tentative de modification de la région échoue et le titre ne peut pas être lu sur ce système.</span><span class="sxs-lookup"><span data-stu-id="a2e2b-113">If the allowed number of region changes has been exhausted, the region change attempt fails and the title cannot be played on that system.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a2e2b-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a2e2b-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2e2b-115">Prise en charge des modifications de région de DVD dans Windows</span><span class="sxs-lookup"><span data-stu-id="a2e2b-115">DVD Region Change Support in Windows</span></span>](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 



