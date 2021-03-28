---
description: La saisie semi-automatique développe des chaînes qui ont été entrées partiellement dans un contrôle d’édition dans des chaînes complètes.
title: Utilisation de la saisie semi-automatique
ms.topic: article
ms.date: 05/31/2018
ms.assetid: b990395b-fc10-48f9-a718-7cc006e37eb7
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: fbbf0c53fc1b26002d1b46a9a6a6f67cd15e3ead
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972083"
---
# <a name="using-autocomplete"></a><span data-ttu-id="6bb04-103">Utilisation de la saisie semi-automatique</span><span class="sxs-lookup"><span data-stu-id="6bb04-103">Using Autocomplete</span></span>

<span data-ttu-id="6bb04-104">La saisie semi-automatique développe des chaînes qui ont été entrées partiellement dans un [contrôle d’édition](/windows/desktop/Controls/edit-controls) dans des chaînes complètes.</span><span class="sxs-lookup"><span data-stu-id="6bb04-104">Autocompletion expands strings that have been partially entered in an [edit control](/windows/desktop/Controls/edit-controls) into complete strings.</span></span> <span data-ttu-id="6bb04-105">Par exemple, lorsqu’un utilisateur commence à entrer une URL dans le contrôle d’édition d’adresse qui est incorporé dans la barre d’outils de Windows Internet Explorer, la saisie semi-automatique développe la chaîne en une ou plusieurs options d’URL complètes qui sont cohérentes avec la chaîne partielle existante.</span><span class="sxs-lookup"><span data-stu-id="6bb04-105">For example, when a user starts to enter a URL in the Address edit control that is embedded in the Windows Internet Explorer toolbar, autocompletion expands the string into one or more complete URL options that are consistent with the existing partial string.</span></span> <span data-ttu-id="6bb04-106">Une chaîne d’URL partielle telle que « MIC » peut être développée en « https://www.microsoft.com » ou «» https://www.microsoft.com/windows .</span><span class="sxs-lookup"><span data-stu-id="6bb04-106">A partial URL string such as "mic" might be expanded to "https://www.microsoft.com" or "https://www.microsoft.com/windows".</span></span> <span data-ttu-id="6bb04-107">La saisie semi-automatique est généralement utilisée avec les contrôles d’édition ou avec les contrôles qui disposent d’un contrôle d’édition incorporé, tel que le contrôle [ComboBoxEx](/windows/desktop/Controls/comboboxex-control-reference) .</span><span class="sxs-lookup"><span data-stu-id="6bb04-107">Autocompletion is typically used with edit controls or with controls that have an embedded edit control, such as the [ComboBoxEx](/windows/desktop/Controls/comboboxex-control-reference) control.</span></span>

## <a name="adding-autocomplete-functionality-to-your-application"></a><span data-ttu-id="6bb04-108">Ajout de la fonctionnalité de saisie semi-automatique à votre application</span><span class="sxs-lookup"><span data-stu-id="6bb04-108">Adding Autocomplete Functionality to Your Application</span></span>

<span data-ttu-id="6bb04-109">Une application peut ajouter la fonctionnalité de saisie semi-automatique à un contrôle d’édition de deux manières :</span><span class="sxs-lookup"><span data-stu-id="6bb04-109">An application can add autocomplete functionality to an edit control in two ways:</span></span>

-   <span data-ttu-id="6bb04-110">[**SHAutoComplete**](/windows/desktop/api/shlwapi/nf-shlwapi-shautocomplete) est une fonction simple qui peut remplir de façon automatique un chemin ou une URL de fichier.</span><span class="sxs-lookup"><span data-stu-id="6bb04-110">[**SHAutoComplete**](/windows/desktop/api/shlwapi/nf-shlwapi-shautocomplete) is a simple function that can autocomplete a file path or URL.</span></span>
-   <span data-ttu-id="6bb04-111">L’interface [**IAutoComplete**](/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete) est exposée par l’objet de saisie semi-automatique (CLSID \_ automatique).</span><span class="sxs-lookup"><span data-stu-id="6bb04-111">[**IAutoComplete**](/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete) interface is exposed by the autocomplete object (CLSID\_AutoComplete).</span></span> <span data-ttu-id="6bb04-112">Elle permet aux applications d’initialiser, d’activer et de désactiver l’objet.</span><span class="sxs-lookup"><span data-stu-id="6bb04-112">It allows applications to initialize, enable, and disable the object.</span></span> <span data-ttu-id="6bb04-113">**IAutoComplete** offre davantage de contrôle sur les sources de saisie semi-automatique, y compris la possibilité d’ajouter une source personnalisée.</span><span class="sxs-lookup"><span data-stu-id="6bb04-113">**IAutoComplete** allows more control over autocomplete sources, including the ability to add a custom source.</span></span> <span data-ttu-id="6bb04-114">Le reste de cette rubrique traite de l’utilisation de **IAutoComplete**.</span><span class="sxs-lookup"><span data-stu-id="6bb04-114">The remainder of this topic discusses the use of **IAutoComplete**.</span></span> <span data-ttu-id="6bb04-115">Consultez [Comment activer la saisie semi-automatique manuellement](how-to-enable-autocomplete-manually.md) pour obtenir des exemples d’utilisation spécifiques.</span><span class="sxs-lookup"><span data-stu-id="6bb04-115">See [How To Enable Autocomplete Manually](how-to-enable-autocomplete-manually.md) for specific usage examples.</span></span>

## <a name="autocomplete-modes"></a><span data-ttu-id="6bb04-116">Modes de saisie semi-automatique</span><span class="sxs-lookup"><span data-stu-id="6bb04-116">Autocomplete Modes</span></span>

<span data-ttu-id="6bb04-117">Lorsque vous utilisez [**IAutoComplete**](/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete), la saisie semi-automatique peut afficher la chaîne terminée dans deux modes : ajout automatique et suggestion automatique.</span><span class="sxs-lookup"><span data-stu-id="6bb04-117">When using [**IAutoComplete**](/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete), autocompletion can display the completed string in two modes: autoappend and autosuggest.</span></span> <span data-ttu-id="6bb04-118">Les modes sont indépendants. vous pouvez activer l’un ou l’autre ou les deux.</span><span class="sxs-lookup"><span data-stu-id="6bb04-118">The modes are independent; you can enable either or both.</span></span> <span data-ttu-id="6bb04-119">Pour spécifier le mode, appelez [**IAutoComplete2 :: SetOptions**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-setoptions).</span><span class="sxs-lookup"><span data-stu-id="6bb04-119">To specify the mode, call [**IAutoComplete2::SetOptions**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-setoptions).</span></span>

<dl> <dt>

<span data-ttu-id="6bb04-120"><span id="Autoappend"></span><span id="autoappend"></span><span id="AUTOAPPEND"></span>Ajout</span><span class="sxs-lookup"><span data-stu-id="6bb04-120"><span id="Autoappend"></span><span id="autoappend"></span><span id="AUTOAPPEND"></span>Autoappend</span></span>
</dt> <dd>

<span data-ttu-id="6bb04-121">En mode d’ajout automatique, la saisie semi-automatique ajoute le reste de la chaîne candidate la plus probable aux caractères existants, en mettant en surbrillance les caractères ajoutés.</span><span class="sxs-lookup"><span data-stu-id="6bb04-121">In autoappend mode, autocompletion appends the remainder of the most likely candidate string to the existing characters, highlighting the appended characters.</span></span> <span data-ttu-id="6bb04-122">Si l’utilisateur continue à entrer des caractères, ceux-ci sont ajoutés à la chaîne partielle existante.</span><span class="sxs-lookup"><span data-stu-id="6bb04-122">If the user continues to enter characters, they are added to the existing partial string.</span></span> <span data-ttu-id="6bb04-123">Si l’utilisateur ajoute un caractère identique au caractère suivant mis en surbrillance, la mise en surbrillance de ce caractère est désactivée.</span><span class="sxs-lookup"><span data-stu-id="6bb04-123">If the user adds a character that is identical to the next highlighted character, the highlighting for that character is turned off.</span></span> <span data-ttu-id="6bb04-124">Les autres caractères seront toujours mis en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="6bb04-124">The remaining characters will still be highlighted.</span></span> <span data-ttu-id="6bb04-125">Si l’utilisateur ajoute un caractère qui ne correspond pas au caractère suivant en surbrillance, la saisie semi-automatique tente de générer une nouvelle chaîne candidate basée sur la plus grande chaîne partielle et ajoute le reste de la nouvelle chaîne candidate à la chaîne partielle actuelle.</span><span class="sxs-lookup"><span data-stu-id="6bb04-125">If the user adds a character that does not match the next highlighted character, autocompletion attempts to generate a new candidate string based on the larger partial string and appends the remainder of the new candidate string to the current partial string.</span></span> <span data-ttu-id="6bb04-126">Si aucune chaîne candidate n’est trouvée, seuls les caractères typés apparaissent et la zone d’édition se comporte comme elle le ferait sans la saisie semi-automatique.</span><span class="sxs-lookup"><span data-stu-id="6bb04-126">If no candidate string can be found, only the typed characters appear and the edit box behaves as it would without autocompletion.</span></span> <span data-ttu-id="6bb04-127">Ce processus se poursuit jusqu’à ce que l’utilisateur accepte une chaîne.</span><span class="sxs-lookup"><span data-stu-id="6bb04-127">This process continues until the user accepts a string.</span></span>

</dd> <dt>

<span data-ttu-id="6bb04-128"><span id="Autosuggest"></span><span id="autosuggest"></span><span id="AUTOSUGGEST"></span>Suggestion automatique</span><span class="sxs-lookup"><span data-stu-id="6bb04-128"><span id="Autosuggest"></span><span id="autosuggest"></span><span id="AUTOSUGGEST"></span>Autosuggest</span></span>
</dt> <dd>

<span data-ttu-id="6bb04-129">Dans le mode de suggestion automatique, la saisie semi-automatique affiche une liste déroulante, avec une ou plusieurs chaînes complètes suggérées, sous le contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="6bb04-129">In autosuggest mode, autocompletion displays a drop-down list, with one or more suggested complete strings, beneath the edit control.</span></span> <span data-ttu-id="6bb04-130">L’utilisateur peut sélectionner l’une des chaînes suggérées ou continuer à taper.</span><span class="sxs-lookup"><span data-stu-id="6bb04-130">The user can select one of the suggested strings or continue typing.</span></span> <span data-ttu-id="6bb04-131">Au fur et à mesure de la saisie, la liste déroulante peut être modifiée en fonction de la chaîne partielle actuelle.</span><span class="sxs-lookup"><span data-stu-id="6bb04-131">As typing progresses, the drop-down list might be modified based on the current partial string.</span></span> <span data-ttu-id="6bb04-132">Si vous définissez l' \_ indicateur de recherche réglementaires dans [**IAutoComplete2 :: SetOptions**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-setoptions), la saisie semi-automatique fournit une option, en bas de la liste déroulante, pour rechercher la chaîne partielle actuelle.</span><span class="sxs-lookup"><span data-stu-id="6bb04-132">If you set the ACO\_SEARCH flag in [**IAutoComplete2::SetOptions**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-setoptions), autocomplete provides an option, at the bottom of the drop-down list, to search for the current partial string.</span></span> <span data-ttu-id="6bb04-133">Cette option s’affiche même s’il n’y a pas de chaînes suggérées.</span><span class="sxs-lookup"><span data-stu-id="6bb04-133">This option is displayed even if there are no suggested strings.</span></span> <span data-ttu-id="6bb04-134">Si l’utilisateur sélectionne l’option de recherche, votre application doit lancer un moteur de recherche pour aider l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6bb04-134">If the user selects the search option, your application should launch a search engine to assist the user.</span></span>

</dd> </dl>

## <a name="using-predefined-autocomplete-sources"></a><span data-ttu-id="6bb04-135">Utilisation de sources de saisie semi-automatique prédéfinies</span><span class="sxs-lookup"><span data-stu-id="6bb04-135">Using Predefined Autocomplete Sources</span></span>

<span data-ttu-id="6bb04-136">La saisie semi-automatique dépend d’une source qui lui fournit des chaînes à faire correspondre à la chaîne partielle de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6bb04-136">Autocompletion depends on having a source that provides it with strings to match against the user's partial string.</span></span> <span data-ttu-id="6bb04-137">Vous avez la possibilité de fournir une source de saisie semi-automatique personnalisée, mais plusieurs des sources les plus courantes sont fournies par le système.</span><span class="sxs-lookup"><span data-stu-id="6bb04-137">You have the option of providing a custom autocomplete source, but several of the most common sources are provided by the system.</span></span>

<dl> <dt>

<span data-ttu-id="6bb04-138"><span id="CLSID_ACLHistory"></span><span id="clsid_aclhistory"></span><span id="CLSID_ACLHISTORY"></span>CLSID \_ ACLHistory</span><span class="sxs-lookup"><span data-stu-id="6bb04-138"><span id="CLSID_ACLHistory"></span><span id="clsid_aclhistory"></span><span id="CLSID_ACLHISTORY"></span>CLSID\_ACLHistory</span></span>
</dt> <dd>

<span data-ttu-id="6bb04-139">Source de saisie semi-automatique qui correspond à la liste d’URL dans la liste historique de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6bb04-139">An autocomplete source that matches against the URL list in the user's History list.</span></span>

</dd> <dt>

<span data-ttu-id="6bb04-140"><span id="CLSID_ACLMRU"></span><span id="clsid_aclmru"></span>CLSID \_ ACLMRU</span><span class="sxs-lookup"><span data-stu-id="6bb04-140"><span id="CLSID_ACLMRU"></span><span id="clsid_aclmru"></span>CLSID\_ACLMRU</span></span>
</dt> <dd>

<span data-ttu-id="6bb04-141">Source de saisie semi-automatique qui correspond à la liste d’URL dans la liste des derniers fichiers utilisés.</span><span class="sxs-lookup"><span data-stu-id="6bb04-141">An autocomplete source that matches against the URL list in the user's Recently Used list.</span></span>

</dd> <dt>

<span data-ttu-id="6bb04-142"><span id="CLSID_ACListISF"></span><span id="clsid_aclistisf"></span><span id="CLSID_ACLISTISF"></span>CLSID \_ ACListISF</span><span class="sxs-lookup"><span data-stu-id="6bb04-142"><span id="CLSID_ACListISF"></span><span id="clsid_aclistisf"></span><span id="CLSID_ACLISTISF"></span>CLSID\_ACListISF</span></span>
</dt> <dd>

<span data-ttu-id="6bb04-143">Source de saisie semi-automatique qui correspond aux éléments de l’espace de noms de l’interpréteur de commandes : les fichiers sur l’ordinateur de l’utilisateur et les éléments dans les dossiers virtuels tels que le panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="6bb04-143">An autocomplete source that matches against items in the Shell namespace: files on the user's computer as well as items in virtual folders such as Control Panel.</span></span>

</dd> </dl>

<span data-ttu-id="6bb04-144">Dans certains cas, au lieu de libérer immédiatement les ressources, vous souhaiterez peut-être conserver les pointeurs d’interface vers les différents objets impliqués dans la saisie semi-automatique.</span><span class="sxs-lookup"><span data-stu-id="6bb04-144">There are occasions when, rather than immediately freeing the resources, you might want to retain the interface pointers to the various objects involved in autocomplete.</span></span> <span data-ttu-id="6bb04-145">En particulier, cette opération est effectuée lorsque vous souhaitez ajuster dynamiquement le comportement de la saisie semi-automatique.</span><span class="sxs-lookup"><span data-stu-id="6bb04-145">In particular, this is done when you want to adjust the autocomplete behavior dynamically.</span></span> <span data-ttu-id="6bb04-146">L’instance la plus courante de cela se produit lors de l’utilisation de l' \_ objet CLSID ACListISF, qui se termine à partir de l’espace de noms Shell et a l’option ([**ACLO \_ CURRENTDIR**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2)) de l’énumération à partir du répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="6bb04-146">The most common instance of this occurs when using the CLSID\_ACListISF object, which autocompletes from the Shell namespace and has the option ([**ACLO\_CURRENTDIR**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2)) of enumerating from the current directory as well.</span></span> <span data-ttu-id="6bb04-147">Par exemple, lorsque vous accédez à un nouveau dossier, Internet Explorer modifie le répertoire actuel de la barre d’adresses et les paramètres doivent donc être modifiés dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="6bb04-147">For example, when you navigate to a new folder, Internet Explorer changes the Address bar's current directory and therefore the settings need to be changed dynamically.</span></span> <span data-ttu-id="6bb04-148">Il existe deux façons de spécifier le répertoire que l' \_ objet ACLISTISF CLSID doit traiter en tant que répertoire actif :</span><span class="sxs-lookup"><span data-stu-id="6bb04-148">There are two ways to specify the directory that the CLSID\_ACListISF object should treat as the current directory:</span></span>

-   <span data-ttu-id="6bb04-149">[**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) spécifie le répertoire via un [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist).</span><span class="sxs-lookup"><span data-stu-id="6bb04-149">[**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) specifies the directory through an [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist).</span></span>
-   <span data-ttu-id="6bb04-150">[**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory) spécifie le répertoire par le biais d’une chaîne de chemin.</span><span class="sxs-lookup"><span data-stu-id="6bb04-150">[**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory) specifies the directory through a path string.</span></span>

<span data-ttu-id="6bb04-151">Dans l’exemple suivant, supposons que **PAL** est un pointeur vers l’interface [**IACList**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist) d’un \_ objet CLSID ACListISF :</span><span class="sxs-lookup"><span data-stu-id="6bb04-151">In the following, assume that **pal** is a pointer to the [**IACList**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist) interface of a CLSID\_ACListISF object:</span></span>

-   <span data-ttu-id="6bb04-152">Utilisation de [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder):</span><span class="sxs-lookup"><span data-stu-id="6bb04-152">Using [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder):</span></span>

    <span data-ttu-id="6bb04-153">Pour indiquer à l' \_ objet CLSID ACListISF qu’un [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) particulier doit être traité comme le répertoire actif, vous pouvez utiliser l’interface [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6bb04-153">To tell the CLSID\_ACListISF object that a particular [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) should be treated as the current directory, you can use the object's [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) interface.</span></span> <span data-ttu-id="6bb04-154">Étant donné qu’un **ITEMIDLIST** peut faire référence à un dossier virtuel, cette méthode est plus souple que l’utilisation de [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory).</span><span class="sxs-lookup"><span data-stu-id="6bb04-154">Since an **ITEMIDLIST** can refer to a virtual folder, this method is more flexible than using [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory).</span></span>

    <span data-ttu-id="6bb04-155">Notez que les exemples suivants utilisent l’appel de procédure QueryInterface, qui permet une liste de paramètres simplifiée.</span><span class="sxs-lookup"><span data-stu-id="6bb04-155">Note that the following examples use the templatized QueryInterface, which allows for a simplified parameter list.</span></span>

    ```C++
    IPersistFolder *ppf;

    hr = pal2->QueryInterface(IID_PPV_ARGS(&ppf));   
    if (SUCCEEDED(hr))
    {
        hr = ppf->Initialize(pidlCurrentDirectory);
        ppf->Release();
    }
    ```

    

-   <span data-ttu-id="6bb04-156">Utilisation de [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory):</span><span class="sxs-lookup"><span data-stu-id="6bb04-156">Using [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory):</span></span>

    <span data-ttu-id="6bb04-157">Pour attribuer à l' \_ objet CLSID ACListISF un chemin d’accès en tant que répertoire actif, vous pouvez utiliser l’interface [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6bb04-157">To give the CLSID\_ACListISF object a path as the current directory, you can use the object's [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory) interface.</span></span>

    ```C++
    WCHAR pwszDirectory[MAX_PATH] = L"C:\\Program Files";
    ICurrentWorkingDirectory *pcwd;

    hr = pal2->QueryInterface(IID_PPV_ARGS(&pcwd));    
    if (SUCCEEDED(hr))
    {
        hr = pcwd->SetDirectory(pwszDirectory);
        pcwd->Release();
    }
    ```

    

 

 
