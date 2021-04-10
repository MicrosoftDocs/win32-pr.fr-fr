---
title: Raccourcis Internet
description: L’objet raccourci Internet est utilisé pour créer des raccourcis de bureau sur des sites Internet.
ms.assetid: 367c003f-2362-408c-81e1-fda1ffc7e15b
keywords:
- Objets de raccourci Internet
- Contrôles WebBrowser
- IPropertySetStorage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f14bc2ed58f75522e59b9008ded7b0f1416a21fe
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031205"
---
# <a name="internet-shortcuts"></a>Raccourcis Internet

L’objet raccourci Internet est utilisé pour créer des raccourcis de bureau sur des sites Internet. Comme les raccourcis vers les éléments du système de fichiers, les raccourcis Internet prennent la forme d’une icône sur le bureau. Lorsque l’utilisateur clique sur l’icône, le navigateur est lancé et affiche le site associé au raccourci.

Les rubriques suivantes sont présentées.

-   [Création de raccourcis Internet](#creating-internet-shortcuts)
    -   [Création d’un raccourci Internet à partir d’un contrôle WebBrowser](#creating-an-internet-shortcut-from-a-webbrowser-control)
    -   [Création d’un raccourci Internet à partir d’une URL](#creating-an-internet-shortcut-from-a-url)
-   [Accès au stockage des propriétés](#accessing-property-storage)
-   [Interfaces](#interfaces)
    -   [interfaces OLE](#ole-interfaces)
    -   [Interfaces Shell](#shell-interfaces)
-   [Fonctions](#functions)
    -   [Fonctions de l’utilitaire de raccourci Internet](#internet-shortcut-utility-functions)

## <a name="creating-internet-shortcuts"></a>Création de raccourcis Internet

Vous pouvez créer un raccourci Internet à l’aide d’un contrôle WebBrowser ou de l’URL de la page.

### <a name="creating-an-internet-shortcut-from-a-webbrowser-control"></a>Création d’un raccourci Internet à partir d’un contrôle WebBrowser

Si votre application héberge un contrôle WebBrowser, vous pouvez utiliser l’objet raccourci Internet pour créer des raccourcis de la façon suivante.

1.  Créez une instance de l’objet raccourci Internet avec [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), à l’aide d’un identificateur de classe (CLSID) du CLSID \_ InternetShortcut.
2.  Transmettez le pointeur à l’interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) du WebBrowser à l’objet raccourci Internet avec [IObjectWithSite :: SetSite](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite).
3.  Appelez la méthode [IPersistFile :: Save](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) de l’objet de raccourci Internet lorsque vous souhaitez créer un raccourci vers la page affichée par le contrôle WebBrowser.

Un raccourci sera créé à l’emplacement spécifié dans [IPersistFile :: Save](/windows/win32/api/objidl/nf-objidl-ipersistfile-save). Cet emplacement permet au contrôle WebBrowser de restaurer son état, ce qui comprend la tâche de chargement des documents corrects dans les jeux de frames.

### <a name="creating-an-internet-shortcut-from-a-url"></a>Création d’un raccourci Internet à partir d’une URL

Vous pouvez également créer un raccourci Internet si vous avez l’URL de la page à laquelle vous souhaitez établir un lien.

1.  Créez une instance de l’objet raccourci Internet avec [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), à l’aide d’un CLSID de CLSID \_ InternetShortcut.
2.  Utilisez la méthode [IUniformResourceLocator :: setURL](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/dd565676(v=vs.85)) pour définir l’URL dans le raccourci.
3.  Utilisez la méthode [IPersistFile :: Save](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) pour enregistrer le fichier de raccourci à l’emplacement souhaité.

## <a name="accessing-property-storage"></a>Accès au stockage des propriétés

L’objet raccourci Internet contient plusieurs propriétés auxquelles vous pouvez accéder par le biais de l’interface [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) de l’objet à l’aide de la procédure suivante.

1.  Pour accéder à l’interface [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) , appelez [QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) avec IID \_ IPropertySetStorage.
2.  Accédez au jeu de stockage des propriétés du raccourci Internet en appelant [IPropertySetStorage :: Open](/windows/win32/api/propidl/nf-propidl-ipropertysetstorage-open) avec fmtid \_ Intshcut ou fmtid \_ InternetSite pour obtenir l’interface [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) .
3.  Lisez les informations de stockage des propriétés avec [IPropertyStorage :: ReadMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) en passant l’ID de propriété approprié.

Avec la [version 4,70 ou une version ultérieure](/previous-versions/windows/desktop/legacy/bb776779(v=vs.85)) de Shell32.dll, vous pouvez également récupérer l’interface [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) en appelant [**IShellFolder :: BindToStorage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtostorage) avec le paramètre *PIDL* défini sur. Fichier URL et paramètre *riid* défini sur IID \_ IPropertySetStorage.

Les ID de propriété suivants peuvent être demandés pour FMTID \_ Intshcut.



| PROPID               | Type de variante | Description                                 |
|----------------------|--------------|---------------------------------------------|
| PID \_ est une \_ URL         | \_LPWStr VT   | URL vers laquelle le raccourci dirige             |
| PID \_ est le \_ nom        | \_LPWStr VT   | Nom du raccourci Internet               |
| le PID \_ est \_ WORKINGDIR  | \_LPWStr VT   | Répertoire de travail pour le raccourci          |
| le PID \_ est \_ Hotkey      | \_UI2 VT      | Raccourci clavier pour le raccourci                     |
| PID \_ est \_ SHOWCMD     | VT \_       | Afficher la commande pour le raccourci                   |
| le PID \_ est \_ IndexIcône   | VT \_       | Index de l’icône                           |
| le PID \_ est \_ ICONFILE    | \_LPWStr VT   | Fichier qui contient l’icône                 |
| PID \_ est \_ WHATSNEW    | \_LPWStr VT   | Texte des nouveautés                             |
| PID \_ est \_ auteur      | \_LPWStr VT   | Auteur                                      |
| PID \_ est une \_ Description | \_LPWStr VT   | Texte de description du site                    |
| PID \_ est un \_ Commentaire     | \_LPWStr VT   | Commentaire annoté par l’utilisateur                      |
| PID \_ est \_ itinérant      | VT \_ bool     | True lorsque le raccourci est itinérant pour la première fois |



 

Les ID de propriété suivants peuvent être demandés pour FMTID \_ InternetSite.



| PROPID                     | Type de variante | Description                                       |
|----------------------------|--------------|---------------------------------------------------|
| PID \_ INTSITE \_ WHATSNEW     | \_LPWStr VT   | Texte des nouveautés                                   |
| PID \_ INTSITE \_ auteur       | \_LPWStr VT   | Auteur                                            |
| PID \_ INTSITE \_ LASTVISIT    | de VT \_ fileTime | Heure de la dernière visite du site                        |
| PID \_ INTSITE \_ LASTMOD      | de VT \_ fileTime | Heure de la dernière modification du site                       |
| PID \_ INTSITE \_ VISITCOUNT   | VT \_ UI4      | Nombre de fois que l’utilisateur a visité                  |
| \_Description INTSITE \_ PID  | \_LPWStr VT   | Texte de description du site                          |
| PID \_ INTSITE, \_ Commentaire      | \_LPWStr VT   | Commentaire annoté par l’utilisateur                            |
| \_indicateurs INTSITE \_ PID        | VT \_ UI4      | Indique l’utilisation des \_ indicateurs PIDISF (voir ci-dessous)       |
| PID \_ INTSITE \_ CONTENTLEN   | N/A          | Non prise en charge pour le moment                           |
| PID \_ INTSITE \_ CONTENTCODE  | N/A          | Non prise en charge pour le moment                           |
| PID \_ INTSITE \_ recurse      | N/A          | Non prise en charge pour le moment                           |
| PID \_ INTSITE \_ Watch        | N/A          | Non prise en charge pour le moment                           |
| PID \_ INTSITE \_ subscription | \_UI8 VT      | Valeur SUBSCRIPTIONCOOKIE pour le gestionnaire d’abonnements |
| \_URL INTSITE \_ PID          | \_LPWStr VT   | URL vers laquelle le raccourci dirige                   |
| \_titre INTSITE \_ PID        | \_LPWStr VT   | Intitulé                                             |
| \_page de \_ codes PID INTSITE     | VT \_ UI4      | Page de codes du document                          |
| \_ \_ suivi des INTSITE PID     | N/A          | Non prise en charge pour le moment                           |
| PID \_ INTSITE \_ IndexIcône    | VT \_       | Index de l’icône                                 |
| PID \_ INTSITE \_ ICONFILE     | \_LPWStr VT   | Fichier qui contient l’icône                       |
| PID \_ INTSITE \_ itinérant       | VT \_ UI4      | L’entrée a été ajoutée en raison de l’itinérance                |



 

Les indicateurs de site Internet sont les suivants.



| Indicateur                    | Description                                |
|-------------------------|--------------------------------------------|
| PIDISF \_ RECENTLYCHANGED | Indique qu’un site a été modifié récemment |
| PIDISF \_ CACHEDSTICKY    | Non prise en charge pour le moment                    |
| PIDISF \_ CACHEIMAGES     | Non prise en charge pour le moment                    |
| PIDISF \_ FOLLOWALLLINKS  | Non prise en charge pour le moment                    |



 

Les valeurs suivantes sont utilisées pour l’historique d’itinérance Internet.



| Valeur du PID \_ INTSITE \_ itinérante         | Description                                                                                                                                                              |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Valeur non définie ou PIDISR \_ \_ à \_ jour | Cette entrée de cache n’a pas été modifiée par l’itinérance.                                                                                                                       |
| PIDISR \_ a besoin d' \_ Ajouter                    | Cette entrée du cache a été ajoutée au cache par itinérance. Définissez PIDISR \_ \_ à \_ jour une fois que le traitement de l’entrée est terminé.                                                   |
| PIDISR \_ a besoin d’une \_ mise à jour                 | Cette entrée de cache existait déjà sur l’ordinateur local, mais elle a été mise à jour par l’itinérance. Définissez PIDISR \_ \_ à \_ jour une fois que le traitement de l’entrée est terminé.                 |
| PIDISR \_ doit être \_ supprimé                 | L’itinérance a détecté que cette entrée de cache devait être supprimée. Par exemple, l’utilisateur a peut-être effacé l’historique de son navigateur. Supprimez l’entrée à l’aide de DeleteUrlCacheEntry. |



 

## <a name="interfaces"></a>Interfaces

L’objet raccourci Internet expose un certain nombre d’interfaces.

### <a name="ole-interfaces"></a>interfaces OLE

-   [IDataObject](/windows/win32/api/objidl/nn-objidl-idataobject)
-   [IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile)
-   [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream)
-   [IOleCommandTarget](/windows/win32/api/docobj/nn-docobj-iolecommandtarget)
-   [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage)
-   [IObjectWithSite](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite)

### <a name="shell-interfaces"></a>Interfaces Shell

-   [**IContextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2)
-   [**IExtractIcon**](/windows/desktop/api/shlobj_core/nn-shlobj_core-iextracticona)
-   [**INewShortcutHook**](/windows/desktop/api/shlobj/nn-shlobj-inewshortcuthooka)
-   [**IShellExtInit**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellextinit)
-   [**IShellLink**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinka)
-   [**IShellPropSheetExt**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext)
-   [**IQueryInfo**](/windows/desktop/api/shlobj_core/nn-shlobj_core-iqueryinfo)

## <a name="functions"></a>Fonctions

Il existe plusieurs fonctions utilitaires qui peuvent être utilisées avec l’objet raccourci Internet.

### <a name="internet-shortcut-utility-functions"></a>Fonctions de l’utilitaire de raccourci Internet

-   [**InetIsOffline**](/windows/desktop/api/intshcut/nf-intshcut-inetisoffline)
-   [**MIMEAssociationDialog**](/windows/desktop/api/intshcut/nf-intshcut-mimeassociationdialoga)
-   [**TranslateURL**](/windows/desktop/api/intshcut/nf-intshcut-translateurla)
-   [**URLAssociationDialog**](/windows/desktop/api/intshcut/nf-intshcut-urlassociationdialoga)

 

 