---
title: Signes
description: Cette section traite des signes d’insertion qui sont des lignes clignotantes, des blocs ou des bitmaps dans la zone cliente d’une fenêtre.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\carets.htm
keywords:
- ressources, signes
- signes d’insertion, à propos de
- lignes clignotantes
- blocs clignotants
- bitmaps clignotantes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50cb99dfc324aa039924fa26683ab0a7674706ea
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104393827"
---
# <a name="carets"></a><span data-ttu-id="2c5c6-108">Signes</span><span class="sxs-lookup"><span data-stu-id="2c5c6-108">Carets</span></span>

<span data-ttu-id="2c5c6-109">Un *signe insertion* est une ligne, un bloc ou un bitmap clignotant dans la zone cliente d’une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="2c5c6-109">A *caret* is a blinking line, block, or bitmap in the client area of a window.</span></span> <span data-ttu-id="2c5c6-110">Le signe insertion indique généralement l’emplacement où le texte ou les graphiques seront insérés.</span><span class="sxs-lookup"><span data-stu-id="2c5c6-110">The caret typically indicates the place at which text or graphics will be inserted.</span></span>

<span data-ttu-id="2c5c6-111">L’illustration suivante montre certaines variations courantes de l’apparence du signe insertion.</span><span class="sxs-lookup"><span data-stu-id="2c5c6-111">The following illustration shows some common variations in the appearance of the caret.</span></span>

![Affiche 5 différentes façons d’afficher un signe insertion.](images/cscrt-01.png)

<span data-ttu-id="2c5c6-113">Les applications peuvent créer un signe insertion, modifier la durée de clignotement et afficher, masquer ou déplacer le signe insertion.</span><span class="sxs-lookup"><span data-stu-id="2c5c6-113">Applications can create a caret, change its blink time, and display, hide, or relocate the caret.</span></span>

### <a name="in-this-section"></a><span data-ttu-id="2c5c6-114">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="2c5c6-114">In This Section</span></span>



| <span data-ttu-id="2c5c6-115">Nom</span><span class="sxs-lookup"><span data-stu-id="2c5c6-115">Name</span></span>                                   | <span data-ttu-id="2c5c6-116">Description</span><span class="sxs-lookup"><span data-stu-id="2c5c6-116">Description</span></span>                                                               |
|----------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="2c5c6-117">À propos des signes</span><span class="sxs-lookup"><span data-stu-id="2c5c6-117">About Carets</span></span>](about-carets.md)       | <span data-ttu-id="2c5c6-118">Décrit les signes d’insertion.</span><span class="sxs-lookup"><span data-stu-id="2c5c6-118">Discusses carets.</span></span><br/>                                              |
| [<span data-ttu-id="2c5c6-119">Utilisation des signes d’insertion</span><span class="sxs-lookup"><span data-stu-id="2c5c6-119">Using Carets</span></span>](using-carets.md)       | <span data-ttu-id="2c5c6-120">Exemples de code qui montrent comment effectuer des tâches liées aux signes d’insertion.</span><span class="sxs-lookup"><span data-stu-id="2c5c6-120">Code samples that show how to perform tasks related to carets.</span></span><br/> |
| [<span data-ttu-id="2c5c6-121">Référence du signe insertion</span><span class="sxs-lookup"><span data-stu-id="2c5c6-121">Caret Reference</span></span>](caret-reference.md) | <span data-ttu-id="2c5c6-122">Contient la référence de l’API.</span><span class="sxs-lookup"><span data-stu-id="2c5c6-122">Contains the API reference.</span></span><br/>                                    |



 

### <a name="caret-functions"></a><span data-ttu-id="2c5c6-123">Fonctions de signe insertion</span><span class="sxs-lookup"><span data-stu-id="2c5c6-123">Caret Functions</span></span>



| <span data-ttu-id="2c5c6-124">Nom</span><span class="sxs-lookup"><span data-stu-id="2c5c6-124">Name</span></span>                                           | <span data-ttu-id="2c5c6-125">Description</span><span class="sxs-lookup"><span data-stu-id="2c5c6-125">Description</span></span>                                                                                                                                                                                                                                                   |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2c5c6-126">**CreateCaret**</span><span class="sxs-lookup"><span data-stu-id="2c5c6-126">**CreateCaret**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createcaret)             | <span data-ttu-id="2c5c6-127">Crée une nouvelle forme pour le signe insertion système et assigne la propriété du signe insertion à la fenêtre spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2c5c6-127">Creates a new shape for the system caret and assigns ownership of the caret to the specified window.</span></span> <span data-ttu-id="2c5c6-128">La forme du signe insertion peut être une ligne, un bloc ou une image bitmap.</span><span class="sxs-lookup"><span data-stu-id="2c5c6-128">The caret shape can be a line, a block, or a bitmap.</span></span> <br/>                                                                                         |
| [<span data-ttu-id="2c5c6-129">**DestroyCaret**</span><span class="sxs-lookup"><span data-stu-id="2c5c6-129">**DestroyCaret**</span></span>](/windows/desktop/api/Winuser/nf-winuser-destroycaret)           | <span data-ttu-id="2c5c6-130">Détruit la forme actuelle du signe insertion, libère le signe insertion de la fenêtre et supprime le signe insertion de l’écran.</span><span class="sxs-lookup"><span data-stu-id="2c5c6-130">Destroys the caret's current shape, frees the caret from the window, and removes the caret from the screen.</span></span> <br/>                                                                                                                                       |
| [<span data-ttu-id="2c5c6-131">**GetCaretBlinkTime**</span><span class="sxs-lookup"><span data-stu-id="2c5c6-131">**GetCaretBlinkTime**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getcaretblinktime) | <span data-ttu-id="2c5c6-132">Récupère le temps nécessaire pour inverser les pixels du signe insertion.</span><span class="sxs-lookup"><span data-stu-id="2c5c6-132">Retrieves the time required to invert the caret's pixels.</span></span> <span data-ttu-id="2c5c6-133">L’utilisateur peut définir cette valeur.</span><span class="sxs-lookup"><span data-stu-id="2c5c6-133">The user can set this value.</span></span> <br/>                                                                                                                                                            |
| [<span data-ttu-id="2c5c6-134">**GetCaretPos**</span><span class="sxs-lookup"><span data-stu-id="2c5c6-134">**GetCaretPos**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getcaretpos)             | <span data-ttu-id="2c5c6-135">Copie la position du signe insertion vers la structure de [**point**](/previous-versions//dd162805(v=vs.85)) spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2c5c6-135">Copies the caret's position to the specified [**POINT**](/previous-versions//dd162805(v=vs.85)) structure.</span></span> <br/>                                                                                                                                                                    |
| [<span data-ttu-id="2c5c6-136">**HideCaret**</span><span class="sxs-lookup"><span data-stu-id="2c5c6-136">**HideCaret**</span></span>](/windows/desktop/api/Winuser/nf-winuser-hidecaret)                 | <span data-ttu-id="2c5c6-137">Supprime le signe insertion de l’écran.</span><span class="sxs-lookup"><span data-stu-id="2c5c6-137">Removes the caret from the screen.</span></span> <span data-ttu-id="2c5c6-138">Le masquage d’un signe insertion ne détruit pas sa forme actuelle ou n’invalide pas le point d’insertion.</span><span class="sxs-lookup"><span data-stu-id="2c5c6-138">Hiding a caret does not destroy its current shape or invalidate the insertion point.</span></span> <br/>                                                                                                                           |
| [<span data-ttu-id="2c5c6-139">**SetCaretBlinkTime**</span><span class="sxs-lookup"><span data-stu-id="2c5c6-139">**SetCaretBlinkTime**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) | <span data-ttu-id="2c5c6-140">Définit la durée de clignotement du signe insertion sur le nombre de millisecondes spécifié.</span><span class="sxs-lookup"><span data-stu-id="2c5c6-140">Sets the caret blink time to the specified number of milliseconds.</span></span> <span data-ttu-id="2c5c6-141">L’heure de clignotement est le temps écoulé, en millisecondes, nécessaire pour inverser les pixels du signe insertion.</span><span class="sxs-lookup"><span data-stu-id="2c5c6-141">The blink time is the elapsed time, in milliseconds, required to invert the caret's pixels.</span></span> <br/>                                                                                    |
| [<span data-ttu-id="2c5c6-142">**SetCaretPos**</span><span class="sxs-lookup"><span data-stu-id="2c5c6-142">**SetCaretPos**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setcaretpos)             | <span data-ttu-id="2c5c6-143">Déplace le signe insertion vers les coordonnées spécifiées.</span><span class="sxs-lookup"><span data-stu-id="2c5c6-143">Moves the caret to the specified coordinates.</span></span> <span data-ttu-id="2c5c6-144">Si la fenêtre qui possède le signe insertion a été créée avec le style de classe **cs \_ OWNDC** , les coordonnées spécifiées sont soumises au mode de mappage du contexte de périphérique associé à cette fenêtre.</span><span class="sxs-lookup"><span data-stu-id="2c5c6-144">If the window that owns the caret was created with the **CS\_OWNDC** class style, then the specified coordinates are subject to the mapping mode of the device context associated with that window.</span></span> <br/> |
| [<span data-ttu-id="2c5c6-145">**ShowCaret**</span><span class="sxs-lookup"><span data-stu-id="2c5c6-145">**ShowCaret**</span></span>](/windows/desktop/api/Winuser/nf-winuser-showcaret)                 | <span data-ttu-id="2c5c6-146">Rend le signe insertion visible à l’écran à la position actuelle du signe insertion.</span><span class="sxs-lookup"><span data-stu-id="2c5c6-146">Makes the caret visible on the screen at the caret's current position.</span></span> <span data-ttu-id="2c5c6-147">Lorsque le signe insertion devient visible, il commence automatiquement à clignoter.</span><span class="sxs-lookup"><span data-stu-id="2c5c6-147">When the caret becomes visible, it begins flashing automatically.</span></span> <br/>                                                                                                          |



 

 

