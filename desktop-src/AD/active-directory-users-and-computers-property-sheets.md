---
title: Active Directory les utilisateurs et les feuilles de propriétés des ordinateurs
description: Le composant logiciel enfichable MMC utilisateurs et ordinateurs Active Directory est conçu pour afficher une feuille de propriétés pour différents objets dans un serveur Active Directory.
ms.assetid: 38032d89-9549-475c-90aa-dac5cfe11084
ms.tgt_platform: multiple
keywords:
- Active Directory les feuilles de propriétés des utilisateurs et ordinateurs Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ea24f34e86f21af178e975852accb667bb69e4
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724668"
---
# <a name="active-directory-users-and-computers-property-sheets"></a>Active Directory les utilisateurs et les feuilles de propriétés des ordinateurs

Le composant logiciel enfichable MMC utilisateurs et ordinateurs Active Directory est conçu pour afficher une feuille de propriétés pour différents objets dans un serveur Active Directory. La feuille de propriétés contient une ou plusieurs pages utilisées pour afficher et modifier les données de l’objet. Différents types d’objets ont des ensembles de pages différents affichés pour eux. Le composant logiciel enfichable MMC Active Directory les utilisateurs et les ordinateurs permet également aux fournisseurs tiers d’ajouter des pages personnalisées à la feuille de propriétés pour un type d’objet spécifique. Pour plus d’informations, consultez [pages de propriétés à utiliser avec les spécificateurs d’affichage](property-pages-for-use-with-display-specifiers.md).

Certaines applications, autres que le composant logiciel enfichable MMC utilisateurs et ordinateurs Active Directory, doivent fournir à l’utilisateur la possibilité d’afficher et de modifier les attributs d’un objet dans un serveur Active Directory. L’application peut implémenter ses propres feuilles de propriétés, mais il est préférable d’offrir une interface utilisateur cohérente pour réduire la confusion et l’apprentissage du temps. Heureusement, le composant logiciel enfichable MMC Active Directory utilisateurs et ordinateurs permet à n’importe quelle application OLE COM d’afficher une feuille de propriétés pour un objet qui est identique à la feuille de propriétés qui serait affichée par le composant logiciel enfichable MMC utilisateurs et ordinateurs Active Directory pour le même objet.

Pour plus d’informations et pour obtenir un exemple de code qui héberge un Active Directory feuille de propriétés utilisateurs et ordinateurs, consultez l’exemple PropSheetHost dans le kit de développement logiciel (SDK) de la plateforme.

## <a name="developer-audience"></a>Public de développeurs

Cette documentation suppose que le lecteur est familiarisé avec l’opération COM et le développement de composants à l’aide de C++. Actuellement, il n’est pas possible de créer une extension de feuille de propriétés Active Directory à l’aide de Visual Basic.

## <a name="hosting-an-active-directory-users-and-computers-property-sheet"></a>Page de propriétés hébergement d’un Active Directory d’utilisateurs et d’ordinateurs

**Pour afficher une feuille de propriétés pour un objet dans un serveur Active Directory**

1.  Créer une fenêtre qui peut être utilisée pour traiter des messages. Il peut s’agir d’une fenêtre existante ou d’une fenêtre à usage spécial. C’est ce que l’on appelle la *fenêtre masquée*.
2.  Créez un objet OLE COM dérivé de [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject). Cet objet de données doit prendre en charge les formats de données suivants :

    -   [**CFSTR \_ DSOBJECTNAMES**](cfstr-dsobjectnames.md) ce format de données contient un [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) qui identifie l’objet auquel s’applique la feuille de propriétés. Lors de l’hébergement d’une feuille de propriétés, les membres les plus significatifs de la structure **DSOBJECTNAMES** sont affichés dans la liste suivante.

        **clsidNamespace** Réservé. Définissez cette valeur sur un GUID pour votre application dans le cas où elle sera utilisée à l’avenir.
        
        **aObjects** Contient un tableau de structures [**DSBOJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) . Chaque structure **DSBOJECT** représente un objet d’annuaire unique. Le membre **CItems** contient le nombre d’éléments dans le tableau. Seul le premier objet de ce tableau est utilisé. Les autres objets sont ignorés.

    -   [**CFSTR \_ DSDISPLAYSPECOPTIONS**](cfstr-ds-display-spec-options.md) ce format de données contient une structure [**DSDISPLAYSPECOPTIONS**](/windows/desktop/api/Dsclient/ns-dsclient-dsdisplayspecoptions) qui contient les données qui seront utilisées par les pages de propriétés, telles que l’emplacement de chargement des pages de propriétés, le serveur et les informations d’identification à utiliser, etc. Les membres les plus significatifs du **DSDISPLAYSPECOPTIONS** sont affichés dans la liste suivante.

        **offsetAttribPrefix** La chaîne de préfixe d’attribut détermine l’emplacement de la liste des pages de propriétés. Il doit contenir l’une des chaînes suivantes.

        

        | Chaîne de préfixe d’attribut | Description                                              |
        |-------------------------|----------------------------------------------------------------------------------------------------------------------|
        | « admin »<br/>      | Les pages de propriétés sont chargées à partir de l’attribut [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages) .<br/> |
        | Shell<br/>      | Les pages de propriétés sont chargées à partir de l’attribut [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages) .<br/> |

        


    -   [**CFSTR \_ DS \_ PROPSHEETCONFIG**](cfstr-ds-propsheetconfig.md) ce format de données contient une structure [**PROPSHEETCFG**](propsheetcfg.md) qui contient les données de l’hôte de feuille de propriétés. Lors de l’hébergement d’une feuille de propriétés, les membres les plus significatifs de la structure **PROPSHEETCFG** contiennent les données affichées dans la liste suivante.

        **lNotifyHandle** Doit être égal à zéro.
        **hwndParentSheet**  Contient le handle de la fenêtre qui reçoit les messages de [**\_ modification de \_ notification \_ WM ADSPROP**](wm-adsprop-notify-change.md) quand une partie de l’une des pages change et est appliquée. Peut avoir la **valeur null** si ce message n’est pas souhaité.

        **hwndHidden** Contient le descripteur de la fenêtre pour recevoir les messages de notification de la feuille de calcul de la feuille de calcul [**WM \_ DSA \_ \_ \_**](wm-dsa-sheet-create-notify.md) et [**WM \_ DSA \_ \_ \_**](wm-dsa-sheet-close-notify.md) . Définissez cette valeur sur le handle de votre fenêtre masquée.

        **wParamSheetClose** Contient un identificateur défini par l’application qui est retourné dans *wParam* dans le message de fermeture de la feuille de calcul [**WM \_ DSA \_ \_ \_**](wm-dsa-sheet-close-notify.md) . Si ce membre est égal à zéro, le message de fermeture de la **\_ \_ feuille \_ \_ DSA DSA** n’est pas publié dans la fenêtre masquée.


3.  Créez une instance de l' [**objet \_ DsPropertyPages CLSID**](guids-of-user-interface-elements.md) et obtenez l’interface [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) pour l’objet. Il est également possible de dupliquer le comportement de l’objet **CLSID \_ DsPropertyPages** . Pour plus d’informations, consultez duplication du comportement de l' \_ objet CLSID DsPropertyPages.
4.  Initialisez l’objet [**CLSID \_ DsPropertyPages**](guids-of-user-interface-elements.md) en appelant la méthode [**IShellExtInit :: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) . Les paramètres *pidlFolder* et *hkeyProgID* ne sont pas utilisés dans cette méthode. Le paramètre *pdtobj* est le pointeur vers l’objet de données créé à l’étape 2. Quand la méthode **IShellExtInit :: Initialize** est appelée, l’objet **CLSID \_ DsPropertyPages** enregistre une référence à l’objet de données.
5.  Obtenez l’interface [**IShellPropSheetExt**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) pour l’objet [**CLSID \_ DsPropertyPages**](guids-of-user-interface-elements.md) et appelez la méthode [**IShellPropSheetExt :: AddPages**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) . Le paramètre *lpfnAddPage* est l’adresse d’une fonction de rappel que vous devez implémenter. Le format de cette fonction est illustré ci-dessous. Si la fonction de rappel est déclarée en tant que membre d’une classe C++, la fonction de rappel doit être déclarée comme **static**. Le paramètre *lParam* est une valeur définie par l’application qui peut être utilisée pour identifier l’objet qui implémente la fonction de rappel. Quand la méthode **IShellPropSheetExt :: AddPages** est appelée, l’objet **CLSID \_ DsPropertyPages** obtient les données de l’objet de données et énumère les pages de propriétés inscrites pour les spécificateurs d’affichage de l’objet. L’objet **CLSID \_ DsPropertyPages** énumère ensuite les objets page de propriétés, en appelant la méthode **IShellPropSheetExt :: AddPages** de chaque objet.

    ```C++
    BOOL CALLBACK AddPagesCallback(HPROPSHEETPAGE, LPARAM)
    ```

    

6.  Chaque page ajoutée par les objets page de propriétés entraînera l’appel de votre fonction de rappel avec le handle vers la page de propriétés et la valeur définie par l’application. Votre fonction de rappel doit stocker chaque descripteur de page de propriétés qui est passé. Lorsque la méthode [**IShellPropSheetExt :: AddPages**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) de l’objet [**CLSID \_ DsPropertyPages**](guids-of-user-interface-elements.md) est retournée, toutes les pages ont été ajoutées via votre fonction de rappel.
7.  Remplissez une structure [**PROPSHEETHEADER**](/windows/win32/api/prsht/ns-prsht-propsheetheadera_v2) pour afficher la feuille de propriétés. Le membre **phpage** reçoit un pointeur vers un tableau de handles de page qui ont été collectés par votre fonction de rappel. Le membre **nPages** reçoit le nombre de pages dans le tableau de handles de page.
8.  Affichez la feuille de propriétés en appelant la fonction [**feuille**](/windows/win32/api/prsht/nf-prsht-propertysheeta) .

Si les données de n’importe quelle page sont modifiées et que l’utilisateur clique sur les boutons **OK** ou **appliquer** , la fenêtre identifiée par le membre **hwndParentSheet** de la structure [**PROPSHEETCFG**](propsheetcfg.md) reçoit un message de [**notification de \_ \_ \_ modification WM ADSPROP**](wm-adsprop-notify-change.md) . Ce message est strictement une notification et ne nécessite aucune action spécifique.

Lorsque la page est fermée, la fenêtre identifiée par le membre **hwndHidden** de la structure [**PROPSHEETCFG**](propsheetcfg.md) reçoit un message de fermeture de la feuille de calcul [**WM \_ \_ \_ \_ DSA**](wm-dsa-sheet-close-notify.md) . Ce message est strictement une notification et ne nécessite pas l’exécution d’une action spécifique.

Dans certains cas, les feuilles de propriétés existantes doivent afficher une feuille de propriétés secondaire. Par exemple, si vous affichez la feuille de propriétés d’un objet utilisateur et que vous sélectionnez la page **membre de** , une liste des groupes dont l’utilisateur est membre s’affiche. Si vous double-cliquez sur l’un de ces groupes dans la liste, la feuille de propriétés de ce groupe s’affiche. La feuille de propriétés principale n’affiche pas la feuille secondaire seule. Elle demande à l’hôte d’afficher la feuille secondaire en envoyant un message de notification de création de la feuille de données [**WM \_ DSA \_ \_ \_**](wm-dsa-sheet-create-notify.md) à la fenêtre identifiée par le membre **hwndHidden** de la structure [**PROPSHEETCFG**](propsheetcfg.md) . Le *wParam* de la **\_ feuille DSA \_ DSA \_ créer \_** un message Notify est un pointeur vers une structure d' [**\_ informations de \_ page \_ DSA sec**](dsa-sec-page-info.md) qui contient des informations sur la feuille de propriétés secondaire et l’objet qu’elle représente. En réponse à ce message, l’hôte de feuille de propriétés doit afficher la feuille de propriétés secondaire de la même manière que celle présentée ci-dessus. Après le traitement du message de notification de création de la **\_ \_ feuille \_ \_ DSA DSA** , le récepteur du message doit libérer la structure des informations de la **\_ \_ page \_ DSA sec** en passant la valeur *wParam* à la fonction [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) .

## <a name="duplicating-the-behavior-of-the-clsid_dspropertypages-object"></a>Duplication du comportement de l' \_ objet DSPROPERTYPAGES CLSID

**Pour dupliquer le comportement de l' \_ objet CLSID DsPropertyPages**

1.  Énumérez les valeurs de l’attribut [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages) ou [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages) pour le spécificateur d’affichage pour la classe d’objet. Chaque valeur est une chaîne qui contient un nombre, suivi d’une virgule, suivi de la représentation sous forme de chaîne de l’identificateur de classe de l’extension de la page de propriétés. Pour plus d’informations sur le format des valeurs du spécificateur d’affichage des pages de propriétés, consultez [inscription de l’objet com de la page de propriétés dans un spécificateur d’affichage](registering-the-property-page-com-object-in-a-display-specifier.md).
2.  Convertissez chaque chaîne d’identificateur de classe en **CLSID** à l’aide de la fonction [**CLSIDFromString**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) .
3.  Triez les identificateurs de classe d’extension par le nombre qui précède chaque chaîne d’identificateur de classe dans la valeur de l’attribut. Si deux nombres sont identiques, triez les identificateurs de classe dans l’ordre dans lequel les valeurs d’attribut sont obtenues à partir du serveur de Active Directory.
4.  Énumérez les identificateurs de classe d’extension, en créant une instance de chaque extension.
5.  Pour chaque extension, dans l’ordre indiqué ci-dessus, appelez [**IShellExtInit :: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) de l’extension à l’aide des mêmes informations que celles décrites à l’étape 4 de la procédure de la feuille de propriétés hébergement d’un Active Directory utilisateurs et ordinateurs.
6.  Pour chaque extension, dans l’ordre indiqué ci-dessus, appelez [**IShellPropSheetExt :: AddPages**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) de l’extension avec les mêmes informations que celles décrites à l’étape 5 de la procédure de la feuille de propriétés hébergement d’un Active Directory utilisateurs et ordinateurs.

Si possible, utilisez l’objet [**CLSID \_ DsPropertyPages**](guids-of-user-interface-elements.md) pour créer les pages au lieu de le faire manuellement. Le **\_ DsPropertyPages CLSID** a été optimisé et gère correctement les cas d’échec, par exemple quand aucun spécificateur d’affichage n’est disponible pour les paramètres régionaux actuels. En outre, l’objet **CLSID \_ DsPropertyPages** peut changer à l’avenir, ce qui signifie que vos feuilles de propriétés peuvent ne pas correspondre exactement à celles affichées par le composant logiciel enfichable MMC Active Directory utilisateurs et ordinateurs.

## <a name="special-programming-elements"></a>Éléments de programmation spéciaux

Actuellement, les éléments de programmation suivants ne sont pas définis dans un fichier d’en-tête publié. Pour utiliser ces éléments, vous devez les définir vous-même dans le format exact affiché dans la page de référence particulière.

-   [**CFSTR \_ DS \_ PROPSHEETCONFIG**](cfstr-ds-propsheetconfig.md)
-   [**PROPSHEETCFG**](propsheetcfg.md)
-   [**notification de fermeture de la \_ feuille du DSA WM \_ \_ \_**](wm-dsa-sheet-close-notify.md)
-   [**créer une notification de la \_ feuille DSA DSA \_ \_ \_**](wm-dsa-sheet-create-notify.md)
-   [**\_ \_ informations sur la page DSA sec \_**](dsa-sec-page-info.md)

## <a name="example-code"></a>Exemple de code

L’exemple de code C++ suivant montre un moyen sûr de définir ces éléments qui continueront de fonctionner même si ces éléments sont définis dans un fichier d’en-tête publié à l’avenir.


```C++
#ifndef CFSTR_DS_PROPSHEETCONFIG
    #define CFSTR_DS_PROPSHEETCONFIG_W L"DsPropSheetCfgClipFormat"
    #define CFSTR_DS_PROPSHEETCONFIG_A "DsPropSheetCfgClipFormat"

    #ifdef UNICODE
        #define CFSTR_DS_PROPSHEETCONFIG CFSTR_DS_PROPSHEETCONFIG_W
    #else
        #define CFSTR_DS_PROPSHEETCONFIG CFSTR_DS_PROPSHEETCONFIG_A
    #endif //UNICODE
#endif //CFSTR_DS_PROPSHEETCONFIG


#ifndef WM_ADSPROP_SHEET_CREATE
    #define WM_ADSPROP_SHEET_CREATE (WM_USER + 1108)
#endif


#ifndef WM_DSA_SHEET_CREATE_NOTIFY
    #define WM_DSA_SHEET_CREATE_NOTIFY (WM_USER + 6)
#endif


#ifndef WM_DSA_SHEET_CLOSE_NOTIFY
    #define WM_DSA_SHEET_CLOSE_NOTIFY (WM_USER + 5) 
#endif


#ifndef DSA_SEC_PAGE_INFO
    typedef struct _DSA_SEC_PAGE_INFO
    {
        HWND    hwndParentSheet;
        DWORD   offsetTitle;
        DSOBJECTNAMES dsObjectNames;
    } DSA_SEC_PAGE_INFO, *PDSA_SEC_PAGE_INFO;
#endif //DSA_SEC_PAGE_INFO

#ifndef PROPSHEETCFG
    typedef struct _PROPSHEETCFG
    {  
        LONG_PTR lNotifyHandle;  
        HWND hwndParentSheet;  
        HWND hwndHidden;  
        WPARAM wParamSheetClose;
    } PROPSHEETCFG, *PPROPSHEETCFG;
#endif //PROPSHEETCFG
```



 

