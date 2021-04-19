---
title: Modification des présélections
description: Modification des présélections
ms.assetid: f8a5565d-676b-4679-a4cb-4bd7551cf41c
keywords:
- visualisations, exemple d’éclat
- visualisations personnalisées, exemple d’éclat
- Guide de programmation, visualisations
- exemples, visualisation lumineuse
- Exemple de visualisation lumineuse
- visualisations, présélections
- visualisations personnalisées, présélections
- présélections dans les visualisations, échantillon lumineux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95d24841c95c3fc1029aa0c405e90b329799fdbe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512044"
---
# <a name="changing-presets"></a><span data-ttu-id="4ac32-111">Modification des présélections</span><span class="sxs-lookup"><span data-stu-id="4ac32-111">Changing Presets</span></span>

<span data-ttu-id="4ac32-112">Les sections de code prédéfinies suivantes ont été modifiées pour autoriser trois présélections :</span><span class="sxs-lookup"><span data-stu-id="4ac32-112">The following preset code sections were changed to allow three presets:</span></span>

## <a name="getpresettitle"></a><span data-ttu-id="4ac32-113">GetPresetTitle</span><span class="sxs-lookup"><span data-stu-id="4ac32-113">GetPresetTitle</span></span>

<span data-ttu-id="4ac32-114">Ce code a été inséré à la place du code prédéfini généré :</span><span class="sxs-lookup"><span data-stu-id="4ac32-114">This code was inserted in place of the generated preset code:</span></span>


```C++
    switch (nPreset)
    {
    case PRESET_RED:
        bstrTemp.LoadString(IDS_REDPRESETNAME); 
        break;

    case PRESET_GREEN:
        bstrTemp.LoadString(IDS_GREENPRESETNAME); 
        break;

    case PRESET_BLUE:
        bstrTemp.LoadString(IDS_BLUEPRESETNAME); 
        break;
    }

```



## <a name="enumerations"></a><span data-ttu-id="4ac32-115">Énumérations</span><span class="sxs-lookup"><span data-stu-id="4ac32-115">Enumerations</span></span>

<span data-ttu-id="4ac32-116">L’énumération suivante dans lueur. h a été modifiée pour autoriser trois présélections :</span><span class="sxs-lookup"><span data-stu-id="4ac32-116">The following enumeration in Glow.h was changed to allow three presets:</span></span>


```C++
enum {
    PRESET_RED = 0,
    PRESET_GREEN,
    PRESET_BLUE,
    PRESET_COUNT
};

```



## <a name="resource-header"></a><span data-ttu-id="4ac32-117">En-tête de ressource</span><span class="sxs-lookup"><span data-stu-id="4ac32-117">Resource Header</span></span>

<span data-ttu-id="4ac32-118">Les ressources suivantes ont été définies dans Resource. h pour autoriser trois présélections :</span><span class="sxs-lookup"><span data-stu-id="4ac32-118">The following resources were defined in Resource.h to allow three presets:</span></span>


```C++
#define IDS_REDPRESETNAME               102
#define IDS_GREENPRESETNAME             103
#define IDS_BLUEPRESETNAME              104

```



<span data-ttu-id="4ac32-119">Notez que vous devez également modifier le numéro de ressource de la **\_ \_ \_ \_ valeur APS Next SYMED** sur 106.</span><span class="sxs-lookup"><span data-stu-id="4ac32-119">Note that you must also change the resource number of **\_APS\_NEXT\_SYMED\_VALUE** to 106.</span></span>

## <a name="resource-file"></a><span data-ttu-id="4ac32-120">Fichier de ressources</span><span class="sxs-lookup"><span data-stu-id="4ac32-120">Resource File</span></span>

<span data-ttu-id="4ac32-121">Les chaînes suivantes doivent être modifiées dans le fichier Glowdll. RC pour autoriser trois présélections et leur donner des noms :</span><span class="sxs-lookup"><span data-stu-id="4ac32-121">The following strings must be changed in the Glowdll.rc file to allow three presets and give them names:</span></span>


```C++
    IDS_REDPRESETNAME       "Glow Red"
    IDS_GREENPRESETNAME     "Glow Green"
    IDS_BLUEPRESETNAME      "Glow Blue"

```



## <a name="related-topics"></a><span data-ttu-id="4ac32-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4ac32-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ac32-123">**L’exemple lueur**</span><span class="sxs-lookup"><span data-stu-id="4ac32-123">**The Glow Sample**</span></span>](the-glow-sample.md)
</dt> </dl>

 

 




