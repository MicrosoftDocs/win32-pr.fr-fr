---
description: L’objet PenInputPanel vous permet d’ajouter facilement une entrée de stylet sur place à vos applications.
ms.assetid: ad63302e-b386-4b32-95bf-be1129839c33
title: PenInputPanel, classe (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PenInputPanel
- PenInputPanel.IPenInputPanel
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 0564f758d47e516873b8df5020f3f03a5bcb0727
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106539326"
---
# <a name="peninputpanel-class"></a><span data-ttu-id="a0460-103">PenInputPanel, classe</span><span class="sxs-lookup"><span data-stu-id="a0460-103">PenInputPanel class</span></span>

<span data-ttu-id="a0460-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="a0460-104">\[Deprecated.</span></span> <span data-ttu-id="a0460-105">**PenInputPanel** a été remplacé par le [panneau de saisie de texte (TIP)](text-input-panel-reference.md).\]</span><span class="sxs-lookup"><span data-stu-id="a0460-105">**PenInputPanel** has been replaced by the [Text Input Panel (TIP)](text-input-panel-reference.md).\]</span></span>

<span data-ttu-id="a0460-106">L’objet **PenInputPanel** vous permet d’ajouter facilement une entrée de stylet sur place à vos applications.</span><span class="sxs-lookup"><span data-stu-id="a0460-106">The **PenInputPanel** object enables you to easily add in-place pen input to your applications.</span></span>

<span data-ttu-id="a0460-107">L’objet **PenInputPanel** est disponible sous la forme d’un objet pouvant être attaché qui vous permet d’ajouter des fonctionnalités du panneau de saisie Tablet PC à des contrôles existants.</span><span class="sxs-lookup"><span data-stu-id="a0460-107">The **PenInputPanel** object is available as an attachable object that allows you to add Tablet PC Input Panel functionality to existing controls.</span></span> <span data-ttu-id="a0460-108">L’interface utilisateur est en grande partie mandatée par la langue d’entrée actuelle.</span><span class="sxs-lookup"><span data-stu-id="a0460-108">The user interface is largely mandated by the current input language.</span></span> <span data-ttu-id="a0460-109">Vous avez la possibilité de choisir la méthode d’entrée par défaut pour l’objet **PenInputPanel** , à savoir l’écriture manuscrite ou le clavier.</span><span class="sxs-lookup"><span data-stu-id="a0460-109">You have the option of choosing the default input method for the **PenInputPanel** object, either handwriting or keyboard.</span></span> <span data-ttu-id="a0460-110">L’utilisateur final peut basculer entre les méthodes d’entrée à l’aide des boutons de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a0460-110">The end user can switch between input methods using buttons on the user interface.</span></span>

<span data-ttu-id="a0460-111">**PenInputPanel** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a0460-111">**PenInputPanel** has these types of members:</span></span>

-   [<span data-ttu-id="a0460-112">Énumérations</span><span class="sxs-lookup"><span data-stu-id="a0460-112">Enumerations</span></span>](#enumerations)
-   [<span data-ttu-id="a0460-113">Événements</span><span class="sxs-lookup"><span data-stu-id="a0460-113">Events</span></span>](#events)
-   [<span data-ttu-id="a0460-114">Interfaces</span><span class="sxs-lookup"><span data-stu-id="a0460-114">Interfaces</span></span>](#interfaces)
-   [<span data-ttu-id="a0460-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a0460-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="a0460-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a0460-116">Properties</span></span>](#properties)

### <a name="enumerations"></a><span data-ttu-id="a0460-117">Énumérations</span><span class="sxs-lookup"><span data-stu-id="a0460-117">Enumerations</span></span>

<span data-ttu-id="a0460-118">La classe **PenInputPanel** possède ces énumérations.</span><span class="sxs-lookup"><span data-stu-id="a0460-118">The **PenInputPanel** class has these enumerations.</span></span>



| <span data-ttu-id="a0460-119">Énumération</span><span class="sxs-lookup"><span data-stu-id="a0460-119">Enumeration</span></span>                    | <span data-ttu-id="a0460-120">Description</span><span class="sxs-lookup"><span data-stu-id="a0460-120">Description</span></span>                                                                               |
|:-------------------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a0460-121">**PanelType**</span><span class="sxs-lookup"><span data-stu-id="a0460-121">**PanelType**</span></span>](/windows/win32/api/peninputpanel/ne-peninputpanel-paneltype) | <span data-ttu-id="a0460-122">Définit le type d’entrée actuellement disponible dans l’objet **PenInputPanel** .</span><span class="sxs-lookup"><span data-stu-id="a0460-122">Defines the type of input currently available in the **PenInputPanel** object.</span></span><br/> |



 

### <a name="events"></a><span data-ttu-id="a0460-123">Événements</span><span class="sxs-lookup"><span data-stu-id="a0460-123">Events</span></span>

<span data-ttu-id="a0460-124">La classe **PenInputPanel** contient ces événements.</span><span class="sxs-lookup"><span data-stu-id="a0460-124">The **PenInputPanel** class has these events.</span></span>



| <span data-ttu-id="a0460-125">Événement</span><span class="sxs-lookup"><span data-stu-id="a0460-125">Event</span></span>                                                  | <span data-ttu-id="a0460-126">Description</span><span class="sxs-lookup"><span data-stu-id="a0460-126">Description</span></span>                                                                                                                             |
|:-------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a0460-127">**InputFailed**</span><span class="sxs-lookup"><span data-stu-id="a0460-127">**InputFailed**</span></span>](peninputpanel-inputfailed.md)       | <span data-ttu-id="a0460-128">Se produit lorsque le focus d’entrée est modifié avant que l’objet **PenInputPanel** ait pu insérer une entrée d’utilisateur dans le contrôle attaché.</span><span class="sxs-lookup"><span data-stu-id="a0460-128">Occurs when input focus changes before the **PenInputPanel** object was able to insert user input into the attached control.</span></span><br/> |
| [<span data-ttu-id="a0460-129">**PanelChanged**</span><span class="sxs-lookup"><span data-stu-id="a0460-129">**PanelChanged**</span></span>](peninputpanel-panelchanged.md)     | <span data-ttu-id="a0460-130">Se produit lorsque l’objet **PenInputPanel** change entre des dispositions.</span><span class="sxs-lookup"><span data-stu-id="a0460-130">Occurs when the **PenInputPanel** object changes between layouts.</span></span><br/>                                                            |
| [<span data-ttu-id="a0460-131">**PanelMoving**</span><span class="sxs-lookup"><span data-stu-id="a0460-131">**PanelMoving**</span></span>](peninputpanel-panelmoving.md)       | <span data-ttu-id="a0460-132">Se produit lorsque l’objet **PenInputPanel** est déplacé.</span><span class="sxs-lookup"><span data-stu-id="a0460-132">Occurs when the **PenInputPanel** object is moving.</span></span><br/>                                                                          |
| [<span data-ttu-id="a0460-133">**VisibleChanged**</span><span class="sxs-lookup"><span data-stu-id="a0460-133">**VisibleChanged**</span></span>](peninputpanel-visiblechanged.md) | <span data-ttu-id="a0460-134">Se produit lorsque l’objet **PenInputPanel** est affiché ou masqué.</span><span class="sxs-lookup"><span data-stu-id="a0460-134">Occurs when the **PenInputPanel** object has shown or hidden itself.</span></span><br/>                                                         |



 

### <a name="interfaces"></a><span data-ttu-id="a0460-135">Interfaces</span><span class="sxs-lookup"><span data-stu-id="a0460-135">Interfaces</span></span>

<span data-ttu-id="a0460-136">La classe **PenInputPanel** définit ces interfaces.</span><span class="sxs-lookup"><span data-stu-id="a0460-136">The **PenInputPanel** class defines these interfaces.</span></span>



| <span data-ttu-id="a0460-137">Interface</span><span class="sxs-lookup"><span data-stu-id="a0460-137">Interface</span></span>          | <span data-ttu-id="a0460-138">Description</span><span class="sxs-lookup"><span data-stu-id="a0460-138">Description</span></span>                                                             |
|:-------------------|:------------------------------------------------------------------------|
| <span data-ttu-id="a0460-139">**IPenInputPanel**</span><span class="sxs-lookup"><span data-stu-id="a0460-139">**IPenInputPanel**</span></span> | <span data-ttu-id="a0460-140">Cet objet implémente l’interface com **IPenInputPanel** .</span><span class="sxs-lookup"><span data-stu-id="a0460-140">This object implements the **IPenInputPanel** COM interface.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="a0460-141">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a0460-141">Methods</span></span>

<span data-ttu-id="a0460-142">La classe **PenInputPanel** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="a0460-142">The **PenInputPanel** class has these methods.</span></span>



| <span data-ttu-id="a0460-143">Méthode</span><span class="sxs-lookup"><span data-stu-id="a0460-143">Method</span></span>                                                         | <span data-ttu-id="a0460-144">Description</span><span class="sxs-lookup"><span data-stu-id="a0460-144">Description</span></span>                                                                                                                                                                                             |
|:---------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a0460-145">**CommitPendingInput**</span><span class="sxs-lookup"><span data-stu-id="a0460-145">**CommitPendingInput**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-commitpendinginput) | <span data-ttu-id="a0460-146">Envoie l’encre collectée au module de reconnaissance et publie le résultat de la reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="a0460-146">Sends collected ink to the recognizer and posts the recognition result.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="a0460-147">**EnableTsf**</span><span class="sxs-lookup"><span data-stu-id="a0460-147">**EnableTsf**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-enabletsf)                   | <span data-ttu-id="a0460-148">Quand la **valeur true est affectée**, **PenInputPanel** tente d’envoyer du texte au contrôle attaché via Text Services Framework (TSF) et permet d’utiliser l’interface utilisateur de correction.</span><span class="sxs-lookup"><span data-stu-id="a0460-148">When passed **TRUE**, the **PenInputPanel** attempts to send text to the attached control through the Text Services Framework (TSF) and enables the use of the correction user interface.</span></span><br/>    |
| [<span data-ttu-id="a0460-149">**DéplacerVers**</span><span class="sxs-lookup"><span data-stu-id="a0460-149">**MoveTo**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto)                         | <span data-ttu-id="a0460-150">Définit la position de l’objet **PenInputPanel** sur une position d’écran statique.</span><span class="sxs-lookup"><span data-stu-id="a0460-150">Sets the position of the **PenInputPanel** object to a static screen position.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="a0460-151">**Générer**</span><span class="sxs-lookup"><span data-stu-id="a0460-151">**Refresh**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-refresh)                       | <span data-ttu-id="a0460-152">Met à jour et restaure les propriétés **PenInputPanel** en fonction des paramètres du panneau de saisie Tablet PC, positionne automatiquement le panneau de saisie du stylet et définit l’interface utilisateur sur le panneau par défaut.</span><span class="sxs-lookup"><span data-stu-id="a0460-152">Updates and restores the **PenInputPanel** properties based on Tablet PC Input Panel settings, automatically positions the pen input panel and sets the user interface to the default panel.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a0460-153">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a0460-153">Properties</span></span>

<span data-ttu-id="a0460-154">La classe **PenInputPanel** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="a0460-154">The **PenInputPanel** class has these properties.</span></span>



| <span data-ttu-id="a0460-155">Propriété</span><span class="sxs-lookup"><span data-stu-id="a0460-155">Property</span></span>                                                                  | <span data-ttu-id="a0460-156">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="a0460-156">Access type</span></span>           | <span data-ttu-id="a0460-157">Description</span><span class="sxs-lookup"><span data-stu-id="a0460-157">Description</span></span>                                                                                                                                                                    |
|:--------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a0460-158">**AttachedEditWindow**</span><span class="sxs-lookup"><span data-stu-id="a0460-158">**AttachedEditWindow**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_attachededitwindow)<br/> | <span data-ttu-id="a0460-159">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a0460-159">Read/write</span></span><br/> | <span data-ttu-id="a0460-160">Obtient ou définit le handle de fenêtre du contrôle auquel l’objet **PenInputPanel** est attaché.</span><span class="sxs-lookup"><span data-stu-id="a0460-160">Gets or sets the window handle of the control that the **PenInputPanel** object is attached to.</span></span><br/>                                                                     |
| [<span data-ttu-id="a0460-161">**Affichage automatique**</span><span class="sxs-lookup"><span data-stu-id="a0460-161">**AutoShow**</span></span>](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow)<br/>                     | <span data-ttu-id="a0460-162">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a0460-162">Read/write</span></span><br/> | <span data-ttu-id="a0460-163">Obtient ou définit une valeur booléenne qui spécifie si l’objet **PenInputPanel** s’affiche lorsque le focus est défini à l’aide du stylet.</span><span class="sxs-lookup"><span data-stu-id="a0460-163">Gets or sets a Boolean value that specifies whether the **PenInputPanel** object appears when focus is set using the pen.</span></span><br/>                                           |
| [<span data-ttu-id="a0460-164">**Emploie**</span><span class="sxs-lookup"><span data-stu-id="a0460-164">**Busy**</span></span>](/windows/desktop/api/Peninputpanel/nf-peninputpanel-ipeninputpanel-get_busy)<br/>                             | <span data-ttu-id="a0460-165">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a0460-165">Read-only</span></span><br/>  | <span data-ttu-id="a0460-166">Obtient une valeur booléenne qui spécifie si l’objet **PenInputPanel** est en cours de traitement de l’encre.</span><span class="sxs-lookup"><span data-stu-id="a0460-166">Gets a Boolean value that specifies whether the **PenInputPanel** object is currently processing ink.</span></span><br/>                                                               |
| [<span data-ttu-id="a0460-167">**CurrentPanel**</span><span class="sxs-lookup"><span data-stu-id="a0460-167">**CurrentPanel**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_currentpanel)<br/>             | <span data-ttu-id="a0460-168">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a0460-168">Read/write</span></span><br/> | <span data-ttu-id="a0460-169">Obtient ou définit le type de panneau actuellement utilisé pour l’entrée dans l’objet **PenInputPanel** .</span><span class="sxs-lookup"><span data-stu-id="a0460-169">Gets or sets which panel type is currently being used for input within the **PenInputPanel** object.</span></span><br/>                                                                |
| [<span data-ttu-id="a0460-170">**DefaultPanel**</span><span class="sxs-lookup"><span data-stu-id="a0460-170">**DefaultPanel**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_defaultpanel)<br/>             | <span data-ttu-id="a0460-171">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a0460-171">Read/write</span></span><br/> | <span data-ttu-id="a0460-172">Obtient ou définit le type de panneau par défaut utilisé pour l’entrée dans l’objet **PenInputPanel** .</span><span class="sxs-lookup"><span data-stu-id="a0460-172">Gets or sets which panel type is the default panel type used for input within the **PenInputPanel** object.</span></span><br/>                                                         |
| [<span data-ttu-id="a0460-173">**Factoid**</span><span class="sxs-lookup"><span data-stu-id="a0460-173">**Factoid**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_factoid)<br/>                       | <span data-ttu-id="a0460-174">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a0460-174">Read/write</span></span><br/> | <span data-ttu-id="a0460-175">Obtient ou définit le nom de chaîne du Factoid utilisé dans la reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="a0460-175">Gets or sets the string name of the factoid used in recognition.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="a0460-176">**Height**</span><span class="sxs-lookup"><span data-stu-id="a0460-176">**Height**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_height)<br/>                         | <span data-ttu-id="a0460-177">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a0460-177">Read-only</span></span><br/>  | <span data-ttu-id="a0460-178">Obtient la hauteur de l’objet **PenInputPanel** dans les coordonnées clientes.</span><span class="sxs-lookup"><span data-stu-id="a0460-178">Gets the height of the **PenInputPanel** object in client coordinates.</span></span><br/>                                                                                              |
| [<span data-ttu-id="a0460-179">**HorizontalOffset**</span><span class="sxs-lookup"><span data-stu-id="a0460-179">**HorizontalOffset**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_horizontaloffset)<br/>     | <span data-ttu-id="a0460-180">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a0460-180">Read/write</span></span><br/> | <span data-ttu-id="a0460-181">Obtient ou définit le décalage entre le bord gauche de l’objet **PenInputPanel** et le bord gauche du contrôle auquel il est attaché.</span><span class="sxs-lookup"><span data-stu-id="a0460-181">Gets or sets the offset between the left edge of the **PenInputPanel** object and the left edge of the control to which it is attached.</span></span><br/>                             |
| [<span data-ttu-id="a0460-182">**Gauche**</span><span class="sxs-lookup"><span data-stu-id="a0460-182">**Left**</span></span>](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_left)<br/>                             | <span data-ttu-id="a0460-183">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a0460-183">Read-only</span></span><br/>  | <span data-ttu-id="a0460-184">Obtient l’emplacement horizontal (ou axe des x) du bord gauche de l’objet **PenInputPanel** , en coordonnées d’écran.</span><span class="sxs-lookup"><span data-stu-id="a0460-184">Gets the horizontal, or x-axis, location of the left edge of the **PenInputPanel** object, in screen coordinates.</span></span><br/>                                                   |
| [<span data-ttu-id="a0460-185">**Retour au début**</span><span class="sxs-lookup"><span data-stu-id="a0460-185">**Top**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_top)<br/>                               | <span data-ttu-id="a0460-186">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a0460-186">Read-only</span></span><br/>  | <span data-ttu-id="a0460-187">Obtient l’emplacement vertical, ou axe y, de l’emplacement du bord supérieur de l’objet **PenInputPanel** , en coordonnées d’écran.</span><span class="sxs-lookup"><span data-stu-id="a0460-187">Gets the vertical, or y-axis, location of the top edge of the **PenInputPanel** object, in screen coordinates.</span></span><br/>                                                      |
| [<span data-ttu-id="a0460-188">**VerticalOffset**</span><span class="sxs-lookup"><span data-stu-id="a0460-188">**VerticalOffset**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_verticaloffset)<br/>         | <span data-ttu-id="a0460-189">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a0460-189">Read/write</span></span><br/> | <span data-ttu-id="a0460-190">Obtient ou définit le décalage entre le bord horizontal le plus proche de l’objet **PenInputPanel** et le bord horizontal le plus proche du contrôle auquel il est attaché.</span><span class="sxs-lookup"><span data-stu-id="a0460-190">Gets or sets the offset between the closest horizontal edge of the **PenInputPanel** object and the closest horizontal edge of the control to which it is attached.</span></span><br/> |
| [<span data-ttu-id="a0460-191">**Parent**</span><span class="sxs-lookup"><span data-stu-id="a0460-191">**Visible**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_visible)<br/>                       | <span data-ttu-id="a0460-192">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a0460-192">Read/write</span></span><br/> | <span data-ttu-id="a0460-193">Obtient ou définit une valeur qui indique si l’objet **PenInputPanel** est visible.</span><span class="sxs-lookup"><span data-stu-id="a0460-193">Gets or sets a value that indicates whether the **PenInputPanel** object is visible.</span></span><br/>                                                                                |
| [<span data-ttu-id="a0460-194">**Width**</span><span class="sxs-lookup"><span data-stu-id="a0460-194">**Width**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_width)<br/>                           | <span data-ttu-id="a0460-195">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a0460-195">Read-only</span></span><br/>  | <span data-ttu-id="a0460-196">Obtient la largeur de l’objet **PenInputPanel** dans les coordonnées clientes.</span><span class="sxs-lookup"><span data-stu-id="a0460-196">Gets the width of the **PenInputPanel** object in client coordinates.</span></span><br/>                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="a0460-197">Notes</span><span class="sxs-lookup"><span data-stu-id="a0460-197">Remarks</span></span>

<span data-ttu-id="a0460-198">Cet objet peut être instancié en appelant la méthode [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.</span><span class="sxs-lookup"><span data-stu-id="a0460-198">This object can be instantiated by calling the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0460-199">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a0460-199">Requirements</span></span>



| <span data-ttu-id="a0460-200">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a0460-200">Requirement</span></span> | <span data-ttu-id="a0460-201">Valeur</span><span class="sxs-lookup"><span data-stu-id="a0460-201">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0460-202">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a0460-202">Minimum supported client</span></span><br/> | <span data-ttu-id="a0460-203">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a0460-203">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="a0460-204">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a0460-204">Minimum supported server</span></span><br/> | <span data-ttu-id="a0460-205">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a0460-205">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="a0460-206">En-tête</span><span class="sxs-lookup"><span data-stu-id="a0460-206">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0460-207"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a0460-207"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a0460-208">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a0460-208">Library</span></span><br/>                  | <dl> <span data-ttu-id="a0460-209"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0460-209"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="a0460-210">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a0460-210">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0460-211">Programmation du panneau de saisie à l’aide de la classe PenInputPanel</span><span class="sxs-lookup"><span data-stu-id="a0460-211">Programming the Input Panel Using the PenInputPanel Class</span></span>](programming-the-input-panel-using-the-peninputpanel-class.md)
</dt> </dl>

 

 
