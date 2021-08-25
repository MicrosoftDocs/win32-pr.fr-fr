---
title: migration vers l’infrastructure de ruban Windows
description: une application qui s’appuie sur des menus, des barres d’outils et des boîtes de dialogue traditionnels peut être migrée vers l’interface utilisateur riche, dynamique et basée sur le contexte de Windows système de commandes de l’infrastructure du ruban.
ms.assetid: 3a8ca41e-18b3-4c9d-865b-5f4c5fcf7ceb
keywords:
- Windows Ruban, migration vers
- Ruban, migration vers
- migration vers Windows ruban
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a011e9b5dad52f6f71fab272f0fded39ec59eb71cc7311ab9cf5ffccb4dfbca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119841119"
---
# <a name="migrating-to-the-windows-ribbon-framework"></a>migration vers l’infrastructure de ruban Windows

une application qui s’appuie sur des menus, des barres d’outils et des boîtes de dialogue traditionnels peut être migrée vers l’interface utilisateur riche, dynamique et basée sur le contexte de Windows système de commandes de l’infrastructure du ruban. Il s’agit d’un moyen simple et efficace de moderniser et de revitaliser l’application tout en améliorant également l’accessibilité, la convivialité et la détectabilité de ses fonctionnalités.

## <a name="introduction"></a>Introduction

En général, la migration d’une application existante vers l’infrastructure du ruban implique les opérations suivantes :

-   Conception d’une disposition de ruban et d’une organisation de contrôle qui expose les fonctionnalités de l’application existante et est suffisamment flexible pour prendre en charge les nouvelles fonctionnalités.
-   Adaptation du code de l’application existante.
-   Migration des ressources d’application existantes (chaînes et images) vers l’infrastructure du ruban.

> [!Note]  
> Les [instructions relatives à l’expérience utilisateur du ruban](https://msdn.microsoft.com/library/cc872782.aspx) doivent être examinées pour déterminer si l’application est un candidat approprié pour une interface ruban.

 

## <a name="design-the-ribbon-layout"></a>Concevoir la disposition du ruban

Les conceptions de l’interface utilisateur du ruban et les dispositions de contrôle potentielles peuvent être identifiées en effectuant les étapes suivantes :

1.  En effectuant l’inventaire de toutes les fonctionnalités existantes.
2.  Conversion de cette fonctionnalité en commandes de ruban.
3.  Organisation des commandes en groupes logiques.

### <a name="take-inventory"></a>Effectuer un inventaire

Dans l’infrastructure du ruban, la fonctionnalité exposée par une application qui manipule l’État ou la vue d’un espace de travail ou d’un document est considérée comme une commande. Ce qui constitue une commande peut varier et dépend de la nature et du domaine de l’application existante.

Le tableau suivant répertorie un ensemble de commandes de base pour une application hypothétique de modification de texte :



| Symbole           | id     | Description               |
|------------------|--------|---------------------------|
| fichier d’ID \_ \_ nouveau    | 0xE100 | Nouveau document              |
| \_enregistrement du fichier d’ID \_   | 0xE103 | Enregistrer le document             |
| \_enregistrement du fichier d’ID \_ | 0xE104 | Enregistrer sous... dialogue       |
| fichier d’ID \_ \_ ouvert   | 0xE101 | Ouvrir... dialogue          |
| \_sortie du fichier d’ID \_   | 0xE102 | Quitter l’application      |
| \_annuler la modification de l’ID \_   | 0xE12B | Annuler                      |
| modifier l’ID \_ \_ couper    | 0xE123 | Couper le texte sélectionné         |
| copier l’ID \_ \_   | 0xE122 | Copier le texte sélectionné        |
| édition de l’ID- \_ \_ coller  | 0xE125 | Coller le texte à partir du presse-papiers |
| modification d’ID \_ \_ Effacer  | 0xE120 | Supprimer le texte sélectionné      |
| ZOOM de la vue d’ID \_ \_   | 1242   | Zoom... dialogue          |



 

Regardez au-delà des menus et des barres d’outils existants lors de la création d’un inventaire des commandes. Prenez en compte toutes les façons dont un utilisateur peut interagir avec l’espace de travail. Même si toutes les commandes ne conviennent pas à l’inclusion dans le ruban, cet exercice peut très bien exposer des commandes qui ont été masquées par des couches d’interface utilisateur.

### <a name="translate"></a>Translate

Toutes les commandes ne doivent pas être représentées dans l’interface ruban. Par exemple, en entrant du texte, en modifiant une sélection, en faisant défiler ou en déplaçant le point d’insertion avec les commandes de la souris toutes éligibles dans l’éditeur de texte hypothétique, toutefois, celles-ci ne conviennent pas à l’exposition dans une barre de commandes, car chacune implique une interaction directe avec l’interface utilisateur de l’application.

À l’inverse, certaines fonctionnalités peuvent ne pas être considérées comme une commande dans le sens traditionnel. Par exemple, au lieu d’être enfoui dans une boîte de dialogue, les réglages de marge de page de l’imprimante peuvent être représentés dans le ruban sous la forme d’un groupe de contrôles Spinner dans un onglet contextuel ou [en mode application](ribbon-applicationmodes.md).

> [!Note]  
> Prenez note de l’ID numérique qui peut être assigné à chaque commande. Certaines infrastructures d’interface utilisateur, telles que Microsoft Foundation Classes (MFC), définissent des ID pour les commandes telles que le menu fichier et Edition (0xE100 à 0xE200).

 

### <a name="organize"></a>Organiser

Avant de tenter d’organiser l’inventaire des commandes, les recommandations relatives à l' [expérience utilisateur du ruban](https://msdn.microsoft.com/library/cc872782.aspx) doivent être examinées pour connaître les meilleures pratiques lors de l’implémentation d’une interface utilisateur du ruban.

En général, les règles suivantes peuvent être appliquées à l’Organisation des commandes du ruban :

-   Les commandes qui opèrent sur le fichier ou l’application globale appartiennent très probablement au menu de l' [application](windowsribbon-controls-applicationmenu.md).
-   Les commandes fréquemment utilisées, telles que couper, copier et coller (comme dans l’exemple de l’éditeur de texte), sont généralement placées sur un onglet de démarrage par défaut. Dans les applications plus complexes, elles peuvent être dupliquées ailleurs dans l’interface ruban.
-   Les commandes importantes ou fréquemment utilisées peuvent garantir l’inclusion par défaut dans la [barre d’outils accès rapide](windowsribbon-controls-quickaccesstoolbar.md).

L’infrastructure du ruban fournit également des contrôles ContextMenu et MiniToolbar via la vue ContextPopup. Ces fonctionnalités ne sont pas obligatoires, mais si votre application possède un ou plusieurs menus contextuels existants, la migration des commandes qu’elles contiennent peut permettre la réutilisation du code base existant avec une liaison automatique avec les ressources existantes.

Étant donné que chaque application est différente, lisez les instructions et essayez de les appliquer dans la mesure du possible. L’un des objectifs de l’infrastructure du ruban est de fournir une expérience utilisateur familière et cohérente. cet objectif sera plus réalisable si les conceptions de nouvelles applications reflètent le plus possible les applications de ruban existantes.

## <a name="adapt-your-code"></a>Adapter votre code

Une fois que les commandes de ruban ont été identifiées et organisées en regroupements logiques, le nombre d’étapes impliquées dans l’incorporation de l’infrastructure du ruban dans le code d’application existant dépend de la complexité de l’application d’origine. En général, il existe trois étapes de base :

-   Créez le balisage du ruban en fonction de l’organisation de la commande et de la spécification de la disposition.
-   Remplacez les fonctionnalités de menu et de barre d’outils héritées par la fonctionnalité du ruban.
-   Implémentez un adaptateur IUICommandHandler.

### <a name="create-the-markup"></a>Créer le balisage

La liste des commandes, ainsi que leur organisation et leur disposition, sont déclarées par le biais du fichier de balisage du ruban qui est consommé par le [compilateur de balisage du ruban](windowsribbon-intentcl.md).

> [!Note]  
> La plupart des étapes requises pour adapter une application existante sont similaires à celles requises pour démarrer une nouvelle application ruban. Pour plus d’informations, consultez le didacticiel [création d’une application de ruban](windowsribbon-stepbystep.md) pour une nouvelle application ruban.

 

Il existe deux sections principales pour le balisage du ruban. La première section est un manifeste de commandes et les ressources associées (chaînes et images). La deuxième section spécifie la structure et le positionnement des contrôles sur le ruban.

Le balisage de l’éditeur de texte simple peut se présenter comme dans l’exemple suivant :

> [!Note]  
> Les ressources de type image et chaîne sont traitées plus loin dans cet article.

 


```C++
<?xml version="1.0" encoding="utf-8"?>
<Application xmlns="http://schemas.microsoft.com/windows/2009/Ribbon">

  <Application.Commands>
    <Command Name="cmdNew" Id="0xE100" Symbol="ID_CMD_NEW" LabelTitle="New document" />
    <Command Name="cmdSave" Id="0xE103" Symbol="ID_CMD_SAVE" LabelTitle="Save" />
    <Command Name="cmdSaveAs" Id="0xE104" Symbol="ID_CMD_SAVEAS" LabelTitle="Save as" />
    <Command Name="cmdOpen" Id="0xE101" Symbol="ID_CMD_OPEN" LabelTitle="Open" />
    <Command Name="cmdExit" Id="0xE102" Symbol="ID_CMD_EXIT" LabelTitle="Exit" />
    <Command Name="cmdUndo" Id="0xE12B" Symbol="ID_CMD_UNDO" LabelTitle="Undo" />
    <Command Name="cmdCut" Id="0xE123" Symbol="ID_CMD_CUT" LabelTitle="Cut" />
    <Command Name="cmdCopy" Id="0xE122" Symbol="ID_CMD_COPY" LabelTitle="Copy" />
    <Command Name="cmdPaste" Id="0xE125" Symbol="ID_CMD_PASTE" LabelTitle="Paste" />
    <Command Name="cmdDelete" Id="0xE120" Symbol="ID_CMD_DELETE" LabelTitle="Delete" />
    <Command Name="cmdZoom" Id="1242" Symbol="ID_CMD_ZOOM" LabelTitle="Zoom" />
  </Application.Commands>

  <Application.Views>
    <Ribbon>
      <Ribbon.ApplicationMenu>
        <ApplicationMenu>
          <MenuGroup>
            <Button CommandName="cmdNew" />
            <Button CommandName="cmdOpen" />
            <Button CommandName="cmdSave" />
            <Button CommandName="cmdSaveAs" />
          </MenuGroup>
          <MenuGroup>
            <Button CommandName="cmdExit" />
          </MenuGroup>
        </ApplicationMenu>
      </Ribbon.ApplicationMenu>
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar>
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdSave" />
            <Button CommandName="cmdUndo" />
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
      <Ribbon.Tabs>
        <Tab>
          <Group CommandName="grpClipboard" SizeDefinition="FourButtons">
            <Button CommandName="cmdPaste" />
            <Button CommandName="cmdCut" />
            <Button CommandName="cmdCopy" />
            <Button CommandName="cmdDelete" />
          </Group>
        </Tab>
        <Tab>
          <Group CommandName="grpView" SizeDefinition="OneButton">
            <Button CommandName="cmdZoom" />
          </Group>
        </Tab>
      </Ribbon.Tabs>
    </Ribbon>
  </Application.Views>

</Application>
```



Pour éviter de redéfinir des symboles définis par une infrastructure d’interface utilisateur telle que MFC, l’exemple précédent utilise des noms de symboles légèrement différents pour chaque commande (fichier d’ID \_ \_ nouveau et ID \_ cmd \_ New). Toutefois, l’ID numérique affecté à chaque commande doit rester le même.

Pour intégrer le fichier de balisage dans une application, configurez une étape de génération personnalisée pour exécuter le compilateur de balisage du ruban, UICC.exe. L’en-tête et les fichiers de ressources qui en résultent sont ensuite incorporés dans le projet existant. Si l’exemple d’application de ruban de l’éditeur de texte est nommé « RibbonPad », une ligne de commande de génération personnalisée semblable à la suivante est requise :


```
UICC.exe res\RibbonPad_ribbon.xml res\RibbonPad_ribbon.bin 
         /header:res\RibbonPad_ribbon.h /res:res\RibbonPad_ribbon.rc2
```



Le compilateur de balisage crée un fichier binaire, un fichier d’en-tête (H) et un fichier de ressources (RC). Étant donné que l’application existante a probablement un fichier RC existant, incluez les fichiers. RC et RC générés dans ce fichier RC, comme indiqué dans l’exemple suivant :


```C++
#ifndef APSTUDIO_INVOKED
/////////////////////////////////////////////////////////////////////////////
//
// Generated from the TEXTINCLUDE 3 resource.
//

#define _AFX_NO_SPLITTER_RESOURCES
#define _AFX_NO_OLE_RESOURCES
#define _AFX_NO_TRACKER_RESOURCES
#define _AFX_NO_PROPERTY_RESOURCES

#if !defined(AFX_RESOURCE_DLL) || defined(AFX_TARG_ENU)
LANGUAGE 9, 1
#pragma code_page(1252)

#include "res\RibbonPad_ribbon.h"  // Ribbon resources
#include "res\RibbonPad_ribbon.rc2"  // Ribbon resources

#include "res\RibbonPad.rc2"  // non-Microsoft Visual C++ edited resources
#include "afxres.rc"    // Standard components
#include "afxprint.rc"  // printing/print preview resources
#endif
#endif    // not APSTUDIO_INVOKED
```



### <a name="replace-legacy-menus-and-toolbars"></a>Remplacer les menus et les barres d’outils hérités

Le remplacement des menus et barres d’outils standard par un ruban dans une application héritée requiert les éléments suivants :

1.  Supprimez les références de ressource de menu et de barre d’outils du fichier de ressources de l’application.
2.  Supprimez tout le code d’initialisation de la barre d’outils et de la barre de menus.
3.  Supprimez tout code utilisé pour attacher une barre d’outils ou une barre de menus à la fenêtre de niveau supérieur de l’application.
4.  Instanciez l’infrastructure du ruban.
5.  Attachez le ruban à la fenêtre de niveau supérieur de l’application.
6.  Chargez le balisage compilé.

> [!IMPORTANT]
> La barre d’État et les tables de raccourcis clavier existantes doivent être conservées, car l’infrastructure du ruban ne remplace pas ces fonctionnalités.

 

L’exemple suivant montre comment initialiser l’infrastructure à l’aide de [**IUIFramework :: Initialize**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-initialize):


```C++
int CMainFrame::OnCreate(LPCREATESTRUCT lpCreateStruct)
{
    if (CFrameWnd::OnCreate(lpCreateStruct) == -1)
        return -1;
    
    if (!m_RibbonBar.Create(this, WS_CHILD|WS_DISABLED|WS_VISIBLE|CBRS_TOP|CBRS_HIDE_INPLACE,0))
        return -1;      // fail to create

    if (!m_wndStatusBar.Create(this) || !m_wndStatusBar.SetIndicators(indicators,sizeof(indicators)/sizeof(UINT)))
        return -1;      // fail to create

    // Ribbon initialization
    InitRibbon(this, &m_spUIFramework);

    return 0;
}
```



L’exemple suivant montre comment utiliser [**IUIFramework :: LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) pour charger le balisage compilé :


```C++
HRESULT InitRibbon(CMainFrame* pMainFrame, IUnknown** ppFramework)
{
    // Create the IUIFramework instance.
    CComPtr<IUIFramework> spFramework;
    HRESULT hr = ::CoCreateInstance(CLSID_UIRibbonFramework, NULL, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&spFramework));
    if (FAILED(hr))
        return hr;
    
    // Instantiate the CApplication object.
    CComObject<CApplication>* pApplication;
    hr = CComObject<CApplication>::CreateInstance(&pApplication);   // Refcount is 0
    
    // Call AddRef on the CApplication object. The smart pointer will release the refcount when it is out of scope.
    CComPtr< CComObject<CApplication> > spApplication(pApplication);

    if (FAILED(hr))
        return hr;

    // Initialize and load the Ribbon.
    spApplication->Initialize(pMainFrame);

    hr = spFramework->Initialize(*pMainFrame, spApplication);
    if (FAILED(hr))
        return hr;

    hr = spFramework->LoadUI(GetModuleHandle(NULL), L"APPLICATION_RIBBON");
    if (FAILED(hr))
        return hr;

    // Return IUIFramework interface to the caller.
    hr = spFramework->QueryInterface(ppFramework);

    return hr;
}
```



La classe CApplication, référencée ci-dessus, doit implémenter une paire d’interfaces COM (Component Object Model) définies par l’infrastructure du ruban : [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) et [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler).

[**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) fournit l’interface de rappel principale entre l’infrastructure et l’application (par exemple, la hauteur du ruban est communiquée par le biais de [**IUIApplication :: OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged)), tandis que les rappels pour les commandes individuelles sont fournis en réponse à [**IUIApplication :: OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand).

**Conseil :** Certaines infrastructures d’application, telles que MFC, requièrent que la hauteur de la barre de ruban soit prise en compte lors du rendu de l’espace de document de l’application. Dans ce cas, l’ajout d’une fenêtre masquée pour superposer la barre du ruban et forcer l’espace du document à la hauteur souhaitée est nécessaire. Pour obtenir un exemple de cette approche, où une fonction de disposition est appelée en fonction de la hauteur du ruban retournée par la méthode [**IUIRibbon :: GetHeight**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-getheight) , consultez l' [exemple HTMLEditRibbon](windowsribbon-htmleditribbonsample.md).

L’exemple de code suivant illustre une implémentation de [**IUIApplication :: OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged) :


```C++
// This is the Ribbon implementation that is done by an application.
// Applications have to implement IUIApplication and IUICommandHandler to set up communication with the Windows Ribbon.
class CApplication
    : public CComObjectRootEx<CComSingleThreadModel>
    , public IUIApplication
    , public IUICommandHandler
{
public:

    BEGIN_COM_MAP(CApplication)
        COM_INTERFACE_ENTRY(IUIApplication)
        COM_INTERFACE_ENTRY(IUICommandHandler)
    END_COM_MAP()

    CApplication() : _pMainFrame(NULL)
    {
    }

    void Initialize(CMainFrame* pFrame)
    {
        // Hold a reference to the main frame.
        _pMainFrame = pFrame;
    }

    void FinalRelease()
    {
        // Release the reference.
        _pMainFrame = NULL;
        __super::FinalRelease();
    }

    STDMETHOD(OnViewChanged)(UINT32 nViewID, __in UI_VIEWTYPE typeID, __in IUnknown* pView, UI_VIEWVERB verb, INT32 uReasonCode)
    {
        HRESULT hr;

        // The Ribbon size has changed.
        if (verb == UI_VIEWVERB_SIZE)
        {
            CComQIPtr<IUIRibbon> pRibbon = pView;
            if (!pRibbon)
                return E_FAIL;

            UINT ulRibbonHeight;
            // Get the Ribbon height.
            hr = pRibbon->GetHeight(&ulRibbonHeight);
            if (FAILED(hr))
                return hr;

            // Update the Ribbon bar so that the main frame can recalculate the child layout.
            _pMainFrame->m_RibbonBar.SetRibbonHeight(ulRibbonHeight);
            _pMainFrame->RecalcLayout();
        }

        return S_OK;
    }

    STDMETHOD(OnCreateUICommand)(UINT32 nCmdID, 
                               __in UI_COMMANDTYPE typeID,
                               __deref_out IUICommandHandler** ppCommandHandler)
    {
        // This application uses one command handler for all ribbon commands.
        return QueryInterface(IID_PPV_ARGS(ppCommandHandler));
    }

    STDMETHOD(OnDestroyUICommand)(UINT32 commandId, __in UI_COMMANDTYPE typeID,  __in_opt  IUICommandHandler *commandHandler)
    {        
        return E_NOTIMPL;
    }

private:
    CMainFrame* _pMainFrame;
};
```



### <a name="implement-an-iuicommandhandler-adapter"></a>Implémenter un adaptateur IUICommandHandler

Selon la conception de l’application d’origine, il peut être plus facile d’avoir plusieurs implémentations de gestionnaire de commandes, ou un gestionnaire de commandes de pontage unique qui appelle la logique de commande d’application existante. De nombreuses applications utilisent \_ des messages de commande WM à cet effet, où il suffit de fournir un gestionnaire de commandes unique et polyvalent qui transfère simplement les \_ messages de commande WM à la fenêtre de niveau supérieur.

Toutefois, cette approche nécessite un traitement spécial pour les commandes telles que **Exit** ou **Close**. Étant donné que le ruban ne peut pas être détruit pendant qu’il traite un message de fenêtre, le \_ message WM Close doit être publié dans le thread d’interface utilisateur de l’application et ne doit pas être traité de façon synchrone, comme illustré dans l’exemple suivant :


```C++
// User action callback, with transient execution parameters.
    STDMETHODIMP Execute(UINT nCmdID,
        UI_EXECUTIONVERB verb, 
        __in_opt const PROPERTYKEY* key,
        __in_opt const PROPVARIANT* ppropvarValue,
        __in_opt IUISimplePropertySet* pCommandExecutionProperties)
    {       
        switch(nCmdID)
        {
        case cmdExit:
            ::PostMessage(*_pMainFrame, WM_CLOSE, nCmdID, 0);
            break;
        default:
            ::SendMessage(*_pMainFrame, WM_COMMAND, nCmdID, 0);
        }
        return S_OK;
    }

    STDMETHODIMP UpdateProperty(UINT32 nCmdID, 
                                __in REFPROPERTYKEY key,
                                __in_opt  const PROPVARIANT *currentValue,
                                __out PROPVARIANT *newValue) 
    {        
        return S_OK;
    }

```



## <a name="migrating-resources"></a>Migration des ressources

Quand le manifeste des commandes a été défini, que la structure du ruban a été déclarée et que le code de l’application est adapté pour héberger l’infrastructure du ruban, la dernière étape consiste à spécifier des ressources de type chaîne et image pour chaque commande.

> [!Note]  
> Les ressources de type chaîne et image sont généralement fournies dans le fichier de balisage. Toutefois, elles peuvent être générées ou remplacées par programme en implémentant la méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

 

### <a name="string-resources"></a>Ressources de chaînes

[**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) est la propriété de chaîne la plus courante définie pour une commande. Ils sont rendus sous la forme d’étiquettes de texte pour les onglets, les groupes et les contrôles individuels. Une chaîne d’étiquette d’un élément de menu hérité peut généralement être réutilisée pour une **commande. LabelTitle** sans modification importante.

Toutefois, les conventions suivantes ont été modifiées avec l’avènement du ruban :

-   Le suffixe des points de suspension (...), utilisé pour indiquer une commande de lancement de dialogue, n’est plus nécessaire.
-   La esperluette (&) peut toujours être utilisée pour indiquer un raccourci clavier pour une commande qui s’affiche dans un menu, mais la propriété [**Command. KeyTip**](windowsribbon-element-command-keytip.md) prise en charge par l’infrastructure respecte un objectif similaire.

En vous référant à l’exemple d’éditeur de texte, les chaînes suivantes pour LabelTitle et KeyTip peuvent être spécifiées :



| Symbole           | Chaîne d’origine | Chaîne LabelTitle | Chaîne de KeyTip |
|------------------|-----------------|-------------------|---------------|
| fichier d’ID \_ \_ nouveau    | &nouveau            | &nouveau              | N             |
| \_enregistrement du fichier d’ID \_   | &enregistrer           | &enregistrer             | S             |
| \_enregistrement du fichier d’ID \_ | Enregistrer &sous...       | Enregistrer &sous          | A             |
| fichier d’ID \_ \_ ouvert   | &ouvrir...          | &amp;Open             | O             |
| \_sortie du fichier d’ID \_   | &Quitter           | &Quitter             | X             |
| \_annuler la modification de l’ID \_   | &annuler           | Annuler              | Z             |
| modifier l’ID \_ \_ couper    | Cu&t            | Cu&t              | X             |
| copier l’ID \_ \_   | Copie &           | Copie &             | C             |
| édition de l’ID- \_ \_ coller  | &coller          | &coller            | V             |
| modification d’ID \_ \_ Effacer  | &supprimer         | &supprimer           | D             |
| ZOOM de la vue d’ID \_ \_   | &zoom...          | Zoom              | Z             |



 

Voici une liste d’autres propriétés de chaîne qui doivent être définies sur la plupart des commandes :

-   [**Commande. LabelDescription**](windowsribbon-element-command-labeldescription.md)
-   [**Commande. TooltipTitle**](windowsribbon-element-command-tooltiptitle.md)
-   [**Commande. TooltipDescription**](windowsribbon-element-command-tooltipdescription.md)

Les onglets, les groupes et les autres fonctionnalités de l’interface utilisateur du ruban peuvent désormais être déclarés avec toutes les ressources de chaîne et d’image spécifiées.

L’exemple de balisage de ruban suivant illustre différentes ressources de type chaîne :


```C++
<Application.Commands>
    <!-- Tabs -->
    <Command Name="tabHome" LabelTitle="Home" Keytip="H" />
    <Command Name="tabView" LabelTitle="View" Keytip="V" />

    <!-- Groups -->
    <Command Name="grpClipboard" LabelTitle="Clipboard" />
    <Command Name="grpZoom" LabelTitle="Zoom" />

    <!-- App menu commands -->
    <Command Name="cmdNew" Id="0xE100" Symbol="ID_CMD_NEW" LabelTitle="New document" Keytip="N" >
      <Command.TooltipTitle>New (Ctrl+N)</Command.TooltipTitle>
      <Command.TooltipDescription>Create a new document.</Command.TooltipDescription>
    </Command>
    <Command Name="cmdSave" Id="0xE103" Symbol="ID_CMD_SAVE" LabelTitle="Save" Keytip="S">
      <Command.TooltipTitle>Save (Ctrl+S)</Command.TooltipTitle>
      <Command.TooltipDescription>Save the current document.</Command.TooltipDescription>
    </Command>
    <Command Name="cmdSaveAs" Id="0xE104" Symbol="ID_CMD_SAVEAS" LabelTitle="Save as" Keytip="A">
      <Command.TooltipDescription>Save the current document with a new name.</Command.TooltipDescription>
    </Command>
    <Command Name="cmdOpen" Id="0xE101" Symbol="ID_CMD_OPEN" LabelTitle="Open" Keytip="O">
      <Command.TooltipTitle>Open (Ctrl+O)</Command.TooltipTitle>
      <Command.TooltipDescription>Open a document.</Command.TooltipDescription>
    </Command>
    <Command Name="cmdExit" Id="0xE102" Symbol="ID_CMD_EXIT" LabelTitle="Exit" Keytip="X">
      <Command.TooltipDescription>Exit the application.</Command.TooltipDescription>
    </Command>

    <!-- ...other commands -->

  </Application.Commands>
```



### <a name="image-resources"></a>Ressources d’image

L’infrastructure du ruban prend en charge les formats d’image qui offrent une apparence beaucoup plus riche que les formats d’image pris en charge par les composants de menu et de barre d’outils précédents.

pour Windows 8 et versions ultérieures, l’infrastructure du ruban prend en charge les formats graphiques suivants : fichiers BMP (bitmaps) 32 bits et fichiers PNG (Portable Network graphics) avec transparence.

pour Windows 7 et les versions antérieures, les ressources d’image doivent être conformes au format graphique BMP standard utilisé dans Windows.

> [!Note]  
> Les fichiers image existants peuvent être convertis dans l’un ou l’autre format. Toutefois, les résultats peuvent être moins satisfaisants si les fichiers image ne prennent pas en charge l’anticrénelage et la transparence.

 

Il n’est pas possible de spécifier une taille par défaut unique pour les ressources d’image dans l’infrastructure du ruban. Toutefois, pour prendre en charge la [disposition adaptative](windowsribbon-templates.md) des contrôles, les images peuvent être spécifiées en deux tailles (grande et petite). Toutes les images de l’infrastructure du ruban sont mises à l’échelle en fonction de la résolution en points par pouce (dpi) de l’affichage avec la taille de rendu exacte dépendante de ce paramètre PPP. Pour plus d’informations, consultez [spécification des ressources d’image du ruban](windowsribbon-imageformats.md) .

L’exemple suivant montre comment un ensemble d’images spécifiques à PPP est référencé dans le balisage :


```C++
<Command Name="cmdNew" Id="0xE100" Symbol="ID_CMD_NEW" LabelTitle="New document" Keytip="N" >
      <Command.TooltipTitle>New (Ctrl+N)</Command.TooltipTitle>
      <Command.TooltipDescription>Create a new document.</Command.TooltipDescription>
      <Command.LargeImages>
        <Image Source="cmdNew-32px.png" MinDPI="96" />
        <Image Source="cmdNew-40px.png" MinDPI="120" />
        <Image Source="cmdNew-48px.png" MinDPI="144" />
        <Image Source="cmdNew-64px.png" MinDPI="192" />
      </Command.LargeImages>
      <Command.SmallImages>
        <Image Source="cmdNew-16px.png" MinDPI="96" />
        <Image Source="cmdNew-20px.png" MinDPI="120" />
        <Image Source="cmdNew-24px.png" MinDPI="144" />
        <Image Source="cmdNew-32px.png" MinDPI="192" />
      </Command.SmallImages>
    </Command>
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification des ressources d’image du ruban](windowsribbon-imageformats.md)
</dt> </dl>

 

 