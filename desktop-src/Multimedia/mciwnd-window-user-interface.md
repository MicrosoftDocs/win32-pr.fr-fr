---
title: Interface utilisateur de la fenêtre MCIWnd
description: Interface utilisateur de la fenêtre MCIWnd
ms.assetid: 422c5acb-bce5-4be2-96ba-5ab7f9dcc826
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c98c0b11b6868828625c6c6e605f005fe842d669
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028826"
---
# <a name="mciwnd-window-user-interface"></a><span data-ttu-id="6683f-103">Interface utilisateur de la fenêtre MCIWnd</span><span class="sxs-lookup"><span data-stu-id="6683f-103">MCIWnd Window User Interface</span></span>

<span data-ttu-id="6683f-104">MCIWnd fournit des fonctionnalités supplémentaires pour ajuster l’apparence de la fenêtre MCIWnd, personnaliser le comportement de votre application et optimiser les performances de lecture.</span><span class="sxs-lookup"><span data-stu-id="6683f-104">MCIWnd provides additional features to adjust the look of the MCIWnd window, customize the behavior of your application, and tune playback performance.</span></span> <span data-ttu-id="6683f-105">Les fonctionnalités suivantes sont incluses dans la fenêtre MCIWnd :</span><span class="sxs-lookup"><span data-stu-id="6683f-105">The following features are included in the MCIWnd window:</span></span>

-   <span data-ttu-id="6683f-106">Une barre d’outils avec des boutons **lire**, **arrêter**, **Enregistrer** et **menu**</span><span class="sxs-lookup"><span data-stu-id="6683f-106">A toolbar with **Play**, **Stop**, **Record** and **Menu** buttons</span></span>
-   <span data-ttu-id="6683f-107">TrackBar qui contrôle le positionnement dans le contenu de lecture</span><span class="sxs-lookup"><span data-stu-id="6683f-107">A trackbar that controls positioning within the playback content</span></span>
-   <span data-ttu-id="6683f-108">Menu contextuel contenant des commandes courantes</span><span class="sxs-lookup"><span data-stu-id="6683f-108">A pop-up menu containing common commands</span></span>
-   <span data-ttu-id="6683f-109">Zone de lecture pour les vidéos et autres périphériques qui affichent des images</span><span class="sxs-lookup"><span data-stu-id="6683f-109">A playback area for video and other devices that display images</span></span>

<span data-ttu-id="6683f-110">L’illustration suivante montre l’état initial de la lecture vidéo contrôlée par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6683f-110">The following illustration shows the initial state of user-controlled video playback.</span></span> <span data-ttu-id="6683f-111">L’exemple de fichier utilisé est CLOCK.AVI.</span><span class="sxs-lookup"><span data-stu-id="6683f-111">The sample file used is CLOCK.AVI.</span></span>

![Image clock.avi](images/mciwnd1.gif)

<span data-ttu-id="6683f-113">La fenêtre MCIWnd comprend une zone de lecture pour les vidéos et autres périphériques qui affichent des images pendant la lecture.</span><span class="sxs-lookup"><span data-stu-id="6683f-113">The MCIWnd window includes a playback area for video and other devices that display images during playback.</span></span> <span data-ttu-id="6683f-114">MCIWnd omet la zone de lecture des appareils Wave-audio, des séquenceurs MIDI et des autres périphériques qui n’écrivent pas dans l’affichage.</span><span class="sxs-lookup"><span data-stu-id="6683f-114">MCIWnd omits the playback area from waveform-audio devices, MIDI sequencers, and other devices that do not write to the display.</span></span> <span data-ttu-id="6683f-115">L’illustration suivante montre la zone de lecture de la forme d’onde audio.</span><span class="sxs-lookup"><span data-stu-id="6683f-115">The following illustration shows the waveform-audio playback area.</span></span>

![image fenêtre MCIWnd](images/mciwnd4.gif)

<span data-ttu-id="6683f-117">Le bouton **lecture** se trouve dans le coin inférieur gauche de la fenêtre MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="6683f-117">The **Play** button is located in the lower-left corner of the MCIWnd window.</span></span> <span data-ttu-id="6683f-118">Il apparaît lorsque le contenu est arrêté.</span><span class="sxs-lookup"><span data-stu-id="6683f-118">It appears when the content is stopped.</span></span> <span data-ttu-id="6683f-119">L’utilisateur peut lire le contenu des manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="6683f-119">The user can play the content in the following ways:</span></span>

-   <span data-ttu-id="6683f-120">Pour lire le contenu à partir de la position de lecture actuelle, sélectionnez le bouton **lecture** .</span><span class="sxs-lookup"><span data-stu-id="6683f-120">To play the content from the current playback position, select the **Play** button.</span></span>
-   <span data-ttu-id="6683f-121">Pour lire le contenu en plein écran à partir de la position de lecture actuelle, sélectionnez le bouton **lecture** tout en maintenant la touche CTRL enfoncée.</span><span class="sxs-lookup"><span data-stu-id="6683f-121">To play the content full-screen from the current playback position, select the **Play** button while holding down the CTRL key.</span></span>
-   <span data-ttu-id="6683f-122">Pour lire le contenu en arrière à partir de la position de lecture actuelle, sélectionnez le bouton **lecture** tout en maintenant la touche Maj enfoncée.</span><span class="sxs-lookup"><span data-stu-id="6683f-122">To play the content backward from the current playback position, select the **Play** button while holding down the SHIFT key.</span></span>

<span data-ttu-id="6683f-123">Le bouton de **menu** , situé en regard du bouton de **lecture** , active un menu qui permet à l’utilisateur d’ouvrir et de fermer des fichiers AVI (Audio-Video entrelacés) et d’ajuster la taille de l’image, la vitesse de lecture et le volume.</span><span class="sxs-lookup"><span data-stu-id="6683f-123">The **Menu** button, located next to the **Play** button, activates a menu that allows the user to open and close audio-video interleaved (AVI) files, and to adjust the image size, playback speed, and volume.</span></span> <span data-ttu-id="6683f-124">(L’utilisateur peut également activer le menu en cliquant sur le bouton droit de la souris chaque fois que le curseur se trouve dans la zone cliente de la fenêtre.) Le menu comprend également des commandes permettant de modifier la configuration de l’appareil actuel, de copier le contenu de lecture dans le presse-papiers et d’émettre des commandes MCI.</span><span class="sxs-lookup"><span data-stu-id="6683f-124">(The user can also activate the menu by clicking the right mouse button whenever the cursor is in the client area of the window.) The menu also includes commands to change the configuration of the current device, to copy the playback content to the clipboard, and to issue MCI commands.</span></span>

<span data-ttu-id="6683f-125">Le TrackBar situé à droite du bouton de **menu** représente la durée du contenu de lecture (ou enregistré).</span><span class="sxs-lookup"><span data-stu-id="6683f-125">The trackbar to the right of the **Menu** button represents the duration of the playback (or recorded) content.</span></span> <span data-ttu-id="6683f-126">Le curseur sur la barre de défilement représente la position de lecture actuelle dans le contenu.</span><span class="sxs-lookup"><span data-stu-id="6683f-126">The slider on the trackbar represents the current playback position within the content.</span></span> <span data-ttu-id="6683f-127">Lorsque le curseur est positionné à l’extrémité gauche du TrackBar, la position de lecture actuelle est le début du contenu.</span><span class="sxs-lookup"><span data-stu-id="6683f-127">When the slider is positioned at the left end of the trackbar, the current playback position is the beginning of the content.</span></span> <span data-ttu-id="6683f-128">L’utilisateur peut se déplacer vers différents emplacements dans le contenu en faisant glisser le curseur sur le TrackBar.</span><span class="sxs-lookup"><span data-stu-id="6683f-128">The user can move to different locations in the content by dragging the slider along the trackbar.</span></span> <span data-ttu-id="6683f-129">Le bouton **arrêter** se trouve dans le coin inférieur gauche de la fenêtre MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="6683f-129">The **Stop** button is located in the lower-left corner of the MCIWnd window.</span></span> <span data-ttu-id="6683f-130">Il apparaît lorsque le contenu est lu.</span><span class="sxs-lookup"><span data-stu-id="6683f-130">It appears when the content is played.</span></span> <span data-ttu-id="6683f-131">L’illustration suivante montre la lecture vidéo en cours.</span><span class="sxs-lookup"><span data-stu-id="6683f-131">The following illustration shows video playback in progress.</span></span>

![image de lecture vidéo](images/mciwnd2.gif)

<span data-ttu-id="6683f-133">Les contrôles MCIWnd peuvent également inclure un bouton d' **enregistrement** pour les appareils qui peuvent enregistrer.</span><span class="sxs-lookup"><span data-stu-id="6683f-133">The MCIWnd controls can also include a **Record** button for devices that can record.</span></span> <span data-ttu-id="6683f-134">Le bouton **Enregistrer** est marqué d’un cercle rouge et s’affiche uniquement lorsque l’appareil est en capacité d’enregistrer.</span><span class="sxs-lookup"><span data-stu-id="6683f-134">The **Record** button is marked with a red circle and appears only when the device is capable of recording.</span></span>

> [!Note]  
> <span data-ttu-id="6683f-135">La fenêtre de lecture doit être alignée sur une limite de quatre pixels pour obtenir les meilleures performances de lecture vidéo.</span><span class="sxs-lookup"><span data-stu-id="6683f-135">The playback window must be aligned on a four-pixel boundary for the best video playback performance.</span></span> <span data-ttu-id="6683f-136">En général, Windows aligne automatiquement la fenêtre quand elle est créée.</span><span class="sxs-lookup"><span data-stu-id="6683f-136">Typically, Windows aligns the window automatically when it is created.</span></span> <span data-ttu-id="6683f-137">Si un utilisateur déplace ou étire la fenêtre à partir de sa position initiale, la vitesse de lecture de la vidéo peut être réduite de moitié.</span><span class="sxs-lookup"><span data-stu-id="6683f-137">If a user moves or stretches the window from its initial position, video playback speed might be reduced by half.</span></span>

 

 

 




