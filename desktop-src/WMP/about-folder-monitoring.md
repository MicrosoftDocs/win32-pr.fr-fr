---
title: À propos de la surveillance des dossiers
description: À propos de la surveillance des dossiers
ms.assetid: d3d83e60-ecc7-4501-a6dd-15f7680a6ec9
keywords:
- Windows Media Player, surveillance des dossiers
- Windows Media Player Object Model, surveillance des dossiers
- modèle objet, surveillance des dossiers
- Contrôle ActiveX du lecteur Windows Media, surveillance des dossiers
- Contrôle ActiveX, surveillance des dossiers
- Contrôle ActiveX mobile du lecteur Windows Media, surveillance des dossiers
- Windows Media Player Mobile, surveillance des dossiers
- surveillance des dossiers
- dossiers d’analyse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c3d6af341df706cd85c4158197b27babad09c86
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104381468"
---
# <a name="about-folder-monitoring"></a><span data-ttu-id="6a375-112">À propos de la surveillance des dossiers</span><span class="sxs-lookup"><span data-stu-id="6a375-112">About Folder Monitoring</span></span>

<span data-ttu-id="6a375-113">Le lecteur Windows Media peut surveiller les dossiers qui contiennent des fichiers multimédias numériques et mettre à jour la bibliothèque lorsque des fichiers sont ajoutés ou supprimés.</span><span class="sxs-lookup"><span data-stu-id="6a375-113">Windows Media Player can monitor folders that contain digital media files and update the library when files are added or removed.</span></span> <span data-ttu-id="6a375-114">Cette fonctionnalité d’analyse des dossiers est fournie par l’interface [IWMPFolderMonitorServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices) .</span><span class="sxs-lookup"><span data-stu-id="6a375-114">This folder monitoring functionality is provided by the [IWMPFolderMonitorServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices) interface.</span></span>

<span data-ttu-id="6a375-115">Pour utiliser les services de surveillance des dossiers, vous devez créer l’objet lecteur dans un État distant.</span><span class="sxs-lookup"><span data-stu-id="6a375-115">To use the folder monitoring services, you must create the Player object in a remote state.</span></span> <span data-ttu-id="6a375-116">Pour plus d’informations sur la communication à distance, consultez [communication à distance avec le contrôle du lecteur Windows Media](remoting-the-windows-media-player-control.md).</span><span class="sxs-lookup"><span data-stu-id="6a375-116">For more information about remoting, see [Remoting the Windows Media Player Control](remoting-the-windows-media-player-control.md).</span></span> <span data-ttu-id="6a375-117">Après avoir créé une instance distante du lecteur, obtenez un pointeur vers l’interface **IWMPFolderMonitorServices** en appelant **QueryInterface** sur l’interface [IWMPPlayer](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer) .</span><span class="sxs-lookup"><span data-stu-id="6a375-117">After you have created a remoted instance of the player, obtain a pointer to the **IWMPFolderMonitorServices** interface by calling **QueryInterface** on the [IWMPPlayer](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer) interface.</span></span>

<span data-ttu-id="6a375-118">Le lecteur Windows Media conserve une liste des dossiers en cours d’analyse.</span><span class="sxs-lookup"><span data-stu-id="6a375-118">Windows Media Player keeps a list of folders that are being monitored.</span></span> <span data-ttu-id="6a375-119">Pour obtenir la liste des dossiers analysés, utilisez les méthodes [IWMPFolderMonitorServices :: obtenir \_ Count](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_count) et [IWMPFolderMonitorServices :: Item](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-item) .</span><span class="sxs-lookup"><span data-stu-id="6a375-119">To get a list of monitored folders, use the [IWMPFolderMonitorServices::get\_count](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_count) and [IWMPFolderMonitorServices::item](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-item) methods.</span></span> <span data-ttu-id="6a375-120">Pour ajouter des dossiers à la liste ou les supprimer de la liste, utilisez respectivement les méthodes [IWMPFolderMonitorServices :: Add](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-add) et [Remove](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-remove) .</span><span class="sxs-lookup"><span data-stu-id="6a375-120">To add folders to the list or remove them from the list, use the [IWMPFolderMonitorServices::add](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-add) and [remove](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-remove) methods, respectively.</span></span>

<span data-ttu-id="6a375-121">**Démarrage d’une analyse**</span><span class="sxs-lookup"><span data-stu-id="6a375-121">**Starting a Scan**</span></span>

<span data-ttu-id="6a375-122">L’analyse des dossiers est normalement un processus en arrière-plan qui n’a pas besoin d’être appelé explicitement.</span><span class="sxs-lookup"><span data-stu-id="6a375-122">Monitoring of folders is normally a background process that does not need to be called explicitly.</span></span> <span data-ttu-id="6a375-123">Si vous souhaitez analyser activement un dossier, appelez [IWMPFolderMonitorServices :: startScan](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-startscan).</span><span class="sxs-lookup"><span data-stu-id="6a375-123">If you want to actively scan a folder, call [IWMPFolderMonitorServices::startScan](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-startscan).</span></span> <span data-ttu-id="6a375-124">Vous pouvez arrêter une analyse en cours à l’aide de la méthode [IWMPFolderMonitorServices :: stopScan](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-stopscan) .</span><span class="sxs-lookup"><span data-stu-id="6a375-124">You can stop a scan in progress with the [IWMPFolderMonitorServices::stopScan](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-stopscan) method.</span></span>

<span data-ttu-id="6a375-125">**Récupération de l’état d’analyse des dossiers**</span><span class="sxs-lookup"><span data-stu-id="6a375-125">**Retrieving the Folder Monitoring Status**</span></span>

<span data-ttu-id="6a375-126">**IWMPFolderMonitorServices** fournit des fonctionnalités permettant de récupérer l’état du processus de surveillance du dossier.</span><span class="sxs-lookup"><span data-stu-id="6a375-126">**IWMPFolderMonitorServices** provides functionality for retrieving the status of the folder monitoring process.</span></span>

<span data-ttu-id="6a375-127">L’analyse des dossiers est effectuée en deux étapes.</span><span class="sxs-lookup"><span data-stu-id="6a375-127">Folder scanning is done in two passes.</span></span> <span data-ttu-id="6a375-128">Lors du premier passage, le lecteur analyse les dossiers nommés un par un dans la liste des dossiers analysés et génère une liste de fichiers à ajouter à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="6a375-128">In the first pass, the Player scans the folders named in the monitored folders list one by one and builds a list of files to be added to the library.</span></span> <span data-ttu-id="6a375-129">Au cours de la deuxième passe, il parcourt la liste des fichiers et ajoute les fichiers à la bibliothèque, et supprime également tous les éléments multimédias de la bibliothèque dont les fichiers physiques correspondants ont été supprimés du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="6a375-129">In the second pass, it goes through the list of files and adds the files to the library, and also removes any media items from the library whose corresponding physical files have been deleted from the file system.</span></span>

<span data-ttu-id="6a375-130">L’événement [FolderScanStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-folderscanstatechange) est utilisé pour notifier votre programme chaque fois que le lecteur passe à un nouvel État.</span><span class="sxs-lookup"><span data-stu-id="6a375-130">The [FolderScanStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-folderscanstatechange) event is used to notify your program whenever the Player switches to a new state.</span></span> <span data-ttu-id="6a375-131">Vous pouvez également récupérer l’état actuel en appelant la [récupération \_ scanState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_scanstate).</span><span class="sxs-lookup"><span data-stu-id="6a375-131">You can also retrieve the current state by calling [get\_scanState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_scanstate).</span></span> <span data-ttu-id="6a375-132">Lors du démarrage de la première passe, la valeur de l’état actuel est wmpfssScanning.</span><span class="sxs-lookup"><span data-stu-id="6a375-132">When the first pass starts, the current state value is wmpfssScanning.</span></span> <span data-ttu-id="6a375-133">Pendant la deuxième passe, l’état passe à wmpfssUpdating.</span><span class="sxs-lookup"><span data-stu-id="6a375-133">During the second pass, the state switches to wmpfssUpdating.</span></span> <span data-ttu-id="6a375-134">Une fois le processus terminé, l’état passe à wmpfssStopped.</span><span class="sxs-lookup"><span data-stu-id="6a375-134">After the process is finished, the state changes to wmpfssStopped.</span></span>

<span data-ttu-id="6a375-135">Pendant que le lecteur analyse les dossiers analysés lors de la première passe, appelez la méthode [obtenir \_ scannedFilesCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_scannedfilescount) pour vérifier le nombre de fichiers analysés.</span><span class="sxs-lookup"><span data-stu-id="6a375-135">While the Player is scanning the monitored folders on the first pass, call [get\_scannedFilesCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_scannedfilescount) to check how many files have been scanned.</span></span> <span data-ttu-id="6a375-136">La méthode [Obtient \_ currentFolder](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_currentfolder) vous indique quel dossier est actuellement en cours d’analyse.</span><span class="sxs-lookup"><span data-stu-id="6a375-136">The [get\_currentFolder](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_currentfolder) method will tell you which folder is currently being scanned.</span></span>

<span data-ttu-id="6a375-137">Après le démarrage de la deuxième passe, appelez la méthode [obtenir \_ addedFilesCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_addedfilescount) pour vérifier le nombre de fichiers qui ont été ajoutés à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="6a375-137">After the second pass starts, call [get\_addedFilesCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_addedfilescount) to check how many files have been added to the library.</span></span> <span data-ttu-id="6a375-138">La méthode [obtenir \_ UpdateProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_updateprogress) vous indiquera la progression de la deuxième passe, sous la forme d’un pourcentage compris entre 0 et 100.</span><span class="sxs-lookup"><span data-stu-id="6a375-138">The [get\_updateProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_updateprogress) method will tell you the progress of the second pass, as a percentage from 0 to 100.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6a375-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6a375-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a375-140">**À propos du modèle objet Player**</span><span class="sxs-lookup"><span data-stu-id="6a375-140">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> <dt>

[<span data-ttu-id="6a375-141">**Interface IWMPFolderMonitorServices**</span><span class="sxs-lookup"><span data-stu-id="6a375-141">**IWMPFolderMonitorServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)
</dt> </dl>

 

 




