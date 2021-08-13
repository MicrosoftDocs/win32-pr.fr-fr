---
description: Avant de pouvoir utiliser un objet d’espace de noms, vous avez besoin d’un moyen de l’identifier.
ms.assetid: 54225481-a147-4d29-a642-24c9b59fc3ac
title: Obtention de l’ID d’un dossier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67d75051d52f0dfcee54b6365a8f546d2cbda2c3b5f7c0f4b6fbbc19fa1e40c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459008"
---
# <a name="getting-a-folders-id"></a>Obtention de l’ID d’un dossier

Avant de pouvoir utiliser un objet d’espace de noms, vous avez besoin d’un moyen de l’identifier. Cela signifie que vous obtenez son pointeur vers une liste d’identificateurs d’élément (PIDL) ou, dans le cas d’objets de système de fichiers, son chemin d’accès. Cette section présente deux méthodes plus simples pour obtenir des ID d’objet.

Pour bénéficier d’une approche plus puissante qui fonctionne avec n’importe quel dossier, utilisez l’interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) . Pour plus d’informations, consultez [obtention d’informations sur le contenu d’un dossier](folder-info.md) .

-   [La boîte de dialogue OpenFiles](#the-openfiles-dialog-box)
-   [Boîte de dialogue SHBrowseForFolder](#the-shbrowseforfolder-dialog-box)
-   [Dossiers spéciaux et CSIDLs](#special-folders-and-csidls)
-   [Exemple simple d’utilisation de CSIDLs et SHBrowseForFolder](#a-simple-example-of-how-to-use-csidls-and-shbrowseforfolder)

## <a name="the-openfiles-dialog-box"></a>La boîte de dialogue OpenFiles

Pour permettre à l’utilisateur de naviguer dans l’espace de noms et de sélectionner un dossier, votre application peut utiliser l’interface [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) . L’appel de cette interface avec l’indicateur **Fos \_ PICKFOLDERS** ouvre la boîte de dialogue courante [fichiers ouverts](../dlgbox/open-and-save-as-dialog-boxes.md) en mode « choisir des dossiers ».

pour Windows Vista et versions ultérieures, il s’agit de la méthode recommandée pour sélectionner des dossiers.

## <a name="the-shbrowseforfolder-dialog-box"></a>Boîte de dialogue SHBrowseForFolder

Pour permettre à l’utilisateur de naviguer dans l’espace de noms et de sélectionner un dossier, votre application peut simplement appeler [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera). L’appel de cette fonction lance une boîte de dialogue avec une interface utilisateur qui fonctionne quelque peu comme les boîtes de dialogue courantes [ouvrir ou enregistrer](../dlgbox/open-and-save-as-dialog-boxes.md) sous.

Lorsque l’utilisateur sélectionne un dossier, [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) retourne le PIDL complet du dossier et son nom complet. Si le dossier se trouve dans le système de fichiers, l’application peut convertir le PIDL en chemin d’accès en appelant [**SHGetPathFromIDList**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetpathfromidlista). L’application peut également limiter la plage de dossiers à partir de laquelle l’utilisateur peut sélectionner en spécifiant un dossier racine. Seuls les dossiers situés en dessous de la racine de l’espace de noms s’affichent. L’illustration suivante montre la boîte de dialogue **SHBrowseForFolder** , avec le dossier racine défini sur Program Files.

![capture d’écran de la boîte de dialogue Rechercher un dossier](images/shell1.png)

Un exemple simple d’utilisation de [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) est fourni ultérieurement.

## <a name="special-folders-and-csidls"></a>Dossiers spéciaux et CSIDLs

Un certain nombre de dossiers couramment utilisés sont désignés comme étant *spéciaux* par le système. Ces dossiers ont un objectif bien défini, et la plupart d’entre eux sont présents sur tous les systèmes. Même s’ils ne sont pas présents au départ, leurs noms et emplacements sont toujours définis, de sorte qu’ils peuvent être ajoutés ultérieurement. La collection de dossiers spéciaux comprend tous les dossiers virtuels standard du système, tels que imprimantes, mes documents et voisinage réseau. Il comprend également un certain nombre de dossiers de système de fichiers standard, tels que Program Files et System.

Même si les dossiers sont un composant standard de tous les systèmes, leur nom et leur emplacement dans l’espace de noms peuvent varier. par exemple, le répertoire système est c : \\ winnt \\ system32 sur certains systèmes et c : \\ Windows \\ system32 sur d’autres. Dans le passé, les variables d’environnement offraient un moyen de déterminer le nom et l’emplacement d’un dossier spécial sur un système particulier. L’interpréteur de commandes offre désormais un moyen plus robuste et plus souple d’identifier les dossiers spéciaux, [**CSIDLs**](csidl.md). Vous devez généralement les utiliser à la place des variables d’environnement.

Les CSIDLs offrent un moyen uniforme d’identifier et de localiser des dossiers spéciaux, quel que soit leur nom ou emplacement sur un système particulier. Contrairement aux variables d’environnement, CSIDLs peut être utilisé avec des dossiers virtuels et des dossiers de système de fichiers. Chaque dossier spécial est associé à un CSIDL unique. Par exemple, le dossier Program Files File System contient un CSIDL des **\_ \_ fichiers programme de CSIDL** et le dossier virtuel du voisinage réseau a un CSIDL du **\_ réseau CSIDL**.

Un CSIDL est utilisé conjointement avec l’une des nombreuses fonctions Shell pour récupérer le PIDL d’un dossier spécial, ou le chemin d’accès d’un dossier de système de fichiers spécial. Si le dossier n’existe pas sur un système, votre application peut forcer sa création en combinant le CSIDL avec l' **indicateur CSIDL \_ \_ Create**. Le CSIDL peut être passé aux fonctions suivantes :

-   [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation), qui récupère le PIDL d’un dossier spécial.
-   [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha), qui récupère le chemin d’accès d’un dossier spécial du système de fichiers.

Notez que ces deux fonctions ont été introduites avec la version 5,0 de l’interpréteur de commandes et remplacent les fonctions [**SHGetSpecialFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderlocation) et [**SHGetSpecialFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderpatha) .

## <a name="a-simple-example-of-how-to-use-csidls-and-shbrowseforfolder"></a>Exemple simple d’utilisation de CSIDLs et SHBrowseForFolder

L’exemple de fonction suivant, PidlBrowse, montre comment utiliser CSIDLs pour récupérer les PIDL d’un dossier et utiliser [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) pour que l’utilisateur sélectionne un dossier. Elle retourne le PIDL et le nom d’affichage du dossier sélectionné.


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



L’application appelante passe un handle de fenêtre, qui est requis par [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera). Le paramètre *nCSIDL* est un CSIDL facultatif qui est utilisé pour spécifier un dossier racine. Seuls les dossiers situés sous le dossier racine de la hiérarchie s’affichent. L’illustration ci-dessus a été générée en appelant cette fonction avec *nCSIDL* défini sur **\_ \_ fichiers programmes CSIDL**. L’application appelante passe également dans une mémoire tampon de chaîne, *pszDisplayName*, pour contenir le nom complet du dossier sélectionné lorsque PidlBrowse retourne. Il incombe à l’application appelante de libérer le IDList retourné par **SHBrowseForFolder** à l’aide de [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).

 

 
