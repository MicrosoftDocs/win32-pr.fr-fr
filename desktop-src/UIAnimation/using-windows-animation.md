---
title: Tâches d’animation Windows
description: Les rubriques contenues dans cette section décrivent les tâches de base requises pour les applications qui utilisent le gestionnaire d’animations Windows.
ms.assetid: 28103e5e-f00a-4ff5-820b-ece24a7ef21a
keywords:
- Animation Windows Animation Windows, tâches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a2007e53a738494e9b143b3aa8a6cf83290acb1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511032"
---
# <a name="windows-animation-tasks"></a><span data-ttu-id="e2f0e-104">Tâches d’animation Windows</span><span class="sxs-lookup"><span data-stu-id="e2f0e-104">Windows Animation Tasks</span></span>

<span data-ttu-id="e2f0e-105">Les rubriques contenues dans cette section décrivent les tâches de base requises pour les applications qui utilisent le gestionnaire d’animations Windows.</span><span class="sxs-lookup"><span data-stu-id="e2f0e-105">The topics contained in this section describe the basic tasks required of applications that use Windows Animation Manager.</span></span>

<span data-ttu-id="e2f0e-106">Ces tâches, dans l’ordre, sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="e2f0e-106">These tasks, in order, include:</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e2f0e-107">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="e2f0e-107">In this section</span></span>



| <span data-ttu-id="e2f0e-108">Rubrique</span><span class="sxs-lookup"><span data-stu-id="e2f0e-108">Topic</span></span>                                                                                                | <span data-ttu-id="e2f0e-109">Description</span><span class="sxs-lookup"><span data-stu-id="e2f0e-109">Description</span></span>                                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e2f0e-110">Créer les objets d’animation principaux</span><span class="sxs-lookup"><span data-stu-id="e2f0e-110">Create the Main Animation Objects</span></span>](adding-animation-to-an-application.md)<br/>               | <span data-ttu-id="e2f0e-111">Pour utiliser l’animation Windows dans votre application, la première étape consiste à créer un petit ensemble d’objets d’animation principaux.</span><span class="sxs-lookup"><span data-stu-id="e2f0e-111">To use Windows Animation in your application, the first step is to create a small set of main animation objects.</span></span><br/>                                                                                                                                                                           |
| [<span data-ttu-id="e2f0e-112">Créer des variables d’animation</span><span class="sxs-lookup"><span data-stu-id="e2f0e-112">Create Animation Variables</span></span>](create-animation-variables.md)<br/>                              | <span data-ttu-id="e2f0e-113">Une application doit créer une variable d’animation pour chaque caractéristique visuelle qui doit être animée à l’aide de l’animation Windows.</span><span class="sxs-lookup"><span data-stu-id="e2f0e-113">An application must create an animation variable for each visual characteristic that is to be animated using Windows Animation.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="e2f0e-114">Mettre à jour le gestionnaire d’animations et dessiner des frames</span><span class="sxs-lookup"><span data-stu-id="e2f0e-114">Update the Animation Manager and Draw Frames</span></span>](introducing-windows-animation-manager.md)<br/> | <span data-ttu-id="e2f0e-115">Chaque fois qu’une application planifie un Storyboard, l’application doit fournir l’heure actuelle au gestionnaire d’animations.</span><span class="sxs-lookup"><span data-stu-id="e2f0e-115">Each time an application schedules a storyboard, the application must supply the current time to the animation manager.</span></span> <span data-ttu-id="e2f0e-116">L’heure actuelle est également requise pour indiquer au gestionnaire d’animations de mettre à jour son état et de définir toutes les variables d’animation sur les valeurs interpolées appropriées.</span><span class="sxs-lookup"><span data-stu-id="e2f0e-116">The current time is also required when directing the animation manager to update its state and set all animation variables to the appropriate interpolated values.</span></span><br/> |
| [<span data-ttu-id="e2f0e-117">Lire les valeurs de la variable d’animation</span><span class="sxs-lookup"><span data-stu-id="e2f0e-117">Read the Animation Variable Values</span></span>](updating---application-driven-animation.md)<br/>         | <span data-ttu-id="e2f0e-118">Chaque fois que votre application peint, elle doit lire les valeurs actuelles des variables d’animation qui représentent les caractéristiques visuelles à animer.</span><span class="sxs-lookup"><span data-stu-id="e2f0e-118">Each time your application paints, it should read the current values of the animation variables that represent the visual characteristics to be animated.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="e2f0e-119">Créer une table de montage séquentiel et ajouter des transitions</span><span class="sxs-lookup"><span data-stu-id="e2f0e-119">Create a Storyboard and Add Transitions</span></span>](updating---timer-driven-animation.md)<br/>          | <span data-ttu-id="e2f0e-120">Pour créer une animation, une application doit construire une table de montage séquentiel.</span><span class="sxs-lookup"><span data-stu-id="e2f0e-120">To create an animation, an application must construct a storyboard.</span></span><br/>                                                                                                                                                                                                                        |
| [<span data-ttu-id="e2f0e-121">Planifier une table de montage séquentiel</span><span class="sxs-lookup"><span data-stu-id="e2f0e-121">Schedule a Storyboard</span></span>](scheduling-a-storyboard.md)<br/>                                      | <span data-ttu-id="e2f0e-122">Une fois la table de montage séquentiel créée, elle est planifiée par le gestionnaire d’animations.</span><span class="sxs-lookup"><span data-stu-id="e2f0e-122">After a storyboard is created, it is scheduled by the animation manager.</span></span><br/>                                                                                                                                                                                                                   |



 

## <a name="related-topics"></a><span data-ttu-id="e2f0e-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e2f0e-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2f0e-124">Vue d’ensemble des animations Windows</span><span class="sxs-lookup"><span data-stu-id="e2f0e-124">Windows Animation Overview</span></span>](scenic-animation-api-overview.md)
</dt> <dt>

[<span data-ttu-id="e2f0e-125">Informations de référence sur les animations Windows</span><span class="sxs-lookup"><span data-stu-id="e2f0e-125">Windows Animation Reference</span></span>](windows-animation-reference.md)
</dt> <dt>

[<span data-ttu-id="e2f0e-126">Exemples d’animation Windows</span><span class="sxs-lookup"><span data-stu-id="e2f0e-126">Windows Animation Samples</span></span>](windows-animation-samples.md)
</dt> </dl>

 

 





