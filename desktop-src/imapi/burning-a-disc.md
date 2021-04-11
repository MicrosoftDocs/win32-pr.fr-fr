---
title: Gravure d’une image de disque
description: 'La maîtrise (gravure d’un disque) à l’aide d’IMAPi se compose des étapes suivantes : créer une image de système de fichiers qui contient les répertoires et les fichiers pour écrire le disque. Configurez un enregistreur de disque pour communiquer avec le périphérique optique. Créez un enregistreur de données et gravez l’image sur le disque.'
ms.assetid: f2eee14e-695d-4678-b3c1-b521ab4d4a7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e3086f728ca0b0826a001d26841edcfe07c6a1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314922"
---
# <a name="burning-a-disc-image"></a><span data-ttu-id="2b6f7-103">Gravure d’une image de disque</span><span class="sxs-lookup"><span data-stu-id="2b6f7-103">Burning a Disc Image</span></span>

<span data-ttu-id="2b6f7-104">La maîtrise (gravure d’un disque) à l’aide d’IMAPi comprend les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="2b6f7-104">Mastering (burning a disc) using IMAPI consists of the following steps:</span></span>

1.  <span data-ttu-id="2b6f7-105">Construisez une image de système de fichiers qui contient les répertoires et les fichiers pour écrire le disque.</span><span class="sxs-lookup"><span data-stu-id="2b6f7-105">Construct a file system image that contains the directories and files to write disc.</span></span>
2.  <span data-ttu-id="2b6f7-106">[Configurez un enregistreur de disque](#set-up-a-disc-recorder) pour communiquer avec le périphérique optique.</span><span class="sxs-lookup"><span data-stu-id="2b6f7-106">[Set up a disc recorder](#set-up-a-disc-recorder) to communicate with the optical device.</span></span>
3.  <span data-ttu-id="2b6f7-107">[Créez un enregistreur de données](#create-a-data-writer-and-write-the-burn-image) et gravez l’image sur le disque.</span><span class="sxs-lookup"><span data-stu-id="2b6f7-107">[Create a data writer](#create-a-data-writer-and-write-the-burn-image) and burn the image to disc.</span></span>

<span data-ttu-id="2b6f7-108">Pour obtenir un exemple qui grave une image disque, consultez l' [exemple VBScript](#vbscript-example).</span><span class="sxs-lookup"><span data-stu-id="2b6f7-108">For an example that burns a disc image, see [VBScript example](#vbscript-example).</span></span>

## <a name="construct-a-burn-image"></a><span data-ttu-id="2b6f7-109">Construire une image de gravure</span><span class="sxs-lookup"><span data-stu-id="2b6f7-109">Construct a burn image</span></span>

<span data-ttu-id="2b6f7-110">Une image de gravure est un flux de données qui est prêt à être écrit sur un support optique.</span><span class="sxs-lookup"><span data-stu-id="2b6f7-110">A burn image is a data stream that is ready to be written to optical media.</span></span> <span data-ttu-id="2b6f7-111">L’image de gravure pour les formats ISO9660, Joliet et UDF se compose d’un système de fichiers de fichiers et de répertoires individuels.</span><span class="sxs-lookup"><span data-stu-id="2b6f7-111">The burn image for ISO9660, Joliet and UDF formats consists of a file system of individual files and directories.</span></span> <span data-ttu-id="2b6f7-112">L’objet **CFileSystemImage** est l’objet de système de fichiers qui contient les fichiers et les répertoires à placer sur le média optique.</span><span class="sxs-lookup"><span data-stu-id="2b6f7-112">The **CFileSystemImage** object is the file system object that holds the files and directories to place on the optical media.</span></span> <span data-ttu-id="2b6f7-113">L’interface [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) fournit l’accès à l’objet et aux paramètres du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="2b6f7-113">The [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) interface provides access to the file system object and settings.</span></span>

<span data-ttu-id="2b6f7-114">Après avoir créé l’objet de système de fichiers, appelez les méthodes [**IFileSystemImage :: CreateFileItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createfileitem) et [**IFileSystemImage :: CreateDirectoryItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createdirectoryitem) pour créer respectivement les objets de fichier et de répertoire.</span><span class="sxs-lookup"><span data-stu-id="2b6f7-114">After creating the file system object, call the [**IFileSystemImage::CreateFileItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createfileitem) and [**IFileSystemImage::CreateDirectoryItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createdirectoryitem) methods to create the file and directory objects, respectively.</span></span> <span data-ttu-id="2b6f7-115">Les objets de fichier et de répertoire peuvent être utilisés pour fournir des détails spécifiques sur le fichier et le répertoire.</span><span class="sxs-lookup"><span data-stu-id="2b6f7-115">The file and directory objects can be used to provide specific details about the file and directory.</span></span> <span data-ttu-id="2b6f7-116">Les méthodes de gestionnaire d’événements disponibles pour [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) peuvent identifier le fichier en cours d’ajout à l’image du système de fichiers, le nombre de secteurs déjà copiés et le nombre total de secteurs à copier.</span><span class="sxs-lookup"><span data-stu-id="2b6f7-116">The event handler methods available for [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) can identify the current file being added to the file system image, the number of sectors already copied, and the total number of sectors to be copied.</span></span>

<span data-ttu-id="2b6f7-117">Si vous le souhaitez, une image de démarrage peut être attachée au système de fichiers à l’aide de la propriété [**IFileSystemImage ::p ut \_ BootImageOptions**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_bootimageoptions) .</span><span class="sxs-lookup"><span data-stu-id="2b6f7-117">Optionally, a boot image can be attached to the file system using the [**IFileSystemImage::put\_BootImageOptions**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_bootimageoptions) property.</span></span> <span data-ttu-id="2b6f7-118">Pour obtenir un exemple, consultez [Ajout d’une image de démarrage](adding-a-boot-image.md).</span><span class="sxs-lookup"><span data-stu-id="2b6f7-118">For an example, see [Adding a Boot Image](adding-a-boot-image.md).</span></span>

<span data-ttu-id="2b6f7-119">Enfin, appelez [**IFileSystemImage :: CreateResultImage**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createresultimage) pour créer un flux de données et fournir l’accès via [**IFileSystemImageResult**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult).</span><span class="sxs-lookup"><span data-stu-id="2b6f7-119">Finally, call [**IFileSystemImage::CreateResultImage**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createresultimage) to create a data stream and provides access through [**IFileSystemImageResult**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult).</span></span> <span data-ttu-id="2b6f7-120">Le nouveau flux de données peut ensuite être fourni directement à la méthode [**IDiscFormat2Data :: Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) ou être enregistré dans un fichier pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="2b6f7-120">The new data stream can then be provided directly to the [**IDiscFormat2Data::Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) method or be saved to a file for later use.</span></span>

## <a name="set-up-a-disc-recorder"></a><span data-ttu-id="2b6f7-121">Configurer un enregistreur de disque</span><span class="sxs-lookup"><span data-stu-id="2b6f7-121">Set up a disc recorder</span></span>

<span data-ttu-id="2b6f7-122">L’objet **MsftDiscMaster2** fournit une énumération des périphériques optiques sur le système.</span><span class="sxs-lookup"><span data-stu-id="2b6f7-122">The **MsftDiscMaster2** object provides an enumeration of the optical devices on the system.</span></span> <span data-ttu-id="2b6f7-123">L’interface [**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2) fournit l’accès à l’énumération d’appareils résultante.</span><span class="sxs-lookup"><span data-stu-id="2b6f7-123">The [**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2) interface provides access to the resultant device enumeration.</span></span> <span data-ttu-id="2b6f7-124">Parcourez les énumérations pour localiser un appareil d’enregistrement approprié.</span><span class="sxs-lookup"><span data-stu-id="2b6f7-124">Traverse the enumerations to locate an appropriate recording device.</span></span> <span data-ttu-id="2b6f7-125">L’objet **MsftDiscMaster2** fournit également des notifications d’événements lors de l’ajout ou de la suppression d’appareils optiques sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="2b6f7-125">The **MsftDiscMaster2** object also provides event notifications when optical devices are added to or deleted from a computer.</span></span>

<span data-ttu-id="2b6f7-126">Après avoir trouvé un enregistreur optique et avoir récupéré son ID, créez un objet **MsftDiscRecorder2** et initialisez l’enregistreur à l’aide de l’ID de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2b6f7-126">After finding an optical recorder and retrieving its ID, create an **MsftDiscRecorder2** object and initialize the recorder using the device ID.</span></span> <span data-ttu-id="2b6f7-127">L’interface [**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2) fournit l’accès à l’objet enregistreur, ainsi que des informations de base sur l’appareil, telles que l’ID du fournisseur, l’ID du produit, la révision du produit et les méthodes permettant d’éjecter le support et de fermer la barre d’État.</span><span class="sxs-lookup"><span data-stu-id="2b6f7-127">The [**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2) interface provides access to the recorder object as well as some basic device information such as vendor ID, product ID, product revision, and methods to eject the media and close the tray.</span></span>

## <a name="create-a-data-writer-and-write-the-burn-image"></a><span data-ttu-id="2b6f7-128">Créer un writer de données et écrire l’image de gravure</span><span class="sxs-lookup"><span data-stu-id="2b6f7-128">Create a data writer and write the burn image</span></span>

<span data-ttu-id="2b6f7-129">L’objet **MsftDiscFormat2Data** fournit la méthode d’écriture, les propriétés relatives à la fonction d’écriture et aux propriétés spécifiques au média.</span><span class="sxs-lookup"><span data-stu-id="2b6f7-129">The **MsftDiscFormat2Data** object provides the writing method, the properties about the write function and media-specific properties.</span></span> <span data-ttu-id="2b6f7-130">L’interface [**IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data) fournit l’accès à l’objet **MsftDiscFormat2Data** .</span><span class="sxs-lookup"><span data-stu-id="2b6f7-130">The [**IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data) interface provides access to the **MsftDiscFormat2Data** object.</span></span>

<span data-ttu-id="2b6f7-131">L’enregistreur de disque est lié au writer de format à l’aide de la propriété [**IDiscFormat2Data ::p ut \_ Recorder**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_recorder) .</span><span class="sxs-lookup"><span data-stu-id="2b6f7-131">The disc recorder links to the format writer using the [**IDiscFormat2Data::put\_Recorder**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_recorder) property.</span></span> <span data-ttu-id="2b6f7-132">Une fois que l’enregistreur est lié au writer de format, vous pouvez exécuter des requêtes sur le média et mettre à jour les propriétés spécifiques à l’écriture avant d’écrire l’image de résultat sur le disque à l’aide de la méthode [**IDiscFormat2Data :: Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) .</span><span class="sxs-lookup"><span data-stu-id="2b6f7-132">After the recorder is bound to the format writer, you can perform queries regarding the media and update write-specific properties before writing the result image to disc using the [**IDiscFormat2Data::Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) method.</span></span>

<span data-ttu-id="2b6f7-133">D’autres interfaces d’écriture de format fournies par IMAPi fonctionnent de la même manière. les interfaces d’écriture de format supplémentaires sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="2b6f7-133">Other format writing interfaces provided by IMAPI work similarly; additional format writing interfaces include:</span></span>

-   <span data-ttu-id="2b6f7-134">[**IDiscFormat2Erase**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase) efface les supports optiques réinscriptibles.</span><span class="sxs-lookup"><span data-stu-id="2b6f7-134">[**IDiscFormat2Erase**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase) erases rewritable optical media.</span></span>
-   <span data-ttu-id="2b6f7-135">[**IDiscFormat2RawCD**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd) écrit une image brute sur un support optique.</span><span class="sxs-lookup"><span data-stu-id="2b6f7-135">[**IDiscFormat2RawCD**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd) writes a raw image to optical media.</span></span>
-   <span data-ttu-id="2b6f7-136">[**IDiscFormat2TrackAtOnce**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce) écrit des pistes audio sur un support optique.</span><span class="sxs-lookup"><span data-stu-id="2b6f7-136">[**IDiscFormat2TrackAtOnce**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce) writes audio tracks to optical media.</span></span>

> [!Note]  
> <span data-ttu-id="2b6f7-137">Il est possible qu’une transition de l’état d’alimentation ait lieu pendant une opération de gravure (c’est-à-dire une fermeture de session de l’utilisateur ou une interruption du système), entraînant l’interruption du processus de gravure et une perte de données éventuelle.</span><span class="sxs-lookup"><span data-stu-id="2b6f7-137">It is possible for a power state transition to take place during a burn operation (i.e. user log-off or system suspend) which leads to the interruption of the burn process and possible data loss.</span></span> <span data-ttu-id="2b6f7-138">Pour plus d’informations sur la programmation, consultez [empêcher la déconnexion ou l’interruption pendant une gravure](preventing-logoff-or-suspend-during-a-burn.md).</span><span class="sxs-lookup"><span data-stu-id="2b6f7-138">For programming considerations, see [Preventing Logoff or Suspend During a Burn](preventing-logoff-or-suspend-during-a-burn.md).</span></span>

 

## <a name="vbscript-example"></a><span data-ttu-id="2b6f7-139">Exemple VBScript</span><span class="sxs-lookup"><span data-stu-id="2b6f7-139">VBScript example</span></span>

<span data-ttu-id="2b6f7-140">Cet exemple de script montre comment utiliser les objets IMAPi pour graver un média optique. plus précisément, écrivez un répertoire sur un disque vierge. Le code ne contient pas de vérification des erreurs et suppose les points suivants :</span><span class="sxs-lookup"><span data-stu-id="2b6f7-140">This script example shows how to use the IMAPI objects to burn optical media; more specifically, write a directory to a blank disc. The code contains no error checking, and assumes the following:</span></span>

-   <span data-ttu-id="2b6f7-141">Un périphérique de disque compatible est installé sur le système.</span><span class="sxs-lookup"><span data-stu-id="2b6f7-141">A compatible disc device is installed on the system.</span></span>
-   <span data-ttu-id="2b6f7-142">Le périphérique à disque est le deuxième lecteur du système.</span><span class="sxs-lookup"><span data-stu-id="2b6f7-142">The disc device is the second drive on the system.</span></span>
-   <span data-ttu-id="2b6f7-143">Un disque compatible est inséré dans le périphérique du disque.</span><span class="sxs-lookup"><span data-stu-id="2b6f7-143">A compatible disc is inserted in the disc device.</span></span>
-   <span data-ttu-id="2b6f7-144">Le disque est vide.</span><span class="sxs-lookup"><span data-stu-id="2b6f7-144">The disc is blank.</span></span>
-   <span data-ttu-id="2b6f7-145">Les fichiers à écrire sur le disque se trouvent dans « g : \\ burndir ».</span><span class="sxs-lookup"><span data-stu-id="2b6f7-145">Files to write to disc are located in "g:\\burndir".</span></span>

<span data-ttu-id="2b6f7-146">Des fonctionnalités supplémentaires telles que la vérification des erreurs, la compatibilité des appareils et des supports, la notification d’événements et le calcul de l’espace libre sur le disque peuvent être ajoutées à ce script.</span><span class="sxs-lookup"><span data-stu-id="2b6f7-146">Additional functionality such as error checking, device and media compatibility, event notification, and calculating free space on the disc can be added to this script.</span></span>


```VB
' This script burns data files to disc in a single session 
' using files from a single directory tree.
 
' Copyright (C) Microsoft Corp. 2006

Option Explicit

' *** CD/DVD disc file system types
Const FsiFileSystemISO9660 = 1
Const FsiFileSystemJoliet  = 2
Const FsiFileSystemUDF102  = 4

WScript.Quit(Main)

Function Main
    Dim Index                ' Index to recording drive.
    Dim Recorder             ' Recorder object
    Dim Path                 ' Directory of files to burn
    Dim Stream               ' Data stream for burning device
    
    Index = 1                ' Second drive on the system
    Path = "g:\BurnDir"      ' Files to transfer to disc

    ' Create a DiscMaster2 object to connect to optical drives.
    Dim g_DiscMaster
    Set g_DiscMaster = WScript.CreateObject("IMAPI2.MsftDiscMaster2")

    ' Create a DiscRecorder object for the specified burning device.
    Dim uniqueId
    set recorder = WScript.CreateObject("IMAPI2.MsftDiscRecorder2")
    uniqueId = g_DiscMaster.Item(index)
    recorder.InitializeDiscRecorder( uniqueId )

    ' Create an image stream for a specified directory.
    Dim FSI                  ' Disc file system
    Dim Dir                  ' Root directory of the disc file system
    Dim dataWriter    
        
    ' Create a new file system image and retrieve root directory
    Set FSI = CreateObject("IMAPI2FS.MsftFileSystemImage")
    Set Dir = FSI.Root

    'Create the new disc format and set the recorder
    Set dataWriter = CreateObject ("IMAPI2.MsftDiscFormat2Data")
    dataWriter.recorder = Recorder
    dataWriter.ClientName = "IMAPIv2 TEST"

    FSI.ChooseImageDefaults(recorder)
        
    ' Add the directory and its contents to the file system 
    Dir.AddTree Path, false
        
    ' Create an image from the file system
    Dim result
    Set result = FSI.CreateResultImage()
    Stream = result.ImageStream
    
    ' Write stream to disc using the specified recorder.
    WScript.Echo "Writing content to disc..."
    dataWriter.write(Stream)

    WScript.Echo "----- Finished writing content -----"
    Main = 0
End Function

```



## <a name="related-topics"></a><span data-ttu-id="2b6f7-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2b6f7-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b6f7-148">Utilisation d’IMAPi</span><span class="sxs-lookup"><span data-stu-id="2b6f7-148">Using IMAPI</span></span>](using-imapi.md)
</dt> <dt>

[<span data-ttu-id="2b6f7-149">**IDiscFormat2Data**</span><span class="sxs-lookup"><span data-stu-id="2b6f7-149">**IDiscFormat2Data**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data)
</dt> <dt>

[<span data-ttu-id="2b6f7-150">**IDiscFormat2Erase**</span><span class="sxs-lookup"><span data-stu-id="2b6f7-150">**IDiscFormat2Erase**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase)
</dt> <dt>

[<span data-ttu-id="2b6f7-151">**IDiscFormat2RawCD**</span><span class="sxs-lookup"><span data-stu-id="2b6f7-151">**IDiscFormat2RawCD**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd)
</dt> <dt>

[<span data-ttu-id="2b6f7-152">**IDiscFormat2TrackAtOnce**</span><span class="sxs-lookup"><span data-stu-id="2b6f7-152">**IDiscFormat2TrackAtOnce**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce)
</dt> <dt>

[<span data-ttu-id="2b6f7-153">**IDiscMaster2**</span><span class="sxs-lookup"><span data-stu-id="2b6f7-153">**IDiscMaster2**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2)
</dt> <dt>

[<span data-ttu-id="2b6f7-154">**IDiscRecorder2**</span><span class="sxs-lookup"><span data-stu-id="2b6f7-154">**IDiscRecorder2**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2)
</dt> <dt>

[<span data-ttu-id="2b6f7-155">**IFileSystemImage**</span><span class="sxs-lookup"><span data-stu-id="2b6f7-155">**IFileSystemImage**</span></span>](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage)
</dt> <dt>

[<span data-ttu-id="2b6f7-156">**IStream**</span><span class="sxs-lookup"><span data-stu-id="2b6f7-156">**IStream**</span></span>](/windows/desktop/api/objidl/nn-objidl-istream)
</dt> </dl>

 

 