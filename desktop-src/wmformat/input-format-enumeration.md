---
title: Énumération de format d’entrée
description: Énumération de format d’entrée
ms.assetid: 75264598-0226-435a-b71f-6997ff0fcaff
keywords:
- Windows Media Format SDK, énumérations de format d’entrée
- Windows Media Format SDK, énumération des formats d’entrée
- ASF (Advanced Systems Format), énumérations de format d’entrée
- ASF (format des systèmes avancés), énumérations de format d’entrée
- ASF (Advanced Systems Format), énumération des formats d’entrée
- ASF (format avancé des systèmes), énumération des formats d’entrée
- énumérations de format d’entrée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e853aeeac5ca470f1b33b611b287cba8fa025dc0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462434"
---
# <a name="input-format-enumeration"></a><span data-ttu-id="e4850-110">Énumération de format d’entrée</span><span class="sxs-lookup"><span data-stu-id="e4850-110">Input Format Enumeration</span></span>

<span data-ttu-id="e4850-111">L’objet Writer obtient les informations de format de flux à partir du profil que vous lui donnez.</span><span class="sxs-lookup"><span data-stu-id="e4850-111">The writer object gets stream format information from the profile you give it.</span></span> <span data-ttu-id="e4850-112">Les informations de configuration de flux dans un profil donnent à l’enregistreur toutes les informations dont il a besoin sur la façon dont les données doivent être écrites dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="e4850-112">Stream configuration information in a profile gives the writer all of the information it needs about how the data is to be written in the file.</span></span> <span data-ttu-id="e4850-113">Le profil ne fournit à l’enregistreur aucune information sur le format des exemples d’entrée fournis par votre application.</span><span class="sxs-lookup"><span data-stu-id="e4850-113">The profile does not provide the writer with any information about the format of the input samples that your application delivers.</span></span> <span data-ttu-id="e4850-114">Les formats d’entrée sont inconnus uniquement pour les flux compressés avec l’un des codecs Windows Media. les entrées des types de flux arbitraires sont prévisibles en fonction des informations contenues dans le profil.</span><span class="sxs-lookup"><span data-stu-id="e4850-114">Input formats will be unknown only for streams compressed with one of the Windows Media codecs; inputs for arbitrary stream types are predictable based on the information in the profile.</span></span>

<span data-ttu-id="e4850-115">L’objet Writer peut communiquer avec le codec d’un flux pour déterminer les types d’entrée qui peuvent être utilisés.</span><span class="sxs-lookup"><span data-stu-id="e4850-115">The writer object can communicate with the codec for a stream to determine the input types that can be used.</span></span> <span data-ttu-id="e4850-116">Des méthodes sont fournies pour énumérer les types d’entrée possibles.</span><span class="sxs-lookup"><span data-stu-id="e4850-116">Methods are provided to enumerate the possible input types.</span></span> <span data-ttu-id="e4850-117">Vous devez toujours trouver le type d’entrée qui correspond à votre média d’entrée en énumérant les types pris en charge au lieu de définir manuellement les propriétés du média d’entrée.</span><span class="sxs-lookup"><span data-stu-id="e4850-117">You should always find the input type that matches your input media by enumerating the supported types rather than setting the input media properties manually.</span></span> <span data-ttu-id="e4850-118">Pour plus d’informations, consultez [pour énumérer les formats d’entrée](to-enumerate-input-formats.md).</span><span class="sxs-lookup"><span data-stu-id="e4850-118">For more information, see [To Enumerate Input Formats](to-enumerate-input-formats.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e4850-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e4850-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4850-120">**Fonctionnalités d’écriture de fichier**</span><span class="sxs-lookup"><span data-stu-id="e4850-120">**File Writing Features**</span></span>](file-writing-features.md)
</dt> <dt>

[<span data-ttu-id="e4850-121">**Utilisation des entrées**</span><span class="sxs-lookup"><span data-stu-id="e4850-121">**Working with Inputs**</span></span>](working-with-inputs.md)
</dt> </dl>

 

 




