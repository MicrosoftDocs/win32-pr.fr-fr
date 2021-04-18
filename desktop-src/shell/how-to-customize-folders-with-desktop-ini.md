---
description: Personnalisation de l’apparence et du comportement d’un dossier individuel avec Desktop.ini.
ms.assetid: 0361b7da-bfb3-4880-b982-85d2fe419805
title: Comment personnaliser des dossiers avec Desktop.ini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaac3e6a96257e63b5e4210da0aa6e6e1db77eaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104560697"
---
# <a name="how-to-customize-folders-with-desktopini"></a><span data-ttu-id="7752f-103">Comment personnaliser des dossiers avec Desktop.ini</span><span class="sxs-lookup"><span data-stu-id="7752f-103">How to Customize Folders with Desktop.ini</span></span>

<span data-ttu-id="7752f-104">Les dossiers du système de fichiers sont généralement affichés avec une icône standard et un ensemble de propriétés, qui spécifient, par exemple, si le dossier est partagé.</span><span class="sxs-lookup"><span data-stu-id="7752f-104">File system folders are commonly displayed with a standard icon and set of properties, which specify, for instance, whether the folder is shared.</span></span> <span data-ttu-id="7752f-105">Vous pouvez personnaliser l’apparence et le comportement d’un dossier individuel en créant un fichier Desktop.ini pour ce dossier.</span><span class="sxs-lookup"><span data-stu-id="7752f-105">You can customize the appearance and behavior of an individual folder by creating a Desktop.ini file for that folder.</span></span>

## <a name="instructions"></a><span data-ttu-id="7752f-106">Instructions</span><span class="sxs-lookup"><span data-stu-id="7752f-106">Instructions</span></span>

### <a name="using-desktopini-files"></a><span data-ttu-id="7752f-107">Utilisation de fichiers Desktop.ini</span><span class="sxs-lookup"><span data-stu-id="7752f-107">Using Desktop.ini Files</span></span>

<span data-ttu-id="7752f-108">Les dossiers s’affichent normalement avec l’icône de dossier standard.</span><span class="sxs-lookup"><span data-stu-id="7752f-108">Folders are normally displayed with the standard folder icon.</span></span> <span data-ttu-id="7752f-109">Le fichier Desktop.ini est couramment utilisé pour assigner une icône ou une image miniature personnalisée à un dossier.</span><span class="sxs-lookup"><span data-stu-id="7752f-109">A common use of the Desktop.ini file is to assign a custom icon or thumbnail image to a folder.</span></span> <span data-ttu-id="7752f-110">Vous pouvez également utiliser Desktop.ini pour créer une *info-bulle* qui affiche des informations sur le dossier et contrôle certains aspects du comportement du dossier, par exemple la spécification de noms localisés pour le ou les éléments du dossier.</span><span class="sxs-lookup"><span data-stu-id="7752f-110">You can also use Desktop.ini to create an *infotip* that displays information about the folder and controls some aspects of the folder's behavior, such as specifying localized names for the folder or items in the folder.</span></span>

<span data-ttu-id="7752f-111">**Utilisez la procédure suivante pour personnaliser le style d’un dossier avec Desktop.ini :**</span><span class="sxs-lookup"><span data-stu-id="7752f-111">**Use the following procedure to customize a folder's style with Desktop.ini:**</span></span>

1.  <span data-ttu-id="7752f-112">Utilisez [**PathMakeSystemFolder**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera) pour transformer le dossier en dossier système.</span><span class="sxs-lookup"><span data-stu-id="7752f-112">Use [**PathMakeSystemFolder**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera) to make the folder a system folder.</span></span> <span data-ttu-id="7752f-113">Cela définit le bit en lecture seule sur le dossier pour indiquer que le comportement spécial réservé à Desktop.ini doit être activé.</span><span class="sxs-lookup"><span data-stu-id="7752f-113">This sets the read-only bit on the folder to indicate that the special behavior reserved for Desktop.ini should be enabled.</span></span> <span data-ttu-id="7752f-114">Vous pouvez également créer un dossier système à partir de la ligne de commande à l’aide d' **Attrib + s** *NomDossier*.</span><span class="sxs-lookup"><span data-stu-id="7752f-114">You can also make a folder a system folder from the command line by using **attrib +s** *FolderName*.</span></span>
2.  <span data-ttu-id="7752f-115">Créez un fichier de Desktop.ini pour le dossier.</span><span class="sxs-lookup"><span data-stu-id="7752f-115">Create a Desktop.ini file for the folder.</span></span> <span data-ttu-id="7752f-116">Vous devez le marquer comme étant *masqué* et *système* pour vous assurer qu’il est masqué pour les utilisateurs normaux.</span><span class="sxs-lookup"><span data-stu-id="7752f-116">You should mark it as *hidden* and *system* to ensure that it is hidden from normal users.</span></span>
3.  <span data-ttu-id="7752f-117">Assurez-vous que le fichier de Desktop.ini que vous créez est au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="7752f-117">Make sure the Desktop.ini file that you create is in the Unicode format.</span></span> <span data-ttu-id="7752f-118">Cela est nécessaire pour stocker les chaînes localisées qui peuvent être affichées aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="7752f-118">This is necessary to store the localized strings that can be displayed to users.</span></span>

### <a name="creating-a-desktopini-file"></a><span data-ttu-id="7752f-119">Création d’un fichier de Desktop.ini</span><span class="sxs-lookup"><span data-stu-id="7752f-119">Creating a Desktop.ini File</span></span>

<span data-ttu-id="7752f-120">Le fichier Desktop.ini est un fichier texte qui vous permet de spécifier le mode d’affichage d’un dossier de système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="7752f-120">The Desktop.ini file is a text file that allows you to specify how a file system folder is viewed.</span></span> <span data-ttu-id="7752f-121">\[. \]La section ShellClassInfo vous permet de personnaliser l’affichage du dossier en affectant des valeurs à plusieurs entrées :</span><span class="sxs-lookup"><span data-stu-id="7752f-121">The \[.ShellClassInfo\] section, allows you to customize the folder's view by assigning values to several entries:</span></span>

|                   |                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7752f-122">**Entrée**</span><span class="sxs-lookup"><span data-stu-id="7752f-122">**Entry**</span></span>         | <span data-ttu-id="7752f-123">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="7752f-123">**Value**</span></span>                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="7752f-124">**ConfirmFileOp**</span><span class="sxs-lookup"><span data-stu-id="7752f-124">**ConfirmFileOp**</span></span> | <span data-ttu-id="7752f-125">Affectez la valeur 0 à cette entrée pour éviter l’avertissement « vous supprimez un dossier système » lors de la suppression ou du déplacement du dossier.</span><span class="sxs-lookup"><span data-stu-id="7752f-125">Set this entry to 0 to avoid a "You Are Deleting a System Folder" warning when deleting or moving the folder.</span></span>                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="7752f-126">**Nopartage**</span><span class="sxs-lookup"><span data-stu-id="7752f-126">**NoSharing**</span></span>     | <span data-ttu-id="7752f-127">Non pris en charge sous Windows Vista ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="7752f-127">Not supported under Windows Vista or later.</span></span> <span data-ttu-id="7752f-128">Définissez cette entrée sur 1 pour empêcher le partage du dossier.</span><span class="sxs-lookup"><span data-stu-id="7752f-128">Set this entry to 1 to prevent the folder from being shared.</span></span>                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="7752f-129">**IconFile**</span><span class="sxs-lookup"><span data-stu-id="7752f-129">**IconFile**</span></span>      | <span data-ttu-id="7752f-130">Si vous souhaitez spécifier une icône personnalisée pour le dossier, définissez cette entrée sur le nom de fichier de l’icône.</span><span class="sxs-lookup"><span data-stu-id="7752f-130">If you want to specify a custom icon for the folder, set this entry to the icon's file name.</span></span> <span data-ttu-id="7752f-131">L’extension de nom de fichier. ico est préférable, mais il est également possible de spécifier des fichiers. bmp ou. exe et. dll qui contiennent des icônes.</span><span class="sxs-lookup"><span data-stu-id="7752f-131">The .ico file name extension is preferred, but it is also possible to specify .bmp files, or .exe and .dll files that contain icons.</span></span> <span data-ttu-id="7752f-132">Si vous utilisez un chemin d’accès relatif, l’icône est disponible pour les personnes qui consultent le dossier sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="7752f-132">If you use a relative path, the icon is available to people who view the folder over the network.</span></span> <span data-ttu-id="7752f-133">Vous devez également définir l’entrée **IndexIcône** .</span><span class="sxs-lookup"><span data-stu-id="7752f-133">You must also set the **IconIndex** entry.</span></span> |
| <span data-ttu-id="7752f-134">**IndexIcône**</span><span class="sxs-lookup"><span data-stu-id="7752f-134">**IconIndex**</span></span>     | <span data-ttu-id="7752f-135">Définissez cette entrée pour spécifier l’index d’une icône personnalisée.</span><span class="sxs-lookup"><span data-stu-id="7752f-135">Set this entry to specify the index for a custom icon.</span></span> <span data-ttu-id="7752f-136">Si le fichier affecté à **IconFile** ne contient qu’une seule icône, définissez **IndexIcône** sur 0.</span><span class="sxs-lookup"><span data-stu-id="7752f-136">If the file assigned to **IconFile** only contains a single icon, set **IconIndex** to 0.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="7752f-137">**InfoTip**</span><span class="sxs-lookup"><span data-stu-id="7752f-137">**InfoTip**</span></span>       | <span data-ttu-id="7752f-138">Définissez cette entrée sur une chaîne de texte informatif.</span><span class="sxs-lookup"><span data-stu-id="7752f-138">Set this entry to an informational text string.</span></span> <span data-ttu-id="7752f-139">Elle s’affiche sous la forme d’une info-bulle lorsque le curseur pointe sur le dossier.</span><span class="sxs-lookup"><span data-stu-id="7752f-139">It is displayed as an infotip when the cursor hovers over the folder.</span></span> <span data-ttu-id="7752f-140">Si l’utilisateur clique sur le dossier, le texte d’information s’affiche dans le bloc d’informations du dossier, sous les informations standard.</span><span class="sxs-lookup"><span data-stu-id="7752f-140">If the user clicks the folder, the information text is displayed in the folder's information block, below the standard information.</span></span>                                                                                                                      |



 

<span data-ttu-id="7752f-141">Les illustrations suivantes sont du dossier Music avec un fichier de Desktop.ini personnalisé.</span><span class="sxs-lookup"><span data-stu-id="7752f-141">The following illustrations are of the Music folder with a custom Desktop.ini file.</span></span> <span data-ttu-id="7752f-142">Le dossier maintenant :</span><span class="sxs-lookup"><span data-stu-id="7752f-142">The folder now:</span></span>

-   <span data-ttu-id="7752f-143">A une icône personnalisée.</span><span class="sxs-lookup"><span data-stu-id="7752f-143">Has a custom icon.</span></span>
-   <span data-ttu-id="7752f-144">N’affiche pas d’avertissement « vous supprimez un dossier système » si le dossier est déplacé ou supprimé.</span><span class="sxs-lookup"><span data-stu-id="7752f-144">Does not display a "You Are Deleting a System Folder" warning if the folder is moved or deleted.</span></span>
-   <span data-ttu-id="7752f-145">Ne peut pas être partagé.</span><span class="sxs-lookup"><span data-stu-id="7752f-145">Cannot be shared.</span></span>
-   <span data-ttu-id="7752f-146">Affiche du texte informatif lorsque le curseur pointe sur le dossier.</span><span class="sxs-lookup"><span data-stu-id="7752f-146">Displays informational text when the cursor hovers over the folder.</span></span>

<span data-ttu-id="7752f-147">Les options des dossiers dans les illustrations suivantes sont définies pour afficher les fichiers masqués afin que Desktop.ini soit visible.</span><span class="sxs-lookup"><span data-stu-id="7752f-147">The folder options in the following illustrations are set to show hidden files so that Desktop.ini is visible.</span></span> <span data-ttu-id="7752f-148">Le dossier se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="7752f-148">The folder looks like this:</span></span>

![capture d’écran du dossier avec icône personnalisée](images/webview4.jpg)

<span data-ttu-id="7752f-150">Quand le curseur pointe sur le dossier, l’info-bulle s’affiche.</span><span class="sxs-lookup"><span data-stu-id="7752f-150">When the cursor hovers over the folder, the infotip is displayed.</span></span>

![capture d’écran d’un dossier avec une info-bulle](images/webview6.jpg)

<span data-ttu-id="7752f-152">L’icône personnalisée remplace l’icône de dossier partout où le nom du dossier s’affiche.</span><span class="sxs-lookup"><span data-stu-id="7752f-152">The custom icon replaces the folder icon everywhere the folder name appears.</span></span>

![capture d’écran de l’icône personnalisée qui remplace l’icône de dossier](images/webview5.jpg)

<span data-ttu-id="7752f-154">Le fichier desktop.ini suivant a été utilisé pour personnaliser le dossier musique, comme indiqué dans les illustrations précédentes.</span><span class="sxs-lookup"><span data-stu-id="7752f-154">The following desktop.ini file was used to customize the Music folder, as seen in the preceding illustrations.</span></span>


```
[.ShellClassInfo]
ConfirmFileOp=0
NoSharing=1
IconFile=Folder.ico
IconIndex=0
InfoTip=Some sensible information.
```



 

 



