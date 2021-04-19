---
title: Messages d’entrée de pointeur et constantes de notifications
description: Les rubriques de cette section fournissent les spécifications de référence pour les messages d’entrée de pointeur et les constantes de notifications.
ms.assetid: 2224DCD0-DAE1-4AC2-AB36-23D114803138
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 6db54614e10c02cea5dfd4df9b7cf637abb3977c
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106525697"
---
# <a name="pointer-input-messages-and-notifications-constants"></a><span data-ttu-id="8d3ca-103">Messages d’entrée de pointeur et constantes de notifications</span><span class="sxs-lookup"><span data-stu-id="8d3ca-103">Pointer Input Messages and Notifications constants</span></span>

<span data-ttu-id="8d3ca-104">Les rubriques de cette section fournissent les spécifications de référence pour les [messages d’entrée de pointeur et](messages-and-notifications-portal.md) les constantes de notifications.</span><span class="sxs-lookup"><span data-stu-id="8d3ca-104">The topics in this section provide the reference specifications for [Pointer Input Messages and Notifications](messages-and-notifications-portal.md) constants.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8d3ca-105">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="8d3ca-105">In this section</span></span>



| <span data-ttu-id="8d3ca-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="8d3ca-106">Topic</span></span>                                                                             | <span data-ttu-id="8d3ca-107">Description</span><span class="sxs-lookup"><span data-stu-id="8d3ca-107">Description</span></span>                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8d3ca-108">**État de la touche de modification**</span><span class="sxs-lookup"><span data-stu-id="8d3ca-108">**Modifier Key State**</span></span>](modifier-key-states-constants.md)<br/>            | <span data-ttu-id="8d3ca-109">Indique les touches de modification du clavier qui ont été activées lors de la génération de l’entrée.</span><span class="sxs-lookup"><span data-stu-id="8d3ca-109">Indicates which keyboard modifier keys were pressed at the time input was being generated.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="8d3ca-110">**Indicateurs de stylet**</span><span class="sxs-lookup"><span data-stu-id="8d3ca-110">**Pen Flags**</span></span>](pen-flags-constants.md)<br/>                               | <span data-ttu-id="8d3ca-111">Valeurs qui peuvent apparaître dans le champ **penFlags** de la structure [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="8d3ca-111">Values that can appear in the **penFlags** field of the [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) structure.</span></span><br/>                                                                         |
| [<span data-ttu-id="8d3ca-112">**Masque du stylet**</span><span class="sxs-lookup"><span data-stu-id="8d3ca-112">**Pen Mask**</span></span>](pen-mask-constants.md)<br/>                                 | <span data-ttu-id="8d3ca-113">Valeurs qui peuvent apparaître dans le champ **penMask** de la structure [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="8d3ca-113">Values that can appear in the **penMask** field of the [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) structure.</span></span><br/>                                                                          |
| [<span data-ttu-id="8d3ca-114">**Modification de l’appareil pointeur**</span><span class="sxs-lookup"><span data-stu-id="8d3ca-114">**Pointer Device Change**</span></span>](pointer-device-change-constants.md)<br/>       | <span data-ttu-id="8d3ca-115">Valeurs qui peuvent être passées dans le paramètre *wParam* du message [**WM_POINTERDEVICECHANGE**](wm-pointerdevicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="8d3ca-115">Values that can be passed in the *wParam* parameter of the [**WM_POINTERDEVICECHANGE**](wm-pointerdevicechange.md) message.</span></span><br/>                                                                    |
| [<span data-ttu-id="8d3ca-116">**Indicateurs de pointeur**</span><span class="sxs-lookup"><span data-stu-id="8d3ca-116">**Pointer Flags**</span></span>](pointer-flags-contants.md)<br/>                        | <span data-ttu-id="8d3ca-117">Valeurs qui peuvent apparaître dans le champ **pointerFlags** de la structure [**POINTER_INFO**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="8d3ca-117">Values that can appear in the **pointerFlags** field of the [**POINTER_INFO**](/previous-versions/windows/desktop/api) structure.</span></span><br/>                                                                              |
| [<span data-ttu-id="8d3ca-118">**Indicateurs de message de pointeur**</span><span class="sxs-lookup"><span data-stu-id="8d3ca-118">**Pointer Message Flags**</span></span>](pointer-message-flags.md)<br/>                 | <span data-ttu-id="8d3ca-119">Valeurs utilisées dans différentes macros de pointeur (consultez [macros](macros.md)).</span><span class="sxs-lookup"><span data-stu-id="8d3ca-119">Values that are used in various pointer macros (see [Macros](macros.md)).</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="8d3ca-120">**Indicateurs tactiles**</span><span class="sxs-lookup"><span data-stu-id="8d3ca-120">**Touch Flags**</span></span>](touch-flags-constants.md)<br/>                           | <span data-ttu-id="8d3ca-121">Valeurs qui peuvent apparaître dans le champ **touchFlags** de la structure [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="8d3ca-121">Values that can appear in the **touchFlags** field of the [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) structure.</span></span><br/>                                                                   |
| [<span data-ttu-id="8d3ca-122">**Fenêtre test d’atteinte tactile**</span><span class="sxs-lookup"><span data-stu-id="8d3ca-122">**Touch Hit Testing Window**</span></span>](touch-hit-testing-window-constants.md)<br/> | <span data-ttu-id="8d3ca-123">Indique comment les messages pour le test d’atteinte tactile sont traités par les fenêtres qui sont inscrites via la fonction [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) .</span><span class="sxs-lookup"><span data-stu-id="8d3ca-123">Indicates how messages for touch hit testing are processed by windows that are registered through the [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) function.</span></span><br/> |
| [<span data-ttu-id="8d3ca-124">**Masque tactile**</span><span class="sxs-lookup"><span data-stu-id="8d3ca-124">**Touch Mask**</span></span>](touch-mask-constants.md)<br/>                             | <span data-ttu-id="8d3ca-125">Valeurs qui peuvent apparaître dans le champ **touchMask** de la structure [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="8d3ca-125">Values that can appear in the **touchMask** field of the [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) structure.</span></span><br/>                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="8d3ca-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8d3ca-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d3ca-127">Référence de message d’entrée de pointeur</span><span class="sxs-lookup"><span data-stu-id="8d3ca-127">Pointer Input Message Reference</span></span>](wmpointer-reference.md)
</dt> </dl>

 

