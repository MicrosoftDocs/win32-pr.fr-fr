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
# <a name="launching-applications-shellexecute-shellexecuteex-shellexecuteinfo"></a>Lancement d’applications (ShellExecute, ShellExecuteEx, SHELLEXECUTEINFO)

Une fois que votre application a localisé un objet fichier, l’étape suivante est souvent d’agir sur celle-ci d’une manière ou d’une autre. Par exemple, votre application peut vouloir lancer une autre application qui permet à l’utilisateur de modifier un fichier de données. Si le fichier d’intérêt est un fichier exécutable, votre application peut vouloir simplement la lancer. Ce document explique comment utiliser [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) ou [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) pour effectuer ces tâches.

-   [Utilisation de ShellExecute et ShellExecuteEx](#using-shellexecute-and-shellexecuteex)
    -   [Verbes d’objet](#object-verbs)
    -   [Utilisation de ShellExecuteEx pour fournir des services d’activation à partir d’un site](#using-shellexecuteex-to-provide-activation-services-from-a-site)
    -   [Utilisation de ShellExecute pour lancer la boîte de dialogue Rechercher](#using-shellexecute-to-launch-the-search-dialog-box)
-   [Exemple simple d’utilisation de ShellExecuteEx](#a-simple-example-of-how-to-use-shellexecuteex)

## <a name="using-shellexecute-and-shellexecuteex"></a>Utilisation de ShellExecute et ShellExecuteEx

Pour utiliser [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) ou [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), votre application doit spécifier l’objet fichier ou dossier sur lequel agir et un *verbe* qui spécifie l’opération. Pour **ShellExecute**, assignez ces valeurs aux paramètres appropriés. Pour **ShellExecuteEx**, renseignez les membres appropriés d’une structure [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) . Il existe également plusieurs autres membres ou paramètres qui peuvent être utilisés pour ajuster le comportement des deux fonctions.

Les objets de fichier et de dossier peuvent faire partie du système de fichiers ou des objets virtuels, et ils peuvent être identifiés par des chemins d’accès ou des pointeurs vers des listes d’identificateurs d’éléments (PIDL).

### <a name="object-verbs"></a>Verbes d’objet

Les verbes disponibles pour un objet sont essentiellement les éléments que vous trouvez dans le menu contextuel d’un objet. Pour rechercher les verbes disponibles, consultez le Registre sous

**HKEY \_ CLASSES \_ racine** \\ **CLSID** \\ *{objet \_ CLSID}* \\ **Shell** \\ 

où *\_ CLSID* de l’objet est l’identificateur de classe (CLSID) de l’objet, et *verbe* est le nom du verbe disponible. La  \\ sous-clé de **commande** Verb contient les données indiquant ce qui se produit lorsque ce verbe est appelé.

Pour savoir quels sont les verbes disponibles pour les [objets Shell prédéfinis](handlers.md), consultez le Registre sous

**HKEY \_ \_** Nom de l’objet racine des classes ( \\ *\_* \\  \\ *verbe* Shell)

où *Object \_ Name* est le nom de l’objet Shell prédéfini. Là encore, la \\ sous-clé de **commande** Verb contient les données indiquant ce qui se produit lorsque ce verbe est appelé.

Les verbes couramment disponibles sont les suivants :



| Verbe       | Description                                                                                              |
|------------|----------------------------------------------------------------------------------------------------------|
| modifier       | Lance un éditeur et ouvre le document en vue de sa modification.                                                   |
| trouver       | Lance une recherche à partir du répertoire spécifié.                                                |
| ouvert       | Lance une application. Si ce fichier n’est pas un fichier exécutable, son application associée est lancée. |
| print      | Imprime le fichier de document.                                                                                |
| properties | Affiche les propriétés de l’objet.                                                                        |
| runas      | Lance une application en tant qu’administrateur. Le contrôle de compte d’utilisateur (UAC) invite l’utilisateur à donner son consentement à |
|            | Exécutez l’application avec des privilèges élevés ou entrez les informations d’identification d’un compte d’administrateur utilisé pour exécuter le        |
|            | application Aha!.                                                                                             |

 

Chaque verbe correspond à la commande qui serait utilisée pour lancer l’application à partir d’une fenêtre de console. Le verbe **Open** est un bon exemple, car il est généralement pris en charge. Pour les fichiers. exe, **ouvrez** simplement l’application. Toutefois, il est plus couramment utilisé pour lancer une application qui fonctionne sur un fichier particulier. Par exemple, les fichiers. txt peuvent être ouverts par Microsoft WordPad. Le verbe **Open** d’un fichier. txt correspond donc à une commande semblable à la suivante :


```C++
C:\Program Files\Windows NT\Accessories\Wordpad.exe" "%1"
```



Quand vous utilisez [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) ou [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) pour ouvrir un fichier. txt, Wordpad.exe est lancé avec le fichier spécifié comme argument. Certaines commandes peuvent avoir des arguments supplémentaires, tels que des indicateurs, qui peuvent être ajoutés en fonction des besoins pour lancer correctement l’application. Pour plus d’informations sur les menus contextuels et les verbes, consultez [extension des menus contextuels](context.md).

En général, essayer de déterminer la liste des verbes disponibles pour un fichier particulier est quelque peu compliqué. Dans de nombreux cas, vous pouvez simplement affecter la **valeur null** au paramètre *lpVerb* , qui appelle la commande par défaut pour le type de fichier. Cette procédure est généralement équivalente à la définition de *lpVerb* sur « Open », mais certains types de fichiers peuvent avoir une commande par défaut différente. Pour plus d’informations, consultez [extension des menus contextuels](context.md) et la documentation de référence [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) .

### <a name="using-shellexecuteex-to-provide-activation-services-from-a-site"></a>Utilisation de ShellExecuteEx pour fournir des services d’activation à partir d’un site

Les services d’une chaîne de site peuvent contrôler de nombreux comportements d’activation d’élément. À partir de Windows 8, vous pouvez fournir un pointeur vers la chaîne de site vers [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) pour activer ces comportements. Pour fournir le site à **ShellExecuteEx**:

-   Spécifiez l' \_ indicateur \_ \_ de masque HINST est un indicateur \_ \_ de site dans le membre **fmask** de [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa).
-   Fournissez [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) dans le membre **hInstApp** de [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa).

### <a name="using-shellexecute-to-launch-the-search-dialog-box"></a>Utilisation de ShellExecute pour lancer la boîte de dialogue Rechercher

Quand un utilisateur clique avec le bouton droit sur une icône de dossier dans l’Explorateur Windows, l’un des éléments de menu est « Rechercher ». S’ils sélectionnent cet élément, l’interpréteur de commandes lance son utilitaire de recherche. Cet utilitaire affiche une boîte de dialogue qui peut être utilisée pour rechercher une chaîne de texte spécifiée dans des fichiers. Une application peut lancer par programmation l’utilitaire de recherche d’un répertoire en appelant [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea), avec « Find » comme paramètre *lpVerb* et le chemin d’accès au répertoire en tant que paramètre *lpFile* . Par exemple, la ligne de code suivante lance l’utilitaire de recherche pour le répertoire c : \\ MyPrograms.


```C++
ShellExecute(hwnd, "find", "c:\\MyPrograms", NULL, NULL, 0);
```



## <a name="a-simple-example-of-how-to-use-shellexecuteex"></a>Exemple simple d’utilisation de ShellExecuteEx

L’exemple d’application console suivant illustre l’utilisation de [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa). La plupart des codes de vérification des erreurs ont été omis par souci de clarté.


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



L’application récupère tout d’abord le PIDL du répertoire Windows et énumère son contenu jusqu’à ce qu’il trouve le premier fichier. bmp. Contrairement à l’exemple précédent, [**IShellFolder :: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) est utilisé pour récupérer le nom d’analyse du fichier au lieu de son nom complet. Étant donné qu’il s’agit d’un dossier de système de fichiers, le nom d’analyse est un chemin d’accès complet, ce qui est nécessaire pour [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).

Une fois le premier fichier. bmp localisé, les valeurs appropriées sont attribuées aux membres d’une structure [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) . Le membre **lpFile** est défini sur le nom d’analyse du fichier et le membre **lpVerb** sur **null** pour commencer l’opération par défaut. Dans ce cas, l’opération par défaut est « Open ». La structure est ensuite transmise à [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), qui lance le gestionnaire par défaut pour les fichiers bitmap, en général MSPaint.exe, pour ouvrir le fichier. Une fois la fonction retournée, les PIDL sont libérés et l’interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) du dossier Windows est libérée.

 

 
