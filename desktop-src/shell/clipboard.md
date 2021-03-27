---
description: Les formats de presse-papiers de l’interpréteur de commandes sont utilisés pour identifier le type de données de Shell transférées via le presse-papiers.
ms.assetid: fb8ce5d3-3215-4e05-a916-4d4a803464d2
title: Formats de presse-papiers de Shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 674ccc33db3a35a1a60abb549f5e1ab5b5c96760
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750268"
---
# <a name="shell-clipboard-formats"></a>Formats de presse-papiers de Shell

Les formats de presse-papiers de l’interpréteur de commandes sont utilisés pour identifier le type de données de Shell transférées via le presse-papiers. La plupart des formats de presse-papiers de l’interpréteur de commandes identifient un type de données, par exemple une liste de noms de fichiers ou de pointeurs vers des listes d’identificateurs d’élément (PIDL). Toutefois, certains formats sont utilisés pour la communication entre la source et la cible. Ils peuvent accélérer le processus de transfert de données en prenant en charge les opérations de Shell, telles que le déplacement et la [delete_on_paste](datascenarios.md) [optimisés](datascenarios.md) . Les données de l’interpréteur de commandes sont toujours contenues dans un [objet de données](dataobject.md) qui utilise une structure [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) comme un moyen plus général de caractériser les données. Le membre **cfFormat** de la structure est défini sur le format du presse-papiers pour l’élément de données particulier. Les autres membres fournissent des informations supplémentaires, telles que le mécanisme de transfert de données. Les données sont contenues dans une structure [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) qui l’accompagne.

> [!Note]  
> Les identificateurs de format du presse-papiers standard se présentent sous la forme CF_ *xxx*. Un exemple courant est CF_TEXT, qui est utilisé pour transférer des données texte ANSI. Ces identificateurs ont des valeurs prédéfinies et peuvent être utilisés directement avec les structures [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) . À l’exception de [CF_HDROP](#cf_hdrop), les identificateurs de format de Shell ne sont pas prédéfinis. À l’exception de DragWindow, ils se présentent sous la forme CFSTR_ *xxx*. Pour différencier ces valeurs des formats prédéfinis, ils sont souvent appelés simples *formats*. Toutefois, à la différence des formats prédéfinis, ils doivent être inscrits par source et cible avant de pouvoir être utilisés pour transférer des données. Pour inscrire un format de Shell, incluez le fichier d’en-tête shlobj. h et transmettez l’identificateur de format CFSTR_ *xxx* à [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata). Cette fonction retourne une valeur de format de presse-papiers valide, qui peut ensuite être utilisée en tant que membre **cfFormat** d’une structure **FORMATETC** .

 

Les formats du presse-papiers de l’interpréteur de commandes sont organisés ici en trois groupes, en fonction de leur utilisation.

-   [Formats pour le transfert d’objets de système de fichiers](#formats-for-transferring-file-system-objects)
    -   [CF_HDROP](#cf_hdrop)
    -   [CFSTR_FILECONTENTS](#cfstr_filecontents)
    -   [CFSTR_FILEDESCRIPTOR](#cfstr_filedescriptor)
    -   [CFSTR_FILENAME](#cfstr_filename)
    -   [CFSTR_FILENAMEMAP](#cfstr_filenamemap)
    -   [CFSTR_MOUNTEDVOLUME](#cfstr_mountedvolume)
    -   [CFSTR_SHELLIDLIST](#cfstr_shellidlist)
    -   [CFSTR_SHELLIDLISTOFFSET](#cfstr_shellidlistoffset)
-   [Formats pour le transfert d’objets virtuels](#formats-for-transferring-virtual-objects)
    -   [CFSTR_NETRESOURCES](#cfstr_netresources)
    -   [CFSTR_PRINTERGROUP](#cfstr_printergroup)
    -   [CFSTR_INETURL](#cfstr_ineturl)
    -   [CFSTR_SHELLURL (déconseillée)](#cfstr_shellurl-deprecated)
-   [Formats pour la communication entre la source et la cible](#formats-for-communication-between-source-and-target)
    -   [CFSTR_INDRAGLOOP](#cfstr_indragloop)
    -   [CFSTR_LOGICALPERFORMEDDROPEFFECT](#cfstr_logicalperformeddropeffect)
    -   [CFSTR_PASTESUCCEEDED](#cfstr_pastesucceeded)
    -   [CFSTR_PERFORMEDDROPEFFECT](#cfstr_performeddropeffect)
    -   [CFSTR_PREFERREDDROPEFFECT](#cfstr_preferreddropeffect)
    -   [CFSTR_TARGETCLSID](#cfstr_targetclsid)
    -   [CFSTR_UNTRUSTEDDRAGDROP](#cfstr_untrusteddragdrop)
    -   [DragWindow](#dragwindow)

## <a name="formats-for-transferring-file-system-objects"></a>Formats pour le transfert d’objets de système de fichiers

Ces formats sont utilisés pour transférer un ou plusieurs fichiers ou d’autres objets Shell.

-   [CF_HDROP](#cf_hdrop)
-   [CFSTR_FILECONTENTS](#cfstr_filecontents)
-   [CFSTR_FILEDESCRIPTOR](#cfstr_filedescriptor)
-   [CFSTR_FILENAME](#cfstr_filename)
-   [CFSTR_FILENAMEMAP](#cfstr_filenamemap)
-   [CFSTR_MOUNTEDVOLUME](#cfstr_mountedvolume)
-   [CFSTR_SHELLIDLIST](#cfstr_shellidlist)
-   [CFSTR_SHELLIDLISTOFFSET](#cfstr_shellidlistoffset)

### <a name="cf_hdrop"></a>CF_HDROP

Ce format de presse-papiers est utilisé lors du transfert des emplacements d’un groupe de fichiers existants. Contrairement aux autres formats de Shell, il est prédéfini, donc il n’est pas nécessaire d’appeler [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata). Les données se composent d’une structure [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) qui contient un objet mémoire global. Le membre **HGLOBAL** de la structure pointe vers une structure [**DROPFILES**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropfiles) comme membre **HGLOBAL** .

Le membre **fichiers pfile** de la structure [**DROPFILES**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropfiles) contient un décalage vers un tableau de caractères double se terminant par un caractère **null** qui contient les noms de fichiers. Si vous extrayez un format de CF_HDROP à partir d’un objet de données, vous pouvez utiliser [**DragQueryFile**](/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea) pour extraire des noms de fichiers individuels de l’objet mémoire globale. Si vous créez un format de CF_HDROP à placer dans un objet de données, vous devrez construire le tableau de noms de fichiers.

Le tableau de noms de fichiers se compose d’une série de chaînes, chacune contenant le chemin d’accès complet d’un fichier, y compris le caractère **null** de fin. Un caractère **null** supplémentaire est ajouté à la chaîne finale pour terminer le tableau. Par exemple, si les fichiers c : \\temp1.txt et c : \\temp2.txt sont en cours de transfert, le tableau de caractères se présente comme suit :


```CMD
c:\temp1.txt'\0'c:\temp2.txt'\0''\0'
```

> [!Note]  
> Dans cet exemple, « \\ 0 » est utilisé pour représenter le caractère **null** , et non les caractères littéraux qui doivent être inclus.


Si l’objet a été copié dans le presse-papiers dans le cadre d’une opération de glisser-déplacer, le membre **PT** de la structure [**DROPFILES**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropfiles) contient les coordonnées du point où l’objet a été supprimé. Vous pouvez utiliser [**DragQueryPoint**](/windows/desktop/api/Shellapi/nf-shellapi-dragquerypoint) pour extraire les coordonnées du curseur.

Si ce format est présent dans un objet de données, une boucle OLE Drag simule [**WM_DROPFILES**](wm-dropfiles.md) fonctionnalité avec des cibles de dépôt non-OLE. Cela est important si votre application est la source d’une opération de glisser-déplacer sur un système Windows 3,1.

### <a name="cfstr_filecontents"></a>CFSTR_FILECONTENTS

Cet identificateur de format est utilisé avec le format [CFSTR_FILEDESCRIPTOR](#cfstr_filedescriptor) pour transférer des données comme s’il s’agissait d’un fichier, quelle que soit la manière dont il est réellement stocké. Les données se composent d’une structure [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) qui représente le contenu d’un fichier. Le fichier est normalement représenté sous la forme d’un objet de flux, ce qui évite d’avoir à placer le contenu du fichier en mémoire. Dans ce cas, le membre **TYMED** de la structure **STGMEDIUM** est défini sur TYMED_ISTREAM, et le fichier est représenté par une interface [**ISTREAM**](/windows/win32/api/objidl/nn-objidl-istream) . Le fichier peut également être un objet de stockage ou de mémoire globale (TYMED_ISTORAGE ou TYMED_HGLOBAL). Le format de CFSTR_FILEDESCRIPTOR associé contient une structure [**FILEDESCRIPTOR**](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora) pour chaque fichier qui spécifie le nom et les attributs du fichier.

La cible traite les données associées à un format de CFSTR_FILECONTENTS comme s’il s’agissait d’un fichier. Quand la cible appelle [**IDataObject :: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) pour extraire les données, elle spécifie un fichier particulier en définissant le membre **Lindex** de la structure [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) sur l’index de base zéro de la structure [**FILEDESCRIPTOR**](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora) du fichier dans le format d' [CFSTR_FILEDESCRIPTOR](#cfstr_filedescriptor) qui l’accompagne. La cible utilise ensuite le pointeur d’interface retourné ou le handle de mémoire globale pour extraire les données.

### <a name="cfstr_filedescriptor"></a>CFSTR_FILEDESCRIPTOR

Cet identificateur de format est utilisé avec le format [CFSTR_FILECONTENTS](#cfstr_filecontents) pour transférer des données sous la forme d’un groupe de fichiers. Ces deux formats sont la méthode recommandée pour transférer des objets Shell qui ne sont pas stockés en tant que fichiers de système de fichiers. Par exemple, ces formats peuvent être utilisés pour transférer un groupe de messages électroniques en tant que fichiers individuels, même si chaque e-mail est stocké en tant que bloc de données dans une base de données. Les données se composent d’une structure [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) qui contient un objet mémoire global. Le membre **hGlobal** de la structure pointe vers une structure [**FILEGROUPDESCRIPTOR**](/windows/win32/api/shlobj_core/ns-shlobj_core-filegroupdescriptora) qui est suivie d’un tableau contenant une structure [**FILEDESCRIPTOR**](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora) pour chaque fichier du groupe. Pour chaque structure **FILEDESCRIPTOR** , il existe un format de CFSTR_FILECONTENTS distinct qui contient le contenu du fichier. Pour identifier le format de CFSTR_FILECONTENTS d’un fichier particulier, définissez la valeur **Lindex** de la structure [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) sur l’index de base zéro de la structure **FILEDESCRIPTOR** du fichier.

Le format CFSTR_FILEDESCRIPTOR est couramment utilisé pour transférer des données comme s’il s’agissait d’un groupe de fichiers, quelle que soit la façon dont ils sont réellement stockés. Du point de vue de la cible, chaque format de CFSTR_FILECONTENTS représente un fichier unique et est traité en conséquence. Toutefois, la source peut stocker les données de la manière choisie. Bien qu’un format de CSFTR_FILECONTENTS puisse correspondre à un seul fichier, il peut, par exemple, représenter des données extraites par la source à partir d’une base de données ou d’un document texte.

### <a name="cfstr_filename"></a>CFSTR_FILENAME

Cet identificateur de format est utilisé pour transférer un fichier unique. Les données se composent d’une structure [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) qui contient un objet mémoire global. Le membre **hGlobal** de la structure pointe vers une chaîne unique se terminant par un caractère **null** qui contient le chemin d’accès complet au fichier. Ce format a été remplacé par [CF_HDROP](#cf_hdrop), mais il est pris en charge pour la compatibilité descendante avec les applications Windows 3,1.

### <a name="cfstr_filenamemap"></a>CFSTR_FILENAMEMAP

Cet identificateur de format est utilisé lorsqu’un groupe de fichiers au format [CF_HDROP](#cf_hdrop) est renommé et transféré. Les données se composent d’une structure [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) qui contient un objet mémoire global. Le membre **hGlobal** de la structure pointe vers un tableau de caractères double se terminant par un caractère **null**. Ce tableau contient un nouveau nom pour chaque fichier, dans l’ordre dans lequel les fichiers sont répertoriés dans le format d’CF_HDROP qui l’accompagne. Le format du tableau de caractères est le même que celui utilisé par CF_HDROP pour répertorier les fichiers transférés.

### <a name="cfstr_mountedvolume"></a>CFSTR_MOUNTEDVOLUME

Cet identificateur de format est utilisé pour transférer un chemin sur un volume monté. Elle est similaire à [CF_HDROP](#cf_hdrop), mais elle ne contient qu’un seul chemin d’accès et peut gérer les chaînes de chemin d’accès plus longues qui peuvent être nécessaires pour représenter un chemin d’accès lorsque le volume est monté sur un dossier. Les données se composent d’une structure [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) qui contient un objet mémoire global. Le membre **hGlobal** de la structure pointe vers une chaîne unique se terminant par un caractère **null** qui contient le chemin d’accès complet au fichier. La chaîne de chemin d’accès doit se terminer par un \\ caractère «», suivi de la **valeur null** de fin.

Avant Windows 2000, les volumes pouvaient être montés uniquement sur des lettres de lecteur. Pour les systèmes Windows 2000 et versions ultérieures avec un lecteur au format NTFS, vous pouvez également monter des volumes sur des dossiers vides. Cette fonctionnalité permet de monter un volume sans prendre de lettre de lecteur. Le volume monté peut utiliser n’importe quel format actuellement pris en charge, y compris FAT, FAT32, NTFS et CDFS.

Vous pouvez ajouter des pages à une feuille de propriétés de propriétés de lecteur en implémentant un [Gestionnaire de feuille de propriétés](propsheet-handlers.md). Si le volume est monté sur une lettre de lecteur, l’interpréteur de commandes transmet les informations de chemin d’accès au gestionnaire avec le format [CF_HDROP](#cf_hdrop) . Avec les systèmes Windows 2000 et versions ultérieures, le format de CF_HDROP est utilisé lorsqu’un volume est monté sur une lettre de lecteur, tout comme avec les systèmes précédents. Toutefois, si un volume est monté sur un dossier, le [CFSTR_MOUNTEDVOLUME](#cfstr_mountedvolume) identificateur de format est utilisé à la place de CF_HDROP.

Si seules les lettres de lecteur sont utilisées pour monter des volumes, seules les [CF_HDROP](#cf_hdrop) sont utilisées, et les gestionnaires de feuille de propriétés existants fonctionnent comme pour les systèmes antérieurs. Toutefois, si vous souhaitez que votre gestionnaire affiche une page pour les volumes montés sur des dossiers, ainsi que des lettres de lecteur, le gestionnaire doit être en mesure de comprendre les formats CSFTR_MOUNTEDVOLUME et CF_HDROP.

### <a name="cfstr_shellidlist"></a>CFSTR_SHELLIDLIST

Cet identificateur de format est utilisé lors du transfert des emplacements d’un ou plusieurs objets d’espace de noms existants. Il est utilisé à peu près de la même façon que [CF_HDROP](#cf_hdrop), mais il contient PIDL au lieu des chemins de système de fichiers. L’utilisation de PIDL permet au format CFSTR_SHELLIDLIST de gérer des objets virtuels et des objets de système de fichiers. Les données sont une structure [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) qui contient un objet mémoire global. Le membre **hGlobal** de [**la structure pointe vers une structure**](/windows/win32/api/shlobj_core/ns-shlobj_core-cida) a.

Le membre **aoffset** de la [**structure dispose**](/windows/win32/api/shlobj_core/ns-shlobj_core-cida) est un tableau contenant des décalages au début de la structure [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) pour chaque PIDL en cours de transfert. Pour extraire un PIDL particulier, commencez par déterminer son index. Ensuite, ajoutez la valeur **aoffset** qui correspond à cet index **à l’adresse de la structure d'** avant.

Le premier élément de **aoffset** contient un décalage vers le PIDL complet d’un dossier parent. Si ce PIDL est vide, le dossier parent est le bureau. Chacun des éléments restants du tableau contient un offset à l’un des PIDL à transférer. Tous ces PIDL sont relatifs au PIDL du dossier parent.

Les deux macros suivantes peuvent être utilisées pour récupérer des PIDL à partir [**d’une structure de**](/windows/win32/api/shlobj_core/ns-shlobj_core-cida) préversion. La première prend un pointeur vers la structure et récupère le PIDL du dossier parent. Le deuxième prend un pointeur vers la structure et récupère l’un des autres PIDL, identifié par son index de base zéro.


```C++
#define GetPIDLFolder(pida) (LPCITEMIDLIST)(((LPBYTE)pida)+(pida)->aoffset[0])

#define GetPIDLItem(pida, i) (LPCITEMIDLIST)(((LPBYTE)pida)+(pida)->aoffset[i+1])
```

> [!Note]  
> La valeur retournée par ces macros est un pointeur vers la structure [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) du PIDL. Dans la mesure où ces structures varient en longueur, vous devez déterminer la fin de la structure en parcourant chacune des structures [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) de la structure **ITEMIDLIST** jusqu’à atteindre la **valeur null** sur deux octets qui marque la fin.

### <a name="cfstr_shellidlistoffset"></a>CFSTR_SHELLIDLISTOFFSET

Cet identificateur de format est utilisé avec les formats tels que [CF_HDROP](#cf_hdrop), [CFSTR_SHELLIDLIST](#cfstr_shellidlist)et [CFSTR_FILECONTENTS](#cfstr_filecontents) pour spécifier la position d’un groupe d’objets après un transfert. Les données se composent d’une structure [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) qui contient un objet mémoire global. Le membre **hGlobal** de la structure pointe vers un tableau de structures [**point**](/previous-versions//dd162805(v=vs.85)) . La première structure spécifie les coordonnées d’écran, en pixels, de l’angle supérieur gauche du rectangle qui englobe le groupe. Les autres structures spécifient les emplacements des objets individuels par rapport à la position du groupe. Ils doivent être dans le même ordre que celui utilisé pour répertorier les objets dans le format associé.

## <a name="formats-for-transferring-virtual-objects"></a>Formats pour le transfert d’objets virtuels

Le format de CFSTR_SHELLIDLIST peut être utilisé pour transférer à la fois le système de fichiers et les objets virtuels. Toutefois, il existe également plusieurs formats spécialisés pour transférer des types particuliers d’objets virtuels.

-   [CFSTR_NETRESOURCES](#cfstr_netresources)
-   [CFSTR_PRINTERGROUP](#cfstr_printergroup)
-   [CFSTR_INETURL](#cfstr_ineturl)
-   [CFSTR_SHELLURL (déconseillée)](#cfstr_shellurl-deprecated)

### <a name="cfstr_netresources"></a>CFSTR_NETRESOURCES

Cet identificateur de format est utilisé lors du transfert des ressources réseau, telles qu’un domaine ou un serveur. Les données sont une structure [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) qui contient un objet mémoire global. Le membre **hGlobal** de la structure pointe vers une structure [**NRESARRAY**](/windows/desktop/api/shlobj_core/ns-shlobj_core-nresarray) . Le membre **Nr** de cette structure indique une structure [**Resource**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) dont le membre **lpRemoteName** contient une chaîne terminée par le caractère **null** qui identifie la ressource réseau. La cible de déplacement peut ensuite utiliser les données avec l’une des fonctions d’API de [mise en réseau Windows (WNET)](../wnet/windows-networking-wnet-.md) , telles que [**WNetAddConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnectiona), pour effectuer des opérations réseau sur l’objet.

### <a name="cfstr_printergroup"></a>CFSTR_PRINTERGROUP

Cet identificateur de format est utilisé lors du transfert des noms conviviaux des imprimantes. Les données sont une structure [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) qui contient un objet mémoire global. Le membre **hGlobal** de la structure pointe vers une chaîne dans le même format que celui utilisé avec [CF_HDROP](#cf_hdrop). Toutefois, le membre **fichiers pfile** de la structure [**DROPFILES**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropfiles) contient un ou plusieurs noms conviviaux d’imprimantes au lieu de chemins d’accès aux fichiers.

### <a name="cfstr_ineturl"></a>CFSTR_INETURL

Cet identificateur de format remplace [CFSTR_SHELLURL (déconseillé)](#cfstr_shellurl-deprecated). Si vous souhaitez que votre application manipule les URL du presse-papiers, utilisez CFSTR_INETURL au lieu de CFSTR_SHELLURL (déconseillé). Ce format donne la meilleure représentation du presse-papiers d’une URL unique. Si UNICODE n’est pas défini, l’application récupère la version CF_TEXT/CFSTR_SHELLURL de l’URL. Si UNICODE est défini, l’application récupère la version CF_UNICODE de l’URL.

### <a name="cfstr_shellurl-deprecated"></a>CFSTR_SHELLURL (déconseillée)

> [!Note]  
> Cet identificateur de format est déconseillé. Utilisez à la place CFSTR_INETURL.

 

## <a name="formats-for-communication-between-source-and-target"></a>Formats pour la communication entre la source et la cible

Ces identificateurs de format autorisent la communication entre la source et la cible. Les formats accompagnent les données et donnent aux applications un plus grand contrôle sur les opérations de glisser-copier-coller ou de glisser-déplacer impliquant des objets Shell.

-   [CFSTR_INDRAGLOOP](#cfstr_indragloop)
-   [CFSTR_LOGICALPERFORMEDDROPEFFECT](#cfstr_logicalperformeddropeffect)
-   [CFSTR_PASTESUCCEEDED](#cfstr_pastesucceeded)
-   [CFSTR_PERFORMEDDROPEFFECT](#cfstr_performeddropeffect)
-   [CFSTR_PREFERREDDROPEFFECT](#cfstr_preferreddropeffect)
-   [CFSTR_TARGETCLSID](#cfstr_targetclsid)
-   [CFSTR_UNTRUSTEDDRAGDROP](#cfstr_untrusteddragdrop)
-   [DragWindow](#dragwindow)

### <a name="cfstr_indragloop"></a>CFSTR_INDRAGLOOP

Cet identificateur de format est utilisé par un objet de données pour indiquer s’il se trouve dans une boucle de glisser-déplacer. Les données sont une structure [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) qui contient un objet mémoire global. Le membre **hGlobal** de la structure pointe vers une valeur **DWORD** . Si la valeur **DWORD** est différente de zéro, l’objet de données se trouve dans une boucle de glisser-déplacer. Si la valeur est définie sur zéro, l’objet de données ne se trouve pas dans une boucle de glisser-déplacer.

Certaines cibles de déplacement peuvent appeler [**IDataObject :: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) et tenter d’extraire des données alors que l’objet se trouve toujours dans la boucle de glisser-déplacer. Le rendu complet de l’objet pour chaque occurrence peut entraîner le blocage du curseur de glissement. Si l’objet de données prend en charge [CFSTR_INDRAGLOOP](#cfstr_indragloop), la cible peut à la place utiliser ce format pour vérifier l’état de la boucle de glisser-déplacer et éviter le rendu gourmand en mémoire de l’objet jusqu’à ce qu’il soit réellement supprimé. Les formats qui consomment beaucoup de mémoire à restituer doivent toujours être inclus dans l’énumérateur [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) et dans les appels à [**IDataObject :: QueryGetData**](/windows/win32/api/objidl/nf-objidl-idataobject-querygetdata). Si l’objet de données ne définit pas CFSTR_INDRAGLOOP, il doit agir comme si la valeur était définie sur zéro.

### <a name="cfstr_logicalperformeddropeffect"></a>CFSTR_LOGICALPERFORMEDDROPEFFECT

[Version 5,0.](versions.md) Cet identificateur de format permet à une source de déplacement d’appeler la méthode [**IDataObject :: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) de l’objet de données pour déterminer le résultat d’un transfert de données de Shell. Les données sont une structure [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) qui contient un objet mémoire global. Le membre **hGlobal** de la structure pointe vers une valeur DWORD contenant une valeur [**DROPEFFECT**](../com/dropeffect-constants.md) .

L’identificateur de format [CFSTR_PERFORMEDDROPEFFECT](#cfstr_performeddropeffect) a été conçu pour permettre à la cible d’indiquer à l’objet de données la nature de l’opération qui a réellement eu lieu. Toutefois, l’interpréteur de commandes utilise des [déplacements optimisés](datascenarios.md) pour les objets du système de fichiers dans la mesure du possible. Dans ce cas, le shell définit normalement la valeur CFSTR_PERFORMEDDROPEFFECT sur DROPEFFECT_NONE pour indiquer à l’objet de données que les données d’origine ont été supprimées. Par conséquent, la source ne peut pas utiliser la valeur CFSTR_PERFORMEDDROPEFFECT pour déterminer quelle opération a eu lieu. Alors que la plupart des sources n’ont pas besoin de ces informations, il existe des exceptions. Par exemple, même si les déplacements optimisés éliminent la nécessité d’une source pour supprimer des données, il se peut que la source doive toujours mettre à jour une base de données associée pour indiquer que les fichiers ont été déplacés ou copiés.

Si une source doit savoir quelle opération a eu lieu, elle peut appeler la méthode [**IDataObject :: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) de l’objet de données et demander le format de CFSTR_LOGICALPERFORMEDDROPEFFECT. Ce format reflète essentiellement ce qui se passe du point de vue de l’utilisateur une fois l’opération terminée. Si un nouveau fichier est créé et que le fichier d’origine est supprimé, l’utilisateur voit une opération de déplacement et la valeur de données du format est définie sur DROPEFFECT_MOVE. Si le fichier d’origine est toujours présent, l’utilisateur voit une opération de copie et la valeur de données du format est définie sur DROPEFFECT_COPY. Si un lien a été créé, la valeur de données du format sera DROPEFFECT_LINK.

### <a name="cfstr_pastesucceeded"></a>CFSTR_PASTESUCCEEDED

Cet identificateur de format est utilisé par la cible pour informer l’objet de données, par le biais de sa méthode [**IDataObject :: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) , qu’une opération de suppression sur le collage a réussi. Les données sont une structure [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) qui contient un objet mémoire global. Le membre **hGlobal** de la structure pointe vers une valeur **DWORD** contenant une valeur [**DROPEFFECT**](../com/dropeffect-constants.md) . Ce format est utilisé pour notifier à l’objet de données qu’il doit terminer l’opération de coupe et supprimer les données d’origine, si nécessaire. Pour plus d’informations, consultez [opérations de suppression sur le collage](datascenarios.md).

### <a name="cfstr_performeddropeffect"></a>CFSTR_PERFORMEDDROPEFFECT

Cet identificateur de format est utilisé par la cible pour informer l’objet de données par le biais de sa méthode [**IDataObject :: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) du résultat d’un transfert de données. Les données sont une structure [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) qui contient un objet mémoire global. Le membre **hGlobal** de la structure pointe vers une valeur **DWORD** définie sur la valeur [**DROPEFFECT**](../com/dropeffect-constants.md) appropriée, normalement DROPEFFECT_MOVE ou DROPEFFECT_COPY.

Ce format est normalement utilisé lorsque le résultat d’une opération peut être Move ou Copy, par exemple dans le cadre d’une opération de déplacement ou de suppression sur le collage [optimisée](datascenarios.md) . Il fournit un moyen fiable pour la cible d’indiquer à l’objet de données ce qui s’est réellement produit. Elle a été introduite, car la valeur de *pdwEffect* retournée par [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) n’indique pas quelle opération a eu lieu. Le format [CFSTR_PERFORMEDDROPEFFECT](#cfstr_performeddropeffect) est la méthode fiable pour indiquer qu’un déplacement non optimisé a eu lieu.

### <a name="cfstr_preferreddropeffect"></a>CFSTR_PREFERREDDROPEFFECT

Cet identificateur de format est utilisé par la source pour spécifier si sa méthode préférée de transfert de données est Move ou Copy. Une cible de déplacement demande ce format en appelant la méthode [**IDataObject :: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) de l’objet de données. Les données sont une structure [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) qui contient un objet mémoire global. Le membre **hGlobal** de la structure pointe vers une valeur **DWORD** . Cette valeur est définie sur DROPEFFECT_MOVE si une opération de déplacement est préférable ou DROPEFFECT_COPY si une opération de copie est préférable.

Cette fonctionnalité est utilisée lorsqu’une source peut prendre en charge une opération de déplacement ou de copie. Elle utilise le format de [CFSTR_PREFERREDDROPEFFECT](#cfstr_preferreddropeffect) pour communiquer sa préférence à la cible. Étant donné que la cible n’est pas obligée d’honorer la demande, la cible doit appeler la méthode [**IDataObject :: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) de la source avec un format [CFSTR_PERFORMEDDROPEFFECT](#cfstr_performeddropeffect) pour indiquer à l’objet de données quelle opération a été effectuée réellement.

Avec une opération de [suppression sur le collage](datascenarios.md) , le format de CFSTR_PREFERREDDROPFORMAT est utilisé pour indiquer à la cible si la source a effectué une coupe ou une copie. Avec une opération de glisser-déplacer, vous pouvez utiliser CFSTR_PREFERREDDROPFORMAT pour spécifier l’action de l’interpréteur de commandes. Si ce format n’est pas présent, l’interpréteur de commandes effectue une action par défaut en fonction du contexte. Par exemple, si un utilisateur fait glisser un fichier à partir d’un volume et le dépose sur un autre volume, l’action par défaut de l’interpréteur de commandes consiste à copier le fichier. En incluant un format de CFSTR_PREFERREDDROPFORMAT dans l’objet de données, vous pouvez substituer l’action par défaut et indiquer explicitement à l’interpréteur de commandes de copier, déplacer ou lier le fichier. Si l’utilisateur choisit de faire glisser avec le bouton droit, CFSTR_PREFERREDDROPFORMAT spécifie la commande par défaut dans le menu contextuel [glisser-déplacer](context-menu-handlers.md) . L’utilisateur est toujours libre de choisir d’autres commandes dans le menu.

Avant Microsoft Internet Explorer 4,0, une application indiquait qu’elle transférait des types de fichiers de raccourci en définissant FD_LINKUI dans le membre **dwFlags** de la structure [**FILEDESCRIPTOR**](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora) . Les cibles devaient ensuite utiliser un appel potentiellement fastidieux à [**IDataObject :: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) pour déterminer si l’indicateur de FD_LINKUI a été défini. À présent, la meilleure façon d’indiquer que les raccourcis sont transférés consiste à utiliser le format de CFSTR_PREFERREDDROPEFFECT défini sur DROPEFFECT_LINK. Toutefois, pour assurer la compatibilité descendante avec les systèmes plus anciens, les sources doivent toujours définir l’indicateur FD_LINKUI.

### <a name="cfstr_targetclsid"></a>CFSTR_TARGETCLSID

Cet identificateur de format est utilisé par une cible pour fournir son CLSID à la source. Les données sont une structure [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) qui contient un objet mémoire global. Le membre **hGlobal** de la structure pointe vers le GUID CLSID de la cible de déplacement.

Ce format est principalement utilisé pour permettre la suppression d’objets en les faisant glisser vers la corbeille. Lorsqu’un objet est supprimé dans la corbeille, la méthode [**IDataObject :: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) de la source est appelée avec un CFSTR_TARGETCLSID format défini sur le CLSID de la corbeille (CLSID_RecycleBin). La source peut ensuite supprimer l’objet d’origine.

### <a name="cfstr_untrusteddragdrop"></a>CFSTR_UNTRUSTEDDRAGDROP

Cet identificateur de format est utilisé par Windows Internet Explorer et le shell Windows pour fournir un mécanisme permettant de bloquer ou de demander des opérations de glisser-déplacer provenant d’Internet Explorer conjointement avec l’indicateur [**URLACTION_SHELL_ENHANCED_DRAGDROP_SECURITY**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537178(v=vs.85)) .

**CFSTR_UNTRUSTEDDRAGDROP** est ajouté par la source d’une opération de glisser-déplacer pour spécifier que l’objet de données peut contenir des données non fiables. Les données sont représentées par une structure [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) qui contient un objet mémoire global. Le membre **hGlobal** de la structure pointe vers un **DWORD** défini sur un indicateur d' [**action d’URL**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537178(v=vs.85)) approprié pour déclencher une vérification de stratégie par le biais de la méthode [**IInternetSecurityManager ::P rocessurlaction**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537136(v=vs.85)) , à l’aide de l’indicateur [**PUAF_ENFORCERESTRICTED**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537171(v=vs.85)) .

### <a name="dragwindow"></a>DragWindow

Ce format est utilisé dans une opération de glisser-déplacer pour identifier l’image de glissement d’un objet (fenêtre) afin que ses informations visuelles puissent être mises à jour dynamiquement. Lorsqu’un objet est glissé sur une cible de dépôt, une application met à jour sa structure [**DROPDESCRIPTION**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription) en réponse à la méthode [**IDropTarget ::D ragover**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) ou [**IDropSource :: GiveFeedback**](/windows/win32/api/oleidl/nf-oleidl-idropsource-givefeedback) . Le **DROPDESCRIPTION** est mis à jour avec une nouvelle valeur [**DROPIMAGETYPE**](/windows/desktop/api/shlobj_core/ne-shlobj_core-dropimagetype) qui indique la décoration à appliquer au visuel de la fenêtre de glissement. par exemple, une indication que le fichier est copié plutôt que déplacé ou que l’objet ne peut pas être supprimé à cet emplacement. Toutefois, tant que l’objet n’a pas reçu de [**DDWM_UPDATEWINDOW**](ddwm-updatewindow.md) message, les éléments visuels ne sont pas mis à jour. Ce format fournit le **HWND** de la fenêtre de glissement du destinataire à l’expéditeur du message de **DDWM_UPDATEWINDOW** .

Les données du presse-papiers sont de type [**TYMED_HGLOBAL**](/windows/win32/api/objidl/ne-objidl-tymed). Il s’agit d’une représentation **DWORD** d’un **HWND**. Les données peuvent être passées à la fonction **ULongToHandle** , définie dans Basetsd. h, pour fournir un **HWND** 64 bits pour une utilisation sur Windows 64 bits.

Ce format ne nécessite pas l’inclusion de shlobj. h.

 

 
