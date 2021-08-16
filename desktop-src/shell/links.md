---
description: un lien d’interpréteur de commandes est un objet de données qui contient des informations utilisées pour accéder à un autre objet dans l’espace de noms du Shell&\# 8212 ; autrement dit, tout objet visible via Windows Explorer.
ms.assetid: 32ad306d-54bd-4130-ad30-08db50ef106e
title: Liens de Shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25f9f5e639cfa3619d5c79b011ab101af7c25ed1813db1c96b9f5422504f8c1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117859021"
---
# <a name="shell-links"></a>Liens de Shell

un *lien d’interpréteur* de commandes est un objet de données qui contient des informations utilisées pour accéder à un autre objet dans l’espace de noms du Shell, c’est-à-dire tout objet visible via Windows Explorer. Les types d’objets accessibles via des liens de Shell incluent des fichiers, des dossiers, des lecteurs de disque et des imprimantes. Un lien de Shell permet à un utilisateur ou à une application d’accéder à un objet à partir de n’importe quel emplacement de l’espace de noms. L’utilisateur ou l’application n’a pas besoin de connaître le nom et l’emplacement actuels de l’objet.

-   [À propos des liens de Shell](#about-shell-links)
    -   [Résolution de lien](#link-resolution)
    -   [Fichiers de liaison](#link-files)
    -   [Identificateurs d’éléments et listes d’identificateurs](#item-identifiers-and-identifier-lists)
-   [Utilisation des liens de l’interpréteur de commandes](#using-shell-links)
    -   [Création d’un raccourci et d’un raccourci vers un fichier](#creating-a-shortcut-and-a-folder-shortcut-to-a-file)
    -   [Résolution d’un raccourci](#resolving-a-shortcut)
    -   [Création d’un raccourci vers un objet qui n’est pas un fichier](#creating-a-shortcut-to-a-nonfile-object)

## <a name="about-shell-links"></a>À propos des liens de Shell

L’utilisateur crée un lien de Shell en choisissant la commande **créer un raccourci** dans le menu contextuel d’un objet. Le système crée automatiquement une icône pour le lien de l’interpréteur de commandes en associant l’icône de l’objet à une petite flèche (appelée icône de superposition de lien définie par le système) qui apparaît dans le coin inférieur gauche de l’icône. Un lien de Shell avec une icône est appelé raccourci ; Toutefois, les termes lien et raccourci de l’interpréteur de commandes sont souvent utilisés indifféremment. En règle générale, l’utilisateur crée des raccourcis pour accéder rapidement aux objets stockés dans des sous-dossiers ou dans des dossiers partagés sur d’autres ordinateurs. par exemple, un utilisateur peut créer un raccourci vers un document Microsoft Word qui se trouve dans un sous-dossier et placer l’icône de raccourci sur le bureau. L’utilisateur peut ensuite ouvrir le document en double-cliquant sur l’icône de raccourci. Si le document est déplacé ou renommé après la création du raccourci, le système tente de mettre à jour le raccourci la prochaine fois que l’utilisateur le sélectionne.

Les applications peuvent également créer et utiliser des liens et des raccourcis de l’interpréteur de commandes. Par exemple, une application de traitement de texte peut créer un lien de Shell pour implémenter une liste des documents les plus récemment utilisés. Une application crée un lien de Shell à l’aide de l’interface [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) pour créer un objet de lien de Shell. L’application utilise l’interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) ou [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream) pour stocker l’objet dans un fichier ou un flux.

> [!Note]  
> Vous ne pouvez pas utiliser [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) pour créer un lien vers une URL.

 

Cette vue d’ensemble décrit l’interface [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) et explique comment l’utiliser pour créer et résoudre des liens de Shell à partir d’une application basée sur Microsoft Win32. Étant donné que la conception des liens de Shell est basée sur le modèle COM (Component Object Model) OLE, vous devez être familiarisé avec les concepts de base de la programmation COM et OLE avant de lire cette vue d’ensemble.

### <a name="link-resolution"></a>Résolution de lien

Si un utilisateur crée un raccourci vers un objet et que le nom ou l’emplacement de l’objet est modifié ultérieurement, le système prend automatiquement les mesures nécessaires pour mettre à jour ou résoudre le raccourci la prochaine fois que l’utilisateur le sélectionne. Toutefois, si une application crée un lien de Shell et le stocke dans un flux, le système n’essaie pas automatiquement de résoudre le lien. L’application doit résoudre le lien en appelant la méthode [**IShellLink :: Resolve**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve) .

Lorsqu’un lien de Shell est créé, le système enregistre les informations sur le lien. Lors de la résolution d’un lien (automatiquement ou à l’aide d’un appel [**IShellLink :: Resolve**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve) ), le système récupère d’abord le chemin d’accès associé au lien de l’interpréteur de commandes en utilisant un pointeur vers la liste d’identificateur du lien de l’interpréteur de commandes. Pour plus d’informations sur la liste d’identificateurs, consultez [identificateurs d’éléments et listes d’identificateurs](#item-identifiers-and-identifier-lists). Le système recherche l’objet associé dans ce chemin d’accès et, s’il trouve l’objet, résout le lien. Si le système ne trouve pas l’objet, il appelle le service de [suivi des liaisons distribuées et les identificateurs d’objets](../fileio/distributed-link-tracking-and-object-identifiers.md) (DLT), s’il est disponible, pour localiser l’objet. Si le service DLT n’est pas disponible ou ne trouve pas l’objet, le système recherche un objet avec les mêmes attributs et heure de création de fichier, mais avec un nom différent. Ce type de recherche résout un lien vers un objet qui a été renommé.

Si le système ne parvient toujours pas à trouver l’objet, il recherche les répertoires, le bureau et les volumes locaux, en regardant de manière récursive l’arborescence de répertoires d’un objet ayant le même nom ou la même heure de création. Si le système ne trouve toujours pas de correspondance, il affiche une boîte de dialogue invitant l’utilisateur à entrer un emplacement. Une application peut supprimer la boîte de dialogue en spécifiant la valeur de la variable de l’interface de l' **\_ \_ utilisateur** dans un appel à [**IShellLink :: Resolve**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve).

### <a name="initialization-of-the-component-object-library"></a>Initialisation de la bibliothèque d’objets du composant

Pour qu’une application puisse créer et résoudre des raccourcis, elle doit initialiser la bibliothèque d’objets de composant en appelant la fonction [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) . Chaque appel à **CoInitialize** requiert un appel correspondant à la fonction [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) , qu’une application doit appeler lorsqu’elle se termine. L’appel à **CoUninitialize** garantit que l’application ne se termine pas tant qu’elle n’a pas reçu tous ses messages en attente.

### <a name="location-independent-names"></a>Noms de Location-Independent

Le système fournit des noms indépendants de l’emplacement pour les liens de Shell vers des objets stockés dans des dossiers partagés. Si l’objet est stocké localement, le système fournit le chemin d’accès local et le nom de fichier de l’objet. Si l’objet est stocké à distance, le système fournit un nom de ressource réseau UNC (Universal Naming Convention) pour l’objet. Étant donné que le système fournit des noms indépendants de l’emplacement, un lien de Shell peut servir de nom universel pour un fichier qui peut être transféré à d’autres ordinateurs.

### <a name="link-files"></a>Fichiers de liaison

quand l’utilisateur crée un raccourci vers un objet en choisissant la commande **créer un raccourci** dans le menu contextuel de l’objet, Windows stocke les informations dont il a besoin pour accéder à l’objet dans un fichier de liaison, c’est-à-dire un fichier binaire avec l’extension de nom de fichier. lnk. Un fichier de liaison contient les informations suivantes :

-   Emplacement (chemin d’accès) de l’objet référencé par le raccourci (appelé objet correspondant).
-   Répertoire de travail de l’objet correspondant.
-   Liste d’arguments que le système passe à l’objet correspondant quand la méthode [**IContextMenu :: commande InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) est activée pour le raccourci.
-   Commande show utilisée pour définir l’état d’affichage initial de l’objet correspondant. Il s’agit de l’une des valeurs LOGICIELles \_ décrites dans [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow).
-   Emplacement (chemin d’accès et index) de l’icône du raccourci.
-   Chaîne de description du raccourci.
-   Raccourci clavier du raccourci.

Lorsqu’un fichier de liaison est supprimé, l’objet correspondant n’est pas affecté.

Si vous créez un raccourci vers un autre raccourci, le système copie simplement le fichier de liaison au lieu de créer un nouveau fichier de liaison. Dans ce cas, les raccourcis ne sont pas indépendants l’un de l’autre.

Une application peut inscrire une extension de nom de fichier en tant que type de fichier de raccourci. Si un fichier a une extension de nom de fichier qui a été inscrite en tant que type de fichier de raccourci, le système ajoute automatiquement l’icône de superposition de lien définie par le système (une petite flèche) à l’icône du fichier. Pour inscrire une extension de nom de fichier en tant que type de fichier de raccourci, vous devez ajouter la valeur IsShortcut à la description du registre de l’extension de nom de fichier, comme indiqué dans l’exemple ci-dessous. Notez que l’interpréteur de commandes doit être redémarré pour que l’icône de superposition prenne effet. IsShortcut n’a pas de valeur de données.

```
HKEY_CLASSES_ROOT
   .xyz
      (Default) = XYZApp
   XYZApp
      IsShortcut
```

### <a name="shortcut-names"></a>Noms de raccourcis

Le nom du raccourci, qui est une chaîne qui apparaît sous l’icône de lien de l’interpréteur de commandes, correspond en fait au nom de fichier du raccourci lui-même. L’utilisateur peut modifier la chaîne de description en la sélectionnant et en entrant une nouvelle chaîne.

### <a name="location-of-shortcuts-in-the-namespace"></a>Emplacement des raccourcis dans l’espace de noms

Un raccourci peut exister sur le bureau ou n’importe où dans l’espace de noms de l’interpréteur de commandes. De même, l’objet associé au raccourci peut également se trouver n’importe où dans l’espace de noms de l’interpréteur de commandes. Une application peut utiliser la méthode [**IShellLink :: setPath**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setpath) pour définir le chemin d’accès et le nom de fichier de l’objet associé, et la méthode [**IShellLink :: GetPath**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getpath) pour récupérer le chemin d’accès et le nom de fichier actuels de l’objet.

### <a name="shortcut-working-directory"></a>Répertoire de travail du raccourci

Le répertoire de travail est le répertoire dans lequel l’objet correspondant d’un raccourci charge ou stocke les fichiers lorsque l’utilisateur n’identifie pas un répertoire spécifique. Un fichier de liaison contient le nom du répertoire de travail de l’objet correspondant. Une application peut définir le nom du répertoire de travail pour l’objet correspondant à l’aide de la méthode [**IShellLink :: SetWorkingDirectory**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setworkingdirectory) et peut récupérer le nom du répertoire de travail actuel pour l’objet correspondant à l’aide de la méthode [**IShellLink :: GetWorkingDirectory**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getworkingdirectory) .

### <a name="shortcut-command-line-arguments"></a>Arguments de ligne de commande du raccourci

Un fichier de liaison contient des arguments de ligne de commande que le shell passe à l’objet correspondant lorsque l’utilisateur sélectionne le lien. Une application peut définir les arguments de ligne de commande d’un raccourci à l’aide de la méthode [**IShellLink :: setArguments**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setarguments) . Il est utile de définir des arguments de ligne de commande lorsque l’application correspondante, telle qu’un éditeur de liens ou un compilateur, prend des indicateurs spéciaux comme arguments. Une application peut récupérer les arguments de ligne de commande à partir d’un raccourci à l’aide de la méthode [**IShellLink :: GetArguments**](/windows/desktop/api/Shobjidl_core/nf-shobjidl_core-ishelllinka-getarguments) .

### <a name="shortcut-show-commands"></a>Commandes d’affichage de raccourci

Lorsque l’utilisateur double-clique sur un raccourci, le système démarre l’application associée à l’objet correspondant et définit l’état d’affichage initial de l’application en fonction de la commande show spécifiée par le raccourci. La commande show peut être l’une des \_ valeurs SW incluses dans la description de la fonction [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) . Une application peut définir la commande Show pour un raccourci à l’aide de la méthode [**IShellLink :: SetShowCmd**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setshowcmd) et peut récupérer la commande Show en cours à l’aide de la méthode [**IShellLink :: GetShowCmd**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getshowcmd) .

### <a name="shortcut-icons"></a>Icônes de raccourci

Comme les autres objets Shell, un raccourci a une icône. L’utilisateur accède à l’objet associé à un raccourci en double-cliquant sur l’icône du raccourci. Lorsque le système crée une icône pour un raccourci, il utilise l’image bitmap de l’objet correspondant et ajoute l’icône de superposition de lien définie par le système (une petite flèche) dans le coin inférieur gauche. Une application peut définir l’emplacement (chemin d’accès et index) d’une icône de raccourci à l’aide de la méthode [**IShellLink :: SetIconLocation**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-seticonlocation) . Une application peut récupérer cet emplacement à l’aide de la méthode [**IShellLink :: GetIconLocation**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-geticonlocation) .

### <a name="shortcut-descriptions"></a>Descriptions des raccourcis

Les raccourcis ont des descriptions, mais l’utilisateur ne les voit jamais. Une application peut utiliser une description pour stocker des informations de texte. Les descriptions sont définies à l’aide de la méthode [**IShellLink :: SetDescription**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setdescription) et récupérées à l’aide de la méthode [**IShellLink :: GetDescription**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getdescription) .

### <a name="shortcut-keyboard-shortcuts"></a>Raccourcis clavier de raccourci

Un raccourci clavier peut être associé à un objet shortcut. Les raccourcis clavier permettent à l’utilisateur d’appuyer sur une combinaison de touches pour activer un raccourci. Une application peut définir le raccourci clavier d’un raccourci à l’aide de la méthode [**IShellLink :: SetHotkey**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-sethotkey) et peut récupérer le raccourci clavier actuel à l’aide de la méthode [**IShellLink :: GetHotkey**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-gethotkey) .

### <a name="item-identifiers-and-identifier-lists"></a>Identificateurs d’éléments et listes d’identificateurs

L’interpréteur de commandes utilise des identificateurs d’objet dans l’espace de noms du shell. Tous les objets visibles dans l’interpréteur de commandes (fichiers, répertoires, serveurs, groupes de travail, etc.) ont des identificateurs uniques parmi les objets de leur dossier parent. Ces identificateurs sont appelés identificateurs d’élément et ont le type de données [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) tel que défini dans le fichier d’en-tête Shtypes. h. Un identificateur d’élément est un flux d’octets de longueur variable qui contient des informations qui identifient un objet dans un dossier. Seul le créateur d’un identificateur d’élément connaît le contenu et le format de l’identificateur. La seule partie d’un identificateur d’élément utilisée par l’interpréteur de commandes est les deux premiers octets, qui spécifient la taille de l’identificateur.

Chaque dossier parent a son propre identificateur d’élément qui l’identifie dans son propre dossier parent. Ainsi, tout objet Shell peut être identifié de manière unique par une liste d’identificateurs d’éléments. Un dossier parent conserve une liste d’identificateurs pour les éléments qu’il contient. La liste a le type de données [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) . Les listes d’identificateurs d’élément sont allouées par le shell et peuvent être passées entre les interfaces de Shell, telles que [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder). Il est important de se souvenir que chaque identificateur dans une liste d’identificateurs d’éléments est uniquement significatif dans le contexte de son dossier parent.

Une application peut définir une liste d’identificateurs d’éléments de raccourci à l’aide de la méthode [**IShellLink :: SetIDList**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setidlist) . Cette méthode est utile lors de la définition d’un raccourci vers un objet qui n’est pas un fichier, tel qu’une imprimante ou un lecteur de disque. Une application peut récupérer la liste des identificateurs d’élément d’un raccourci à l’aide de la méthode [**IShellLink :: GetIDList**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getidlist) .

## <a name="using-shell-links"></a>Utilisation des liens de l’interpréteur de commandes

Cette section contient des exemples qui montrent comment créer et résoudre des raccourcis à partir d’une application Win32. Cette section suppose que vous êtes familiarisé avec la programmation Win32, C++ et OLE COM.

### <a name="creating-a-shortcut-and-a-folder-shortcut-to-a-file"></a>Création d’un raccourci et d’un raccourci vers un fichier

L’exemple de fonction CreateLink de l’exemple suivant crée un raccourci. Les paramètres incluent un pointeur vers le nom du fichier à lier, un pointeur vers le nom du raccourci que vous créez et un pointeur vers la description du lien. La description se compose de la chaîne « raccourci vers le **nom de fichier**», où nom de **fichier** est le nom du fichier à lier.

Pour créer un raccourci vers un dossier à l’aide de l’exemple de fonction CreateLink, appelez [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) en utilisant CLSID \_ FolderShortcut, au lieu de CLSID \_ ShellLink (CLSID \_ FolderShortcut prend en charge IShellLink). Tout autre code reste le même.

Étant donné que CreateLink appelle la fonction [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) , il est supposé que la fonction [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) a déjà été appelée. CreateLink utilise l’interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) pour enregistrer le raccourci et l’interface [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) pour stocker le nom et la description du fichier.


```C++
// CreateLink - Uses the Shell's IShellLink and IPersistFile interfaces 
//              to create and store a shortcut to the specified object. 
//
// Returns the result of calling the member functions of the interfaces. 
//
// Parameters:
// lpszPathObj  - Address of a buffer that contains the path of the object,
//                including the file name.
// lpszPathLink - Address of a buffer that contains the path where the 
//                Shell link is to be stored, including the file name.
// lpszDesc     - Address of a buffer that contains a description of the 
//                Shell link, stored in the Comment field of the link
//                properties.

#include "stdafx.h"
#include "windows.h"
#include "winnls.h"
#include "shobjidl.h"
#include "objbase.h"
#include "objidl.h"
#include "shlguid.h"

HRESULT CreateLink(LPCWSTR lpszPathObj, LPCSTR lpszPathLink, LPCWSTR lpszDesc) 
{ 
    HRESULT hres; 
    IShellLink* psl; 
 
    // Get a pointer to the IShellLink interface. It is assumed that CoInitialize
    // has already been called.
    hres = CoCreateInstance(CLSID_ShellLink, NULL, CLSCTX_INPROC_SERVER, IID_IShellLink, (LPVOID*)&psl); 
    if (SUCCEEDED(hres)) 
    { 
        IPersistFile* ppf; 
 
        // Set the path to the shortcut target and add the description. 
        psl->SetPath(lpszPathObj); 
        psl->SetDescription(lpszDesc); 
 
        // Query IShellLink for the IPersistFile interface, used for saving the 
        // shortcut in persistent storage. 
        hres = psl->QueryInterface(IID_IPersistFile, (LPVOID*)&ppf); 
 
        if (SUCCEEDED(hres)) 
        { 
            WCHAR wsz[MAX_PATH]; 
 
            // Ensure that the string is Unicode. 
            MultiByteToWideChar(CP_ACP, 0, lpszPathLink, -1, wsz, MAX_PATH); 
            
            // Add code here to check return value from MultiByteWideChar 
            // for success.
 
            // Save the link by calling IPersistFile::Save. 
            hres = ppf->Save(wsz, TRUE); 
            ppf->Release(); 
        } 
        psl->Release(); 
    } 
    return hres; 
```



### <a name="resolving-a-shortcut"></a>Résolution d’un raccourci

Une application peut avoir besoin d’accéder à un raccourci précédemment créé et de le manipuler. Cette opération est appelée résolution du raccourci.

La fonction ResolveIt définie par l’application dans l’exemple suivant résout un raccourci. Ses paramètres incluent un handle de fenêtre, un pointeur vers le chemin d’accès du raccourci et l’adresse d’une mémoire tampon qui reçoit le nouveau chemin d’accès à l’objet. Le handle de fenêtre identifie la fenêtre parente pour les boîtes de message que le Shell peut avoir besoin d’afficher. Par exemple, l’interpréteur de commandes peut afficher une boîte de message si le lien se trouve sur un média non partagé, si des problèmes réseau se produisent, si l’utilisateur doit insérer une disquette, et ainsi de suite.

La fonction ResolveIt appelle la fonction [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) et suppose que la fonction [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) a déjà été appelée. Notez que ResolveIt doit utiliser l’interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) pour stocker les informations de lien. **IPersistFile** est implémenté par l’objet [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) . Les informations de lien doivent être chargées avant que les informations de chemin d’accès ne soient récupérées, ce qui est indiqué plus loin dans cet exemple. L’échec du chargement des informations de lien entraîne l’échec des appels aux fonctions membres [**IShellLink :: GetPath**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getpath) et [**IShellLink :: GetDescription**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getdescription) .


```C++
// ResolveIt - Uses the Shell's IShellLink and IPersistFile interfaces 
//             to retrieve the path and description from an existing shortcut. 
//
// Returns the result of calling the member functions of the interfaces. 
//
// Parameters:
// hwnd         - A handle to the parent window. The Shell uses this window to 
//                display a dialog box if it needs to prompt the user for more 
//                information while resolving the link.
// lpszLinkFile - Address of a buffer that contains the path of the link,
//                including the file name.
// lpszPath     - Address of a buffer that receives the path of the link
                  target, including the file name.
// lpszDesc     - Address of a buffer that receives the description of the 
//                Shell link, stored in the Comment field of the link
//                properties.

#include "stdafx.h"
#include "windows.h"
#include "shobjidl.h"
#include "shlguid.h"
#include "strsafe.h"
                            
HRESULT ResolveIt(HWND hwnd, LPCSTR lpszLinkFile, LPWSTR lpszPath, int iPathBufferSize) 
{ 
    HRESULT hres; 
    IShellLink* psl; 
    WCHAR szGotPath[MAX_PATH]; 
    WCHAR szDescription[MAX_PATH]; 
    WIN32_FIND_DATA wfd; 
 
    *lpszPath = 0; // Assume failure 

    // Get a pointer to the IShellLink interface. It is assumed that CoInitialize
    // has already been called. 
    hres = CoCreateInstance(CLSID_ShellLink, NULL, CLSCTX_INPROC_SERVER, IID_IShellLink, (LPVOID*)&psl); 
    if (SUCCEEDED(hres)) 
    { 
        IPersistFile* ppf; 
 
        // Get a pointer to the IPersistFile interface. 
        hres = psl->QueryInterface(IID_IPersistFile, (void**)&ppf); 
        
        if (SUCCEEDED(hres)) 
        { 
            WCHAR wsz[MAX_PATH]; 
 
            // Ensure that the string is Unicode. 
            MultiByteToWideChar(CP_ACP, 0, lpszLinkFile, -1, wsz, MAX_PATH); 
 
            // Add code here to check return value from MultiByteWideChar 
            // for success.
 
            // Load the shortcut. 
            hres = ppf->Load(wsz, STGM_READ); 
            
            if (SUCCEEDED(hres)) 
            { 
                // Resolve the link. 
                hres = psl->Resolve(hwnd, 0); 

                if (SUCCEEDED(hres)) 
                { 
                    // Get the path to the link target. 
                    hres = psl->GetPath(szGotPath, MAX_PATH, (WIN32_FIND_DATA*)&wfd, SLGP_SHORTPATH); 

                    if (SUCCEEDED(hres)) 
                    { 
                        // Get the description of the target. 
                        hres = psl->GetDescription(szDescription, MAX_PATH); 

                        if (SUCCEEDED(hres)) 
                        {
                            hres = StringCbCopy(lpszPath, iPathBufferSize, szGotPath);
                            if (SUCCEEDED(hres))
                            {
                                // Handle success
                            }
                            else
                            {
                                // Handle the error
                            }
                        }
                    }
                } 
            } 

            // Release the pointer to the IPersistFile interface. 
            ppf->Release(); 
        } 

        // Release the pointer to the IShellLink interface. 
        psl->Release(); 
    } 
    return hres; 
}
```



### <a name="creating-a-shortcut-to-a-nonfile-object"></a>Création d’un raccourci vers un objet qui n’est pas un fichier

La création d’un raccourci vers un objet non-fichier, tel qu’une imprimante, est similaire à la création d’un raccourci vers un fichier, à ceci près qu’au lieu de définir le chemin d’accès au fichier, vous devez définir la liste d’identificateurs sur l’imprimante. Pour définir la liste d’identificateurs, appelez la méthode [**IShellLink :: SetIDList**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setidlist) , en spécifiant l’adresse d’une liste d’identificateurs.

Chaque objet dans l’espace de noms de l’interpréteur de commandes a un identificateur d’élément. L’interpréteur de commandes concatène souvent des identificateurs d’élément dans des listes se terminant par un caractère null, composées de n’importe quel nombre d’identificateurs d’élément. Pour plus d’informations sur les identificateurs d’élément, consultez [identificateurs d’élément et listes d’identificateurs](#item-identifiers-and-identifier-lists).

En général, si vous devez définir un raccourci vers un élément qui n’a pas de nom de fichier, tel qu’une imprimante, vous aurez déjà un pointeur vers l’interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) de l’objet. **IShellFolder** est utilisé pour créer des extensions d’espace de noms.

Une fois que vous disposez de l’identificateur de classe pour [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder), vous pouvez appeler la fonction [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour récupérer l’adresse de l’interface. Vous pouvez ensuite appeler l’interface pour énumérer les objets dans le dossier et récupérer l’adresse de l’identificateur d’élément pour l’objet que vous recherchez. Enfin, vous pouvez utiliser l’adresse dans un appel à la fonction membre [**IShellLink :: SetIDList**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setidlist) pour créer un raccourci vers l’objet.

 

 
