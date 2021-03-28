---
description: Les gestionnaires de menus contextuels sont également appelés gestionnaires de menus contextuels ou gestionnaires de verbes. Un gestionnaire de menu contextuel est un type de gestionnaire de type de fichier.
ms.assetid: 7FC65C6F-3798-404c-B359-2BC75D3F54E7
title: Personnalisation d’un menu contextuel à l’aide de verbes dynamiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9b24f035e84f0bde6dccde09f1ed94fefce421b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973463"
---
# <a name="customizing-a-shortcut-menu-using-dynamic-verbs"></a>Personnalisation d’un menu contextuel à l’aide de verbes dynamiques

Les gestionnaires de menus contextuels sont également appelés gestionnaires de menus contextuels ou gestionnaires de verbes. Un gestionnaire de menu contextuel est un type de gestionnaire de type de fichier.

Cette rubrique est organisée comme suit :

-   [À propos des verbes statiques et dynamiques](#about-static-and-dynamic-verbs)
-   [Fonctionnement des gestionnaires de menus contextuels avec les verbes dynamiques](#how-shortcut-menu-handlers-work-with-dynamic-verbs)
-   [Éviter les collisions dues à des noms de verbe non qualifiés](#avoiding-collisions-due-to-unqualified-verb-names)
-   [Inscription d’un gestionnaire de menu contextuel avec un verbe dynamique](#registering-a-shortcut-menu-handler-with-a-dynamic-verb)
-   [Implémentation de l’interface IContextMenu](#implementing-the-icontextmenu-interface)
    -   [IContextMenu :: GetCommandString, méthode](#icontextmenugetcommandstring-method)
    -   [IContextMenu :: commande InvokeCommand, méthode](#icontextmenuinvokecommand-method)
    -   [IContextMenu :: QueryContextMenu, méthode](#icontextmenuquerycontextmenu-method)
-   [Rubriques connexes](#related-topics)

## <a name="about-static-and-dynamic-verbs"></a>À propos des verbes statiques et dynamiques

Nous vous encourageons vivement à implémenter un menu contextuel à l’aide d’une des méthodes de verbe statiques. Nous vous recommandons de suivre les instructions fournies dans la section « personnalisation d’un menu contextuel à l’aide de verbes statiques » de [création de gestionnaires de menu contextuel](context-menu-handlers.md). Pour obtenir le comportement dynamique pour les verbes statiques dans Windows 7 et versions ultérieures, consultez « obtention du comportement dynamique pour les verbes statiques » dans [création de gestionnaires de menus contextuels](context-menu-handlers.md). Pour plus d’informations sur l’implémentation d’un verbe statique et sur les verbes dynamiques à éviter, consultez [choix d’un verbe statique ou dynamique pour votre menu contextuel](shortcut-choose-method.md).

Si vous devez étendre le menu contextuel d’un type de fichier en inscrivant un verbe dynamique pour le type de fichier, suivez les instructions fournies plus loin dans cette rubrique.

> [!Note]  
> Des considérations spéciales sont à prendre en compte pour Windows 64 bits lors de l’enregistrement de gestionnaires qui fonctionnent dans le contexte d’applications 32 bits : quand les verbes de Shell sont appelés dans le contexte d’une application 32 bits, le sous-système WOW64 redirige l’accès au système de fichiers vers certains chemins d’accès. Si votre gestionnaire. exe est stocké dans l’un de ces chemins d’accès, il n’est pas accessible dans ce contexte. Par conséquent, pour une solution de contournement, stockez votre fichier. exe dans un chemin d’accès qui n’est pas redirigé, ou stockez une version stub de votre fichier. exe qui lance la version réelle.

 

## <a name="how-shortcut-menu-handlers-work-with-dynamic-verbs"></a>Fonctionnement des gestionnaires de menus contextuels avec les verbes dynamiques

En plus de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), les gestionnaires de menus contextuels exportent les interfaces supplémentaires suivantes pour gérer la messagerie nécessaire pour implémenter les éléments de menu owner-drawn :

-   [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) (obligatoire)
-   [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) (obligatoire)
-   [**IContextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2) (facultatif)
-   [**IContextMenu3**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu3) (facultatif)

Pour plus d’informations sur les éléments de menu owner-drawn, consultez la section *creating Owner-Drawn menu items* dans [using menus](../menurc/using-menus.md).

L’interpréteur de commandes utilise l’interface [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) pour initialiser le gestionnaire. Lorsque l’interpréteur de commandes appelle [**IShellExtInit :: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), il passe un objet de données avec le nom de l’objet et un pointeur vers une liste d’identificateurs d’éléments (PIDL) du dossier qui contient le fichier. Le paramètre *hkeyProgID* est l’emplacement du Registre sous lequel le handle du menu contextuel est inscrit. La méthode **IShellExtInit :: Initialize** doit extraire le nom de fichier de l’objet de données et stocker le nom et le pointeur du dossier vers une liste d’identificateurs d’éléments (PIDL) pour une utilisation ultérieure. Pour plus d’informations sur l’initialisation du gestionnaire, consultez [implémentation de IShellExtInit](handlers.md).

Lorsque les verbes sont présentés dans un menu contextuel, ils sont d’abord découverts, puis présentés à l’utilisateur et enfin appelés. La liste suivante décrit ces trois étapes plus en détail :

1.  L’interpréteur de commandes appelle [**IContextMenu :: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu), qui retourne un jeu de verbes qui peut être basé sur l’état des éléments ou du système.
2.  Le système transmet un handle **HMENU** que la méthode peut utiliser pour ajouter des éléments au menu contextuel.
3.  Si l’utilisateur clique sur l’un des éléments du gestionnaire, le shell appelle [**IContextMenu :: commande InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand). Le gestionnaire peut ensuite exécuter la commande appropriée.

## <a name="avoiding-collisions-due-to-unqualified-verb-names"></a>Éviter les collisions dues à des noms de verbe non qualifiés

Étant donné que les verbes sont inscrits par type, le même nom de verbe peut être utilisé pour les verbes sur différents éléments. Cela permet aux applications de faire référence à des verbes communs indépendants du type d’élément. Bien que cette fonctionnalité soit utile, l’utilisation de noms non qualifiés peut entraîner des collisions entre plusieurs éditeurs de logiciels indépendants (ISV) qui choisissent le même nom de verbe. Pour éviter cela, préfixez toujours les verbes avec le nom ISV comme suit :

`ISV_Name.verb`

Utilisez toujours un ProgID spécifique à l’application. L’adoption de la Convention de mappage de l’extension de nom de fichier à un ProgID fourni par un ISV évite les collisions potentielles. Toutefois, étant donné que certains types d’éléments n’utilisent pas ce mappage, il est nécessaire de nommer les noms uniques des fournisseurs. Lorsque vous ajoutez un verbe à un ProgID existant qui peut déjà être inscrit dans ce verbe, vous devez d’abord supprimer la clé de registre de l’ancien verbe avant d’ajouter votre propre verbe. Vous devez le faire pour éviter de fusionner les informations de verbe à partir des deux verbes. Dans le cas contraire, cela entraîne un comportement imprévisible.

## <a name="registering-a-shortcut-menu-handler-with-a-dynamic-verb"></a>Inscription d’un gestionnaire de menu contextuel avec un verbe dynamique

Les gestionnaires de menus contextuels sont associés à un type de fichier ou à un dossier. Pour les types de fichiers, le gestionnaire est inscrit sous la sous-clé suivante.

```
HKEY_CLASSES_ROOT
   Program ID
      shellex
         ContextMenuHandlers
```

Pour associer un gestionnaire de menu contextuel à un type de fichier ou à un dossier, commencez par créer une sous-clé sous la sous-clé **ContextMenuHandlers** . Nommez la sous-clé du gestionnaire et définissez la valeur par défaut de la sous-clé sur la forme de chaîne du GUID de l’identificateur de classe (CLSID) du gestionnaire.

Ensuite, pour associer un gestionnaire de menu contextuel à différents genres de dossiers, inscrivez le gestionnaire de la même façon que vous le feriez pour un type de fichier, mais sous la sous-clé *FolderType* comme indiqué dans l’exemple suivant.

```
HKEY_CLASSES_ROOT
   FolderType
      shellex
         ContextMenuHandlers
```

Pour plus d’informations sur les types de dossiers pour lesquels vous pouvez enregistrer des gestionnaires, consultez [inscription des gestionnaires d’extensions de Shell](handlers.md).

Si un menu contextuel est associé à un type de fichier, double-cliquez sur un objet pour lancer normalement la commande par défaut et la méthode [**IContextMenu :: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) du gestionnaire n’est pas appelée. Pour spécifier que la méthode **IContextMenu :: QueryContextMenu** du gestionnaire doit être appelée lors d’un double-clic sur un objet, créez une sous-clé sous la sous-clé **CLSID** du gestionnaire, comme indiqué ici.

```
HKEY_CLASSES_ROOT
   CLSID
      {00000000-1111-2222-3333-444444444444}
         shellex
            MayChangeDefaultMenu
```

Quand vous double-cliquez sur un objet associé au gestionnaire, [**IContextMenu :: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) est appelé avec l’indicateur **CMF \_ DEFAULTONLY** défini dans le paramètre *uFlags* .

Les gestionnaires de menus contextuels ne doivent définir la sous-clé **MayChangeDefaultMenu** que s’ils peuvent avoir besoin de modifier le verbe par défaut du menu contextuel. La définition de cette sous-clé force le système à charger la DLL du gestionnaire lors d’un double-clic sur un élément associé. Si votre gestionnaire ne modifie pas le verbe par défaut, vous ne devez pas définir cette sous-clé, car cela amène le système à charger votre DLL inutilement.

L’exemple suivant illustre les entrées de Registre qui activent un gestionnaire de menu contextuel pour un type de fichier. MYP. La sous-clé **CLSID** du gestionnaire comprend une sous-clé **MayChangeDefaultMenu** pour garantir que le gestionnaire est appelé lorsque l’utilisateur double-clique sur un objet connexe.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {00000000-1111-2222-3333-444444444444}
         InProcServer32
            (Default) = C:\MyDir\MyCommand.dll
            ThreadingModel = Apartment
         shellex
            MayChangeDefaultMenu
   MyProgram.1
      (Default) = MyProgram Application
      shellex
         ContextMenuHandler
            MyCommand = {00000000-1111-2222-3333-444444444444}
```

## <a name="implementing-the-icontextmenu-interface"></a>Implémentation de l’interface IContextMenu

[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) est la méthode la plus simple, mais également la plus compliquée à implémenter. Nous vous recommandons vivement d’implémenter un verbe à l’aide de l’une des méthodes Verb statiques. Pour plus d’informations, consultez [choix d’un verbe statique ou dynamique pour votre menu contextuel](shortcut-choose-method.md). [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) a trois méthodes, **GetCommandString**, **commande InvokeCommand** et **QueryContextMenu**, qui sont décrites ici en détail.

### <a name="icontextmenugetcommandstring-method"></a>IContextMenu :: GetCommandString, méthode

La méthode [**IContextMenu :: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) du gestionnaire est utilisée pour retourner le nom canonique d’un verbe. Cette méthode est facultative. Dans Windows XP et les versions antérieures de Windows, lorsque l’Explorateur Windows a une barre d’État, cette méthode est utilisée pour récupérer le texte d’aide qui s’affiche dans la barre d’État pour un élément de menu.

Le paramètre *idCmd* contient le décalage de l’identificateur de la commande qui a été définie lors de l’appel de [**IContextMenu :: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) . Si une chaîne d’aide est demandée, *uFlags* est défini sur **GC \_ HELPTEXTW**. Copiez la chaîne d’aide dans la mémoire tampon *pszName* , en la convertissant en **PWSTR**. La chaîne de verbe est demandée en affectant à *uFlags* la valeur **GC \_ VERBW**. Copiez la chaîne appropriée dans *pszName*, tout comme avec la chaîne d’aide. Les indicateurs **GC \_ Validate** et **GC \_ VALIDATEW** ne sont pas utilisés par les gestionnaires de menu contextuel.

L’exemple suivant illustre une implémentation simple de [**IContextMenu :: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) qui correspond à l’exemple [**IContextMenu :: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) donné dans la section [IContextMenu :: QueryContextMenu](#icontextmenuquerycontextmenu-method) de cette rubrique. Étant donné que le gestionnaire ajoute un seul élément de menu, il n’existe qu’un seul jeu de chaînes qui peut être retourné. La méthode teste si *idCmd* est valide et, si c’est le cas, retourne la chaîne demandée.

La fonction [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya) est utilisée pour copier la chaîne demandée dans *pszName* afin de garantir que la chaîne copiée ne dépasse pas la taille de la mémoire tampon spécifiée par *cchName*. Cet exemple implémente uniquement la prise en charge des valeurs Unicode de *uFlags*, car seules celles-ci ont été utilisées dans l’Explorateur Windows depuis Windows 2000.


```C++
IFACEMETHODIMP CMenuExtension::GetCommandString(UINT idCommand, 
                                                UINT uFlags, 
                                                UINT *pReserved, 
                                                PSTR pszName, 
                                                UINT cchName)
{
    HRESULT hr = E_INVALIDARG;

    if (idCommand == IDM_DISPLAY)
    {
        switch (uFlags)
        {
            case GCS_HELPTEXTW:
                // Only useful for pre-Vista versions of Windows that 
                // have a Status bar.
                hr = StringCchCopyW(reinterpret_cast<PWSTR>(pszName), 
                                    cchName, 
                                    L"Display File Name");
                break; 

            case GCS_VERBW:
                // GCS_VERBW is an optional feature that enables a caller
                // to discover the canonical name for the verb passed in
                // through idCommand.
                hr = StringCchCopyW(reinterpret_cast<PWSTR>(pszName), 
                                    cchName, 
                                    L"DisplayFileName");
                break; 
        }
    }
    return hr;
}
```



### <a name="icontextmenuinvokecommand-method"></a>IContextMenu :: commande InvokeCommand, méthode

Cette méthode est appelée lorsqu’un utilisateur clique sur un élément de menu pour indiquer au gestionnaire d’exécuter la commande associée. Le paramètre *Pici* pointe vers une structure qui contient les informations requises.

Bien que *Pici* soit déclaré dans shlobj. h comme une structure [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) , dans la pratique, il pointe souvent vers une structure [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) . Cette structure est une version étendue de **CMINVOKECOMMANDINFO** et a plusieurs membres supplémentaires qui permettent de passer des chaînes Unicode.

Vérifiez le membre **cbSize** de *Pici* pour déterminer la structure qui a été transmise. S’il s’agit d’une structure [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) et que l’indicateur **\_ \_ Unicode de masque Cmic** est défini pour le membre **fmask** , castez *Pici* en **CMINVOKECOMMANDINFOEX**. Cela permet à votre application d’utiliser les informations Unicode contenues dans les cinq derniers membres de la structure.

Le membre **lpVerb** ou **lpVerbW** de la structure est utilisé pour identifier la commande à exécuter. Les commandes sont identifiées de l’une des deux manières suivantes :

-   Par la chaîne du verbe de la commande
-   Par le décalage de l’identificateur de la commande

Pour faire la distinction entre ces deux cas, vérifiez le mot de poids fort de **lpVerb** pour le cas ANSI ou **lpVerbW** pour la casse Unicode. Si le mot de poids fort est différent de zéro, **lpVerb** ou **lpVerbW** contient une chaîne de verbe. Si le mot de poids fort est égal à zéro, le décalage de la commande se trouve dans le mot de poids faible de **lpVerb**.

L’exemple suivant illustre une implémentation simple de [**IContextMenu :: commande InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) qui correspond aux exemples [**IContextMenu :: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) et [**IContextMenu :: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) fournis avant et après cette section. La méthode détermine d’abord la structure qui est passée. Elle détermine ensuite si la commande est identifiée par son décalage ou son verbe. Si **lpVerb** ou **lpVerbW** contient un verbe ou un offset valide, la méthode affiche une boîte de message.


```C++
STDMETHODIMP CShellExtension::InvokeCommand(LPCMINVOKECOMMANDINFO lpcmi)
{
    BOOL fEx = FALSE;
    BOOL fUnicode = FALSE;

    if(lpcmi->cbSize == sizeof(CMINVOKECOMMANDINFOEX))
    {
        fEx = TRUE;
        if((lpcmi->fMask & CMIC_MASK_UNICODE))
        {
            fUnicode = TRUE;
        }
    }

    if( !fUnicode && HIWORD(lpcmi->lpVerb))
    {
        if(StrCmpIA(lpcmi->lpVerb, m_pszVerb))
        {
            return E_FAIL;
        }
    }

    else if( fUnicode && HIWORD(((CMINVOKECOMMANDINFOEX *) lpcmi)->lpVerbW))
    {
        if(StrCmpIW(((CMINVOKECOMMANDINFOEX *)lpcmi)->lpVerbW, m_pwszVerb))
        {
            return E_FAIL;
        }
    }

    else if(LOWORD(lpcmi->lpVerb) != IDM_DISPLAY)
    {
        return E_FAIL;
    }

    else
    {
        MessageBox(lpcmi->hwnd,
                   "The File Name",
                   "File Name",
                   MB_OK|MB_ICONINFORMATION);
    }

    return S_OK;
}
```



### <a name="icontextmenuquerycontextmenu-method"></a>IContextMenu :: QueryContextMenu, méthode

L’interpréteur de commandes appelle [**IContextMenu :: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) pour permettre au gestionnaire de menu contextuel d’ajouter ses éléments de menu au menu. Il passe le handle **HMENU** dans le paramètre *HMENU* . Le paramètre *indexMenu* est défini sur l’index à utiliser pour le premier élément de menu à ajouter.

Tous les éléments de menu ajoutés par le gestionnaire doivent avoir des identificateurs qui se trouvent entre les valeurs des paramètres *idCmdFirst* et *idCmdLast* . En règle générale, le premier identificateur de commande est défini sur *idCmdFirst*, qui est incrémenté d’une unité (1) pour chaque commande supplémentaire. Cette pratique vous permet d’éviter de dépasser les *idCmdLast* et d’optimiser le nombre d’identificateurs disponibles au cas où l’interpréteur de commandes appellera plus d’un gestionnaire.

Le *décalage de commande* d’un identificateur d’élément correspond à la différence entre l’identificateur et la valeur dans *idCmdFirst*. Stockez le décalage de chaque élément que votre gestionnaire ajoute au menu contextuel, car l’interpréteur de commandes peut l’utiliser pour identifier l’élément s’il appelle ensuite [**IContextMenu :: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) ou [**IContextMenu :: commande InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).

Vous devez également affecter un [verbe](launch.md) à chaque commande que vous ajoutez. Un verbe est une chaîne qui peut être utilisée à la place de l’offset pour identifier la commande lorsque [**IContextMenu :: commande InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) est appelé. Il est également utilisé par des fonctions telles que [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) pour exécuter des commandes de menu contextuel.

Il existe trois indicateurs qui peuvent être transmis via le paramètre *uFlags* qui sont pertinents pour les gestionnaires de menus contextuels. Ils sont décrits dans le tableau suivant.



| Indicateur             | Description                                                                                                                                                                                                              |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CMF \_ DEFAULTONLY | L’utilisateur a sélectionné la commande par défaut, généralement en double-cliquant sur l’objet. [**IContextMenu :: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) doit retourner le contrôle à l’interpréteur de commandes sans modifier le menu. |
| CMF \_ NOdéfaut   | Aucun élément dans le menu ne doit être l’élément par défaut. La méthode doit ajouter ses commandes au menu.                                                                                                                          |
| CMF \_ normal      | Le menu contextuel s’affiche normalement. La méthode doit ajouter ses commandes au menu.                                                                                                                            |



 

Utilisez [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) ou [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) pour ajouter des éléments de menu à la liste. Ensuite, retournez une valeur **HRESULT** avec la gravité définie sur **gravité \_ réussite**. Définissez la valeur de code sur le décalage de l’identificateur de commande le plus grand qui a été assigné, plus un (1). Par exemple, supposons que *idCmdFirst* a la valeur 5 et que vous ajoutez trois éléments au menu avec des identificateurs de commande 5, 7 et 8. La valeur de retour doit être `MAKE_HRESULT(SEVERITY_SUCCESS, 0, 8 - 5 + 1)` .

L’exemple suivant illustre une implémentation simple de [**IContextMenu :: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) qui insère une seule commande. Le décalage de l’identificateur de la commande est l' \_ affichage IDM, qui est défini à zéro. Les variables **m \_ pszVerb** et **m \_ pwszVerb** sont des variables privées utilisées pour stocker la chaîne de verbe indépendante du langage associée à la fois dans les formats ANSI et Unicode.


```C++
#define IDM_DISPLAY 0

STDMETHODIMP CMenuExtension::QueryContextMenu(HMENU hMenu,
                                              UINT indexMenu,
                                              UINT idCmdFirst,
                                              UINT idCmdLast,
                                              UINT uFlags)
{
    HRESULT hr;
    
    if(!(CMF_DEFAULTONLY & uFlags))
    {
        InsertMenu(hMenu, 
                   indexMenu, 
                   MF_STRING | MF_BYPOSITION, 
                   idCmdFirst + IDM_DISPLAY, 
                   "&Display File Name");

    
        
        hr = StringCbCopyA(m_pszVerb, sizeof(m_pszVerb), "display");
        hr = StringCbCopyW(m_pwszVerb, sizeof(m_pwszVerb), L"display");

        return MAKE_HRESULT(SEVERITY_SUCCESS, 0, USHORT(IDM_DISPLAY + 1));
    }

    return MAKE_HRESULT(SEVERITY_SUCCESS, 0, USHORT(0));
}
```



Pour d’autres tâches d’implémentation de verbe, consultez [création de gestionnaires de menus contextuels](context-menu-handlers.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Menus contextuels (menu contextuel) et gestionnaires de menus contextuels](context-menu.md)
</dt> <dt>

[Verbes et associations de fichiers](fa-verbs.md)
</dt> <dt>

[Choix d’un verbe statique ou dynamique pour votre menu contextuel](shortcut-choose-method.md)
</dt> <dt>

[Meilleures pratiques pour les gestionnaires de menus contextuels et les verbes de sélection multiple](verbs-best-practices.md)
</dt> <dt>

[Création de gestionnaires de menu contextuel](context-menu-handlers.md)
</dt> <dt>

[Référence du menu contextuel](context-menu-reference.md)
</dt> </dl>

 

 
