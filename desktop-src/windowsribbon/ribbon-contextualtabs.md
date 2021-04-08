---
title: Affichage des onglets contextuels
description: Dans une application de l’infrastructure de ruban Windows, un onglet contextuel est un contrôle onglet masqué qui est affiché dans la ligne d’onglet lorsqu’un objet dans l’espace de travail d’application, tel qu’une image, est sélectionné ou mis en surbrillance.
ms.assetid: 2059ca42-6a99-43a2-b1f5-ce5554156993
keywords:
- Ruban Windows, onglets contextuels
- Ruban, onglets contextuels
- affichage des onglets contextuels du ruban Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8a1e81ac6587e39a04114fa2f938a6da0e9a4d1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727365"
---
# <a name="displaying-contextual-tabs"></a><span data-ttu-id="02f7e-106">Affichage des onglets contextuels</span><span class="sxs-lookup"><span data-stu-id="02f7e-106">Displaying Contextual Tabs</span></span>

<span data-ttu-id="02f7e-107">Dans une application de l’infrastructure de ruban Windows, un onglet contextuel est un contrôle [onglet](windowsribbon-controls-tab.md) masqué qui est affiché dans la ligne d’onglet lorsqu’un objet dans l’espace de travail d’application, tel qu’une image, est sélectionné ou mis en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="02f7e-107">In a Windows Ribbon framework application, a contextual tab is a hidden [Tab](windowsribbon-controls-tab.md) control that is displayed in the tab row when an object in the application workspace, such as an image, is selected or highlighted.</span></span>

-   [<span data-ttu-id="02f7e-108">Introduction</span><span class="sxs-lookup"><span data-stu-id="02f7e-108">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="02f7e-109">Implémentation des onglets contextuels</span><span class="sxs-lookup"><span data-stu-id="02f7e-109">Implementing Contextual Tabs</span></span>](#implementing-contextual-tabs)
    -   [<span data-ttu-id="02f7e-110">balisage</span><span class="sxs-lookup"><span data-stu-id="02f7e-110">Markup</span></span>](#markup)
    -   [<span data-ttu-id="02f7e-111">Code</span><span class="sxs-lookup"><span data-stu-id="02f7e-111">Code</span></span>](#code)
-   [<span data-ttu-id="02f7e-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="02f7e-112">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="02f7e-113">Introduction</span><span class="sxs-lookup"><span data-stu-id="02f7e-113">Introduction</span></span>

<span data-ttu-id="02f7e-114">Contrairement aux onglets principaux, qui contiennent différentes commandes courantes qui sont pertinentes quel que soit le contexte de l’espace de travail, les onglets contextuels contiennent généralement une ou plusieurs commandes applicables à un objet sélectionné ou en surbrillance uniquement.</span><span class="sxs-lookup"><span data-stu-id="02f7e-114">In contrast to core tabs, which contain various common Commands that are relevant regardless of workspace context, contextual tabs typically contain one or more Commands that are applicable to a selected or highlighted object only.</span></span>

<span data-ttu-id="02f7e-115">Lorsqu’un objet est sélectionné ou mis en surbrillance dans l’espace de travail de l’application, le type et le contexte de l’objet peuvent nécessiter des commandes disparates qui n’effectuent pas d’organisation ou de sens fonctionnel sur un onglet contextuel. Dans ce cas, plusieurs onglets contextuels, qui sont contenus dans un [groupe d’onglets](windowsribbon-controls-tabgroup.md), peuvent être nécessaires.</span><span class="sxs-lookup"><span data-stu-id="02f7e-115">When an object is selected or highlighted in the application workspace, the type and context of the object might require disparate Commands that do not make organizational or functional sense on one contextual tab. In these cases, multiple contextual tabs, which are contained within a [Tab Group](windowsribbon-controls-tabgroup.md), may be required.</span></span> <span data-ttu-id="02f7e-116">Par exemple, la sélection d’une image contenue dans une cellule de tableau peut nécessiter deux onglets contextuels qui exposent les fonctionnalités de table et d’image.</span><span class="sxs-lookup"><span data-stu-id="02f7e-116">For example, selecting an image contained in a table cell might require two contextual tabs that expose both table and image functionality.</span></span>

> [!Note]  
> <span data-ttu-id="02f7e-117">Outre plusieurs onglets contextuels, l’infrastructure du ruban prend également en charge plusieurs contrôles de [groupe d’onglets](windowsribbon-controls-tabgroup.md) dans un ruban.</span><span class="sxs-lookup"><span data-stu-id="02f7e-117">In addition to multiple contextual tabs, the Ribbon framework also supports multiple [Tab Group](windowsribbon-controls-tabgroup.md) controls within a ribbon.</span></span>

 

<span data-ttu-id="02f7e-118">Lorsque vous affichez des onglets contextuels, l’infrastructure du ruban applique un ensemble de comportements de base qui incluent :</span><span class="sxs-lookup"><span data-stu-id="02f7e-118">When displaying contextual tabs, the Ribbon framework enforces a basic set of behaviors that include:</span></span>

-   <span data-ttu-id="02f7e-119">Les onglets contextuels sont positionnés dans l’ordre dans lequel ils sont déclarés et à droite des onglets centraux dans la ligne de l’onglet du ruban.</span><span class="sxs-lookup"><span data-stu-id="02f7e-119">Contextual tabs are positioned in the order they are declared and to the right of core tabs in the ribbon tab row.</span></span>
-   <span data-ttu-id="02f7e-120">Lorsque le ruban est redimensionné, les onglets sont mis à l’échelle et les étiquettes d’onglet sont tronquées en fonction de l’espace requis.</span><span class="sxs-lookup"><span data-stu-id="02f7e-120">When the ribbon is resized, tabs are scaled and tab labels are truncated as space requires.</span></span> <span data-ttu-id="02f7e-121">Toutefois, les onglets contextuels visibles reçoivent une priorité d’affichage plus élevée dans laquelle ils sont mis à l’échelle et tronqués en dernier.</span><span class="sxs-lookup"><span data-stu-id="02f7e-121">However, visible contextual tabs are given a higher display priority in which they are scaled and truncated last.</span></span>
-   <span data-ttu-id="02f7e-122">L’étiquette d’un [groupe d’onglets](windowsribbon-controls-tabgroup.md) s’affiche dans la barre de titre de l’application et s’étend sur tous les onglets contextuels associés.</span><span class="sxs-lookup"><span data-stu-id="02f7e-122">The label for a [Tab Group](windowsribbon-controls-tabgroup.md) is displayed in the application title bar and spans all associated contextual tabs.</span></span>
-   <span data-ttu-id="02f7e-123">Lorsque plusieurs contrôles de [groupe d’onglets](windowsribbon-controls-tabgroup.md) sont affichés en même temps, l’une des cinq couleurs uniques est assignée à l’arrière-plan de chaque groupe d’onglets dans la barre de titre de l’application.</span><span class="sxs-lookup"><span data-stu-id="02f7e-123">When multiple [Tab Group](windowsribbon-controls-tabgroup.md) controls are displayed at the same time, one of five unique colors is assigned to the background of each Tab Group in the application title bar.</span></span> <span data-ttu-id="02f7e-124">Cette couleur est également utilisée comme couleur de surbrillance pour les onglets contextuels dans le groupe d’onglets.</span><span class="sxs-lookup"><span data-stu-id="02f7e-124">This color is also used as a highlight color for the contextual tabs in the Tab Group.</span></span>
-   <span data-ttu-id="02f7e-125">L’affectation de couleur au [groupe d’onglets](windowsribbon-controls-tabgroup.md) est basée sur l’ordre dans lequel les éléments du groupe d’onglets sont déclarés dans le balisage.</span><span class="sxs-lookup"><span data-stu-id="02f7e-125">The [Tab Group](windowsribbon-controls-tabgroup.md) color assignment is based on the order the Tab Group elements are declared in markup.</span></span> <span data-ttu-id="02f7e-126">Les couleurs sont définies par l’infrastructure et ne peuvent pas être spécifiées par l’application.</span><span class="sxs-lookup"><span data-stu-id="02f7e-126">The colors are defined by the framework and cannot be specified by the application.</span></span>
-   <span data-ttu-id="02f7e-127">Les couleurs des [groupes d’onglets](windowsribbon-controls-tabgroup.md) définies par l’infrastructure peuvent être modifiées indirectement via les clés de propriété des [Propriétés du Framework](windowsribbon-reference-properties-framework.md) .</span><span class="sxs-lookup"><span data-stu-id="02f7e-127">The [Tab Group](windowsribbon-controls-tabgroup.md) colors defined by the framework can be modified indirectly through the [Framework Properties](windowsribbon-reference-properties-framework.md) property keys.</span></span> <span data-ttu-id="02f7e-128">Pour plus d’informations, consultez [Personnalisation des couleurs du ruban](ribbon-color.md).</span><span class="sxs-lookup"><span data-stu-id="02f7e-128">For more information, see [Customizing Ribbon Colors](ribbon-color.md).</span></span>
-   <span data-ttu-id="02f7e-129">Lorsque plus de cinq contrôles de [groupe d’onglets](windowsribbon-controls-tabgroup.md) sont affichés à un moment donné, le Framework effectue le cycle des couleurs associées.</span><span class="sxs-lookup"><span data-stu-id="02f7e-129">When more than five [Tab Group](windowsribbon-controls-tabgroup.md) controls are displayed at any single time, the framework cycles the associated colors.</span></span>
-   <span data-ttu-id="02f7e-130">Le nombre maximal de contrôles [onglet](windowsribbon-controls-tab.md) dans un ruban est limité à 100.</span><span class="sxs-lookup"><span data-stu-id="02f7e-130">The maximum number of [Tab](windowsribbon-controls-tab.md) controls in a ribbon is limited to 100.</span></span> <span data-ttu-id="02f7e-131">Cela comprend les onglets contextuels, visibles ou non.</span><span class="sxs-lookup"><span data-stu-id="02f7e-131">This includes contextual tabs, visible or not.</span></span>

<span data-ttu-id="02f7e-132">La capture d’écran suivante montre un onglet contextuel de Windows 7 Paint.</span><span class="sxs-lookup"><span data-stu-id="02f7e-132">The following screen shot shows a contextual tab from Windows 7 Paint.</span></span>

![capture d’écran qui montre un contrôle d’onglet contextuel.](images/controls/contextualtab.png)

## <a name="implementing-contextual-tabs"></a><span data-ttu-id="02f7e-134">Implémentation des onglets contextuels</span><span class="sxs-lookup"><span data-stu-id="02f7e-134">Implementing Contextual Tabs</span></span>

<span data-ttu-id="02f7e-135">Cette section présente les détails de l’implémentation des onglets contextuels du ruban et explique comment les incorporer dans une application de ruban.</span><span class="sxs-lookup"><span data-stu-id="02f7e-135">This section discusses the implementation details of Ribbon contextual tabs and walks through how to incorporate them in a Ribbon application.</span></span>

### <a name="markup"></a><span data-ttu-id="02f7e-136">balisage</span><span class="sxs-lookup"><span data-stu-id="02f7e-136">Markup</span></span>

<span data-ttu-id="02f7e-137">Les exemples suivants illustrent le balisage de base pour un élément [**TabGroup**](windowsribbon-element-tabgroup.md) qui contient deux onglets contextuels.</span><span class="sxs-lookup"><span data-stu-id="02f7e-137">The following examples demonstrate the basic markup for a [**TabGroup**](windowsribbon-element-tabgroup.md) element that contains two contextual tabs.</span></span>

<span data-ttu-id="02f7e-138">Cette section de code montre les déclarations de commande [**TabGroup**](windowsribbon-element-tabgroup.md) et [Tab](windowsribbon-controls-tab.md) .</span><span class="sxs-lookup"><span data-stu-id="02f7e-138">This section of code shows the [**TabGroup**](windowsribbon-element-tabgroup.md) and [Tab](windowsribbon-controls-tab.md) Command declarations.</span></span>


```XML
<!-- Contextual Tabs -->
<Command Name='cmdContextualTab1'
         LabelTitle='Contextual Tab 1'
         Symbol='ID_CONTEXTUALTAB1'/>
<Command Name='cmdContextualTab2'
         LabelTitle='Contextual Tab 2'
         Symbol='ID_CONTEXTUALTAB2'/>
<Command Name='cmdContextualTabGroup'
         LabelTitle='Contextual Tabs'
         Symbol='ID_CONTEXTUALTAB_GROUP'/>
```



<span data-ttu-id="02f7e-139">Cette section de code montre les déclarations de contrôle requises pour afficher deux onglets contextuels dans un [**TabGroup**](windowsribbon-element-tabgroup.md).</span><span class="sxs-lookup"><span data-stu-id="02f7e-139">This section of code shows the control declarations required to display two contextual tabs within a [**TabGroup**](windowsribbon-element-tabgroup.md).</span></span>


```XML
      <Ribbon.ContextualTabs>
        <TabGroup CommandName='cmdContextualTabGroup'>
          <Tab CommandName='cmdContextualTab1'>
            <!--InRibbonGallery Group-->
            <Group CommandName='cmdInRibbonGalleryGroup'
                   SizeDefinition='OneInRibbonGallery'>
              <InRibbonGallery CommandName='cmdTextSizeGallery3'
                               HasLargeItems='true'
                               ItemHeight='32'
                               ItemWidth='32'
                               MaxColumns='3' >
                <InRibbonGallery.MenuLayout>
                  <FlowMenuLayout Columns='3'
                                  Gripper ='Corner'/>
                </InRibbonGallery.MenuLayout>
              </InRibbonGallery>
            </Group>
            <!--Command Galleries Group-->
            <Group CommandName='cmdCommandGalleriesGroup'
                   SizeDefinition='OneInRibbonGallery'>
              <InRibbonGallery CommandName='cmdCommandGallery1'
                               Type='Commands'
                               MaxRows='3'
                               MaxColumns='3'>
                <InRibbonGallery.MenuLayout>
                  <FlowMenuLayout Columns='3'
                                  Gripper ='Corner'/>
                </InRibbonGallery.MenuLayout>
              </InRibbonGallery>
            </Group>
          </Tab>
          <Tab CommandName='cmdContextualTab2'></Tab>
        </TabGroup>
      </Ribbon.ContextualTabs> 
```



### <a name="code"></a><span data-ttu-id="02f7e-140">Code</span><span class="sxs-lookup"><span data-stu-id="02f7e-140">Code</span></span>

<span data-ttu-id="02f7e-141">[Interface utilisateur \_ Le \_ ContextAvailable](windowsribbon-reference-properties-uipkey-contextavailable.md) de la clé de serveur est la clé de propriété unique définie par l’infrastructure pour la spécification de la visibilité et de l’état des onglets contextuels.</span><span class="sxs-lookup"><span data-stu-id="02f7e-141">[UI\_PKEY\_ContextAvailable](windowsribbon-reference-properties-uipkey-contextavailable.md) is the single property key defined by the framework for specifying the visibility and state of contextual tabs.</span></span> <span data-ttu-id="02f7e-142">Lorsqu’un objet est sélectionné dans l’espace de travail d’application, l’une des trois valeurs de l’énumération [**\_ CONTEXTAVAILABILITY de l’interface utilisateur**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_contextavailability) peut être affectée à cette propriété, qui définit si un onglet contextuel existe et, le cas échéant, s’il est affiché sous la forme de l’onglet actif.</span><span class="sxs-lookup"><span data-stu-id="02f7e-142">When an object is selected in the application workspace, this property can be assigned one of three values from the [**UI\_CONTEXTAVAILABILITY**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_contextavailability) enumeration that define whether a contextual tab exists and, if it does, whether it is shown as the active tab.</span></span>

<span data-ttu-id="02f7e-143">Une application demande une mise à jour du [groupe d’onglets](windowsribbon-controls-tabgroup.md) en invalidant et en mettant à jour la propriété [ \_ \_ ContextAvailable de l’interface utilisateur](windowsribbon-reference-properties-uipkey-contextavailable.md) , lorsque le contexte de l’espace de travail change.</span><span class="sxs-lookup"><span data-stu-id="02f7e-143">An application requests a [Tab Group](windowsribbon-controls-tabgroup.md) update by invalidating and updating the [UI\_PKEY\_ContextAvailable](windowsribbon-reference-properties-uipkey-contextavailable.md) property when the workspace context changes.</span></span>

<span data-ttu-id="02f7e-144">Les sections suivantes du code montrent comment afficher un onglet contextuel quand une image est sélectionnée dans un espace de travail d’application.</span><span class="sxs-lookup"><span data-stu-id="02f7e-144">The follow sections of code demonstrate how to display a contextual tab when an image is selected in an application workspace.</span></span>


```C++
// Initialize the image tools contextual tab visibility setting.
UI_CONTEXTAVAILABILITY g_ImageTools = UI_CONTEXTAVAILABILITY_NOTAVAILABLE;

// Called when an image is selected in the application.
void SelectImage()
{
  ...
  g_ImageTools = UI_CONTEXTAVAILABILITY_ACTIVE;

  // Invalidate the UI_PKEY_ContextAvailable property of the image tools  
  // contextual tab Command and trigger the UpdatePropery callback function.
  pUIFramework->InvalidateUICommand(
                  cmdImageTabSet, 
                  UI_INVALIDATIONS_PROPERTY, 
                  UI_PKEY_ContextAvailable);
  ...
}

// Update Tab Group properties.
HRESULT MyTabGroupCommandHandler::UpdateProperty(
                                  UINT nCmdID,
                                  REFPROPERTYKEY key,
                                  const PROPVARIANT* ppropvarCurrentValue,
                                  PROPVARIANT* ppropvarNewValue)
{
  HRESULT hr = E_FAIL;

  if (key == UI_PKEY_ContextAvailable)
  {
    hr = UIInitPropertyFromUInt32(key, g_ImageTools, ppropvarNewValue);
  }
  ...
  return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="02f7e-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="02f7e-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02f7e-146">Instructions relatives à l’expérience utilisateur du ruban</span><span class="sxs-lookup"><span data-stu-id="02f7e-146">Ribbon User Experience Guidelines</span></span>](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[<span data-ttu-id="02f7e-147">Processus de conception du ruban</span><span class="sxs-lookup"><span data-stu-id="02f7e-147">Ribbon Design Process</span></span>](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

 

 