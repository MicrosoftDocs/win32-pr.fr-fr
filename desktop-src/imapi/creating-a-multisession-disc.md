---
title: Création d’un disque multisession
ms.assetid: 327304c4-fdb9-47c6-9b19-49100b933590
description: 'En savoir plus sur : création d’un disque multisession'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2db17b8a16f46797fc0f6de2bf94850e3b3039bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485433"
---
# <a name="creating-a-multisession-disc"></a><span data-ttu-id="d064d-103">Création d’un disque multisession</span><span class="sxs-lookup"><span data-stu-id="d064d-103">Creating a Multisession Disc</span></span>

<span data-ttu-id="d064d-104">L' [API de mastérisation d’image](about-imapi.md) (IMAPI) prend en charge l’ajout et la suppression de fichiers dans, ou à partir de, les types de disques multisessions suivants :</span><span class="sxs-lookup"><span data-stu-id="d064d-104">The [Image Mastering API](about-imapi.md) (IMAPI) supports the addition and removal of files to, or from, the following multisession disc types:</span></span>

-   <span data-ttu-id="d064d-105">CD-R/CD-RW</span><span class="sxs-lookup"><span data-stu-id="d064d-105">CD-R/CD-RW</span></span>
-   <span data-ttu-id="d064d-106">Single-Layer DVD + R/DVD-R</span><span class="sxs-lookup"><span data-stu-id="d064d-106">Single-Layer DVD+R/DVD-R</span></span>
-   <span data-ttu-id="d064d-107">DVD + R double couche</span><span class="sxs-lookup"><span data-stu-id="d064d-107">DVD+R Dual Layer</span></span>
-   <span data-ttu-id="d064d-108">BD-R</span><span class="sxs-lookup"><span data-stu-id="d064d-108">BD-R</span></span>
-   <span data-ttu-id="d064d-109">DVD-RW/DVD + RW (**Windows 7 uniquement**)</span><span class="sxs-lookup"><span data-stu-id="d064d-109">DVD-RW/DVD+RW (**Windows 7 Only**)</span></span>
-   <span data-ttu-id="d064d-110">DVD-RAM (**Windows 7 uniquement**)</span><span class="sxs-lookup"><span data-stu-id="d064d-110">DVD-RAM (**Windows 7 Only**)</span></span>
-   <span data-ttu-id="d064d-111">BD-RE (**Windows 7 uniquement**)</span><span class="sxs-lookup"><span data-stu-id="d064d-111">BD-RE (**Windows 7 Only**)</span></span>

<span data-ttu-id="d064d-112">La création d’un disque multisession à l’aide d’IMAPi se compose des étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="d064d-112">Creation of a multisession disc using IMAPI consists of the following steps.</span></span> <span data-ttu-id="d064d-113">Chacune de ces étapes documentées contient la partie appropriée de l’exemple complet de script Visual Basic fourni dans la dernière section.</span><span class="sxs-lookup"><span data-stu-id="d064d-113">Each of these documented steps contains the relevant portion of the complete Visual Basic script example provided in the final section.</span></span>

## <a name="initializing-the-disc-recorder"></a><span data-ttu-id="d064d-114">Initialisation de l’enregistreur de disque</span><span class="sxs-lookup"><span data-stu-id="d064d-114">Initializing the Disc Recorder</span></span>

<span data-ttu-id="d064d-115">Avant l’initialisation de l’appareil, l’objet **MsftDiscMaster2** fournit une énumération des périphériques optiques sur le système.</span><span class="sxs-lookup"><span data-stu-id="d064d-115">Prior to device initialization, the **MsftDiscMaster2** object provides an enumeration of the optical devices on the system.</span></span> <span data-ttu-id="d064d-116">L’interface [**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2) fournit l’accès à cette énumération d’appareils pour faciliter l’emplacement de l’appareil d’enregistrement approprié.</span><span class="sxs-lookup"><span data-stu-id="d064d-116">The [**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2) interface provides access to this device enumeration to facilitate the location of the appropriate recording device.</span></span> <span data-ttu-id="d064d-117">L’objet **MsftDiscMaster2** fournit également des notifications d’événements lors de l’ajout ou de la suppression d’appareils optiques sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="d064d-117">The **MsftDiscMaster2** object also provides event notifications when optical devices are added to or removed from a machine.</span></span>

<span data-ttu-id="d064d-118">Après avoir localisé un enregistreur optique et récupéré l’ID qui lui est affecté, créez un nouvel objet **MsftDiscMaster2** et initialisez l’enregistreur à l’aide de l’ID d’appareil spécifique.</span><span class="sxs-lookup"><span data-stu-id="d064d-118">After locating an optical recorder and retrieving the ID assigned to it, create a new **MsftDiscMaster2** object and initialize the recorder using the specific device ID.</span></span>

<span data-ttu-id="d064d-119">L’interface [**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2) fournit un accès aux informations de base sur l’appareil, telles que l’ID de fournisseur, l’ID de produit, la révision de produit, ainsi que les méthodes permettant d’éjecter un support ou de fermer la barre d’État.</span><span class="sxs-lookup"><span data-stu-id="d064d-119">The [**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2) interface provides access to basic device information such as vendor ID, product ID, product revision, as well as the methods to eject media or close the tray.</span></span>

> [!Note]  
> <span data-ttu-id="d064d-120">Les constantes et dimensions supplémentaires déclarées dans l’exemple suivant sont utilisées ultérieurement dans l’exemple de script complet situé dans la dernière section de ce document.</span><span class="sxs-lookup"><span data-stu-id="d064d-120">The additional constants and dimensions declared in the following sample are used later in the complete sample script located in the final section of this document.</span></span> <span data-ttu-id="d064d-121">Ces éléments ne sont pas requis pour l’initialisation d’un enregistreur de disque.</span><span class="sxs-lookup"><span data-stu-id="d064d-121">These elements are not required for the act of initializing a disc recorder.</span></span>

 


```VB
' **_ CD/DVD disc file system types
Const FsiFileSystemISO9660 = 1
Const FsiFileSystemJoliet  = 2
Const FsiFileSystemUDF102  = 4

WScript.Quit(Main)

Function Main
    Dim Index                ' Index to recording drive.
    Dim Recorder             ' Recorder object
    Dim Path                 ' Directory of files to add
    Dim Stream               ' Data stream for burning device
    
    Index = 0                ' First drive on the system
    Path = "G:\BurnDir"      ' Files to add to the disc

    ' Create a DiscMaster2 object to connect to optical drives.
    Dim DiscMaster
    Set DiscMaster = WScript.CreateObject("IMAPI2.MsftDiscMaster2")

    ' Create a DiscRecorder2 object for the specified burning device.
    Dim UniqueId
    set Recorder = WScript.CreateObject("IMAPI2.MsftDiscRecorder2")
    UniqueId = DiscMaster.Item(Index)
    Recorder.InitializeDiscRecorder(UniqueId)
```



## <a name="creating-a-data-writer"></a><span data-ttu-id="d064d-122">Création d’un enregistreur de données</span><span class="sxs-lookup"><span data-stu-id="d064d-122">Creating a Data Writer</span></span>

<span data-ttu-id="d064d-123">L’objet _ *MsftDiscFormat2Data*\* fournit la méthode d’écriture, ses propriétés, ainsi que les propriétés spécifiques au média.</span><span class="sxs-lookup"><span data-stu-id="d064d-123">The _ *MsftDiscFormat2Data*\* object provides the writing method, its properties, as well as the media-specific properties.</span></span> <span data-ttu-id="d064d-124">L’interface [**IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data) fournit l’accès à cet objet.</span><span class="sxs-lookup"><span data-stu-id="d064d-124">The [**IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data) interface provides access to this object.</span></span>

<span data-ttu-id="d064d-125">L’enregistreur de disque est lié au writer de format à l’aide de la propriété [**IDiscFormat2Data ::p ut \_ Recorder**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_recorder) .</span><span class="sxs-lookup"><span data-stu-id="d064d-125">The disc recorder binds to the format writer using the [**IDiscFormat2Data::put\_Recorder**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_recorder) property.</span></span> <span data-ttu-id="d064d-126">Une fois que l’enregistreur est lié au writer de format, les requêtes de propriété de média et d’écriture peuvent être effectuées avant d’écrire l’image de résultat sur le disque à l’aide de la méthode [**IDiscFormat2Data :: Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) .</span><span class="sxs-lookup"><span data-stu-id="d064d-126">After the recorder is bound to the format writer, media and write-specific property queries can be performed prior to writing the result image to disc using the [**IDiscFormat2Data::Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) method.</span></span>

> [!Note]  
> <span data-ttu-id="d064d-127">La chaîne de nom de client spécifiée dans l’exemple de code ci-dessous doit être ajustée en fonction de l’application spécifique.</span><span class="sxs-lookup"><span data-stu-id="d064d-127">The client name string specified in the sample code below should be adjusted as appropriate for the specific application.</span></span>

 


```VB
    ' Create a DiscFormat2Data object and set the recorder
    Dim DataWriter
    Set DataWriter = CreateObject ("IMAPI2.MsftDiscFormat2Data")
    DataWriter.Recorder = Recorder
    DataWriter.ClientName = "IMAPIv2 TEST"
```



## <a name="creating-the-file-system-object"></a><span data-ttu-id="d064d-128">Création de l’objet de système de fichiers</span><span class="sxs-lookup"><span data-stu-id="d064d-128">Creating the File System Object</span></span>

<span data-ttu-id="d064d-129">Pour pouvoir enregistrer une nouvelle session, vous devez d’abord générer une image de gravure.</span><span class="sxs-lookup"><span data-stu-id="d064d-129">In order to record a new session, a burn image must be generated for it first.</span></span> <span data-ttu-id="d064d-130">Une image de gravure pour les formats **ISO9660**, **Joliet** et **UDF** est constituée de systèmes de fichiers de fichiers et de répertoires individuels.</span><span class="sxs-lookup"><span data-stu-id="d064d-130">A burn image for **ISO9660**, **Joliet** and **UDF** formats consist of file systems of individual files and directories.</span></span> <span data-ttu-id="d064d-131">L’objet **MsftFileSystemImage** est l’objet de système de fichiers qui contient les fichiers et les répertoires à placer sur le support optique.</span><span class="sxs-lookup"><span data-stu-id="d064d-131">The **MsftFileSystemImage** object is the file system object that contains the files and directories to be placed on the optical media.</span></span> <span data-ttu-id="d064d-132">L’interface [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) fournit l’accès à l’objet et aux paramètres du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="d064d-132">The [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) interface provides access to the file system object and settings.</span></span>


```VB
    ' Create a new file system image object
    Dim FSI
    Set FSI = CreateObject("IMAPI2FS.MsftFileSystemImage")
```



## <a name="importing-a-file-system"></a><span data-ttu-id="d064d-133">Importation d’un système de fichiers</span><span class="sxs-lookup"><span data-stu-id="d064d-133">Importing a File System</span></span>

<span data-ttu-id="d064d-134">Avant de continuer, assurez-vous que le disque n’est pas vide en vérifiant la propriété [**IDiscFormat2 :: obtenir \_ MediaHeuristicallyBlank**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2-get_mediaheuristicallyblank) .</span><span class="sxs-lookup"><span data-stu-id="d064d-134">Before proceeding, ensure that the disc is not blank by checking the [**IDiscFormat2::get\_MediaHeuristicallyBlank**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2-get_mediaheuristicallyblank) property.</span></span>

<span data-ttu-id="d064d-135">Après la création de l’objet **MsftFileSystemImage** , la propriété [**IFileSystemImage ::p ut \_ MultisessionInterfaces**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_multisessioninterfaces) doit être initialisée avant un appel à la méthode [**IFileSystemImage :: ImportFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem) ou [**IFileSystemImage :: ImportSpecificFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importspecificfilesystem) pour importer le système de fichiers à partir de la dernière session enregistrée.</span><span class="sxs-lookup"><span data-stu-id="d064d-135">After creating the **MsftFileSystemImage** object, the [**IFileSystemImage::put\_MultisessionInterfaces**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_multisessioninterfaces) property should be initialized prior to a call to either the [**IFileSystemImage::ImportFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem) or [**IFileSystemImage::ImportSpecificFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importspecificfilesystem) method to import the file system from the last recorded session.</span></span> <span data-ttu-id="d064d-136">Ces méthodes remplissent automatiquement l’objet **MsftFileSystemImage** avec des informations décrivant les fichiers et répertoires précédemment enregistrés.</span><span class="sxs-lookup"><span data-stu-id="d064d-136">These methods will automatically populate the **MsftFileSystemImage** object with information describing the previously recorded files and directories.</span></span>

> [!Note]  
> <span data-ttu-id="d064d-137">La propriété [**IFileSystemImage ::p ut \_ MultisessionInterfaces**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_multisessioninterfaces) est généralement initialisée avec les interfaces multisession fournies par l’enregistreur de données via la propriété [**IDiscFormat2Data :: obten \_ MultisessionInterfaces**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_multisessioninterfaces) .</span><span class="sxs-lookup"><span data-stu-id="d064d-137">The [**IFileSystemImage::put\_MultisessionInterfaces**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_multisessioninterfaces) property is typically initialized with the multisession interfaces provided by the data writer via the [**IDiscFormat2Data::get\_MultisessionInterfaces**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_multisessioninterfaces) property.</span></span>

 

<span data-ttu-id="d064d-138">Les tentatives de définition de la propriété **IFileSystemImage ::p ut \_ MultisessionInterfaces** ÉCHOUEnt si IMAPI ne prend pas en charge la multisession pour le support actuellement inséré ou si le support ne peut pas être ajouté pour une raison quelconque (par exemple, parce qu’il est fermé).</span><span class="sxs-lookup"><span data-stu-id="d064d-138">Attempts to set the **IFileSystemImage::put\_MultisessionInterfaces** property will fail if IMAPI does not support multisession for the currently inserted media or the media cannot be appended for some other reason (e.g. because it is closed).</span></span>

<span data-ttu-id="d064d-139">Si la session de gravure précédente contenait plusieurs types de système de fichiers, la méthode [**IFileSystemImage :: ImportFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem) importera les informations du type de système de fichiers le plus avancé présent.</span><span class="sxs-lookup"><span data-stu-id="d064d-139">If the previous burn session contained more than one file system type, the [**IFileSystemImage::ImportFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem) method will import information from the most advanced file system type present.</span></span> <span data-ttu-id="d064d-140">Par exemple, dans l’exemple fourni dans cette rubrique, UDF est le système de fichiers importé.</span><span class="sxs-lookup"><span data-stu-id="d064d-140">For example, in the example provided in this topic, UDF is the imported file system.</span></span> <span data-ttu-id="d064d-141">Toutefois, l’utilisation de la méthode [**IFileSystemImage :: ImportSpecificFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importspecificfilesystem) permet la sélection spécifique du système de fichiers à importer.</span><span class="sxs-lookup"><span data-stu-id="d064d-141">However, use of the [**IFileSystemImage::ImportSpecificFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importspecificfilesystem) method allows the specific selection of the file system to import.</span></span>

> [!Note]  
> <span data-ttu-id="d064d-142">La méthode [**IFileSystemImage :: IdentifyFileSystemsOnDisc**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-identifyfilesystemsondisc) peut être utilisée pour déterminer les systèmes de fichiers disponibles sur le disque.</span><span class="sxs-lookup"><span data-stu-id="d064d-142">The [**IFileSystemImage::IdentifyFileSystemsOnDisc**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-identifyfilesystemsondisc) method can be used to determine which file systems are available on the disc.</span></span>

 


```VB
    ' Import the last session, if the disc is not empty, or initialize
    ' the file system, if the disc is empty
    If Not DataWriter.MediaHeuristicallyBlank _
    Then
        On Error Resume Next
        FSI.MultisessionInterfaces = DataWriter.MultisessionInterfaces
        If Err.Number <> 0 _
        Then
            WScript.Echo "Multisession is not supported for this disc"
            Main = 1
            Exit Function
        End If
        On Error Goto 0

        WScript.Echo "Importing data from the previous session..."
        FSI.ImportFileSystem()
    Else 
        FSI.ChooseImageDefaults(Recorder)
    End If
```



## <a name="adding-or-removing-files-to-the-file-system"></a><span data-ttu-id="d064d-143">Ajout ou suppression de fichiers dans le système de fichiers</span><span class="sxs-lookup"><span data-stu-id="d064d-143">Adding or Removing Files to the File System</span></span>

<span data-ttu-id="d064d-144">Après avoir créé l’objet de système de fichiers et importé le système de fichiers à partir de la session précédente, appelez les méthodes [**IFileSystemImage :: CreateFileItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createfileitem) et [**IFileSystemImage :: CreateDirectoryItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createdirectoryitem) pour créer respectivement des objets de fichier et de répertoire.</span><span class="sxs-lookup"><span data-stu-id="d064d-144">After creating the file system object and importing the file system from the previous session, call the [**IFileSystemImage::CreateFileItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createfileitem) and [**IFileSystemImage::CreateDirectoryItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createdirectoryitem) methods to create new file and directory objects, respectively.</span></span> <span data-ttu-id="d064d-145">Les objets de fichier et de répertoire fournissent des détails spécifiques sur les fichiers et les répertoires.</span><span class="sxs-lookup"><span data-stu-id="d064d-145">The file and directory objects provide specific details about the files and directories.</span></span> <span data-ttu-id="d064d-146">Vous pouvez également utiliser la méthode [**IFsiDirectoryItem :: AddTree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-addtree) d’un objet d’annuaire, représenté par le biais de l’interface [**IFsiDirectoryItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem) , pour ajouter des fichiers et des répertoires existants à partir d’un autre dispositif de stockage (par exemple, un disque dur).</span><span class="sxs-lookup"><span data-stu-id="d064d-146">Alternatively, the [**IFsiDirectoryItem::AddTree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-addtree) method of a directory object, represented via the [**IFsiDirectoryItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem) interface, can be used to add existing files and directories from another storage device (i.e. a hard drive).</span></span>

<span data-ttu-id="d064d-147">La méthode de mise à jour du gestionnaire d’événements disponible pour [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) identifie le fichier en cours d’ajout à l’image du système de fichiers, le nombre de secteurs déjà copiés et le nombre total de secteurs à copier.</span><span class="sxs-lookup"><span data-stu-id="d064d-147">The event handler update method available for [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) identifies the current file being added to the file system image, the number of sectors already copied, and the total number of sectors to be copied.</span></span>

<span data-ttu-id="d064d-148">Pour supprimer des fichiers et des répertoires existants du système de fichiers, utilisez les méthodes [**IFsiDirectoryItem :: Remove**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-remove) et [**IFsiDirectoryItem :: RemoveTree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-removetree) des objets d’annuaire représentés par le biais de l’interface [**IFsiDirectoryItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem) .</span><span class="sxs-lookup"><span data-stu-id="d064d-148">To remove existing files and directories from the file system, use the [**IFsiDirectoryItem::Remove**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-remove) and [**IFsiDirectoryItem::RemoveTree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-removetree) methods of the directory objects represented via the [**IFsiDirectoryItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem) interface.</span></span> <span data-ttu-id="d064d-149">La propriété [**\_ racine IFileSystemImage :: obtenir**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_root) est utilisée pour obtenir un pointeur vers le répertoire racine du système de fichiers et l’interface **IFsiDirectoryItem** pour traverser l’arborescence de répertoires.</span><span class="sxs-lookup"><span data-stu-id="d064d-149">The [**IFileSystemImage::get\_Root**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_root) property is used to get a pointer to the root directory of the file system and the **IFsiDirectoryItem** interface to traverse through the directory tree.</span></span>

> [!Note]  
> <span data-ttu-id="d064d-150">Les fichiers et répertoires supprimés via les méthodes [**IFsiDirectoryItem :: Remove**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-remove) et [**IFsiDirectoryItem :: RemoveTree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-removetree) ne sont pas physiquement supprimés du disque, et les logiciels avancés peuvent facilement récupérer les informations supprimées.</span><span class="sxs-lookup"><span data-stu-id="d064d-150">Files and directories removed via the [**IFsiDirectoryItem::Remove**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-remove) and [**IFsiDirectoryItem::RemoveTree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-removetree) methods are not physically removed from the disc, and advanced software can easily recover the deleted information.</span></span>

 


```VB
    ' Add the directory and its contents to the file system 
    WScript.Echo "Adding " & Path & " directory to the disc..."
    FSI.Root.AddTree Path, false
```



## <a name="constructing-a-file-system-image"></a><span data-ttu-id="d064d-151">Construction d’une image de système de fichiers</span><span class="sxs-lookup"><span data-stu-id="d064d-151">Constructing a File System Image</span></span>

<span data-ttu-id="d064d-152">La dernière étape consiste à appeler [**IFileSystemImage :: CreateResultImage**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createresultimage) pour créer un flux de données pour l’image de gravure et lui fournir un accès via l’interface [**IFileSystemImageResult**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult) .</span><span class="sxs-lookup"><span data-stu-id="d064d-152">The final step is to call [**IFileSystemImage::CreateResultImage**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createresultimage) to create a data stream for the burn image and provide access to it through the [**IFileSystemImageResult**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult) interface.</span></span> <span data-ttu-id="d064d-153">Ce flux de données peut être fourni directement à la méthode [**IDiscFormat2Data :: Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) ou être enregistré dans un fichier en vue d’une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="d064d-153">This data stream can either be provided directly to the [**IDiscFormat2Data::Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) method or be saved to a file for later use.</span></span>


```VB
    ' Create an image from the file system image object
    Dim Result
    Set Result = FSI.CreateResultImage()
    Stream = Result.ImageStream
```



## <a name="example-summary"></a><span data-ttu-id="d064d-154">Exemple de résumé</span><span class="sxs-lookup"><span data-stu-id="d064d-154">Example Summary</span></span>

<span data-ttu-id="d064d-155">L’exemple de script Visual Basic suivant montre comment utiliser des objets IMAPi pour créer des disques multisession.</span><span class="sxs-lookup"><span data-stu-id="d064d-155">The following Visual Basic script example shows how to use IMAPI objects to create multisession discs.</span></span> <span data-ttu-id="d064d-156">L’exemple crée une nouvelle session et ajoute un répertoire au disque. Par souci de simplicité, le code n’effectue pas de vérification étendue des erreurs et suppose les points suivants :</span><span class="sxs-lookup"><span data-stu-id="d064d-156">The example creates a new session and adds a directory to the disc. For the sake of simplicity, the code does not perform extensive error checking, and assumes the following:</span></span>

-   <span data-ttu-id="d064d-157">Un périphérique de disque compatible est installé sur le système.</span><span class="sxs-lookup"><span data-stu-id="d064d-157">A compatible disc device is installed on the system.</span></span>
-   <span data-ttu-id="d064d-158">Le périphérique à disque est le premier lecteur sur le système.</span><span class="sxs-lookup"><span data-stu-id="d064d-158">The disc device is the first drive on the system.</span></span>
-   <span data-ttu-id="d064d-159">Un disque compatible est inséré dans le périphérique du disque.</span><span class="sxs-lookup"><span data-stu-id="d064d-159">A compatible disc is inserted in the disc device.</span></span>
-   <span data-ttu-id="d064d-160">Les fichiers à ajouter au disque se trouvent dans « g : \\ burndir ».</span><span class="sxs-lookup"><span data-stu-id="d064d-160">Files to add to the disc are located in "g:\\burndir".</span></span>

<span data-ttu-id="d064d-161">Des fonctionnalités supplémentaires telles que la vérification étendue des erreurs, la compatibilité des appareils et des supports, la notification d’événements et le calcul de l’espace libre sur le disque peuvent être ajoutées au script.</span><span class="sxs-lookup"><span data-stu-id="d064d-161">Additional functionality such as extensive error checking, device and media compatibility, event notification, and calculation of free space on the disc can be added to the script.</span></span>


```VB
' This script adds data files from a single directory tree to a
' disc (a new session is added, if the disc already contains data)

' Copyright (C) Microsoft. All rights reserved.

Option Explicit

' **_ CD/DVD disc file system types
Const FsiFileSystemISO9660 = 1
Const FsiFileSystemJoliet  = 2
Const FsiFileSystemUDF102  = 4

WScript.Quit(Main)

Function Main
    Dim Index                ' Index to recording drive.
    Dim Recorder             ' Recorder object
    Dim Path                 ' Directory of files to add
    Dim Stream               ' Data stream for burning device
    
    Index = 0                ' First drive on the system
    Path = "G:\BurnDir"      ' Files to add to the disc

    ' Create a DiscMaster2 object to connect to optical drives.
    Dim DiscMaster
    Set DiscMaster = WScript.CreateObject("IMAPI2.MsftDiscMaster2")

    ' Create a DiscRecorder2 object for the specified burning device.
    Dim UniqueId
    set Recorder = WScript.CreateObject("IMAPI2.MsftDiscRecorder2")
    UniqueId = DiscMaster.Item(Index)
    Recorder.InitializeDiscRecorder(UniqueId)

    ' Create a DiscFormat2Data object and set the recorder
    Dim DataWriter
    Set DataWriter = CreateObject ("IMAPI2.MsftDiscFormat2Data")
    DataWriter.Recorder = Recorder
    DataWriter.ClientName = "IMAPIv2 TEST"

    ' Create a new file system image object
    Dim FSI
    Set FSI = CreateObject("IMAPI2FS.MsftFileSystemImage")

    ' Import the last session, if the disc is not empty, or initialize
    ' the file system, if the disc is empty
    If Not DataWriter.MediaHeuristicallyBlank _
    Then
        On Error Resume Next
        FSI.MultisessionInterfaces = DataWriter.MultisessionInterfaces
        If Err.Number <> 0 _
        Then
            WScript.Echo "Multisession is not supported for this disc"
            Main = 1
            Exit Function
        End If
        On Error Goto 0

        WScript.Echo "Importing data from the previous session..."
        FSI.ImportFileSystem()
    Else 
        FSI.ChooseImageDefaults(Recorder)
    End If

    ' Add the directory and its contents to the file system 
    WScript.Echo "Adding " & Path & " directory to the disc..."
    FSI.Root.AddTree Path, false

    ' Create an image from the file system image object
    Dim Result
    Set Result = FSI.CreateResultImage()
    Stream = Result.ImageStream
    
    ' Write stream to disc using the specified recorder
    WScript.Echo "Writing content to the disc..."
    DataWriter.Write(Stream)

    WScript.Echo "Finished writing content."
    Main = 0
End Function

```



## <a name="related-topics"></a><span data-ttu-id="d064d-162">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d064d-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d064d-163">Utilisation d’IMAPi</span><span class="sxs-lookup"><span data-stu-id="d064d-163">Using IMAPI</span></span>](using-imapi.md)
</dt> <dt>

[<span data-ttu-id="d064d-164">_ *IStream*\*</span><span class="sxs-lookup"><span data-stu-id="d064d-164">_ *IStream*\*</span></span>](/windows/desktop/api/objidl/nn-objidl-istream)
</dt> <dt>

[<span data-ttu-id="d064d-165">**IDiscMaster2**</span><span class="sxs-lookup"><span data-stu-id="d064d-165">**IDiscMaster2**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2)
</dt> <dt>

[<span data-ttu-id="d064d-166">**IDiscFormat2Data**</span><span class="sxs-lookup"><span data-stu-id="d064d-166">**IDiscFormat2Data**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data)
</dt> <dt>

[<span data-ttu-id="d064d-167">**IFileSystemImage**</span><span class="sxs-lookup"><span data-stu-id="d064d-167">**IFileSystemImage**</span></span>](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage)
</dt> </dl>

 

 
