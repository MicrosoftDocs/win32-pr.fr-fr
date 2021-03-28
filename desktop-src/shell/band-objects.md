---
description: La barre d’exploration a été introduite avec Microsoft Internet Explorer 4,0 pour fournir une zone d’affichage adjacente au volet du navigateur.
title: Créer des barres d’explorateur, des bandes d’outils et des bandes de bureau personnalisées
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 4bf46b3f-f833-42e0-baf7-21bfa9e6d890
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: b4adeaaf089c22bd3e1db3d60d552ccc3252545a
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/28/2021
ms.locfileid: "104562930"
---
# <a name="creating-custom-explorer-bars-tool-bands-and-desk-bands"></a>Création de barres d’exploration, de bandes d’outils et de bandes de bureau personnalisées

La barre d’exploration a été introduite avec Microsoft Internet Explorer 4,0 pour fournir une zone d’affichage adjacente au volet du navigateur. En fait, il s’agit d’une fenêtre enfant dans la fenêtre Windows Internet Explorer, qui peut être utilisée pour afficher des informations et interagir avec l’utilisateur à peu près de la même façon. Les barres d’exploration sont le plus souvent affichées sous la forme d’un volet vertical sur le côté gauche du volet du navigateur. Toutefois, une barre d’exploration peut également être affichée horizontalement, sous le volet du navigateur.

![Capture d’écran montrant les barres d’exploration verticales et horizontales.](images/expl1.jpg)

Il existe un large éventail d’utilisations possibles pour le volet d’exploration. Les utilisateurs peuvent sélectionner l’option qu’ils souhaitent voir de différentes façons, notamment en les sélectionnant dans le sous-menu du **volet d’exploration** du menu **affichage** ou en cliquant sur un bouton de barre d’outils. Internet Explorer propose plusieurs barres d’exploration standard, y compris les favoris et la recherche.

L’une des méthodes permettant de personnaliser Internet Explorer consiste à ajouter un volet d’exploration personnalisé. Lorsqu’elle est implémentée et inscrite, elle est ajoutée au sous-menu du **volet d’exploration** du menu **affichage** . Lorsqu’il est sélectionné par l’utilisateur, la zone d’affichage de la barre d’exploration peut ensuite être utilisée pour afficher des informations et effectuer des entrées utilisateur de la même façon qu’une fenêtre normale.

![capture d’écran des barres de l’Explorateur](images/expl2.jpg)

Pour créer une barre d’exploration personnalisée, vous devez implémenter et inscrire un *objet de bande*. Les objets Band ont été introduits avec la version 4,71 de l’interpréteur de commandes et offrent des fonctionnalités similaires à celles des fenêtres normales. Toutefois, étant donné qu’il s’agit d’objets COM (Component Object Model) et qu’ils sont contenus par Internet Explorer ou le shell, ils sont implémentés un peu différemment. Des objets de bande simples ont été utilisés pour créer les exemples de barres d’explorateur affichées dans le premier graphique. L’implémentation de l’exemple de barre d’exploration verticale sera traitée en détail dans une section ultérieure.

## <a name="tool-bands"></a>Bandes d’outils

Une *bande d’outils* est un objet de bande introduit avec Microsoft Internet Explorer 5 pour prendre en charge la fonctionnalité de la barre d’outils radio Windows. La barre d’outils Internet Explorer est en fait un [contrôle rebar](../controls/rebar-controls.md) qui contient plusieurs [contrôles ToolBar](../controls/toolbar-control-reference.md). En créant une bande d’outils, vous pouvez ajouter une bande à ce contrôle rebar. Toutefois, comme les barres d’exploration, une bande d’outils est une fenêtre à usage général.

![capture d’écran des bandes d’outils](images/toolband1.jpg)

Les utilisateurs affichent une barre d’outils en les sélectionnant dans le sous-menu **barres** d’outils du menu **affichage** ou dans le menu contextuel qui s’affiche lorsque vous cliquez avec le bouton droit sur la zone de la barre d’outils.

## <a name="desk-bands"></a>Bandes de bureau

Les objets de bande peuvent également être utilisés pour créer des *bandes de bureau*. Bien que leur implémentation de base soit similaire aux barres d’exploration, les bandes de bureau ne sont pas liées à Internet Explorer. Une bande de bureau est fondamentalement un moyen de créer une fenêtre Ancrable sur le bureau. L’utilisateur le sélectionne en cliquant avec le bouton droit sur la barre des tâches et en le sélectionnant dans le sous-menu **barres d’outils** .

![Capture d’écran montrant un exemple de bande de bureau.](images/desk2.png)

Initialement, les bandes de bureau sont ancrées dans la barre des tâches.

![Capture d’écran montrant les bandes de bureau ancrées dans la barre des tâches.](images/desk1.jpg)

L’utilisateur peut ensuite faire glisser la bande de bureau sur le Bureau pour qu’elle s’affiche en tant que fenêtre normale.

![capture d’écran des bandes de bureau](images/desk3.png)

## <a name="implementing-band-objects"></a>Implémentation d’objets de bande

Les rubriques suivantes sont présentées.

-   [Notions de base sur les objets Band](#band-object-basics)
-   [Enregistrement de la bande](#band-registration)
-   [Exemple simple d’une barre d’exploration personnalisée](#a-simple-example-of-a-custom-explorer-bar)

### <a name="band-object-basics"></a>Notions de base sur les objets Band

Bien qu’ils puissent être utilisés comme des fenêtres normales, les objets de bande sont des objets COM qui existent au sein d’un conteneur. Les barres d’exploration sont contenues dans Internet Explorer et les bandes de bureau sont contenues dans l’interpréteur de commandes. Bien qu’elles remplissent des fonctions différentes, leur implémentation de base est très similaire. La principale différence réside dans la façon dont l’objet de bande est inscrit, qui à son tour contrôle le type d’objet et son conteneur. Cette section décrit les aspects de l’implémentation qui sont communs à tous les objets de bande. Pour plus d’informations sur l’implémentation, consultez [un exemple simple d’une barre d’explorateur personnalisée](#a-simple-example-of-a-custom-explorer-bar) .

En plus des [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) et [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory), tous les objets Band doivent implémenter les interfaces suivantes.

-   [**IDeskBand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband)
-   [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite)
-   [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream)

En plus d’inscrire leur identificateur de classe (CLSID), le volet d’exploration et les objets de la bande de bureau doivent également être inscrits pour la catégorie de composant appropriée. L’inscription de la catégorie de composant détermine le type de l’objet et son conteneur. Les bandes d’outils utilisent une autre procédure d’inscription et n’ont pas d’identificateur de catégorie (CATID). Les CATID des objets à trois bandes qui en ont besoin sont les suivants :



| Type de bande               | Catégorie de composant |
|-------------------------|--------------------|
| Barre d’explorateur verticale   | InfoBand CATID \_    |
| Barre d’explorateur horizontale | CommBand CATID \_    |
| Bande de bureau               | Deskband CATID \_    |



 

Pour plus d’informations sur la façon d’inscrire des objets de bande, consultez enregistrement de la [bande](#band-registration) .

Si l’objet de bande doit accepter l’entrée d’utilisateur, il doit également implémenter [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject). Pour ajouter des éléments au menu contextuel pour la barre d’explorateur ou les bandes de bureau, l’objet Band doit exporter [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu). Les bandes d’outils ne prennent pas en charge les menus contextuels.

Étant donné que les objets de bande implémentent une fenêtre enfant, ils doivent également implémenter une procédure de fenêtre pour gérer Windows Messaging.

Les objets Band peuvent envoyer des commandes à leur conteneur par le biais de l’interface [**IOleCommandTarget**](/windows/win32/api/docobj/nn-docobj-iolecommandtarget) du conteneur. Pour obtenir le pointeur d’interface, appelez la méthode [**IInputObjectSite :: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) du conteneur et demandez l’IID \_ IOleCommandTarget. Vous envoyez ensuite des commandes au conteneur avec [**IOleCommandTarget :: exec**](/windows/win32/api/docobj/nf-docobj-iolecommandtarget-exec). Le groupe de commandes est CGID \_ Deskband. Quand la méthode [**IDeskBand :: GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) d’un objet Band est appelée, le conteneur utilise le paramètre *dwBandID* pour affecter à l’objet Band un identificateur utilisé pour trois des commandes. Quatre ID de commande **IOleCommandTarget :: exec** sont pris en charge.

-   DBID \_ BANDINFOCHANGED

    Les informations de la bande ont changé. Définissez le paramètre *pvaIn* sur l’identificateur de bande reçu lors de l’appel le plus récent à [**IDeskBand :: GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband). Le conteneur appellera la méthode **IDeskBand :: GetBandInfo** de l’objet de la bande pour demander les informations mises à jour.

-   DBID \_ MAXIMIZEBAND

    Agrandissez la bande. Définissez le paramètre *pvaIn* sur l’identificateur de bande reçu lors de l’appel le plus récent à [**IDeskBand :: GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband).

-   DBID \_ SHOWONLY

    Activez ou désactivez les autres bandes dans le conteneur. Définissez le paramètre *pvaIn* sur le \_ type VT inconnu avec l’une des valeurs suivantes :

    

    | Valeur | Description                                                                                                 |
    |-------|-------------------------------------------------------------------------------------------------------------|
    | pUnk  | Pointeur vers l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) de l’objet de bande. Toutes les autres bandes de bureau seront masquées. |
    | 0     | Masquer toutes les bandes de bureau.                                                                                        |
    | 1     | Afficher toutes les bandes de bureau.                                                                                        |

    

     

-   DBID \_ PUSHCHEVRON

    [Version 5](versions.md). Affichez un menu Chevron. Le conteneur envoie un message [**RB \_ PUSHCHEVRON**](../controls/rb-pushchevron.md) et l’objet Band reçoit une notification [ \_ CHEVRONPUSHED RBN](../controls/rbn-chevronpushed.md) qui lui invite à afficher le menu Chevron. Définissez le paramètre *nCmdExecOpt* de la méthode [**IOleCommandTarget :: exec**](/windows/win32/api/docobj/nf-docobj-iolecommandtarget-exec) sur l’identificateur de bande reçu lors de l’appel le plus récent à [**IDeskBand :: GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband). Définissez le paramètre *pvaIn* de la méthode **IOleCommandTarget :: exec** sur le \_ type VT I4 avec une valeur définie par l’application. Elle est retransmise à l’objet de bande comme valeur *lAppValue* de la \_ notification CHEVRONPUSHED RBN.

### <a name="band-registration"></a>Enregistrement de la bande

Un objet de bande doit être inscrit en tant que serveur OLE in-process qui prend en charge le thread cloisonné. La valeur par défaut pour le serveur est une chaîne de texte de menu. Pour les barres d’exploration, elles s’affichent dans le sous-menu du **volet d’exploration** du menu **affichage** d’Internet Explorer. Pour les bandes d’outils, elles s’affichent dans le sous-menu **barres d’outils** du menu **affichage** d’Internet Explorer. Pour les bandes de bureau, elles s’affichent dans le sous-menu **barres d’outils** du menu contextuel de la barre des tâches. Comme pour les ressources de menu, le fait de placer un et commercial (&) devant une lettre est alors souligné et active les raccourcis clavier. Par exemple, la chaîne de menu de la barre d’explorateur verticale affichée dans le premier graphique est « exemple &barre d’exploration verticale ».

Au départ, Internet Explorer récupère une énumération des objets de la barre d’exploration inscrits à partir du Registre à l’aide des catégories de composants. Pour améliorer les performances, il met en cache cette énumération, ce qui a pour effet d’ajouter à la suite des barres de l’Explorateur. Pour forcer Windows Internet Explorer à reconstruire le cache et à reconnaître un nouveau volet d’exploration, supprimez les clés de Registre suivantes lors de l’inscription de la nouvelle barre d’exploration :

**HKEY \_ Logiciel \_ utilisateur actuel** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Explorer** \\  \\ **PostSetup** les \\ **catégories** \\ **de composants de composant {00021493-0000-0000-C000-000000000046}** \\ **enum**

**HKEY \_ Logiciel \_ utilisateur actuel** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Explorer** \\  \\ **PostSetup** les \\ **catégories** \\ **de composants de composant {00021494-0000-0000-C000-000000000046}** \\ **enum**

> [!Note]  
> Étant donné qu’un cache de barre d’exploration est créé pour chaque utilisateur, votre application de configuration doit peut-être énumérer toutes les ruches de Registre utilisateur ou ajouter un stub par utilisateur à exécuter lorsque l’utilisateur se connecte pour la première fois.

 

En général, l’entrée de registre de base pour un objet de bande s’affiche comme suit.

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         (Default) = Menu Text String
         InProcServer32
            (Default) = DLL Path Name
            ThreadingModel = Apartment
```

Le CLSID de l’objet doit également être inscrit auprès d’Internet Explorer pour les bandes d’outils. Pour ce faire, affectez une valeur sous la barre d’outils **HKEY \_ local \_ machine** \\ **Software** \\ **Microsoft** \\ **Internet Explorer** \\  avec le GUID CLSID de l’objet de la bande outil, comme indiqué ici. Comme sa valeur de données est ignorée, le type de valeur n’est pas important.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Internet Explorer
            Toolbar
               {Your Band Object's CLSID GUID}
```

Plusieurs valeurs facultatives peuvent également être ajoutées au registre. Par exemple, la valeur suivante est nécessaire si vous souhaitez utiliser le volet d’exploration pour afficher le code HTML. la valeur affichée n’est pas un exemple, mais la valeur réelle à utiliser.

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         Instance
            CLSID
               (Default) = {4D5C8C2A-D075-11D0-B416-00C04FB90376}
```

Utilisé conjointement avec la valeur indiquée ci-dessus, la valeur facultative suivante est également nécessaire si vous souhaitez utiliser le volet d’exploration pour afficher du code HTML. Cette valeur doit être définie sur l’emplacement du fichier qui contient le contenu HTML pour le volet d’exploration.

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         Instance
            InitPropertyBag
               Url
```

Une autre valeur facultative définit la largeur ou la hauteur par défaut du volet d’exploration, selon qu’il est vertical ou horizontal, respectivement.

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Internet Explorer
            Explorer Bars
               {Your Band Object's CLSID GUID}
                  BarSize
```

La valeur de la coordonnée doit être définie sur la largeur ou la hauteur de la barre. La valeur nécessite huit octets et est placée dans le registre en tant que valeur binaire. Les quatre premiers octets spécifient la taille en pixels, au format hexadécimal, à partir de l’octet le plus à gauche. Les quatre derniers octets sont réservés et doivent être définis sur zéro.

Par exemple, les entrées de Registre complètes pour un volet d’exploration HTML avec une largeur par défaut de 291 (0X123) pixels sont indiquées ici.

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         (Default) = Menu Text String
         InProcServer32
            (Default) = DLL Path Name
            ThreadingModel = Apartment
         Instance
            CLSID
               (Default) = {4D5C8C2A-D075-11D0-B416-00C04FB90376}
            InitPropertyBag
               Url = Your HTML File
HKEY_CURRENT_USER
   Software
      Microsoft
         Internet Explorer
            Explorer Bars
               {Your Band Object's CLSID GUID}
                  BarSize = 23 01 00 00 00 00 00 00
```

Vous pouvez gérer l’inscription du CATID d’un objet de bande par programme. Créez un objet gestionnaire de catégories de composants (CLSID \_ StdComponentCategoriesMgr) et demandez un pointeur vers son interface [**ICatRegister**](/windows/win32/api/comcat/nn-comcat-icatregister) . Transmettez le CLSID de l’objet de la bande et le CATID à [**ICatRegister :: RegisterClassImplCategories**](/windows/win32/api/comcat/nf-comcat-icatregister-registerclassimplcategories).

### <a name="a-simple-example-of-a-custom-explorer-bar"></a>Exemple simple d’une barre d’exploration personnalisée

Cet exemple passe en revue l’implémentation de l’exemple de barre d’exploration verticale présentée dans l’introduction.

La procédure de base pour créer une barre d’exploration personnalisée est la suivante.

1.  [Implémentez les fonctions nécessaires à la dll](#dll-functions).
2.  [Implémentez les interfaces COM requises.](#required-interface-implementations)
3.  [Implémentez toutes les interfaces COM facultatives souhaitées.](#optional-interface-implementations)
4.  [Enregistrez le CLSID de l’objet et, si nécessaire, la catégorie du composant.](#clsid-registration)
5.  Créer une fenêtre enfant d’Internet Explorer, dimensionnée pour s’ajuster à la zone d’affichage de la barre d’exploration.
6.  [Utilisez la fenêtre enfant pour afficher des informations et interagir avec l’utilisateur.](#the-window-procedure)

L’implémentation très simple utilisée dans l’exemple de volet d’exploration peut être utilisée pour un type de barre d’exploration ou une bande de bureau, en l’inscrivant simplement pour la catégorie de composant appropriée. Des implémentations plus sophistiquées devront être personnalisées pour la région d’affichage et le conteneur de chaque type d’objet. Toutefois, une grande partie de cette personnalisation peut être accomplie en utilisant l’exemple de code et en l’étendant en appliquant des techniques de programmation Windows familières à la fenêtre enfant. Par exemple, vous pouvez ajouter des contrôles pour l’interaction de l’utilisateur ou des graphiques pour un affichage plus riche.

### <a name="dll-functions"></a>Fonctions DLL

Les trois objets sont empaquetés dans une seule DLL, qui expose les fonctions suivantes.

-   [**DllMain**](../dlls/dllmain.md)
-   [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow)
-   [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject)
-   [**Accompli**](/windows/win32/api/olectl/nf-olectl-dllregisterserver)

Les trois premières fonctions sont des implémentations standard et ne sont pas abordées ici. L’implémentation de la fabrique de classes est également standard.

### <a name="required-interface-implementations"></a>Implémentations d’interface requises

L’exemple vertical du volet d’exploration implémente les quatre interfaces requises : [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite), [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream)et [**IDeskBand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) dans le cadre de la classe CExplorerBar. Le constructeur, le destructeur et les implémentations **IUnknown** sont simples et ne seront pas abordés ici. Consultez l'exemple de code pour plus d'informations.

Les interfaces suivantes sont décrites en détail.

-   [IObjectWithSite](#iobjectwithsite)
-   [IPersistStream](#ipersiststream)
-   [IDeskBand](#ideskband)

### <a name="iobjectwithsite"></a>IObjectWithSite

Quand l’utilisateur sélectionne une barre d’exploration, le conteneur appelle la méthode [**IObjectWithSite :: SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) correspondante de l’objet de bande. Le paramètre *punkSite* est défini sur le pointeur [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) du site.

En général, une implémentation de [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) doit effectuer les étapes suivantes :

1.  Libère tout pointeur de site qui est actuellement détenu.
2.  Si le pointeur passé à [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) a la valeur **null**, la bande est en cours de suppression. **SetSite** peut retourner S \_ OK.
3.  Si le pointeur passé à [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) est non **null**, un nouveau site est défini. La **SetSite** doit effectuer les opérations suivantes :
    1.  Appelez [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur le site pour son interface [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) .
    2.  Appelez [**IOleWindow :: GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) pour obtenir le handle de la fenêtre parente. Enregistrez le descripteur pour une utilisation ultérieure. Release [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) si elle n’est plus nécessaire.
    3.  Créez la fenêtre de l’objet de la bande en tant qu’enfant de la fenêtre obtenue à l’étape précédente. Ne le créez pas en tant que fenêtre visible.
    4.  Si l’objet de bande implémente [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject), appelez [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur le site pour son interface [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) . Stockez le pointeur vers cette interface pour une utilisation ultérieure.
    5.  Si toutes les étapes sont réussies, l’opération retourne S \_ OK. Si ce n’est pas le cas, retournez le code d’erreur défini par OLE indiquant ce qui a échoué.

L’exemple de volet d’exploration implémente [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) de la façon suivante. Dans le code m suivant, *\_ pSite* est une variable membre privée qui contient le pointeur [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) et *m \_ hwndParent* contient le handle de la fenêtre parente. Dans cet exemple, la création de fenêtres est également gérée. Si la fenêtre n’existe pas, cette méthode crée la fenêtre de la barre d’exploration en tant qu’enfant de taille appropriée de la fenêtre parente obtenue par **SetSite**. Le handle de la fenêtre enfant est stocké dans *m \_ HWND*.


```C++
STDMETHODIMP CDeskBand::SetSite(IUnknown *pUnkSite)
{
    HRESULT hr = S_OK;

    m_hwndParent = NULL;

    if (m_pSite)
    {
        m_pSite->Release();
    }

    if (pUnkSite)
    {
        IOleWindow *pow;
        hr = pUnkSite->QueryInterface(IID_IOleWindow, reinterpret_cast<void **>(&pow));
        if (SUCCEEDED(hr))
        {
            hr = pow->GetWindow(&m_hwndParent);
            if (SUCCEEDED(hr))
            {
                WNDCLASSW wc = { 0 };
                wc.style         = CS_HREDRAW | CS_VREDRAW;
                wc.hCursor       = LoadCursor(NULL, IDC_ARROW);
                wc.hInstance     = g_hInst;
                wc.lpfnWndProc   = WndProc;
                wc.lpszClassName = g_szDeskBandSampleClass;
                wc.hbrBackground = CreateSolidBrush(RGB(255, 255, 0));

                RegisterClassW(&wc);

                CreateWindowExW(0,
                                g_szDeskBandSampleClass,
                                NULL,
                                WS_CHILD | WS_CLIPCHILDREN | WS_CLIPSIBLINGS,
                                0,
                                0,
                                0,
                                0,
                                m_hwndParent,
                                NULL,
                                g_hInst,
                                this);

                if (!m_hwnd)
                {
                    hr = E_FAIL;
                }
            }

            pow->Release();
        }

        hr = pUnkSite->QueryInterface(IID_IInputObjectSite, reinterpret_cast<void **>(&m_pSite));
    }

    return hr;
}
```



L’implémentation [**GetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-getsite) de l’exemple encapsule simplement un appel à la méthode [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) du site, à l’aide du pointeur de site enregistré par [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite).


```C++
STDMETHODIMP CDeskBand::GetSite(REFIID riid, void **ppv)
{
    HRESULT hr = E_FAIL;

    if (m_pSite)
    {
        hr =  m_pSite->QueryInterface(riid, ppv);
    }
    else
    {
        *ppv = NULL;
    }

    return hr;
}
```



### <a name="ipersiststream"></a>IPersistStream

Internet Explorer appellera l’interface [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream) de la barre d’explorateur pour permettre au volet d’exploration de charger ou d’enregistrer les données persistantes. S’il n’y a pas de données persistantes, les méthodes doivent toujours retourner un code de réussite. L’interface **IPersistStream** hérite d' [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist), donc cinq méthodes doivent être implémentées.

-   [**IPersist :: GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid)
-   [**IPersistStream :: IsDirty**](/windows/win32/api/objidl/nf-objidl-ipersiststream-isdirty)
-   [**IPersistStream :: Load**](/windows/win32/api/objidl/nf-objidl-ipersiststream-load)
-   [**IPersistStream :: Save**](/windows/win32/api/objidl/nf-objidl-ipersiststream-save)
-   [**IPersistStream :: GetSizeMax**](/windows/win32/api/objidl/nf-objidl-ipersiststream-getsizemax)

L’exemple de volet d’exploration n’utilise pas de données persistantes et n’a qu’une implémentation minimale d' [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream). [**IPersist :: GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) retourne le CLSID de l’objet (CLSID \_ SampleExplorerBar) et le reste retourne soit S \_ OK, s \_ false, soit E \_ NOTIMPL.

### <a name="ideskband"></a>IDeskBand

L’interface [**IDeskBand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) est spécifique aux objets Band. En plus de sa méthode, elle hérite de [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow), qui à son tour hérite de [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow).

Il existe deux méthodes [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) : [**GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) et [**IOleWindow :: ContextSensitiveHelp**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-contextsensitivehelp). L’implémentation de **GetWindow** de l’exemple de volet d’exploration retourne le handle de fenêtre enfant de la barre d’exploration, *m \_ HWND*. L’aide contextuelle n’étant pas implémentée, **ContextSensitiveHelp** retourne **E \_ NOTIMPL**.

L’interface [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) a trois méthodes.

-   [**IDockingWindow::ShowDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-showdw)
-   [**IDockingWindow::CloseDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-closedw)
-   [**IDockingWindow::ResizeBorderDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-resizeborderdw)

La méthode [**ResizeBorderDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-resizeborderdw) n’est pas utilisée avec un type d’objet Band et doit toujours retourner E \_ NOTIMPL. La méthode [**ShowDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-showdw) affiche ou masque la fenêtre de la barre d’exploration, en fonction de la valeur de son paramètre.


```C++
STDMETHODIMP CDeskBand::ShowDW(BOOL fShow)
{
    if (m_hwnd)
    {
        ShowWindow(m_hwnd, fShow ? SW_SHOW : SW_HIDE);
    }

    return S_OK;
}
```



La méthode [**CloseDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-closedw) détruit la fenêtre de la barre d’exploration.


```C++
STDMETHODIMP CDeskBand::CloseDW(DWORD)
{
    if (m_hwnd)
    {
        ShowWindow(m_hwnd, SW_HIDE);
        DestroyWindow(m_hwnd);
        m_hwnd = NULL;
    }

    return S_OK;
}
```



La méthode restante, [**GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband), est spécifique à **IDeskBand**. Internet Explorer l’utilise pour spécifier l’identificateur et le mode d’affichage de la barre d’exploration. Internet Explorer peut également demander une ou plusieurs informations à partir du volet de l’Explorateur en remplissant le membre **dwMask** de la structure [**DESKBANDINFO**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-deskbandinfo) qui est passée comme troisième paramètre. **GetBandInfo** doit stocker l’identificateur et le mode d’affichage, et remplir la structure **DESKBANDINFO** avec les données demandées. L’exemple de volet d’exploration implémente **GetBandInfo** comme indiqué dans l’exemple de code suivant.


```C++
STDMETHODIMP CDeskBand::GetBandInfo(DWORD dwBandID, DWORD, DESKBANDINFO *pdbi)
{
    HRESULT hr = E_INVALIDARG;

    if (pdbi)
    {
        m_dwBandID = dwBandID;

        if (pdbi->dwMask & DBIM_MINSIZE)
        {
            pdbi->ptMinSize.x = 200;
            pdbi->ptMinSize.y = 30;
        }

        if (pdbi->dwMask & DBIM_MAXSIZE)
        {
            pdbi->ptMaxSize.y = -1;
        }

        if (pdbi->dwMask & DBIM_INTEGRAL)
        {
            pdbi->ptIntegral.y = 1;
        }

        if (pdbi->dwMask & DBIM_ACTUAL)
        {
            pdbi->ptActual.x = 200;
            pdbi->ptActual.y = 30;
        }

        if (pdbi->dwMask & DBIM_TITLE)
        {
            // Don't show title by removing this flag.
            pdbi->dwMask &= ~DBIM_TITLE;
        }

        if (pdbi->dwMask & DBIM_MODEFLAGS)
        {
            pdbi->dwModeFlags = DBIMF_NORMAL | DBIMF_VARIABLEHEIGHT;
        }

        if (pdbi->dwMask & DBIM_BKCOLOR)
        {
            // Use the default background color by removing this flag.
            pdbi->dwMask &= ~DBIM_BKCOLOR;
        }

        hr = S_OK;
    }

    return hr;
}
```



### <a name="optional-interface-implementations"></a>Implémentations d’interface facultatives

Il existe deux interfaces qui ne sont pas requises, mais qui peuvent être utiles pour implémenter : [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject) et [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu). L’exemple de volet d’exploration implémente **IInputObject**. Reportez-vous à la documentation pour plus d’informations sur l’implémentation de **IContextMenu**.

### <a name="iinputobject"></a>IInputObject

L’interface [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject) doit être implémentée si un objet Band accepte une entrée d’utilisateur. Internet Explorer implémente [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) et utilise **IInputObject** pour maintenir le focus d’entrée d’utilisateur approprié lorsqu’il a plusieurs fenêtres contenues. Il existe trois méthodes qui doivent être implémentées par une barre d’exploration.

-   [**IInputObject::UIActivateIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-uiactivateio)
-   [**IInputObject::HasFocusIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-hasfocusio)
-   [**IInputObject::TranslateAcceleratorIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-translateacceleratorio)

Internet Explorer appelle [**UIActivateIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-uiactivateio) pour informer le volet d’exploration qu’il est en cours d’activation ou de désactivation. Lorsqu’il est activé, l’exemple de volet d’exploration appelle [**SetFocus**](/windows/win32/api/winuser/nf-winuser-setfocus) pour définir le focus sur sa fenêtre.

Internet Explorer appelle [**HasFocusIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-hasfocusio) lorsqu’il tente de déterminer la fenêtre qui a le focus. Si la fenêtre de la barre d’exploration ou l’un de ses descendants a le focus, **HasFocusIO** doit retourner s \_ OK. Si ce n’est pas le cas, elle doit retourner S \_ false.

[**TranslateAcceleratorIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-translateacceleratorio) permet à l’objet de traiter des accélérateurs de clavier. L’exemple de volet d’exploration n’implémente pas cette méthode. il retourne alors S \_ false.

L’implémentation de la barre d’exemple de [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) est la suivante.


```C++
STDMETHODIMP CDeskBand::UIActivateIO(BOOL fActivate, MSG *)
{
    if (fActivate)
    {
        SetFocus(m_hwnd);
    }

    return S_OK;
}

STDMETHODIMP CDeskBand::HasFocusIO()
{
    return m_fHasFocus ? S_OK : S_FALSE;
}

STDMETHODIMP CDeskBand::TranslateAcceleratorIO(MSG *)
{
    return S_FALSE;
};
```



### <a name="clsid-registration"></a>Inscription du CLSID

Comme pour tous les objets COM, le CLSID de la barre d’exploration doit être enregistré. Pour que l’objet fonctionne correctement avec Internet Explorer, il doit également être inscrit pour la catégorie de composant appropriée (CATID \_ InfoBand). La section de code appropriée pour le volet d’exploration est présentée dans l’exemple de code suivant.


```C++
HRESULT RegisterServer()
{
    WCHAR szCLSID[MAX_PATH];
    StringFromGUID2(CLSID_DeskBandSample, szCLSID, ARRAYSIZE(szCLSID));

    WCHAR szSubkey[MAX_PATH];
    HKEY hKey;

    HRESULT hr = StringCchPrintfW(szSubkey, ARRAYSIZE(szSubkey), L"CLSID\\%s", szCLSID);
    if (SUCCEEDED(hr))
    {
        hr = E_FAIL;
        if (ERROR_SUCCESS == RegCreateKeyExW(HKEY_CLASSES_ROOT,
                                             szSubkey,
                                             0,
                                             NULL,
                                             REG_OPTION_NON_VOLATILE,
                                             KEY_WRITE,
                                             NULL,
                                             &hKey,
                                             NULL))
        {
            WCHAR const szName[] = L"DeskBand Sample";
            if (ERROR_SUCCESS == RegSetValueExW(hKey,
                                                NULL,
                                                0,
                                                REG_SZ,
                                                (LPBYTE) szName,
                                                sizeof(szName)))
            {
                hr = S_OK;
            }

            RegCloseKey(hKey);
        }
    }

    if (SUCCEEDED(hr))
    {
        hr = StringCchPrintfW(szSubkey, ARRAYSIZE(szSubkey), L"CLSID\\%s\\InprocServer32", szCLSID);
        if (SUCCEEDED(hr))
        {
            hr = HRESULT_FROM_WIN32(RegCreateKeyExW(HKEY_CLASSES_ROOT, szSubkey,
                 0, NULL, REG_OPTION_NON_VOLATILE, KEY_WRITE, NULL, &hKey, NULL));
            if (SUCCEEDED(hr))
            {
                WCHAR szModule[MAX_PATH];
                if (GetModuleFileNameW(g_hInst, szModule, ARRAYSIZE(szModule)))
                {
                    DWORD cch = lstrlen(szModule);
                    hr = HRESULT_FROM_WIN32(RegSetValueExW(hKey, NULL, 0, REG_SZ, (LPBYTE) szModule, cch * sizeof(szModule[0])));
                }

                if (SUCCEEDED(hr))
                {
                    WCHAR const szModel[] = L"Apartment";
                    hr = HRESULT_FROM_WIN32(RegSetValueExW(hKey, L"ThreadingModel", 0,  REG_SZ, (LPBYTE) szModel, sizeof(szModel)));
                }

                RegCloseKey(hKey);
            }
        }
    }

    return hr;
}
```



L’inscription des objets Band dans l’exemple utilise des procédures COM normales.

En plus du CLSID, le serveur d’objets de bande doit également être inscrit pour une ou plusieurs catégories de composants. Il s’agit en fait de la principale différence d’implémentation entre les exemples de barres d’exploration verticales et horizontales. Ce processus est géré en créant un objet gestionnaire de catégories de composants (CLSID \_ StdComponentCategoriesMgr) et en utilisant la méthode [**ICatRegister :: RegisterClassImplCategories**](/windows/win32/api/comcat/nf-comcat-icatregister-registerclassimplcategories) pour inscrire le serveur d’objets de bande. Dans cet exemple, l’inscription de catégorie de composant est gérée en passant le CLSID de l’exemple de volet d’exploration et le CATID à une fonction privée (**RegisterComCat**), comme indiqué dans l’exemple de code suivant.


```C++
HRESULT RegisterComCat()
{
    ICatRegister *pcr;
    HRESULT hr = CoCreateInstance(CLSID_StdComponentCategoriesMgr, NULL, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pcr));
    if (SUCCEEDED(hr))
    {
        CATID catid = CATID_DeskBand;
        hr = pcr->RegisterClassImplCategories(CLSID_DeskBandSample, 1, &catid);
        pcr->Release();
    }
    return hr;
}
```



### <a name="the-window-procedure"></a>La procédure de fenêtre

Comme un objet de bande utilise une fenêtre enfant pour son affichage, il doit implémenter une procédure de fenêtre pour gérer Windows Messaging. L’exemple de bande a des fonctionnalités minimales, donc la procédure de fenêtre gère uniquement cinq messages :

-   [**\_NCCREATE WM**](../winmsg/wm-nccreate.md)
-   [**\_peinture WM**](../gdi/wm-paint.md)
-   [**WM, \_ commande**](../menurc/wm-command.md)
-   [**WM \_ SetFocus**](../inputdev/wm-setfocus.md)
-   [**\_KILLFOCUS WM**](../inputdev/wm-killfocus.md)

La procédure peut facilement être développée pour accueillir des messages supplémentaires afin de prendre en charge davantage de fonctionnalités.


```C++
LRESULT CALLBACK CDeskBand::WndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    LRESULT lResult = 0;

    CDeskBand *pDeskBand = reinterpret_cast<CDeskBand *>(GetWindowLongPtr(hwnd, GWLP_USERDATA));

    switch (uMsg)
    {
    case WM_CREATE:
        pDeskBand = reinterpret_cast<CDeskBand *>(reinterpret_cast<CREATESTRUCT *>(lParam)->lpCreateParams);
        pDeskBand->m_hwnd = hwnd;
        SetWindowLongPtr(hwnd, GWLP_USERDATA, reinterpret_cast<LONG_PTR>(pDeskBand));
        break;

    case WM_SETFOCUS:
        pDeskBand->OnFocus(TRUE);
        break;

    case WM_KILLFOCUS:
        pDeskBand->OnFocus(FALSE);
        break;

    case WM_PAINT:
        pDeskBand->OnPaint(NULL);
        break;

    case WM_PRINTCLIENT:
        pDeskBand->OnPaint(reinterpret_cast<HDC>(wParam));
        break;

    case WM_ERASEBKGND:
        if (pDeskBand->m_fCompositionEnabled)
        {
            lResult = 1;
        }
        break;
    }

    if (uMsg != WM_ERASEBKGND)
    {
        lResult = DefWindowProc(hwnd, uMsg, wParam, lParam);
    }

    return lResult;
}
```



Le \_ Gestionnaire de commandes WM retourne simplement zéro. Le \_ Gestionnaire de peinture WM crée l’affichage de texte simple présenté dans l’exemple du volet d’exploration de l’introduction.


```C++
void CDeskBand::OnPaint(const HDC hdcIn)
{
    HDC hdc = hdcIn;
    PAINTSTRUCT ps;
    static WCHAR szContent[] = L"DeskBand Sample";
    static WCHAR szContentGlass[] = L"DeskBand Sample (Glass)";

    if (!hdc)
    {
        hdc = BeginPaint(m_hwnd, &ps);
    }

    if (hdc)
    {
        RECT rc;
        GetClientRect(m_hwnd, &rc);

        SIZE size;

        if (m_fCompositionEnabled)
        {
            HTHEME hTheme = OpenThemeData(NULL, L"BUTTON");
            if (hTheme)
            {
                HDC hdcPaint = NULL;
                HPAINTBUFFER hBufferedPaint = BeginBufferedPaint(hdc, &rc, BPBF_TOPDOWNDIB, NULL, &hdcPaint);

                DrawThemeParentBackground(m_hwnd, hdcPaint, &rc);

                GetTextExtentPointW(hdc, szContentGlass, ARRAYSIZE(szContentGlass), &size);
                RECT rcText;
                rcText.left   = (RECTWIDTH(rc) - size.cx) / 2;
                rcText.top    = (RECTHEIGHT(rc) - size.cy) / 2;
                rcText.right  = rcText.left + size.cx;
                rcText.bottom = rcText.top + size.cy;

                DTTOPTS dttOpts = {sizeof(dttOpts)};
                dttOpts.dwFlags = DTT_COMPOSITED | DTT_TEXTCOLOR | DTT_GLOWSIZE;
                dttOpts.crText = RGB(255, 255, 0);
                dttOpts.iGlowSize = 10;
                DrawThemeTextEx(hTheme, hdcPaint, 0, 0, szContentGlass, -1, 0, &rcText, &dttOpts);

                EndBufferedPaint(hBufferedPaint, TRUE);

                CloseThemeData(hTheme);
            }
        }
        else
        {
            SetBkColor(hdc, RGB(255, 255, 0));
            GetTextExtentPointW(hdc, szContent, ARRAYSIZE(szContent), &size);
            TextOutW(hdc,
                     (RECTWIDTH(rc) - size.cx) / 2,
                     (RECTHEIGHT(rc) - size.cy) / 2,
                     szContent,
                     ARRAYSIZE(szContent));
        }
    }

    if (!hdcIn)
    {
        EndPaint(m_hwnd, &ps);
    }
}
```



Les \_ gestionnaires WM SetFocus et WM \_ KILLFOCUS informent le site d’une modification de focus en appelant la méthode [**IInputObjectSite :: OnFocusChangeIS**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iinputobjectsite-onfocuschangeis) du site.


```C++
void CDeskBand::OnFocus(const BOOL fFocus)
{
    m_fHasFocus = fFocus;

    if (m_pSite)
    {
        m_pSite->OnFocusChangeIS(static_cast<IOleWindow*>(this), m_fHasFocus);
    }
}
```



Les objets Band offrent un moyen flexible et puissant d’étendre les fonctionnalités d’Internet Explorer en créant des barres d’exploration personnalisées. L’implémentation d’une bande de bureau vous permet d’étendre les fonctionnalités des fenêtres normales. Bien que certaines programmations COM soient nécessaires, elle sert en fin de vue de fournir une fenêtre enfant pour votre interface utilisateur. À partir de là, la majeure partie de l’implémentation peut utiliser des techniques de programmation Windows familières. Bien que l’exemple présenté ici ait uniquement des fonctionnalités limitées, il illustre toutes les fonctionnalités nécessaires d’un objet Band et peut être facilement étendu pour créer une interface utilisateur unique et puissante.

 

 
