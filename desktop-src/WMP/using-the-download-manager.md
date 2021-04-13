---
title: Utilisation du gestionnaire de téléchargement
description: Utilisation du gestionnaire de téléchargement
ms.assetid: f332a981-727f-4abc-a84e-76ab3e72b7f2
keywords:
- Windows Media Player Online stores, gestionnaire de téléchargement
- magasins en ligne, gestionnaire de téléchargement
- tapez 2 magasins en ligne, gestionnaire de téléchargement
- Lecteur Windows Media, gestionnaire de téléchargement
- Gestionnaire de téléchargement du lecteur Windows Media
- Gestionnaire de téléchargement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cecb7b99ae36d3881fdf80eaad7d851205b9b2e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380393"
---
# <a name="using-the-download-manager"></a><span data-ttu-id="2255d-109">Utilisation du gestionnaire de téléchargement</span><span class="sxs-lookup"><span data-stu-id="2255d-109">Using the Download Manager</span></span>

<span data-ttu-id="2255d-110">Le kit de développement logiciel (SDK) Windows Media Player comprend un exemple de page Web illustrant l’utilisation du gestionnaire de téléchargement pour télécharger des fichiers sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2255d-110">The Windows Media Player SDK includes a sample webpage that demonstrates using the Download Manager to download files to the user's computer.</span></span> <span data-ttu-id="2255d-111">Vous pouvez localiser l’exemple dans le dossier nommé page Web dans lequel vous avez installé le kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="2255d-111">You can locate the sample in the folder named WebPage where you installed the SDK.</span></span> <span data-ttu-id="2255d-112">Le nom du fichier est Sample. asp.</span><span class="sxs-lookup"><span data-stu-id="2255d-112">The name of the file is sample.asp.</span></span> <span data-ttu-id="2255d-113">L’exemple fournit les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="2255d-113">The sample provides the following functionality:</span></span>

-   <span data-ttu-id="2255d-114">Crée l’objet **downloadmanager** .</span><span class="sxs-lookup"><span data-stu-id="2255d-114">Creates the **DownloadManager** object.</span></span>
-   <span data-ttu-id="2255d-115">Crée un objet **DownloadCollection** .</span><span class="sxs-lookup"><span data-stu-id="2255d-115">Creates a **DownloadCollection** object.</span></span>
-   <span data-ttu-id="2255d-116">Démarre le téléchargement de cinq fichiers lorsque l’utilisateur clique sur **Télécharger**.</span><span class="sxs-lookup"><span data-stu-id="2255d-116">Starts downloading five files when the user clicks **Download**.</span></span> <span data-ttu-id="2255d-117">Les chemins d’accès aux fichiers par défaut sont fournis dans l’exemple.</span><span class="sxs-lookup"><span data-stu-id="2255d-117">Default file paths are provided in the sample.</span></span> <span data-ttu-id="2255d-118">Vous devez remplacer ces chemins par défaut par les emplacements des fichiers sur votre propre serveur.</span><span class="sxs-lookup"><span data-stu-id="2255d-118">You should replace these default paths with the locations of files on your own server.</span></span> <span data-ttu-id="2255d-119">Vous pouvez modifier les chemins d’accès en modifiant les valeurs assignées au tableau global nommé g \_ sFiles.</span><span class="sxs-lookup"><span data-stu-id="2255d-119">You can change the paths by changing the values assigned to the global array named g\_sFiles.</span></span>
-   <span data-ttu-id="2255d-120">Affiche les informations d’état d’un téléchargement lorsque l’utilisateur le sélectionne.</span><span class="sxs-lookup"><span data-stu-id="2255d-120">Shows status information for a download when the user selects it.</span></span>
-   <span data-ttu-id="2255d-121">Fournit des contrôles pour suspendre, reprendre, annuler et supprimer un élément de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="2255d-121">Provides controls to pause, resume, cancel, and remove a download item.</span></span>
-   <span data-ttu-id="2255d-122">Gère les informations relatives aux regroupements de téléchargement entre les sessions à l’aide de cookies.</span><span class="sxs-lookup"><span data-stu-id="2255d-122">Maintains information about download collections between sessions by using cookies.</span></span> <span data-ttu-id="2255d-123">C’est important, car l’utilisateur peut fermer le lecteur à tout moment.</span><span class="sxs-lookup"><span data-stu-id="2255d-123">This is important because the user can close the Player at any time.</span></span> <span data-ttu-id="2255d-124">En outre, si l’utilisateur bascule les volets des tâches dans le lecteur, la session de la Banque en ligne se termine.</span><span class="sxs-lookup"><span data-stu-id="2255d-124">Also, if the user switches task panes in the Player, the online store session ends.</span></span>
-   <span data-ttu-id="2255d-125">Utilise le téléchargement en temps réel par défaut.</span><span class="sxs-lookup"><span data-stu-id="2255d-125">Uses real-time downloading by default.</span></span> <span data-ttu-id="2255d-126">Vous pouvez modifier le comportement du téléchargement en arrière-plan en modifiant la valeur de la variable nommée g \_ sDLType.</span><span class="sxs-lookup"><span data-stu-id="2255d-126">You can change the behavior to background downloading by changing the value of the variable named g\_sDLType.</span></span> <span data-ttu-id="2255d-127">Le téléchargement en arrière-plan peut être utilisé avec le système d’exploitation Microsoft Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2255d-127">Background downloading is available for use with the Microsoft Windows XP operating system.</span></span>
-   <span data-ttu-id="2255d-128">Synchronise la couleur d’arrière-plan avec la couleur du joueur.</span><span class="sxs-lookup"><span data-stu-id="2255d-128">Synchronizes the background color with the Player color.</span></span> <span data-ttu-id="2255d-129">Vous pouvez utiliser cette fonctionnalité pour modifier l’apparence de votre magasin en ligne lorsque l’utilisateur choisit de modifier la couleur du joueur.</span><span class="sxs-lookup"><span data-stu-id="2255d-129">You can use this feature to make your online store change appearance when the user chooses to change the color of the Player.</span></span>

<span data-ttu-id="2255d-130">Les sections suivantes fournissent plus d’informations :</span><span class="sxs-lookup"><span data-stu-id="2255d-130">The following sections provide more information:</span></span>

-   [<span data-ttu-id="2255d-131">Initialisation de la page</span><span class="sxs-lookup"><span data-stu-id="2255d-131">Initializing the Page</span></span>](initializing-the-page.md)
-   [<span data-ttu-id="2255d-132">Démarrage des téléchargements</span><span class="sxs-lookup"><span data-stu-id="2255d-132">Starting the Downloads</span></span>](starting-the-downloads.md)
-   [<span data-ttu-id="2255d-133">Récupération des informations d’État</span><span class="sxs-lookup"><span data-stu-id="2255d-133">Retrieving Status Information</span></span>](retrieving-status-information.md)
-   [<span data-ttu-id="2255d-134">Gestion des informations de session</span><span class="sxs-lookup"><span data-stu-id="2255d-134">Maintaining Session Information</span></span>](maintaining-session-information.md)
-   [<span data-ttu-id="2255d-135">Débogage de la page</span><span class="sxs-lookup"><span data-stu-id="2255d-135">Debugging the Page</span></span>](debugging-the-page.md)

## <a name="related-topics"></a><span data-ttu-id="2255d-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2255d-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2255d-137">**Guide de programmation pour les magasins en ligne de type 2**</span><span class="sxs-lookup"><span data-stu-id="2255d-137">**Programming Guide for Type 2 Online Stores**</span></span>](programming-guide-for-type-2-online-stores.md)
</dt> </dl>

 

 




