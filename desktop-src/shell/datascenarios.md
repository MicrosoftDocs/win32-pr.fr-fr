---
description: Ce document présente les scénarios courants de transfert de données de Shell et explique comment les implémenter dans votre application.
ms.assetid: 7fce555c-a93d-4414-9119-7ae9acdd4d89
title: Gestion des scénarios de transfert de données de Shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50c834768a22ad48a3cc85ec33e79bb1acafb37f0e52537f4be33daee4337a5a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057799"
---
# <a name="handling-shell-data-transfer-scenarios"></a>Gestion des scénarios de transfert de données de Shell

Le document d' [objet de données Shell](dataobject.md) a abordé l’approche générale utilisée pour transférer des données de Shell avec glisser-déplacer ou le presse-papiers. Toutefois, pour implémenter le transfert de données de Shell dans votre application, vous devez également comprendre comment appliquer ces principes généraux et techniques à différents moyens de transférer les données de l’interpréteur de commandes. Ce document présente les scénarios courants de transfert de données de Shell et explique comment les implémenter dans votre application.

-   [Instructions générales](#general-guidelines)
-   [Copie de noms de fichier du presse-papiers vers une application](#copying-file-names-from-the-clipboard-to-an-application)
    -   [Extraction des noms de fichiers de l’objet de données](#extracting-the-file-names-from-the-data-object)
-   [Copie du contenu d’un fichier déplacé dans une application](#copying-the-contents-of-a-dropped-file-into-an-application)
    -   [Utilisation du \_ format CFSTR FILECONTENTS pour extraire des données d’un fichier](/windows)
-   [Gestion des opérations de déplacement optimisées](#handling-optimized-move-operations)
-   [Gestion des opérations de suppression sur le collage](#handling-delete-on-paste-operations)
-   [Transfert de données vers et à partir de dossiers virtuels](#transfering-data-to-and-from-virtual-folders)
    -   [Acceptation de données à partir d’un dossier virtuel](#accepting-data-from-a-virtual-folder)
    -   [Transfert de données vers et à partir d’une extension d’espace de noms](#transferring-data-to-and-from-a-namespace-extension)
-   [Suppression de fichiers dans la corbeille](#dropping-files-on-the-recycle-bin)
-   [Création et importation de fichiers bribes](#creating-and-importing-scrap-files)
    -   [Prise en charge des allers-retours](#round-trip-support)
    -   [Formats de données mis en cache](#cached-data-formats)
    -   [Rendu différé](#delayed-rendering)
-   [Glisser-déplacer des objets Shell de manière asynchrone](#dragging-and-dropping-shell-objects-asynchronously)
    -   [Utilisation de IASyncOperation/IDataObjectAsyncCapability](#using-iasyncoperationidataobjectasynccapability)

> [!Note]  
> Bien que chacun de ces scénarios traite d’une opération de transfert de données spécifique, un grand nombre d’entre eux s’appliquent à un large éventail de scénarios associés. Par exemple, la principale différence entre le presse-papiers et les transferts par glisser-déplacer réside dans la façon dont l’objet de données arrive à la cible. Une fois que la cible a un pointeur vers l’interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) de l’objet de données, les procédures d’extraction d’informations sont en grande partie les mêmes pour les deux types de transfert de données. Toutefois, certains scénarios sont limités à un type d’opération spécifique. Pour plus d’informations, reportez-vous au scénario individuel.

 

## <a name="general-guidelines"></a>Instructions générales

Chacune des sections suivantes décrit un scénario de transfert de données unique et relativement spécifique. Toutefois, les transferts de données sont souvent plus complexes et peuvent impliquer des aspects de plusieurs scénarios. En général, vous ne savez pas, à l’avance, le scénario que vous devrez gérer. Voici quelques recommandations générales à prendre en compte.

Pour les sources de données :

-   Les formats du presse-papiers de l’interpréteur de commandes, à l’exception de [CF \_ HDROP](clipboard.md), ne sont pas prédéfinis. Chaque format que vous souhaitez utiliser doit être inscrit en appelant [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata).
-   Les formats dans les objets de données sont fournis dans l’ordre de préférence à partir de la source. Énumérez l’objet de données et choisissez le premier que vous pouvez consommer.
-   Incluez autant de formats que vous pouvez en prendre en charge. En général, vous ne savez pas où l’objet de données sera supprimé. Cette pratique améliore les chances que l’objet de données contienne un format que la cible de déplacement peut accepter.
-   Les fichiers existants doivent être fournis avec le format [CF \_ HDROP](clipboard.md) .
-   Offrez des données de type fichier avec des formats [CFSTR \_ FILECONTENTS](clipboard.md) / [CFSTR \_ FILEDESCRIPTOR](clipboard.md) . Cette approche permet à la cible de créer un fichier à partir d’un objet de données sans avoir besoin de connaître le stockage de données sous-jacent. Normalement, vous devez présenter les données sous la forme d’une interface [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) . Ce mécanisme de transfert de données est plus souple qu’un objet de mémoire globale et utilise moins de mémoire.
-   Les sources de glissement doivent offrir le format [CFSTR \_ SHELLIDLIST](clipboard.md) lorsque vous faites glisser des éléments de Shell. Les objets de données pour les éléments peuvent être obtenus via les méthodes [**IShellFolder :: GetUIObjectOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof) ou [**IShellItem :: BindToHandler**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler) . Les sources de données peuvent créer une implémentation d’objet de données standard qui prend en charge le format [CFSTR \_ SHELLIDLIST](clipboard.md) à l’aide de [**SHCreateDataObject**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedataobject).
-   Les cibles de dépôt qui souhaitent avoir un motif sur les éléments glissés à l’aide du modèle de programmation d’élément de Shell peuvent convertir un IDataObject en [**IShellItemArray**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray) à l’aide de [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject).
-   Utilisez des curseurs de commentaires standard.
-   Prenez en charge le déplacement vers la gauche et vers la droite.
-   Utilisez l’objet de données lui-même à partir d’un objet incorporé. Cette approche permet à votre application de récupérer tous les formats supplémentaires que l’objet de données doit offrir et évite de créer une couche supplémentaire de relation contenant-contenu. Par exemple, un objet incorporé du serveur A est glissé à partir du serveur/conteneur B et déposé sur le conteneur C. C doit créer un objet incorporé du serveur A, et non un objet incorporé du serveur B contenant un objet incorporé du serveur A.
-   N’oubliez pas que l’interpréteur de commandes peut utiliser des opérations de déplacement ou [de suppression](#handling-delete-on-paste-operations) en déplacement [optimisées](#handling-optimized-move-operations) lors du déplacement de fichiers. Votre application doit être en mesure de reconnaître ces opérations et de répondre de manière appropriée.

Pour les cibles de données :

-   Les formats du presse-papiers de l’interpréteur de commandes, à l’exception de [CF \_ HDROP](clipboard.md), ne sont pas prédéfinis. Chaque format que vous souhaitez utiliser doit être inscrit en appelant [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata).
-   Implémenter et inscrire une cible de dépôt OLE. évitez d’utiliser Windows cibles 3,1 ou le message [**WM \_ DROPFILES**](wm-dropfiles.md) , si possible.
-   Les formats contenus dans un objet de données varient selon l’origine de l’objet. Étant donné que vous ne connaissez pas à l’avance l’origine d’un objet de données, ne supposez pas qu’un format particulier sera présent. L’objet de données doit énumérer les formats par ordre de qualité, en commençant par le meilleur. Ainsi, pour obtenir le meilleur format disponible, les applications énumèrent normalement les formats disponibles et utilisent le premier format de l’énumération qu’elles peuvent prendre en charge.
-   Prenez en charge le glisser-déplacer. Vous pouvez personnaliser le menu contextuel du glissement en créant un [Gestionnaire de glisser-déplacer](context-menu-handlers.md).
-   Si votre application accepte des fichiers existants, elle doit être en mesure de gérer le format [CF \_ HDROP](clipboard.md) .
-   En général, les applications qui acceptent des fichiers doivent également gérer les formats [CFSTR \_ FILECONTENTS](clipboard.md) / [CFSTR \_ FILEDESCRIPTOR](clipboard.md) . Tandis que les fichiers du système de fichiers ont le format [CF \_ HDROP](clipboard.md) , les fichiers des fournisseurs comme les extensions d’espace de noms utilisent généralement [CFSTR \_ FILECONTENTS](clipboard.md) / [CFSTR \_ FILEDESCRIPTOR](clipboard.md). exemples : dossiers Windows CE, dossiers protocole FTP (FTP), dossiers web et dossiers CAB. La source implémente normalement une interface [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) pour présenter les données de son stockage sous la forme d’un fichier.
-   N’oubliez pas que l’interpréteur de commandes peut utiliser des opérations de déplacement ou [de suppression](#handling-delete-on-paste-operations) en déplacement [optimisées](#handling-optimized-move-operations) lors du déplacement de fichiers. Votre application doit être en mesure de reconnaître ces opérations et de répondre de manière appropriée.

## <a name="copying-file-names-from-the-clipboard-to-an-application"></a>Copie de noms de fichier du presse-papiers vers une application

**Scénario :** un utilisateur sélectionne un ou plusieurs fichiers dans Windows Explorer et les copie dans le presse-papiers. Votre application extrait les noms de fichiers et les colle dans le document.

Ce scénario peut être utilisé, par exemple, pour permettre à un utilisateur de créer un lien HTML en coupant et collant le fichier dans votre application. Votre application peut ensuite extraire le nom de fichier de l’objet de données et la traiter pour créer une balise d’ancrage.

quand un utilisateur sélectionne un fichier dans Windows Explorer et le copie dans le presse-papiers, l’interpréteur de commandes crée un objet de données. Il appelle ensuite [**OleSetClipboard**](/windows/win32/api/ole2/nf-ole2-olesetclipboard) pour placer un pointeur vers l’interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) de l’objet de données dans le presse-papiers.

Lorsque l’utilisateur sélectionne la commande **coller** dans le menu ou la barre d’outils de votre application :

1.  Appelez [**OleGetClipboard**](/windows/win32/api/ole2/nf-ole2-olegetclipboard) pour récupérer l’interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) de l’objet de données.
2.  Appelez [**IDataObject :: EnumFormatEtc**](/windows/win32/api/objidl/nf-objidl-idataobject-enumformatetc) pour demander un objet énumérateur.
3.  Utilisez l’interface [**IEnumFORMATETC**](/windows/win32/api/objidl/nn-objidl-ienumformatetc) de l’objet Enumerator pour énumérer les formats contenus dans l’objet de données.

> [!Note]  
> Les deux dernières étapes de cette procédure sont incluses par exhaustivité. Ils ne sont généralement pas nécessaires pour les transferts de fichiers simples. Tous les objets de données utilisés pour ce type de transfert de données doivent contenir le format [CF \_ HDROP](clipboard.md) , qui peut être utilisé pour déterminer les noms des fichiers contenus dans l’objet. Toutefois, pour les transferts de données plus généraux, vous devez énumérer les formats et sélectionner le meilleur que votre application peut gérer.

 

### <a name="extracting-the-file-names-from-the-data-object"></a>Extraction des noms de fichiers de l’objet de données

L’étape suivante consiste à extraire un ou plusieurs noms de fichiers de l’objet de données et à les coller dans votre application. Notez que la procédure décrite dans cette section pour l’extraction d’un nom de fichier à partir d’un objet de données s’applique également aux transferts par glisser-déplacer.

Le moyen le plus simple de récupérer des noms de fichiers à partir d’un objet de données est le format [CF \_ HDROP](clipboard.md) :

1.  Appelez [**IDataObject :: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata). Définissez le membre **cfFormat** de la structure [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) sur [CF \_ HDROP](clipboard.md) et le membre **TYMED** sur [TYMED \_ HGLOBAL](dataobject.md). Le membre **dwAspect** est normalement défini sur le \_ contenu DVASPECT. Toutefois, si le chemin d’accès au fichier est au format short (8,3), définissez **dwAspect** sur DVASPECT \_ short.

    Lorsque [**IDataObject :: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) retourne, le membre **hGlobal** de la structure [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) pointe vers un objet mémoire global qui contient les données.

2.  Créez une variable HDROP et affectez-lui le membre **hGlobal** de la structure [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) . La variable HDROP est désormais un handle vers une structure [**DROPFILES**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropfiles) suivie d’une chaîne double se terminant par un caractère NULL contenant les chemins d’accès complets des fichiers copiés.
3.  Déterminez le nombre de chemins d’accès aux fichiers figurant dans la liste en appelant [**DragQueryFile**](/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea) avec le paramètre *iFile* défini sur 0xFFFFFFFF. La fonction retourne le nombre de chemins d’accès de fichiers dans la liste. L’index de base zéro du chemin d’accès de fichier de cette liste est utilisé à l’étape suivante pour identifier un chemin d’accès particulier.
4.  Extrayez les chemins d’accès de fichier de l’objet de mémoire globale en appelant [**DragQueryFile**](/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea) une fois pour chaque fichier, avec *iFile* défini sur l’index du fichier.
5.  Traitez les chemins d’accès des fichiers en fonction des besoins et collez-les dans votre application.
6.  Appelez [**ReleaseStgMedium**](/windows/win32/api/ole2/nf-ole2-releasestgmedium) et transmettez le pointeur vers la structure [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que vous avez passée à [**IDataObject :: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) à l’étape 1. Une fois que vous avez libéré la structure, la valeur HDROP que vous avez créée à l’étape 2 n’est plus valide et ne doit pas être utilisée.

## <a name="copying-the-contents-of-a-dropped-file-into-an-application"></a>Copie du contenu d’un fichier déplacé dans une application

**Scénario :** un utilisateur fait glisser un ou plusieurs fichiers à partir de Windows Explorer et les dépose dans la fenêtre de votre application. Votre application extrait le contenu du ou des fichiers et les colle dans l’application.

ce scénario utilise le glisser-déplacer pour transférer les fichiers de Windows Explorer vers l’application. Avant l’opération, votre application doit :

1.  Appelez [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata) pour enregistrer les formats de presse-papiers Shell nécessaires.
2.  Appelez [**RegisterDragDrop**](/windows/win32/api/ole2/nf-ole2-registerdragdrop) pour inscrire une fenêtre cible et l’interface [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) de votre application.

Une fois que l’utilisateur a lancé l’opération en sélectionnant un ou plusieurs fichiers et en commençant à les faire glisser :

1.  Windows L’Explorateur crée un objet de données et y charge les formats pris en charge.
2.  Windows L’Explorateur appelle [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) pour initier la boucle de glissement.
3.  Lorsque l’image de glissement atteint votre fenêtre cible, le système vous avertit en appelant [**IDropTarget ::D ragenter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter).
4.  Pour déterminer ce que contient l’objet de données, appelez la méthode [**IDataObject :: EnumFormatEtc**](/windows/win32/api/objidl/nf-objidl-idataobject-enumformatetc) de l’objet de données. Utilisez l’objet énumérateur retourné par la méthode pour énumérer les formats contenus dans l’objet de données. Si votre application ne souhaite pas accepter l’un de ces formats, retournez DROPEFFECT \_ None. Dans le cadre de ce scénario, votre application doit ignorer tous les objets de données qui ne contiennent pas de formats utilisés pour transférer des fichiers, tels que [CF \_ HDROP](clipboard.md).
5.  Lorsque l’utilisateur supprime les données, le système appelle [**IDropTarget ::D ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop).
6.  Utilisez l’interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) pour extraire le contenu des fichiers.

Il existe différentes façons d’extraire le contenu d’un objet Shell d’un objet de données. En général, utilisez l’ordre suivant :

-   Si le fichier contient un format de [ \_ texte CF](clipboard.md) , les données sont du texte ANSI. Vous pouvez utiliser le \_ format de texte CF pour extraire les données au lieu d’ouvrir le fichier lui-même.
-   Si le fichier contient un objet OLE lié ou incorporé, l’objet de données contient un \_ format CF EMBEDDEDOBJECT. Utilisez les techniques OLE standard pour extraire les données. Les [fichiers bribes](#creating-and-importing-scrap-files) contiennent toujours un \_ format CF EMBEDDEDOBJECT.
-   Si l’objet Shell provient du système de fichiers, l’objet de données contient un format [CF \_ HDROP](clipboard.md) avec les noms des fichiers. Extrayez le nom de fichier de [CF \_ HDROP](clipboard.md) et appelez [**OleCreateFromFile**](/windows/win32/api/ole2/nf-ole2-olecreatefromfile) pour créer un nouvel objet lié ou incorporé. Pour plus d’informations sur la récupération d’un nom de fichier à partir d’un format [CF \_ HDROP](clipboard.md) , consultez [copie de noms de fichiers à partir du presse-papiers vers une application](#copying-file-names-from-the-clipboard-to-an-application).
-   Si l’objet de données contient un format [CFSTR \_ FILEDESCRIPTOR](clipboard.md) , vous pouvez extraire le contenu d’un fichier à partir du format [CFSTR \_ FILECONTENTS](clipboard.md) du fichier. Pour plus d’informations sur cette procédure, consultez [utilisation du \_ format CFSTR FILECONTENTS pour extraire des données d’un fichier](/windows).
-   Avant la [version 4,71](versions.md)de Shell, une application indiquait qu’elle transférait un type de fichier de raccourci en définissant **FD \_ LINKUI** dans le membre **dwFlags** de la structure [**FILEDESCRIPTOR**](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora) . Pour les versions ultérieures de l’interpréteur de commandes, la meilleure façon d’indiquer que les raccourcis sont transférés consiste à utiliser le format [CFSTR \_ PREFERREDDROPEFFECT](clipboard.md) défini sur le \_ lien DROPEFFECT. Cette approche est bien plus efficace que l’extraction de la structure **FILEDESCRIPTOR** uniquement pour vérifier un indicateur.

Si le processus d’extraction de données est long, vous souhaiterez peut-être effectuer l’opération de façon asynchrone sur un thread d’arrière-plan. Votre thread principal peut alors continuer sans délai inutile. Pour plus d’informations sur la gestion de l’extraction asynchrone des données, consultez [glisser-déplacer des objets Shell de manière asynchrone](#dragging-and-dropping-shell-objects-asynchronously).

### <a name="using-the-cfstr_filecontents-format-to-extract-data-from-a-file"></a>Utilisation du \_ format CFSTR FILECONTENTS pour extraire des données d’un fichier

Le format [CFSTR \_ FILECONTENTS](clipboard.md) offre un moyen très flexible et puissant de transférer le contenu d’un fichier. Il n’est même pas nécessaire de stocker les données en tant que fichier unique. Tout ce qui est requis pour ce format est que l’objet de données présente les données à la cible comme s’il s’agissait d’un fichier. Par exemple, les données réelles peuvent être une section d’un document texte ou un bloc de données extraites d’une base de données. La cible peut traiter les données en tant que fichier et n’a pas besoin de savoir quoi que ce soit sur le mécanisme de stockage sous-jacent.

Les extensions d’espace de noms utilisent normalement [CFSTR \_ FILECONTENTS](clipboard.md) pour transférer des données, car ce format ne prend pas en compte un mécanisme de stockage particulier. Une extension d’espace de noms peut utiliser n’importe quel mécanisme de stockage pratique et utiliser ce format pour présenter ses objets aux applications comme s’il s’agissait de fichiers.

Le mécanisme de transfert de données pour [CFSTR \_ FILECONTENTS](clipboard.md) est normalement [TYMED \_ ISTREAM](dataobject.md). Le transfert d’un pointeur d’interface [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) nécessite une quantité de mémoire inférieure à celle du chargement des données dans un objet de mémoire globale, et **IStream** est un moyen plus simple de représenter des données que [**IStorage**](/windows/win32/api/objidl/nn-objidl-istorage).

Un format [CFSTR \_ FILECONTENTS](clipboard.md) est toujours accompagné d’un format [CFSTR \_ FILEDESCRIPTOR](clipboard.md) . Vous devez d’abord examiner le contenu de ce format. Si plusieurs fichiers sont en cours de transfert, l’objet de données contient en fait plusieurs formats [CFSTR \_ FILECONTENTS](clipboard.md) , un pour chaque fichier. Le format [CFSTR \_ FILEDESCRIPTOR](clipboard.md) contient le nom et les attributs de chaque fichier et fournit une valeur d’index pour chaque fichier nécessaire pour extraire le format [CFSTR \_ FILECONTENTS](clipboard.md) d’un fichier particulier.

Pour extraire un format [CFSTR \_ FILECONTENTS](clipboard.md) :

1.  Extrayez le format [CFSTR \_ FILEDESCRIPTOR](clipboard.md) en tant que valeur de [ \_ HGLOBAL TYMED](dataobject.md) .
2.  Le membre **hGlobal** de la structure [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) retournée pointe vers un objet mémoire global. Verrouillez cet objet en passant la valeur **hGlobal** à [**GlobalLock**](/windows/win32/api/winbase/nf-winbase-globallock).
3.  Cast du pointeur retourné par [**GlobalLock**](/windows/win32/api/winbase/nf-winbase-globallock) en pointeur [**FILEGROUPDESCRIPTOR**](/windows/win32/api/shlobj_core/ns-shlobj_core-filegroupdescriptora) . Il pointe vers une structure **FILEGROUPDESCRIPTOR** suivie d’une ou de plusieurs structures [**FILEDESCRIPTOR**](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora) . Chaque structure **FILEDESCRIPTOR** contient une description d’un fichier qui est contenu dans l’un des formats [CFSTR \_ FILECONTENTS](clipboard.md) associés.
4.  Examinez les structures [**FILEDESCRIPTOR**](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora) pour déterminer celle qui correspond au fichier que vous souhaitez extraire. L’index de base zéro de cette structure **FILEDESCRIPTOR** est utilisé pour identifier le format [CFSTR \_ FILECONTENTS](clipboard.md) du fichier. Étant donné que la taille d’un bloc de mémoire globale n’est pas précise en octets, utilisez les membres **nFileSizeLow** et **nFileSizeHigh** de la structure pour déterminer le nombre d’octets représentant le fichier dans l’objet mémoire globale.
5.  Appelez [**IDataObject :: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) avec le membre **cfFormat** de la structure [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) défini sur la valeur [CFSTR \_ FILECONTENTS](clipboard.md) et le membre **Lindex** défini sur l’index que vous avez déterminé à l’étape précédente. Le membre **TYMED** est généralement défini sur [TYMED \_ HGLOBAL](dataobject.md) \| TYMED \_ ISTREAM \| TYMED \_ ISTORAGE. L’objet de données peut ensuite choisir son mécanisme de transfert de données par défaut.
6.  La structure [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que [**IDataObject :: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) retourne contient un pointeur vers les données du fichier. Examinez le membre **TYMED** de la structure pour déterminer le mécanisme de transfert de données.
7.  Si **TYMED** a la valeur [TYMED \_ ISTREAM](dataobject.md) ou TYMED \_ ISTORAGE, utilisez l’interface pour extraire les données. Si **TYMED** a la valeur TYMED \_ HGLOBAL, les données sont contenues dans un objet mémoire global. Pour plus d’informations sur l’extraction de données à partir d’un objet mémoire global, consultez la section *extraction d’un objet mémoire global d’un* objet de données [Shell](dataobject.md).
8.  Appelez [**GlobalLock**](/windows/win32/api/winbase/nf-winbase-globallock) pour déverrouiller l’objet mémoire global que vous avez verrouillé à l’étape 2.

## <a name="handling-optimized-move-operations"></a>Gestion des opérations de déplacement optimisées

**Scénario :** Un fichier est déplacé du système de fichiers vers une extension d’espace de noms à l’aide d’un déplacement optimisé.

Dans une opération de déplacement classique, la cible effectue une copie des données et la source supprime l’original. Cette procédure peut être inefficace car elle nécessite deux copies des données. Avec les objets volumineux tels que les bases de données, une opération de déplacement classique peut même ne pas être pratique.

Avec un déplacement optimisé, la cible utilise la compréhension de la façon dont les données sont stockées pour gérer l’ensemble de l’opération de déplacement. Il n’y a jamais de deuxième copie des données, et il n’est pas nécessaire que la source supprime les données d’origine. Les données de l’interpréteur de commandes sont parfaitement adaptées aux déplacements optimisés, car la cible peut gérer l’ensemble de l’opération à l’aide de l’API Shell. Un exemple classique consiste à déplacer des fichiers. Une fois que la cible a le chemin d’un fichier à déplacer, elle peut utiliser [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) pour la déplacer. La source ne doit pas nécessairement supprimer le fichier d’origine.

> [!Note]  
> L’interpréteur de commandes utilise normalement un déplacement optimisé pour déplacer des fichiers. Pour gérer correctement le transfert de données de Shell, votre application doit être en capacité de détecter et de gérer un déplacement optimisé.

 

Les déplacements optimisés sont traités de la manière suivante :

1.  La source appelle [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) avec le paramètre *DWEFFECT* défini sur DROPEFFECT \_ Move pour indiquer que les objets sources peuvent être déplacés.
2.  La cible reçoit la \_ valeur de déplacement DROPEFFECT via l’une de ses méthodes [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) , ce qui indique qu’un déplacement est autorisé.
3.  La cible copie l’objet (déplacement non optimisé) ou déplace l’objet (déplacement optimisé).
4.  La cible indique ensuite à la source s’il doit supprimer les données d’origine.

    Un déplacement optimisé est l’opération par défaut, avec les données supprimées par la cible. Pour informer la source qu’un déplacement optimisé a été effectué :

    -   -   La cible définit la valeur *pdwEffect* qu’elle a reçue par le biais de sa méthode [**IDropTarget ::D ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) sur une valeur autre que DROPEFFECT \_ Move. Elle est généralement définie sur DROPEFFECT \_ None ou DROPEFFECT \_ Copy. La valeur sera retournée à la source par [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop).
        -   La cible appelle également la méthode [**IDataObject :: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) de l’objet de données et la transmet à un identificateur de format [CFSTR \_ PERFORMEDDROPEFFECT](clipboard.md) défini sur DROPEFFECT \_ None. Cet appel de méthode est nécessaire, car certaines cibles de déplacement peuvent ne pas définir correctement le paramètre *pdwEffect* de [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) . Le format [CFSTR \_ PERFORMEDDROPEFFECT](clipboard.md) est la méthode fiable pour indiquer qu’un déplacement optimisé a eu lieu.

    Si la cible a été déplacée de manière non optimisée, les données doivent être supprimées par la source. Pour informer la source qu’un déplacement non optimisé a été effectué :

    -   -   La cible définit la valeur *pdwEffect* qu’elle a reçue par le biais de sa méthode [**IDropTarget ::D ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) pour DROPEFFECT \_ Move. La valeur sera retournée à la source par [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop).
        -   La cible appelle également la méthode [**IDataObject :: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) de l’objet de données et la transmet à un identificateur de format [CFSTR \_ PERFORMEDDROPEFFECT](clipboard.md) défini sur DROPEFFECT \_ Move. Cet appel de méthode est nécessaire, car certaines cibles de déplacement peuvent ne pas définir correctement le paramètre *pdwEffect* de [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) . Le format [CFSTR \_ PERFORMEDDROPEFFECT](clipboard.md) est la méthode fiable pour indiquer qu’un déplacement non optimisé a eu lieu.

5.  La source inspecte les deux valeurs qui peuvent être retournées par la cible. Si les deux sont définis sur DROPEFFECT Move, le déplacement n’est pas \_ optimisé en supprimant les données d’origine. Dans le cas contraire, la cible faisait un déplacement optimisé et les données d’origine ont été supprimées.

## <a name="handling-delete-on-paste-operations"></a>Gestion des opérations de suppression sur le collage

**Scénario :** un ou plusieurs fichiers sont coupés à partir d’un dossier dans Windows Explorer et collés dans une extension d’espace de noms. Windows L’Explorateur laisse les fichiers en surbrillance jusqu’à ce qu’il reçoive des commentaires sur le résultat de l’opération de collage.

Traditionnellement, lorsqu’un utilisateur coupe des données, il disparaît immédiatement de l’affichage. Cela peut ne pas être efficace et peut entraîner des problèmes d’utilisation si l’utilisateur s’inquiète de ce qui est arrivé aux données. Une autre approche consiste à utiliser une opération de suppression sur collage.

Avec une opération de suppression sur collage, les données sélectionnées ne sont pas immédiatement supprimées de la vue. Au lieu de cela, l’application source la marque comme étant sélectionnée, peut-être en modifiant la police ou la couleur d’arrière-plan. Une fois que l’application cible a collé les données, elle notifie la source du résultat de l’opération. Si la cible a effectué un [déplacement optimisé](#handling-optimized-move-operations), la source peut simplement mettre à jour son affichage. Si la cible a effectué un déplacement normal, la source doit également supprimer sa copie des données. Si le collage échoue, l’application source restaure les données sélectionnées à leur apparence d’origine.

> [!Note]  
> L’interpréteur de commandes utilise normalement delete-on-Paste lorsqu’une opération couper/coller est utilisée pour déplacer des fichiers. Les opérations de suppression sur le collage avec des objets Shell utilisent normalement un [déplacement optimisé](#handling-optimized-move-operations) pour déplacer les fichiers. Pour gérer correctement le transfert de données de Shell, votre application doit être en capacité de détecter et de gérer les opérations de suppression sur collage.

 

La condition essentielle pour la suppression sur le collage est que la cible doit signaler le résultat de l’opération à la source. Toutefois, les techniques du presse-papiers standard ne peuvent pas être utilisées pour implémenter delete-on-Paste, car elles ne permettent pas à la cible de communiquer avec la source. Au lieu de cela, l’application cible utilise la méthode [**IDataObject :: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) de l’objet de données pour signaler le résultat à l’objet de données. L’objet de données peut ensuite communiquer avec la source par le biais d’une interface privée.

La procédure de base pour une opération de suppression sur le collage est la suivante :

1.  La source marque l’affichage de l’écran des données sélectionnées.
2.  La source crée un objet de données. Elle indique une opération de coupe en ajoutant le format [CFSTR \_ PREFERREDDROPEFFECT](clipboard.md) avec la valeur de données DROPEFFECT \_ Move.
3.  La source place l’objet de données dans le presse-papiers à l’aide de [**OleSetClipboard**](/windows/win32/api/ole2/nf-ole2-olesetclipboard).
4.  La cible récupère l’objet de données du presse-papiers à l’aide de [**OleGetClipboard**](/windows/win32/api/ole2/nf-ole2-olegetclipboard).
5.  La cible extrait les données [CFSTR \_ PREFERREDDROPEFFECT](clipboard.md) . S’il est défini sur DROPEFFECT \_ Move, la cible peut soit effectuer un déplacement optimisé, soit simplement copier les données.
6.  Si la cible n’effectue pas de déplacement optimisé, elle appelle la méthode [**IDataObject :: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) avec le format [CFSTR \_ PERFORMEDDROPEFFECT](clipboard.md) défini sur DROPEFFECT \_ Move.
7.  Une fois le collage terminé, la cible appelle la méthode [**IDataObject :: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) avec le format [CFSTR \_ PASTESUCCEEDED](clipboard.md) défini sur DROPEFFECT \_ Move.
8.  Lorsque la méthode [**IDataObject :: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) de la source est appelée avec le format [CFSTR \_ PASTESUCCEEDED](clipboard.md) défini sur DROPEFFECT \_ Move, elle doit vérifier si elle a également reçu le [format \_ PERFORMEDDROPEFFECT CFSTR](clipboard.md) défini sur DROPEFFECT \_ Move. Si les deux formats sont envoyés par la cible, la source devra supprimer les données. Si seul le format [CFSTR \_ PASTESUCCEEDED](clipboard.md) est reçu, la source peut simplement supprimer les données de son affichage. Si le transfert échoue, la source met à jour l’affichage à son apparence d’origine.

## <a name="transfering-data-to-and-from-virtual-folders"></a>Transfert de données vers et à partir de dossiers virtuels

**Scénario :** Un utilisateur fait glisser un objet à partir de ou le supprime dans un dossier virtuel.

Les dossiers virtuels contiennent des objets qui ne font généralement pas partie du système de fichiers. Certains dossiers virtuels, tels que la corbeille, peuvent représenter des données stockées sur le disque dur, mais pas en tant qu’objets de système de fichiers ordinaires. Certains peuvent représenter des données stockées qui se trouvent sur un système distant, tel qu’un ordinateur de poche, ou un site FTP. D’autres, tels que le dossier Imprimantes, contiennent des objets qui ne représentent pas du tout des données stockées. Bien que certains dossiers virtuels fassent partie du système, les développeurs peuvent également créer et installer des dossiers virtuels personnalisés en implémentant une extension d’espace de noms.

Quel que soit le type de données ou la manière dont il est stocké, les objets de dossier et de fichier contenus dans un dossier virtuel sont présentés par le Shell comme s’il s’agissait de fichiers et de dossiers normaux. Il incombe au dossier virtuel de prendre toutes les données qu’il contient et de le présenter correctement à l’interpréteur de commandes. Cette exigence signifie que les dossiers virtuels prennent normalement en charge le glisser-déplacer et les transferts de données du presse-papiers.

Il y a donc deux groupes de développeurs qui doivent se préoccuper du transfert de données vers et à partir de dossiers virtuels :

-   Les développeurs dont les applications ont besoin d’accepter des données transférées à partir d’un dossier virtuel.
-   Les développeurs dont les extensions d’espace de noms doivent prendre en charge le transfert de données.

### <a name="accepting-data-from-a-virtual-folder"></a>Acceptation de données à partir d’un dossier virtuel

Les dossiers virtuels peuvent représenter pratiquement n’importe quel type de données et peuvent stocker ces données de la manière qu’ils choisissent. Certains dossiers virtuels peuvent en fait contenir des fichiers et dossiers de système de fichiers normaux. D’autres peuvent, par exemple, empaqueter tous leurs objets dans un document ou une base de données unique.

Lorsqu’un objet de système de fichiers est transféré à une application, l’objet de données contient normalement un format [CF \_ HDROP](clipboard.md) avec le chemin d’accès complet de l’objet. Votre application peut extraire cette chaîne et utiliser les fonctions normales du système de fichiers pour ouvrir le fichier et extraire ses données. Toutefois, étant donné que les dossiers virtuels ne contiennent généralement pas d’objets de système de fichiers normaux, ils n’utilisent généralement pas [CF \_ HDROP](clipboard.md).

Au lieu de [CF \_ HDROP](clipboard.md), les données sont normalement transférées à partir de dossiers virtuels avec les formats [CFSTR \_ FILEDESCRIPTOR](clipboard.md) / [CFSTR \_ FILECONTENTS](clipboard.md) . Le format [CFSTR \_ FILECONTENTS](clipboard.md) présente deux avantages par rapport à [CF \_ HDROP](clipboard.md):

-   Aucune méthode particulière n’est utilisée pour le stockage des données.
-   Le format est plus souple. Il prend en charge trois mécanismes de transfert de données : un objet de mémoire globale, une interface [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) ou une interface [**IStorage**](/windows/win32/api/objidl/nn-objidl-istorage) .

Les objets mémoire globaux sont rarement utilisés pour transférer des données vers ou depuis des objets virtuels, car les données doivent être copiées en mémoire dans leur intégralité. Le transfert d’un pointeur d’interface ne nécessite pratiquement aucune mémoire et est beaucoup plus efficace. Avec des fichiers très volumineux, un pointeur d’interface peut être le seul mécanisme pratique de transfert de données. En général, les données sont représentées par un pointeur [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) , car cette interface est un peu plus flexible que [**IStorage**](/windows/win32/api/objidl/nn-objidl-istorage). La cible extrait le pointeur de l’objet de données et utilise les méthodes d’interface pour extraire les données.

Pour plus d’informations sur la gestion des formats [CFSTR \_ FILEDESCRIPTOR](clipboard.md) / [CFSTR \_ filecontents](clipboard.md) , consultez [utilisation du \_ format CFSTR filecontents pour extraire des données d’un fichier](/windows).

### <a name="transferring-data-to-and-from-a-namespace-extension"></a>Transfert de données vers et à partir d’une extension d’espace de noms

Lorsque vous implémentez une extension d’espace de noms, vous devez normalement prendre en charge les fonctionnalités de glisser-déplacer. Suivez les recommandations relatives aux sources de dépôt et aux cibles présentées dans [instructions générales](#general-guidelines). En particulier, une extension d’espace de noms doit :

-   Être en mesure de gérer les formats [CFSTR \_ FILEDESCRIPTOR](clipboard.md) / [CFSTR \_ FILECONTENTS](clipboard.md) . Ces deux formats sont généralement utilisés pour transférer des objets vers et à partir d’extensions d’espace de noms.
-   Pouvoir gérer les [déplacements optimisés](#handling-optimized-move-operations). L’interpréteur de commandes s’attend à ce que les objets Shell soient déplacés avec un déplacement optimisé.
-   Pouvoir gérer une opération [de suppression sur collage](#handling-delete-on-paste-operations) . L’interpréteur de commandes utilise l’opération de suppression sur collage lorsque des objets sont déplacés de l’interpréteur de commandes à l’aide d’une opération couper/coller.
-   Pouvoir gérer le transfert de données via une interface [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) ou [**IStorage**](/windows/win32/api/objidl/nn-objidl-istorage) . Le transfert de données vers ou à partir d’un dossier virtuel est normalement géré par le transfert de l’un de ces deux pointeurs d’interface, généralement un pointeur **IStream** . La cible appelle ensuite les méthodes d’interface pour extraire les données :
    -   -   En tant que source de déplacement, l’extension de l’espace de noms doit extraire les données du stockage et les transmettre à la cible via cette interface.
        -   En tant que cible de déplacement, une extension d’espace de noms doit accepter les données provenant d’une source via cette interface et les stocker correctement.

## <a name="dropping-files-on-the-recycle-bin"></a>Suppression de fichiers dans la corbeille

**Scénario :** L’utilisateur dépose un fichier dans la **Corbeille**. Votre application ou extension d’espace de noms supprime le fichier d’origine.

La corbeille est un dossier virtuel qui est utilisé comme référentiel pour les fichiers qui ne sont plus nécessaires. Tant que la Corbeille n’a pas été vidée, l’utilisateur peut récupérer ultérieurement le fichier et le renvoyer au système de fichiers.

Dans la plupart des cas, le transfert d’objets Shell à la corbeille fonctionne comme n’importe quel autre dossier. Toutefois, lorsqu’un utilisateur dépose un fichier sur la **Corbeille**, la source doit supprimer l’original, même si les commentaires du dossier indiquent une opération de copie. Normalement, une source de déplacement n’a aucun moyen de savoir dans quel dossier son objet de données a été déposé. toutefois, pour les systèmes Windows 2000 et versions ultérieures, lorsqu’un objet de données est déposé sur la **corbeille**, l’interpréteur de commandes appelle la méthode [**IDataObject :: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) de l’objet de données avec un format [CFSTR \_ TARGETCLSID](clipboard.md) défini sur l’identificateur de classe (clsid) de la corbeille (clsid \_ RecycleBin). Pour gérer correctement le cas de la corbeille, votre objet de données doit être en mesure de reconnaître ce format et de communiquer les informations à la source par le biais d’une interface privée.

> [!Note]  
> Quand [**IDataObject :: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) est appelé avec un format [CFSTR \_ TARGETCLSID](clipboard.md) défini sur CLSID \_ RecycleBin, la source de données doit fermer tous les descripteurs ouverts aux objets qui sont transférés avant de retourner à partir de la méthode. Dans le cas contraire, vous risquez de créer des violations de partage.

 

## <a name="creating-and-importing-scrap-files"></a>Création et importation de fichiers bribes

**Scénario :** un utilisateur fait glisser des données à partir d’un fichier de données de l’application OLE et le dépose sur le bureau ou l’explorateur de Windows.

Windows permet aux utilisateurs de faire glisser un objet à partir d’un fichier de données d’une application OLE et de le déposer sur le bureau ou sur un dossier du système de fichiers. Cette opération crée un *fichier bribe*, qui contient les données ou un lien vers les données. Le nom de fichier est extrait du nom abrégé inscrit pour le CLSID de l’objet et des données de [ \_ texte CF](clipboard.md) . Pour que l’interpréteur de commandes crée un fichier bribe contenant des données, l’interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) de l’application doit prendre en charge le \_ format de presse-papiers CF EMBEDSOURCE. Pour créer un fichier contenant un lien, **IDataObject** doit prendre en charge le \_ format CF LINKSOURCE.

Il existe également trois fonctionnalités facultatives qu’une application peut implémenter pour prendre en charge les fichiers bribes :

-   Prise en charge des allers-retours
-   Formats de données mis en cache
-   Rendu différé

### <a name="round-trip-support"></a>Prise en charge des allers-retours

Un aller- *retour* implique le transfert d’un objet de données vers un autre conteneur, puis vers le document d’origine. Par exemple, un utilisateur peut transférer un groupe de cellules d’une feuille de calcul vers le bureau, en créant un fichier bribe contenant les données. Si l’utilisateur transfère ensuite le rebut à la feuille de calcul, les données doivent être intégrées dans le document tel qu’il était avant le transfert d’origine.

Lorsque l’interpréteur de commandes crée le fichier bribe, il représente les données sous la forme d’un objet incorporé. Lorsque le rebut est transféré vers un autre conteneur, il est transféré en tant qu’objet incorporé, même s’il est retourné au document d’origine. Votre application est chargée de déterminer le format de données contenu dans le rebut et de replacer les données dans son format natif, si nécessaire.

Pour définir le format de l’objet incorporé, déterminez son CLSID en extrayant le format CF OBJECTDESCRIPTOR de l’objet \_ . Si le CLSID indique un format de données qui appartient à l’application, il doit transférer les données natives au lieu d’appeler [**OleCreateFromData**](/windows/win32/api/ole2/nf-ole2-olecreatefromdata).

### <a name="cached-data-formats"></a>Formats de données mis en cache

Lorsque l’interpréteur de commandes crée un fichier bribe, il vérifie la liste des formats disponibles dans le registre. Par défaut, deux formats sont disponibles : CF \_ EMBEDSOURCE et CF \_ LINKSOURCE. Toutefois, il existe plusieurs scénarios dans lesquels les applications peuvent avoir besoin de fichiers bribes dans différents formats :

-   Pour autoriser le transfert de bribes vers des conteneurs non-OLE, qui ne peuvent pas accepter des formats d’objet incorporés.
-   Pour permettre aux suites d’applications de communiquer avec un format privé.
-   Pour faciliter le traitement des allers-retours.

Les applications peuvent ajouter des formats au rebut en les mettant en cache dans le registre. Il existe deux types de formats mis en cache :

-   Formats de cache de priorité. Pour ces formats, les données sont copiées dans leur intégralité dans le rebut à partir de l’objet de données.
-   Formats avec rendu différé. Pour ces formats, l’objet de données n’est pas copié dans le rebut. Au lieu de cela, le rendu est retardé jusqu’à ce qu’une cible demande les données. Le rendu différé est abordé plus en détail dans la section suivante.

Pour ajouter un format de cache prioritaire ou de rendu différé, créez une sous-clé **DataFormat** sous la clé **CLSID** de l’application qui est la source des données. Sous cette sous-clé, créez une sous-clé **PriorityCacheFormats** ou **DelayRenderFormats** . Pour chaque format de cache prioritaire ou de rendu différé, créez une sous-clé numérotée commençant par zéro. Définissez la valeur de cette clé sur une chaîne avec le nom enregistré du format ou une \# valeur x, où X représente le numéro de format d’un format de presse-papiers standard.

L’exemple suivant montre des formats mis en cache pour deux applications. L’application MyProg1 a le format de texte enrichi comme format de cache de priorité et un format privé « mon format » comme format de rendu différé. L’application MyProg2 a le \_ format de bitmap CF ( \# 8 ") comme format de cache de priorité.

```
HKEY_CLASSES_ROOT
   CLSID
      {GUID}
         (Default) = MyProg1
         DataFormats
            PriorityCacheFormats
               0
                  (Default) = Rich Text Format
            DelayRenderFormats
               0
                  (Default) = My Format
      {GUID}
         (Default) = MyProg2
         DataFormats
            PriorityCacheFormats
               0
                  (Default) = #8
```

Vous pouvez ajouter des formats supplémentaires en créant des sous-clés numérotées supplémentaires.

### <a name="delayed-rendering"></a>Rendu différé

Un format de rendu différé permet à une application de créer un fichier bribe, mais retarder le coût de rendu des données jusqu’à ce qu’elles soient demandées par une cible. L’interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) d’un rebut offre des formats de rendu différés à la cible, ainsi que des données natives et mises en cache. Si la cible demande un format de rendu retardé, le Shell exécute l’application et fournit les données à la cible à partir de l’objet actif.

> [!Note]  
> Étant donné que le rendu différé est un peu risqué, il doit être utilisé avec précaution. Elle ne fonctionnera pas si le serveur n’est pas disponible ou sur des applications qui ne sont pas compatibles OLE.

 

## <a name="dragging-and-dropping-shell-objects-asynchronously"></a>Glisser-déplacer des objets Shell de manière asynchrone

**Scénario :** Un utilisateur transfère un grand bloc de données de la source vers la cible. Pour éviter de bloquer les deux applications pendant un laps de temps significatif, la cible extrait les données de manière asynchrone.

Normalement, le glisser-déplacer est une opération synchrone. En bref :

1.  La source de déplacement appelle [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) et bloque son thread principal jusqu’à ce que la fonction retourne. Le blocage du thread principal bloque normalement le traitement de l’interface utilisateur.
2.  Après l’appel de la méthode [**IDropTarget ::D ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) de la cible, la cible extrait les données de l’objet de données sur son thread principal. Cette procédure bloque normalement le traitement de l’interface utilisateur de la cible pendant la durée du processus d’extraction.
3.  Une fois que les données ont été extraites, la cible retourne l’appel d' [**IDropTarget ::D ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) , le système retourne [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop)et les deux threads peuvent continuer.

En bref, le transfert de données synchrones peut bloquer les threads principaux des deux applications pendant un laps de temps significatif. En particulier, les deux threads doivent attendre que la cible extraie les données. Pour les petites quantités de données, le temps nécessaire à l’extraction des données est faible et les transferts de données synchrones fonctionnent très bien. Toutefois, l’extraction synchrone de grandes quantités de données peut entraîner des retards de longue durée et perturber l’interface utilisateur de la cible et de la source.

L’interface [**IAsyncOperation**](/previous-versions//bb776309(v=vs.85)) / [**IDataObjectAsyncCapability**](/windows/desktop/api/Shldisp/nn-shldisp-idataobjectasynccapability) est une interface facultative qui peut être implémentée par un objet de données. Elle donne à la cible de déplacement la possibilité d’extraire des données de l’objet de données de façon asynchrone sur un thread d’arrière-plan. Une fois que l’extraction de données est transremise au thread d’arrière-plan, les threads principaux des deux applications sont libres de continuer.

### <a name="using-iasyncoperationidataobjectasynccapability"></a>Utilisation de IASyncOperation/IDataObjectAsyncCapability

> [!Note]  
> L’interface a été initialement nommée [**IAsyncOperation**](/previous-versions//bb776309(v=vs.85)), mais elle a été remplacée par la valeur [**IDataObjectAsyncCapability**](/windows/desktop/api/Shldisp/nn-shldisp-idataobjectasynccapability). Dans le cas contraire, les deux interfaces sont identiques.

 

L’objectif de [**IAsyncOperation**](/previous-versions//bb776309(v=vs.85)) / [**IDataObjectAsyncCapability**](/windows/desktop/api/Shldisp/nn-shldisp-idataobjectasynccapability) est d’autoriser la source de déplacement et la cible de dépôt à négocier si les données peuvent être extraites de façon asynchrone. La procédure suivante décrit comment la source de déplacement utilise l’interface :

1.  Créez un objet de données qui expose [**IAsyncOperation**](/previous-versions//bb776309(v=vs.85)) / [**IDataObjectAsyncCapability**](/windows/desktop/api/Shldisp/nn-shldisp-idataobjectasynccapability).
2.  Appelez [**SetAsyncMode**](/windows/desktop/api/Shldisp/nf-shldisp-idataobjectasynccapability-setasyncmode) avec *FDoOpAsync* défini sur **Variant \_ true** pour indiquer qu’une opération asynchrone est prise en charge.
3.  Après le retour de [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) , appelez [**INOPÉRATION**](/windows/desktop/api/Shldisp/nf-shldisp-idataobjectasynccapability-inoperation):
    -   En cas d’échec de l' [**opération**](/windows/desktop/api/Shldisp/nf-shldisp-idataobjectasynccapability-inoperation) ou de renvoi de la **\_ valeur false**, un transfert de données synchrone normal a eu lieu et le processus d’extraction des données est terminé. La source doit effectuer tout nettoyage requis et continuer.
    -   Si [**inaction**](/windows/desktop/api/Shldisp/nf-shldisp-idataobjectasynccapability-inoperation) retourne **la \_ valeur true**, les données sont extraites de façon asynchrone. Les opérations de nettoyage doivent être gérées par [**EndOperation**](/windows/desktop/api/Shldisp/nf-shldisp-idataobjectasynccapability-endoperation).
4.  Libère l’objet de données.
5.  Lorsque le transfert de données asynchrone est terminé, l’objet de données avertit normalement la source par le biais d’une interface privée.

La procédure suivante décrit comment la cible de déplacement utilise l’interface [**IAsyncOperation**](/previous-versions//bb776309(v=vs.85)) / [**IDataObjectAsyncCapability**](/windows/desktop/api/Shldisp/nn-shldisp-idataobjectasynccapability) pour extraire des données de façon asynchrone :

1.  Lorsque le système appelle [**IDropTarget ::D ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop), appelez [**IDataObject :: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) et demandez une interface [**IAsyncOperation**](/previous-versions//bb776309(v=vs.85)) / [**IDataObjectAsyncCapability**](/windows/desktop/api/Shldisp/nn-shldisp-idataobjectasynccapability) (IID \_ IAsyncOperation/IID \_ IDataObjectAsyncCapability) à partir de l’objet de données.
2.  Appelez [**GetAsyncMode**](/windows/desktop/api/Shldisp/nf-shldisp-idataobjectasynccapability-getasyncmode). Si la méthode retourne **la \_ valeur variant true**, l’objet de données prend en charge l’extraction de données asynchrone.
3.  Créez un thread distinct pour gérer l’extraction de données et appelez [**StartOperation**](/windows/desktop/api/Shldisp/nf-shldisp-idataobjectasynccapability-startoperation).
4.  Retournez l’appel de la fonction [**IDropTarget ::D ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) , comme vous le feriez pour une opération normale de transfert de données. [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) renverra et débloquera la source de dépôt. N’appelez pas [**IDataObject :: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) pour indiquer le résultat d’une opération de déplacement ou de suppression sur collage optimisée. Attendez que l’opération soit terminée.
5.  Extrayez les données sur le thread d’arrière-plan. Le thread principal de la cible est débloqué et gratuit pour continuer.
6.  Si le transfert de données était une opération de déplacement ou [de suppression sur collage](#handling-delete-on-paste-operations) [optimisée](#handling-optimized-move-operations) , appelez [**IDataObject :: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) pour indiquer le résultat.
7.  Informez l’objet de données que l’extraction est terminée en appelant [**EndOperation**](/windows/desktop/api/Shldisp/nf-shldisp-idataobjectasynccapability-endoperation).

 

 
