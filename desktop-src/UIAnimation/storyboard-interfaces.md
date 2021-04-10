---
title: Interfaces de Storyboard
description: Cette section contient les spécifications de référence pour les interfaces du gestionnaire d’animations Windows qui prennent en charge les storyboards.
ms.assetid: 372D6348-3DF2-48EB-B495-BAD4E5DAAAD3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fba60c480ef4c316731da6eefbe5334616a72b5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031428"
---
# <a name="storyboard-interfaces"></a><span data-ttu-id="58552-103">Interfaces de Storyboard</span><span class="sxs-lookup"><span data-stu-id="58552-103">Storyboard Interfaces</span></span>

<span data-ttu-id="58552-104">Cette section contient les spécifications de référence pour les interfaces du gestionnaire d’animations Windows qui prennent en charge les storyboards.</span><span class="sxs-lookup"><span data-stu-id="58552-104">This section contains the reference specifications for the Windows Animation Manager interfaces that support storyboards.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="58552-105">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="58552-105">In this section</span></span>



| <span data-ttu-id="58552-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="58552-106">Topic</span></span>                                                                                                 | <span data-ttu-id="58552-107">Description</span><span class="sxs-lookup"><span data-stu-id="58552-107">Description</span></span>                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="58552-108">**IUIAnimationStoryboard**</span><span class="sxs-lookup"><span data-stu-id="58552-108">**IUIAnimationStoryboard**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationstoryboard)<br/>                                   | <span data-ttu-id="58552-109">Définit une table de montage séquentiel, qui contient un groupe de transitions synchronisées les unes par rapport aux autres.</span><span class="sxs-lookup"><span data-stu-id="58552-109">Defines a storyboard, which contains a group of transitions that are synchronized relative to one another.</span></span><br/> |
| [<span data-ttu-id="58552-110">**IUIAnimationStoryboard2**</span><span class="sxs-lookup"><span data-stu-id="58552-110">**IUIAnimationStoryboard2**</span></span>](/windows/win32/api/uianimation/nn-uianimation-iuianimationstoryboard2)<br/>                                 | <span data-ttu-id="58552-111">Définit une table de montage séquentiel, qui contient un groupe de transitions synchronisées les unes par rapport aux autres.</span><span class="sxs-lookup"><span data-stu-id="58552-111">Defines a storyboard, which contains a group of transitions that are synchronized relative to one another.</span></span><br/> |
| [<span data-ttu-id="58552-112">**IUIAnimationStoryboardEventHandler**</span><span class="sxs-lookup"><span data-stu-id="58552-112">**IUIAnimationStoryboardEventHandler**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationstoryboardeventhandler)<br/>           | <span data-ttu-id="58552-113">Définit des méthodes pour gérer l’État et les événements de mise à jour d’une table de montage séquentiel.</span><span class="sxs-lookup"><span data-stu-id="58552-113">Defines methods for handling status and update events for a storyboard.</span></span><br/>                                    |
| [<span data-ttu-id="58552-114">**IUIAnimationStoryboardEventHandler2**</span><span class="sxs-lookup"><span data-stu-id="58552-114">**IUIAnimationStoryboardEventHandler2**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationstoryboardeventhandler2)<br/>         | <span data-ttu-id="58552-115">Définit des méthodes pour gérer les événements de Storyboard.</span><span class="sxs-lookup"><span data-stu-id="58552-115">Defines methods for handling storyboard events.</span></span> <br/>                                                           |
| [<span data-ttu-id="58552-116">**IUIAnimationLoopIterationChangeHandler2**</span><span class="sxs-lookup"><span data-stu-id="58552-116">**IUIAnimationLoopIterationChangeHandler2**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationloopiterationchangehandler2)<br/> | <span data-ttu-id="58552-117">Définit une méthode pour gérer les événements d’itération de la boucle de Storyboard.</span><span class="sxs-lookup"><span data-stu-id="58552-117">Defines a method for handling storyboard loop iteration events.</span></span><br/>                                            |
| [<span data-ttu-id="58552-118">**IUIAnimationPriorityComparison**</span><span class="sxs-lookup"><span data-stu-id="58552-118">**IUIAnimationPriorityComparison**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationprioritycomparison)<br/>                   | <span data-ttu-id="58552-119">Définit une méthode pour la comparaison de priorité que le gestionnaire d’animations utilise pour résoudre les conflits de planification.</span><span class="sxs-lookup"><span data-stu-id="58552-119">Defines a method for priority comparison that the animation manager uses to resolve scheduling conflicts.</span></span><br/>  |
| [<span data-ttu-id="58552-120">**IUIAnimationPriorityComparison2**</span><span class="sxs-lookup"><span data-stu-id="58552-120">**IUIAnimationPriorityComparison2**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationprioritycomparison2)<br/>                 | <span data-ttu-id="58552-121">Définit une méthode qui résout les conflits de planification par comparaison de priorité.</span><span class="sxs-lookup"><span data-stu-id="58552-121">Defines a method that resolves scheduling conflicts through priority comparison.</span></span><br/>                           |



 

## <a name="related-topics"></a><span data-ttu-id="58552-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="58552-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58552-123">Interfaces</span><span class="sxs-lookup"><span data-stu-id="58552-123">Interfaces</span></span>](windows-animation-reference.md)
</dt> </dl>

 

