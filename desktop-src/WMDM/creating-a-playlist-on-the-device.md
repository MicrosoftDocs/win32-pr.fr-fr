---
title: Création d’une sélection sur l’appareil
description: Création d’une sélection sur l’appareil
ms.assetid: 9f803e1a-ff33-443a-9448-e8c875d77e51
keywords:
- Gestionnaire de périphériques Windows Media, sélections
- Gestionnaire de périphériques, sélections
- Guide de programmation, sélections
- applications de bureau, sélections
- création d’applications Windows Media Gestionnaire de périphériques, de sélections
- sélections abstraites
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c287cc406b795db07fde3f10103822dea32185a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309773"
---
# <a name="creating-a-playlist-on-the-device"></a><span data-ttu-id="85328-109">Création d’une sélection sur l’appareil</span><span class="sxs-lookup"><span data-stu-id="85328-109">Creating a Playlist on the Device</span></span>

<span data-ttu-id="85328-110">Le kit de développement logiciel (SDK) Windows Media Gestionnaire de périphériques permet à une application MTP de créer une sélection sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="85328-110">The Windows Media Device Manager SDK provides the means for an MTP application to create a playlist on a device.</span></span> <span data-ttu-id="85328-111">Ce type de playlist est appelé une sélection *abstraite* , car le fichier créé sur l’appareil ne contient aucune donnée multimédia, mais uniquement les métadonnées qui contiennent les liens vers les fichiers multimédias de la sélection.</span><span class="sxs-lookup"><span data-stu-id="85328-111">This type of playlist is called an *abstract* playlist, because the file created on the device contains no media data, but only metadata, which holds the links to media files in the playlist.</span></span>

<span data-ttu-id="85328-112">Les autres éléments abstraits qui peuvent être créés sur l’appareil incluent les listes de sélection avec des propriétés supplémentaires, telles que les jaquettes, les contacts et les messages.</span><span class="sxs-lookup"><span data-stu-id="85328-112">Other abstract items that can be created on the device include albums (essentially playlists with extra properties such as cover art), contacts, and messages.</span></span>

<span data-ttu-id="85328-113">**Pour créer une sélection**</span><span class="sxs-lookup"><span data-stu-id="85328-113">**To create a playlist**</span></span>

1.  <span data-ttu-id="85328-114">Acquérir une interface [**IWMDMDevice3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice3) sur l’appareil cible.</span><span class="sxs-lookup"><span data-stu-id="85328-114">Acquire an [**IWMDMDevice3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice3) interface to the target device.</span></span>
2.  <span data-ttu-id="85328-115">Appelez [**IWMDMDevice3 :: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) pour obtenir la \_ propriété g wszWMDMFormatsSupported.</span><span class="sxs-lookup"><span data-stu-id="85328-115">Call [**IWMDMDevice3::GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) to obtain the g\_wszWMDMFormatsSupported property.</span></span>
3.  <span data-ttu-id="85328-116">Si aucun format de sélection n’est pris en charge, interdisez l’envoi de playlists à l’appareil et ignorez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="85328-116">If no playlist formats are supported, disallow sending playlists to the device, and skip the following steps.</span></span> <span data-ttu-id="85328-117">Sinon, choisissez le code de format pris en charge par l’appareil qui correspond le mieux au type d’objet souhaité.</span><span class="sxs-lookup"><span data-stu-id="85328-117">Otherwise, choose the device-supported format code that matches most closely the intended object type.</span></span> <span data-ttu-id="85328-118">Les codes de \_ format Generic WMDM FORMATCODE \_ ABSTRACTAUDIOVIDEOPLAYLIST et WMDM \_ FORMATCODE ABSTRACTAUDIOLAYLIST \_ sont les plus couramment pris en charge.</span><span class="sxs-lookup"><span data-stu-id="85328-118">The generic WMDM\_FORMATCODE\_ABSTRACTAUDIOVIDEOPLAYLIST and WMDM\_FORMATCODE\_ABSTRACTAUDIOLAYLIST format codes are the most commonly supported.</span></span>
4.  <span data-ttu-id="85328-119">Obtenez une interface [**IWMDMStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3) pour le stockage (la racine ou un dossier) dans lequel vous souhaitez créer l’objet.</span><span class="sxs-lookup"><span data-stu-id="85328-119">Obtain an [**IWMDMStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3) interface for the storage (the root or a folder) where you want to create the object.</span></span> <span data-ttu-id="85328-120">Certains appareils fonctionnent mieux si l’objet de sélection est placé dans un dossier de niveau supérieur nommé « playlists ».</span><span class="sxs-lookup"><span data-stu-id="85328-120">Some devices work best if the playlist object is placed in a top level folder named "Playlists".</span></span>
5.  <span data-ttu-id="85328-121">Créez un objet de métadonnées vide à l’aide de [**IWMDMStorage3 :: CreateEmptyMetadataObject**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-createemptymetadataobject).</span><span class="sxs-lookup"><span data-stu-id="85328-121">Create an empty metadata object by using [**IWMDMStorage3::CreateEmptyMetadataObject**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-createemptymetadataobject).</span></span>
6.  <span data-ttu-id="85328-122">À l’aide de l’interface **IWMDMMetaData** obtenue à l’étape précédente, appelez [**IWMDMMetaData :: AddItem**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmmetadata-additem) pour ajouter le code de format que vous avez choisi (de l’étape 3) aux propriétés de métadonnées de stockage.</span><span class="sxs-lookup"><span data-stu-id="85328-122">Using the **IWMDMMetaData** interface obtained in the previous step, call [**IWMDMMetaData::AddItem**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmmetadata-additem) to add your chosen format code (from step 3) to the storage metadata properties.</span></span>
7.  <span data-ttu-id="85328-123">Obtenez l’interface [**IWMDMStorageControl3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol3) à partir de l’interface **IWMDMStorage3** .</span><span class="sxs-lookup"><span data-stu-id="85328-123">Obtain the [**IWMDMStorageControl3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol3) interface from the **IWMDMStorage3** interface.</span></span>
8.  <span data-ttu-id="85328-124">Appelez [**IWMDMStorageControl3 :: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) pour insérer un nouveau fichier de sélection dans le stockage sélectionné.</span><span class="sxs-lookup"><span data-stu-id="85328-124">Call [**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) to insert a new playlist file in the selected storage.</span></span> <span data-ttu-id="85328-125">Ce fichier contient les métadonnées représentées par l’interface **IWMDMMetaData** que vous avez créée à l’étape 5 et passée à **Insert3**.</span><span class="sxs-lookup"><span data-stu-id="85328-125">This file contains the metadata represented by the **IWMDMMetaData** interface you created in step 5 and passed to **Insert3**.</span></span> <span data-ttu-id="85328-126">La méthode retourne une interface **IWMDMStorage** pour le fichier de sélection ; vous pouvez interroger l’interface [**IWMDMStorage4**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage4) .</span><span class="sxs-lookup"><span data-stu-id="85328-126">The method returns an **IWMDMStorage** interface for the playlist file; you can query for the [**IWMDMStorage4**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage4) interface.</span></span>
9.  <span data-ttu-id="85328-127">Appelez [**IWMDMStorage4 :: SetReferences**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-setreferences) pour créer des références aux interfaces **IWMDMStorage** des fichiers multimédias de la sélection.</span><span class="sxs-lookup"><span data-stu-id="85328-127">Call [**IWMDMStorage4::SetReferences**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-setreferences) to create references to the **IWMDMStorage** interfaces of the media files in the playlist.</span></span>

<span data-ttu-id="85328-128">Pour obtenir un exemple de code, consultez la \_ fonction OnCreatePlaylist dans l' [exemple d’application de bureau](sample-desktop-application.md).</span><span class="sxs-lookup"><span data-stu-id="85328-128">For example code, see the \_OnCreatePlaylist function in the [Sample Desktop Application](sample-desktop-application.md).</span></span>

> [!Note]  
> <span data-ttu-id="85328-129">Le fournisseur de services MTP fourni par Microsoft permet à une application de définir des références dans les métadonnées.</span><span class="sxs-lookup"><span data-stu-id="85328-129">The Microsoft-provided MTP service provider enables an application to set references in metadata.</span></span> <span data-ttu-id="85328-130">Pour implémenter des sélections, votre application doit communiquer avec un périphérique MTP ou à l’aide d’un fournisseur de services personnalisé capable de gérer des objets abstraits.</span><span class="sxs-lookup"><span data-stu-id="85328-130">To implement playlists, your application must be communicating with an MTP device or using a custom service provider that can handle abstract objects.</span></span> <span data-ttu-id="85328-131">Le fournisseur de services CE gère les objets de sélection et d’album.</span><span class="sxs-lookup"><span data-stu-id="85328-131">The CE service provider handles playlist and album objects.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="85328-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="85328-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85328-133">**Écriture de fichiers sur l’appareil**</span><span class="sxs-lookup"><span data-stu-id="85328-133">**Writing Files to the Device**</span></span>](writing-files-to-the-device.md)
</dt> </dl>

 

 




