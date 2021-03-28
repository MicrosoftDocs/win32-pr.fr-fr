---
description: À compter de Windows Vista, la boîte de dialogue élément commun remplace l’ancienne boîte de dialogue de fichier courant lorsqu’elle est utilisée pour ouvrir ou enregistrer un fichier.
title: Boîte de dialogue élément commun
ms.topic: article
ms.date: 05/31/2018
ms.assetid: f8846148-89a5-4b9b-ad68-56137a5c2f65
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 896514779b2ba3d11d3db0551f82e21f1d4120b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318114"
---
# <a name="common-item-dialog"></a><span data-ttu-id="0fb4d-103">Boîte de dialogue élément commun</span><span class="sxs-lookup"><span data-stu-id="0fb4d-103">Common Item Dialog</span></span>

<span data-ttu-id="0fb4d-104">À compter de Windows Vista, la boîte de dialogue élément commun remplace l’ancienne boîte de dialogue de fichier courant lorsqu’elle est utilisée pour ouvrir ou enregistrer un fichier.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-104">Starting with Windows Vista, the Common Item Dialog supersedes the older Common File Dialog when used to open or save a file.</span></span> <span data-ttu-id="0fb4d-105">La boîte de dialogue élément commun est utilisée dans deux variantes : la boîte de dialogue **ouvrir** et la boîte de dialogue **Enregistrer** .</span><span class="sxs-lookup"><span data-stu-id="0fb4d-105">The Common Item Dialog is used in two variations: the **Open** dialog and the **Save** dialog.</span></span> <span data-ttu-id="0fb4d-106">Ces deux boîtes de dialogue partagent la plupart de leurs fonctionnalités, mais chacune possède ses propres méthodes uniques.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-106">These two dialogs share most of their functionality, but each has its own unique methods.</span></span>

<span data-ttu-id="0fb4d-107">Bien que cette version plus récente s’intitule la boîte de dialogue élément commun, elle continue d’être appelée boîte de dialogue de fichier commune dans la plupart des documents.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-107">While this newer version is named the Common Item Dialog, it continues to be called the Common File Dialog in most documentation.</span></span> <span data-ttu-id="0fb4d-108">À moins que vous ne traitiez spécifiquement avec une version antérieure de Windows, vous devez supposer que toute mention de la boîte de dialogue de fichier commune fait référence à cette boîte de dialogue d’élément commune.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-108">Unless you are dealing specifically with an older version of Windows, you should assume that any mention of the Common File Dialog refers to this Common Item Dialog.</span></span>

<span data-ttu-id="0fb4d-109">Les rubriques suivantes sont présentées ici :</span><span class="sxs-lookup"><span data-stu-id="0fb4d-109">The following topics are discussed here:</span></span>

-   [<span data-ttu-id="0fb4d-110">IFileDialog, IFileOpenDialog et IFileSaveDialog</span><span class="sxs-lookup"><span data-stu-id="0fb4d-110">IFileDialog, IFileOpenDialog, and IFileSaveDialog</span></span>](#ifiledialog-ifileopendialog-and-ifilesavedialog)
    -   [<span data-ttu-id="0fb4d-111">Exemple d’utilisation</span><span class="sxs-lookup"><span data-stu-id="0fb4d-111">Sample Usage</span></span>](#sample-usage)
-   [<span data-ttu-id="0fb4d-112">Écoute des événements à partir de la boîte de dialogue</span><span class="sxs-lookup"><span data-stu-id="0fb4d-112">Listening to Events from the Dialog</span></span>](#listening-to-events-from-the-dialog)
    -   [<span data-ttu-id="0fb4d-113">OnFileOk</span><span class="sxs-lookup"><span data-stu-id="0fb4d-113">OnFileOk</span></span>](#onfileok)
    -   [<span data-ttu-id="0fb4d-114">OnShareViolation et OnOverwrite</span><span class="sxs-lookup"><span data-stu-id="0fb4d-114">OnShareViolation and OnOverwrite</span></span>](#onshareviolation-and-onoverwrite)
-   [<span data-ttu-id="0fb4d-115">Personnalisation de la boîte de dialogue</span><span class="sxs-lookup"><span data-stu-id="0fb4d-115">Customizing the Dialog</span></span>](#customizing-the-dialog)
    -   [<span data-ttu-id="0fb4d-116">Ajout d’options au bouton OK</span><span class="sxs-lookup"><span data-stu-id="0fb4d-116">Adding Options to the OK Button</span></span>](#adding-options-to-the-ok-button)
    -   [<span data-ttu-id="0fb4d-117">Réponse aux événements dans les contrôles ajoutés</span><span class="sxs-lookup"><span data-stu-id="0fb4d-117">Responding to Events in Added Controls</span></span>](#responding-to-events-in-added-controls)
-   [<span data-ttu-id="0fb4d-118">Exemples complets</span><span class="sxs-lookup"><span data-stu-id="0fb4d-118">Full Samples</span></span>](#full-samples)
-   [<span data-ttu-id="0fb4d-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0fb4d-119">Related topics</span></span>](#related-topics)

## <a name="ifiledialog-ifileopendialog-and-ifilesavedialog"></a><span data-ttu-id="0fb4d-120">IFileDialog, IFileOpenDialog et IFileSaveDialog</span><span class="sxs-lookup"><span data-stu-id="0fb4d-120">IFileDialog, IFileOpenDialog, and IFileSaveDialog</span></span>

<span data-ttu-id="0fb4d-121">Windows Vista fournit des implémentations des boîtes de dialogue **ouvrir** et **Enregistrer** : CLSID \_ FileOpenDialog et \_ CLSID FileSaveDialog.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-121">Windows Vista provides implementations of the **Open** and **Save** dialogs: CLSID\_FileOpenDialog and CLSID\_FileSaveDialog.</span></span> <span data-ttu-id="0fb4d-122">Ces boîtes de dialogue sont affichées ici.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-122">Those dialog boxes are shown here.</span></span>

![capture d’écran de la boîte de dialogue Ouvrir](images/cid/openfiledialog.png)

![capture d’écran de la boîte de dialogue Enregistrer sous](images/cid/savefiledialog.png)

<span data-ttu-id="0fb4d-125">[**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) et [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog) héritent de [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) et partagent une grande partie de leur fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-125">[**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) and [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog) inherit from [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) and share much of their functionality.</span></span> <span data-ttu-id="0fb4d-126">En outre, la boîte de dialogue **ouvrir** prend en charge **IFileOpenDialog** et la boîte de dialogue **Enregistrer** prend en charge **IFileSaveDialog**.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-126">In addition, the **Open** dialog supports **IFileOpenDialog**, and the **Save** dialog supports **IFileSaveDialog**.</span></span>

<span data-ttu-id="0fb4d-127">L’implémentation de la boîte de dialogue d’élément commune trouvée dans Windows Vista offre plusieurs avantages par rapport à l’implémentation fournie dans les versions antérieures :</span><span class="sxs-lookup"><span data-stu-id="0fb4d-127">The Common Item Dialog implementation found in Windows Vista provides several advantages over the implementation provided in earlier versions:</span></span>

-   <span data-ttu-id="0fb4d-128">Prend en charge l’utilisation directe de l’espace de noms Shell via [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) au lieu d’utiliser des chemins d’accès de système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-128">Supports direct use of the Shell namespace through [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) instead of using file system paths.</span></span>
-   <span data-ttu-id="0fb4d-129">Active la personnalisation simple de la boîte de dialogue, telle que la définition de l’étiquette sur le bouton **OK** , sans nécessiter de procédure de raccordement.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-129">Enables simple customization of the dialog, such as setting the label on the **OK** button, without requiring a hook procedure.</span></span>
-   <span data-ttu-id="0fb4d-130">Prend en charge une personnalisation plus complète de la boîte de dialogue en ajoutant un ensemble de contrôles pilotés par les données qui fonctionnent sans modèle de boîte de dialogue Win32.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-130">Supports more extensive customization of the dialog by the addition of a set of data-driven controls that operate without a Win32 dialog template.</span></span> <span data-ttu-id="0fb4d-131">Ce schéma de personnalisation libère le processus appelant de la disposition de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-131">This customization scheme frees the calling process from UI layout.</span></span> <span data-ttu-id="0fb4d-132">Étant donné que les modifications apportées à la conception de la boîte de dialogue continuent à utiliser ce modèle de données, l’implémentation de la boîte de dialogue n’est pas liée à la version actuelle spécifique de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-132">Since any changes to the dialog design continue to use this data model, the dialog implementation is not tied to the specific current version of the dialog.</span></span>
-   <span data-ttu-id="0fb4d-133">Prend en charge la notification de l’appelant des événements dans la boîte de dialogue, tels que la modification de la sélection ou la modification du type de fichier.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-133">Supports caller notification of events within the dialog, such as selection change or file type change.</span></span> <span data-ttu-id="0fb4d-134">Permet également au processus appelant de raccorder certains événements dans la boîte de dialogue, tels que l’analyse.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-134">Also enables the calling process to hook certain events in the dialog, such as the parsing.</span></span>
-   <span data-ttu-id="0fb4d-135">Introduit de nouvelles fonctionnalités de boîte de dialogue telles que l’ajout d’emplacements spécifiés par l’appelant à la barre des **emplacements** .</span><span class="sxs-lookup"><span data-stu-id="0fb4d-135">Introduces new dialog features such as adding caller-specified places to the **Places** bar.</span></span>
-   <span data-ttu-id="0fb4d-136">Dans la boîte de dialogue **Enregistrer** , les développeurs peuvent tirer parti des nouvelles fonctionnalités de métadonnées de l’interpréteur de commandes Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-136">In the **Save** dialog, developers can take advantage of new metadata features of the Windows Vista Shell.</span></span>

<span data-ttu-id="0fb4d-137">En outre, les développeurs peuvent choisir d’implémenter les interfaces suivantes :</span><span class="sxs-lookup"><span data-stu-id="0fb4d-137">Additionally, developers can choose to implement the following interfaces:</span></span>

-   <span data-ttu-id="0fb4d-138">[**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) pour recevoir des notifications d’événements dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-138">[**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) to receive notifications of events within the dialog.</span></span>
-   <span data-ttu-id="0fb4d-139">[**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) pour ajouter des contrôles à la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-139">[**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) to add controls to the dialog.</span></span>
-   <span data-ttu-id="0fb4d-140">[**IFileDialogControlEvents**](/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents) pour être informé des événements dans ces contrôles ajoutés.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-140">[**IFileDialogControlEvents**](/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents) to be notified of events in those added controls.</span></span>

<span data-ttu-id="0fb4d-141">La boîte de dialogue **ouvrir** ou **Enregistrer** retourne un objet [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) ou [**IShellItemArray**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray) au processus appelant.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-141">The **Open** or **Save** dialog returns an [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) or [**IShellItemArray**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray) object to the calling process.</span></span> <span data-ttu-id="0fb4d-142">L’appelant peut ensuite utiliser un objet **IShellItem** individuel pour obtenir un chemin d’accès au système de fichiers ou ouvrir un flux sur l’élément pour lire ou écrire des informations.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-142">The caller can then use an individual **IShellItem** object to get a file system path or to open a stream on the item to read or write information.</span></span>

<span data-ttu-id="0fb4d-143">Les indicateurs et les options disponibles pour les nouvelles méthodes de dialogue sont très similaires aux anciens indicateurs **OFN** trouvés dans la structure [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) et utilisés dans [**GetOpenFileName**](/windows/win32/api/commdlg/nf-commdlg-getopenfilenamea) et [**GetSaveFileName**](/windows/win32/api/commdlg/nf-commdlg-getsavefilenamea).</span><span class="sxs-lookup"><span data-stu-id="0fb4d-143">Flags and options available to the new dialog methods are very similar to the older **OFN** flags found in the [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure and used in [**GetOpenFileName**](/windows/win32/api/commdlg/nf-commdlg-getopenfilenamea) and [**GetSaveFileName**](/windows/win32/api/commdlg/nf-commdlg-getsavefilenamea).</span></span> <span data-ttu-id="0fb4d-144">Un grand nombre d’entre eux sont exactement les mêmes, sauf qu’ils commencent par un préfixe FOS.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-144">Many of them are exactly the same, except that they begin with an FOS prefix.</span></span> <span data-ttu-id="0fb4d-145">La liste complète se trouve dans les rubriques [**IFileDialog :: GetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getoptions) et [**IFileDialog :: SetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) .</span><span class="sxs-lookup"><span data-stu-id="0fb4d-145">The complete list can be found in the [**IFileDialog::GetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getoptions) and [**IFileDialog::SetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) topics.</span></span> <span data-ttu-id="0fb4d-146">Les boîtes de dialogue **ouvrir** et **Enregistrer** sont créées par défaut avec les indicateurs les plus courants.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-146">**Open** and **Save** dialogs are created by default with the most common flags.</span></span> <span data-ttu-id="0fb4d-147">Pour la boîte de dialogue **ouvrir** , il s’agit de (FOS \_ PATHMUSTEXIST \| Fos \_ FILEMUSTEXIST \| Fos \_ NOCHANGEDIR) et, pour la boîte de dialogue **Enregistrer** , il s’agit de (FOS \_ \| \_ \| \_ \| \_ OVERWRITEPROMPT Fos NOREADONLYRETURN Fos PATHMUSTEXIST Fos NOCHANGEDIR).</span><span class="sxs-lookup"><span data-stu-id="0fb4d-147">For the **Open** dialog, this is (FOS\_PATHMUSTEXIST \| FOS\_FILEMUSTEXIST \| FOS\_NOCHANGEDIR) and for the **Save** dialog this is (FOS\_OVERWRITEPROMPT \| FOS\_NOREADONLYRETURN \| FOS\_PATHMUSTEXIST \| FOS\_NOCHANGEDIR).</span></span>

<span data-ttu-id="0fb4d-148">[**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) et ses interfaces descendantes héritent de et étendent [**IModalWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imodalwindow).</span><span class="sxs-lookup"><span data-stu-id="0fb4d-148">[**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) and its descendant interfaces inherit from and extend [**IModalWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imodalwindow).</span></span> <span data-ttu-id="0fb4d-149">L' [**affichage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) prend comme seul paramètre le handle de la fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-149">[**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) takes as its only parameter the handle of the parent window.</span></span> <span data-ttu-id="0fb4d-150">Si **Show** aboutit, il y a un résultat valide.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-150">If **Show** returns successfully, there is a valid result.</span></span> <span data-ttu-id="0fb4d-151">Si elle retourne `HRESULT_FROM_WIN32(ERROR_CANCELLED)` , cela signifie que l’utilisateur a annulé la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-151">If it returns `HRESULT_FROM_WIN32(ERROR_CANCELLED)`, it means the user canceled the dialog.</span></span> <span data-ttu-id="0fb4d-152">Elle peut également retourner légitimement un autre code d’erreur tel que **E \_ OUTOFMEMORY**.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-152">It might also legitimately return another error code such as **E\_OUTOFMEMORY**.</span></span>

### <a name="sample-usage"></a><span data-ttu-id="0fb4d-153">Exemple d’utilisation</span><span class="sxs-lookup"><span data-stu-id="0fb4d-153">Sample Usage</span></span>

<span data-ttu-id="0fb4d-154">Les sections suivantes présentent un exemple de code pour diverses tâches de dialogue.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-154">The following sections show example code for a variety of dialog tasks.</span></span>

-   [<span data-ttu-id="0fb4d-155">Utilisation de base</span><span class="sxs-lookup"><span data-stu-id="0fb4d-155">Basic Usage</span></span>](#basic-usage)
-   [<span data-ttu-id="0fb4d-156">Limiter les résultats aux éléments du système de fichiers</span><span class="sxs-lookup"><span data-stu-id="0fb4d-156">Limiting Results to File System Items</span></span>](#limiting-results-to-file-system-items)
-   [<span data-ttu-id="0fb4d-157">Spécification des types de fichiers pour une boîte de dialogue</span><span class="sxs-lookup"><span data-stu-id="0fb4d-157">Specifying File Types for a Dialog</span></span>](#specifying-file-types-for-a-dialog)
-   [<span data-ttu-id="0fb4d-158">Contrôle du dossier par défaut</span><span class="sxs-lookup"><span data-stu-id="0fb4d-158">Controlling the Default Folder</span></span>](#controlling-the-default-folder)
-   [<span data-ttu-id="0fb4d-159">Ajout d’éléments à la barre des emplacements</span><span class="sxs-lookup"><span data-stu-id="0fb4d-159">Adding Items to the Places Bar</span></span>](#adding-items-to-the-places-bar)
-   [<span data-ttu-id="0fb4d-160">Persistance de l’État</span><span class="sxs-lookup"><span data-stu-id="0fb4d-160">State Persistence</span></span>](#state-persistence)
-   [<span data-ttu-id="0fb4d-161">Fonctionnalités de MultiSelect</span><span class="sxs-lookup"><span data-stu-id="0fb4d-161">Multiselect Capabilities</span></span>](#multiselect-capabilities)

<span data-ttu-id="0fb4d-162">La plupart des exemples de code se trouvent dans l' [exemple de boîte de dialogue de fichier commun](samples-commonfiledialog.md)SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-162">Most of the sample code can be found in the Windows SDK [Common File Dialog Sample](samples-commonfiledialog.md).</span></span>

### <a name="basic-usage"></a><span data-ttu-id="0fb4d-163">Utilisation de base</span><span class="sxs-lookup"><span data-stu-id="0fb4d-163">Basic Usage</span></span>

<span data-ttu-id="0fb4d-164">L’exemple suivant montre comment lancer une boîte de dialogue **ouverte** .</span><span class="sxs-lookup"><span data-stu-id="0fb4d-164">The following example illustrates how to launch an **Open** dialog.</span></span> <span data-ttu-id="0fb4d-165">Dans cet exemple, il est limité aux documents Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-165">In this example, it is restricted to Microsoft Word documents.</span></span>

> [!Note]  
> <span data-ttu-id="0fb4d-166">Plusieurs exemples de cette rubrique utilisent la `CDialogEventHandler_CreateInstance` fonction d’assistance pour créer une instance de l’implémentation de [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) .</span><span class="sxs-lookup"><span data-stu-id="0fb4d-166">Several examples in this topic use the `CDialogEventHandler_CreateInstance` helper function to create an instance of the [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) implementation.</span></span> <span data-ttu-id="0fb4d-167">Pour utiliser cette fonction dans votre propre code, copiez le code source de la `CDialogEventHandler_CreateInstance` fonction à partir de l' [exemple de boîte de dialogue de fichier commune](samples-commonfiledialog.md), à partir duquel tous les exemples de cette rubrique sont pris.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-167">To use this function in your own code, copy the source code for the `CDialogEventHandler_CreateInstance` function from the [Common File Dialog Sample](samples-commonfiledialog.md), from which all of the examples in this topic are taken.</span></span>

 


```C++
HRESULT BasicFileOpen()
{
    // CoCreate the File Open Dialog object.
    IFileDialog *pfd = NULL;
    HRESULT hr = CoCreateInstance(CLSID_FileOpenDialog, 
                      NULL, 
                      CLSCTX_INPROC_SERVER, 
                      IID_PPV_ARGS(&pfd));
    if (SUCCEEDED(hr))
    {
        // Create an event handling object, and hook it up to the dialog.
        IFileDialogEvents *pfde = NULL;
        hr = CDialogEventHandler_CreateInstance(IID_PPV_ARGS(&pfde));
        if (SUCCEEDED(hr))
        {
            // Hook up the event handler.
            DWORD dwCookie;
            hr = pfd->Advise(pfde, &dwCookie);
            if (SUCCEEDED(hr))
            {
                // Set the options on the dialog.
                DWORD dwFlags;

                // Before setting, always get the options first in order 
                // not to override existing options.
                hr = pfd->GetOptions(&dwFlags);
                if (SUCCEEDED(hr))
                {
                    // In this case, get shell items only for file system items.
                    hr = pfd->SetOptions(dwFlags | FOS_FORCEFILESYSTEM);
                    if (SUCCEEDED(hr))
                    {
                        // Set the file types to display only. 
                        // Notice that this is a 1-based array.
                        hr = pfd->SetFileTypes(ARRAYSIZE(c_rgSaveTypes), c_rgSaveTypes);
                        if (SUCCEEDED(hr))
                        {
                            // Set the selected file type index to Word Docs for this example.
                            hr = pfd->SetFileTypeIndex(INDEX_WORDDOC);
                            if (SUCCEEDED(hr))
                            {
                                // Set the default extension to be ".doc" file.
                                hr = pfd->SetDefaultExtension(L"doc;docx");
                                if (SUCCEEDED(hr))
                                {
                                    // Show the dialog
                                    hr = pfd->Show(NULL);
                                    if (SUCCEEDED(hr))
                                    {
                                        // Obtain the result once the user clicks 
                                        // the 'Open' button.
                                        // The result is an IShellItem object.
                                        IShellItem *psiResult;
                                        hr = pfd->GetResult(&psiResult);
                                        if (SUCCEEDED(hr))
                                        {
                                            // We are just going to print out the 
                                            // name of the file for sample sake.
                                            PWSTR pszFilePath = NULL;
                                            hr = psiResult->GetDisplayName(SIGDN_FILESYSPATH, 
                                                               &pszFilePath);
                                            if (SUCCEEDED(hr))
                                            {
                                                TaskDialog(NULL,
                                                           NULL,
                                                           L"CommonFileDialogApp",
                                                           pszFilePath,
                                                           NULL,
                                                           TDCBF_OK_BUTTON,
                                                           TD_INFORMATION_ICON,
                                                           NULL);
                                                CoTaskMemFree(pszFilePath);
                                            }
                                            psiResult->Release();
                                        }
                                    }
                                }
                            }
                        }
                    }
                }
                // Unhook the event handler.
                pfd->Unadvise(dwCookie);
            }
            pfde->Release();
        }
        pfd->Release();
    }
    return hr;
}
```



### <a name="limiting-results-to-file-system-items"></a><span data-ttu-id="0fb4d-168">Limiter les résultats aux éléments du système de fichiers</span><span class="sxs-lookup"><span data-stu-id="0fb4d-168">Limiting Results to File System Items</span></span>

<span data-ttu-id="0fb4d-169">L’exemple suivant, pris comme indiqué ci-dessus, montre comment limiter les résultats aux éléments du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-169">The following example, taken from above, demonstrates how to restrict results to file system items.</span></span> <span data-ttu-id="0fb4d-170">Notez que [**IFileDialog :: SetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) ajoute le nouvel indicateur à une valeur obtenue par le biais de [**IFileDialog :: GetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getoptions).</span><span class="sxs-lookup"><span data-stu-id="0fb4d-170">Note that [**IFileDialog::SetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) adds the new flag to a value obtained through [**IFileDialog::GetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getoptions).</span></span> <span data-ttu-id="0fb4d-171">Il s’agit de la méthode recommandée.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-171">This is the recommended method.</span></span>


```C++
                // Set the options on the dialog.
                DWORD dwFlags;

                // Before setting, always get the options first in order 
                // not to override existing options.
                hr = pfd->GetOptions(&dwFlags);
                if (SUCCEEDED(hr))
                {
                    // In this case, get shell items only for file system items.
                    hr = pfd->SetOptions(dwFlags | FOS_FORCEFILESYSTEM);
```



### <a name="specifying-file-types-for-a-dialog"></a><span data-ttu-id="0fb4d-172">Spécification des types de fichiers pour une boîte de dialogue</span><span class="sxs-lookup"><span data-stu-id="0fb4d-172">Specifying File Types for a Dialog</span></span>

<span data-ttu-id="0fb4d-173">Pour définir des types de fichiers spécifiques que la boîte de dialogue peut gérer, utilisez la méthode [**IFileDialog :: SetFileTypes**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfiletypes) .</span><span class="sxs-lookup"><span data-stu-id="0fb4d-173">To set specific file types that the dialog can handle, use the [**IFileDialog::SetFileTypes**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfiletypes) method.</span></span> <span data-ttu-id="0fb4d-174">Cette méthode accepte un tableau de structures [**COMDLG \_ FILTERSPEC**](/windows/desktop/api/Shtypes/ns-shtypes-comdlg_filterspec) , chacune représentant un type de fichier.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-174">That method accepts an array of [**COMDLG\_FILTERSPEC**](/windows/desktop/api/Shtypes/ns-shtypes-comdlg_filterspec) structures, each of which represents a file type.</span></span>

<span data-ttu-id="0fb4d-175">Le mécanisme d’extension par défaut d’une boîte de dialogue n’est pas modifié dans [**GetOpenFileName**](/windows/win32/api/commdlg/nf-commdlg-getopenfilenamea) et [**GetSaveFileName**](/windows/win32/api/commdlg/nf-commdlg-getsavefilenamea).</span><span class="sxs-lookup"><span data-stu-id="0fb4d-175">The default extension mechanism in a dialog is unchanged from [**GetOpenFileName**](/windows/win32/api/commdlg/nf-commdlg-getopenfilenamea) and [**GetSaveFileName**](/windows/win32/api/commdlg/nf-commdlg-getsavefilenamea).</span></span> <span data-ttu-id="0fb4d-176">L’extension de nom de fichier qui est ajoutée au texte que l’utilisateur tape dans la zone d’édition nom de fichier est initialisée lorsque la boîte de dialogue s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-176">The file name extension that is appended to the text the user types in the file name edit box is initialized when the dialog opens.</span></span> <span data-ttu-id="0fb4d-177">Il doit correspondre au type de fichier par défaut (sélectionné à l’ouverture de la boîte de dialogue).</span><span class="sxs-lookup"><span data-stu-id="0fb4d-177">It should match the default file type (that selected as the dialog opens).</span></span> <span data-ttu-id="0fb4d-178">Si le type de fichier par défaut est « \* . \* » (tous les fichiers), le fichier peut être une extension de votre choix.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-178">If the default file type is "\*.\*" (all files), the file can be an extension of your choice.</span></span> <span data-ttu-id="0fb4d-179">Si l’utilisateur choisit un type de fichier différent, l’extension est automatiquement mise à jour vers la première extension de nom de fichier associée à ce type de fichier.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-179">If the user chooses a different file type, the extension automatically updates to the first file name extension associated with that file type.</span></span> <span data-ttu-id="0fb4d-180">Si l’utilisateur choisit « \* . \* » (tous les fichiers), l’extension revient à sa valeur d’origine.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-180">If the user chooses "\*.\*" (all files), then the extension reverts to its original value.</span></span>

<span data-ttu-id="0fb4d-181">L’exemple suivant montre comment cela a été fait ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-181">The following example illustrates how this was done above.</span></span>


```C++
                        // Set the file types to display only. 
                        // Notice that this is a 1-based array.
                        hr = pfd->SetFileTypes(ARRAYSIZE(c_rgSaveTypes), c_rgSaveTypes);
                        if (SUCCEEDED(hr))
                        {
                            // Set the selected file type index to Word Docs for this example.
                            hr = pfd->SetFileTypeIndex(INDEX_WORDDOC);
                            if (SUCCEEDED(hr))
                            {
                                // Set the default extension to be ".doc" file.
                                hr = pfd->SetDefaultExtension(L"doc;docx");
```



### <a name="controlling-the-default-folder"></a><span data-ttu-id="0fb4d-182">Contrôle du dossier par défaut</span><span class="sxs-lookup"><span data-stu-id="0fb4d-182">Controlling the Default Folder</span></span>

<span data-ttu-id="0fb4d-183">Presque tous les dossiers de l’espace de noms Shell peuvent être utilisés comme dossier par défaut de la boîte de dialogue (le dossier présenté lorsque l’utilisateur choisit d’ouvrir ou d’enregistrer un fichier).</span><span class="sxs-lookup"><span data-stu-id="0fb4d-183">Almost any folder in the Shell namespace can be used as the default folder for the dialog (the folder presented when the user chooses to open or save a file).</span></span> <span data-ttu-id="0fb4d-184">Appelez [**IFileDialog :: SetDefaultFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setdefaultfolder) avant d’appeler [**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) pour le faire.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-184">Call [**IFileDialog::SetDefaultFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setdefaultfolder) prior to calling [**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) to do so.</span></span>

<span data-ttu-id="0fb4d-185">Le dossier par défaut est le dossier dans lequel la boîte de dialogue démarre la première fois qu’un utilisateur l’ouvre à partir de votre application.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-185">The default folder is the folder in which the dialog starts the first time a user opens it from your application.</span></span> <span data-ttu-id="0fb4d-186">Après cela, la boîte de dialogue s’ouvre dans le dernier dossier ouvert par l’utilisateur ou dans le dernier dossier utilisé pour enregistrer un élément.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-186">After that, the dialog will open in the last folder a user opened or the last folder they used to save an item.</span></span> <span data-ttu-id="0fb4d-187">Pour plus d’informations, consultez [persistance](#state-persistence) de l’État.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-187">See [State Persistence](#state-persistence) for more details.</span></span>

<span data-ttu-id="0fb4d-188">Vous pouvez forcer la boîte de dialogue à toujours afficher le même dossier lors de son ouverture, quelle que soit l’action précédente de l’utilisateur, en appelant [**IFileDialog :: SetFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfolder).</span><span class="sxs-lookup"><span data-stu-id="0fb4d-188">You can force the dialog to always show the same folder when it opens, regardless of previous user action, by calling [**IFileDialog::SetFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfolder).</span></span> <span data-ttu-id="0fb4d-189">Toutefois, nous vous déconseillons de le faire.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-189">However, we do not recommended doing this.</span></span> <span data-ttu-id="0fb4d-190">Si vous appelez **SetFolder** avant d’afficher la boîte de dialogue, l’emplacement le plus récent à partir duquel l’utilisateur a été enregistré ou ouvert n’est pas affiché.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-190">If you call **SetFolder** before you display the dialog box, the most recent location that the user saved to or opened from is not shown.</span></span> <span data-ttu-id="0fb4d-191">À moins qu’il y ait une raison très spécifique pour ce comportement, il ne s’agit pas d’une expérience utilisateur correcte ou attendue et doit être évitée.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-191">Unless there is a very specific reason for this behavior, it is not a good or expected user experience and should be avoided.</span></span> <span data-ttu-id="0fb4d-192">Dans presque toutes les instances, [**IFileDialog :: SetDefaultFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setdefaultfolder) est la meilleure méthode.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-192">In almost all instances, [**IFileDialog::SetDefaultFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setdefaultfolder) is the better method.</span></span>

<span data-ttu-id="0fb4d-193">Lorsque vous enregistrez un document pour la première fois dans la boîte de dialogue **Enregistrer** , vous devez suivre les mêmes instructions pour déterminer le dossier initial que vous avez fait dans la boîte de dialogue **ouvrir** .</span><span class="sxs-lookup"><span data-stu-id="0fb4d-193">When saving a document for the first time in the **Save** dialog, you should follow the same guidelines in determining the initial folder as you did in the **Open** dialog.</span></span> <span data-ttu-id="0fb4d-194">Si l’utilisateur modifie un document existant, ouvrez la boîte de dialogue dans le dossier où ce document est stocké, puis remplissez la zone d’édition avec le nom de ce document.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-194">If the user is editing a previously existing document, open the dialog in the folder where that document is stored, and populate the edit box with that document's name.</span></span> <span data-ttu-id="0fb4d-195">Appelez [**IFileSaveDialog :: SetSaveAsItem**](/windows/desktop/api/Shobjidl_core/nf-shobjidl_core-ifilesavedialog-setsaveasitem) avec l’élément actuel avant d’appeler [**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show).</span><span class="sxs-lookup"><span data-stu-id="0fb4d-195">Call [**IFileSaveDialog::SetSaveAsItem**](/windows/desktop/api/Shobjidl_core/nf-shobjidl_core-ifilesavedialog-setsaveasitem) with the current item prior to calling [**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show).</span></span>

### <a name="adding-items-to-the-places-bar"></a><span data-ttu-id="0fb4d-196">Ajout d’éléments à la barre des emplacements</span><span class="sxs-lookup"><span data-stu-id="0fb4d-196">Adding Items to the Places Bar</span></span>

<span data-ttu-id="0fb4d-197">L’exemple suivant illustre l’ajout d’éléments à la barre des **emplacements** :</span><span class="sxs-lookup"><span data-stu-id="0fb4d-197">The following example demonstrates the addition of items to the **Places** bar:</span></span>


```C++
HRESULT AddItemsToCommonPlaces()
{
    // CoCreate the File Open Dialog object.
    IFileDialog *pfd = NULL;
    HRESULT hr = CoCreateInstance(CLSID_FileOpenDialog, 
                      NULL, 
                      CLSCTX_INPROC_SERVER, 
                      IID_PPV_ARGS(&pfd));
    if (SUCCEEDED(hr))
    {
        // Always use known folders instead of hard-coding physical file paths.
        // In this case we are using Public Music KnownFolder.
        IKnownFolderManager *pkfm = NULL;
        hr = CoCreateInstance(CLSID_KnownFolderManager, 
                      NULL, 
                      CLSCTX_INPROC_SERVER, 
                      IID_PPV_ARGS(&pkfm));
        if (SUCCEEDED(hr))
        {
            // Get the known folder.
            IKnownFolder *pKnownFolder = NULL;
            hr = pkfm->GetFolder(FOLDERID_PublicMusic, &pKnownFolder);
            if (SUCCEEDED(hr))
            {
                // File Dialog APIs need an IShellItem that represents the location.
                IShellItem *psi = NULL;
                hr = pKnownFolder->GetShellItem(0, IID_PPV_ARGS(&psi));
                if (SUCCEEDED(hr))
                {
                    // Add the place to the bottom of default list in Common File Dialog.
                    hr = pfd->AddPlace(psi, FDAP_BOTTOM);
                    if (SUCCEEDED(hr))
                    {
                        // Show the File Dialog.
                        hr = pfd->Show(NULL);
                        if (SUCCEEDED(hr))
                        {
                            //
                            // You can add your own code here to handle the results.
                            //
                        }
                    }
                    psi->Release();
                }
                pKnownFolder->Release();
            }
            pkfm->Release();
        }
        pfd->Release();
    }
    return hr;
}
```



### <a name="state-persistence"></a><span data-ttu-id="0fb4d-198">Persistance de l’État</span><span class="sxs-lookup"><span data-stu-id="0fb4d-198">State Persistence</span></span>

<span data-ttu-id="0fb4d-199">Avant Windows Vista, un État, tel que le dernier dossier visité, a été enregistré par processus.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-199">Prior to Windows Vista, a state, such as the last visited folder, was saved on a per-process basis.</span></span> <span data-ttu-id="0fb4d-200">Toutefois, ces informations ont été utilisées indépendamment de l’action en question.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-200">However, that information was used regardless of the particular action.</span></span> <span data-ttu-id="0fb4d-201">Par exemple, une application de modification vidéo présente le même dossier dans la boîte de dialogue **Afficher** en tant que dans la boîte de dialogue **Importer un média** .</span><span class="sxs-lookup"><span data-stu-id="0fb4d-201">For example, a video editing application would present the same folder in the **Render As** dialog as is would in the **Import Media** dialog.</span></span> <span data-ttu-id="0fb4d-202">Dans Windows Vista, vous pouvez être plus précis grâce à l’utilisation de GUID.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-202">In Windows Vista you can be more specific through the use of GUIDs.</span></span> <span data-ttu-id="0fb4d-203">Pour assigner un **GUID** à la boîte de dialogue, appelez [**IFileDialog :: SetClientGuid**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setclientguid).</span><span class="sxs-lookup"><span data-stu-id="0fb4d-203">To assign a **GUID** to the dialog, call [**iFileDialog::SetClientGuid**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setclientguid).</span></span>

### <a name="multiselect-capabilities"></a><span data-ttu-id="0fb4d-204">Fonctionnalités de MultiSelect</span><span class="sxs-lookup"><span data-stu-id="0fb4d-204">Multiselect Capabilities</span></span>

<span data-ttu-id="0fb4d-205">La fonctionnalité de multisélection est disponible dans la boîte de dialogue **ouvrir** à l’aide de la méthode [**GetResults**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifileopendialog-getresults) , comme indiqué ici.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-205">Multiselect functionality is available in the **Open** dialog using the [**GetResults**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifileopendialog-getresults) method as shown here.</span></span>


```C++
HRESULT MultiselectInvoke()
{
    IFileOpenDialog *pfd;
    
    // CoCreate the dialog object.
    HRESULT hr = CoCreateInstance(CLSID_FileOpenDialog, 
                                  NULL, 
                                  CLSCTX_INPROC_SERVER, 
                                  IID_PPV_ARGS(&pfd));

    if (SUCCEEDED(hr))
    {
        DWORD dwOptions;
        // Specify multiselect.
        hr = pfd->GetOptions(&dwOptions);
        
        if (SUCCEEDED(hr))
        {
            hr = pfd->SetOptions(dwOptions | FOS_ALLOWMULTISELECT);
        }

        if (SUCCEEDED(hr))
        {
            // Show the Open dialog.
            hr = pfd->Show(NULL);

            if (SUCCEEDED(hr))
            {
                // Obtain the result of the user interaction.
                IShellItemArray *psiaResults;
                hr = pfd->GetResults(&psiaResults);
                
                if (SUCCEEDED(hr))
                {
                    //
                    // You can add your own code here to handle the results.
                    //
                    psiaResults->Release();
                }
            }
        }
        pfd->Release();
    }
    return hr;
}
```



## <a name="listening-to-events-from-the-dialog"></a><span data-ttu-id="0fb4d-206">Écoute des événements à partir de la boîte de dialogue</span><span class="sxs-lookup"><span data-stu-id="0fb4d-206">Listening to Events from the Dialog</span></span>

<span data-ttu-id="0fb4d-207">Un processus appelant peut inscrire une interface [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) avec la boîte de dialogue à l’aide des méthodes [**IFileDialog :: Advise**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-advise) et [**IFileDialog :: Unadvise**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-unadvise) comme indiqué ici.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-207">A calling process can register an [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) interface with the dialog by using the [**IFileDialog::Advise**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-advise) and [**IFileDialog::Unadvise**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-unadvise) methods as shown here.</span></span>

<span data-ttu-id="0fb4d-208">Cela est tiré de l’exemple [utilisation de base](#basic-usage) .</span><span class="sxs-lookup"><span data-stu-id="0fb4d-208">This is taken from the [Basic Usage](#basic-usage) sample.</span></span>


```C++
        // Create an event handling object, and hook it up to the dialog.
        IFileDialogEvents *pfde = NULL;
        hr = CDialogEventHandler_CreateInstance(IID_PPV_ARGS(&pfde));
        if (SUCCEEDED(hr))
        {
            // Hook up the event handler.
            DWORD dwCookie;
            hr = pfd->Advise(pfde, &dwCookie);
```



<span data-ttu-id="0fb4d-209">La majeure partie du traitement de la boîte de dialogue est placée ici.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-209">The bulk of the dialog processing would be placed here.</span></span>


```C++
                // Unhook the event handler.
                pfd->Unadvise(dwCookie);
            }
            pfde->Release();
        }
        pfd->Release();
    }
    return hr;
}
```



<span data-ttu-id="0fb4d-210">Le processus appelant peut utiliser des événements pour la notification lorsque l’utilisateur modifie le dossier, le type de fichier ou la sélection.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-210">The calling process can use events for notification when the user changes the folder, file type, or selection.</span></span> <span data-ttu-id="0fb4d-211">Ces événements sont particulièrement utiles lorsque le processus appelant a ajouté des contrôles à la boîte de dialogue (voir [Personnalisation de la boîte de dialogue](#customizing-the-dialog)) et doit modifier l’état de ces contrôles en réaction à ces événements.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-211">These events are particularly useful when the calling process has added controls to the dialog (see [Customizing the Dialog](#customizing-the-dialog)) and must change the state of those controls in reaction to these events.</span></span> <span data-ttu-id="0fb4d-212">Utile dans tous les cas, la capacité du processus appelant à fournir du code personnalisé pour gérer des situations telles que le partage de violations, le remplacement de fichiers ou la détermination de la validité d’un fichier avant la fermeture de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-212">Useful in all cases is the ability of the calling process to provide custom code to deal with situations such as sharing violations, overwriting files, or determining if a file is valid before the dialog closes.</span></span> <span data-ttu-id="0fb4d-213">Certains de ces cas sont décrits dans cette section.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-213">Some of those cases are described in this section.</span></span>

### <a name="onfileok"></a><span data-ttu-id="0fb4d-214">OnFileOk</span><span class="sxs-lookup"><span data-stu-id="0fb4d-214">OnFileOk</span></span>

<span data-ttu-id="0fb4d-215">Cette méthode est appelée une fois que l’utilisateur a choisi un élément, juste avant la fermeture de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-215">This method is called after the user chooses an item, just before the dialog closes.</span></span> <span data-ttu-id="0fb4d-216">L’application peut ensuite appeler [**IFileDialog :: GetResult**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) ou [**IFileOpenDialog :: GetResults**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifileopendialog-getresults) comme c’est le cas une fois que la boîte de dialogue a été fermée.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-216">The application can then call [**IFileDialog::GetResult**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) or [**IFileOpenDialog::GetResults**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifileopendialog-getresults) as would be done once the dialog had closed.</span></span> <span data-ttu-id="0fb4d-217">Si l’élément choisi est acceptable, il peut retourner S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-217">If the item chosen is acceptable, they can return S\_OK.</span></span> <span data-ttu-id="0fb4d-218">Dans le cas contraire, ils retournent S \_ false et affichent l’interface utilisateur qui indique à l’utilisateur la raison pour laquelle l’élément choisi n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-218">Otherwise, they return S\_FALSE and display UI that tells the user why the chosen item is not valid.</span></span> <span data-ttu-id="0fb4d-219">Si S \_ false est retourné, la boîte de dialogue ne se ferme pas.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-219">If S\_FALSE is returned, the dialog does not close.</span></span>

<span data-ttu-id="0fb4d-220">Le processus appelant peut utiliser le handle de fenêtre de la boîte de dialogue proprement dite comme parent de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-220">The calling process can use the window handle of the dialog itself as the parent of the UI.</span></span> <span data-ttu-id="0fb4d-221">Ce handle peut être obtenu en appelant [**IOleWindow :: QueryInterface**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) , puis en appelant [**IOleWindow :: GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) avec le handle comme indiqué dans cet exemple.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-221">That handle can be obtained by first calling [**IOleWindow::QueryInterface**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) and then calling [**IOleWindow::GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) with the handle as shown in this example.</span></span>


```C++
HRESULT CDialogEventHandler::OnFileOk(IFileDialog *pfd) 
{ 
    IShellItem *psiResult;
    HRESULT hr = pfd->GetResult(&psiResult);
    
    if (SUCCEEDED(hr))
    {
        SFGAOF attributes;
        hr = psiResult->GetAttributes(SFGAO_COMPRESSED, &attributes);
    
        if (SUCCEEDED(hr))
        {
            if (attributes & SFGAO_COMPRESSED)
            {
                // Accept the file.
                hr = S_OK;
            }
            else
            {
                // Refuse the file.
                hr = S_FALSE;
                
                _DisplayMessage(pfd, L"Not a compressed file.");
            }
        }
        psiResult->Release();
    }
    return hr;
};

HRESULT CDialogEventHandler::_DisplayMessage(IFileDialog *pfd, PCWSTR pszMessage)
{
    IOleWindow *pWindow;
    HRESULT hr = pfd->QueryInterface(IID_PPV_ARGS(&pWindow));
    
    if (SUCCEEDED(hr))
    {
        HWND hwndDialog;
        hr = pWindow->GetWindow(&hwndDialog);
    
        if (SUCCEEDED(hr))
        {
            MessageBox(hwndDialog, pszMessage, L"An error has occurred", MB_OK);
        }
        pWindow->Release();
    }
    return hr;
}
```



### <a name="onshareviolation-and-onoverwrite"></a><span data-ttu-id="0fb4d-222">OnShareViolation et OnOverwrite</span><span class="sxs-lookup"><span data-stu-id="0fb4d-222">OnShareViolation and OnOverwrite</span></span>

<span data-ttu-id="0fb4d-223">Si l’utilisateur choisit de remplacer un fichier dans la boîte de dialogue d' **enregistrement** , ou si un fichier enregistré ou remplacé est en cours d’utilisation et ne peut pas être écrit (violation de partage), l’application peut fournir des fonctionnalités personnalisées pour remplacer le comportement par défaut de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-223">If the user chooses to overwrite a file in the **Save** dialog, or if a file being saved or replaced is in use and cannot be written to (a sharing violation), the application can provide custom functionality to override the default behavior of the dialog.</span></span> <span data-ttu-id="0fb4d-224">Par défaut, lors du remplacement d’un fichier, la boîte de dialogue affiche une invite qui permet à l’utilisateur de vérifier cette action.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-224">By default, when overwriting a file, the dialog displays a prompt allowing the user to verify this action.</span></span> <span data-ttu-id="0fb4d-225">Pour les violations de partage, par défaut la boîte de dialogue affiche un message d’erreur, il ne se ferme pas et l’utilisateur doit faire un autre choix.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-225">For sharing violations, by default the dialog displays an error message, it does not close, and the user is required to make another choice.</span></span> <span data-ttu-id="0fb4d-226">Le processus appelant peut remplacer ces valeurs par défaut et afficher sa propre interface utilisateur si vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-226">The calling process can override these defaults and display its own UI if desired.</span></span> <span data-ttu-id="0fb4d-227">La boîte de dialogue peut être invitée à refuser le fichier et à rester ouvert ou à accepter le fichier et à se fermer avec succès.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-227">The dialog can be instructed to refuse the file and remain open or accept the file and close successfully.</span></span>

## <a name="customizing-the-dialog"></a><span data-ttu-id="0fb4d-228">Personnalisation de la boîte de dialogue</span><span class="sxs-lookup"><span data-stu-id="0fb4d-228">Customizing the Dialog</span></span>

<span data-ttu-id="0fb4d-229">Divers contrôles peuvent être ajoutés à la boîte de dialogue sans fournir de modèle de boîte de dialogue Win32.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-229">A variety of controls can be added to the dialog without supplying a Win32 dialog template.</span></span> <span data-ttu-id="0fb4d-230">Ces contrôles incluent PushButton, ComboBox, EditBox, CheckButton, les listes de RadioButton, les groupes, les séparateurs et les contrôles de texte statique.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-230">These controls include PushButton, ComboBox, EditBox, CheckButton, RadioButton lists, Groups, Separators, and Static Text controls.</span></span> <span data-ttu-id="0fb4d-231">Appelez **QueryInterface** sur l’objet Dialog ([**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog), [**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog)ou [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog)) pour obtenir un pointeur [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) .</span><span class="sxs-lookup"><span data-stu-id="0fb4d-231">Call **QueryInterface** on the dialog object ([**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog), [**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog), or [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog)) to obtain an [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) pointer.</span></span> <span data-ttu-id="0fb4d-232">Utilisez cette interface pour ajouter des contrôles.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-232">Use that interface to add controls.</span></span> <span data-ttu-id="0fb4d-233">Chaque contrôle est associé à un ID fourni par l’appelant, ainsi qu’à un état *visible* et *activé* qui peut être défini par le processus appelant.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-233">Each control has an associated caller-supplied ID as well as a *visible* and *enabled* state that can be set by the calling process.</span></span> <span data-ttu-id="0fb4d-234">Certains contrôles, tels que le bouton de commande, ont également un texte qui leur est associé.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-234">Some controls, such as PushButton, also have text associated with them.</span></span>

<span data-ttu-id="0fb4d-235">Vous pouvez ajouter plusieurs contrôles dans un « groupe visuel » qui se déplace en tant qu’unité unique dans la disposition de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-235">Multiple controls can be added into a "visual group" that moves as a single unit in the layout of the dialog.</span></span> <span data-ttu-id="0fb4d-236">Des groupes peuvent être associés à une étiquette.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-236">Groups can have a label associated with them.</span></span>

<span data-ttu-id="0fb4d-237">Les contrôles peuvent être ajoutés uniquement avant que la boîte de dialogue ne s’affiche.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-237">Controls can be added only before the dialog is shown.</span></span> <span data-ttu-id="0fb4d-238">Toutefois, une fois la boîte de dialogue affichée, les contrôles peuvent être masqués ou affichés comme vous le souhaitez, peut-être en réponse à une action de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-238">However, once the dialog is displayed, controls can be hidden or shown as desired, perhaps in response to user action.</span></span> <span data-ttu-id="0fb4d-239">Les exemples suivants montrent comment ajouter une liste de cases d’option à la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-239">The following examples show how to add a radio button list to the dialog.</span></span>


```C++
// Controls
#define CONTROL_GROUP           2000
#define CONTROL_RADIOBUTTONLIST 2
#define CONTROL_RADIOBUTTON1    1
#define CONTROL_RADIOBUTTON2    2       // It is OK for this to have the same ID
                    // as CONTROL_RADIOBUTTONLIST, because it 
                    // is a child control under CONTROL_RADIOBUTTONLIST


// This code snippet demonstrates how to add custom controls in the Common File Dialog.
HRESULT AddCustomControls()
{
    // CoCreate the File Open Dialog object.
    IFileDialog *pfd = NULL;
    HRESULT hr = CoCreateInstance(CLSID_FileOpenDialog, 
                                  NULL, 
                                  CLSCTX_INPROC_SERVER, 
                                  IID_PPV_ARGS(&pfd));
    if (SUCCEEDED(hr))
    {
        // Create an event handling object, and hook it up to the dialog.
        IFileDialogEvents   *pfde       = NULL;
        DWORD               dwCookie    = 0;
        hr = CDialogEventHandler_CreateInstance(IID_PPV_ARGS(&pfde));
        if (SUCCEEDED(hr))
        {
            // Hook up the event handler.
            hr = pfd->Advise(pfde, &dwCookie);
            if (SUCCEEDED(hr))
            {
                // Set up a Customization.
                IFileDialogCustomize *pfdc = NULL;
                hr = pfd->QueryInterface(IID_PPV_ARGS(&pfdc));
                if (SUCCEEDED(hr))
                {
                    // Create a Visual Group.
                    hr = pfdc->StartVisualGroup(CONTROL_GROUP, L&quot;Sample Group&quot;);
                    if (SUCCEEDED(hr))
                    {
                        // Add a radio-button list.
                        hr = pfdc->AddRadioButtonList(CONTROL_RADIOBUTTONLIST);
                        if (SUCCEEDED(hr))
                        {
                            // Set the state of the added radio-button list.
                            hr = pfdc->SetControlState(CONTROL_RADIOBUTTONLIST, 
                                               CDCS_VISIBLE | CDCS_ENABLED);
                            if (SUCCEEDED(hr))
                            {
                                // Add individual buttons to the radio-button list.
                                hr = pfdc->AddControlItem(CONTROL_RADIOBUTTONLIST,
                                                          CONTROL_RADIOBUTTON1,
                                                          L&quot;Change Title to ABC&quot;);
                                if (SUCCEEDED(hr))
                                {
                                    hr = pfdc->AddControlItem(CONTROL_RADIOBUTTONLIST,
                                                              CONTROL_RADIOBUTTON2,
                                                              L&quot;Change Title to XYZ&quot;);
                                    if (SUCCEEDED(hr))
                                    {
                                        // Set the default selection to option 1.
                                        hr = pfdc->SetSelectedControlItem(CONTROL_RADIOBUTTONLIST,
                                                                          CONTROL_RADIOBUTTON1);
                                    }
                                }
                            }
                        }
                        // End the visual group.
                        pfdc->EndVisualGroup();
                    }
                    pfdc->Release();
                }

                if (FAILED(hr))
                {
                    // Unadvise here in case we encounter failures 
                    // before we get a chance to show the dialog.
                    pfd->Unadvise(dwCookie);
                }
            }
            pfde->Release();
        }

        if (SUCCEEDED(hr))
        {
            // Now show the dialog.
            hr = pfd->Show(NULL);
            if (SUCCEEDED(hr))
            {
                //
                // You can add your own code here to handle the results.
                //
            }
            // Unhook the event handler.
            pfd->Unadvise(dwCookie);
        }
        pfd->Release();
    }
    return hr;
}
```





### <a name="adding-options-to-the-ok-button"></a><span data-ttu-id="0fb4d-240">Ajout d’options au bouton OK</span><span class="sxs-lookup"><span data-stu-id="0fb4d-240">Adding Options to the OK Button</span></span>

<span data-ttu-id="0fb4d-241">De même, vous pouvez ajouter des choix aux boutons **ouvrir** ou **Enregistrer** , qui sont le bouton **OK** pour leurs types de boîtes de dialogue respectifs.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-241">Similarly, choices can be added to the **Open** or **Save** buttons, which are the **OK** button for their respective dialog types.</span></span> <span data-ttu-id="0fb4d-242">Les options sont accessibles par le biais d’une zone de liste déroulante associée au bouton.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-242">The options are accessible through a drop-down list box attached to the button.</span></span> <span data-ttu-id="0fb4d-243">Le premier élément de la liste devient le texte du bouton.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-243">The first item in the list becomes the text for the button.</span></span> <span data-ttu-id="0fb4d-244">L’exemple suivant montre comment fournir un bouton **ouvrir** avec deux possibilités : « ouvrir » et « ouvrir en lecture seule ».</span><span class="sxs-lookup"><span data-stu-id="0fb4d-244">The following example shows how to provide an **Open** button with two possibilities: "Open" and "Open as read-only".</span></span>


```C++
// OpenChoices options
#define OPENCHOICES 0
#define OPEN 0
#define OPEN_AS_READONLY 1


HRESULT AddOpenChoices()
{
    // CoCreate the File Open Dialog object.
    IFileDialog *pfd = NULL;
    HRESULT hr = CoCreateInstance(CLSID_FileOpenDialog, 
                      NULL, 
                      CLSCTX_INPROC_SERVER, 
                      IID_PPV_ARGS(&pfd));
    if (SUCCEEDED(hr))
    {
        // Create an event handling object, and hook it up to the dialog.
        IFileDialogEvents   *pfde       = NULL;
        DWORD               dwCookie    = 0;
        hr = CDialogEventHandler_CreateInstance(IID_PPV_ARGS(&pfde));
        if (SUCCEEDED(hr))
        {
            // Hook up the event handler.
            hr = pfd->Advise(pfde, &dwCookie);
            if (SUCCEEDED(hr))
            {
                // Set up a Customization.
                IFileDialogCustomize *pfdc = NULL;
                hr = pfd->QueryInterface(IID_PPV_ARGS(&pfdc));
                if (SUCCEEDED(hr))
                {
                    hr = pfdc->EnableOpenDropDown(OPENCHOICES);
                    if (SUCCEEDED(hr))
                    {
                        hr = pfdc->AddControlItem(OPENCHOICES, OPEN, L&quot;&Open&quot;);
                    }                    
                    if (SUCCEEDED(hr))
                    {
                        hr = pfdc->AddControlItem(OPENCHOICES, 
                                                OPEN_AS_READONLY, 
                                                L&quot;Open as &read-only&quot;);
                    }
                    if (SUCCEEDED(hr))
                    {
                        pfd->Show(NULL);
                    }
                }
                pfdc->Release();
            }
            pfd->Unadvise(dwCookie);
        }
        pfde->Release();
    }
    pfd->Release();
    return hr;
}
```





<span data-ttu-id="0fb4d-245">Le choix de l’utilisateur peut être vérifié une fois que la boîte de dialogue a été retournée par la méthode [**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) comme vous le feriez pour un contrôle ComboBox, ou elle peut être vérifiée dans le cadre de la gestion par [**IFileDialogEvents :: OnFileOk**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogevents-onfileok).</span><span class="sxs-lookup"><span data-stu-id="0fb4d-245">The user's choice can be verified after the dialog returns from the [**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) method as you would for a ComboBox, or it can verified as part of the handling by [**IFileDialogEvents::OnFileOk**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogevents-onfileok).</span></span>

### <a name="responding-to-events-in-added-controls"></a><span data-ttu-id="0fb4d-246">Réponse aux événements dans les contrôles ajoutés</span><span class="sxs-lookup"><span data-stu-id="0fb4d-246">Responding to Events in Added Controls</span></span>

<span data-ttu-id="0fb4d-247">Le gestionnaire d’événements fourni par le processus appelant peut implémenter [**IFileDialogControlEvents**](/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents) en plus de [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents).</span><span class="sxs-lookup"><span data-stu-id="0fb4d-247">The events handler provided by the calling process can implement [**IFileDialogControlEvents**](/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents) in addition to [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents).</span></span> <span data-ttu-id="0fb4d-248">**IFileDialogControlEvents** permet au processus appelant de réagir à ces événements :</span><span class="sxs-lookup"><span data-stu-id="0fb4d-248">**IFileDialogControlEvents** enables the calling process to react to these events:</span></span>

-   <span data-ttu-id="0fb4d-249">Clic de bouton de bouton</span><span class="sxs-lookup"><span data-stu-id="0fb4d-249">PushButton clicked</span></span>
-   <span data-ttu-id="0fb4d-250">État de CheckButton modifié</span><span class="sxs-lookup"><span data-stu-id="0fb4d-250">CheckButton state changed</span></span>
-   <span data-ttu-id="0fb4d-251">Élément sélectionné dans une liste de menus, ComboBox ou RadioButton</span><span class="sxs-lookup"><span data-stu-id="0fb4d-251">Item selected from a menu, ComboBox, or RadioButton list</span></span>
-   <span data-ttu-id="0fb4d-252">Contrôle d’activation.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-252">Control activating.</span></span> <span data-ttu-id="0fb4d-253">Il est envoyé lorsqu’un menu est sur le paragraphe pour afficher une liste déroulante, au cas où le processus appelant souhaite modifier les éléments de la liste.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-253">This is sent when a menu is about to display a drop-down list, in case the calling process wants to change the items in the list.</span></span>

## <a name="full-samples"></a><span data-ttu-id="0fb4d-254">Exemples complets</span><span class="sxs-lookup"><span data-stu-id="0fb4d-254">Full Samples</span></span>

<span data-ttu-id="0fb4d-255">Voici des exemples C++ complets et téléchargeables du kit de développement logiciel (SDK) Windows, qui illustrent l’utilisation de et de l’interaction avec la boîte de dialogue d’élément commune.</span><span class="sxs-lookup"><span data-stu-id="0fb4d-255">The following are complete, downloadable C++ samples from the Windows Software Development Kit (SDK) which demonstrate the use of and interaction with the Common Item Dialog.</span></span>

-   [<span data-ttu-id="0fb4d-256">Boîte de dialogue de fichier courante, exemple</span><span class="sxs-lookup"><span data-stu-id="0fb4d-256">Common File Dialog Sample</span></span>](samples-commonfiledialog.md)
-   [<span data-ttu-id="0fb4d-257">Modes de boîte de dialogue de fichier courante, exemple</span><span class="sxs-lookup"><span data-stu-id="0fb4d-257">Common File Dialog Modes Sample</span></span>](samples-commonfiledialogmodes.md)

## <a name="related-topics"></a><span data-ttu-id="0fb4d-258">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0fb4d-258">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0fb4d-259">**IID \_ PPV \_ args**</span><span class="sxs-lookup"><span data-stu-id="0fb4d-259">**IID\_PPV\_ARGS**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args)
</dt> </dl>

 

 
