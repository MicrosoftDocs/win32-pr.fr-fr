---
description: Pour obtenir une liste complète des volumes sur un ordinateur, ou pour manipuler chaque volume, vous pouvez énumérer les volumes.
ms.assetid: 5adcd59a-48b7-4373-a10b-c352962f715a
title: Énumération des volumes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc294d72fa3fad24536b175ee7e5e023066586c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531716"
---
# <a name="enumerating-volumes"></a><span data-ttu-id="18788-103">Énumération des volumes</span><span class="sxs-lookup"><span data-stu-id="18788-103">Enumerating Volumes</span></span>

<span data-ttu-id="18788-104">Pour obtenir une liste complète des volumes sur un ordinateur, ou pour manipuler chaque volume, vous pouvez énumérer les volumes.</span><span class="sxs-lookup"><span data-stu-id="18788-104">To make a complete list of the volumes on a computer, or to manipulate each volume in turn, you can enumerate volumes.</span></span> <span data-ttu-id="18788-105">Au sein d’un volume, vous pouvez [Rechercher des dossiers montés](enumerating-volume-mount-points.md) ou d’autres objets sur le volume.</span><span class="sxs-lookup"><span data-stu-id="18788-105">Within a volume, you can [scan for mounted folders](enumerating-volume-mount-points.md) or other objects on the volume.</span></span>

<span data-ttu-id="18788-106">Trois fonctions permettent à une application d’énumérer des volumes sur un ordinateur :</span><span class="sxs-lookup"><span data-stu-id="18788-106">Three functions allow an application to enumerate volumes on a computer:</span></span>

-   [<span data-ttu-id="18788-107">**FindFirstVolume**</span><span class="sxs-lookup"><span data-stu-id="18788-107">**FindFirstVolume**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew)
-   [<span data-ttu-id="18788-108">**FindNextVolume**</span><span class="sxs-lookup"><span data-stu-id="18788-108">**FindNextVolume**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew)
-   [<span data-ttu-id="18788-109">**FindVolumeClose**</span><span class="sxs-lookup"><span data-stu-id="18788-109">**FindVolumeClose**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose)

<span data-ttu-id="18788-110">Ces trois fonctions fonctionnent de manière très similaire aux fonctions [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)et [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) .</span><span class="sxs-lookup"><span data-stu-id="18788-110">These three functions operate in a manner very similar to the [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea), and [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) functions.</span></span>

<span data-ttu-id="18788-111">Commencez une recherche sur les volumes avec [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew).</span><span class="sxs-lookup"><span data-stu-id="18788-111">Begin a search for volumes with [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew).</span></span> <span data-ttu-id="18788-112">Si la recherche est réussie, traitez les résultats en fonction de la conception de votre application.</span><span class="sxs-lookup"><span data-stu-id="18788-112">If the search is successful, process the results according to the design of your application.</span></span> <span data-ttu-id="18788-113">Utilisez ensuite [**FindNextVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew) dans une boucle pour localiser et traiter chaque volume suivant.</span><span class="sxs-lookup"><span data-stu-id="18788-113">Then use [**FindNextVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew) in a loop to locate and process each subsequent volume.</span></span> <span data-ttu-id="18788-114">Lorsque l’alimentation de volumes est épuisée, fermez la recherche avec [**FindVolumeClose**](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose).</span><span class="sxs-lookup"><span data-stu-id="18788-114">When the supply of volumes is exhausted, close the search with [**FindVolumeClose**](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose).</span></span>

<span data-ttu-id="18788-115">Vous ne devez pas supposer une corrélation entre l’ordre des volumes retournés par ces fonctions et l’ordre des volumes retournés par d’autres fonctions ou outils.</span><span class="sxs-lookup"><span data-stu-id="18788-115">You should not assume any correlation between the order of the volumes that are returned by these functions and the order of the volumes that are returned by other functions or tools.</span></span> <span data-ttu-id="18788-116">En particulier, ne supposez pas de corrélation entre l’ordre des volumes et les lettres de lecteur telles qu’elles sont affectées par le BIOS (le cas échéant) ou par l’administrateur de disque.</span><span class="sxs-lookup"><span data-stu-id="18788-116">In particular, do not assume any correlation between volume order and drive letters as assigned by the BIOS (if any) or the Disk Administrator.</span></span>

<span data-ttu-id="18788-117">Pour obtenir un exemple d’énumération des volumes sur un ordinateur, consultez [exemples de dossiers montés](volume-mount-point-examples.md) .</span><span class="sxs-lookup"><span data-stu-id="18788-117">See [Mounted Folder Examples](volume-mount-point-examples.md) for an example of how to enumerate the volumes on a computer.</span></span>

 

 



