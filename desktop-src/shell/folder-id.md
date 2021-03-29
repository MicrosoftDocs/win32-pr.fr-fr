---
description: Avant de pouvoir utiliser un objet d’espace de noms, vous avez besoin d’un moyen de l’identifier.
ms.assetid: 54225481-a147-4d29-a642-24c9b59fc3ac
title: Obtention de l’ID d’un dossier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb2e62454bf27f2c203f59aecb325cefe6537d2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991589"
---
# <a name="getting-a-folders-id"></a><span data-ttu-id="75ac6-103">Obtention de l’ID d’un dossier</span><span class="sxs-lookup"><span data-stu-id="75ac6-103">Getting a Folder's ID</span></span>

<span data-ttu-id="75ac6-104">Avant de pouvoir utiliser un objet d’espace de noms, vous avez besoin d’un moyen de l’identifier.</span><span class="sxs-lookup"><span data-stu-id="75ac6-104">Before you can make use of a namespace object, you need a way to identify it.</span></span> <span data-ttu-id="75ac6-105">Cela signifie que vous obtenez son pointeur vers une liste d’identificateurs d’élément (PIDL) ou, dans le cas d’objets de système de fichiers, son chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="75ac6-105">This means obtaining either its pointer to an item identifier list (PIDL) or, in the case of file system objects, its path.</span></span> <span data-ttu-id="75ac6-106">Cette section présente deux méthodes plus simples pour obtenir des ID d’objet.</span><span class="sxs-lookup"><span data-stu-id="75ac6-106">This section discusses two of the simpler ways to obtain object IDs.</span></span>

<span data-ttu-id="75ac6-107">Pour bénéficier d’une approche plus puissante qui fonctionne avec n’importe quel dossier, utilisez l’interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) .</span><span class="sxs-lookup"><span data-stu-id="75ac6-107">For a more powerful approach that will work with any folder, use the [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface.</span></span> <span data-ttu-id="75ac6-108">Pour plus d’informations, consultez [obtention d’informations sur le contenu d’un dossier](folder-info.md) .</span><span class="sxs-lookup"><span data-stu-id="75ac6-108">See [Getting Information About the Contents of a Folder](folder-info.md) for more details.</span></span>

-   [<span data-ttu-id="75ac6-109">La boîte de dialogue OpenFiles</span><span class="sxs-lookup"><span data-stu-id="75ac6-109">The OpenFiles Dialog Box</span></span>](#the-openfiles-dialog-box)
-   [<span data-ttu-id="75ac6-110">Boîte de dialogue SHBrowseForFolder</span><span class="sxs-lookup"><span data-stu-id="75ac6-110">The SHBrowseForFolder Dialog Box</span></span>](#the-shbrowseforfolder-dialog-box)
-   [<span data-ttu-id="75ac6-111">Dossiers spéciaux et CSIDLs</span><span class="sxs-lookup"><span data-stu-id="75ac6-111">Special Folders and CSIDLs</span></span>](#special-folders-and-csidls)
-   [<span data-ttu-id="75ac6-112">Exemple simple d’utilisation de CSIDLs et SHBrowseForFolder</span><span class="sxs-lookup"><span data-stu-id="75ac6-112">A Simple Example of How to Use CSIDLs and SHBrowseForFolder</span></span>](#a-simple-example-of-how-to-use-csidls-and-shbrowseforfolder)

## <a name="the-openfiles-dialog-box"></a><span data-ttu-id="75ac6-113">La boîte de dialogue OpenFiles</span><span class="sxs-lookup"><span data-stu-id="75ac6-113">The OpenFiles Dialog Box</span></span>

<span data-ttu-id="75ac6-114">Pour permettre à l’utilisateur de naviguer dans l’espace de noms et de sélectionner un dossier, votre application peut utiliser l’interface [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) .</span><span class="sxs-lookup"><span data-stu-id="75ac6-114">To enable the user to navigate the namespace and select a folder, your application can use the [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) interface.</span></span> <span data-ttu-id="75ac6-115">L’appel de cette interface avec l’indicateur **Fos \_ PICKFOLDERS** ouvre la boîte de dialogue courante [fichiers ouverts](../dlgbox/open-and-save-as-dialog-boxes.md) en mode « choisir des dossiers ».</span><span class="sxs-lookup"><span data-stu-id="75ac6-115">Calling this interface with the **FOS\_PICKFOLDERS** flag launches the [Open Files](../dlgbox/open-and-save-as-dialog-boxes.md) common dialog box in "pick folders" mode.</span></span>

<span data-ttu-id="75ac6-116">Pour Windows Vista et versions ultérieures, il s’agit de la méthode recommandée pour sélectionner des dossiers.</span><span class="sxs-lookup"><span data-stu-id="75ac6-116">For Windows Vista and later, this is the recommended way to pick folders.</span></span>

## <a name="the-shbrowseforfolder-dialog-box"></a><span data-ttu-id="75ac6-117">Boîte de dialogue SHBrowseForFolder</span><span class="sxs-lookup"><span data-stu-id="75ac6-117">The SHBrowseForFolder Dialog Box</span></span>

<span data-ttu-id="75ac6-118">Pour permettre à l’utilisateur de naviguer dans l’espace de noms et de sélectionner un dossier, votre application peut simplement appeler [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera).</span><span class="sxs-lookup"><span data-stu-id="75ac6-118">To enable the user to navigate the namespace and select a folder, your application can simply invoke [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera).</span></span> <span data-ttu-id="75ac6-119">L’appel de cette fonction lance une boîte de dialogue avec une interface utilisateur qui fonctionne quelque peu comme les boîtes de dialogue courantes [ouvrir ou enregistrer](../dlgbox/open-and-save-as-dialog-boxes.md) sous.</span><span class="sxs-lookup"><span data-stu-id="75ac6-119">Calling this function launches a dialog box with a UI that works somewhat like the [Open or SaveAs](../dlgbox/open-and-save-as-dialog-boxes.md) common dialog boxes.</span></span>

<span data-ttu-id="75ac6-120">Lorsque l’utilisateur sélectionne un dossier, [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) retourne le PIDL complet du dossier et son nom complet.</span><span class="sxs-lookup"><span data-stu-id="75ac6-120">When the user selects a folder, [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) returns the folder's fully qualified PIDL and its display name.</span></span> <span data-ttu-id="75ac6-121">Si le dossier se trouve dans le système de fichiers, l’application peut convertir le PIDL en chemin d’accès en appelant [**SHGetPathFromIDList**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetpathfromidlista).</span><span class="sxs-lookup"><span data-stu-id="75ac6-121">If the folder is in the file system, the application can convert the PIDL to a path by calling [**SHGetPathFromIDList**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetpathfromidlista).</span></span> <span data-ttu-id="75ac6-122">L’application peut également limiter la plage de dossiers à partir de laquelle l’utilisateur peut sélectionner en spécifiant un dossier racine.</span><span class="sxs-lookup"><span data-stu-id="75ac6-122">The application can also restrict the range of folders that the user can select from by specifying a root folder.</span></span> <span data-ttu-id="75ac6-123">Seuls les dossiers situés en dessous de la racine de l’espace de noms s’affichent.</span><span class="sxs-lookup"><span data-stu-id="75ac6-123">Only folders that are below that root in the namespace will appear.</span></span> <span data-ttu-id="75ac6-124">L’illustration suivante montre la boîte de dialogue **SHBrowseForFolder** , avec le dossier racine défini sur Program Files.</span><span class="sxs-lookup"><span data-stu-id="75ac6-124">The following illustration shows the **SHBrowseForFolder** dialog box, with the root folder set to Program Files.</span></span>

![capture d’écran de la boîte de dialogue Rechercher un dossier](images/shell1.png)

<span data-ttu-id="75ac6-126">Un exemple simple d’utilisation de [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) est fourni ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="75ac6-126">A simple example of how to use [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) is provided later.</span></span>

## <a name="special-folders-and-csidls"></a><span data-ttu-id="75ac6-127">Dossiers spéciaux et CSIDLs</span><span class="sxs-lookup"><span data-stu-id="75ac6-127">Special Folders and CSIDLs</span></span>

<span data-ttu-id="75ac6-128">Un certain nombre de dossiers couramment utilisés sont désignés comme étant *spéciaux* par le système.</span><span class="sxs-lookup"><span data-stu-id="75ac6-128">A number of commonly used folders are designated as *special* by the system.</span></span> <span data-ttu-id="75ac6-129">Ces dossiers ont un objectif bien défini, et la plupart d’entre eux sont présents sur tous les systèmes.</span><span class="sxs-lookup"><span data-stu-id="75ac6-129">These folders have a well-defined purpose, and most of them are present on all systems.</span></span> <span data-ttu-id="75ac6-130">Même s’ils ne sont pas présents au départ, leurs noms et emplacements sont toujours définis, de sorte qu’ils peuvent être ajoutés ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="75ac6-130">Even if they are not present initially, their names and locations are still defined, so they can be added later.</span></span> <span data-ttu-id="75ac6-131">La collection de dossiers spéciaux comprend tous les dossiers virtuels standard du système, tels que imprimantes, mes documents et voisinage réseau.</span><span class="sxs-lookup"><span data-stu-id="75ac6-131">The collection of special folders includes all of the system's standard virtual folders, such as Printers, My Documents, and Network Neighborhood.</span></span> <span data-ttu-id="75ac6-132">Il comprend également un certain nombre de dossiers de système de fichiers standard, tels que Program Files et System.</span><span class="sxs-lookup"><span data-stu-id="75ac6-132">It also includes a number of standard file system folders, such as Program Files and System.</span></span>

<span data-ttu-id="75ac6-133">Même si les dossiers sont un composant standard de tous les systèmes, leur nom et leur emplacement dans l’espace de noms peuvent varier.</span><span class="sxs-lookup"><span data-stu-id="75ac6-133">Even though the folders are a standard component of all systems, their names and locations in the namespace can vary.</span></span> <span data-ttu-id="75ac6-134">Par exemple, le répertoire système est C : \\ winnt \\ system32 sur certains systèmes et c : \\ Windows \\ system32 sur d’autres.</span><span class="sxs-lookup"><span data-stu-id="75ac6-134">For example, the System directory is C:\\Winnt\\System32 on some systems and C:\\Windows\\System32 on others.</span></span> <span data-ttu-id="75ac6-135">Dans le passé, les variables d’environnement offraient un moyen de déterminer le nom et l’emplacement d’un dossier spécial sur un système particulier.</span><span class="sxs-lookup"><span data-stu-id="75ac6-135">In the past, environment variables provided a way to determine the name and location of a special folder on any particular system.</span></span> <span data-ttu-id="75ac6-136">L’interpréteur de commandes offre désormais un moyen plus robuste et plus souple d’identifier les dossiers spéciaux, [**CSIDLs**](csidl.md).</span><span class="sxs-lookup"><span data-stu-id="75ac6-136">The Shell now provides a more robust and flexible way to identify special folders, [**CSIDLs**](csidl.md).</span></span> <span data-ttu-id="75ac6-137">Vous devez généralement les utiliser à la place des variables d’environnement.</span><span class="sxs-lookup"><span data-stu-id="75ac6-137">You should generally use them instead of environment variables.</span></span>

<span data-ttu-id="75ac6-138">Les CSIDLs offrent un moyen uniforme d’identifier et de localiser des dossiers spéciaux, quel que soit leur nom ou emplacement sur un système particulier.</span><span class="sxs-lookup"><span data-stu-id="75ac6-138">CSIDLs provide a uniform way of identifying and locating special folders, regardless of their name or location on a particular system.</span></span> <span data-ttu-id="75ac6-139">Contrairement aux variables d’environnement, CSIDLs peut être utilisé avec des dossiers virtuels et des dossiers de système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="75ac6-139">Unlike environment variables, CSIDLs can be used with virtual folders as well as file system folders.</span></span> <span data-ttu-id="75ac6-140">Chaque dossier spécial est associé à un CSIDL unique.</span><span class="sxs-lookup"><span data-stu-id="75ac6-140">Each special folder has a unique CSIDL assigned to it.</span></span> <span data-ttu-id="75ac6-141">Par exemple, le dossier Program Files File System contient un CSIDL des **\_ \_ fichiers programme de CSIDL** et le dossier virtuel du voisinage réseau a un CSIDL du **\_ réseau CSIDL**.</span><span class="sxs-lookup"><span data-stu-id="75ac6-141">For example, the Program Files file system folder has a CSIDL of **CSIDL\_PROGRAM\_FILES**, and the Network Neighborhood virtual folder has a CSIDL of **CSIDL\_NETWORK**.</span></span>

<span data-ttu-id="75ac6-142">Un CSIDL est utilisé conjointement avec l’une des nombreuses fonctions Shell pour récupérer le PIDL d’un dossier spécial, ou le chemin d’accès d’un dossier de système de fichiers spécial.</span><span class="sxs-lookup"><span data-stu-id="75ac6-142">A CSIDL is used in conjunction with one of several Shell functions to retrieve a special folder's PIDL, or a special file system folder's path.</span></span> <span data-ttu-id="75ac6-143">Si le dossier n’existe pas sur un système, votre application peut forcer sa création en combinant le CSIDL avec l' **indicateur CSIDL \_ \_ Create**.</span><span class="sxs-lookup"><span data-stu-id="75ac6-143">If the folder does not exist on a system, your application can force it to be created by combining its CSIDL with **CSIDL\_FLAG\_CREATE**.</span></span> <span data-ttu-id="75ac6-144">Le CSIDL peut être passé aux fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="75ac6-144">The CSIDL can be passed to the following functions:</span></span>

-   <span data-ttu-id="75ac6-145">[**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation), qui récupère le PIDL d’un dossier spécial.</span><span class="sxs-lookup"><span data-stu-id="75ac6-145">[**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation), which retrieves the PIDL of a special folder.</span></span>
-   <span data-ttu-id="75ac6-146">[**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha), qui récupère le chemin d’accès d’un dossier spécial du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="75ac6-146">[**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha), which retrieves the path of a file system special folder.</span></span>

<span data-ttu-id="75ac6-147">Notez que ces deux fonctions ont été introduites avec la version 5,0 de l’interpréteur de commandes et remplacent les fonctions [**SHGetSpecialFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderlocation) et [**SHGetSpecialFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderpatha) .</span><span class="sxs-lookup"><span data-stu-id="75ac6-147">Note that these two functions were introduced with version 5.0 of the Shell and supersede the [**SHGetSpecialFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderlocation) and [**SHGetSpecialFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderpatha) functions.</span></span>

## <a name="a-simple-example-of-how-to-use-csidls-and-shbrowseforfolder"></a><span data-ttu-id="75ac6-148">Exemple simple d’utilisation de CSIDLs et SHBrowseForFolder</span><span class="sxs-lookup"><span data-stu-id="75ac6-148">A Simple Example of How to Use CSIDLs and SHBrowseForFolder</span></span>

<span data-ttu-id="75ac6-149">L’exemple de fonction suivant, PidlBrowse, montre comment utiliser CSIDLs pour récupérer les PIDL d’un dossier et utiliser [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) pour que l’utilisateur sélectionne un dossier.</span><span class="sxs-lookup"><span data-stu-id="75ac6-149">The following sample function, PidlBrowse, illustrates how to use CSIDLs to retrieve a folder's PIDL, and use [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) to have the user select a folder.</span></span> <span data-ttu-id="75ac6-150">Elle retourne le PIDL et le nom d’affichage du dossier sélectionné.</span><span class="sxs-lookup"><span data-stu-id="75ac6-150">It returns the PIDL and display name of the selected folder.</span></span>


```
LPITEMIDLIST PidlBrowse(HWND hwnd, int nCSIDL, LPSTR pszDisplayName)
{
    LPITEMIDLIST pidlRoot = NULL;
    LPITEMIDLIST pidlSelected = NULL;
    BROWSEINFO bi = {0};

    if(nCSIDL)
    {
        SHGetFolderLocation(hwnd, nCSIDL, NULL, NULL, &pidlRoot);
    }

    else
    {
        pidlRoot = NULL;
    }

    bi.hwndOwner = hwnd;
    bi.pidlRoot = pidlRoot;
    bi.pszDisplayName = pszDisplayName;
    bi.lpszTitle = "Choose a folder";
    bi.ulFlags = 0;
    bi.lpfn = NULL;
    bi.lParam = 0;

    pidlSelected = SHBrowseForFolder(&bi);

    if(pidlRoot)
    {
        CoTaskMemFree(pidlRoot);
    }

    return pidlSelected;
}
```



<span data-ttu-id="75ac6-151">L’application appelante passe un handle de fenêtre, qui est requis par [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera).</span><span class="sxs-lookup"><span data-stu-id="75ac6-151">The calling application passes in a window handle, which is needed by [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera).</span></span> <span data-ttu-id="75ac6-152">Le paramètre *nCSIDL* est un CSIDL facultatif qui est utilisé pour spécifier un dossier racine.</span><span class="sxs-lookup"><span data-stu-id="75ac6-152">The *nCSIDL* parameter is an optional CSIDL that is used to specify a root folder.</span></span> <span data-ttu-id="75ac6-153">Seuls les dossiers situés sous le dossier racine de la hiérarchie s’affichent.</span><span class="sxs-lookup"><span data-stu-id="75ac6-153">Only folders below the root folder in the hierarchy will be displayed.</span></span> <span data-ttu-id="75ac6-154">L’illustration ci-dessus a été générée en appelant cette fonction avec *nCSIDL* défini sur **\_ \_ fichiers programmes CSIDL**.</span><span class="sxs-lookup"><span data-stu-id="75ac6-154">The illustration shown earlier was generated by calling this function with *nCSIDL* set to **CSIDL\_PROGRAM\_FILES**.</span></span> <span data-ttu-id="75ac6-155">L’application appelante passe également dans une mémoire tampon de chaîne, *pszDisplayName*, pour contenir le nom complet du dossier sélectionné lorsque PidlBrowse retourne.</span><span class="sxs-lookup"><span data-stu-id="75ac6-155">The calling application also passes in a string buffer, *pszDisplayName*, to hold the display name of the selected folder when PidlBrowse returns.</span></span> <span data-ttu-id="75ac6-156">Il incombe à l’application appelante de libérer le IDList retourné par **SHBrowseForFolder** à l’aide de [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="75ac6-156">It is the responsibility of the calling application to free the IDList returned by **SHBrowseForFolder** using [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

 

 
