---
title: Fonctionnement des propriétés
description: Fonctionnement des propriétés
ms.assetid: 469af852-593c-4b54-8dc3-b76ad460fa77
keywords:
- Plug-ins du lecteur Windows Media, exemples de propriétés Echo
- plug-ins, exemples de propriétés d’écho
- plug-ins de traitement de signal numérique, exemples de propriétés Echo
- Plug-ins DSP, exemples de propriétés Echo
- Echo DSP, exemple de plug-in, propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ad37b71ddc6a097dd43e1ac41147c571f81a67a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673909"
---
# <a name="how-properties-work"></a><span data-ttu-id="5327d-108">Fonctionnement des propriétés</span><span class="sxs-lookup"><span data-stu-id="5327d-108">How Properties Work</span></span>

<span data-ttu-id="5327d-109">Les valeurs de propriété sont stockées dans des variables membres.</span><span class="sxs-lookup"><span data-stu-id="5327d-109">Property values are stored in member variables.</span></span>

<span data-ttu-id="5327d-110">Les propriétés sont rendues accessibles par les paires de méthodes.</span><span class="sxs-lookup"><span data-stu-id="5327d-110">Properties are made accessible by method pairs.</span></span> <span data-ttu-id="5327d-111">Une méthode fournit l’implémentation pour spécifier la valeur de la propriété ; son nom commence par put \_ .</span><span class="sxs-lookup"><span data-stu-id="5327d-111">One method provides the implementation to specify the property value; its name starts with put\_.</span></span> <span data-ttu-id="5327d-112">L’autre méthode fournit l’implémentation pour récupérer la valeur de la propriété ; son nom commence par la fonction obtient \_ .</span><span class="sxs-lookup"><span data-stu-id="5327d-112">The other method provides the implementation to retrieve the property value; its name starts with get\_.</span></span> <span data-ttu-id="5327d-113">La définition de l’interface se trouve dans Echo. idl.</span><span class="sxs-lookup"><span data-stu-id="5327d-113">The interface definition is in Echo.idl.</span></span> <span data-ttu-id="5327d-114">Les prototypes de méthode de propriété se trouvent dans Echo. h.</span><span class="sxs-lookup"><span data-stu-id="5327d-114">The property method prototypes are in Echo.h.</span></span> <span data-ttu-id="5327d-115">Elles sont implémentées dans Echo. cpp.</span><span class="sxs-lookup"><span data-stu-id="5327d-115">They are implemented in Echo.cpp.</span></span>

<span data-ttu-id="5327d-116">Les trois sections suivantes vous montrent comment modifier les méthodes de propriété existantes en fonction de vos besoins et comment ajouter les méthodes pour une propriété supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="5327d-116">The next three sections will show you how to modify the existing property methods to suit your needs and how to add the methods for an additional property.</span></span>

-   [<span data-ttu-id="5327d-117">Variables pour stocker les propriétés</span><span class="sxs-lookup"><span data-stu-id="5327d-117">Variables to Store Properties</span></span>](variables-to-store-properties.md)
-   [<span data-ttu-id="5327d-118">Modification de la propriété Scale</span><span class="sxs-lookup"><span data-stu-id="5327d-118">Modifying the Scale Property</span></span>](modifying-the-scale-property.md)
-   [<span data-ttu-id="5327d-119">Ajout de la propriété de combinaison humide</span><span class="sxs-lookup"><span data-stu-id="5327d-119">Adding the Wet Mix Property</span></span>](adding-the-wet-mix-property.md)

## <a name="related-topics"></a><span data-ttu-id="5327d-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5327d-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5327d-121">**Exemples de propriétés Echo**</span><span class="sxs-lookup"><span data-stu-id="5327d-121">**Echo Sample Properties**</span></span>](echo-sample-properties.md)
</dt> </dl>

 

 




