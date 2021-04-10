---
description: ICE71 vérifie que la table des médias contient une entrée dont le depatinage est égal à 1.
ms.assetid: b48c2f3f-24ef-48a8-849f-7abed69c0fc9
title: ICE71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c6e136362caa13da2b6305e3d8c3ca9c3a5c7bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952730"
---
# <a name="ice71"></a><span data-ttu-id="e882b-103">ICE71</span><span class="sxs-lookup"><span data-stu-id="e882b-103">ICE71</span></span>

<span data-ttu-id="e882b-104">ICE71 vérifie que la [table des médias](media-table.md) contient une entrée dont le depatinage est égal à 1.</span><span class="sxs-lookup"><span data-stu-id="e882b-104">ICE71 verifies that the [Media table](media-table.md) contains an entry with DiskId equal to 1.</span></span> <span data-ttu-id="e882b-105">(Windows Installer suppose que le package. msi est sur le disque 1.)</span><span class="sxs-lookup"><span data-stu-id="e882b-105">(Windows Installer assumes that the .msi package is on disk 1.)</span></span>

## <a name="result"></a><span data-ttu-id="e882b-106">Résultats</span><span class="sxs-lookup"><span data-stu-id="e882b-106">Result</span></span>

<span data-ttu-id="e882b-107">ICE71 renvoie une erreur si la table de média ne contient pas d’entrée avec un depatinage égal à 1.</span><span class="sxs-lookup"><span data-stu-id="e882b-107">ICE71 returns an error if the Media table does not contain an entry with DiskId equal to 1.</span></span>

## <a name="example"></a><span data-ttu-id="e882b-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="e882b-108">Example</span></span>

<span data-ttu-id="e882b-109">ICE71 signale l’erreur suivante pour l’exemple indiqué.</span><span class="sxs-lookup"><span data-stu-id="e882b-109">ICE71 reports the following error for the example shown.</span></span>

``` syntax
The Media table requires an entry with DiskId=1. First DiskId is '2'.
```

<span data-ttu-id="e882b-110">T0 corriger cette erreur, modifiez le depatinage de l’entrée où le package est stocké sur 1.</span><span class="sxs-lookup"><span data-stu-id="e882b-110">T0 fix this error, change the DiskId of the entry where the package is stored to 1.</span></span>

<span data-ttu-id="e882b-111">[Table des médias](media-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="e882b-111">[Media Table](media-table.md) (partial)</span></span>



| <span data-ttu-id="e882b-112">DiskId</span><span class="sxs-lookup"><span data-stu-id="e882b-112">DiskId</span></span> |
|--------|
| <span data-ttu-id="e882b-113">2</span><span class="sxs-lookup"><span data-stu-id="e882b-113">2</span></span>      |



 

## <a name="related-topics"></a><span data-ttu-id="e882b-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e882b-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e882b-115">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="e882b-115">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



