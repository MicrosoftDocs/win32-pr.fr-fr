---
title: Utilisation de l’exemple d’application de bureau
description: Utilisation de l’exemple d’application de bureau
ms.assetid: 5e3e5283-9e27-4f6a-93a9-84d84f2e875a
keywords:
- Gestionnaire de périphériques Windows Media, exemples
- Gestionnaire de périphériques, exemples
- applications de bureau, exemples
- Windows Media Gestionnaire de périphériques, exemple d’application de bureau
- Gestionnaire de périphériques, exemple d’application de bureau
- exemples, applications de bureau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd511ea5241f458d2cd926dc8fb2f3681757ff8b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672030"
---
# <a name="using-the-sample-desktop-application"></a><span data-ttu-id="ed5ac-109">Utilisation de l’exemple d’application de bureau</span><span class="sxs-lookup"><span data-stu-id="ed5ac-109">Using the Sample Desktop Application</span></span>

<span data-ttu-id="ed5ac-110">L’exemple d’application de bureau est une fenêtre de base à deux volets qui ressemble un peu à l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="ed5ac-110">The sample desktop application is a basic two-paned window somewhat like Windows Explorer.</span></span> <span data-ttu-id="ed5ac-111">Elle vous permet de parcourir le contenu d’un appareil à l’aide d’un affichage en arborescence des dossiers dans le volet gauche et des fichiers dans le volet droit.</span><span class="sxs-lookup"><span data-stu-id="ed5ac-111">It allows you to browse the contents of a device, using a tree view display of folders in the left pane, and files in the right pane.</span></span> <span data-ttu-id="ed5ac-112">La racine de chaque arborescence de dossiers est considérée logiquement comme un appareil différent, bien que certains appareils puissent se représenter comme plusieurs objets (un pour chaque stockage racine).</span><span class="sxs-lookup"><span data-stu-id="ed5ac-112">The root of each folder tree is logically considered a different device, although some devices might represent themselves as several objects (one for each root storage).</span></span> <span data-ttu-id="ed5ac-113">Pour lire les propriétés de base d’un dossier ou d’un fichier, cliquez avec le bouton droit sur l’objet et sélectionnez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="ed5ac-113">To read the basic properties of either a folder or a file, right-click the object and select **Properties**.</span></span>

<span data-ttu-id="ed5ac-114">Vous pouvez supprimer des fichiers sur l’appareil en sélectionnant un fichier dans le volet droit et en sélectionnant **supprimer** dans le menu **fichier** .</span><span class="sxs-lookup"><span data-stu-id="ed5ac-114">You can delete files on the device by selecting a file in the right pane and selecting **Delete** on the **File** menu.</span></span> <span data-ttu-id="ed5ac-115">Pour ajouter des fichiers multimédias à l’appareil, vous pouvez faire glisser des fichiers du bureau vers le volet droit du programme.</span><span class="sxs-lookup"><span data-stu-id="ed5ac-115">To add media files to the device, you can drag files from the desktop onto the right pane of the program.</span></span> <span data-ttu-id="ed5ac-116">Notez que les fichiers doivent être d’un format de média pris en charge par l’appareil. les fichiers de formats inacceptables (fichiers non multimédias, tels que les fichiers. txt ou les formats de média non pris en charge par l’appareil) ne sont pas envoyés à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ed5ac-116">Note that files must be of a media format supported by the device; files of unacceptable formats (non-media files such as .txt files, or media formats not supported by the device) will not be sent to the device.</span></span> <span data-ttu-id="ed5ac-117">(Notez que cette restriction est le programme ; Windows Media Gestionnaire de périphériques vous permet d’envoyer n’importe quel fichier à un appareil s’il est accepté par l’appareil.)</span><span class="sxs-lookup"><span data-stu-id="ed5ac-117">(Note that this restriction is the program's; Windows Media Device Manager enables you to send any file to a device if the device will accept it.)</span></span>

<span data-ttu-id="ed5ac-118">Pour capturer les événements de rappel envoyés à l’interface [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation) , vous devez activer l’option « utiliser l’interface de l’opération » dans le menu **options** .</span><span class="sxs-lookup"><span data-stu-id="ed5ac-118">To capture callback events sent to the [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation) interface, you must check the "Use Operation Interface" option in the **Options** menu.</span></span>

<span data-ttu-id="ed5ac-119">Le menu **options** vous permet également de choisir s’il faut utiliser plusieurs interfaces plus avancées avec les fonctionnalités prises en charge par les appareils avancés.</span><span class="sxs-lookup"><span data-stu-id="ed5ac-119">The **Options** menu also enables you to choose whether to use several more advanced interfaces with features supported by advanced devices.</span></span>

<span data-ttu-id="ed5ac-120">Le menu **conteneurs** contient des options pour vous permettre de créer une sélection ou un album.</span><span class="sxs-lookup"><span data-stu-id="ed5ac-120">The **Containers** menu has options to allow you to create a playlist or an album.</span></span> <span data-ttu-id="ed5ac-121">Pour créer une sélection, sélectionnez une ou plusieurs chansons sur l’appareil, puis cliquez sur **créer une sélection** dans le menu **conteneurs** .</span><span class="sxs-lookup"><span data-stu-id="ed5ac-121">To create a playlist, select one or more songs on the device and click **Create Playlist** on the **Containers** menu.</span></span> <span data-ttu-id="ed5ac-122">Cette fonctionnalité fonctionne uniquement sur les appareils MTP, car le code ne prend en charge que la création d’un fichier de sélection « virtuel ».</span><span class="sxs-lookup"><span data-stu-id="ed5ac-122">This feature only works on MTP devices, because the code only supports the creation of an "virtual" playlist file.</span></span> <span data-ttu-id="ed5ac-123">(Une sélection virtuelle est une sélection spécifiée uniquement par des valeurs de métadonnées, plutôt que par un fichier physique, par exemple un fichier WPL.) L’appareil doit prendre en charge les sélections vides pour utiliser cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="ed5ac-123">(A virtual playlist is a playlist that is specified only by metadata values, rather than by a physical file, for example a WPL file.) The device must support empty playlists to use this feature.</span></span>

<span data-ttu-id="ed5ac-124">Pour créer un album (une sélection avec une image associée), sélectionnez une ou plusieurs chansons sur l’appareil, puis cliquez sur **créer un album** dans le menu **conteneurs** .</span><span class="sxs-lookup"><span data-stu-id="ed5ac-124">To create an album (a playlist with an associated image), select one or more songs on the device and click **Create Album** on the **Containers** menu.</span></span> <span data-ttu-id="ed5ac-125">Une boîte de dialogue vous permet d’accéder à un fichier image sur votre ordinateur pour l’associer à l’album.</span><span class="sxs-lookup"><span data-stu-id="ed5ac-125">A dialog box allows you to browse to a picture file on your computer to associate with the album.</span></span> <span data-ttu-id="ed5ac-126">De même que pour créer des sélections, l’application crée un fichier d’album « vide ». Si l’appareil ne prend pas en charge les albums vides, cette fonctionnalité ne fonctionnera pas.</span><span class="sxs-lookup"><span data-stu-id="ed5ac-126">Similarly to the way it creates playlists, the application creates an "empty" album file; if the device does not support empty albums, this feature will not work.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ed5ac-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ed5ac-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed5ac-128">**Exemple d’application de bureau**</span><span class="sxs-lookup"><span data-stu-id="ed5ac-128">**Sample Desktop Application**</span></span>](sample-desktop-application.md)
</dt> </dl>

 

 




