---
title: Barre d'outils Accès rapide
description: La barre d’outils accès rapide (QAT) est une petite barre d’outils personnalisable qui expose un ensemble de commandes spécifiées par l’application ou sélectionnées par l’utilisateur.
ms.assetid: b2adf4e9-0de1-4c4d-9293-693d0f7cf6fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20a50d562477e5c626d2d2bffa8ee5e0ecc84919
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031257"
---
# <a name="quick-access-toolbar"></a><span data-ttu-id="dbcb0-103">Barre d'outils Accès rapide</span><span class="sxs-lookup"><span data-stu-id="dbcb0-103">Quick Access Toolbar</span></span>

<span data-ttu-id="dbcb0-104">La barre d’outils accès rapide (QAT) est une petite barre d’outils personnalisable qui expose un ensemble de commandes spécifiées par l’application ou sélectionnées par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="dbcb0-104">The Quick Access Toolbar (QAT) is a small, customizable toolbar that exposes a set of Commands that are specified by the application or selected by the user.</span></span>

- [<span data-ttu-id="dbcb0-105">Introduction</span><span class="sxs-lookup"><span data-stu-id="dbcb0-105">Introduction</span></span>](#introduction)
- [<span data-ttu-id="dbcb0-106">Implémenter la barre d’outils accès rapide</span><span class="sxs-lookup"><span data-stu-id="dbcb0-106">Implement the Quick Access Toolbar</span></span>](#implement-the-quick-access-toolbar)
  - [<span data-ttu-id="dbcb0-107">balisage</span><span class="sxs-lookup"><span data-stu-id="dbcb0-107">Markup</span></span>](#markup)
  - [<span data-ttu-id="dbcb0-108">Code</span><span class="sxs-lookup"><span data-stu-id="dbcb0-108">Code</span></span>](#code)
- [<span data-ttu-id="dbcb0-109">Persistance de QAT</span><span class="sxs-lookup"><span data-stu-id="dbcb0-109">QAT Persistence</span></span>](#qat-persistence)
- [<span data-ttu-id="dbcb0-110">Propriétés de la barre d’outils accès rapide</span><span class="sxs-lookup"><span data-stu-id="dbcb0-110">Quick Access Toolbar Properties</span></span>](#quick-access-toolbar-properties)
- [<span data-ttu-id="dbcb0-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dbcb0-111">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="dbcb0-112">Introduction</span><span class="sxs-lookup"><span data-stu-id="dbcb0-112">Introduction</span></span>

<span data-ttu-id="dbcb0-113">Par défaut, la barre d’outils accès rapide (QAT) est située dans la barre de titre de la fenêtre d’application, mais elle peut être configurée pour s’afficher sous le ruban.</span><span class="sxs-lookup"><span data-stu-id="dbcb0-113">By default, the Quick Access Toolbar (QAT) is located in the title bar of the application window but can be configured to display below the ribbon.</span></span> <span data-ttu-id="dbcb0-114">En plus de l’exposition des commandes, la barre d’outils accès rapide (QAT) inclut également un menu déroulant personnalisable qui contient l’ensemble complet des commandes de la barre d’outils accès rapide (QAT) par défaut (masqué ou affiché dans la barre d’outils accès rapide) et un ensemble de la barre d’outils accès rapide (qat) et des options du ruban.</span><span class="sxs-lookup"><span data-stu-id="dbcb0-114">In addition to exposing Commands, the Quick Access Toolbar (QAT) also includes a customizable drop-down menu that contains the complete set of default Quick Access Toolbar (QAT) Commands (whether hidden or displayed in the Quick Access Toolbar (QAT)) and a set of Quick Access Toolbar (QAT) and ribbon options.</span></span>

<span data-ttu-id="dbcb0-115">La capture d’écran suivante montre un exemple de la barre d’outils accès rapide du ruban (QAT).</span><span class="sxs-lookup"><span data-stu-id="dbcb0-115">The following screen shot shows an example of the Ribbon Quick Access Toolbar (QAT).</span></span>

![capture d’écran du qat dans le ruban Microsoft Paint.](images/markup/qat-and-menu.png)

<span data-ttu-id="dbcb0-117">La barre d’outils accès rapide (QAT) est constituée d’une combinaison d’au plus 20 commandes spécifiées par l’application (appelée liste des valeurs par défaut de l’application) ou sélectionnées par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="dbcb0-117">The Quick Access Toolbar (QAT) consists of a combination of up to 20 Commands either specified by the application (known as the application defaults list) or selected by the user.</span></span> <span data-ttu-id="dbcb0-118">La barre d’outils accès rapide (QAT) peut contenir des commandes uniques qui ne sont pas disponibles ailleurs dans l’interface ruban.</span><span class="sxs-lookup"><span data-stu-id="dbcb0-118">The Quick Access Toolbar (QAT) can contain unique Commands that are not available elsewhere in the ribbon UI.</span></span>

> [!Note]
> <span data-ttu-id="dbcb0-119">Bien que presque tous les contrôles de ruban autorisent l’ajout de leur commande associée à la barre d’outils accès rapide (QAT) via le menu contextuel affiché dans la capture d’écran suivante, les commandes exposées dans une [fenêtre contextuelle de contexte](windowsribbon-controls-contextpopup.md) ne fournissent pas ce menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="dbcb0-119">While almost all ribbon controls allow their associated Command to be added to the Quick Access Toolbar (QAT) through the context menu shown in the following screen shot, Commands exposed in a [Context Popup](windowsribbon-controls-contextpopup.md) do not provide this context menu.</span></span>
>
> ![capture d’écran du menu contextuel de commande dans le ruban Microsoft Paint.](images/controls/qat-contextmenu-add.png) 

## <a name="implement-the-quick-access-toolbar"></a><span data-ttu-id="dbcb0-121">Implémenter la barre d’outils accès rapide</span><span class="sxs-lookup"><span data-stu-id="dbcb0-121">Implement the Quick Access Toolbar</span></span>

<span data-ttu-id="dbcb0-122">Comme avec tous les contrôles de l’infrastructure de ruban Windows, tirer pleinement parti de la barre d’outils accès rapide (QAT) nécessite un composant de balisage qui contrôle sa présentation dans le ruban et un composant de code qui régit ses fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="dbcb0-122">As with all Windows Ribbon framework controls, taking full advantage of the Quick Access Toolbar (QAT) requires both a markup component that controls its presentation within the ribbon and a code component that governs its functionality.</span></span>

### <a name="markup"></a><span data-ttu-id="dbcb0-123">balisage</span><span class="sxs-lookup"><span data-stu-id="dbcb0-123">Markup</span></span>

<span data-ttu-id="dbcb0-124">Le contrôle de la barre d’outils accès rapide (QAT) est déclaré et associé à un ID de commande, dans le balisage par le biais de l’élément [QuickAccessToolbar](windowsribbon-element-quickaccesstoolbar.md) .</span><span class="sxs-lookup"><span data-stu-id="dbcb0-124">The Quick Access Toolbar (QAT) control is declared, and associated with a Command ID, in markup through the [QuickAccessToolbar](windowsribbon-element-quickaccesstoolbar.md) element.</span></span> <span data-ttu-id="dbcb0-125">L’ID de commande est utilisé pour identifier et lier la barre d’outils accès rapide (QAT) à un gestionnaire de commandes défini par l’application.</span><span class="sxs-lookup"><span data-stu-id="dbcb0-125">The Command ID is used to identify and bind the Quick Access Toolbar (QAT) to a Command handler defined by the application.</span></span>

<span data-ttu-id="dbcb0-126">En plus du gestionnaire de commandes de base pour la fonctionnalité de la barre d’outils accès rapide principale (QAT), la déclaration de l’attribut facultatif de l’élément [QuickAccessToolbar](windowsribbon-element-quickaccesstoolbar.md) *CustomizeCommandName* fait que l’infrastructure ajoute un élément **commandes supplémentaires** à la liste des commandes du menu déroulant de la barre d’outils accès rapide (qat) qui requiert la définition d’un gestionnaire de commandes secondaire.</span><span class="sxs-lookup"><span data-stu-id="dbcb0-126">In addition to the basic Command handler for primary Quick Access Toolbar (QAT) functionality, declaring the optional *CustomizeCommandName* [QuickAccessToolbar](windowsribbon-element-quickaccesstoolbar.md) element attribute causes the framework to add a **More Commands** item to the Command list of the Quick Access Toolbar (QAT) drop-down menu that requires a secondary Command handler be defined.</span></span>

<span data-ttu-id="dbcb0-127">Pour assurer la cohérence entre les applications du ruban, il est recommandé que le gestionnaire de commandes *CustomizeCommandName* lance une boîte de dialogue de personnalisation de la barre d’outils accès rapide.</span><span class="sxs-lookup"><span data-stu-id="dbcb0-127">For consistency across Ribbon applications, it is recommended that the *CustomizeCommandName* Command handler launch a Quick Access Toolbar (QAT) customization dialog.</span></span> <span data-ttu-id="dbcb0-128">Étant donné que l’infrastructure de ruban fournit uniquement le point de lancement dans l’interface utilisateur, l’application est uniquement responsable de la mise en œuvre de la boîte de dialogue de personnalisation lorsque la notification de rappel pour cette commande est reçue.</span><span class="sxs-lookup"><span data-stu-id="dbcb0-128">Because the Ribbon framework only provides the launching point in the UI, the application is solely responsible for providing the customization dialog implementation when the callback notification for this Command is received.</span></span>

<span data-ttu-id="dbcb0-129">La capture d’écran suivante montre un menu déroulant de barre d’outils accès rapide (QAT) avec l’élément de commande **autres commandes** .</span><span class="sxs-lookup"><span data-stu-id="dbcb0-129">The following screen shot shows a Quick Access Toolbar (QAT) drop-down menu with the **More Commands** Command item.</span></span>

![capture d’écran d’un menu qat avec les commandes supplémentaires... élément de commande.](images/markup/qat-customizecommandname.png)

<span data-ttu-id="dbcb0-131">La liste des valeurs par défaut de l’application pour la barre d’outils accès rapide (QAT) est spécifiée par le biais de la propriété [QuickAccessToolbar. ApplicationDefaults](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) , qui identifie une liste par défaut des commandes recommandées, toutes répertoriées dans le menu déroulant de la barre d’outils accès rapide (qat).</span><span class="sxs-lookup"><span data-stu-id="dbcb0-131">The application defaults list for the Quick Access Toolbar (QAT) is specified through the [QuickAccessToolbar.ApplicationDefaults](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) property which identifies a default list of recommended Commands, all of which are listed in the Quick Access Toolbar (QAT) drop-down menu.</span></span>

<span data-ttu-id="dbcb0-132">Pour afficher les commandes à partir de la liste des valeurs par défaut de l’application dans la barre d’outils de la barre d’outils accès rapide (QAT), l’attribut *ApplicationDefaults. IsChecked* de chaque élément de contrôle doit avoir la valeur `true` .</span><span class="sxs-lookup"><span data-stu-id="dbcb0-132">To display Commands from the application defaults list in the Quick Access Toolbar (QAT) toolbar, the *ApplicationDefaults.IsChecked* attribute of each control element must have a value of `true`.</span></span> <span data-ttu-id="dbcb0-133">Les images précédentes montrent les résultats de la définition de cet attribut sur `true` pour les commandes **Enregistrer**, **Annuler** et **rétablir** .</span><span class="sxs-lookup"><span data-stu-id="dbcb0-133">The preceding images show the results of setting this attribute to `true` for the **Save**, **Undo**, and **Redo** Commands.</span></span>

<span data-ttu-id="dbcb0-134">[QuickAccessToolbar. ApplicationDefaults](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) prend en charge trois types de contrôles de ruban : [bouton](windowsribbon-controls-button.md), [bouton bascule](windowsribbon-controls-togglebutton.md)et case [à cocher](windowsribbon-controls-checkbox.md).</span><span class="sxs-lookup"><span data-stu-id="dbcb0-134">[QuickAccessToolbar.ApplicationDefaults](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) supports three types of Ribbon controls: [Button](windowsribbon-controls-button.md), [Toggle Button](windowsribbon-controls-togglebutton.md), and [Check Box](windowsribbon-controls-checkbox.md).</span></span>

> [!Note]
> <span data-ttu-id="dbcb0-135">Windows 8 et versions ultérieures : tous les contrôles basés sur la galerie sont pris en charge ([ComboBox](windowsribbon-element-combobox.md), [InRibbonGallery](windowsribbon-element-inribbongallery.md), [SplitButtonGallery](windowsribbon-element-splitbuttongallery.md)et [DropDownGallery](windowsribbon-element-dropdowngallery.md)).</span><span class="sxs-lookup"><span data-stu-id="dbcb0-135">Windows 8 and newer: All gallery-based controls are supported ([ComboBox](windowsribbon-element-combobox.md), [InRibbonGallery](windowsribbon-element-inribbongallery.md), [SplitButtonGallery](windowsribbon-element-splitbuttongallery.md), and [DropDownGallery](windowsribbon-element-dropdowngallery.md)).</span></span>
>
> <span data-ttu-id="dbcb0-136">Les éléments d’un contrôle Gallery peuvent prendre en charge la mise en surbrillance au pointage.</span><span class="sxs-lookup"><span data-stu-id="dbcb0-136">Items in a gallery control can support highlighting on hover.</span></span> <span data-ttu-id="dbcb0-137">Pour prendre en charge la mise en surbrillance au pointage, la Galerie doit être une galerie d’éléments et utiliser un [FlowMenuLayout](windowsribbon-element-flowmenulayout.md) de type [VerticalMenuLayout](windowsribbon-element-verticalmenulayout.md).</span><span class="sxs-lookup"><span data-stu-id="dbcb0-137">To support hover highlighting, the gallery must be an items gallery and use a [FlowMenuLayout](windowsribbon-element-flowmenulayout.md) of type [VerticalMenuLayout](windowsribbon-element-verticalmenulayout.md).</span></span>

<span data-ttu-id="dbcb0-138">L’exemple suivant illustre le balisage de base pour un élément [QuickAccessToolbar](windowsribbon-element-quickaccesstoolbar.md) .</span><span class="sxs-lookup"><span data-stu-id="dbcb0-138">The following example demonstrates the basic markup for a [QuickAccessToolbar](windowsribbon-element-quickaccesstoolbar.md) element.</span></span>

<span data-ttu-id="dbcb0-139">Cette section de code montre les déclarations de commande pour un élément de la [barre d’outils accès rapide (qat)](windowsribbon-element-quickaccesstoolbar.md) .</span><span class="sxs-lookup"><span data-stu-id="dbcb0-139">This section of code shows the Command declarations for a [Quick Access Toolbar (QAT)](windowsribbon-element-quickaccesstoolbar.md) element.</span></span>

```XML
<Command Name="cmdQAT"
         Symbol="ID_QAT"
         Id="40000"/>
<Command Name="cmdCustomizeQAT"
         Symbol="ID_CUSTOM_QAT"
         Id="40001"/>
```

<span data-ttu-id="dbcb0-140">Cette section de code montre les déclarations de contrôle pour un élément de la [barre d’outils accès rapide (qat)](windowsribbon-element-quickaccesstoolbar.md) .</span><span class="sxs-lookup"><span data-stu-id="dbcb0-140">This section of code shows the control declarations for a [Quick Access Toolbar (QAT)](windowsribbon-element-quickaccesstoolbar.md) element.</span></span>

```XML
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar CommandName="cmdQAT"
                            CustomizeCommandName="cmdCustomizeQAT">
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdButton1"/>
            <ToggleButton CommandName="cmdMinimize"
                          ApplicationDefaults.IsChecked="false"/>
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
```

### <a name="code"></a><span data-ttu-id="dbcb0-141">Code</span><span class="sxs-lookup"><span data-stu-id="dbcb0-141">Code</span></span>

<span data-ttu-id="dbcb0-142">L’application de l’infrastructure du ruban doit fournir une méthode de rappel du gestionnaire de commandes pour manipuler la barre d’outils accès rapide (QAT).</span><span class="sxs-lookup"><span data-stu-id="dbcb0-142">The Ribbon framework application must provide a Command handler callback method to manipulate the Quick Access Toolbar (QAT).</span></span> <span data-ttu-id="dbcb0-143">Ce gestionnaire fonctionne de la même façon que les gestionnaires de la bibliothèque de commandes, sauf que la barre d’outils accès rapide (QAT) ne prend pas en charge les catégories.</span><span class="sxs-lookup"><span data-stu-id="dbcb0-143">This handler works in a similar fashion to Command gallery handlers, except that the Quick Access Toolbar (QAT) does not support categories.</span></span> <span data-ttu-id="dbcb0-144">Pour plus d’informations, consultez [utilisation des galeries](ribbon-controls-galleries.md).</span><span class="sxs-lookup"><span data-stu-id="dbcb0-144">For more information, see [Working with Galleries](ribbon-controls-galleries.md).</span></span>

<span data-ttu-id="dbcb0-145">La collection de commandes de la barre d’outils accès rapide (QAT) est récupérée sous la forme d’un objet [IUICollection](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) via la clé de propriété [ \_ \_ ItemsSource de l’interface utilisateur](windowsribbon-reference-properties-uipkey-itemssource.md) .</span><span class="sxs-lookup"><span data-stu-id="dbcb0-145">The Quick Access Toolbar (QAT) Command collection is retrieved as an [IUICollection](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) object through the [UI\_PKEY\_ItemsSource](windowsribbon-reference-properties-uipkey-itemssource.md) property key.</span></span> <span data-ttu-id="dbcb0-146">L’ajout de commandes à la barre d’outils accès rapide (QAT) au moment de l’exécution s’effectue en ajoutant un objet [IUISimplePropertySet](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) à **IUICollection**.</span><span class="sxs-lookup"><span data-stu-id="dbcb0-146">Adding Commands to the Quick Access Toolbar (QAT) at run time is accomplished by adding an [IUISimplePropertySet](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) object to the **IUICollection**.</span></span>

<span data-ttu-id="dbcb0-147">Contrairement aux galeries de commandes, une propriété de type de commande ([UI de l’interface utilisateur \_ \_ CommandType](windowsribbon-reference-properties-uipkey-commandtype.md)) n’est pas requise pour l’objet [IUISimplePropertySet](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) de la barre d’outils accès rapide (qat).</span><span class="sxs-lookup"><span data-stu-id="dbcb0-147">Unlike Command galleries, a command type property ([UI\_PKEY\_CommandType](windowsribbon-reference-properties-uipkey-commandtype.md)) is not required for the Quick Access Toolbar (QAT) [IUISimplePropertySet](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) object.</span></span> <span data-ttu-id="dbcb0-148">Toutefois, la commande doit exister dans la liste des valeurs par défaut de l’application ruban ou barre d’outils accès rapide (QAT). Impossible de créer une nouvelle commande au moment de l’exécution et de l’ajouter à la barre d’outils accès rapide (QAT).</span><span class="sxs-lookup"><span data-stu-id="dbcb0-148">However, the Command must exist in the ribbon or Quick Access Toolbar (QAT) application defaults list; a new Command cannot be created at run time and added to the Quick Access Toolbar (QAT).</span></span>

> [!Note]  
> <span data-ttu-id="dbcb0-149">L’application ruban ne peut pas remplacer la barre d’outils accès rapide (QAT) [IUICollection](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) par un objet de collection personnalisé dérivé de IEnumUnknown.</span><span class="sxs-lookup"><span data-stu-id="dbcb0-149">The Ribbon application cannot replace the Quick Access Toolbar (QAT) [IUICollection](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) with a custom collection object derived from IEnumUnknown.</span></span>

<span data-ttu-id="dbcb0-150">L’exemple suivant illustre une implémentation du gestionnaire de commandes de la barre d’outils d’accès rapide (QAT) de base.</span><span class="sxs-lookup"><span data-stu-id="dbcb0-150">The following example demonstrates a basic Quick Access Toolbar (QAT) Command handler implementation.</span></span>

```C++
/* QAT COMMAND HANDLER IMPLEMENTATION */
class CQATCommandHandler
      : public CComObjectRootEx<CComMultiThreadModel>
      , public IUICommandHandler
{
  public:
    BEGIN_COM_MAP(CQATCommandHandler)
      COM_INTERFACE_ENTRY(IUICommandHandler)
    END_COM_MAP()

    // QAT command handler's Execute method
    STDMETHODIMP Execute(UINT nCmdID,
                         UI_EXECUTIONVERB verb, 
                         const PROPERTYKEY* key,
                         const PROPVARIANT* ppropvarValue,
                         IUISimplePropertySet* pCommandExecutionProperties)
    {
      UNREFERENCED_PARAMETER(nCmdID);
      UNREFERENCED_PARAMETER(verb);
      UNREFERENCED_PARAMETER(ppropvarValue);
      UNREFERENCED_PARAMETER(pCommandExecutionProperties);

      // Do not expect Execute callback for a QAT command
      return E_NOTIMPL;
    }

    // QAT command handler's UpdateProperty method
    STDMETHODIMP UpdateProperty(UINT nCmdID,
                                REFPROPERTYKEY key,
                                const PROPVARIANT* ppropvarCurrentValue,
                                PROPVARIANT* ppropvarNewValue)
    {
      UNREFERENCED_PARAMETER(nCmdID);
      UNREFERENCED_PARAMETER(ppropvarNewValue);

      HRESULT hr = E_NOTIMPL;

      if (key == UI_PKEY_ItemsSource)
      {
        ATLASSERT(ppropvarCurrentValue->vt == VT_UNKNOWN);

        CComQIPtr<IUICollection> spCollection(ppropvarCurrentValue->punkVal);

        UINT nCount;
        if (SUCCEEDED(hr = spCollection->GetCount(&nCount)))
        {
          if (nCount == 0)
          {
            // If the current Qat list is empty, then we will add a few items here.
            UINT commands[] =  { cmdSave, cmdUndo};

            int count = _countof(commands);

            for (int i = 0; i < count; i++)
            {
              PROPERTYKEY keys[1] = {UI_PKEY_CommandId};
              CComObject<CItemProperties> *pItem = NULL;
              if (SUCCEEDED(CComObject<CItemProperties>::CreateInstance(&pItem)))
              {
                PROPVARIANT vars[1];

                InitPropVariantFromUInt32(commands[i], &vars[0]);

                pItem->Initialize(NULL, _countof(vars), keys, vars);

                CComPtr<IUnknown> spUnknown;
                pItem->QueryInterface(&spUnknown);
                spCollection->Add(spUnknown);
                            
                FreePropVariantArray(_countof(vars), vars);
              }
            }
          }
          else
          {
            // Do nothing if the Qat list is not empty.
            // Return S_FALSE to indicate the callback succeeded.
            return S_FALSE; 
          }
        }
      }
    return hr;
  }
};
```

## <a name="qat-persistence"></a><span data-ttu-id="dbcb0-151">Persistance de QAT</span><span class="sxs-lookup"><span data-stu-id="dbcb0-151">QAT Persistence</span></span>

<span data-ttu-id="dbcb0-152">Les éléments et les paramètres de commande de la barre d’outils accès rapide (QAT) peuvent être rendus persistants entre les sessions d’application à l’aide des fonctions [IUIRibbon :: SaveSettingsToStream](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) et [IUIRibbon :: LoadSettingsFromStream](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) .</span><span class="sxs-lookup"><span data-stu-id="dbcb0-152">Quick Access Toolbar (QAT) Command items and settings can be persisted across application sessions using the [IUIRibbon::SaveSettingsToStream](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) and [IUIRibbon::LoadSettingsFromStream](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) functions.</span></span> <span data-ttu-id="dbcb0-153">Pour plus d’informations, consultez [persistance de l’état du ruban](ribbon-statepersistence.md).</span><span class="sxs-lookup"><span data-stu-id="dbcb0-153">For more information, see [Persisting Ribbon State](ribbon-statepersistence.md).</span></span>

## <a name="quick-access-toolbar-properties"></a><span data-ttu-id="dbcb0-154">Propriétés de la barre d’outils accès rapide</span><span class="sxs-lookup"><span data-stu-id="dbcb0-154">Quick Access Toolbar Properties</span></span>

<span data-ttu-id="dbcb0-155">L’infrastructure du ruban définit une collection de [clés de propriété](windowsribbon-reference-properties.md) pour le contrôle de la barre d’outils accès rapide (qat).</span><span class="sxs-lookup"><span data-stu-id="dbcb0-155">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Quick Access Toolbar (QAT) control.</span></span>

<span data-ttu-id="dbcb0-156">En règle générale, une propriété de la barre d’outils accès rapide (QAT) est mise à jour dans l’interface ruban en invalidant la commande associée au contrôle via un appel à la méthode [IUIFramework :: InvalidateUICommand](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="dbcb0-156">Typically, a Quick Access Toolbar (QAT) property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [IUIFramework::InvalidateUICommand](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="dbcb0-157">L’événement d’invalidation est géré, et les mises à jour de la propriété sont définies par la méthode de rappel [IUICommandHandler :: UpdateProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="dbcb0-157">The invalidation event is handled, and the property updates defined, by the [IUICommandHandler::UpdateProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="dbcb0-158">La méthode de rappel [IUICommandHandler :: UpdateProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) n’est pas exécutée et l’application a interrogé une valeur de propriété mise à jour, jusqu’à ce que la propriété soit requise par le Framework.</span><span class="sxs-lookup"><span data-stu-id="dbcb0-158">The [IUICommandHandler::UpdateProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="dbcb0-159">Par exemple, lorsqu’un onglet est activé et qu’un contrôle est affiché dans l’interface ruban, ou lorsqu’une info-bulle est affichée.</span><span class="sxs-lookup"><span data-stu-id="dbcb0-159">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="dbcb0-160">Dans certains cas, une propriété peut être récupérée par le biais de la méthode [IUIFramework :: GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) et définie avec la méthode [IUIFramework :: SetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="dbcb0-160">In some cases, a property can be retrieved through the [IUIFramework::GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [IUIFramework::SetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

<span data-ttu-id="dbcb0-161">Le tableau suivant répertorie les clés de propriété associées au contrôle de la barre d’outils accès rapide (QAT).</span><span class="sxs-lookup"><span data-stu-id="dbcb0-161">The following table lists the property keys that are associated with the Quick Access Toolbar (QAT) control.</span></span>

| <span data-ttu-id="dbcb0-162">Clé de propriété</span><span class="sxs-lookup"><span data-stu-id="dbcb0-162">Property Key</span></span> | <span data-ttu-id="dbcb0-163">Notes</span><span class="sxs-lookup"><span data-stu-id="dbcb0-163">Notes</span></span> |
|---|---|
| [<span data-ttu-id="dbcb0-164">IU de l’IU \_ \_</span><span class="sxs-lookup"><span data-stu-id="dbcb0-164">UI\_PKEY\_ItemsSource</span></span>](windowsribbon-reference-properties-uipkey-itemssource.md) | <span data-ttu-id="dbcb0-165">Prend en charge [IUIFramework :: GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) (ne prend pas en charge [IUIFramework :: SetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)). [IUIFramework :: GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) retourne un pointeur vers un objet IUICollection qui représente les commandes dans le qat.</span><span class="sxs-lookup"><span data-stu-id="dbcb0-165">Supports [IUIFramework::GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) (does not support [IUIFramework::SetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)).[IUIFramework::GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) returns a pointer to an IUICollection object that represents the commands in the QAT.</span></span> <span data-ttu-id="dbcb0-166">Chaque commande est identifiée par son ID de commande, qui est obtenu en appelant la méthode [IUISimplePropertySet :: GetValue](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) et en passant la clé de propriété de l' [interface utilisateur de l’interface utilisateur \_ \_ CommandID](windowsribbon-reference-properties-uipkey-commandid.md).</span><span class="sxs-lookup"><span data-stu-id="dbcb0-166">Each Command is identified by its Command ID, which is obtained by calling the [IUISimplePropertySet::GetValue](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) method and passing in the property key [UI\_PKEY\_CommandId](windowsribbon-reference-properties-uipkey-commandid.md).</span></span> |

<span data-ttu-id="dbcb0-167">Aucune clé de propriété n’est associée à l’élément de commande **autres commandes** du menu déroulant de la barre d’outils accès rapide (qat)</span><span class="sxs-lookup"><span data-stu-id="dbcb0-167">There are no property keys associated with the **More Commands** Command item of the Quick Access Toolbar (QAT) drop-down menu</span></span>

## <a name="related-topics"></a><span data-ttu-id="dbcb0-168">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dbcb0-168">Related topics</span></span>

- [<span data-ttu-id="dbcb0-169">Bibliothèque de contrôles de l’infrastructure du ruban Windows</span><span class="sxs-lookup"><span data-stu-id="dbcb0-169">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
- [<span data-ttu-id="dbcb0-170">Élément de balisage QuickAccessToolbar</span><span class="sxs-lookup"><span data-stu-id="dbcb0-170">QuickAccessToolbar markup element</span></span>](windowsribbon-element-quickaccesstoolbar.md)