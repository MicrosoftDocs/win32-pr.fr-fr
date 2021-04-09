---
description: Exemple DVApp
ms.assetid: 80375170-d0d6-4371-abe3-078703e158b1
title: Exemple DVApp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86653781d08921bf638e7798fb34f3a86e8d34a8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109386"
---
# <a name="dvapp-sample"></a><span data-ttu-id="fe085-103">Exemple DVApp</span><span class="sxs-lookup"><span data-stu-id="fe085-103">DVApp Sample</span></span>

## <a name="description"></a><span data-ttu-id="fe085-104">Description</span><span class="sxs-lookup"><span data-stu-id="fe085-104">Description</span></span>

<span data-ttu-id="fe085-105">Application de capture vidéo numérique (DV).</span><span class="sxs-lookup"><span data-stu-id="fe085-105">Digital Video (DV) capture application.</span></span>

<span data-ttu-id="fe085-106">Cet exemple montre comment créer différents types de graphiques de filtre pour contrôler les caméscopes DV.</span><span class="sxs-lookup"><span data-stu-id="fe085-106">This sample demonstrates how to build various types of filter graphs for controlling DV camcorders.</span></span> <span data-ttu-id="fe085-107">Il montre également comment effectuer des captures, des aperçus, des transmissions et des contrôles d’appareil avec un caméscope DV.</span><span class="sxs-lookup"><span data-stu-id="fe085-107">It also shows how to perform capture, preview, transmit, and device control with a DV camcorder.</span></span>

### <a name="usage"></a><span data-ttu-id="fe085-108">Utilisation</span><span class="sxs-lookup"><span data-stu-id="fe085-108">Usage</span></span>

<span data-ttu-id="fe085-109">L’application DVApp prend en charge les modes suivants :</span><span class="sxs-lookup"><span data-stu-id="fe085-109">The DVApp application supports the following modes:</span></span>

-   <span data-ttu-id="fe085-110">Aperçu : effectue le rendu du DV à partir du caméscope dans une fenêtre vidéo.</span><span class="sxs-lookup"><span data-stu-id="fe085-110">Preview: Renders DV from the camcorder to a video window.</span></span>
-   <span data-ttu-id="fe085-111">Fichier DV vers type-1 : capture les données DV du caméscope dans un fichier DV de type 1.</span><span class="sxs-lookup"><span data-stu-id="fe085-111">DV to type-1 file: Captures DV data from the camcorder to a type-1 DV file.</span></span>
-   <span data-ttu-id="fe085-112">Tapez-1 fichier sur DV : transmet les données d’un fichier DV type-1 au caméscope.</span><span class="sxs-lookup"><span data-stu-id="fe085-112">Type-1 file to DV: Transmits data from a type-1 DV file to the camcorder.</span></span>
-   <span data-ttu-id="fe085-113">Fichier DV vers type-2 : capture les données DV du caméscope dans un fichier DV de type 2.</span><span class="sxs-lookup"><span data-stu-id="fe085-113">DV to type-2 file: Captures DV data from the camcorder to a type-2 DV file.</span></span>
-   <span data-ttu-id="fe085-114">Tapez-2 fichier sur DV : transmet les données d’un fichier DV type-2 au caméscope.</span><span class="sxs-lookup"><span data-stu-id="fe085-114">Type-2 file to DV: Transmits data from a type-2 DV file to the camcorder.</span></span>

<span data-ttu-id="fe085-115">Les modes capture et transmission effectuent également une préversion.</span><span class="sxs-lookup"><span data-stu-id="fe085-115">The capture and transmit modes also perform preview.</span></span> <span data-ttu-id="fe085-116">Chacun de ces modes n’a **pas** d’option d’aperçu, ce qui désactive la version préliminaire.</span><span class="sxs-lookup"><span data-stu-id="fe085-116">Each of those modes has a **No Preview** option as well, which disables preview.</span></span> <span data-ttu-id="fe085-117">La capture sans aperçu est plus efficace et peut réduire le nombre d’images supprimées.</span><span class="sxs-lookup"><span data-stu-id="fe085-117">Capturing without preview is more efficient and can reduce the number of dropped frames.</span></span>

<span data-ttu-id="fe085-118">L’application démarre en mode aperçu.</span><span class="sxs-lookup"><span data-stu-id="fe085-118">The application starts in preview mode.</span></span> <span data-ttu-id="fe085-119">Pour sélectionner un autre mode, choisissez un mode dans le menu **mode du graphique** .</span><span class="sxs-lookup"><span data-stu-id="fe085-119">To select another mode, choose a mode from the **Graph Mode** menu.</span></span> <span data-ttu-id="fe085-120">Pour chaque mode, DVApp génère un graphique de filtre qui prend en charge les fonctionnalités de ce mode.</span><span class="sxs-lookup"><span data-stu-id="fe085-120">For each mode, DVApp builds a filter graph that supports the functionality of that mode.</span></span> <span data-ttu-id="fe085-121">Pour enregistrer le graphique en tant que fichier GraphEdit (. GRF), sélectionnez **enregistrer le graphique dans un fichier** dans le menu **fichier** .</span><span class="sxs-lookup"><span data-stu-id="fe085-121">To save the graph as a GraphEdit (.grf) file, select **Save Graph to File** from the **File** menu.</span></span> <span data-ttu-id="fe085-122">Quittez DVApp avant d’ouvrir le fichier dans GraphEdit.</span><span class="sxs-lookup"><span data-stu-id="fe085-122">Quit DVApp before opening the file in GraphEdit.</span></span>

<span data-ttu-id="fe085-123">Pour capturer dans un fichier :</span><span class="sxs-lookup"><span data-stu-id="fe085-123">To capture to a file:</span></span>

1.  <span data-ttu-id="fe085-124">Dans le menu **fichier** , choisissez **définir le fichier de sortie** et entrez un nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="fe085-124">From the **File** menu, choose **Set Output File** and enter a file name.</span></span>
2.  <span data-ttu-id="fe085-125">Dans le menu **mode du graphique** , sélectionnez un mode *DV vers fichier* (tapez 1 ou tapez 2, avec ou sans aperçu).</span><span class="sxs-lookup"><span data-stu-id="fe085-125">From the **Graph Mode** menu, select a *DV to File* mode (type 1 or type 2, with or without preview).</span></span>
3.  <span data-ttu-id="fe085-126">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="fe085-126">Click **Record**.</span></span>
4.  <span data-ttu-id="fe085-127">Si le caméscope est en mode VTR, cliquez sur **lire**.</span><span class="sxs-lookup"><span data-stu-id="fe085-127">If the camcorder is in VTR mode, click **Play**.</span></span>
5.  <span data-ttu-id="fe085-128">Pour arrêter la capture, cliquez sur **arrêter**.</span><span class="sxs-lookup"><span data-stu-id="fe085-128">To stop capturing, click **Stop**.</span></span>

<span data-ttu-id="fe085-129">Pour transmettre un fichier au caméscope, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="fe085-129">To transmit from a file to the camcorder:</span></span>

1.  <span data-ttu-id="fe085-130">Dans le menu **fichier** , cliquez sur **définir le fichier d’entrée** et sélectionnez un fichier DV.</span><span class="sxs-lookup"><span data-stu-id="fe085-130">From the **File** menu, click **Set Input File** and select a DV file.</span></span> <span data-ttu-id="fe085-131">Le fichier doit correspondre au mode sélectionné (type 1 ou type 2).</span><span class="sxs-lookup"><span data-stu-id="fe085-131">The file must match the selected mode (type 1 or type 2).</span></span>
2.  <span data-ttu-id="fe085-132">Dans le menu **mode du graphique** , sélectionnez un fichier en mode *DV* (tapez 1 ou tapez 2, avec ou sans aperçu).</span><span class="sxs-lookup"><span data-stu-id="fe085-132">From the **Graph Mode** menu, select a *File to DV* mode (type 1 or type 2, with or without preview).</span></span>
3.  <span data-ttu-id="fe085-133">Cliquez sur **Lire**.</span><span class="sxs-lookup"><span data-stu-id="fe085-133">Click **Play**.</span></span>
4.  <span data-ttu-id="fe085-134">Pour enregistrer les données sur bande, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="fe085-134">To record the data to tape, click **Record**.</span></span>
5.  <span data-ttu-id="fe085-135">Pour arrêter la transmission, cliquez sur **arrêter**.</span><span class="sxs-lookup"><span data-stu-id="fe085-135">To stop transmitting, click **Stop**.</span></span>

<span data-ttu-id="fe085-136">Si le caméscope est en mode VTR, l’utilisateur peut contrôler le mécanisme de transport via les boutons de style VCR de l’application.</span><span class="sxs-lookup"><span data-stu-id="fe085-136">If the camcorder is in VTR mode, the user can control the transport mechanism through the application's VCR-style buttons.</span></span> <span data-ttu-id="fe085-137">Pour rechercher la bande, entrez le code temporel cible, puis cliquez sur le bouton Rechercher.</span><span class="sxs-lookup"><span data-stu-id="fe085-137">To seek the tape, enter the target timecode and click the seek button.</span></span>

<span data-ttu-id="fe085-138">Pour limiter la quantité de données capturées par l’application, choisissez **taille de capture** dans le menu **fichier** .</span><span class="sxs-lookup"><span data-stu-id="fe085-138">To limit how much data the application captures, choose **Capture Size** from the **File** menu.</span></span>

<span data-ttu-id="fe085-139">Pour vérifier le format de bande (NTSC ou PAL), choisissez **Vérifier la bande** dans le menu **options** .</span><span class="sxs-lookup"><span data-stu-id="fe085-139">To check the tape format (NTSC or PAL), choose **Check Tape** from the **Options** menu.</span></span>

<span data-ttu-id="fe085-140">Pour modifier la taille de la fenêtre d’aperçu, choisissez **modifier la taille du décodage** dans le menu **options** .</span><span class="sxs-lookup"><span data-stu-id="fe085-140">To change the size of the preview window, choose **Change Decode Size** from the **Options** menu.</span></span>

### <a name="programming-notes"></a><span data-ttu-id="fe085-141">Notes de programmation</span><span class="sxs-lookup"><span data-stu-id="fe085-141">Programming Notes</span></span>

<span data-ttu-id="fe085-142">L’objectif principal de cette application est de montrer comment créer différents graphiques de capture DV et de transmission.</span><span class="sxs-lookup"><span data-stu-id="fe085-142">The main purpose of this application is to show how to build various DV capture and transmit graphs.</span></span>

### <a name="device-arrival-and-removal"></a><span data-ttu-id="fe085-143">Arrivée et suppression de l’appareil</span><span class="sxs-lookup"><span data-stu-id="fe085-143">Device Arrival and Removal</span></span>

<span data-ttu-id="fe085-144">L’application gère l’arrivée et la suppression des appareils à l’aide de deux techniques différentes.</span><span class="sxs-lookup"><span data-stu-id="fe085-144">The application handles device arrival and removal, using two different techniques.</span></span> <span data-ttu-id="fe085-145">Pour l’arrivée de l’appareil, la boucle de message de l’application répond aux \_ messages WM DEVICECHANGE.</span><span class="sxs-lookup"><span data-stu-id="fe085-145">For device arrival, the application's message loop responds to WM\_DEVICECHANGE messages.</span></span> <span data-ttu-id="fe085-146">Pour la suppression de l’appareil, l’application répond aux événements de [**\_ \_ perte d’appareil EC**](ec-device-lost.md) du gestionnaire de graphes de filtre.</span><span class="sxs-lookup"><span data-stu-id="fe085-146">For device removal, the application responds to [**EC\_DEVICE\_LOST**](ec-device-lost.md) events from the filter graph manager.</span></span> <span data-ttu-id="fe085-147">L’une ou l’autre approche fonctionne, bien que l' \_ \_ événement de perte de l’appareil EC dépende de l’existence de l’appareil dans le graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="fe085-147">Either approach works, although the EC\_DEVICE\_LOST event depends on the existence of the device in the filter graph.</span></span>

<span data-ttu-id="fe085-148">L’application ne gère qu’un seul appareil à la fois.</span><span class="sxs-lookup"><span data-stu-id="fe085-148">The application only handles one device at a time.</span></span> <span data-ttu-id="fe085-149">Si l’appareil en cours est supprimé, l’application recherche un autre périphérique DV sur le système.</span><span class="sxs-lookup"><span data-stu-id="fe085-149">If the current device is removed, the application looks for another DV device on the system.</span></span>

<span data-ttu-id="fe085-150">Sur certains caméscopes DV, l’utilisateur doit éteindre l’appareil lors de son basculement entre le mode caméra et le mode VTR, ce qui déclenche un message de perte d’appareil.</span><span class="sxs-lookup"><span data-stu-id="fe085-150">On some DV camcorders, the user must shut off the device when switching it between camera mode and VTR mode, which triggers a device-lost message.</span></span> <span data-ttu-id="fe085-151">L’application répond en activant ou désactivant les commandes de menu appropriées.</span><span class="sxs-lookup"><span data-stu-id="fe085-151">The application responds by enabling or disabling the appropriate menu commands.</span></span> <span data-ttu-id="fe085-152">Toutefois, si l’utilisateur bascule rapidement entre les modes, il se peut que le caméscope ne génère pas de message de perte d’appareil.</span><span class="sxs-lookup"><span data-stu-id="fe085-152">However, if the user toggles rapidly between modes, the camcorder might not generate a device-lost message.</span></span> <span data-ttu-id="fe085-153">Vous pouvez forcer la mise à jour des menus en choisissant le **mode d’actualisation** dans le menu **options** .</span><span class="sxs-lookup"><span data-stu-id="fe085-153">You can force the menus to update by choosing **Refresh Mode** from the **Options** menu.</span></span> <span data-ttu-id="fe085-154">Certains caméscopes DV peuvent basculer les modes sans éteindre l’appareil, mais envoyer un message perdu uniquement quand ils basculent en mode VTR.</span><span class="sxs-lookup"><span data-stu-id="fe085-154">Some DV camcorders can toggle modes without shutting off, but send a device-lost message only when they switch to VTR mode.</span></span>

### <a name="device-control"></a><span data-ttu-id="fe085-155">Contrôle de l’appareil</span><span class="sxs-lookup"><span data-stu-id="fe085-155">Device Control</span></span>

<span data-ttu-id="fe085-156">La fonctionnalité du bouton **lire** et **Enregistrer** dépend du mode actuel :</span><span class="sxs-lookup"><span data-stu-id="fe085-156">The functionality of the **Play** and **Record** button depends on the current mode:</span></span>

-   <span data-ttu-id="fe085-157">Aperçu : le graphique de filtre s’exécute automatiquement.</span><span class="sxs-lookup"><span data-stu-id="fe085-157">Preview: The filter graph runs automatically.</span></span> <span data-ttu-id="fe085-158">Le bouton de **lecture** démarre le transport.</span><span class="sxs-lookup"><span data-stu-id="fe085-158">The **Play** button starts the transport.</span></span>
-   <span data-ttu-id="fe085-159">Capturer dans un fichier : le bouton d' **enregistrement** exécute le graphique et le bouton de **lecture** démarre le transport.</span><span class="sxs-lookup"><span data-stu-id="fe085-159">Capture to file: The **Record** button runs the graph, and the **Play** button starts the transport.</span></span>
-   <span data-ttu-id="fe085-160">Transmettre à l’appareil : le bouton de **lecture** exécute le graphique et le bouton d' **enregistrement** démarre le transport.</span><span class="sxs-lookup"><span data-stu-id="fe085-160">Transmit to device: The **Play** button runs the graph, and the **Record** button starts the transport.</span></span>

<span data-ttu-id="fe085-161">L’exemple d’application n’effectue pas de capture de précision de trame.</span><span class="sxs-lookup"><span data-stu-id="fe085-161">The sample application does not perform frame-accurate capture.</span></span> <span data-ttu-id="fe085-162">À différents moments, l’application appelle la fonction **Sleep** pour attendre que l’appareil réponde.</span><span class="sxs-lookup"><span data-stu-id="fe085-162">At various points, the application calls the **Sleep** function to wait for the device to respond.</span></span> <span data-ttu-id="fe085-163">Les nouveaux caméscopes DV envoient une notification lorsque l’état de l’appareil change.</span><span class="sxs-lookup"><span data-stu-id="fe085-163">Newer DV camcorders send a notification when the state of the device changes.</span></span> <span data-ttu-id="fe085-164">Les appareils plus anciens peuvent ne pas prendre en charge la notification. dans le cadre d’un exemple, l’appel de **Sleep** est une solution plus simple.</span><span class="sxs-lookup"><span data-stu-id="fe085-164">Older devices might not support notification; for the purposes of a sample, calling **Sleep** is a simpler solution.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="fe085-165">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="fe085-165">Downloading the Sample</span></span>

<span data-ttu-id="fe085-166">Pour télécharger les exemples du kit de développement logiciel (SDK) DirectShow, installez la dernière version du [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="fe085-166">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="fe085-167">Cet exemple est installé sous le chemin d’accès suivant : exemples *\[ racine \] du kit de développement logiciel (SDK)* \\ \\ \\ \\ capture DirectShow \\ DVApp.</span><span class="sxs-lookup"><span data-stu-id="fe085-167">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Capture\\DVApp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fe085-168">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fe085-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe085-169">Contrôle d’un caméscope DV</span><span class="sxs-lookup"><span data-stu-id="fe085-169">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> <dt>

[<span data-ttu-id="fe085-170">Vidéo numérique dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="fe085-170">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="fe085-171">Exemples DirectShow</span><span class="sxs-lookup"><span data-stu-id="fe085-171">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



