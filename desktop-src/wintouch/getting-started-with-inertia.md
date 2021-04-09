---
title: Inertie
description: Cette section décrit l’inertie pour Windows Touch.
ms.assetid: c33dda89-c715-4da0-a7af-aa0010dfd88b
keywords:
- Tactile Windows, inertie
- inertie, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3b69ad31ec4a61f8723c9e52f87883dc4af3772
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028695"
---
# <a name="inertia"></a><span data-ttu-id="40007-105">Inertie</span><span class="sxs-lookup"><span data-stu-id="40007-105">Inertia</span></span>

<span data-ttu-id="40007-106">Cette section décrit l’inertie pour Windows Touch.</span><span class="sxs-lookup"><span data-stu-id="40007-106">This section explains inertia for Windows Touch.</span></span>

<span data-ttu-id="40007-107">L’API d’inertie incluse dans Windows 7 permet un comportement cohérent des objets dans les applications tactiles Windows en fournissant un modèle physique simple.</span><span class="sxs-lookup"><span data-stu-id="40007-107">The inertia API included in Windows 7 enables consistent object behavior in Windows Touch applications by providing a simple physics model.</span></span> <span data-ttu-id="40007-108">L’inertie est activée à l’aide du processeur d’inertie, une classe qui encapsule les fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="40007-108">Inertia is enabled by using the inertia processor, a class that encapsulates functionality.</span></span> <span data-ttu-id="40007-109">Le processeur d’inertie fonctionne en traitant les événements qui lui sont passés lorsque les manipulations d’objets se terminent et en gérant les trajectoires d’objet d’une manière qui est cohérente avec les autres applications.</span><span class="sxs-lookup"><span data-stu-id="40007-109">The inertia processor works by processing events that are passed to it when object manipulations finish and by handling object trajectories in a way that is consistent with other applications.</span></span> <span data-ttu-id="40007-110">Notez que le processeur d’inertie est étroitement couplé au processeur de manipulation pour simplifier l’ajout de la prise en charge de l’inertie aux applications qui utilisent des manipulations.</span><span class="sxs-lookup"><span data-stu-id="40007-110">Note that the inertia processor is tightly coupled to the manipulation processor to simplify adding inertia support to applications that use manipulations.</span></span> <span data-ttu-id="40007-111">En fait, le processeur d’inertie déclenche les mêmes événements que le processeur de manipulation.</span><span class="sxs-lookup"><span data-stu-id="40007-111">In fact, the inertia processor raises the same events that the manipulation processor does.</span></span> <span data-ttu-id="40007-112">La section suivante explique comment prendre en main l’inertie.</span><span class="sxs-lookup"><span data-stu-id="40007-112">The following section explains how to get started with inertia.</span></span>



| <span data-ttu-id="40007-113">Section</span><span class="sxs-lookup"><span data-stu-id="40007-113">Section</span></span>                                                                      | <span data-ttu-id="40007-114">Description</span><span class="sxs-lookup"><span data-stu-id="40007-114">Description</span></span>                                                                                                              |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="40007-115">Mécanismes d’inertie</span><span class="sxs-lookup"><span data-stu-id="40007-115">Inertia Mechanics</span></span>](inertia-mechanics.md)                                   | <span data-ttu-id="40007-116">Explique les principes de base des calculs d’inertie.</span><span class="sxs-lookup"><span data-stu-id="40007-116">Explains the basics of inertia calculations.</span></span>                                                                             |
| [<span data-ttu-id="40007-117">Gestion de l’inertie dans du code non managé</span><span class="sxs-lookup"><span data-stu-id="40007-117">Handling Inertia in Unmanaged Code</span></span>](handling-inertia-in-unmanaged-code.md) | <span data-ttu-id="40007-118">Explique comment utiliser l’interface [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) pour gérer l’inertie dans du code non managé.</span><span class="sxs-lookup"><span data-stu-id="40007-118">Explains how to use the [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) interface for handling inertia in unmanaged code.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="40007-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="40007-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40007-120">Manipulations et inertie</span><span class="sxs-lookup"><span data-stu-id="40007-120">Manipulations and Inertia</span></span>](manipulation-and-inertia.md)
</dt> </dl>

 

 




