---
title: À propos du modèle objet Player
description: À propos du modèle objet Player
ms.assetid: 41a9cbce-b982-4377-a0ee-b0ca735954f5
keywords:
- Lecteur Windows Media, modèle objet
- Windows Media Player Object Model, à propos de
- modèle objet, à propos de
- Contrôle ActiveX du lecteur Windows Media, modèle objet
- Contrôle ActiveX, modèle objet
- Windows Media Player Mobile contrôle ActiveX, modèle objet
- Windows Media Player Mobile, modèle objet
- Kit de développement logiciel (SDK), modèle objet de contrôle ActiveX du lecteur Windows Media
- SDK (kit de développement logiciel), modèle objet de contrôle ActiveX du lecteur Windows Media
- documentation, modèle objet de contrôle ActiveX du lecteur Windows Media
- Objet Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06a0ded1f25d8d08bd9e588b5384a171698d2ea2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512255"
---
# <a name="about-the-player-object-model"></a><span data-ttu-id="22d31-114">À propos du modèle objet Player</span><span class="sxs-lookup"><span data-stu-id="22d31-114">About the Player Object Model</span></span>

<span data-ttu-id="22d31-115">Le contrôle de lecteur Microsoft Windows Media est un contrôle ActiveX standard qui utilise la technologie COM (Component Object Model) Microsoft.</span><span class="sxs-lookup"><span data-stu-id="22d31-115">The Microsoft Windows Media Player control is a standard ActiveX control that uses Microsoft Component Object Model (COM) technology.</span></span> <span data-ttu-id="22d31-116">La fonctionnalité du lecteur Windows Media est divisée en un ensemble d’interfaces de programmation qui suit les directives COM standard.</span><span class="sxs-lookup"><span data-stu-id="22d31-116">The Windows Media Player functionality is distilled into a set of programming interfaces that follows standard COM guidelines.</span></span> <span data-ttu-id="22d31-117">Vous pouvez programmer ces interfaces sur une page Web HTML standard à l’aide du modèle objet de contrôle du lecteur avec Microsoft JScript ou Microsoft Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="22d31-117">You can program these interfaces on a standard HTML webpage using the Player control object model with Microsoft JScript or Microsoft Visual Basic Scripting Edition (VBScript).</span></span> <span data-ttu-id="22d31-118">Vous pouvez également les programmer dans des habillages à l’aide de Microsoft JScript.</span><span class="sxs-lookup"><span data-stu-id="22d31-118">You can also program them in skins by using Microsoft JScript.</span></span> <span data-ttu-id="22d31-119">Si vous souhaitez créer un programme personnalisé qui incorpore le contrôle, vous pouvez utiliser l’un des langages suivants, notamment Visual Basic, C++ et C#.</span><span class="sxs-lookup"><span data-stu-id="22d31-119">If you want to create a custom program that embeds the control, you can use one of several languages, including Visual Basic, C++, and C#.</span></span>

<span data-ttu-id="22d31-120">Le contrôle Windows Media Player ActiveX est installé avec le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="22d31-120">The Windows Media Player ActiveX control is installed with Windows Media Player.</span></span> <span data-ttu-id="22d31-121">Le contrôle du lecteur n’est pas installé avec le kit de développement logiciel (SDK) du lecteur Windows Media et ne peut pas être redistribué séparément.</span><span class="sxs-lookup"><span data-stu-id="22d31-121">The Player control is not installed with the Windows Media Player SDK and cannot be redistributed separately.</span></span> <span data-ttu-id="22d31-122">Les fonctionnalités spécifiques disponibles pour votre code dépendent de la version du lecteur Windows Media que l’utilisateur a installée.</span><span class="sxs-lookup"><span data-stu-id="22d31-122">The particular features available to your code depend on which version of Windows Media Player the user has installed.</span></span> <span data-ttu-id="22d31-123">La [Référence du modèle objet pour les scripts](object-model-reference-for-scripting.md) et la [Référence du modèle objet pour C++](object-model-reference-for-c.md) inclut des informations sur la spécification de la version pour chaque propriété, méthode et événement.</span><span class="sxs-lookup"><span data-stu-id="22d31-123">The [Object Model Reference for Scripting](object-model-reference-for-scripting.md) and [Object Model Reference for C++](object-model-reference-for-c.md) include version requirement information for each property, method, and event.</span></span>

<span data-ttu-id="22d31-124">Les sections suivantes fournissent des informations générales sur le modèle objet du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="22d31-124">The following sections provide overview information about the Windows Media Player object model.</span></span>



| <span data-ttu-id="22d31-125">Section</span><span class="sxs-lookup"><span data-stu-id="22d31-125">Section</span></span>                                                                                        | <span data-ttu-id="22d31-126">Description</span><span class="sxs-lookup"><span data-stu-id="22d31-126">Description</span></span>                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="22d31-127">Modèle objet de lecteur pour les langages de script</span><span class="sxs-lookup"><span data-stu-id="22d31-127">Player Object Model for Scripting Languages</span></span>](player-object-model-for-scripting-languages.md) | <span data-ttu-id="22d31-128">Cette section décrit les objets disponibles dans le modèle objet.</span><span class="sxs-lookup"><span data-stu-id="22d31-128">This section describes the objects available in the object model.</span></span>                                                                                             |
| [<span data-ttu-id="22d31-129">À propos des versions de modèle objet</span><span class="sxs-lookup"><span data-stu-id="22d31-129">About the Object Model Versions</span></span>](about-the-object-model-versions.md)                         | <span data-ttu-id="22d31-130">Cette section détaille les éléments de modèle objet qui ont été ajoutés à chaque version depuis l’introduction du lecteur Windows Media 7,0.</span><span class="sxs-lookup"><span data-stu-id="22d31-130">This section details which object model items have been added in each version since the introduction of Windows Media Player 7.0.</span></span>                             |
| [<span data-ttu-id="22d31-131">Propriétés, méthodes et événements</span><span class="sxs-lookup"><span data-stu-id="22d31-131">Properties, Methods, and Events</span></span>](properties--methods-and-events.md)                          | <span data-ttu-id="22d31-132">Cette section décrit les propriétés, les méthodes et les événements.</span><span class="sxs-lookup"><span data-stu-id="22d31-132">This section explains properties, methods, and events.</span></span>                                                                                                        |
| [<span data-ttu-id="22d31-133">Protocoles et types de fichiers pris en charge</span><span class="sxs-lookup"><span data-stu-id="22d31-133">Supported Protocols and File Types</span></span>](supported-protocols-and-file-types.md)                   | <span data-ttu-id="22d31-134">Cette section répertorie les protocoles et types de fichiers pris en charge par le lecteur Windows Media et le modèle objet de contrôle du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="22d31-134">This section lists the protocols and file types supported by Windows Media Player and the Windows Media Player control object model.</span></span>                          |
| [<span data-ttu-id="22d31-135">À propos de la bibliothèque</span><span class="sxs-lookup"><span data-stu-id="22d31-135">About the Library</span></span>](about-the-library.md)                                                     | <span data-ttu-id="22d31-136">Cette section décrit la bibliothèque du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="22d31-136">This section describes the Windows Media Player library.</span></span>                                                                                                      |
| [<span data-ttu-id="22d31-137">Utilisation du HTML avec le lecteur Windows Media</span><span class="sxs-lookup"><span data-stu-id="22d31-137">Using HTML with Windows Media Player</span></span>](using-html-with-windows-media-player.md)               | <span data-ttu-id="22d31-138">Cette section décrit les différentes façons de faire fonctionner ensemble le lecteur Windows Media et le code HTML.</span><span class="sxs-lookup"><span data-stu-id="22d31-138">This section describes the various ways to make Windows Media Player and HTML work together.</span></span>                                                                  |
| [<span data-ttu-id="22d31-139">Incorporation du contrôle du lecteur Windows Media</span><span class="sxs-lookup"><span data-stu-id="22d31-139">Embedding the Windows Media Player Control</span></span>](embedding-the-windows-media-player-control.md)   | <span data-ttu-id="22d31-140">Cette section décrit les différentes façons d’incorporer le contrôle du lecteur Windows Media dans Microsoft Office documents et dans des programmes personnalisés.</span><span class="sxs-lookup"><span data-stu-id="22d31-140">This section describes the various ways to embed the Windows Media Player control in Microsoft Office documents and in custom programs.</span></span>                       |
| [<span data-ttu-id="22d31-141">À propos de la synchronisation des appareils</span><span class="sxs-lookup"><span data-stu-id="22d31-141">About Device Synchronization</span></span>](about-device-synchronization.md)                               | <span data-ttu-id="22d31-142">Cette section décrit les fonctionnalités fournies par le contrôle du lecteur Windows Media 10 ou ultérieur pour le transfert de contenu multimédia numérique vers des appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="22d31-142">This section describes the functionality provided by the Windows Media Player 10 or later control for transferring digital media content to portable devices.</span></span> |
| [<span data-ttu-id="22d31-143">À propos de la gravure de CD</span><span class="sxs-lookup"><span data-stu-id="22d31-143">About CD Burning</span></span>](about-cd-burning.md)                                                       | <span data-ttu-id="22d31-144">Cette section décrit les fonctionnalités fournies par le contrôle du lecteur Windows Media pour la création de CD.</span><span class="sxs-lookup"><span data-stu-id="22d31-144">This section describes the functionality provided by the Windows Media Player control for creating CDs.</span></span>                                                       |
| [<span data-ttu-id="22d31-145">À propos de l’extraction de CD</span><span class="sxs-lookup"><span data-stu-id="22d31-145">About CD Ripping</span></span>](about-cd-ripping.md)                                                       | <span data-ttu-id="22d31-146">Cette section décrit les fonctionnalités fournies par le contrôle du lecteur Windows Media pour copier des pistes de CD audio sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="22d31-146">This section describes the functionality provided by the Windows Media Player control for copying tracks from audio CDs to the user's computer.</span></span>               |
| [<span data-ttu-id="22d31-147">À propos de la surveillance des dossiers</span><span class="sxs-lookup"><span data-stu-id="22d31-147">About Folder Monitoring</span></span>](about-folder-monitoring.md)                                         | <span data-ttu-id="22d31-148">Cette section décrit les fonctionnalités fournies par le contrôle du lecteur Windows Media pour le contrôle des processus de surveillance des dossiers du lecteur.</span><span class="sxs-lookup"><span data-stu-id="22d31-148">This section describes the functionality provided by the Windows Media Player control for controlling the Player's folder monitoring processes.</span></span>               |



 

## <a name="related-topics"></a><span data-ttu-id="22d31-149">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="22d31-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22d31-150">**Modèle objet du lecteur Windows Media**</span><span class="sxs-lookup"><span data-stu-id="22d31-150">**Windows Media Player Object Model**</span></span>](windows-media-player-object-model.md)
</dt> </dl>

 

 




