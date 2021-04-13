---
title: Macros
description: Les rubriques de cette section fournissent les spécifications de référence pour les messages d’entrée de pointeur et les macros de notifications permettant de récupérer des informations à partir de paramètres de message d’entrée de pointeur.
ms.assetid: 2324DCD0-DAE1-4AC2-AB36-23D114803138
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 07b099a9d0595278e7eb53960da42714763a7f90
ms.sourcegitcommit: f2fe9d9bd65333b74f2af8e30eddbb1643b40c8f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2020
ms.locfileid: "104381388"
---
# <a name="macros"></a><span data-ttu-id="29e27-103">Macros</span><span class="sxs-lookup"><span data-stu-id="29e27-103">Macros</span></span>

<span data-ttu-id="29e27-104">Les rubriques de cette section fournissent les spécifications de référence pour les [messages d’entrée de pointeur et](messages-and-notifications-portal.md) les macros de notifications permettant de récupérer des informations à partir de paramètres de message d’entrée de pointeur.</span><span class="sxs-lookup"><span data-stu-id="29e27-104">The topics in this section provide the reference specifications for [Pointer Input Messages and Notifications](messages-and-notifications-portal.md) macros for retrieving information from pointer input message parameters.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="29e27-105">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="29e27-105">In this section</span></span>



| <span data-ttu-id="29e27-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="29e27-106">Topic</span></span>                                                                                  | <span data-ttu-id="29e27-107">Description</span><span class="sxs-lookup"><span data-stu-id="29e27-107">Description</span></span>                                                                                                                         |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="29e27-108">**GET_POINTERID_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="29e27-108">**GET_POINTERID_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>                      | <span data-ttu-id="29e27-109">Récupère l’ID de pointeur à l’aide de la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="29e27-109">Retrieves the pointer ID using the specified value.</span></span> <br/>                                                                     |
| [<span data-ttu-id="29e27-110">**HAS_POINTER_CONFIDENCE_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="29e27-110">**HAS_POINTER_CONFIDENCE_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>   | <span data-ttu-id="29e27-111">Vérifie si le message de pointeur spécifié est considéré comme intentionnel plutôt que accidentel.</span><span class="sxs-lookup"><span data-stu-id="29e27-111">Checks whether the specified pointer message is considered intentional rather than accidental.</span></span><br/>                           |
| [<span data-ttu-id="29e27-112">**IS_POINTER_CANCELED_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="29e27-112">**IS_POINTER_CANCELED_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>         | <span data-ttu-id="29e27-113">Vérifie si l’entrée de pointeur spécifiée s’est terminée brusquement ou n’est pas valide, ce qui indique que l’interaction n’a pas été effectuée.</span><span class="sxs-lookup"><span data-stu-id="29e27-113">Checks whether the specified pointer input ended abruptly, or was invalid, indicating the interaction was not completed.</span></span><br/> |
| [<span data-ttu-id="29e27-114">**IS_POINTER_FIFTHBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="29e27-114">**IS_POINTER_FIFTHBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>   | <span data-ttu-id="29e27-115">Vérifie si le pointeur spécifié a pris la cinquième mesure.</span><span class="sxs-lookup"><span data-stu-id="29e27-115">Checks whether the specified pointer took fifth action.</span></span> <br/>                                                                 |
| [<span data-ttu-id="29e27-116">**IS_POINTER_FIRSTBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="29e27-116">**IS_POINTER_FIRSTBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>   | <span data-ttu-id="29e27-117">Vérifie si le pointeur spécifié a pris la première action.</span><span class="sxs-lookup"><span data-stu-id="29e27-117">Checks whether the specified pointer took first action.</span></span><br/>                                                                  |
| [<span data-ttu-id="29e27-118">**IS_POINTER_FLAG_SET_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="29e27-118">**IS_POINTER_FLAG_SET_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>        | <span data-ttu-id="29e27-119">Vérifie si une macro pointeur définit l’indicateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="29e27-119">Checks whether a pointer macro sets the specified flag.</span></span> <br/>                                                                 |
| [<span data-ttu-id="29e27-120">**IS_POINTER_FOURTHBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="29e27-120">**IS_POINTER_FOURTHBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/> | <span data-ttu-id="29e27-121">Vérifie si le pointeur spécifié a pris la quatrième action.</span><span class="sxs-lookup"><span data-stu-id="29e27-121">Checks whether the specified pointer took fourth action.</span></span> <br/>                                                                |
| [<span data-ttu-id="29e27-122">**IS_POINTER_INCONTACT_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="29e27-122">**IS_POINTER_INCONTACT_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>       | <span data-ttu-id="29e27-123">Vérifie si le pointeur spécifié est en contact.</span><span class="sxs-lookup"><span data-stu-id="29e27-123">Checks whether the specified pointer is in contact.</span></span> <br/>                                                                     |
| [<span data-ttu-id="29e27-124">**IS_POINTER_INRANGE_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="29e27-124">**IS_POINTER_INRANGE_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>           | <span data-ttu-id="29e27-125">Vérifie si le pointeur spécifié se trouve dans la plage.</span><span class="sxs-lookup"><span data-stu-id="29e27-125">Checks whether the specified pointer is in range.</span></span> <br/>                                                                       |
| [<span data-ttu-id="29e27-126">**IS_POINTER_NEW_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="29e27-126">**IS_POINTER_NEW_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>                   | <span data-ttu-id="29e27-127">Vérifie si le pointeur spécifié est un nouveau pointeur.</span><span class="sxs-lookup"><span data-stu-id="29e27-127">Checks whether the specified pointer is a new pointer.</span></span> <br/>                                                                  |
| [<span data-ttu-id="29e27-128">**IS_POINTER_PRIMARY_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="29e27-128">**IS_POINTER_PRIMARY_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>           | <span data-ttu-id="29e27-129">Vérifie si le pointeur spécifié est le pointeur principal.</span><span class="sxs-lookup"><span data-stu-id="29e27-129">Checks whether the specified pointer is the primary pointer.</span></span> <br/>                                                            |
| [<span data-ttu-id="29e27-130">**IS_POINTER_SECONDBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="29e27-130">**IS_POINTER_SECONDBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/> | <span data-ttu-id="29e27-131">Vérifie si le pointeur spécifié a pris la seconde action.</span><span class="sxs-lookup"><span data-stu-id="29e27-131">Checks whether the specified pointer took second action.</span></span> <br/>                                                                |
| [<span data-ttu-id="29e27-132">**IS_POINTER_THIRDBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="29e27-132">**IS_POINTER_THIRDBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>   | <span data-ttu-id="29e27-133">Vérifie si le pointeur spécifié a pris la troisième action.</span><span class="sxs-lookup"><span data-stu-id="29e27-133">Checks whether the specified pointer took third action.</span></span> <br/>                                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="29e27-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="29e27-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29e27-135">Référence de message d’entrée de pointeur</span><span class="sxs-lookup"><span data-stu-id="29e27-135">Pointer Input Message Reference</span></span>](wmpointer-reference.md)
</dt> </dl>

 

 





