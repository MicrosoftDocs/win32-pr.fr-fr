---
description: Cette rubrique décrit quelques éléments à prendre en compte lors de l’utilisation de bibliothèques dans votre programme.
ms.assetid: 40ACC8F6-1416-4390-A8D7-8F924DC2C2FE
title: Utilisation de bibliothèques dans votre programme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b2c76c4ce8bf9114d7294b257c03bcc62adecc947a3d7e651d6f94fa8876d4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821109"
---
# <a name="using-libraries-in-your-program"></a>Utilisation de bibliothèques dans votre programme

Cette rubrique décrit quelques éléments à prendre en compte lors de l’utilisation de bibliothèques dans votre programme.

Dans cette rubrique :

-   [Vue d’ensemble de la programmation de bibliothèque](#library-programming-overview)
-   [Programmation à l’aide de bibliothèques](#programming-with-libraries)
    -   [Passage de dossiers connus aux bibliothèques](#moving-from-known-folders-to-libraries)
    -   [Groupes résidentiels et bibliothèques partagées](#homegroup-and-shared-libraries)
-   [Utilisation d’une boîte de dialogue de fichier commune avec des bibliothèques](#using-a-common-file-dialog-box-with-libraries)
-   [Activation de la sélection de la bibliothèque à partir de l’interface utilisateur](#enabling-library-selection-from-the-user-interface)
-   [Accès au contenu de la bibliothèque dans un programme](#accessing-library-content-in-a-program)
    -   [Accès au contenu de la bibliothèque avec l’interface IShellLibrary](#accessing-library-content-with-the-ishelllibrary-interface)
    -   [Accès au contenu de la bibliothèque à l’aide des API Shell](#accessing-library-content-with-the-shell-apis)
-   [Enregistrement du contenu utilisateur dans une bibliothèque](#saving-user-content-in-a-library)
-   [Prise en charge des opérations de glisser-déplacer dans une bibliothèque](#supporting-drag-and-drop-operations-in-a-library)
-   [Maintien de la synchronisation avec une bibliothèque](#keeping-in-sync-with-a-library)
    -   [Mise à jour en bloc](#bulk-update)
    -   [Notification de l’API Shell](#shell-api-notification)
    -   [Notification de l’API du système de fichiers](#file-system-api-notification)
-   [Rubriques connexes](#related-topics)

## <a name="library-programming-overview"></a>Vue d’ensemble de la programmation de bibliothèque

Les bibliothèques permettent aux utilisateurs d’organiser leurs contenus basés sur des fichiers d’une façon qui leur est significative et qui ne sont pas limités par l’organisation du système de fichiers. lorsque votre programme prend en charge les bibliothèques, il permet à l’utilisateur de trouver son contenu d’une manière qui lui semble logique tout en présentant une interface utilisateur qui est cohérente avec l’expérience utilisateur Windows 7. Les bibliothèques permettent également à votre programme de localiser plus facilement le contenu basé sur des fichiers qui est stocké dans différents dossiers ou sur des ordinateurs différents.

Les rubriques de cette section décrivent comment vous pouvez ajouter la prise en charge de bibliothèque à votre programme et tirer parti des nouvelles fonctionnalités offertes par les bibliothèques. Windows 7 fournit une partie de cette prise en charge par défaut. Si votre programme ne modifie pas les boîtes de dialogue de fichier courantes qu’il utilise actuellement, il peut nécessiter très peu de programmation supplémentaire pour prendre en charge les bibliothèques.

Cette section décrit certaines des fonctionnalités clés fournies par les bibliothèques et comment les prendre en charge dans votre programme. Grâce à ces informations, vous pouvez choisir les fonctionnalités qui offriront la meilleure expérience utilisateur à partir de votre programme. si votre programme personnalise les boîtes de dialogue de fichier courantes, les informations contenues dans cette section peuvent vous aider à déterminer comment utiliser les nouvelles boîtes de dialogue de fichier courantes pour utiliser des bibliothèques et fournir des fonctionnalités équivalentes dans Windows 7.

## <a name="programming-with-libraries"></a>Programmation à l’aide de bibliothèques

le modèle de programmation Windows shell décrit comment un programme interagit avec des objets de programmation Windows shell. alors que les objets de système de fichiers, tels que les fichiers et les répertoires, sont représentés par Windows objets shell, les objets shell Windows ne sont pas tous représentés par le système de fichiers. par exemple, les bibliothèques sont Windows des objets Shell qui n’ont pas d’équivalent de système de fichiers. l’utilisation d’Windows objets shell dans votre programme permet à votre programme d’accéder à tous les objets shell et pas uniquement aux objets de système de fichiers.

Pour obtenir les meilleurs résultats, votre programme utilise l' [**API de la bibliothèque de shells**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) pour interagir avec les bibliothèques et accéder à leur contenu. Les bibliothèques contiennent des éléments de système de fichiers tels que des dossiers et des fichiers, mais pas des éléments de système de fichiers. Ainsi, les API du système de fichiers ne peuvent pas être utilisées pour accéder aux fonctionnalités ou au contenu de la bibliothèque.

Si vous disposez déjà d’un programme qui utilise de nombreuses API du système de fichiers, votre programme peut toujours tirer parti des fonctionnalités de la bibliothèque. L' [**API de la bibliothèque de shells**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) peut fournir des références de système de fichiers aux éléments qui se trouvent dans une bibliothèque, et ces références de système de fichiers, telles que le nom de fichier et le chemin d’accès, peuvent être passées aux API de système de fichiers existantes qui se trouvent dans votre programme existant.

### <a name="moving-from-known-folders-to-libraries"></a>Passage de dossiers connus aux bibliothèques

avant le Windows 7, il était courant d’utiliser un dossier connu, tel que le dossier mes Documents, comme dossier par défaut dans les opérations d’enregistrement ou d’ouverture de fichier. dans Windows 7, la bibliothèque correspondante doit être utilisée pour que l’utilisateur dispose de la même expérience dans votre programme qu’avec d’autres programmes Windows 7, tels que l’explorateur de Windows.

si vous utilisez actuellement l’API Windows Shell dans votre programme, l’ajout de la prise en charge de bibliothèque est simple. Par exemple, si vous appelez actuellement la fonction [**SHGetKnownFolderItem**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderitem) pour obtenir l’emplacement du dossier Mes documents, vous pouvez remplacer la valeur [**KNOWNFOLDERID**](knownfolderid.md) du dossier connu mes documents par la valeur **KNOWNFOLDERID** de la bibliothèque correspondante.

le tableau suivant montre la relation entre les valeurs [**KNOWNFOLDERID**](knownfolderid.md) des dossiers connus et la valeur **KNOWNFOLDERID** de la bibliothèque correspondante dans Windows 7. 

| Valeurs KNOWNFOLDERID de dossier connues | Valeurs KNOWNFOLDERID de la bibliothèque |
|-----------------------------------|------------------------------|
| \_Documents FOLDERID               | FOLDERID \_ DocumentsLibrary   |
| \_Images FOLDERID                | FOLDERID \_ PicturesLibrary    |
| FOLDERID \_ Musique                   | FOLDERID \_ MusicLibrary       |
| FOLDERID \_ RecordedTV              | FOLDERID \_ RecordedTVLibrary  |



 

### <a name="homegroup-and-shared-libraries"></a>Groupes résidentiels et bibliothèques partagées

L’ajout de la prise en charge de bibliothèque à votre programme permet la prise en charge des bibliothèques partagées dans un groupe résidentiel. Le groupe résidentiel est identifié par sa valeur [**KNOWNFOLDERID**](knownfolderid.md) de [**\_ groupe résidentiel FOLDERID**](knownfolderid.md). Votre programme peut identifier l’emplacement d’enregistrement par défaut privé ou partagé de l’utilisateur en définissant la valeur [**DEFAULTSAVEFOLDERTYPE**](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-defaultsavefoldertype) dans l’appel à la méthode [**IShellLibrary :: GetDefaultSaveFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllibrary-getdefaultsavefolder) .

## <a name="using-a-common-file-dialog-box-with-libraries"></a>Utilisation d’une boîte de dialogue de fichier commune avec des bibliothèques

utilisation d’une boîte de dialogue de fichier commune avec des bibliothèques la boîte de dialogue fichier courant a été mise à jour pour prendre en charge les bibliothèques dans Windows 7. l’illustration suivante montre comment la boîte de dialogue fichier commun s’affiche à un utilisateur dans Windows 7.

![capture d’écran de la boîte de dialogue fichier courant avec les bibliothèques](images/libraries-commonfiledialog.png)

dans Windows 7, si votre programme affiche actuellement une boîte de dialogue de fichier commune et ne modifie pas le modèle de boîte de dialogue ou ne raccorde aucun de ses événements, il affiche automatiquement la nouvelle version de Windows 7 de la boîte de dialogue. Plus précisément, dans l’appel à la fonction de boîte de dialogue de fichier commune, les membres **lpfnHook**, **HINSTANCE**, **lpTemplatename** de la structure [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) doivent avoir la **valeur null** et les indicateurs **OFN \_ ENABLEHOOK** et **OFN \_ ENABLETEMPLATE** doivent être clairs.

dans Windows 7, les interfaces associées à [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog)remplacent les fonctions de boîte de dialogue de fichier courantes qui ont été utilisées dans les versions antérieures de Windows. les fonctions de la boîte de dialogue de fichier courantes précédentes sont toujours prises en charge dans Windows 7, mais elles ne fournissent pas l’expérience utilisateur complète de Windows 7 et ne prennent pas en charge les bibliothèques. Voici quelques-unes des nouvelles fonctionnalités prises en charge par les interfaces associées à **IFileDialog**:

-   l’utilisateur peut accéder aux propriétés de fichier prises en charge par le Windows 7 Windows Explorer pour rechercher et sélectionner les fichiers.
-   Le programme peut utiliser des interfaces et des méthodes de l’API de l’espace de noms du Shell pour travailler avec les éléments.
-   Le programme peut utiliser un modèle de personnalisation piloté par les données au lieu d’un modèle de personnalisation piloté par des fichiers de ressources pour ajouter de nouveaux contrôles aux boîtes de dialogue de fichier courantes.

Vous devez utiliser les interfaces relatives à [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog)dans les cas suivants :

-   vous devez personnaliser la boîte de dialogue fichier commun de votre programme dans Windows 7. Cela permettra à votre programme de travailler avec des bibliothèques et de prendre en charge la personnalisation de votre boîte de dialogue.
-   vous souhaitez que l’utilisateur puisse sélectionner plusieurs fichiers dans une boîte de dialogue fichier commun. Cela garantit que vous obtiendrez les chemins d’accès corrects à l’objet sélectionné, car une bibliothèque peut avoir du contenu stocké dans des dossiers différents.

Pour plus d’informations sur les interfaces associées à [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog), consultez :

-   [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog)
-   [**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog)
-   [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog)
-   [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize)
-   [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents)
-   [**IFileDialogControlEvents**](/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents)

## <a name="enabling-library-selection-from-the-user-interface"></a>Activation de la sélection de la bibliothèque à partir de l’interface utilisateur

si votre programme permet à l’utilisateur de sélectionner un dossier, par exemple pour les fonctions d’importation ou d’exportation, dans Windows 7, il doit permettre à l’utilisateur de sélectionner également une bibliothèque. L’interface [**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) et la fonction [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) permettent à l’utilisateur de sélectionner une bibliothèque lorsque vous êtes invité à sélectionner un dossier. l’interface **IFileOpenDialog** est préférable à la fonction **SHBrowseForFolder** , car **IFileOpenDialog** prend en charge l’interface utilisateur Windows 7.

Pour permettre aux utilisateurs de sélectionner des dossiers lors de l’utilisation de l’interface [**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) , appelez SetOptions avec l’indicateur Fos PICKFOLDERS défini et assurez-vous \_ que l' \_ indicateur Fos FORCEFILESYSTEM est désactivé.


```C++
FILEOPENDIALOGOPTIONS fileOptions;

hr = fileOpenDialogBox->GetOptions(&fileOptions);
fileOptions = fileOptions | FOS_PICKFOLDERS | ~FOS_FORCEFILESYSTEM;
hr = fileOpenDialogBox->SetOptions(fileOptions);
```



Pour permettre aux utilisateurs de sélectionner des dossiers lors de l’appel de la fonction SHBrowseForFolder, dans le membre ulFlags de la structure [**BROWSEINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa) , définissez l' \_ indicateur BIF USENEWUI et décochez l' \_ indicateur BIF RETURNONLYFSDIRS.


```C++
BROWSEINFO    browseInfo;
browseInfo.ulFlags = BIF_USENEWUI | ~BIF_RETURNONLYFSDIRS;
// Set other member values
pidl = SHBrowseForFolder(&browseInfo);
```



## <a name="accessing-library-content-in-a-program"></a>Accès au contenu de la bibliothèque dans un programme

pour accéder au contenu d’une bibliothèque, vous devez utiliser l’API Windows Shell. Les fonctions de l’API du système de fichiers ne peuvent pas être utilisées pour accéder au contenu de la bibliothèque, car les bibliothèques ne sont pas des objets de système de fichiers. Si votre programme utilise un Explorateur de fichiers personnalisé basé sur l’API du système de fichiers, il ne pourra pas parcourir les bibliothèques ou accéder au contenu de la bibliothèque.

Cette section décrit la façon dont vous pouvez accéder au contenu de la bibliothèque afin de pouvoir sélectionner la meilleure façon de mettre à jour votre programme pour qu’il fonctionne avec les bibliothèques.

### <a name="accessing-library-content-with-the-ishelllibrary-interface"></a>Accès au contenu de la bibliothèque avec l’interface IShellLibrary

Le moyen le plus simple pour un programme d’accéder au contenu de la bibliothèque consiste à utiliser l’API de bibliothèque de l' [**interpréteur**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary)de commandes. Si vous travaillez sur un programme qui utilise l’API de système de fichiers, l' **API de bibliothèque de Shell** peut retourner les dossiers de système de fichiers d’une bibliothèque, ce qui réduit la modification apportée à votre code de programme existant.


```C++
IShellLibrary *picturesLibrary;

hr = SHLoadLibraryFromKnownFolder(FOLDERID_PicturesLibrary, 
                                  STGM_READ, 
                                  IID_PPV_ARGS(&picturesLibrary));

// picturesLibrary now points to the user's picture library
    
IShellItemArray *pictureFolders; 

hr = pslLibrary->GetFolders(LFF_FORCEFILESYSTEM, IID_PPV_ARGS(&pictureFolders));

// pictureFolders now contains an array of Shell items that
// represent the folders found in the user's pictures library
```



### <a name="accessing-library-content-with-the-shell-apis"></a>Accès au contenu de la bibliothèque à l’aide des API Shell

étant donné que les objets de bibliothèque font partie du modèle de programmation de l’interpréteur de commandes, ils peuvent être utilisés avec d’autres api Windows shell. Par exemple, vous pouvez utiliser les interfaces [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) et [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) dans votre programme, ainsi que les fonctions d’assistance associées, pour accéder au contenu d’une bibliothèque de la même façon que vous énumérez les dossiers et le contenu du dossier pour accéder au contenu avec les API du système de fichiers.

les api Shell Windows prennent en charge deux modes d’énumération pour accéder au contenu d’une bibliothèque :

-   **Parcourir l’énumération**

    L’énumération Browse est le mode d’énumération par défaut et énumère le contenu d’un dossier de bibliothèque. Désactivez \_ l' \_ indicateur d’énumération de navigation SHCONTF pour utiliser ce mode.

-   **Énumération de navigation**

    L’énumération de navigation énumère les dossiers de bibliothèque. Définissez l' \_ \_ indicateur d’énumération de navigation SHCONTF pour utiliser ce mode.

si votre programme utilise un contrôle d’arborescence personnalisé pour naviguer dans les dossiers de l’utilisateur, l’énumération des dossiers en mode d’énumération de navigation vous donnera une liste des dossiers d’une bibliothèque qui est cohérente avec la manière dont l’explorateur de Windows énumère les dossiers dans Windows 7.

pour obtenir des exemples d’utilisation de ces fonctionnalités dans un programme, consultez l’exemple ShellStorage dans le SDK Windows.

## <a name="saving-user-content-in-a-library"></a>Enregistrement du contenu utilisateur dans une bibliothèque

Votre programme peut enregistrer le contenu de l’utilisateur dans une bibliothèque et dans un dossier de la bibliothèque. De même, l’utilisateur peut enregistrer dans un dossier spécifique d’une bibliothèque, ou il peut simplement enregistrer dans la bibliothèque.

Chaque bibliothèque a un dossier qui est désigné comme emplacement d’enregistrement par défaut. L’emplacement d’enregistrement par défaut est défini lors de la création de la bibliothèque. Toutefois, l’utilisateur peut réassigner l’emplacement d’enregistrement par défaut à n’importe quel dossier de la bibliothèque. Bien que l’utilisateur n’ait pas besoin de configurer un emplacement d’enregistrement par défaut, il a la possibilité de le modifier. Si l’utilisateur supprime le dossier actuellement défini comme emplacement d’enregistrement par défaut, la bibliothèque configure automatiquement le dossier suivant dans la bibliothèque comme emplacement d’enregistrement par défaut.

Vous pouvez enregistrer le contenu utilisateur dans une bibliothèque de plusieurs manières.

-   **API Shell**

    Si vous utilisez le modèle de programmation de l’interpréteur de commandes et enregistrez un élément de Shell, tel que représenté par un [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem), IStorage ou IStream, sur un objet de bibliothèque, l’élément de Shell sera automatiquement stocké dans l’emplacement d’enregistrement par défaut de la bibliothèque.

-   **API du système de fichiers**

    Si vous disposez d’un programme existant qui utilise de nombreux appels d’API de système de fichiers, vous pouvez obtenir un chemin d’accès au dossier défini en tant qu’emplacement d’enregistrement par défaut de la bibliothèque. Le chemin d’accès au dossier peut ensuite être passé à une API de système de fichiers.

pour obtenir des exemples d’utilisation de ces fonctionnalités dans un programme, consultez l’exemple ShellStorage dans le SDK Windows.

## <a name="supporting-drag-and-drop-operations-in-a-library"></a>Prise en charge des opérations de glisser-déplacer dans une bibliothèque

Si votre programme prend en charge les actions de glisser-déplacer, celles-ci doivent être mises à jour pour prendre en charge l’interaction de bibliothèque correcte. Si un fichier est supprimé dans une bibliothèque, le fichier supprimé doit être enregistré dans l’emplacement d’enregistrement par défaut. Si un dossier est déposé dans une bibliothèque, le dossier supprimé doit être ajouté en tant que nouveau dossier à la bibliothèque. Si un fichier est déplacé dans un dossier existant qui n’est pas l’emplacement d’enregistrement par défaut, le fichier doit être ajouté au dossier sélectionné.

pour obtenir des exemples d’ajout de la prise en charge de bibliothèque pour la fonctionnalité glisser-déplacer de vos programmes, consultez l’exemple ShellLibraryCommandLine dans le SDK Windows.

## <a name="keeping-in-sync-with-a-library"></a>Maintien de la synchronisation avec une bibliothèque

Cette rubrique décrit comment un programme peut conserver son affichage du contenu d’une bibliothèque à jour.

### <a name="bulk-update"></a>Mise à jour en bloc

Étant donné que l’utilisateur peut modifier les dossiers d’une bibliothèque de manière interactive lorsque votre programme n’est pas en cours d’exécution, votre programme doit appeler [**SHResolveLibrary**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shresolvelibrary) lorsqu’il commence à détecter et à stocker les modifications apportées à la bibliothèque. L’API Shell fournit la fonction **SHResolveLibrary** pour permettre à un programme d’obtenir le contenu actuel d’une bibliothèque et les emplacements actuels des dossiers que la bibliothèque peut contenir.

Notez que [**SHResolveLibrary**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shresolvelibrary) est une fonction de blocage qui peut prendre beaucoup de temps pour être retournée en fonction de ce qui a changé dans la bibliothèque. Par conséquent, il ne doit pas être appelé à partir d’un thread d’interface utilisateur.

Une fois le programme mis à jour, il peut s’inscrire aux notifications de modification pour conserver une vue actuelle.

### <a name="shell-api-notification"></a>Notification de l’API Shell

l’API Windows Shell fournit la fonction [**SHChangeNotifyRegister**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotifyregister) , qui est la méthode recommandée pour que les processus de non-service soient avertis d’une modification dans la bibliothèque.

pour détecter les modifications apportées aux éléments d’une bibliothèque à l’aide de l’API Windows Shell, appelez [**SHChangeNotifyRegister**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotifyregister) pour inscrire votre programme afin de recevoir des notifications des modifications apportées aux éléments d’un dossier de bibliothèque. Cette fonction peut notifier votre programme s’il y a une modification dans une bibliothèque ou dans une bibliothèque spécifique. Les notifications sont envoyées immédiatement lorsqu’une bibliothèque est modifiée.

### <a name="file-system-api-notification"></a>Notification de l’API du système de fichiers

Les notifications de système de fichiers doivent être utilisées dans les processus de service.

Pour détecter les modifications apportées aux éléments d’une bibliothèque à l’aide de l’API du système de fichiers, énumérez les dossiers dans la bibliothèque et appelez [**FindFirstChangeNotification**](/windows/win32/api/fileapi/nf-fileapi-findfirstchangenotificationa) pour chaque dossier à surveiller. Votre programme recevra une notification lors de la modification d’un dossier surveillé. Pour rechercher le fichier spécifique des fichiers qui ont été modifiés dans le dossier, appelez [**ReadDirectoryChangesW**](/windows/win32/api/winbase/nf-winbase-readdirectorychangesw). Pour détecter les modifications apportées au fichier de description de la bibliothèque, surveillez le dossier qui le contient. Le fichier de description de la bibliothèque se trouve dans le dossier [**FOLDERID \_ Libraries**](knownfolderid.md) . Toutefois, le fichier de description de la bibliothèque ne doit pas être ouvert ou modifié.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos des bibliothèques](library-leverage-to-manage-folders.md)
</dt> <dt>

[**IShellLibrary**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary)
</dt> <dt>

[Liens de Shell](./links.md)
</dt> <dt>

[Dossiers connus](known-folders.md)
</dt> <dt>

[Schéma de description de la bibliothèque](library-schema-entry.md)
</dt> <dt>

[**IID \_ PPV \_ args**](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args)
</dt> </dl>

 

 
