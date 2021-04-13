---
title: Structures de contexte d’interaction
description: Les rubriques de cette section fournissent les spécifications de référence pour les structures de contexte d’interaction.
ms.assetid: 38C5CE85-405B-455F-809D-19C77B8A217B
keywords:
- intervention de l'utilisateur
- entrée
- pointeur
- interface tactile
- souris
- stylet
- stylet
ms.topic: article
ms.date: 02/06/2020
ms.openlocfilehash: 975b1342c681d4d154ba31d31348e13063c9fc88
ms.sourcegitcommit: 6b8d5058d02daacad4d2ed7830da63b63a509586
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/07/2020
ms.locfileid: "104381405"
---
# <a name="interaction-context-structures"></a><span data-ttu-id="1ac4b-110">Structures de contexte d’interaction</span><span class="sxs-lookup"><span data-stu-id="1ac4b-110">Interaction Context Structures</span></span>

<span data-ttu-id="1ac4b-111">Les rubriques de cette section fournissent les spécifications de référence pour les structures de [contexte d’interaction](interaction-context-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="1ac4b-111">The topics in this section provide the reference specifications for [Interaction Context](interaction-context-portal.md) structures.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1ac4b-112">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="1ac4b-112">In this section</span></span>

| <span data-ttu-id="1ac4b-113">Rubrique</span><span class="sxs-lookup"><span data-stu-id="1ac4b-113">Topic</span></span> | <span data-ttu-id="1ac4b-114">Description</span><span class="sxs-lookup"><span data-stu-id="1ac4b-114">Description</span></span> |
|---|---|
| [<span data-ttu-id="1ac4b-115">**\_paramètre de diapositives croisées \_**</span><span class="sxs-lookup"><span data-stu-id="1ac4b-115">**CROSS\_SLIDE\_PARAMETER**</span></span>](/windows/win32/api/interactioncontext/ns-interactioncontext-cross_slide_parameter)<br/>                           | <span data-ttu-id="1ac4b-116">Définit le seuil de la diapositive croisée et son seuil de distance.</span><span class="sxs-lookup"><span data-stu-id="1ac4b-116">Defines the cross-slide threshold and its distance threshold.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="1ac4b-117">**\_intersection des arguments d’interaction \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1ac4b-117">**INTERACTION\_ARGUMENTS\_CROSS\_SLIDE**</span></span>](/windows/win32/api/interactioncontext/ns-interactioncontext-interaction_arguments_cross_slide)<br/>  | <span data-ttu-id="1ac4b-118">Définit l’état de l’interaction entre les diapositives.</span><span class="sxs-lookup"><span data-stu-id="1ac4b-118">Defines the state of the cross-slide interaction.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="1ac4b-119">**\_manipulation des arguments d’interaction \_**</span><span class="sxs-lookup"><span data-stu-id="1ac4b-119">**INTERACTION\_ARGUMENTS\_MANIPULATION**</span></span>](/windows/win32/api/interactioncontext/ns-interactioncontext-interaction_arguments_manipulation)<br/> | <span data-ttu-id="1ac4b-120">Définit l’état d’une manipulation.</span><span class="sxs-lookup"><span data-stu-id="1ac4b-120">Defines the state of a manipulation.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="1ac4b-121">**\_robinet des arguments d’interaction \_**</span><span class="sxs-lookup"><span data-stu-id="1ac4b-121">**INTERACTION\_ARGUMENTS\_TAP**</span></span>](/windows/win32/api/interactioncontext/ns-interactioncontext-interaction_arguments_tap)<br/>                   | <span data-ttu-id="1ac4b-122">Définit l’état de l’interaction TAP.</span><span class="sxs-lookup"><span data-stu-id="1ac4b-122">Defines the state of the tap interaction.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="1ac4b-123">**\_configuration du contexte d’interaction \_**</span><span class="sxs-lookup"><span data-stu-id="1ac4b-123">**INTERACTION\_CONTEXT\_CONFIGURATION**</span></span>](/windows/win32/api/interactioncontext/ns-interactioncontext-interaction_context_configuration)<br/>   | <span data-ttu-id="1ac4b-124">Définit la configuration d’un objet de [contexte d’interaction](interaction-context-portal.md) qui active, désactive ou modifie le comportement d’une interaction.</span><span class="sxs-lookup"><span data-stu-id="1ac4b-124">Defines the configuration of an [Interaction Context](interaction-context-portal.md) object that enables, disables, or modifies the behavior of an interaction.</span></span><br/> |
| [<span data-ttu-id="1ac4b-125">**\_sortie du contexte d’interaction \_**</span><span class="sxs-lookup"><span data-stu-id="1ac4b-125">**INTERACTION\_CONTEXT\_OUTPUT**</span></span>](/windows/win32/api/interactioncontext/ns-interactioncontext-interaction_context_output)<br/>                 | <span data-ttu-id="1ac4b-126">Définit la sortie de l’objet de [contexte d’interaction](interaction-context-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="1ac4b-126">Defines the output of the [Interaction Context](interaction-context-portal.md) object.</span></span><br/>                                                                          |
| [<span data-ttu-id="1ac4b-127">**transformation de MANIPULATION \_**</span><span class="sxs-lookup"><span data-stu-id="1ac4b-127">**MANIPULATION\_TRANSFORM**</span></span>](/windows/win32/api/interactioncontext/ns-interactioncontext-manipulation_transform)<br/>                          | <span data-ttu-id="1ac4b-128">Définit les données de transformation pour une manipulation.</span><span class="sxs-lookup"><span data-stu-id="1ac4b-128">Defines the transformation data for a manipulation.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="1ac4b-129">**vélocité de MANIPULATION \_**</span><span class="sxs-lookup"><span data-stu-id="1ac4b-129">**MANIPULATION\_VELOCITY**</span></span>](/windows/win32/api/interactioncontext/ns-interactioncontext-manipulation_velocity)<br/>                            | <span data-ttu-id="1ac4b-130">Définit les données de vélocité d’une manipulation.</span><span class="sxs-lookup"><span data-stu-id="1ac4b-130">Defines the velocity data of a manipulation.</span></span><br/>                                                                                                                     |
## <a name="related-topics"></a><span data-ttu-id="1ac4b-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1ac4b-131">Related topics</span></span>

[<span data-ttu-id="1ac4b-132">Interaction de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="1ac4b-132">User Interaction</span></span>](../user-interaction.md)
