---
title: Conversion de l’espace colorimétrique
description: Conversion de l’espace colorimétrique
ms.assetid: f5f1ec99-b3b9-4420-bf64-3872d9bbe650
keywords:
- Windows Media Format SDK, conversion d’espace colorimétrique
- ASF (Advanced Systems Format), conversion de l’espace colorimétrique
- ASF (format des systèmes avancés), conversion de l’espace colorimétrique
- conversion de l’espace colorimétrique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cbc284995cbc72aee148e12977dad9f4476b29c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196764"
---
# <a name="color-space-conversion"></a><span data-ttu-id="a31b3-107">Conversion de l’espace colorimétrique</span><span class="sxs-lookup"><span data-stu-id="a31b3-107">Color Space Conversion</span></span>

<span data-ttu-id="a31b3-108">Il existe souvent une différence entre la profondeur de couleur du format vidéo compressé dans le profil et le format d’entrée.</span><span class="sxs-lookup"><span data-stu-id="a31b3-108">There is often a difference between the color depth of the compressed video format in the profile and the input format.</span></span> <span data-ttu-id="a31b3-109">Dans ce cas, la vidéo source doit être convertie pour se conformer à l’espace colorimétrique de la destination.</span><span class="sxs-lookup"><span data-stu-id="a31b3-109">When this happens, the source video must be converted to conform to the color space of the destination.</span></span> <span data-ttu-id="a31b3-110">L’enregistreur gère ce processus et communique avec un convertisseur d’espace colorimétrique interne.</span><span class="sxs-lookup"><span data-stu-id="a31b3-110">The writer handles this process, communicating with an internal color-space converter.</span></span>

<span data-ttu-id="a31b3-111">Le lecteur communique également avec le convertisseur d’espace colorimétrique pour rapprocher toute différence entre le format compressé et le format de sortie.</span><span class="sxs-lookup"><span data-stu-id="a31b3-111">The reader also communicates with the color-space converter to reconcile any difference between the compressed format and the output format.</span></span>

<span data-ttu-id="a31b3-112">Comme avec toutes les transformations effectuées sur les données, la conversion entre les profondeurs de couleurs peut réduire la qualité de la sortie.</span><span class="sxs-lookup"><span data-stu-id="a31b3-112">As with all transforms performed on data, converting between color depths can reduce the quality of the output.</span></span> <span data-ttu-id="a31b3-113">Lorsque cela est possible, vous devez utiliser des formats d’entrée et de sortie avec la même profondeur de couleurs que le format compressé.</span><span class="sxs-lookup"><span data-stu-id="a31b3-113">When possible, you should use input and output formats with the same color depth as the compressed format.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a31b3-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a31b3-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a31b3-115">**Fonctionnalités d’écriture de fichier**</span><span class="sxs-lookup"><span data-stu-id="a31b3-115">**File Writing Features**</span></span>](file-writing-features.md)
</dt> <dt>

[<span data-ttu-id="a31b3-116">**Utilisation des entrées**</span><span class="sxs-lookup"><span data-stu-id="a31b3-116">**Working with Inputs**</span></span>](working-with-inputs.md)
</dt> <dt>

[<span data-ttu-id="a31b3-117">**Utilisation des sorties**</span><span class="sxs-lookup"><span data-stu-id="a31b3-117">**Working with Outputs**</span></span>](working-with-outputs.md)
</dt> </dl>

 

 




