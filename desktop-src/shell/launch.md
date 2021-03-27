---
description: Une fois que votre application a localisé un objet fichier, l’étape suivante est souvent d’agir sur celle-ci d’une manière ou d’une autre.
ms.assetid: d774c3b2-4caf-460a-ac32-0ed603491d5f
title: Lancement d’applications (ShellExecute, ShellExecuteEx, SHELLEXECUTEINFO)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5e528e6c816040a83d57864999fbb2d683f9fea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864126"
---
# <a name="launching-applications-shellexecute-shellexecuteex-shellexecuteinfo"></a><span data-ttu-id="120bd-103">Lancement d’applications (ShellExecute, ShellExecuteEx, SHELLEXECUTEINFO)</span><span class="sxs-lookup"><span data-stu-id="120bd-103">Launching Applications (ShellExecute, ShellExecuteEx, SHELLEXECUTEINFO)</span></span>

<span data-ttu-id="120bd-104">Une fois que votre application a localisé un objet fichier, l’étape suivante est souvent d’agir sur celle-ci d’une manière ou d’une autre.</span><span class="sxs-lookup"><span data-stu-id="120bd-104">Once your application has located a file object, the next step is often to act on it in some way.</span></span> <span data-ttu-id="120bd-105">Par exemple, votre application peut vouloir lancer une autre application qui permet à l’utilisateur de modifier un fichier de données.</span><span class="sxs-lookup"><span data-stu-id="120bd-105">For instance, your application might want to launch another application that allows the user to modify a data file.</span></span> <span data-ttu-id="120bd-106">Si le fichier d’intérêt est un fichier exécutable, votre application peut vouloir simplement la lancer.</span><span class="sxs-lookup"><span data-stu-id="120bd-106">If the file of interest is an executable, your application might want to simply launch it.</span></span> <span data-ttu-id="120bd-107">Ce document explique comment utiliser [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) ou [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) pour effectuer ces tâches.</span><span class="sxs-lookup"><span data-stu-id="120bd-107">This document discusses how to use [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) or [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to perform these tasks.</span></span>

-   [<span data-ttu-id="120bd-108">Utilisation de ShellExecute et ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="120bd-108">Using ShellExecute and ShellExecuteEx</span></span>](#using-shellexecute-and-shellexecuteex)
    -   [<span data-ttu-id="120bd-109">Verbes d’objet</span><span class="sxs-lookup"><span data-stu-id="120bd-109">Object Verbs</span></span>](#object-verbs)
    -   [<span data-ttu-id="120bd-110">Utilisation de ShellExecuteEx pour fournir des services d’activation à partir d’un site</span><span class="sxs-lookup"><span data-stu-id="120bd-110">Using ShellExecuteEx to Provide Activation Services from a Site</span></span>](#using-shellexecuteex-to-provide-activation-services-from-a-site)
    -   [<span data-ttu-id="120bd-111">Utilisation de ShellExecute pour lancer la boîte de dialogue Rechercher</span><span class="sxs-lookup"><span data-stu-id="120bd-111">Using ShellExecute to Launch the Search Dialog Box</span></span>](#using-shellexecute-to-launch-the-search-dialog-box)
-   [<span data-ttu-id="120bd-112">Exemple simple d’utilisation de ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="120bd-112">A Simple Example of How to Use ShellExecuteEx</span></span>](#a-simple-example-of-how-to-use-shellexecuteex)

## <a name="using-shellexecute-and-shellexecuteex"></a><span data-ttu-id="120bd-113">Utilisation de ShellExecute et ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="120bd-113">Using ShellExecute and ShellExecuteEx</span></span>

<span data-ttu-id="120bd-114">Pour utiliser [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) ou [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), votre application doit spécifier l’objet fichier ou dossier sur lequel agir et un *verbe* qui spécifie l’opération.</span><span class="sxs-lookup"><span data-stu-id="120bd-114">To use [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) or [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), your application must specify the file or folder object that is to be acted on, and a *verb* that specifies the operation.</span></span> <span data-ttu-id="120bd-115">Pour **ShellExecute**, assignez ces valeurs aux paramètres appropriés.</span><span class="sxs-lookup"><span data-stu-id="120bd-115">For **ShellExecute**, assign these values to the appropriate parameters.</span></span> <span data-ttu-id="120bd-116">Pour **ShellExecuteEx**, renseignez les membres appropriés d’une structure [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) .</span><span class="sxs-lookup"><span data-stu-id="120bd-116">For **ShellExecuteEx**, fill in the appropriate members of a [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) structure.</span></span> <span data-ttu-id="120bd-117">Il existe également plusieurs autres membres ou paramètres qui peuvent être utilisés pour ajuster le comportement des deux fonctions.</span><span class="sxs-lookup"><span data-stu-id="120bd-117">There are also several other members or parameters that can be used to fine-tune the behavior of the two functions.</span></span>

<span data-ttu-id="120bd-118">Les objets de fichier et de dossier peuvent faire partie du système de fichiers ou des objets virtuels, et ils peuvent être identifiés par des chemins d’accès ou des pointeurs vers des listes d’identificateurs d’éléments (PIDL).</span><span class="sxs-lookup"><span data-stu-id="120bd-118">File and folder objects can be part of the file system or virtual objects, and they can be identified by either paths or pointers to item identifier lists (PIDLs).</span></span>

### <a name="object-verbs"></a><span data-ttu-id="120bd-119">Verbes d’objet</span><span class="sxs-lookup"><span data-stu-id="120bd-119">Object Verbs</span></span>

<span data-ttu-id="120bd-120">Les verbes disponibles pour un objet sont essentiellement les éléments que vous trouvez dans le menu contextuel d’un objet.</span><span class="sxs-lookup"><span data-stu-id="120bd-120">The verbs available for an object are essentially the items that you find on an object's shortcut menu.</span></span> <span data-ttu-id="120bd-121">Pour rechercher les verbes disponibles, consultez le Registre sous</span><span class="sxs-lookup"><span data-stu-id="120bd-121">To find which verbs are available, look in the registry under</span></span>

<span data-ttu-id="120bd-122">**HKEY \_ CLASSES \_ racine** \\ **CLSID** \\ *{objet \_ CLSID}* \\ **Shell** \\ </span><span class="sxs-lookup"><span data-stu-id="120bd-122">**HKEY\_CLASSES\_ROOT**\\**CLSID**\\ *{object\_clsid}*\\**Shell**\\*verb*</span></span>

<span data-ttu-id="120bd-123">où *\_ CLSID* de l’objet est l’identificateur de classe (CLSID) de l’objet, et *verbe* est le nom du verbe disponible.</span><span class="sxs-lookup"><span data-stu-id="120bd-123">where *object\_clsid* is the class identifier (CLSID) of the object, and *verb* is the name of the available verb.</span></span> <span data-ttu-id="120bd-124">La  \\ sous-clé de **commande** Verb contient les données indiquant ce qui se produit lorsque ce verbe est appelé.</span><span class="sxs-lookup"><span data-stu-id="120bd-124">The *verb*\\**command** subkey contains the data indicating what happens when that verb is invoked.</span></span>

<span data-ttu-id="120bd-125">Pour savoir quels sont les verbes disponibles pour les [objets Shell prédéfinis](handlers.md), consultez le Registre sous</span><span class="sxs-lookup"><span data-stu-id="120bd-125">To find out which verbs are available for [predefined Shell objects](handlers.md), look in the registry under</span></span>

<span data-ttu-id="120bd-126">**HKEY \_ \_** Nom de l’objet racine des classes ( \\ *\_* \\  \\ *verbe* Shell)</span><span class="sxs-lookup"><span data-stu-id="120bd-126">**HKEY\_CLASSES\_ROOT**\\*object\_name*\\**shell**\\*verb*</span></span>

<span data-ttu-id="120bd-127">où *Object \_ Name* est le nom de l’objet Shell prédéfini.</span><span class="sxs-lookup"><span data-stu-id="120bd-127">where *object\_name* is the name of the predefined Shell object.</span></span> <span data-ttu-id="120bd-128">Là encore, la \\ sous-clé de **commande** Verb contient les données indiquant ce qui se produit lorsque ce verbe est appelé.</span><span class="sxs-lookup"><span data-stu-id="120bd-128">Again, the *verb*\\**command** subkey contains the data indicating what happens when that verb is invoked.</span></span>

<span data-ttu-id="120bd-129">Les verbes couramment disponibles sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="120bd-129">Commonly available verbs include:</span></span>



| <span data-ttu-id="120bd-130">Verbe</span><span class="sxs-lookup"><span data-stu-id="120bd-130">Verb</span></span>       | <span data-ttu-id="120bd-131">Description</span><span class="sxs-lookup"><span data-stu-id="120bd-131">Description</span></span>                                                                                              |
|------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="120bd-132">modifier</span><span class="sxs-lookup"><span data-stu-id="120bd-132">edit</span></span>       | <span data-ttu-id="120bd-133">Lance un éditeur et ouvre le document en vue de sa modification.</span><span class="sxs-lookup"><span data-stu-id="120bd-133">Launches an editor and opens the document for editing.</span></span>                                                   |
| <span data-ttu-id="120bd-134">trouver</span><span class="sxs-lookup"><span data-stu-id="120bd-134">find</span></span>       | <span data-ttu-id="120bd-135">Lance une recherche à partir du répertoire spécifié.</span><span class="sxs-lookup"><span data-stu-id="120bd-135">Initiates a search starting from the specified directory.</span></span>                                                |
| <span data-ttu-id="120bd-136">ouvert</span><span class="sxs-lookup"><span data-stu-id="120bd-136">open</span></span>       | <span data-ttu-id="120bd-137">Lance une application.</span><span class="sxs-lookup"><span data-stu-id="120bd-137">Launches an application.</span></span> <span data-ttu-id="120bd-138">Si ce fichier n’est pas un fichier exécutable, son application associée est lancée.</span><span class="sxs-lookup"><span data-stu-id="120bd-138">If this file is not an executable file, its associated application is launched.</span></span> |
| <span data-ttu-id="120bd-139">print</span><span class="sxs-lookup"><span data-stu-id="120bd-139">print</span></span>      | <span data-ttu-id="120bd-140">Imprime le fichier de document.</span><span class="sxs-lookup"><span data-stu-id="120bd-140">Prints the document file.</span></span>                                                                                |
| <span data-ttu-id="120bd-141">properties</span><span class="sxs-lookup"><span data-stu-id="120bd-141">properties</span></span> | <span data-ttu-id="120bd-142">Affiche les propriétés de l’objet.</span><span class="sxs-lookup"><span data-stu-id="120bd-142">Displays the object's properties.</span></span>                                                                        |
| <span data-ttu-id="120bd-143">runas</span><span class="sxs-lookup"><span data-stu-id="120bd-143">runas</span></span>      | <span data-ttu-id="120bd-144">Lance une application en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="120bd-144">Launches an application as Administrator.</span></span> <span data-ttu-id="120bd-145">Le contrôle de compte d’utilisateur (UAC) invite l’utilisateur à donner son consentement à</span><span class="sxs-lookup"><span data-stu-id="120bd-145">User Account Control (UAC) will prompt the user for consent to</span></span> |
|            | <span data-ttu-id="120bd-146">Exécutez l’application avec des privilèges élevés ou entrez les informations d’identification d’un compte d’administrateur utilisé pour exécuter le</span><span class="sxs-lookup"><span data-stu-id="120bd-146">run the application elevated or enter the credentials of an administrator account used to run the</span></span>        |
|            | <span data-ttu-id="120bd-147">application Aha!.</span><span class="sxs-lookup"><span data-stu-id="120bd-147">application.</span></span>                                                                                             |

 

<span data-ttu-id="120bd-148">Chaque verbe correspond à la commande qui serait utilisée pour lancer l’application à partir d’une fenêtre de console.</span><span class="sxs-lookup"><span data-stu-id="120bd-148">Each verb corresponds to the command that would be used to launch the application from a console window.</span></span> <span data-ttu-id="120bd-149">Le verbe **Open** est un bon exemple, car il est généralement pris en charge.</span><span class="sxs-lookup"><span data-stu-id="120bd-149">The **open** verb is a good example, as it is commonly supported.</span></span> <span data-ttu-id="120bd-150">Pour les fichiers. exe, **ouvrez** simplement l’application.</span><span class="sxs-lookup"><span data-stu-id="120bd-150">For .exe files, **open** simply launches the application.</span></span> <span data-ttu-id="120bd-151">Toutefois, il est plus couramment utilisé pour lancer une application qui fonctionne sur un fichier particulier.</span><span class="sxs-lookup"><span data-stu-id="120bd-151">However, it is more commonly used to launch an application that operates on a particular file.</span></span> <span data-ttu-id="120bd-152">Par exemple, les fichiers. txt peuvent être ouverts par Microsoft WordPad.</span><span class="sxs-lookup"><span data-stu-id="120bd-152">For instance, .txt files can be opened by Microsoft WordPad.</span></span> <span data-ttu-id="120bd-153">Le verbe **Open** d’un fichier. txt correspond donc à une commande semblable à la suivante :</span><span class="sxs-lookup"><span data-stu-id="120bd-153">The **open** verb for a .txt file would thus correspond to something like the following command:</span></span>


```C++
C:\Program Files\Windows NT\Accessories\Wordpad.exe" "%1"
```



<span data-ttu-id="120bd-154">Quand vous utilisez [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) ou [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) pour ouvrir un fichier. txt, Wordpad.exe est lancé avec le fichier spécifié comme argument.</span><span class="sxs-lookup"><span data-stu-id="120bd-154">When you use [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) or [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to open a .txt file, Wordpad.exe is launched with the specified file as its argument.</span></span> <span data-ttu-id="120bd-155">Certaines commandes peuvent avoir des arguments supplémentaires, tels que des indicateurs, qui peuvent être ajoutés en fonction des besoins pour lancer correctement l’application.</span><span class="sxs-lookup"><span data-stu-id="120bd-155">Some commands can have additional arguments, such as flags, that can be added as needed to launch the application properly.</span></span> <span data-ttu-id="120bd-156">Pour plus d’informations sur les menus contextuels et les verbes, consultez [extension des menus contextuels](context.md).</span><span class="sxs-lookup"><span data-stu-id="120bd-156">For further discussion of shortcut menus and verbs, see [Extending Shortcut Menus](context.md).</span></span>

<span data-ttu-id="120bd-157">En général, essayer de déterminer la liste des verbes disponibles pour un fichier particulier est quelque peu compliqué.</span><span class="sxs-lookup"><span data-stu-id="120bd-157">In general, trying to determine the list of available verbs for a particular file is somewhat complicated.</span></span> <span data-ttu-id="120bd-158">Dans de nombreux cas, vous pouvez simplement affecter la **valeur null** au paramètre *lpVerb* , qui appelle la commande par défaut pour le type de fichier.</span><span class="sxs-lookup"><span data-stu-id="120bd-158">In many cases, you can simply set the *lpVerb* parameter to **NULL**, which invokes the default command for the file type.</span></span> <span data-ttu-id="120bd-159">Cette procédure est généralement équivalente à la définition de *lpVerb* sur « Open », mais certains types de fichiers peuvent avoir une commande par défaut différente.</span><span class="sxs-lookup"><span data-stu-id="120bd-159">This procedure is usually equivalent to setting *lpVerb* to "open", but some file types may have a different default command.</span></span> <span data-ttu-id="120bd-160">Pour plus d’informations, consultez [extension des menus contextuels](context.md) et la documentation de référence [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) .</span><span class="sxs-lookup"><span data-stu-id="120bd-160">For further information, see [Extending Shortcut Menus](context.md) and the [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) reference documentation.</span></span>

### <a name="using-shellexecuteex-to-provide-activation-services-from-a-site"></a><span data-ttu-id="120bd-161">Utilisation de ShellExecuteEx pour fournir des services d’activation à partir d’un site</span><span class="sxs-lookup"><span data-stu-id="120bd-161">Using ShellExecuteEx to Provide Activation Services from a Site</span></span>

<span data-ttu-id="120bd-162">Les services d’une chaîne de site peuvent contrôler de nombreux comportements d’activation d’élément.</span><span class="sxs-lookup"><span data-stu-id="120bd-162">A site chain's services can control many behaviors of item activation.</span></span> <span data-ttu-id="120bd-163">À partir de Windows 8, vous pouvez fournir un pointeur vers la chaîne de site vers [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) pour activer ces comportements.</span><span class="sxs-lookup"><span data-stu-id="120bd-163">As of Windows 8, you can provide a pointer to the site chain to [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to enable these behaviors.</span></span> <span data-ttu-id="120bd-164">Pour fournir le site à **ShellExecuteEx**:</span><span class="sxs-lookup"><span data-stu-id="120bd-164">To provide the site to **ShellExecuteEx**:</span></span>

-   <span data-ttu-id="120bd-165">Spécifiez l' \_ indicateur \_ \_ de masque HINST est un indicateur \_ \_ de site dans le membre **fmask** de [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa).</span><span class="sxs-lookup"><span data-stu-id="120bd-165">Specify the SEE\_MASK\_FLAG\_HINST\_IS\_SITE flag in the **fMask** member of [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa).</span></span>
-   <span data-ttu-id="120bd-166">Fournissez [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) dans le membre **hInstApp** de [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa).</span><span class="sxs-lookup"><span data-stu-id="120bd-166">Provide the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) in the **hInstApp** member of [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa).</span></span>

### <a name="using-shellexecute-to-launch-the-search-dialog-box"></a><span data-ttu-id="120bd-167">Utilisation de ShellExecute pour lancer la boîte de dialogue Rechercher</span><span class="sxs-lookup"><span data-stu-id="120bd-167">Using ShellExecute to Launch the Search Dialog Box</span></span>

<span data-ttu-id="120bd-168">Quand un utilisateur clique avec le bouton droit sur une icône de dossier dans l’Explorateur Windows, l’un des éléments de menu est « Rechercher ».</span><span class="sxs-lookup"><span data-stu-id="120bd-168">When a user right-clicks a folder icon in Windows Explorer, one of the menu items is "Search".</span></span> <span data-ttu-id="120bd-169">S’ils sélectionnent cet élément, l’interpréteur de commandes lance son utilitaire de recherche.</span><span class="sxs-lookup"><span data-stu-id="120bd-169">If they select that item, the Shell launches its Search utility.</span></span> <span data-ttu-id="120bd-170">Cet utilitaire affiche une boîte de dialogue qui peut être utilisée pour rechercher une chaîne de texte spécifiée dans des fichiers.</span><span class="sxs-lookup"><span data-stu-id="120bd-170">This utility displays a dialog box that can be used to search files for a specified text string.</span></span> <span data-ttu-id="120bd-171">Une application peut lancer par programmation l’utilitaire de recherche d’un répertoire en appelant [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea), avec « Find » comme paramètre *lpVerb* et le chemin d’accès au répertoire en tant que paramètre *lpFile* .</span><span class="sxs-lookup"><span data-stu-id="120bd-171">An application can programmatically launch the Search utility for a directory by calling [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea), with "find" as the *lpVerb* parameter, and the directory path as the *lpFile* parameter.</span></span> <span data-ttu-id="120bd-172">Par exemple, la ligne de code suivante lance l’utilitaire de recherche pour le répertoire c : \\ MyPrograms.</span><span class="sxs-lookup"><span data-stu-id="120bd-172">For instance, the following line of code launches the Search utility for the c:\\MyPrograms directory.</span></span>


```C++
ShellExecute(hwnd, "find", "c:\\MyPrograms", NULL, NULL, 0);
```



## <a name="a-simple-example-of-how-to-use-shellexecuteex"></a><span data-ttu-id="120bd-173">Exemple simple d’utilisation de ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="120bd-173">A Simple Example of How to Use ShellExecuteEx</span></span>

<span data-ttu-id="120bd-174">L’exemple d’application console suivant illustre l’utilisation de [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span><span class="sxs-lookup"><span data-stu-id="120bd-174">The following sample console application illustrates the use of [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span></span> <span data-ttu-id="120bd-175">La plupart des codes de vérification des erreurs ont été omis par souci de clarté.</span><span class="sxs-lookup"><span data-stu-id="120bd-175">Most error checking code has been omitted for clarity.</span></span>


```C++
#include <shlobj.h>
#include <shlwapi.h>
#include <objbase.h>

main()
{
    LPITEMIDLIST pidlWinFiles = NULL;
    LPITEMIDLIST pidlItems = NULL;
    IShellFolder *psfWinFiles = NULL;
    IShellFolder *psfDeskTop = NULL;
    LPENUMIDLIST ppenum = NULL;
    STRRET strDispName;
    TCHAR pszParseName[MAX_PATH];
    ULONG celtFetched;
    SHELLEXECUTEINFO ShExecInfo;
    HRESULT hr;
    BOOL fBitmap = FALSE;

    hr = SHGetFolderLocation(NULL, CSIDL_WINDOWS, NULL, NULL, &pidlWinFiles);

    hr = SHGetDesktopFolder(&psfDeskTop);

    hr = psfDeskTop->BindToObject(pidlWinFiles, NULL, IID_IShellFolder, (LPVOID *) &psfWinFiles);
    hr = psfDeskTop->Release();

    hr = psfWinFiles->EnumObjects(NULL,SHCONTF_FOLDERS | SHCONTF_NONFOLDERS, &ppenum);

    while( hr = ppenum->Next(1,&pidlItems, &celtFetched) == S_OK && (celtFetched) == 1)
    {
        psfWinFiles->GetDisplayNameOf(pidlItems, SHGDN_FORPARSING, &strDispName);
        StrRetToBuf(&strDispName, pidlItems, pszParseName, MAX_PATH);
        CoTaskMemFree(pidlItems);
        if(StrCmpI(PathFindExtension(pszParseName), TEXT( ".bmp")) == 0)
        {
            fBitmap = TRUE;
            break;
        }
    }

    ppenum->Release();

    if(fBitmap)
    {
        ShExecInfo.cbSize = sizeof(SHELLEXECUTEINFO);
        ShExecInfo.fMask = NULL;
        ShExecInfo.hwnd = NULL;
        ShExecInfo.lpVerb = NULL;
        ShExecInfo.lpFile = pszParseName;
        ShExecInfo.lpParameters = NULL;
        ShExecInfo.lpDirectory = NULL;
        ShExecInfo.nShow = SW_MAXIMIZE;
        ShExecInfo.hInstApp = NULL;

        ShellExecuteEx(&ShExecInfo);
    }

    CoTaskMemFree(pidlWinFiles);
    psfWinFiles->Release();

    return 0;
}
```



<span data-ttu-id="120bd-176">L’application récupère tout d’abord le PIDL du répertoire Windows et énumère son contenu jusqu’à ce qu’il trouve le premier fichier. bmp.</span><span class="sxs-lookup"><span data-stu-id="120bd-176">The application first retrieves the PIDL of the Windows directory, and enumerates its contents until it finds the first .bmp file.</span></span> <span data-ttu-id="120bd-177">Contrairement à l’exemple précédent, [**IShellFolder :: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) est utilisé pour récupérer le nom d’analyse du fichier au lieu de son nom complet.</span><span class="sxs-lookup"><span data-stu-id="120bd-177">Unlike the earlier example, [**IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) is used to retrieve the file's parsing name instead of its display name.</span></span> <span data-ttu-id="120bd-178">Étant donné qu’il s’agit d’un dossier de système de fichiers, le nom d’analyse est un chemin d’accès complet, ce qui est nécessaire pour [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span><span class="sxs-lookup"><span data-stu-id="120bd-178">Because this is a file system folder, the parsing name is a fully qualified path, which is what is needed for [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span></span>

<span data-ttu-id="120bd-179">Une fois le premier fichier. bmp localisé, les valeurs appropriées sont attribuées aux membres d’une structure [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) .</span><span class="sxs-lookup"><span data-stu-id="120bd-179">Once the first .bmp file has been located, appropriate values are assigned to the members of a [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) structure.</span></span> <span data-ttu-id="120bd-180">Le membre **lpFile** est défini sur le nom d’analyse du fichier et le membre **lpVerb** sur **null** pour commencer l’opération par défaut.</span><span class="sxs-lookup"><span data-stu-id="120bd-180">The **lpFile** member is set to the parsing name of the file, and the **lpVerb** member to **NULL**, to begin the default operation.</span></span> <span data-ttu-id="120bd-181">Dans ce cas, l’opération par défaut est « Open ».</span><span class="sxs-lookup"><span data-stu-id="120bd-181">In this case, the default operation is "open".</span></span> <span data-ttu-id="120bd-182">La structure est ensuite transmise à [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), qui lance le gestionnaire par défaut pour les fichiers bitmap, en général MSPaint.exe, pour ouvrir le fichier.</span><span class="sxs-lookup"><span data-stu-id="120bd-182">The structure is then passed to [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), which launches the default handler for bitmap files, typically MSPaint.exe, to open the file.</span></span> <span data-ttu-id="120bd-183">Une fois la fonction retournée, les PIDL sont libérés et l’interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) du dossier Windows est libérée.</span><span class="sxs-lookup"><span data-stu-id="120bd-183">After the function returns, the PIDLs are freed and the Windows folder's [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface is released.</span></span>

 

 
