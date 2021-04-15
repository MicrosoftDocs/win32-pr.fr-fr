---
description: Pour vous assurer que vos données sont indexées et présentées correctement à l’utilisateur pendant les recherches, vous devez implémenter des magasins de données Shell (également appelés extensions d’espace de noms de Shell) et des gestionnaires de type de fichier (également appelés extensions d’interpréteur de commandes, gestionnaires d’extension ou gestionnaires d’extension de Shell).
ms.assetid: 38cebb3c-51bf-439c-8d4e-445344f6cb66
title: Ajout d’icônes, d’aperçus et de menus contextuels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 501006227f6192b7d81a2a88ba915c368a9cc398
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525533"
---
# <a name="adding-icons-previews-and-shortcut-menus"></a>Ajout d’icônes, d’aperçus et de menus contextuels

Pour vous assurer que vos données sont indexées et présentées correctement à l’utilisateur pendant les recherches, vous devez implémenter des magasins de données Shell (également appelés [extensions d’espace de noms de Shell](../shell/nse-works.md)) et des gestionnaires de type de fichier (également appelés extensions d’interpréteur de commandes, gestionnaires d' [extension](../shell/handlers.md)ou gestionnaires d’extension de Shell).

Cette rubrique décrit les interfaces suivantes :

-   [Implémentation de gestionnaires de types de fichiers](#implementing-file-type-handlers)
    -   [IPersist](#ipersist)
    -   [IPersistFolder](#ipersistfolder)
    -   [IShellFolder](#ishellfolder)
    -   [IContextMenu](#icontextmenu)
    -   [IExtractIcon](#iextracticon)
    -   [IPreviewHandler](#ipreviewhandler)
-   [Ressources supplémentaires](#additional-resources)
-   [Rubriques connexes](#related-topics)

## <a name="implementing-file-type-handlers"></a>Implémentation de gestionnaires de types de fichiers

Ces extensions de Shell ou gestionnaires de type de fichier fournissent à vos utilisateurs les expériences d’environnement suivantes :

-   La vue résultats affiche une icône spécifique pour votre type d’élément.
-   La vue résultats affiche un aperçu de l’élément lorsque l’utilisateur sélectionne l’élément.
-   Les utilisateurs peuvent double-cliquer sur des éléments pour initier des événements tels que l’ouverture du fichier.
-   Les utilisateurs peuvent cliquer avec le bouton droit sur les éléments pour accéder à un menu contextuel (contexte).
-   Les utilisateurs peuvent glisser-déplacer des éléments.

Comme tous les objets COM (Component Object Model), les gestionnaires de types de fichiers doivent implémenter une interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) et une fabrique de classe.

Dans Windows XP ou version antérieure, les gestionnaires doivent également implémenter :

-   L' [interface IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile)
-   Ou [interface IShellExtInit](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit)

Dans Windows Vista, l’interface [IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile) et l' [interface IShellExtInit](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) ont été remplacées par les trois interfaces suivantes pour que Shell Initialise le gestionnaire :

-   [IInitializeWithStream, interface](/windows/win32/api/propsys/nn-propsys-iinitializewithstream)
-   [Interface IInitializeWithItem](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)
-   [Interface IInitializeWithFile](/windows/win32/api/propsys/nn-propsys-iinitializewithfile)

Pour fournir une expérience utilisateur raisonnable, vous devez fournir un magasin de données Shell avec votre gestionnaire de protocole. Ce magasin de données sert alors de « fabrique » pour les gestionnaires d’icônes, les gestionnaires de menus contextuels, les gestionnaires d’aperçus, etc. Les implémentations minimales de l’interface [IPersist](/windows/desktop/api/objidl/nn-objidl-ipersist) et de l' [interface IPersistFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) sont requises par l' [interface IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder), et une implémentation minimale de l’interface IShellFolder est requise pour [IContextMenu](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) et [IExtractIcon](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona).

> [!Note]  
> Le même identificateur de classe (CLSID) doit être implémenté pour **IPersist**, **IPersistFolder** et **IShellFolder**.

 

Pour plus d’informations sur la création d’un magasin de données Shell pour prendre en charge un gestionnaire de protocole, consultez [implémentation des interfaces d’objets de dossier de base](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).

### <a name="ipersist"></a>IPersist

L’interface **IPersist** définit la méthode unique **GetClassID**, conçue pour fournir le CLSID d’un objet qui peut être stocké de manière permanente dans le système.



| Méthode     | Description                                      |
|------------|--------------------------------------------------|
| GetClassID | Retourne le CLSID de l’objet de magasin de données Shell |



 

### <a name="ipersistfolder"></a>IPersistFolder

L’interface **IPersistFolder** est utilisée pour initialiser les objets de dossier de l’interpréteur de commandes. L’implémentation de cette interface, dérivée de **IPersist**, est la manière dont le dossier est indiqué à l’emplacement où il se trouve dans l’espace de noms Shell. Vous n’utilisez pas cette interface directement. Elle est utilisée par l’implémentation du système de fichiers de la [méthode IShellFolder :: BindToObject](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) lors de l’initialisation d’un objet de dossier de l’interpréteur de commandes.



| Méthode     | Description                                                                                            |
|------------|--------------------------------------------------------------------------------------------------------|
| Initialiser | Demande à un objet de dossier de Shell de s’initialiser en fonction des informations transmises et des retours \_ OK |



 

### <a name="ishellfolder"></a>IShellFolder

L’interface d' [interface IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) est utilisée pour gérer les dossiers, et une implémentation partielle est nécessaire pour que les interfaces d’icône et de contexte implémentées pour un gestionnaire de protocole se comportent correctement dans l’interface utilisateur des résultats de la recherche Windows. La plupart des fonctionnalités requises sont exposées par le biais de la méthode **GetUIObjectOf** . Cette méthode permet à un complément d’interroger les interfaces **IExtractIcon** et **IContextMenu** .

L’interface d' [interface IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) utilise PIDL à la place des URL. Contrairement aux spécifications d’un magasin de données Shell complet, les compléments peuvent utiliser une structure IDL simple qui contient uniquement l’URL.

Les méthodes suivantes de l' [interface IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) doivent être implémentées. Cinq de ces méthodes nécessitent une implémentation minimale.



| Méthode           | Description                                                                                                                                                                                                                                                                   |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BindToObject     | Retourne E \_ NOTIMPL                                                                                                                                                                                                                                                            |
| BindToStorage    | Retourne E \_ NOTIMPL                                                                                                                                                                                                                                                            |
| CreateViewObject | Retourne E \_ NOTIMPL                                                                                                                                                                                                                                                            |
| SetNameOf        | Retourne E \_ NOTIMPL                                                                                                                                                                                                                                                            |
| ParseDisplayName | Convertit une URL en structure PIDL                                                                                                                                                                                                                                          |
| CompareIDs       | Compare deux valeurs PIDL                                                                                                                                                                                                                                                      |
| GetDisplayNameOf | Retourne l’URL d’un PIDL                                                                                                                                                                                                                                                    |
| GetUIObjectOf    | Cette méthode est semblable à la [méthode IUnknown :: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)). Si une icône est demandée, l’appelant demande l’IID \_ IExtractIcon ; si un menu contextuel est demandé, l’appelant demande l’IID \_ IContextMenu |



 

**IShellFolder** n’est pas utilisé pour énumérer des dossiers. Cela signifie que le nom complet d’un dossier sera l’URL physique. Cela peut changer à l’avenir.

### <a name="icontextmenu"></a>IContextMenu

Lorsque Windows Search affiche les résultats à l’utilisateur, l’utilisateur peut cliquer avec le bouton droit sur un élément et afficher un menu contextuel défini par votre interface **IContextMenu** . Les menus contextuels sont également appelés menus contextuels.

L’action par défaut dans le menu contextuel est la même que celle effectuée lors d’un double-clic sur l’élément. Sans les interfaces **IShellFolder** ou **IContextMenu** correspondantes pour l’élément, le comportement par défaut d’un événement de double-clic consiste à transmettre l’URL en tant qu’argument à la fonction [ShellExecute](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) .

Pour plus d’informations sur la création de gestionnaires de menus contextuels et sur les [Exemples : extensions de Shell pour les gestionnaires de protocole](-search-3x-wds-ph-ui-samplecode.md) pour l’exemple de code, consultez Création de gestionnaires de [menus](../shell/context-menu-handlers.md) contextuels.

### <a name="iextracticon"></a>IExtractIcon

**IExtractIcon** récupère une icône pour l’interface utilisateur de recherche Windows en fonction de l’URL figurant dans le PIDL fourni par votre gestionnaire de protocole.

Pour plus d’informations sur la création de gestionnaires d’icône et d' [Exemples : extensions de Shell pour les gestionnaires de protocole](-search-3x-wds-ph-ui-samplecode.md) pour l’exemple de code, consultez [création de gestionnaires d’icône](../shell/how-to-create-icon-handlers.md) .

### <a name="ipreviewhandler"></a>IPreviewHandler

Le [IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) affiche un aperçu complet d’un élément sélectionné dans l’Explorateur Windows. Les versions préliminaires sont disponibles dans Windows Search 4,0 ou dans Windows Vista avec Windows Desktop Search 3. x.

Pour créer un gestionnaire d’aperçus personnalisé :

1.  Implémentez un [IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) qui prend un [IStream](/windows/win32/api/objidl/nn-objidl-istream), en suivant les instructions fournies dans les [gestionnaires d’aperçus](../shell/preview-handlers.md).
2.  Inscrire votre gestionnaire d’aperçus :

    ```
    HKEY_CLASSES_ROOT\<Your_Object_Type>
    ```

    ```
    HKEY_CLASSES_ROOT\<Your_Object_Type>\ShellEx
    ```

    ```
    HKEY_CLASSES_ROOT\<Your_Object_Type>\ShellEx\{8895b1c6-b41f-4c1c-a562-0d564250836f}
       @ = {<Your_PreviewHandler_GUID>}
    ```

3.  Effectuez les deux étapes suivantes pour implémenter un dossier Shell pour votre URL :
    1.  Dans la [méthode IShellFolder :: GetUIObjectOf](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof), gérez [IQueryAssociations](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) et retournez votre Association pour vos éléments de Shell, comme illustré dans l’exemple de code suivant.

        ```
        CComPtr<IQueryAssociations> spqa;
        AssocCreate(CLSID_QueryAssociations, __uuidof(IQueryAssociations), &spqa);
        spqa->Init(0, L"Your_Object_Type", NULL, NULL);
        spqa->QueryInterface(riid, ppvReturn);
        ```

        

    2.  Une fois que l’interpréteur de commandes interroge votre dossier Shell pour obtenir le flux de données pour initialiser le gestionnaire d’aperçus, accédez à votre méthode de [méthode IShellFolder :: BindToObject](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) , gérez IID IID \_ et renvoyez un [IStream](/windows/win32/api/objidl/nn-objidl-istream) à votre URL.

Pour réutiliser un gestionnaire d’aperçus existant pour votre type de fichier, procédez comme suit :

1.  Inscrivez ce gestionnaire d’aperçus pour votre type de fichier à l’aide du CLSID du gestionnaire d’aperçus existant à la place de <votre \_ \_ GUID PreviewHandler>.
2.  Implémentez un dossier shell.

Pour plus d’informations sur la création de gestionnaires d’aperçus, consultez [IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) et les [gestionnaires d’aperçus](../shell/preview-handlers.md).

## <a name="additional-resources"></a>Ressources supplémentaires

-   Pour obtenir une vue d’ensemble du processus d’indexation, consultez [processus d’indexation](-search-indexing-process-overview.md).
-   Pour plus d’informations sur la création de gestionnaires, consultez [inscription d’extensions de Shell](../shell/reg-shell-exts.md), création de gestionnaires d’extensions de [Shell](../shell/handlers.md), [menu contextuel](/previous-versions/windows/desktop/legacy/cc144169(v=vs.85)), [extensions d’espace de noms de Shell](../shell/nse-works.md) et gestionnaires d' [Aperçu](../shell/preview-handlers.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Développement de gestionnaires de protocole](-search-3x-wds-phaddins.md)
</dt> <dt>

[Fonctionnement des gestionnaires de protocole](-search-3x-wds-extidx-prot-implementing.md)
</dt> <dt>

[Notification de l’index des modifications](-search-3x-wds-notifyingofchanges.md)
</dt> <dt>

[Exemple de code : extensions de Shell pour les gestionnaires de protocole](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[Installation et inscription de gestionnaires de protocole](-search-3x-wds-ph-install-registration.md)
</dt> <dt>

[Création d’un connecteur de recherche pour un gestionnaire de protocole](-search-3x-wds-ph-search-connector.md)
</dt> <dt>

[Débogage de gestionnaires de protocole](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 
