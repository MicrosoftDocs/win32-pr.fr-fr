---
title: Référence de programmation de l’apparence
description: Référence de programmation de l’apparence
ms.assetid: 914f6045-7252-4a06-a514-d31ef6d2d03b
keywords:
- Lecteur Windows Media, habillages
- Apparences du lecteur Windows Media, informations de référence sur la programmation
- Skins, informations de référence sur la programmation
- référence pour les apparences, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30194f0048f4ef66cf32b7c5f3f94c2bd4e190ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671658"
---
# <a name="skin-programming-reference"></a><span data-ttu-id="daa90-107">Référence de programmation de l’apparence</span><span class="sxs-lookup"><span data-stu-id="daa90-107">Skin Programming Reference</span></span>

<span data-ttu-id="daa90-108">La référence de programmation de l’apparence documente les éléments suivants et leurs attributs, méthodes et événements associés.</span><span class="sxs-lookup"><span data-stu-id="daa90-108">The Skin Programming Reference documents the following elements and their associated attributes, methods, and events.</span></span>

<span data-ttu-id="daa90-109">Les éléments et les attributs de cette section nécessitent le lecteur Windows Media 7,0 ou une version ultérieure, sauf indication contraire.</span><span class="sxs-lookup"><span data-stu-id="daa90-109">The elements and attributes in this section require Windows Media Player 7.0 or later unless otherwise noted.</span></span>



| <span data-ttu-id="daa90-110">Élément</span><span class="sxs-lookup"><span data-stu-id="daa90-110">Element</span></span>                                                  | <span data-ttu-id="daa90-111">Description</span><span class="sxs-lookup"><span data-stu-id="daa90-111">Description</span></span>                                                                         |
|----------------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="daa90-112">Attributs ambiants</span><span class="sxs-lookup"><span data-stu-id="daa90-112">Ambient Attributes</span></span>](ambient-attributes.md)             | <span data-ttu-id="daa90-113">Attributs qui s’appliquent à tous les éléments d’apparence avec des exceptions notées.</span><span class="sxs-lookup"><span data-stu-id="daa90-113">Attributes that apply to all skin elements with exceptions noted.</span></span>                   |
| [<span data-ttu-id="daa90-114">Gestionnaires d’événements ambiants</span><span class="sxs-lookup"><span data-stu-id="daa90-114">Ambient Event Handlers</span></span>](ambient-event-handlers.md)     | <span data-ttu-id="daa90-115">Gestionnaires d’événements qui peuvent être implémentés par la plupart des éléments d’apparence.</span><span class="sxs-lookup"><span data-stu-id="daa90-115">Event handlers that can be implemented by most skin elements.</span></span>                       |
| [<span data-ttu-id="daa90-116">Attributs d’événement ambiant</span><span class="sxs-lookup"><span data-stu-id="daa90-116">Ambient Event Attributes</span></span>](ambient-event-attributes.md) | <span data-ttu-id="daa90-117">Attributs détaillant l’état du lecteur Windows Media lorsqu’un événement est déclenché.</span><span class="sxs-lookup"><span data-stu-id="daa90-117">Attributes detailing the state of Windows Media Player when an event is fired.</span></span>      |
| [<span data-ttu-id="daa90-118">MENU contextuel</span><span class="sxs-lookup"><span data-stu-id="daa90-118">AUTOMENU</span></span>](automenu-element.md)                         | <span data-ttu-id="daa90-119">Offre un moyen d’afficher le panneau d’accès rapide dans une apparence.</span><span class="sxs-lookup"><span data-stu-id="daa90-119">Provides a way to display the Quick Access Panel in a skin.</span></span>                         |
| [<span data-ttu-id="daa90-120">BOUTON</span><span class="sxs-lookup"><span data-stu-id="daa90-120">BUTTON</span></span>](button-element.md)                             | <span data-ttu-id="daa90-121">Bouton autonome.</span><span class="sxs-lookup"><span data-stu-id="daa90-121">A standalone button.</span></span>                                                                |
| [<span data-ttu-id="daa90-122">BUTTONELEMENT</span><span class="sxs-lookup"><span data-stu-id="daa90-122">BUTTONELEMENT</span></span>](buttonelement-element.md)               | <span data-ttu-id="daa90-123">Bouton dans un groupe de boutons.</span><span class="sxs-lookup"><span data-stu-id="daa90-123">A button within a button group.</span></span>                                                     |
| [<span data-ttu-id="daa90-124">BUTTONGROUP</span><span class="sxs-lookup"><span data-stu-id="daa90-124">BUTTONGROUP</span></span>](buttongroup-element.md)                   | <span data-ttu-id="daa90-125">Groupe d’éléments Button.</span><span class="sxs-lookup"><span data-stu-id="daa90-125">A group of button elements.</span></span>                                                         |
| [<span data-ttu-id="daa90-126">COLUMN</span><span class="sxs-lookup"><span data-stu-id="daa90-126">COLUMN</span></span>](column-element.md)                             | <span data-ttu-id="daa90-127">Représente une colonne dans un contrôle playlist.</span><span class="sxs-lookup"><span data-stu-id="daa90-127">Represents a column within a playlist control.</span></span>                                      |
| [<span data-ttu-id="daa90-128">COMMANDES</span><span class="sxs-lookup"><span data-stu-id="daa90-128">CONTROLS</span></span>](controls-element.md)                         | <span data-ttu-id="daa90-129">Fournit l’accès à l’objet [contrôles](controls-object.md) à partir d’une apparence.</span><span class="sxs-lookup"><span data-stu-id="daa90-129">Provides access to the [Controls](controls-object.md) object from within a skin.</span></span>   |
| [<span data-ttu-id="daa90-130">CUSTOMSLIDER</span><span class="sxs-lookup"><span data-stu-id="daa90-130">CUSTOMSLIDER</span></span>](customslider-element.md)                 | <span data-ttu-id="daa90-131">Contrôle Slider personnalisable.</span><span class="sxs-lookup"><span data-stu-id="daa90-131">A customizable slider control.</span></span>                                                      |
| [<span data-ttu-id="daa90-132">EDITBOX</span><span class="sxs-lookup"><span data-stu-id="daa90-132">EDITBOX</span></span>](editbox-element.md)                           | <span data-ttu-id="daa90-133">Permet aux utilisateurs d’entrer du texte dans une apparence.</span><span class="sxs-lookup"><span data-stu-id="daa90-133">Provides a way for users to enter text within a skin.</span></span>                               |
| [<span data-ttu-id="daa90-134">EFFETS</span><span class="sxs-lookup"><span data-stu-id="daa90-134">EFFECTS</span></span>](effects-element.md)                           | <span data-ttu-id="daa90-135">Élément qui contient et contrôle une collection d’effets.</span><span class="sxs-lookup"><span data-stu-id="daa90-135">An element that contains and controls a collection of effects.</span></span>                      |
| [<span data-ttu-id="daa90-136">EQUALIZERSETTINGS</span><span class="sxs-lookup"><span data-stu-id="daa90-136">EQUALIZERSETTINGS</span></span>](equalizersettings-element.md)       | <span data-ttu-id="daa90-137">Élément permettant la manipulation de l’égaliseur graphique.</span><span class="sxs-lookup"><span data-stu-id="daa90-137">An element allowing manipulation of the graphic equalizer.</span></span>                          |
| [<span data-ttu-id="daa90-138">FICHE</span><span class="sxs-lookup"><span data-stu-id="daa90-138">ITEM</span></span>](item-element.md)                                 | <span data-ttu-id="daa90-139">Représente un élément dans une zone de liste ou un contrôle contextuel.</span><span class="sxs-lookup"><span data-stu-id="daa90-139">Represents an item in a list box or pop-up control.</span></span>                                 |
| [<span data-ttu-id="daa90-140">LISTBOX</span><span class="sxs-lookup"><span data-stu-id="daa90-140">LISTBOX</span></span>](listbox-element.md)                           | <span data-ttu-id="daa90-141">Offre aux utilisateurs la possibilité de sélectionner des éléments dans une liste.</span><span class="sxs-lookup"><span data-stu-id="daa90-141">Provides a way for users to select items from a list.</span></span>                               |
| [<span data-ttu-id="daa90-142">LECTEUR</span><span class="sxs-lookup"><span data-stu-id="daa90-142">PLAYER</span></span>](player-element.md)                             | <span data-ttu-id="daa90-143">Fournit l’accès à l’objet [lecteur](player-object.md) à partir d’une apparence.</span><span class="sxs-lookup"><span data-stu-id="daa90-143">Provides access to the [Player](player-object.md) object from within a skin.</span></span>       |
| [<span data-ttu-id="daa90-144">PLAYLIST</span><span class="sxs-lookup"><span data-stu-id="daa90-144">PLAYLIST</span></span>](playlist-element.md)                         | <span data-ttu-id="daa90-145">Élément permettant de contrôler l’apparence d’une sélection dans une apparence.</span><span class="sxs-lookup"><span data-stu-id="daa90-145">An element for controlling the appearance of a playlist within a skin.</span></span>              |
| [<span data-ttu-id="daa90-146">MESSAGES</span><span class="sxs-lookup"><span data-stu-id="daa90-146">POPUP</span></span>](popup-element.md)                               | <span data-ttu-id="daa90-147">Offre aux utilisateurs la possibilité de sélectionner des éléments dans une liste.</span><span class="sxs-lookup"><span data-stu-id="daa90-147">Provides a way for users to select items from a list.</span></span>                               |
| [<span data-ttu-id="daa90-148">PROGRESSBAR</span><span class="sxs-lookup"><span data-stu-id="daa90-148">PROGRESSBAR</span></span>](progressbar-element.md)                   | <span data-ttu-id="daa90-149">Fournit un moyen d’afficher des informations de progression dans un contrôle horizontal ou vertical.</span><span class="sxs-lookup"><span data-stu-id="daa90-149">Provides a way to display progress information in a horizontal or vertical control.</span></span> |
| [<span data-ttu-id="daa90-150">PARAMÈTRES</span><span class="sxs-lookup"><span data-stu-id="daa90-150">SETTINGS</span></span>](settings-element.md)                         | <span data-ttu-id="daa90-151">Fournit l’accès à l’objet de [paramètres](settings-object.md) à partir d’une apparence.</span><span class="sxs-lookup"><span data-stu-id="daa90-151">Provides access to the [Settings](settings-object.md) object from within a skin.</span></span>   |
| [<span data-ttu-id="daa90-152">CURSEUR</span><span class="sxs-lookup"><span data-stu-id="daa90-152">SLIDER</span></span>](slider-element.md)                             | <span data-ttu-id="daa90-153">Contrôle Slider.</span><span class="sxs-lookup"><span data-stu-id="daa90-153">A slider control.</span></span>                                                                   |
| [<span data-ttu-id="daa90-154">SOUS</span><span class="sxs-lookup"><span data-stu-id="daa90-154">SUBVIEW</span></span>](subview-element.md)                           | <span data-ttu-id="daa90-155">Sous-sections d’une vue qui peuvent être déplacées ou masquées.</span><span class="sxs-lookup"><span data-stu-id="daa90-155">Subsections within a view that can be moved or hidden.</span></span>                              |
| [<span data-ttu-id="daa90-156">FINANCIÈRE</span><span class="sxs-lookup"><span data-stu-id="daa90-156">TEXT</span></span>](text-element.md)                                 | <span data-ttu-id="daa90-157">Contrôle contenant du texte.</span><span class="sxs-lookup"><span data-stu-id="daa90-157">A control containing text.</span></span>                                                          |
| [<span data-ttu-id="daa90-158">THÉMATIQUE</span><span class="sxs-lookup"><span data-stu-id="daa90-158">THEME</span></span>](theme-element.md)                               | <span data-ttu-id="daa90-159">Élément principal identifiant un fichier d’apparence.</span><span class="sxs-lookup"><span data-stu-id="daa90-159">The main element identifying a skin file.</span></span>                                           |
| [<span data-ttu-id="daa90-160">VIDÉOSURVEILLANCE</span><span class="sxs-lookup"><span data-stu-id="daa90-160">VIDEO</span></span>](video-element.md)                               | <span data-ttu-id="daa90-161">Élément permettant de spécifier l’apparence d’une fenêtre vidéo.</span><span class="sxs-lookup"><span data-stu-id="daa90-161">An element for specifying the appearance of a video window.</span></span>                         |
| [<span data-ttu-id="daa90-162">VIDEOSETTINGS</span><span class="sxs-lookup"><span data-stu-id="daa90-162">VIDEOSETTINGS</span></span>](videosettings-element.md)               | <span data-ttu-id="daa90-163">Élément autorisant le contrôle de différents paramètres vidéo.</span><span class="sxs-lookup"><span data-stu-id="daa90-163">An element allowing control of various video settings.</span></span>                              |
| [<span data-ttu-id="daa90-164">VIEW</span><span class="sxs-lookup"><span data-stu-id="daa90-164">VIEW</span></span>](view-element.md)                                 | <span data-ttu-id="daa90-165">Spécifie l’aspect de l’interface utilisateur (IU) pour chaque catégorie de média.</span><span class="sxs-lookup"><span data-stu-id="daa90-165">Specifies what the user interface (UI) looks like for each category of media.</span></span>       |
| [<span data-ttu-id="daa90-166">Divers</span><span class="sxs-lookup"><span data-stu-id="daa90-166">Miscellaneous</span></span>](miscellaneous.md)                       | <span data-ttu-id="daa90-167">Attributs spécialisés et autres rubriques diverses à utiliser pour la création d’apparences.</span><span class="sxs-lookup"><span data-stu-id="daa90-167">Specialized attributes and other miscellaneous topics for use in creating skins.</span></span>    |



 

## <a name="related-topics"></a><span data-ttu-id="daa90-168">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="daa90-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="daa90-169">**Apparences du lecteur Windows Media**</span><span class="sxs-lookup"><span data-stu-id="daa90-169">**Windows Media Player Skins**</span></span>](windows-media-player-skins.md)
</dt> </dl>

 

 




