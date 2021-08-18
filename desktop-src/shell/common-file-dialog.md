---
description: à partir de Windows Vista, la boîte de dialogue élément commun remplace l’ancienne boîte de dialogue de fichier courant lorsqu’elle est utilisée pour ouvrir ou enregistrer un fichier.
title: Boîte de dialogue élément commun
ms.topic: article
ms.date: 05/31/2018
ms.assetid: f8846148-89a5-4b9b-ad68-56137a5c2f65
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 2956bf7329ff9c92b777199d040d1275aa827cfa9ea9c8bfbec175d234b204f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943519"
---
# <a name="common-item-dialog"></a>Boîte de dialogue élément commun

à partir de Windows Vista, la boîte de dialogue élément commun remplace l’ancienne boîte de dialogue de fichier courant lorsqu’elle est utilisée pour ouvrir ou enregistrer un fichier. La boîte de dialogue élément commun est utilisée dans deux variantes : la boîte de dialogue **ouvrir** et la boîte de dialogue **Enregistrer** . Ces deux boîtes de dialogue partagent la plupart de leurs fonctionnalités, mais chacune possède ses propres méthodes uniques.

Bien que cette version plus récente s’intitule la boîte de dialogue élément commun, elle continue d’être appelée boîte de dialogue de fichier commune dans la plupart des documents. à moins que vous ne traitiez spécifiquement avec une version antérieure de Windows, vous devez supposer que toute mention de la boîte de dialogue de fichier commune fait référence à cette boîte de dialogue d’élément commune.

Les rubriques suivantes sont présentées ici :

-   [IFileDialog, IFileOpenDialog et IFileSaveDialog](#ifiledialog-ifileopendialog-and-ifilesavedialog)
    -   [Exemple d’utilisation](#sample-usage)
-   [Écoute des événements à partir de la boîte de dialogue](#listening-to-events-from-the-dialog)
    -   [OnFileOk](#onfileok)
    -   [OnShareViolation et OnOverwrite](#onshareviolation-and-onoverwrite)
-   [Personnalisation de la boîte de dialogue](#customizing-the-dialog)
    -   [Ajout d’options au bouton OK](#adding-options-to-the-ok-button)
    -   [Réponse aux événements dans les contrôles ajoutés](#responding-to-events-in-added-controls)
-   [Exemples complets](#full-samples)
-   [Rubriques connexes](#related-topics)

## <a name="ifiledialog-ifileopendialog-and-ifilesavedialog"></a>IFileDialog, IFileOpenDialog et IFileSaveDialog

Windows Vista fournit des implémentations des boîtes de dialogue **ouvrir** et **Enregistrer** : CLSID \_ FileOpenDialog et \_ CLSID FileSaveDialog. Ces boîtes de dialogue sont affichées ici.

![capture d’écran de la boîte de dialogue Ouvrir](images/cid/openfiledialog.png)

![capture d’écran de la boîte de dialogue Enregistrer sous](images/cid/savefiledialog.png)

[**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) et [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog) héritent de [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) et partagent une grande partie de leur fonctionnalité. En outre, la boîte de dialogue **ouvrir** prend en charge **IFileOpenDialog** et la boîte de dialogue **Enregistrer** prend en charge **IFileSaveDialog**.

l’implémentation de la boîte de dialogue d’élément commune trouvée dans Windows Vista offre plusieurs avantages par rapport à l’implémentation fournie dans les versions antérieures :

-   Prend en charge l’utilisation directe de l’espace de noms Shell via [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) au lieu d’utiliser des chemins d’accès de système de fichiers.
-   Active la personnalisation simple de la boîte de dialogue, telle que la définition de l’étiquette sur le bouton **OK** , sans nécessiter de procédure de raccordement.
-   Prend en charge une personnalisation plus complète de la boîte de dialogue en ajoutant un ensemble de contrôles pilotés par les données qui fonctionnent sans modèle de boîte de dialogue Win32. Ce schéma de personnalisation libère le processus appelant de la disposition de l’interface utilisateur. Étant donné que les modifications apportées à la conception de la boîte de dialogue continuent à utiliser ce modèle de données, l’implémentation de la boîte de dialogue n’est pas liée à la version actuelle spécifique de la boîte de dialogue.
-   Prend en charge la notification de l’appelant des événements dans la boîte de dialogue, tels que la modification de la sélection ou la modification du type de fichier. Permet également au processus appelant de raccorder certains événements dans la boîte de dialogue, tels que l’analyse.
-   Introduit de nouvelles fonctionnalités de boîte de dialogue telles que l’ajout d’emplacements spécifiés par l’appelant à la barre des **emplacements** .
-   dans la boîte de dialogue **enregistrer** , les développeurs peuvent tirer parti des nouvelles fonctionnalités de métadonnées du Shell Windows Vista.

En outre, les développeurs peuvent choisir d’implémenter les interfaces suivantes :

-   [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) pour recevoir des notifications d’événements dans la boîte de dialogue.
-   [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) pour ajouter des contrôles à la boîte de dialogue.
-   [**IFileDialogControlEvents**](/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents) pour être informé des événements dans ces contrôles ajoutés.

La boîte de dialogue **ouvrir** ou **Enregistrer** retourne un objet [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) ou [**IShellItemArray**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray) au processus appelant. L’appelant peut ensuite utiliser un objet **IShellItem** individuel pour obtenir un chemin d’accès au système de fichiers ou ouvrir un flux sur l’élément pour lire ou écrire des informations.

Les indicateurs et les options disponibles pour les nouvelles méthodes de dialogue sont très similaires aux anciens indicateurs **OFN** trouvés dans la structure [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) et utilisés dans [**GetOpenFileName**](/windows/win32/api/commdlg/nf-commdlg-getopenfilenamea) et [**GetSaveFileName**](/windows/win32/api/commdlg/nf-commdlg-getsavefilenamea). Un grand nombre d’entre eux sont exactement les mêmes, sauf qu’ils commencent par un préfixe FOS. La liste complète se trouve dans les rubriques [**IFileDialog :: GetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getoptions) et [**IFileDialog :: SetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) . Les boîtes de dialogue **ouvrir** et **Enregistrer** sont créées par défaut avec les indicateurs les plus courants. Pour la boîte de dialogue **ouvrir** , il s’agit de (FOS \_ PATHMUSTEXIST \| Fos \_ FILEMUSTEXIST \| Fos \_ NOCHANGEDIR) et, pour la boîte de dialogue **Enregistrer** , il s’agit de (FOS \_ \| \_ \| \_ \| \_ OVERWRITEPROMPT Fos NOREADONLYRETURN Fos PATHMUSTEXIST Fos NOCHANGEDIR).

[**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) et ses interfaces descendantes héritent de et étendent [**IModalWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imodalwindow). L' [**affichage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) prend comme seul paramètre le handle de la fenêtre parente. Si **Show** aboutit, il y a un résultat valide. Si elle retourne `HRESULT_FROM_WIN32(ERROR_CANCELLED)` , cela signifie que l’utilisateur a annulé la boîte de dialogue. Elle peut également retourner légitimement un autre code d’erreur tel que **E \_ OUTOFMEMORY**.

### <a name="sample-usage"></a>Exemple d’utilisation

Les sections suivantes présentent un exemple de code pour diverses tâches de dialogue.

-   [Utilisation de base](#basic-usage)
-   [Limiter les résultats aux éléments du système de fichiers](#limiting-results-to-file-system-items)
-   [Spécification des types de fichiers pour une boîte de dialogue](#specifying-file-types-for-a-dialog)
-   [Contrôle du dossier par défaut](#controlling-the-default-folder)
-   [Ajout d’éléments à la barre des emplacements](#adding-items-to-the-places-bar)
-   [Persistance de l’État](#state-persistence)
-   [Fonctionnalités de MultiSelect](#multiselect-capabilities)

la plupart des exemples de code se trouvent dans l' [exemple de boîte de dialogue de fichier commun](samples-commonfiledialog.md)SDK Windows.

### <a name="basic-usage"></a>Utilisation de base

L’exemple suivant montre comment lancer une boîte de dialogue **ouverte** . dans cet exemple, il est limité à Microsoft Word documents.

> [!Note]  
> Plusieurs exemples de cette rubrique utilisent la `CDialogEventHandler_CreateInstance` fonction d’assistance pour créer une instance de l’implémentation de [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) . Pour utiliser cette fonction dans votre propre code, copiez le code source de la `CDialogEventHandler_CreateInstance` fonction à partir de l' [exemple de boîte de dialogue de fichier commune](samples-commonfiledialog.md), à partir duquel tous les exemples de cette rubrique sont pris.

 


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



### <a name="limiting-results-to-file-system-items"></a>Limiter les résultats aux éléments du système de fichiers

L’exemple suivant, pris comme indiqué ci-dessus, montre comment limiter les résultats aux éléments du système de fichiers. Notez que [**IFileDialog :: SetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) ajoute le nouvel indicateur à une valeur obtenue par le biais de [**IFileDialog :: GetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getoptions). Il s’agit de la méthode recommandée.


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



### <a name="specifying-file-types-for-a-dialog"></a>Spécification des types de fichiers pour une boîte de dialogue

Pour définir des types de fichiers spécifiques que la boîte de dialogue peut gérer, utilisez la méthode [**IFileDialog :: SetFileTypes**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfiletypes) . Cette méthode accepte un tableau de structures [**COMDLG \_ FILTERSPEC**](/windows/desktop/api/Shtypes/ns-shtypes-comdlg_filterspec) , chacune représentant un type de fichier.

Le mécanisme d’extension par défaut d’une boîte de dialogue n’est pas modifié dans [**GetOpenFileName**](/windows/win32/api/commdlg/nf-commdlg-getopenfilenamea) et [**GetSaveFileName**](/windows/win32/api/commdlg/nf-commdlg-getsavefilenamea). L’extension de nom de fichier qui est ajoutée au texte que l’utilisateur tape dans la zone d’édition nom de fichier est initialisée lorsque la boîte de dialogue s’ouvre. Il doit correspondre au type de fichier par défaut (sélectionné à l’ouverture de la boîte de dialogue). Si le type de fichier par défaut est « \* . \* » (tous les fichiers), le fichier peut être une extension de votre choix. Si l’utilisateur choisit un type de fichier différent, l’extension est automatiquement mise à jour vers la première extension de nom de fichier associée à ce type de fichier. Si l’utilisateur choisit « \* . \* » (tous les fichiers), l’extension revient à sa valeur d’origine.

L’exemple suivant montre comment cela a été fait ci-dessus.


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



### <a name="controlling-the-default-folder"></a>Contrôle du dossier par défaut

Presque tous les dossiers de l’espace de noms Shell peuvent être utilisés comme dossier par défaut de la boîte de dialogue (le dossier présenté lorsque l’utilisateur choisit d’ouvrir ou d’enregistrer un fichier). Appelez [**IFileDialog :: SetDefaultFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setdefaultfolder) avant d’appeler [**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) pour le faire.

Le dossier par défaut est le dossier dans lequel la boîte de dialogue démarre la première fois qu’un utilisateur l’ouvre à partir de votre application. Après cela, la boîte de dialogue s’ouvre dans le dernier dossier ouvert par l’utilisateur ou dans le dernier dossier utilisé pour enregistrer un élément. Pour plus d’informations, consultez [persistance](#state-persistence) de l’État.

Vous pouvez forcer la boîte de dialogue à toujours afficher le même dossier lors de son ouverture, quelle que soit l’action précédente de l’utilisateur, en appelant [**IFileDialog :: SetFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfolder). Toutefois, nous vous déconseillons de le faire. Si vous appelez **SetFolder** avant d’afficher la boîte de dialogue, l’emplacement le plus récent à partir duquel l’utilisateur a été enregistré ou ouvert n’est pas affiché. À moins qu’il y ait une raison très spécifique pour ce comportement, il ne s’agit pas d’une expérience utilisateur correcte ou attendue et doit être évitée. Dans presque toutes les instances, [**IFileDialog :: SetDefaultFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setdefaultfolder) est la meilleure méthode.

Lorsque vous enregistrez un document pour la première fois dans la boîte de dialogue **Enregistrer** , vous devez suivre les mêmes instructions pour déterminer le dossier initial que vous avez fait dans la boîte de dialogue **ouvrir** . Si l’utilisateur modifie un document existant, ouvrez la boîte de dialogue dans le dossier où ce document est stocké, puis remplissez la zone d’édition avec le nom de ce document. Appelez [**IFileSaveDialog :: SetSaveAsItem**](/windows/desktop/api/Shobjidl_core/nf-shobjidl_core-ifilesavedialog-setsaveasitem) avec l’élément actuel avant d’appeler [**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show).

### <a name="adding-items-to-the-places-bar"></a>Ajout d’éléments à la barre des emplacements

L’exemple suivant illustre l’ajout d’éléments à la barre des **emplacements** :


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



### <a name="state-persistence"></a>Persistance de l’État

avant Windows Vista, un état, tel que le dernier dossier visité, a été enregistré par processus. Toutefois, ces informations ont été utilisées indépendamment de l’action en question. Par exemple, une application de modification vidéo présente le même dossier dans la boîte de dialogue **Afficher** en tant que dans la boîte de dialogue **Importer un média** . dans Windows Vista, vous pouvez être plus précis grâce à l’utilisation de guid. Pour assigner un **GUID** à la boîte de dialogue, appelez [**IFileDialog :: SetClientGuid**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setclientguid).

### <a name="multiselect-capabilities"></a>Fonctionnalités de MultiSelect

La fonctionnalité de multisélection est disponible dans la boîte de dialogue **ouvrir** à l’aide de la méthode [**GetResults**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifileopendialog-getresults) , comme indiqué ici.


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



## <a name="listening-to-events-from-the-dialog"></a>Écoute des événements à partir de la boîte de dialogue

Un processus appelant peut inscrire une interface [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) avec la boîte de dialogue à l’aide des méthodes [**IFileDialog :: Advise**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-advise) et [**IFileDialog :: Unadvise**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-unadvise) comme indiqué ici.

Cela est tiré de l’exemple [utilisation de base](#basic-usage) .


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



La majeure partie du traitement de la boîte de dialogue est placée ici.


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



Le processus appelant peut utiliser des événements pour la notification lorsque l’utilisateur modifie le dossier, le type de fichier ou la sélection. Ces événements sont particulièrement utiles lorsque le processus appelant a ajouté des contrôles à la boîte de dialogue (voir [Personnalisation de la boîte de dialogue](#customizing-the-dialog)) et doit modifier l’état de ces contrôles en réaction à ces événements. Utile dans tous les cas, la capacité du processus appelant à fournir du code personnalisé pour gérer des situations telles que le partage de violations, le remplacement de fichiers ou la détermination de la validité d’un fichier avant la fermeture de la boîte de dialogue. Certains de ces cas sont décrits dans cette section.

### <a name="onfileok"></a>OnFileOk

Cette méthode est appelée une fois que l’utilisateur a choisi un élément, juste avant la fermeture de la boîte de dialogue. L’application peut ensuite appeler [**IFileDialog :: GetResult**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) ou [**IFileOpenDialog :: GetResults**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifileopendialog-getresults) comme c’est le cas une fois que la boîte de dialogue a été fermée. Si l’élément choisi est acceptable, il peut retourner S \_ OK. Dans le cas contraire, ils retournent S \_ false et affichent l’interface utilisateur qui indique à l’utilisateur la raison pour laquelle l’élément choisi n’est pas valide. Si S \_ false est retourné, la boîte de dialogue ne se ferme pas.

Le processus appelant peut utiliser le handle de fenêtre de la boîte de dialogue proprement dite comme parent de l’interface utilisateur. Ce handle peut être obtenu en appelant [**IOleWindow :: QueryInterface**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) , puis en appelant [**IOleWindow :: GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) avec le handle comme indiqué dans cet exemple.


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



### <a name="onshareviolation-and-onoverwrite"></a>OnShareViolation et OnOverwrite

Si l’utilisateur choisit de remplacer un fichier dans la boîte de dialogue d' **enregistrement** , ou si un fichier enregistré ou remplacé est en cours d’utilisation et ne peut pas être écrit (violation de partage), l’application peut fournir des fonctionnalités personnalisées pour remplacer le comportement par défaut de la boîte de dialogue. Par défaut, lors du remplacement d’un fichier, la boîte de dialogue affiche une invite qui permet à l’utilisateur de vérifier cette action. Pour les violations de partage, par défaut la boîte de dialogue affiche un message d’erreur, il ne se ferme pas et l’utilisateur doit faire un autre choix. Le processus appelant peut remplacer ces valeurs par défaut et afficher sa propre interface utilisateur si vous le souhaitez. La boîte de dialogue peut être invitée à refuser le fichier et à rester ouvert ou à accepter le fichier et à se fermer avec succès.

## <a name="customizing-the-dialog"></a>Personnalisation de la boîte de dialogue

Divers contrôles peuvent être ajoutés à la boîte de dialogue sans fournir de modèle de boîte de dialogue Win32. Ces contrôles incluent PushButton, ComboBox, EditBox, CheckButton, les listes de RadioButton, les groupes, les séparateurs et les contrôles de texte statique. Appelez **QueryInterface** sur l’objet Dialog ([**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog), [**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog)ou [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog)) pour obtenir un pointeur [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) . Utilisez cette interface pour ajouter des contrôles. Chaque contrôle est associé à un ID fourni par l’appelant, ainsi qu’à un état *visible* et *activé* qui peut être défini par le processus appelant. Certains contrôles, tels que le bouton de commande, ont également un texte qui leur est associé.

Vous pouvez ajouter plusieurs contrôles dans un « groupe visuel » qui se déplace en tant qu’unité unique dans la disposition de la boîte de dialogue. Des groupes peuvent être associés à une étiquette.

Les contrôles peuvent être ajoutés uniquement avant que la boîte de dialogue ne s’affiche. Toutefois, une fois la boîte de dialogue affichée, les contrôles peuvent être masqués ou affichés comme vous le souhaitez, peut-être en réponse à une action de l’utilisateur. Les exemples suivants montrent comment ajouter une liste de cases d’option à la boîte de dialogue.


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





### <a name="adding-options-to-the-ok-button"></a>Ajout d’options au bouton OK

De même, vous pouvez ajouter des choix aux boutons **ouvrir** ou **Enregistrer** , qui sont le bouton **OK** pour leurs types de boîtes de dialogue respectifs. Les options sont accessibles par le biais d’une zone de liste déroulante associée au bouton. Le premier élément de la liste devient le texte du bouton. L’exemple suivant montre comment fournir un bouton **ouvrir** avec deux possibilités : « ouvrir » et « ouvrir en lecture seule ».


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





Le choix de l’utilisateur peut être vérifié une fois que la boîte de dialogue a été retournée par la méthode [**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) comme vous le feriez pour un contrôle ComboBox, ou elle peut être vérifiée dans le cadre de la gestion par [**IFileDialogEvents :: OnFileOk**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogevents-onfileok).

### <a name="responding-to-events-in-added-controls"></a>Réponse aux événements dans les contrôles ajoutés

Le gestionnaire d’événements fourni par le processus appelant peut implémenter [**IFileDialogControlEvents**](/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents) en plus de [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents). **IFileDialogControlEvents** permet au processus appelant de réagir à ces événements :

-   Clic de bouton de bouton
-   État de CheckButton modifié
-   Élément sélectionné dans une liste de menus, ComboBox ou RadioButton
-   Contrôle d’activation. Il est envoyé lorsqu’un menu est sur le paragraphe pour afficher une liste déroulante, au cas où le processus appelant souhaite modifier les éléments de la liste.

## <a name="full-samples"></a>Exemples complets

voici des exemples C++ complets et téléchargeables du kit de développement logiciel (SDK) Windows qui illustrent l’utilisation de et de l’interaction avec la boîte de dialogue d’élément commune.

-   [Boîte de dialogue de fichier courante, exemple](samples-commonfiledialog.md)
-   [Modes de boîte de dialogue de fichier courante, exemple](samples-commonfiledialogmodes.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IID \_ PPV \_ args**](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args)
</dt> </dl>

 

 
