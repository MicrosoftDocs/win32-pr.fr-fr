---
description: IContextMenu est la plus puissante, mais également l’interface la plus compliquée à implémenter.
ms.assetid: F0C1D60E-7A5A-4609-9136-F4E535E9F6F1
title: Comment implémenter l’interface IContextMenu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f44ec65d95a4f6d67a9f15e10f5720be21c3b6c57fba5d0cf920bd12be54f662
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118223466"
---
# <a name="how-to-implement-the-icontextmenu-interface"></a>Comment implémenter l’interface IContextMenu

[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) est la plus puissante, mais également l’interface la plus compliquée à implémenter. Nous vous recommandons vivement d’implémenter un verbe à l’aide de l’une des méthodes Verb statiques. Pour plus d’informations, consultez [choix d’une méthode de menu contextuel statique ou dynamique](shortcut-choose-method.md). [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) a trois méthodes, [**GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring), [**commande InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand)et [**QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu), qui sont décrites ici en détail.

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   C++

### <a name="prerequisites"></a>Prérequis

-   Verbe statique
-   Menu contextuel

## <a name="instructions"></a>Instructions

### <a name="icontextmenugetcommandstring-method"></a>IContextMenu :: GetCommandString, méthode

La méthode [**IContextMenu :: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) du gestionnaire est utilisée pour retourner le nom canonique d’un verbe. Cette méthode est facultative. dans Windows XP et les versions antérieures de Windows, lorsque Windows Explorer possède une barre d’état, cette méthode est utilisée pour récupérer le texte d’aide qui s’affiche dans la barre d’état pour un élément de menu.

Le paramètre *idCmd* contient le décalage de l’identificateur de la commande qui a été définie lors de l’appel de [**IContextMenu :: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) . Si une chaîne d’aide est demandée, *uFlags* est défini sur **GC \_ HELPTEXTW**. Copiez la chaîne d’aide dans la mémoire tampon *pszName* , en la convertissant en **PWSTR**. La chaîne de verbe est demandée en affectant à *uFlags* la valeur **GC \_ VERBW**. Copiez la chaîne appropriée dans *pszName*, tout comme avec la chaîne d’aide. Les indicateurs **GC \_ Validate** et **GC \_ VALIDATEW** ne sont pas utilisés par les gestionnaires de menu contextuel.

L’exemple suivant illustre une implémentation simple de [**GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) qui correspond à l’exemple [**QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) fourni dans la section de la [méthode IContextMenu :: QueryContextMenu](shortcut-menu-using-dynamic-verbs.md) de cette rubrique. Étant donné que le gestionnaire ajoute un seul élément de menu, il n’existe qu’un seul jeu de chaînes qui peut être retourné. La méthode teste si *idCmd* est valide et, si c’est le cas, retourne la chaîne demandée.

La fonction [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya) est utilisée pour copier la chaîne demandée dans *pszName* afin de garantir que la chaîne copiée ne dépasse pas la taille de la mémoire tampon spécifiée par *cchName*. cet exemple implémente la prise en charge uniquement des valeurs Unicode de *uFlags*, car seules celles-ci ont été utilisées dans l’explorateur de Windows depuis Windows 2000.


```
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
                // to discover the canonical name for the verb that is passed in
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

Cette méthode est appelée lorsqu’un utilisateur clique sur un élément de menu pour indiquer au gestionnaire d’exécuter la commande associée. Le paramètre *Pici* pointe vers une structure qui contient les informations requises pour exécuter la commande.

Bien que *Pici* soit déclaré dans shlobj. h comme une structure [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) , dans la pratique, il pointe souvent vers une structure [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) . Cette structure est une version étendue de **CMINVOKECOMMANDINFO** et a plusieurs membres supplémentaires qui permettent de passer des chaînes Unicode.

Vérifiez le membre **cbSize** de *Pici* pour déterminer la structure qui a été transmise. S’il s’agit d’une structure [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) et que l’indicateur **\_ \_ Unicode de masque Cmic** est défini pour le membre **fmask** , castez *Pici* en **CMINVOKECOMMANDINFOEX**. Cela permet à votre application d’utiliser les informations Unicode contenues dans les cinq derniers membres de la structure.

Le membre **lpVerb** ou **lpVerbW** de la structure est utilisé pour identifier la commande à exécuter. Les commandes sont identifiées de l’une des deux manières suivantes :

-   Par la chaîne du verbe de la commande
-   Par le décalage de l’identificateur de la commande

Pour faire la distinction entre ces deux cas, vérifiez le mot de poids fort de **lpVerb** pour le cas ANSI ou **lpVerbW** pour la casse Unicode. Si le mot de poids fort est différent de zéro, **lpVerb** ou **lpVerbW** contient une chaîne de verbe. Si le mot de poids fort est égal à zéro, le décalage de la commande se trouve dans le mot de poids faible de **lpVerb**.

L’exemple suivant illustre une implémentation simple de [**IContextMenu :: commande InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) qui correspond aux exemples [**IContextMenu :: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) et [**IContextMenu :: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) fournis avant et après cette section. La méthode détermine d’abord la structure qui est passée. Elle détermine ensuite si la commande est identifiée par son décalage ou son verbe. Si **lpVerb** ou **lpVerbW** contient un verbe ou un offset valide, la méthode affiche une boîte de message.


```
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

Le *décalage de commande* d’un identificateur d’élément correspond à la différence entre l’identificateur et la valeur dans *idCmdFirst*. Stockez le décalage de chaque élément que votre gestionnaire ajoute au menu contextuel, car l’interpréteur de commandes peut utiliser le décalage pour identifier l’élément s’il appelle ensuite [**IContextMenu :: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) ou [**IContextMenu :: commande InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).

Vous devez également assigner un [verbe](launch.md) à chaque commande que vous ajoutez. Un verbe est une chaîne qui peut être utilisée à la place de l’offset pour identifier la commande lorsque [**commande InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) est appelé. Il est également utilisé par des fonctions telles que [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) pour exécuter des commandes de menu contextuel.

Il existe trois indicateurs qui peuvent être transmis via le paramètre *uFlags* qui sont pertinents pour les gestionnaires de menus contextuels. Ils sont décrits dans le tableau suivant.



| Indicateur             | Description                                                                                                                                                                                                              |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CMF \_ DEFAULTONLY | L’utilisateur a sélectionné la commande par défaut, généralement en double-cliquant sur l’objet. [**IContextMenu :: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) doit retourner le contrôle à l’interpréteur de commandes sans modifier le menu. |
| CMF \_ NOdéfaut   | Aucun élément dans le menu ne doit être l’élément par défaut. La méthode doit ajouter ses commandes au menu.                                                                                                                          |
| CMF \_ normal      | Le menu contextuel s’affiche normalement. La méthode doit ajouter ses commandes au menu.                                                                                                                            |



 

Utilisez [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) ou [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) pour ajouter des éléments de menu à la liste. Ensuite, retournez une valeur **HRESULT** avec la gravité définie sur gravité \_ réussite. Définissez la valeur de code sur le décalage de l’identificateur de commande le plus grand qui a été assigné, plus un (1). Par exemple, supposons que *idCmdFirst* a la valeur 5 et que vous ajoutez trois éléments au menu avec des identificateurs de commande 5, 7 et 8. La valeur de retour doit correspondre à \_ HRESULT (gravité \_ réussie, 0,8 + 1).

L’exemple suivant illustre une implémentation simple de [**QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) qui insère une seule commande. Le décalage de l’identificateur de la commande est l' \_ affichage IDM, qui est défini à zéro. Les variables **m \_ pszVerb** et **m \_ pwszVerb** sont des variables privées utilisées pour stocker la chaîne de verbe indépendante du langage associée à la fois dans les formats ANSI et Unicode.


```
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

    return MAKE_HRESULT(SEVERITY_SUCCESS, 0, USHORT(0));}
```



## <a name="remarks"></a>Remarques

Pour d’autres tâches d’implémentation de verbe, consultez [création de gestionnaires de menu contextuel](context-menu-handlers.md).

 

 
