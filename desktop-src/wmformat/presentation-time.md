---
title: Heure de présentation
description: Heure de présentation
ms.assetid: 856e1783-85b4-4195-970f-3d7b5612672b
keywords:
- Windows Media Format SDK, durée de présentation
- ASF (Advanced Systems Format), temps de présentation
- ASF (format de systèmes avancés), durées de présentation
- durées de présentation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bc88dbba93d1fc68905a4bfea92328a4ef600eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310894"
---
# <a name="presentation-time"></a><span data-ttu-id="c9c76-107">Heure de présentation</span><span class="sxs-lookup"><span data-stu-id="c9c76-107">Presentation Time</span></span>

<span data-ttu-id="c9c76-108">Une heure de présentation est une mesure du temps à partir du premier exemple du premier flux dans un fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="c9c76-108">A presentation time is a measurement of time from the first sample of the first stream in an ASF file.</span></span> <span data-ttu-id="c9c76-109">Cette mesure, ainsi que la plupart des autres mesures de temps utilisées par les objets de ce kit de développement logiciel (SDK), sont en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="c9c76-109">This measurement, as well as most other measurements of time used by the objects of this SDK, is in 100-nanosecond units.</span></span> <span data-ttu-id="c9c76-110">Les durées de présentation sont importantes car elles permettent aux différents flux d’un fichier d’être synchronisés.</span><span class="sxs-lookup"><span data-stu-id="c9c76-110">Presentation times are important because they enable the various streams in a file to be synchronized.</span></span> <span data-ttu-id="c9c76-111">Vous devez fournir une durée de présentation pour chaque exemple d’entrée que vous transmettez au writer.</span><span class="sxs-lookup"><span data-stu-id="c9c76-111">You must supply a presentation time for each input sample you pass to the writer.</span></span> <span data-ttu-id="c9c76-112">Chaque objet de données de la section de données d’un fichier ASF est associé à une heure de présentation.</span><span class="sxs-lookup"><span data-stu-id="c9c76-112">Every data object in the data section of an ASF file has a presentation time associated with it.</span></span> <span data-ttu-id="c9c76-113">Chaque exemple de sortie récupéré par le lecteur présente également une heure de présentation.</span><span class="sxs-lookup"><span data-stu-id="c9c76-113">Every output sample retrieved by the reader also has a presentation time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c9c76-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c9c76-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9c76-115">**Concepts**</span><span class="sxs-lookup"><span data-stu-id="c9c76-115">**Concepts**</span></span>](concepts.md)
</dt> <dt>

[<span data-ttu-id="c9c76-116">**Entrées, flux et sorties**</span><span class="sxs-lookup"><span data-stu-id="c9c76-116">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> <dt>

[<span data-ttu-id="c9c76-117">**Exemples de supports**</span><span class="sxs-lookup"><span data-stu-id="c9c76-117">**Media Samples**</span></span>](media-samples.md)
</dt> </dl>

 

 




