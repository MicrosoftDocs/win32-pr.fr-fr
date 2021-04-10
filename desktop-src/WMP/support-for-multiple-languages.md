---
title: Prise en charge de plusieurs langues
description: Prise en charge de plusieurs langues
ms.assetid: f46efb7f-73d1-4f64-aa44-cb50170a2245
keywords:
- Sélections de métafichiers Windows Media, prise en charge de plusieurs langues
- sélections de métafichiers, prise en charge de plusieurs langues
- sélections, prise en charge de plusieurs langues
- Sélections de métafichiers Windows Media, prise en charge de plusieurs langues
- sélections de métafichiers, prise en charge de plusieurs langues
- sélections, prise en charge de plusieurs langues
- Sélections de métafichiers Windows Media, prise en charge des langues
- sélections de métafichiers, prise en charge des langues
- sélections, prise en charge des langues
- prise en charge de plusieurs langues
- prise en charge multilingue
- prise en charge d'autres langues
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d8855aeb798e4243182a6f82479289ccccbd97d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029691"
---
# <a name="support-for-multiple-languages"></a><span data-ttu-id="1486b-115">Prise en charge de plusieurs langues</span><span class="sxs-lookup"><span data-stu-id="1486b-115">Support for Multiple Languages</span></span>

<span data-ttu-id="1486b-116">Le lecteur Windows Media série 9 ou version ultérieure prend en charge les fichiers Windows Media créés à l’aide du jeu de caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="1486b-116">Windows Media Player 9 Series or later supports Windows Media metafiles created using the Unicode character set.</span></span> <span data-ttu-id="1486b-117">Cela vous permet d’inclure des métadonnées multilingues dans votre sélection de métafichiers.</span><span class="sxs-lookup"><span data-stu-id="1486b-117">This allows you to include multilingual metadata in your metafile playlist.</span></span> <span data-ttu-id="1486b-118">Les règles suivantes régissent l’utilisation des métadonnées multilingues dans les fichiers Windows Media :</span><span class="sxs-lookup"><span data-stu-id="1486b-118">The following rules govern the use of multilingual metadata in Windows Media metafiles:</span></span>

-   <span data-ttu-id="1486b-119">Les caractères doivent être encodés à l’aide du schéma d’encodage UTF-8.</span><span class="sxs-lookup"><span data-stu-id="1486b-119">Characters must be encoded using the UTF-8 encoding scheme.</span></span>
-   <span data-ttu-id="1486b-120">La sélection de métafichier doit inclure le **paramètre** suivant au niveau de la sélection :</span><span class="sxs-lookup"><span data-stu-id="1486b-120">The metafile playlist must include the following **PARAM** at the playlist level:</span></span>
    ```XML
    <PARAM  NAME = "Encoding"  VALUE = "utf-8">
    
    ```

    

-   <span data-ttu-id="1486b-121">Seul le lecteur Windows Media série 9 ou version ultérieure prend en charge cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="1486b-121">Only Windows Media Player 9 Series or later supports this functionality.</span></span>
-   <span data-ttu-id="1486b-122">Si la sélection de métafichiers n’est pas enregistrée avec l’encodage UTF-8 et l’élément **param** correct, elle est analysée à l’aide de la page de codes des paramètres régionaux système par défaut de l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1486b-122">If the metafile playlist is not saved with UTF-8 encoding and the correct **PARAM** element, it will be parsed using the default system locale code page of the user's computer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1486b-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1486b-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1486b-124">**Élément PARAM**</span><span class="sxs-lookup"><span data-stu-id="1486b-124">**PARAM Element**</span></span>](param-element.md)
</dt> <dt>

[<span data-ttu-id="1486b-125">**Présentation des fichiers Windows Media**</span><span class="sxs-lookup"><span data-stu-id="1486b-125">**Windows Media Metafiles Overview**</span></span>](windows-media-metafiles-overview.md)
</dt> </dl>

 

 




