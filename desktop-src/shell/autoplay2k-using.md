---
description: Lorsque l’interpréteur de commandes détecte l’insertion d’un nouveau média ou la pièce jointe d’un périphérique enfichable à chaud, le contenu du périphérique ou du support est déterminé. La lecture automatique, en fonction de ses paramètres actuels, effectue l’une des opérations suivantes.
title: Utilisation et configuration de l’exécution automatique
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 096c7042-8cf0-4e4f-934f-274564218f4c
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 04a4f6dd09e03f26b13649e860beb7f2621ce952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750301"
---
# <a name="using-and-configuring-autoplay"></a><span data-ttu-id="1887b-104">Utilisation et configuration de l’exécution automatique</span><span class="sxs-lookup"><span data-stu-id="1887b-104">Using and Configuring AutoPlay</span></span>

<span data-ttu-id="1887b-105">Lorsque l’interpréteur de commandes détecte l’insertion d’un nouveau média ou la pièce jointe d’un périphérique enfichable à chaud, le contenu du périphérique ou du support est déterminé.</span><span class="sxs-lookup"><span data-stu-id="1887b-105">When the Shell detects the insertion of new media or the attachment of a hot-plug device, the contents of the device or media are determined.</span></span> <span data-ttu-id="1887b-106">La lecture automatique, en fonction de ses paramètres actuels, effectue l’une des opérations suivantes.</span><span class="sxs-lookup"><span data-stu-id="1887b-106">AutoPlay, depending on its current settings, does one of the following.</span></span>

-   <span data-ttu-id="1887b-107">Lit le contenu automatiquement.</span><span class="sxs-lookup"><span data-stu-id="1887b-107">Plays the content automatically.</span></span>
-   <span data-ttu-id="1887b-108">Affiche une boîte de dialogue invitant l’utilisateur à choisir un gestionnaire par défaut pour un type de contenu unique.</span><span class="sxs-lookup"><span data-stu-id="1887b-108">Displays a dialog box prompting the user to choose a default handler for a single content type.</span></span>
-   <span data-ttu-id="1887b-109">Présente, dans le cas d’un contenu mixte, une liste d’applications de gestionnaire disponibles à lancer.</span><span class="sxs-lookup"><span data-stu-id="1887b-109">Presents, in the case of mixed content, a list of available handler applications to launch.</span></span> <span data-ttu-id="1887b-110">Le gestionnaire choisi lit ensuite automatiquement son type de contenu associé.</span><span class="sxs-lookup"><span data-stu-id="1887b-110">The chosen handler then automatically plays its associated content type.</span></span>
-   <span data-ttu-id="1887b-111">Affiche un affichage des dossiers standard des fichiers.</span><span class="sxs-lookup"><span data-stu-id="1887b-111">Displays a standard folder view of the files.</span></span>
-   <span data-ttu-id="1887b-112">Ne fait rien si, précédemment, l’utilisateur a choisi n' **effectuer aucune action** pour ce type de contenu, et spécifié **toujours effectuer l’action sélectionnée**.</span><span class="sxs-lookup"><span data-stu-id="1887b-112">Does nothing if, earlier, the user had chosen **Take no action** for that content type as well as specified **Always do the selected action**.</span></span>

<span data-ttu-id="1887b-113">Si le contenu ne répond pas aux critères de lecture automatique, l’événement est ensuite transmis à WIA (Windows Image Acquisition).</span><span class="sxs-lookup"><span data-stu-id="1887b-113">If the contents do not meet the criteria for AutoPlay, the event is then passed to Windows Image Acquisition (WIA).</span></span>

<span data-ttu-id="1887b-114">Les rubriques suivantes traitent de la configuration et de l’utilisation de la lecture automatique.</span><span class="sxs-lookup"><span data-stu-id="1887b-114">The following topics discuss the setup and use of AutoPlay.</span></span>

-   [<span data-ttu-id="1887b-115">Préparation du matériel et des logiciels à utiliser avec l’exécution automatique</span><span class="sxs-lookup"><span data-stu-id="1887b-115">Preparing Hardware and Software for Use with AutoPlay</span></span>](#preparing-hardware-and-software-for-use-with-autoplay)
-   [<span data-ttu-id="1887b-116">Comment la fonctionnalité d’exécution automatique recherche les médias</span><span class="sxs-lookup"><span data-stu-id="1887b-116">How AutoPlay Searches Media</span></span>](#how-autoplay-searches-media)
-   [<span data-ttu-id="1887b-117">Définition de types de contenu unique et mixte</span><span class="sxs-lookup"><span data-stu-id="1887b-117">Defining Single and Mixed Content Types</span></span>](#defining-single-and-mixed-content-types)
-   [<span data-ttu-id="1887b-118">Exemples de scénarios</span><span class="sxs-lookup"><span data-stu-id="1887b-118">Sample Scenarios</span></span>](#sample-scenarios)
    -   [<span data-ttu-id="1887b-119">Lecture automatique pour les appareils de stockage avec image multimédia</span><span class="sxs-lookup"><span data-stu-id="1887b-119">AutoPlay for Storage Devices with Picture Media</span></span>](#autoplay-for-storage-devices-with-picture-media)
    -   [<span data-ttu-id="1887b-120">Lecture automatique pour les périphériques de lecture de fichiers musicaux et les dispositifs de stockage contenant des médias musicaux</span><span class="sxs-lookup"><span data-stu-id="1887b-120">AutoPlay for Music File Playback Devices and Storage Devices Containing Music Media</span></span>](#autoplay-for-music-file-playback-devices-and-storage-devices-containing-music-media)
    -   [<span data-ttu-id="1887b-121">Lecture automatique pour la lecture vidéo lors de la première présentation</span><span class="sxs-lookup"><span data-stu-id="1887b-121">AutoPlay for Video Playback on First Presentation</span></span>](#autoplay-for-video-playback-on-first-presentation)
-   [<span data-ttu-id="1887b-122">Affectation d’applications de gestionnaire par défaut</span><span class="sxs-lookup"><span data-stu-id="1887b-122">Assigning Default Handler Applications</span></span>](#assigning-default-handler-applications)
-   [<span data-ttu-id="1887b-123">Gestion des médias contenant des types de contenu mixtes</span><span class="sxs-lookup"><span data-stu-id="1887b-123">Handling Media Containing Mixed Content Types</span></span>](#handling-media-containing-mixed-content-types)
-   [<span data-ttu-id="1887b-124">Interfaces utilisateur de lecture automatique</span><span class="sxs-lookup"><span data-stu-id="1887b-124">AutoPlay User Interfaces</span></span>](#autoplay-user-interfaces)
    -   [<span data-ttu-id="1887b-125">Type de contenu unique, boîte de dialogue</span><span class="sxs-lookup"><span data-stu-id="1887b-125">Single Content Type Dialog Box</span></span>](#single-content-type-dialog-box)
    -   [<span data-ttu-id="1887b-126">Boîte de dialogue mixte de média</span><span class="sxs-lookup"><span data-stu-id="1887b-126">Mixed Media Dialog Box</span></span>](#mixed-media-dialog-box)
    -   [<span data-ttu-id="1887b-127">Page Propriété</span><span class="sxs-lookup"><span data-stu-id="1887b-127">Property Page</span></span>](#property-page)

## <a name="preparing-hardware-and-software-for-use-with-autoplay"></a><span data-ttu-id="1887b-128">Préparation du matériel et des logiciels à utiliser avec l’exécution automatique</span><span class="sxs-lookup"><span data-stu-id="1887b-128">Preparing Hardware and Software for Use with AutoPlay</span></span>

<span data-ttu-id="1887b-129">Plusieurs informations doivent apparaître dans le registre pour que l’exécution automatique fonctionne.</span><span class="sxs-lookup"><span data-stu-id="1887b-129">Several pieces of information need to appear in the registry for AutoPlay to function.</span></span> <span data-ttu-id="1887b-130">Ces informations interagissent et se référencent les unes aux autres pour former l’intégralité de l’environnement d’exécution automatique.</span><span class="sxs-lookup"><span data-stu-id="1887b-130">These pieces of information interact and reference each other to form the full AutoPlay environment.</span></span> <span data-ttu-id="1887b-131">Ce document présente la configuration de chacun de ces éléments d’information sous la forme d’une procédure autonome individuelle.</span><span class="sxs-lookup"><span data-stu-id="1887b-131">This document presents the setup of each of these pieces of information as an individual stand-alone procedure.</span></span>

<span data-ttu-id="1887b-132">Pour obtenir des instructions supplémentaires, consultez les rubriques suivantes.</span><span class="sxs-lookup"><span data-stu-id="1887b-132">See the following topics for additional instructions.</span></span>

-   [<span data-ttu-id="1887b-133">Comment affecter un gestionnaire d’appareils à un appareil</span><span class="sxs-lookup"><span data-stu-id="1887b-133">How To Assign a Device Handler to a Device</span></span>](how-to-assign-a-device-handler-to-a-device.md)
-   [<span data-ttu-id="1887b-134">Comment spécifier une icône, une étiquette ou un gestionnaire de périphériques pour un appareil à l’aide d’un groupe d’appareils</span><span class="sxs-lookup"><span data-stu-id="1887b-134">How To Specify an Icon, Label, or Device Handler for a Device Using a Device Group</span></span>](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-group.md)
-   [<span data-ttu-id="1887b-135">Comment spécifier une icône, une étiquette ou un gestionnaire de périphériques pour un appareil à l’aide d’une classe d’appareil</span><span class="sxs-lookup"><span data-stu-id="1887b-135">How To Specify an Icon, Label, or Device Handler for a Device Using a Device Class</span></span>](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-class.md)
-   [<span data-ttu-id="1887b-136">Comment empêcher l’exécution automatique d’un composant</span><span class="sxs-lookup"><span data-stu-id="1887b-136">How To Prevent AutoPlay for a Component</span></span>](how-to-prevent-autoplay-for-a-component.md)
-   [<span data-ttu-id="1887b-137">Comment inscrire un gestionnaire pour un événement d’appareil</span><span class="sxs-lookup"><span data-stu-id="1887b-137">How To Register a Handler for a Device Event</span></span>](how-to-register-a-handler-for-a-device-event.md)
-   [<span data-ttu-id="1887b-138">Guide pratique pour utiliser des événements de lecture automatique dans des applications en cours d’exécution</span><span class="sxs-lookup"><span data-stu-id="1887b-138">How To Use AutoPlay Events in Running Applications</span></span>](how-to-use-autoplay-events-in-running-applications.md)
-   [<span data-ttu-id="1887b-139">Comment inscrire un gestionnaire d’événements</span><span class="sxs-lookup"><span data-stu-id="1887b-139">How To Register an Event Handler</span></span>](how-to-register-an-event-handler.md)

## <a name="how-autoplay-searches-media"></a><span data-ttu-id="1887b-140">Comment la fonctionnalité d’exécution automatique recherche les médias</span><span class="sxs-lookup"><span data-stu-id="1887b-140">How AutoPlay Searches Media</span></span>

<span data-ttu-id="1887b-141">L’exécution automatique recherche les quatre niveaux de répertoire du média sous le répertoire racine pour rechercher les types de fichiers connus.</span><span class="sxs-lookup"><span data-stu-id="1887b-141">AutoPlay searches for media four directory levels below the root directory to find known file types.</span></span> <span data-ttu-id="1887b-142">Elle utilise la valeur PerceivedType associée à une extension de nom de fichier dans le registre pour déterminer la catégorie de fichier, qu’il s’agisse d’une image, d’un fichier audio ou d’un fichier vidéo.</span><span class="sxs-lookup"><span data-stu-id="1887b-142">It uses the PerceivedType value associated with a file name extension in the registry to determine the file category, whether it is an image, an audio file, or a video file.</span></span> <span data-ttu-id="1887b-143">Avec ces informations, l’exécution automatique lance le gestionnaire approprié pour l’appareil et le type de fichier.</span><span class="sxs-lookup"><span data-stu-id="1887b-143">With this information, AutoPlay launches the appropriate handler for that device and file type.</span></span> <span data-ttu-id="1887b-144">Pour plus d’informations, consultez [types perçus et inscription des applications](fa-perceivedtypes.md).</span><span class="sxs-lookup"><span data-stu-id="1887b-144">For more information, see [Perceived Types and Application Registration](fa-perceivedtypes.md).</span></span>

## <a name="defining-single-and-mixed-content-types"></a><span data-ttu-id="1887b-145">Définition de types de contenu unique et mixte</span><span class="sxs-lookup"><span data-stu-id="1887b-145">Defining Single and Mixed Content Types</span></span>

<span data-ttu-id="1887b-146">L’exécution automatique définit trois catégories de contenu principales.</span><span class="sxs-lookup"><span data-stu-id="1887b-146">AutoPlay defines three main content categories.</span></span>

-   <span data-ttu-id="1887b-147">Images</span><span class="sxs-lookup"><span data-stu-id="1887b-147">Pictures</span></span>
-   <span data-ttu-id="1887b-148">Musique</span><span class="sxs-lookup"><span data-stu-id="1887b-148">Music</span></span>
-   <span data-ttu-id="1887b-149">Vidéo</span><span class="sxs-lookup"><span data-stu-id="1887b-149">Video</span></span>

<span data-ttu-id="1887b-150">Un support est considéré comme contenant un type de contenu unique si tous les fichiers sur le support appartiennent à une seule de ces trois catégories.</span><span class="sxs-lookup"><span data-stu-id="1887b-150">A medium is considered to contain a single content type if all of the files on the medium fall into only one of these three categories.</span></span> <span data-ttu-id="1887b-151">Notez que cela ne signifie pas que les fichiers doivent être du même type de *fichier* ;. jpg,. gif et. bmp sont des types de fichiers différents, mais un type de contenu (images).</span><span class="sxs-lookup"><span data-stu-id="1887b-151">Note that this does not mean that the files must be of the same *file* type; .jpg, .gif, and .bmp are different file types, but one content type (pictures).</span></span>

<span data-ttu-id="1887b-152">Si les types de contenu pris en charge sont présents sur le support, mais qu’aucun type de contenu ne peut prendre en compte 100% du total, le support est considéré comme contenant un type de contenu mixte et est géré en conséquence.</span><span class="sxs-lookup"><span data-stu-id="1887b-152">If supported content types are present on the medium, but no single content type can account for 100 percent of the total, then the medium is considered to contain mixed content type and is handled accordingly.</span></span> <span data-ttu-id="1887b-153">Pour plus d’informations, consultez [gestion des médias contenant des types de contenu mixtes](#handling-media-containing-mixed-content-types).</span><span class="sxs-lookup"><span data-stu-id="1887b-153">For more information, see [Handling Media Containing Mixed Content Types](#handling-media-containing-mixed-content-types).</span></span>

## <a name="sample-scenarios"></a><span data-ttu-id="1887b-154">Exemples de scénarios</span><span class="sxs-lookup"><span data-stu-id="1887b-154">Sample Scenarios</span></span>

<span data-ttu-id="1887b-155">Les scénarios suivants fournissent une compréhension élémentaire des éléments à attendre de l’exécution automatique.</span><span class="sxs-lookup"><span data-stu-id="1887b-155">The following scenarios provide a basic understanding of what to expect from AutoPlay.</span></span>

### <a name="autoplay-for-storage-devices-with-picture-media"></a><span data-ttu-id="1887b-156">Lecture automatique pour les appareils de stockage avec image multimédia</span><span class="sxs-lookup"><span data-stu-id="1887b-156">AutoPlay for Storage Devices with Picture Media</span></span>

1.  <span data-ttu-id="1887b-157">L’utilisateur attache un lecteur USB SanDisk CompactFlash qui a déjà un support inséré contenant un type de contenu d’image de 100% sous la forme de fichiers. jpg.</span><span class="sxs-lookup"><span data-stu-id="1887b-157">The user attaches a USB SanDisk CompactFlash reader device that already has media inserted containing 100 percent picture content type in the form of .jpg files.</span></span>
2.  <span data-ttu-id="1887b-158">La notification affiche **le nouveau matériel-SanDisk ImageMate**.</span><span class="sxs-lookup"><span data-stu-id="1887b-158">Notification displays **Found New Hardware - SanDisk ImageMate**.</span></span>
3.  <span data-ttu-id="1887b-159">L’exécution automatique lance l’application d’image appropriée.</span><span class="sxs-lookup"><span data-stu-id="1887b-159">AutoPlay launches the appropriate image application.</span></span>

<span data-ttu-id="1887b-160">De même, lorsque l’utilisateur insère le même média CompactFlash dans le lecteur alors que le lecteur est déjà attaché au système, l’événement Media Insert fait également en sorte que l’exécution automatique lance l’application diaporama d’images.</span><span class="sxs-lookup"><span data-stu-id="1887b-160">Similarly, when the user inserts that same CompactFlash media into the reader when the reader is already attached to the system, the media insert event also causes AutoPlay to launch the image slide show application.</span></span> <span data-ttu-id="1887b-161">L’utilisateur a la possibilité d’accéder à la page des propriétés du périphérique multimédia SanDisk pour remplacer la valeur par défaut par une autre application d’exécution automatique inscrite, telle que l’Assistant scanneur et appareil photo, ou Picture It !.</span><span class="sxs-lookup"><span data-stu-id="1887b-161">The user has the option of going to the Properties page of the SanDisk media device to change the default to another registered AutoPlay application, such as the Scanner and Camera Wizard or Picture It!.</span></span>

### <a name="autoplay-for-music-file-playback-devices-and-storage-devices-containing-music-media"></a><span data-ttu-id="1887b-162">Lecture automatique pour les périphériques de lecture de fichiers musicaux et les dispositifs de stockage contenant des médias musicaux</span><span class="sxs-lookup"><span data-stu-id="1887b-162">AutoPlay for Music File Playback Devices and Storage Devices Containing Music Media</span></span>

1.  <span data-ttu-id="1887b-163">L’utilisateur attache un lecteur MP3 Diamond Rio USB.</span><span class="sxs-lookup"><span data-stu-id="1887b-163">The user attaches a USB Diamond Rio MP3 Player.</span></span>
2.  <span data-ttu-id="1887b-164">La notification affiche **un nouveau matériel-lecteur MP3 Diamond Rio**.</span><span class="sxs-lookup"><span data-stu-id="1887b-164">Notification displays **Found New Hardware - Diamond Rio MP3 Player**.</span></span>
3.  <span data-ttu-id="1887b-165">L’exécution automatique lit les fichiers à l’aide de son gestionnaire par défaut enregistré, par exemple le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="1887b-165">AutoPlay plays the files using its registered default handler—for instance, Windows Media Player.</span></span>

<span data-ttu-id="1887b-166">De même, si l’utilisateur insère un support contenant des fichiers. mp3 (par exemple, CompactFlash, SmartMedia, Memory Stick ou CD-ROM) qui compte 100% du contenu total pris en charge dans un dispositif de stockage, l’événement Media Insert entraîne également la lecture des fichiers par la lecture automatique à l’aide du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="1887b-166">Similarly, if the user inserts any media containing .mp3 files (for example, CompactFlash, SmartMedia, Memory Stick, or CD-ROM) that account for 100 percent of the total supported content into a storage device, the media insert event would also cause AutoPlay to play the files using the Windows Media Player.</span></span> <span data-ttu-id="1887b-167">L’utilisateur peut accéder à la feuille de propriétés du dispositif de stockage et remplacer l’action par défaut par une autre application de lecture automatique inscrite, telle que WinAmp ou Real Player.</span><span class="sxs-lookup"><span data-stu-id="1887b-167">The user can access the property sheet of the storage device and change the default action to another registered AutoPlay application, such as WinAmp or Real Player.</span></span>

### <a name="autoplay-for-video-playback-on-first-presentation"></a><span data-ttu-id="1887b-168">Lecture automatique pour la lecture vidéo lors de la première présentation</span><span class="sxs-lookup"><span data-stu-id="1887b-168">AutoPlay for Video Playback on First Presentation</span></span>

1.  <span data-ttu-id="1887b-169">L’utilisateur se connecte à une caméra vidéo numérique 1394 pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="1887b-169">The user plugs in a 1394 digital video camera for the first time.</span></span>
2.  <span data-ttu-id="1887b-170">L’utilisateur reçoit une boîte de dialogue simple qui demande l’exécution de l’application.</span><span class="sxs-lookup"><span data-stu-id="1887b-170">The user is presented with a simple dialog box that asks what application to run.</span></span> <span data-ttu-id="1887b-171">Les choix sont d’exécuter l’une des applications de lecture automatique inscrite ou d’ouvrir un dossier pour afficher les fichiers.</span><span class="sxs-lookup"><span data-stu-id="1887b-171">The choices are to run one of the registered AutoPlay applications or to open a folder to view files.</span></span> <span data-ttu-id="1887b-172">L’utilisateur peut définir le comportement sélectionné pour qu’il soit enregistré en tant qu’action par défaut pour les événements de connexion à chaud d’une caméra vidéo numérique.</span><span class="sxs-lookup"><span data-stu-id="1887b-172">The user may set the selected behavior to be saved as the default action for later digital video camera hot-plug events.</span></span>

## <a name="assigning-default-handler-applications"></a><span data-ttu-id="1887b-173">Affectation d’applications de gestionnaire par défaut</span><span class="sxs-lookup"><span data-stu-id="1887b-173">Assigning Default Handler Applications</span></span>

<span data-ttu-id="1887b-174">Une nouvelle installation de Windows recherche l’exécution automatique avec un ensemble d’applications de gestionnaire inscrites.</span><span class="sxs-lookup"><span data-stu-id="1887b-174">A fresh installation of Windows finds AutoPlay with a set of registered handler applications.</span></span> <span data-ttu-id="1887b-175">Les applications inscrites par défaut lors de l’installation de Windows sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="1887b-175">Applications registered by default during a Windows installation are as follows.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1887b-176">Type de support</span><span class="sxs-lookup"><span data-stu-id="1887b-176">Media Type</span></span></th>
<th><span data-ttu-id="1887b-177">Applications</span><span class="sxs-lookup"><span data-stu-id="1887b-177">Applications</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1887b-178">Images</span><span class="sxs-lookup"><span data-stu-id="1887b-178">Pictures</span></span></td>
<td><ul>
<li><span data-ttu-id="1887b-179">Diaporama (par défaut)</span><span class="sxs-lookup"><span data-stu-id="1887b-179">Slide Show (default)</span></span></li>
<li><span data-ttu-id="1887b-180">Assistant appareil photo et scanneur</span><span class="sxs-lookup"><span data-stu-id="1887b-180">Camera and Scanner Wizard</span></span></li>
<li><span data-ttu-id="1887b-181">Assistant impression</span><span class="sxs-lookup"><span data-stu-id="1887b-181">Printing Wizard</span></span></li>
<li><span data-ttu-id="1887b-182">Ouvrir le dossier</span><span class="sxs-lookup"><span data-stu-id="1887b-182">Open folder</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1887b-183">Musique</span><span class="sxs-lookup"><span data-stu-id="1887b-183">Music</span></span></td>
<td><ul>
<li><span data-ttu-id="1887b-184">Lecteur Windows Media (par défaut)</span><span class="sxs-lookup"><span data-stu-id="1887b-184">Windows Media Player (default)</span></span></li>
<li><span data-ttu-id="1887b-185">Ouvrir le dossier</span><span class="sxs-lookup"><span data-stu-id="1887b-185">Open folder</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1887b-186">Vidéo</span><span class="sxs-lookup"><span data-stu-id="1887b-186">Video</span></span></td>
<td><ul>
<li><span data-ttu-id="1887b-187">Lecteur Windows Media (par défaut)</span><span class="sxs-lookup"><span data-stu-id="1887b-187">Windows Media Player (default)</span></span></li>
<li><span data-ttu-id="1887b-188">Ouvrir le dossier</span><span class="sxs-lookup"><span data-stu-id="1887b-188">Open folder</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="1887b-189">Dans le cas de types non pris en charge, les utilisateurs sont invités à attribuer le paramètre par défaut de l’action d’exécution automatique associée à chaque périphérique de stockage lors de sa première introduction au système.</span><span class="sxs-lookup"><span data-stu-id="1887b-189">In the case of non-supported types, users are asked to assign the default setting for the AutoPlay action associated with each storage device on its first introduction to the system.</span></span> <span data-ttu-id="1887b-190">À ce moment-là, l’utilisateur est invité à choisir une action dans une liste fournie d’applications inscrites ou à afficher un affichage des dossiers qui répertorie le contenu du média.</span><span class="sxs-lookup"><span data-stu-id="1887b-190">At that time, the user is prompted to choose an action from a provided list of registered applications or to display a folder view listing the media content.</span></span> <span data-ttu-id="1887b-191">L’utilisateur a également la possibilité de choisir d’être invité à chaque fois que le type de média est détecté, plutôt que d’enregistrer une application particulière par défaut.</span><span class="sxs-lookup"><span data-stu-id="1887b-191">The user also has the option of choosing to be prompted each time the media type is detected rather than saving any particular application as a default.</span></span>

> [!Note]  
> <span data-ttu-id="1887b-192">Les fabricants de périphériques ont la possibilité d’inscrire et d’attribuer des applications par défaut à utiliser avec leurs produits spécifiques.</span><span class="sxs-lookup"><span data-stu-id="1887b-192">Device manufacturers have the option of registering and assigning default applications to be used with their particular products.</span></span> <span data-ttu-id="1887b-193">Dans ce cas, la boîte de dialogue offrant un choix à l’utilisateur n’est pas affichée.</span><span class="sxs-lookup"><span data-stu-id="1887b-193">In these cases, the dialog box offering a choice to the user is not displayed.</span></span>

 

<span data-ttu-id="1887b-194">Pour être proposé en tant qu’option de gestionnaire par l’exécution automatique, les applications nouvellement installées doivent s’inscrire dans le registre.</span><span class="sxs-lookup"><span data-stu-id="1887b-194">To be offered as a handler option by AutoPlay, newly installed applications must register themselves in the registry.</span></span> <span data-ttu-id="1887b-195">Pour plus d’informations, consultez [préparation du matériel et des logiciels à utiliser avec l’exécution automatique](#preparing-hardware-and-software-for-use-with-autoplay).</span><span class="sxs-lookup"><span data-stu-id="1887b-195">For details, see [Preparing Hardware and Software for Use with AutoPlay](#preparing-hardware-and-software-for-use-with-autoplay).</span></span>

<span data-ttu-id="1887b-196">Les utilisateurs peuvent toujours modifier le gestionnaire d’exécution automatique par défaut pour n’importe quel périphérique de stockage ou type de contenu.</span><span class="sxs-lookup"><span data-stu-id="1887b-196">Users can always change the default AutoPlay handler for any storage device or content type.</span></span> <span data-ttu-id="1887b-197">La page de propriétés lecture automatique est accessible en modification dans la feuille de propriétés du dispositif de stockage dans **poste de travail**.</span><span class="sxs-lookup"><span data-stu-id="1887b-197">The AutoPlay property page is accessible for change in the property sheet of the storage device in **My Computer**.</span></span>

<span data-ttu-id="1887b-198">Pour obtenir des exemples d’invites utilisateur et de pages de propriétés, consultez [lecture automatique d’interfaces utilisateur](#autoplay-user-interfaces).</span><span class="sxs-lookup"><span data-stu-id="1887b-198">For examples of user prompts and property pages, see [AutoPlay User Interfaces](#autoplay-user-interfaces).</span></span>

## <a name="handling-media-containing-mixed-content-types"></a><span data-ttu-id="1887b-199">Gestion des médias contenant des types de contenu mixtes</span><span class="sxs-lookup"><span data-stu-id="1887b-199">Handling Media Containing Mixed Content Types</span></span>

<span data-ttu-id="1887b-200">Lorsque l’exécution automatique est présentée avec un support de contenu mixte, elle nécessite une intervention de l’utilisateur avant de pouvoir agir.</span><span class="sxs-lookup"><span data-stu-id="1887b-200">When AutoPlay is presented with a mixed content medium, it requires user input before it can take action.</span></span> <span data-ttu-id="1887b-201">Dans ce cas, une boîte de dialogue contenant une liste filtrée de toutes les applications inscrites appropriées disponibles pour les types de contenu présents sur le média est présentée à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1887b-201">In this case, the user is presented with a dialog box containing a filtered list of all appropriate registered applications available for the content types present on the media.</span></span> <span data-ttu-id="1887b-202">L’utilisateur peut choisir l’une de ces applications pour effectuer une lecture automatique de ce type de contenu particulier, tandis que le reste reste intact.</span><span class="sxs-lookup"><span data-stu-id="1887b-202">The user can choose one of these applications to AutoPlay that particular content type, while the rest remain untouched.</span></span> <span data-ttu-id="1887b-203">Étant donné que la composition d’un contenu mixte varie avec chaque disque, il n’existe aucune option permettant d’enregistrer ce choix par défaut.</span><span class="sxs-lookup"><span data-stu-id="1887b-203">As the composition of mixed content media varies with each individual disc, there is no option to save this choice as a default.</span></span>

<span data-ttu-id="1887b-204">Pour obtenir des exemples d’invites utilisateur, consultez [lecture automatique d’interfaces utilisateur](#autoplay-user-interfaces).</span><span class="sxs-lookup"><span data-stu-id="1887b-204">For examples of user prompts, see [AutoPlay User Interfaces](#autoplay-user-interfaces).</span></span>

## <a name="autoplay-user-interfaces"></a><span data-ttu-id="1887b-205">Interfaces utilisateur de lecture automatique</span><span class="sxs-lookup"><span data-stu-id="1887b-205">AutoPlay User Interfaces</span></span>

<span data-ttu-id="1887b-206">Il existe trois interfaces utilisateur possibles.</span><span class="sxs-lookup"><span data-stu-id="1887b-206">There are three possible user interfaces.</span></span>

-   <span data-ttu-id="1887b-207">Boîte de dialogue qui invite l’utilisateur à entrer une action pour un type de contenu unique</span><span class="sxs-lookup"><span data-stu-id="1887b-207">A dialog box that prompts the user to enter an action for a single content type</span></span>
-   <span data-ttu-id="1887b-208">Boîte de dialogue qui invite l’utilisateur à entrer une action pour les types de contenu mixtes</span><span class="sxs-lookup"><span data-stu-id="1887b-208">A dialog box that prompts the user to enter an action for mixed content types</span></span>
-   <span data-ttu-id="1887b-209">Une page de propriétés</span><span class="sxs-lookup"><span data-stu-id="1887b-209">A property page</span></span>

### <a name="single-content-type-dialog-box"></a><span data-ttu-id="1887b-210">Type de contenu unique, boîte de dialogue</span><span class="sxs-lookup"><span data-stu-id="1887b-210">Single Content Type Dialog Box</span></span>

<span data-ttu-id="1887b-211">Une boîte de dialogue similaire à ce qui suit s’affiche quand un support pris en charge n’a pas encore été affecté à une action d’exécution automatique par défaut est présenté au système.</span><span class="sxs-lookup"><span data-stu-id="1887b-211">A dialog box similar to the following is displayed when any supported media not yet assigned a default AutoPlay action is presented to the system.</span></span>

![capture d’écran de la boîte de dialogue de type de contenu unique](images/pix.png)

<span data-ttu-id="1887b-213">Les utilisateurs peuvent effectuer l’une des opérations suivantes.</span><span class="sxs-lookup"><span data-stu-id="1887b-213">Users can do one of the following.</span></span>

-   <span data-ttu-id="1887b-214">Choisissez une action dans la liste des applications inscrites.</span><span class="sxs-lookup"><span data-stu-id="1887b-214">Choose an action from the list of registered applications.</span></span>
-   <span data-ttu-id="1887b-215">Répertoriez les fichiers sur le support dans un affichage normal du dossier.</span><span class="sxs-lookup"><span data-stu-id="1887b-215">List the files on the medium in a normal folder view.</span></span>
-   <span data-ttu-id="1887b-216">Aucune action n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="1887b-216">Take no action.</span></span>

<span data-ttu-id="1887b-217">Un utilisateur peut également enregistrer un choix en tant qu’action par défaut pour ce support en cliquant sur la zone **toujours faire l’action sélectionnée** .</span><span class="sxs-lookup"><span data-stu-id="1887b-217">A user can also save a choice as the default action for this medium by clicking the **Always do the selected action** box.</span></span> <span data-ttu-id="1887b-218">Une fois ce choix effectué, la boîte de dialogue ne s’affiche plus.</span><span class="sxs-lookup"><span data-stu-id="1887b-218">Once this choice is made, the dialog is not shown again.</span></span> <span data-ttu-id="1887b-219">Toutefois, dans Windows XP Service Pack 1 (SP1), si une nouvelle application capable de gérer un type de média particulier est ajoutée à l’ordinateur, la boîte de dialogue est à nouveau présentée à l’utilisateur, ce qui lui donne la possibilité de sélectionner la nouvelle application comme action d’exécution par défaut.</span><span class="sxs-lookup"><span data-stu-id="1887b-219">However, in Windows XP Service Pack 1 (SP1), if a new application that can handle a particular media type is added to the computer, the dialog is once again presented to the user, giving them the opportunity to select the new application as the default AutoPlay action.</span></span> <span data-ttu-id="1887b-220">Les applications peuvent également se définir comme sélection par défaut lorsqu’elles sont installées.</span><span class="sxs-lookup"><span data-stu-id="1887b-220">Applications can also set themselves as the default selection when they are installed.</span></span>

<span data-ttu-id="1887b-221">Windows XP SP1 ajoute également une fonctionnalité qui conserve le choix de l’action d’exécution automatique de l’utilisateur s’il ne clique pas sur la zone **toujours faire l’action sélectionnée** .</span><span class="sxs-lookup"><span data-stu-id="1887b-221">Windows XP SP1 also adds a feature that retains the user's choice of AutoPlay action if they do not click the **Always do the selected action** box.</span></span> <span data-ttu-id="1887b-222">Si un utilisateur choisit une action d’exécution automatique pour une instance unique, la prochaine fois que cette boîte de dialogue est présentée pour ce type de média, la même action est la sélection par défaut.</span><span class="sxs-lookup"><span data-stu-id="1887b-222">If a user chooses an AutoPlay action for a single instance, the next time that dialog is presented for that media type, the same action is the default selection.</span></span>

<span data-ttu-id="1887b-223">Pour qu’une application soit incluse dans la liste des actions possibles, elle doit être inscrite avec l’exécution automatique.</span><span class="sxs-lookup"><span data-stu-id="1887b-223">For an application to be included in the list of possible actions, it must be registered with AutoPlay.</span></span> <span data-ttu-id="1887b-224">Pour plus d’informations, consultez [préparation du matériel et des logiciels à utiliser avec l’exécution automatique](#preparing-hardware-and-software-for-use-with-autoplay).</span><span class="sxs-lookup"><span data-stu-id="1887b-224">For more information, see [Preparing Hardware and Software for Use with AutoPlay](#preparing-hardware-and-software-for-use-with-autoplay).</span></span>

### <a name="mixed-media-dialog-box"></a><span data-ttu-id="1887b-225">Boîte de dialogue mixte de média</span><span class="sxs-lookup"><span data-stu-id="1887b-225">Mixed Media Dialog Box</span></span>

<span data-ttu-id="1887b-226">La boîte de dialogue suivante s’affiche lorsqu’un support contenant un mélange de types de fichiers pris en charge est présenté au système.</span><span class="sxs-lookup"><span data-stu-id="1887b-226">The following dialog box is displayed when any medium containing a mix of supported file types is presented to the system.</span></span> <span data-ttu-id="1887b-227">Il s’agit essentiellement de la même boîte de dialogue de support de contenu, mais avec deux différences significatives.</span><span class="sxs-lookup"><span data-stu-id="1887b-227">This is essentially the same as the single content medium dialog box but with two significant differences.</span></span> <span data-ttu-id="1887b-228">Tout d’abord, les options d’action disponibles consistent en une liste filtrée d’applications pertinentes pour tous les types de contenu présents sur le support.</span><span class="sxs-lookup"><span data-stu-id="1887b-228">First, the available action options consist of a filtered list of applications relevant to all content types present on the medium.</span></span> <span data-ttu-id="1887b-229">Deuxièmement, il n’est pas possible de choisir une action par défaut permanente, car les types de contenu et les pourcentages de médias de contenu mixte sont trop imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="1887b-229">Second, there is no option to choose a permanent default action because the content types and percentages of mixed content media are too unpredictable.</span></span>

![capture d’écran de la boîte de dialogue de média mixte](images/mix.png)

<span data-ttu-id="1887b-231">Pour qu’une application soit incluse dans la liste des actions possibles, elle doit être inscrite avec l’exécution automatique.</span><span class="sxs-lookup"><span data-stu-id="1887b-231">For an application to be included in the list of possible actions, it must be registered with AutoPlay.</span></span> <span data-ttu-id="1887b-232">Pour plus d’informations, consultez [préparation du matériel et des logiciels à utiliser avec l’exécution automatique](#preparing-hardware-and-software-for-use-with-autoplay).</span><span class="sxs-lookup"><span data-stu-id="1887b-232">For more information, see [Preparing Hardware and Software for Use with AutoPlay](#preparing-hardware-and-software-for-use-with-autoplay).</span></span>

### <a name="property-page"></a><span data-ttu-id="1887b-233">Page Propriété</span><span class="sxs-lookup"><span data-stu-id="1887b-233">Property Page</span></span>

<span data-ttu-id="1887b-234">Voici un exemple de page de propriétés d’exécution automatique pour un périphérique DVD/CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="1887b-234">The following is a sample AutoPlay property page for a DVD/CD-ROM device.</span></span>

![capture d’écran de la page de propriétés](images/apdlg.png)

<span data-ttu-id="1887b-236">Chaque type d’appareil offre un sous-ensemble approprié de types de contenu pour la configuration de l’exécution automatique.</span><span class="sxs-lookup"><span data-stu-id="1887b-236">Each device type offers an appropriate subset of content types for AutoPlay configuration.</span></span> <span data-ttu-id="1887b-237">À son tour, chaque type de contenu, lorsqu’il est sélectionné, offre une liste appropriée des options d’action dans la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="1887b-237">In turn, each content type, when selected, offers an appropriate list of action options in the list box.</span></span> <span data-ttu-id="1887b-238">Une action différente peut être choisie pour chaque type de contenu.</span><span class="sxs-lookup"><span data-stu-id="1887b-238">A different action can be chosen for each content type.</span></span>

 

 



