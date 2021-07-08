---
description: Une fois que votre application a localisé un objet fichier, l’étape suivante est souvent d’agir sur celle-ci d’une manière ou d’une autre.
ms.assetid: d774c3b2-4caf-460a-ac32-0ed603491d5f
title: Lancement d’applications (ShellExecute, ShellExecuteEx, SHELLEXECUTEINFO)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3ae5640acdbf4d959b97607cc66a4fd8fe8ac24
ms.sourcegitcommit: 89aa14b1f685f8d65d56ecbdb8bef12246c33cf9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/08/2021
ms.locfileid: "113508610"
---
# <a name="launching-applications-shellexecute-shellexecuteex-shellexecuteinfo"></a><span data-ttu-id="c82be-103">Lancement d’applications (ShellExecute, ShellExecuteEx, SHELLEXECUTEINFO)</span><span class="sxs-lookup"><span data-stu-id="c82be-103">Launching Applications (ShellExecute, ShellExecuteEx, SHELLEXECUTEINFO)</span></span>

<span data-ttu-id="c82be-104">Une fois que votre application a localisé un objet fichier, l’étape suivante est souvent d’agir sur celle-ci d’une manière ou d’une autre.</span><span class="sxs-lookup"><span data-stu-id="c82be-104">Once your application has located a file object, the next step is often to act on it in some way.</span></span> <span data-ttu-id="c82be-105">Par exemple, votre application peut vouloir lancer une autre application qui permet à l’utilisateur de modifier un fichier de données.</span><span class="sxs-lookup"><span data-stu-id="c82be-105">For instance, your application might want to launch another application that allows the user to modify a data file.</span></span> <span data-ttu-id="c82be-106">Si le fichier d’intérêt est un fichier exécutable, votre application peut vouloir simplement la lancer.</span><span class="sxs-lookup"><span data-stu-id="c82be-106">If the file of interest is an executable, your application might want to simply launch it.</span></span> <span data-ttu-id="c82be-107">Ce document explique comment utiliser [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) ou [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) pour effectuer ces tâches.</span><span class="sxs-lookup"><span data-stu-id="c82be-107">This document discusses how to use [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) or [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to perform these tasks.</span></span>

-   [<span data-ttu-id="c82be-108">Utilisation de ShellExecute et ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="c82be-108">Using ShellExecute and ShellExecuteEx</span></span>](#using-shellexecute-and-shellexecuteex)
    -   [<span data-ttu-id="c82be-109">Verbes d’objet</span><span class="sxs-lookup"><span data-stu-id="c82be-109">Object Verbs</span></span>](#object-verbs)
    -   [<span data-ttu-id="c82be-110">Utilisation de ShellExecuteEx pour fournir des services d’activation à partir d’un site</span><span class="sxs-lookup"><span data-stu-id="c82be-110">Using ShellExecuteEx to Provide Activation Services from a Site</span></span>](#using-shellexecuteex-to-provide-activation-services-from-a-site)
    -   [<span data-ttu-id="c82be-111">Utilisation de ShellExecute pour lancer la boîte de dialogue Rechercher</span><span class="sxs-lookup"><span data-stu-id="c82be-111">Using ShellExecute to Launch the Search Dialog Box</span></span>](#using-shellexecute-to-launch-the-search-dialog-box)
-   [<span data-ttu-id="c82be-112">Exemple simple d’utilisation de ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="c82be-112">A Simple Example of How to Use ShellExecuteEx</span></span>](#a-simple-example-of-how-to-use-shellexecuteex)

## <a name="using-shellexecute-and-shellexecuteex"></a><span data-ttu-id="c82be-113">Utilisation de ShellExecute et ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="c82be-113">Using ShellExecute and ShellExecuteEx</span></span>

<span data-ttu-id="c82be-114">Pour utiliser [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) ou [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), votre application doit spécifier l’objet fichier ou dossier sur lequel agir et un *verbe* qui spécifie l’opération.</span><span class="sxs-lookup"><span data-stu-id="c82be-114">To use [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) or [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), your application must specify the file or folder object that is to be acted on, and a *verb* that specifies the operation.</span></span> <span data-ttu-id="c82be-115">Pour **ShellExecute**, assignez ces valeurs aux paramètres appropriés.</span><span class="sxs-lookup"><span data-stu-id="c82be-115">For **ShellExecute**, assign these values to the appropriate parameters.</span></span> <span data-ttu-id="c82be-116">Pour **ShellExecuteEx**, renseignez les membres appropriés d’une structure [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) .</span><span class="sxs-lookup"><span data-stu-id="c82be-116">For **ShellExecuteEx**, fill in the appropriate members of a [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) structure.</span></span> <span data-ttu-id="c82be-117">Il existe également plusieurs autres membres ou paramètres qui peuvent être utilisés pour ajuster le comportement des deux fonctions.</span><span class="sxs-lookup"><span data-stu-id="c82be-117">There are also several other members or parameters that can be used to fine-tune the behavior of the two functions.</span></span>

<span data-ttu-id="c82be-118">Les objets de fichier et de dossier peuvent faire partie du système de fichiers ou des objets virtuels, et ils peuvent être identifiés par des chemins d’accès ou des pointeurs vers des listes d’identificateurs d’éléments (PIDL).</span><span class="sxs-lookup"><span data-stu-id="c82be-118">File and folder objects can be part of the file system or virtual objects, and they can be identified by either paths or pointers to item identifier lists (PIDLs).</span></span>

### <a name="object-verbs"></a><span data-ttu-id="c82be-119">Verbes d’objet</span><span class="sxs-lookup"><span data-stu-id="c82be-119">Object Verbs</span></span>

<span data-ttu-id="c82be-120">Les verbes disponibles pour un objet sont essentiellement les éléments que vous trouvez dans le menu contextuel d’un objet.</span><span class="sxs-lookup"><span data-stu-id="c82be-120">The verbs available for an object are essentially the items that you find on an object's shortcut menu.</span></span> <span data-ttu-id="c82be-121">Pour rechercher les verbes disponibles, consultez le Registre sous</span><span class="sxs-lookup"><span data-stu-id="c82be-121">To find which verbs are available, look in the registry under</span></span>

<span data-ttu-id="c82be-122">**HKEY \_ CLASSES \_ racine** \\ **CLSID** \\ *{objet \_ CLSID}* \\ **Shell** \\ </span><span class="sxs-lookup"><span data-stu-id="c82be-122">**HKEY\_CLASSES\_ROOT**\\**CLSID**\\ *{object\_clsid}*\\**Shell**\\*verb*</span></span>

<span data-ttu-id="c82be-123">où *\_ CLSID* de l’objet est l’identificateur de classe (CLSID) de l’objet, et *verbe* est le nom du verbe disponible.</span><span class="sxs-lookup"><span data-stu-id="c82be-123">where *object\_clsid* is the class identifier (CLSID) of the object, and *verb* is the name of the available verb.</span></span> <span data-ttu-id="c82be-124">La  \\ sous-clé de **commande** Verb contient les données indiquant ce qui se produit lorsque ce verbe est appelé.</span><span class="sxs-lookup"><span data-stu-id="c82be-124">The *verb*\\**command** subkey contains the data indicating what happens when that verb is invoked.</span></span>

<span data-ttu-id="c82be-125">Pour savoir quels sont les verbes disponibles pour les [objets Shell prédéfinis](handlers.md), consultez le Registre sous</span><span class="sxs-lookup"><span data-stu-id="c82be-125">To find out which verbs are available for [predefined Shell objects](handlers.md), look in the registry under</span></span>

<span data-ttu-id="c82be-126">**HKEY \_ \_** Nom de l’objet racine des classes ( \\ *\_* \\  \\ *verbe* Shell)</span><span class="sxs-lookup"><span data-stu-id="c82be-126">**HKEY\_CLASSES\_ROOT**\\*object\_name*\\**shell**\\*verb*</span></span>

<span data-ttu-id="c82be-127">où *Object \_ Name* est le nom de l’objet Shell prédéfini.</span><span class="sxs-lookup"><span data-stu-id="c82be-127">where *object\_name* is the name of the predefined Shell object.</span></span> <span data-ttu-id="c82be-128">Là encore, la \\ sous-clé de **commande** Verb contient les données indiquant ce qui se produit lorsque ce verbe est appelé.</span><span class="sxs-lookup"><span data-stu-id="c82be-128">Again, the *verb*\\**command** subkey contains the data indicating what happens when that verb is invoked.</span></span>

<span data-ttu-id="c82be-129">Les verbes couramment disponibles sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="c82be-129">Commonly available verbs include:</span></span>



| <span data-ttu-id="c82be-130">Verbe</span><span class="sxs-lookup"><span data-stu-id="c82be-130">Verb</span></span>       | <span data-ttu-id="c82be-131">Description</span><span class="sxs-lookup"><span data-stu-id="c82be-131">Description</span></span>                                                                                              |
|------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c82be-132">modifier</span><span class="sxs-lookup"><span data-stu-id="c82be-132">edit</span></span>       | <span data-ttu-id="c82be-133">Lance un éditeur et ouvre le document en vue de sa modification.</span><span class="sxs-lookup"><span data-stu-id="c82be-133">Launches an editor and opens the document for editing.</span></span>                                                   |
| <span data-ttu-id="c82be-134">trouver</span><span class="sxs-lookup"><span data-stu-id="c82be-134">find</span></span>       | <span data-ttu-id="c82be-135">Lance une recherche à partir du répertoire spécifié.</span><span class="sxs-lookup"><span data-stu-id="c82be-135">Initiates a search starting from the specified directory.</span></span>                                                |
| <span data-ttu-id="c82be-136">ouvert</span><span class="sxs-lookup"><span data-stu-id="c82be-136">open</span></span>       | <span data-ttu-id="c82be-137">Lance une application.</span><span class="sxs-lookup"><span data-stu-id="c82be-137">Launches an application.</span></span> <span data-ttu-id="c82be-138">Si ce fichier n’est pas un fichier exécutable, son application associée est lancée.</span><span class="sxs-lookup"><span data-stu-id="c82be-138">If this file is not an executable file, its associated application is launched.</span></span> |
| <span data-ttu-id="c82be-139">print</span><span class="sxs-lookup"><span data-stu-id="c82be-139">print</span></span>      | <span data-ttu-id="c82be-140">Imprime le fichier de document.</span><span class="sxs-lookup"><span data-stu-id="c82be-140">Prints the document file.</span></span>                                                                                |
| <span data-ttu-id="c82be-141">properties</span><span class="sxs-lookup"><span data-stu-id="c82be-141">properties</span></span> | <span data-ttu-id="c82be-142">Affiche les propriétés de l’objet.</span><span class="sxs-lookup"><span data-stu-id="c82be-142">Displays the object's properties.</span></span>                                                                        |
| <span data-ttu-id="c82be-143">runas</span><span class="sxs-lookup"><span data-stu-id="c82be-143">runas</span></span>      | <span data-ttu-id="c82be-144">Lance une application en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="c82be-144">Launches an application as Administrator.</span></span> <span data-ttu-id="c82be-145">Le contrôle de compte d’utilisateur (UAC) invite l’utilisateur à donner son consentement pour exécuter l’application avec des privilèges élevés ou entrer les informations d’identification d’un compte d’administrateur utilisé pour exécuter l’application.</span><span class="sxs-lookup"><span data-stu-id="c82be-145">User Account Control (UAC) will prompt the user for consent to run the application elevated or enter the credentials of an administrator account used to run the application.</span></span> |



<span data-ttu-id="c82be-146">Chaque verbe correspond à la commande qui serait utilisée pour lancer l’application à partir d’une fenêtre de console.</span><span class="sxs-lookup"><span data-stu-id="c82be-146">Each verb corresponds to the command that would be used to launch the application from a console window.</span></span> <span data-ttu-id="c82be-147">Le verbe **Open** est un bon exemple, car il est généralement pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c82be-147">The **open** verb is a good example, as it is commonly supported.</span></span> <span data-ttu-id="c82be-148">Pour les fichiers .exe, **ouvrez** lance simplement l’application.</span><span class="sxs-lookup"><span data-stu-id="c82be-148">For .exe files, **open** simply launches the application.</span></span> <span data-ttu-id="c82be-149">Toutefois, il est plus couramment utilisé pour lancer une application qui fonctionne sur un fichier particulier.</span><span class="sxs-lookup"><span data-stu-id="c82be-149">However, it is more commonly used to launch an application that operates on a particular file.</span></span> <span data-ttu-id="c82be-150">Par exemple, .txt fichiers peuvent être ouverts par Microsoft WordPad.</span><span class="sxs-lookup"><span data-stu-id="c82be-150">For instance, .txt files can be opened by Microsoft WordPad.</span></span> <span data-ttu-id="c82be-151">Le verbe **Open** d’un fichier .txt correspond donc à une commande semblable à la suivante :</span><span class="sxs-lookup"><span data-stu-id="c82be-151">The **open** verb for a .txt file would thus correspond to something like the following command:</span></span>


```C++
C:\Program Files\Windows NT\Accessories\Wordpad.exe" "%1"
```



<span data-ttu-id="c82be-152">Quand vous utilisez [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) ou [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) pour ouvrir un fichier .txt, Wordpad.exe est lancé avec le fichier spécifié comme argument.</span><span class="sxs-lookup"><span data-stu-id="c82be-152">When you use [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) or [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to open a .txt file, Wordpad.exe is launched with the specified file as its argument.</span></span> <span data-ttu-id="c82be-153">Certaines commandes peuvent avoir des arguments supplémentaires, tels que des indicateurs, qui peuvent être ajoutés en fonction des besoins pour lancer correctement l’application.</span><span class="sxs-lookup"><span data-stu-id="c82be-153">Some commands can have additional arguments, such as flags, that can be added as needed to launch the application properly.</span></span> <span data-ttu-id="c82be-154">Pour plus d’informations sur les menus contextuels et les verbes, consultez [extension des menus contextuels](context.md).</span><span class="sxs-lookup"><span data-stu-id="c82be-154">For further discussion of shortcut menus and verbs, see [Extending Shortcut Menus](context.md).</span></span>

<span data-ttu-id="c82be-155">En général, essayer de déterminer la liste des verbes disponibles pour un fichier particulier est quelque peu compliqué.</span><span class="sxs-lookup"><span data-stu-id="c82be-155">In general, trying to determine the list of available verbs for a particular file is somewhat complicated.</span></span> <span data-ttu-id="c82be-156">Dans de nombreux cas, vous pouvez simplement affecter la **valeur null** au paramètre *lpVerb* , qui appelle la commande par défaut pour le type de fichier.</span><span class="sxs-lookup"><span data-stu-id="c82be-156">In many cases, you can simply set the *lpVerb* parameter to **NULL**, which invokes the default command for the file type.</span></span> <span data-ttu-id="c82be-157">Cette procédure est généralement équivalente à la définition de *lpVerb* sur « Open », mais certains types de fichiers peuvent avoir une commande par défaut différente.</span><span class="sxs-lookup"><span data-stu-id="c82be-157">This procedure is usually equivalent to setting *lpVerb* to "open", but some file types may have a different default command.</span></span> <span data-ttu-id="c82be-158">Pour plus d’informations, consultez [extension des menus contextuels](context.md) et la documentation de référence [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) .</span><span class="sxs-lookup"><span data-stu-id="c82be-158">For further information, see [Extending Shortcut Menus](context.md) and the [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) reference documentation.</span></span>

### <a name="using-shellexecuteex-to-provide-activation-services-from-a-site"></a><span data-ttu-id="c82be-159">Utilisation de ShellExecuteEx pour fournir des services d’activation à partir d’un site</span><span class="sxs-lookup"><span data-stu-id="c82be-159">Using ShellExecuteEx to Provide Activation Services from a Site</span></span>

<span data-ttu-id="c82be-160">Les services d’une chaîne de site peuvent contrôler de nombreux comportements d’activation d’élément.</span><span class="sxs-lookup"><span data-stu-id="c82be-160">A site chain's services can control many behaviors of item activation.</span></span> <span data-ttu-id="c82be-161">à partir de Windows 8, vous pouvez fournir un pointeur vers la chaîne de site vers [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) pour activer ces comportements.</span><span class="sxs-lookup"><span data-stu-id="c82be-161">As of Windows 8, you can provide a pointer to the site chain to [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to enable these behaviors.</span></span> <span data-ttu-id="c82be-162">Pour fournir le site à **ShellExecuteEx**:</span><span class="sxs-lookup"><span data-stu-id="c82be-162">To provide the site to **ShellExecuteEx**:</span></span>

-   <span data-ttu-id="c82be-163">Spécifiez l' \_ indicateur \_ \_ de masque HINST est un indicateur \_ \_ de site dans le membre **fmask** de [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa).</span><span class="sxs-lookup"><span data-stu-id="c82be-163">Specify the SEE\_MASK\_FLAG\_HINST\_IS\_SITE flag in the **fMask** member of [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa).</span></span>
-   <span data-ttu-id="c82be-164">Fournissez [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) dans le membre **hInstApp** de [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa).</span><span class="sxs-lookup"><span data-stu-id="c82be-164">Provide the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) in the **hInstApp** member of [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa).</span></span>

### <a name="using-shellexecute-to-launch-the-search-dialog-box"></a><span data-ttu-id="c82be-165">Utilisation de ShellExecute pour lancer la boîte de dialogue Rechercher</span><span class="sxs-lookup"><span data-stu-id="c82be-165">Using ShellExecute to Launch the Search Dialog Box</span></span>

<span data-ttu-id="c82be-166">quand un utilisateur clique avec le bouton droit sur une icône de dossier dans l’explorateur de Windows, l’un des éléments de menu est « rechercher ».</span><span class="sxs-lookup"><span data-stu-id="c82be-166">When a user right-clicks a folder icon in Windows Explorer, one of the menu items is "Search".</span></span> <span data-ttu-id="c82be-167">S’ils sélectionnent cet élément, l’interpréteur de commandes lance son utilitaire de recherche.</span><span class="sxs-lookup"><span data-stu-id="c82be-167">If they select that item, the Shell launches its Search utility.</span></span> <span data-ttu-id="c82be-168">Cet utilitaire affiche une boîte de dialogue qui peut être utilisée pour rechercher une chaîne de texte spécifiée dans des fichiers.</span><span class="sxs-lookup"><span data-stu-id="c82be-168">This utility displays a dialog box that can be used to search files for a specified text string.</span></span> <span data-ttu-id="c82be-169">Une application peut lancer par programmation l’utilitaire de recherche d’un répertoire en appelant [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea), avec « Find » comme paramètre *lpVerb* et le chemin d’accès au répertoire en tant que paramètre *lpFile* .</span><span class="sxs-lookup"><span data-stu-id="c82be-169">An application can programmatically launch the Search utility for a directory by calling [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea), with "find" as the *lpVerb* parameter, and the directory path as the *lpFile* parameter.</span></span> <span data-ttu-id="c82be-170">Par exemple, la ligne de code suivante lance l’utilitaire de recherche pour le répertoire c : \\ MyPrograms.</span><span class="sxs-lookup"><span data-stu-id="c82be-170">For instance, the following line of code launches the Search utility for the c:\\MyPrograms directory.</span></span>


```C++
ShellExecute(hwnd, "find", "c:\\MyPrograms", NULL, NULL, 0);
```



## <a name="a-simple-example-of-how-to-use-shellexecuteex"></a><span data-ttu-id="c82be-171">Exemple simple d’utilisation de ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="c82be-171">A Simple Example of How to Use ShellExecuteEx</span></span>

<span data-ttu-id="c82be-172">L’exemple d’application console suivant illustre l’utilisation de [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span><span class="sxs-lookup"><span data-stu-id="c82be-172">The following sample console application illustrates the use of [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span></span> <span data-ttu-id="c82be-173">La plupart des codes de vérification des erreurs ont été omis par souci de clarté.</span><span class="sxs-lookup"><span data-stu-id="c82be-173">Most error checking code has been omitted for clarity.</span></span>


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



<span data-ttu-id="c82be-174">l’application récupère tout d’abord le PIDL du répertoire Windows et énumère son contenu jusqu’à ce qu’il trouve le premier fichier .bmp.</span><span class="sxs-lookup"><span data-stu-id="c82be-174">The application first retrieves the PIDL of the Windows directory, and enumerates its contents until it finds the first .bmp file.</span></span> <span data-ttu-id="c82be-175">Contrairement à l’exemple précédent, [**IShellFolder :: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) est utilisé pour récupérer le nom d’analyse du fichier au lieu de son nom complet.</span><span class="sxs-lookup"><span data-stu-id="c82be-175">Unlike the earlier example, [**IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) is used to retrieve the file's parsing name instead of its display name.</span></span> <span data-ttu-id="c82be-176">Étant donné qu’il s’agit d’un dossier de système de fichiers, le nom d’analyse est un chemin d’accès complet, ce qui est nécessaire pour [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span><span class="sxs-lookup"><span data-stu-id="c82be-176">Because this is a file system folder, the parsing name is a fully qualified path, which is what is needed for [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span></span>

<span data-ttu-id="c82be-177">Une fois le premier fichier de .bmp localisé, les valeurs appropriées sont attribuées aux membres d’une structure [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) .</span><span class="sxs-lookup"><span data-stu-id="c82be-177">Once the first .bmp file has been located, appropriate values are assigned to the members of a [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) structure.</span></span> <span data-ttu-id="c82be-178">Le membre **lpFile** est défini sur le nom d’analyse du fichier et le membre **lpVerb** sur **null** pour commencer l’opération par défaut.</span><span class="sxs-lookup"><span data-stu-id="c82be-178">The **lpFile** member is set to the parsing name of the file, and the **lpVerb** member to **NULL**, to begin the default operation.</span></span> <span data-ttu-id="c82be-179">Dans ce cas, l’opération par défaut est « Open ».</span><span class="sxs-lookup"><span data-stu-id="c82be-179">In this case, the default operation is "open".</span></span> <span data-ttu-id="c82be-180">La structure est ensuite transmise à [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), qui lance le gestionnaire par défaut pour les fichiers bitmap, en général MSPaint.exe, pour ouvrir le fichier.</span><span class="sxs-lookup"><span data-stu-id="c82be-180">The structure is then passed to [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), which launches the default handler for bitmap files, typically MSPaint.exe, to open the file.</span></span> <span data-ttu-id="c82be-181">une fois la fonction retournée, les pidl sont libérés et l’interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) du dossier Windows est libérée.</span><span class="sxs-lookup"><span data-stu-id="c82be-181">After the function returns, the PIDLs are freed and the Windows folder's [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface is released.</span></span>

 

 
