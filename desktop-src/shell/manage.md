---
description: L’interpréteur de commandes offre plusieurs moyens de gérer les systèmes de fichiers.
ms.assetid: d9ffda6f-adc0-44a3-b410-e23bf5f4f165
title: Gestion du système de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee0f3b47e17e691c540a9775f3b8588b311b9878
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127226868"
---
# <a name="managing-the-file-system"></a>Gestion du système de fichiers

L’interpréteur de commandes offre plusieurs moyens de gérer les systèmes de fichiers. L’interpréteur de commandes fournit une fonction, [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa), qui permet à une application de déplacer, copier, renommer et supprimer des fichiers par programmation. L’interpréteur de commandes prend également en charge des fonctionnalités de gestion de fichiers supplémentaires.

-   Les documents HTML peuvent être *connectés* à des fichiers associés, tels que des fichiers graphiques ou des feuilles de style. Lorsque le document est déplacé ou copié, les fichiers connectés sont également déplacés ou copiés automatiquement.
-   Pour les systèmes qui sont disponibles pour plusieurs utilisateurs, les fichiers peuvent être gérés par utilisateur. Les utilisateurs ont facilement accès à leurs fichiers de données, mais pas aux fichiers appartenant à d’autres utilisateurs.
-   Si des fichiers de document sont ajoutés ou modifiés, ils peuvent être ajoutés à la liste des documents récents de l’interpréteur de commandes. quand l’utilisateur clique sur la commande **documents** du menu Démarrer, une liste de liens vers les documents s’affiche.

Ce document décrit le fonctionnement de ces technologies de gestion de fichiers. Il décrit ensuite comment utiliser l’interpréteur de commandes pour déplacer, copier, renommer et supprimer des fichiers, et comment gérer des objets dans la corbeille.

-   [Gestion des fichiers par utilisateur](#per-user-file-management)
-   [Dossiers Mes documents et mes images](#my-documents-and-my-pictures-folders)
-   [Fichiers connectés](#connected-files)
-   [Déplacement, copie, attribution d’un nouveau nom et suppression de fichiers](#moving-copying-renaming-and-deleting-files)
    -   [Notification de l’interpréteur de commandes](#notifying-the-shell)
-   [Exemple simple de gestion de fichiers avec SHFileOperation](#simple-example-of-managing-files-with-shfileoperation)
-   [Ajout de fichiers à la liste des documents récents de l’interpréteur de commandes](#adding-files-to-the-shells-list-of-recent-documents)

## <a name="per-user-file-management"></a>Gestion de fichiers Per-User

l’interpréteur de commandes Windows 2000 permet à des fichiers d’être associés à un utilisateur particulier, de sorte que les fichiers restent masqués pour les autres utilisateurs. en termes de système de fichiers, les fichiers sont stockés dans le dossier de profil de l’utilisateur, en général C : \\ Documents et Paramètres \\ *nom d’utilisateur* \\ sur Windows systèmes 2000. Cette fonctionnalité permet à de nombreuses personnes d’utiliser le même ordinateur, tout en préservant la confidentialité de leurs fichiers d’autres utilisateurs. Différents utilisateurs peuvent avoir différents programmes disponibles. Il offre également un moyen simple aux administrateurs et aux applications de stocker des éléments tels que les fichiers d’initialisation (.ini) ou de lien (. lnk). Les applications peuvent donc conserver un état différent pour chaque utilisateur et récupérer facilement cet état particulier en cas de besoin. Il existe également un dossier de profil pour stocker des informations qui sont communes à tous les utilisateurs.

Étant donné qu’il est peu commode de déterminer quel utilisateur est connecté et où se trouvent ses fichiers, les dossiers par utilisateur standard sont des dossiers spéciaux et sont identifiés par un [**CSIDL**](csidl.md). Par exemple, le CSIDL pour le dossier Program Files par utilisateur est programmes CSIDL \_ . Si votre application appelle [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) ou [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) avec l’un des CSIDLs par utilisateur, la fonction retourne le pointeur vers une liste d’identificateurs d’éléments (PIDL) ou un chemin d’accès approprié à l’utilisateur actuellement connecté. Si votre application doit récupérer le chemin d’accès ou le PIDL du dossier du profil, son CSIDL est un **\_ Profil CSIDL**.

## <a name="my-documents-and-my-pictures-folders"></a>Dossiers Mes documents et mes images

L’une des icônes standard se trouvant sur le bureau est **Mes documents**. Lorsque vous ouvrez ce dossier, il contient les fichiers de document de l’utilisateur actuel. L’instance de bureau de mes documents est un dossier virtuel (un alias vers l’emplacement du système de fichiers utilisé pour stocker physiquement les documents de l’utilisateur) situé juste sous le bureau dans la hiérarchie de l’espace de noms.

L’objectif des dossiers Mes documents et mes images est de fournir une méthode simple et sécurisée permettant aux utilisateurs d’accéder à leurs fichiers de documents et d’images sur un système qui peut avoir plusieurs utilisateurs. Des dossiers de système de fichiers distincts sont attribués à chaque utilisateur pour ses fichiers. par exemple, l’emplacement du dossier documents d’un utilisateur dans le système de fichiers est généralement le suivant : C : \\ documents et Paramètres \\ *username* \\ My documents. Les utilisateurs n’ont pas besoin de connaître l’emplacement physique de leurs dossiers de système de fichiers. Ils accèdent simplement à leurs fichiers via l’icône Mes documents.

> [!Note]  
> Mes documents permet à un utilisateur d’accéder à ses propres fichiers, mais pas à ceux d’autres utilisateurs. Si plusieurs personnes utilisent le même ordinateur, un administrateur peut verrouiller les utilisateurs de la partie du système de fichiers où sont stockés les fichiers réels. Les utilisateurs pourront ainsi travailler sur leurs propres documents par le biais du dossier Mes documents, mais pas sur des documents appartenant à d’autres utilisateurs.

 

Il n’est généralement pas nécessaire pour une application de savoir quel utilisateur est connecté ou dans le système de fichiers où se trouve le dossier Mes documents de cet utilisateur. Au lieu de cela, votre application peut récupérer le PIDL de l’icône Mes documents du Bureau en appelant la méthode [**IShellFolder ::P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) du bureau. Le nom d’analyse utilisé pour identifier le dossier Mes documents n’est pas un chemin d’accès de fichier, mais à la place : {450d8fba-ad25-11D0-98a8-0800361b1103}. L’expression entre crochets est la forme textuelle du GUID mes documents. Par exemple, pour récupérer le PIDL de mes documents, votre application doit utiliser cet appel à **IShellFolder ::P arsedisplayname**.


```C++
hr = psfDeskTop->ParseDisplayName(NULL, 
                                  NULL, 
                                  L"::{450d8fba-ad25-11d0-98a8-0800361b1103}", 
                                  &chEaten, 
                                  &pidlDocFiles, 
                                  NULL);
```



Une fois que votre application a le PIDL mes documents, elle peut gérer le dossier comme s’il s’agissait d’un dossier de système de fichiers normal (énumération d’éléments, analyse, liaison et exécution de toute autre opération de dossier valide). L’interpréteur de commandes mappe automatiquement les modifications dans mes documents ou ses sous-dossiers vers les dossiers du système de fichiers appropriés.

Si votre application a besoin d’accéder au dossier réel du système de fichiers qui contient les documents de l’utilisateur actuel, transmettez la valeur de CSIDL- \_ Personal à [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation). La fonction retourne le PIDL du dossier de système de fichiers qui est affiché dans le dossier Mes documents de l’utilisateur actuel.

## <a name="connected-files"></a>Fichiers connectés

les documents HTML ont souvent plusieurs fichiers graphiques associés, un fichier de feuille de style, plusieurs JScript Microsoft (compatibles avec les fichiers de spécification de langage ECMA 262), et ainsi de suite. Lorsque vous déplacez ou copiez le document HTML principal, vous souhaitez également déplacer ou copier les fichiers associés afin d’éviter de rompre les liens. Malheureusement, il n’existait aucun moyen simple de déterminer quels fichiers sont associés à un document HTML donné, à l’exception de l’analyse de leur contenu. pour pallier ce problème, Windows 2000 fournit un moyen simple de *connecter* un document HTML primaire à son groupe de fichiers associés. Si la connexion de fichiers est activée, lorsque le document est déplacé ou copié, tous ses fichiers connectés y sont associés.

Pour créer un groupe de fichiers connectés, le document principal doit avoir une extension de nom de fichier .htm ou .html. Créez un sous-dossier du dossier parent du document principal. Le nom du sous-dossier doit être le nom du document principal, moins le .htm ou .html extension, suivis de l’une des extensions listées ci-dessous. Les extensions les plus couramment utilisées sont « . Files » ou « \_ files ». Par exemple, si le document principal est nommé MyDoc.htm, le fait de nommer le sous-dossier « \_ fichiers MyDoc » définit le sous-dossier comme le conteneur des fichiers connectés du document. Si le document principal est déplacé ou copié, le sous-dossier et ses fichiers sont également déplacés ou copiés.

Pour certaines langues, il est possible d’utiliser un équivalent localisé de « \_ files » pour créer un sous-dossier pour les fichiers connectés. Le tableau suivant répertorie les chaînes valides qui peuvent être ajoutées à un nom de document pour créer un sous-dossier de fichiers connectés. Notez que certaines de ces chaînes ont « - » comme premier caractère plutôt que « \_ » ou « . ».



:::row:::
   :::column span="":::
      « \_ Archivos »
   :::column-end:::
   :::column span="":::
      « \_ Arquivos »
   :::column-end:::
   :::column span="":::
      « \_ debout »
   :::column-end:::
   :::column span="":::
      « \_ Bylos »
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      "-Dateien"
   :::column-end:::
   :::column span="":::
      « \_ datoteke »
   :::column-end:::
   :::column span="":::
      « \_ dosyalar »
   :::column-end:::
   :::column span="":::
      « \_ elemei »
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      « \_ failid »
   :::column-end:::
   :::column span="":::
      « \_ échec »
   :::column-end:::
   :::column span="":::
      « \_ fajlovi »
   :::column-end:::
   :::column span="":::
      « \_ ficheiros »
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      « \_ fichier »
   :::column-end:::
   :::column span="":::
      « -du serveur de fichiers »
   :::column-end:::
   :::column span="":::
      ". Files"
   :::column-end:::
   :::column span="":::
      « \_ fichiers »
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      « \_ fichier »
   :::column-end:::
   :::column span="":::
      « \_ fitxers »
   :::column-end:::
   :::column span="":::
      « \_ fitxategiak »
   :::column-end:::
   :::column span="":::
      « \_ pliki »
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      « \_ Soubory »
   :::column-end:::
   :::column span="":::
      « \_ tiedostot »
   :::column-end:::
   :::column span="":::
   :::column-end:::
   :::column span="":::
   :::column-end:::
:::row-end:::



 

> [!Note]  
> Cette fonctionnalité est sensible à la casse de l’extension. Par exemple, dans l’exemple ci-dessus, un sous-dossier nommé « fichiers MyDoc » n’est \_ pas connecté à MyDoc.htm.

 

L’activation ou la désactivation de la connexion de fichiers est contrôlée par une valeur **reg \_ DWORD** , NoFileFolderConnection, de la clé de Registre suivante.

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
```

Normalement, cette valeur n’est pas définie et la connexion de fichiers est activée. Si nécessaire, vous pouvez désactiver la connexion de fichiers en ajoutant cette valeur à la clé et en lui affectant la valeur 1. Pour réactiver la connexion de fichiers, affectez à NoFileFolderConnection la valeur zéro.

> [!Note]  
> La connexion de fichiers doit normalement être activée, car d’autres applications peuvent en dépendre. Désactivez la connexion de fichiers uniquement si cela est absolument nécessaire.

 

## <a name="moving-copying-renaming-and-deleting-files"></a>Déplacement, copie, attribution d’un nouveau nom et suppression de fichiers

L’espace de noms n’est pas statique, et les applications doivent généralement gérer le système de fichiers en effectuant l’une des opérations suivantes.

-   Copie d’un objet dans un autre dossier.
-   Déplacement d’un objet vers un autre dossier.
-   Suppression d’un objet.
-   Attribution d’un nouveau nom à un objet.

Ces opérations sont toutes effectuées avec [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa). Cette fonction accepte un ou plusieurs fichiers sources et produit les fichiers de destination correspondants. Dans le cas de l’opération de suppression, le système tente de placer les fichiers supprimés dans la corbeille.

Il est également possible de déplacer des fichiers à l’aide de la fonctionnalité de [glisser-déplacer](dragdrop.md) .

Pour utiliser la fonction, vous devez renseigner les membres d’une structure [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) et la passer à [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa). Les membres clés de la structure sont **pFrom** et **pTo**.

Le membre **pFrom** est une chaîne double se terminant par un caractère **null** qui contient un ou plusieurs noms de fichiers sources. Ces noms peuvent être des chemins d’accès complets ou des caractères génériques DOS standard tels que \* . \* Bien que ce membre soit déclaré comme une chaîne terminée par le caractère **null**, il est utilisé comme mémoire tampon pour contenir plusieurs noms de fichiers. Chaque nom de fichier doit se terminer par le caractère **null** unique habituel. Un caractère **null** supplémentaire doit être ajouté à la fin du nom final pour indiquer la fin de **pFrom**.

Le membre **pTo** est une chaîne double terminée par un caractère **null**, similaire à **pFrom**. Le membre **pTo** contient les noms d’un ou de plusieurs noms de destination qualifiés complets. Elles sont compressées dans **pTo** de la même façon que pour les **pFrom**. Si **pTo** contient plusieurs noms, vous devez également définir l’indicateur **FOF \_ MULTIDESTFILES** dans le membre **fFlags** . L’utilisation de **pTo** dépend de l’opération, comme décrit ici.

-   Pour les opérations de copie et de déplacement, si tous les fichiers sont dirigés vers un répertoire unique, **pTo** contient le nom de répertoire complet. Si les fichiers sont destinés à des destinations différentes, la fonction **pTo** peut également contenir un nom de fichier ou de répertoire complet pour chaque fichier source. Si un répertoire n’existe pas, le système le crée.
-   Pour les opérations de changement de nom, **pTo** contient un chemin d’accès complet pour chaque fichier source dans **pFrom**.
-   Pour les opérations de suppression, **pTo** n’est pas utilisé.

### <a name="notifying-the-shell"></a>Notification de l’interpréteur de commandes

Notifiez l’interpréteur de la modification après avoir utilisé [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) pour déplacer, copier, renommer ou supprimer des fichiers, ou après avoir effectué une autre action qui affecte l’espace de noms. Les actions qui doivent être accompagnées de notifications sont les suivantes :

-   Ajout ou suppression de fichiers ou de dossiers.
-   Déplacement, copie ou attribution d’un nouveau nom aux fichiers ou dossiers.
-   Modification d’une association de fichiers.
-   Modification des attributs de fichier.
-   Ajout ou suppression de lecteurs ou de supports de stockage.
-   Création ou désactivation d’un dossier partagé.
-   Modification de la liste d’images système.

Une application avertit l’interpréteur de commandes en appelant [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) avec les détails de ce qui a changé. L’interpréteur de commandes peut ensuite mettre à jour son image de l’espace de noms pour refléter précisément son nouvel État.

## <a name="simple-example-of-managing-files-with-shfileoperation"></a>Exemple simple de gestion de fichiers avec SHFileOperation

L’exemple d’application console suivant illustre l’utilisation de [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) pour copier des fichiers d’un répertoire vers un autre. Les répertoires source et de destination, C : \\ My \_ docs et c : \\ My \_ Docs2, sont codés en dur dans l’application pour des raisons de simplicité.


```C++
#include <shlobj.h>
#include <shlwapi.h>
#include <strsafe.h>

int main(void)
{
    IShellFolder *psfDeskTop = NULL;
    IShellFolder *psfDocFiles = NULL;
    LPITEMIDLIST pidlDocFiles = NULL;
    LPITEMIDLIST pidlItems = NULL;
    IEnumIDList *ppenum = NULL;
    SHFILEOPSTRUCT sfo;
    STRRET strDispName;
    TCHAR szParseName[MAX_PATH];
    TCHAR szSourceFiles[256];
    int i;
    int iBufPos = 0;
    ULONG chEaten;
    ULONG celtFetched;
    size_t ParseNameSize = 0;
    HRESULT hr;
    

    szSourceFiles[0] = '\0';
    hr = SHGetDesktopFolder(&psfDeskTop);

    hr = psfDeskTop->ParseDisplayName(NULL, NULL, L"c:\\My_Docs", 
         &chEaten, &pidlDocFiles, NULL);
    hr = psfDeskTop->BindToObject(pidlDocFiles, NULL, IID_IShellFolder, 
         (LPVOID *) &psfDocFiles);
    hr = psfDeskTop->Release();

    hr = psfDocFiles->EnumObjects(NULL,SHCONTF_FOLDERS | SHCONTF_NONFOLDERS, 
         &ppenum);

    while( (hr = ppenum->Next(1,&pidlItems, &celtFetched)) == S_OK 
       && (celtFetched) == 1)
    {
        psfDocFiles->GetDisplayNameOf(pidlItems, SHGDN_FORPARSING, 
            &strDispName);
        StrRetToBuf(&strDispName, pidlItems, szParseName, MAX_PATH);
        
        hr = StringCchLength(szParseName, MAX_PATH, &ParseNameSize);
        
        if (SUCCEEDED(hr))
        {
            for(i=0; i<=ParseNameSize; i++)
            {
                szSourceFiles[iBufPos++] = szParseName[i];
            }
            CoTaskMemFree(pidlItems);
        }
    }
    ppenum->Release();
    
    szSourceFiles[iBufPos] = '\0';

    sfo.hwnd = NULL;
    sfo.wFunc = FO_COPY;
    sfo.pFrom = szSourceFiles;
    sfo.pTo = "c:\\My_Docs2\0";
    sfo.fFlags = FOF_SILENT | FOF_NOCONFIRMATION | FOF_NOCONFIRMMKDIR;

    hr = SHFileOperation(&sfo);
    
    SHChangeNotify(SHCNE_UPDATEDIR, SHCNF_PATH, (LPCVOID) "c:\\My_Docs2", 0);

    CoTaskMemFree(pidlDocFiles);
    psfDocFiles->Release();

    return 0;
}
```



L’application récupère d’abord un pointeur vers l’interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) du bureau. Il récupère ensuite le PIDL du répertoire source en passant son chemin d’accès complet à [**IShellFolder ::P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname). Notez que **IShellFolder ::P arsedisplayname** requiert que le chemin d’accès du répertoire soit une chaîne Unicode. L’application est ensuite liée au répertoire source et utilise son interface **IShellFolder** pour récupérer l’interface [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) d’un objet énumérateur.

À mesure que chaque fichier du répertoire source est énuméré, [**IShellFolder :: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) est utilisé pour récupérer son nom. L' \_ indicateur SHGDN FORPARSING est défini, ce qui amène **IShellFolder :: GetDisplayNameOf** à retourner le chemin d’accès qualifié complet du fichier. Les chemins d’accès aux fichiers, y compris les caractères **null** de fin, sont concaténés dans un tableau unique, *szSourceFiles*. Un deuxième caractère **null** est ajouté au chemin final pour terminer correctement le tableau.

Une fois l’énumération terminée, l’application assigne des valeurs à une structure [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) . Notez que le tableau affecté à **pTo** pour spécifier la destination doit également se terminer par une valeur double **null**. Dans ce cas, il est simplement inclus dans la chaîne qui est assignée à **pTo**. Étant donné qu’il s’agit d’une application console, les \_ indicateurs FOF Silent, FOF \_ noconfirm et FOF \_ NOCONFIRMMKDIR sont définis de manière à supprimer toutes les boîtes de dialogue susceptibles d’apparaître. Une fois [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) retourné, [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) est appelé pour avertir l’interpréteur de la modification. L’application effectue ensuite le nettoyage habituel et retourne.

## <a name="adding-files-to-the-shells-list-of-recent-documents"></a>Ajout de fichiers à la liste des documents récents de l’interpréteur de commandes

L’interpréteur de commandes gère une liste de documents récemment ajoutés ou modifiés pour chaque utilisateur. l’utilisateur peut afficher une liste de liens vers ces fichiers en cliquant sur Documents sur le menu Démarrer. Comme avec mes documents, chaque utilisateur dispose d’un répertoire de système de fichiers pour stocker les liens réels. Pour récupérer le PIDL de l’annuaire récent de l’utilisateur actuel, votre application peut appeler [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) avec CSIDL \_ récent ou appeler [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) pour récupérer son chemin d’accès.

Votre application peut énumérer le contenu du dossier récent à l’aide des techniques présentées plus haut dans ce document. Toutefois, une application ne doit pas modifier le contenu du dossier comme s’il s’agissait d’un dossier de système de fichiers normal. si c’est le cas, la liste des documents récents de l’interpréteur de commandes ne sera pas mise à jour correctement et les modifications ne seront pas reflétées dans la menu Démarrer. Au lieu de cela, pour ajouter un lien de document au dossier récent d’un utilisateur, votre application peut appeler [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs). l’interpréteur de commandes ajoute un lien au dossier du système de fichiers approprié et met à jour sa liste de documents récents et le menu Démarrer. Vous pouvez également utiliser cette fonction pour effacer le dossier.

 

 
