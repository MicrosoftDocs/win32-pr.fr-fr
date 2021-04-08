---
title: Propriété Ribbon. ContextualTabs
description: Représente un conteneur pour les onglets contextuels.
ms.assetid: 1f57a8d7-97ac-4007-8a36-c6aec5b85e6c
keywords:
- Ruban de la propriété Ribbon. ContextualTabs
topic_type:
- apiref
api_name:
- Ribbon.ContextualTabs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 790a7c93df71ab5117b591367c6b80fc0f8a748d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740533"
---
# <a name="ribboncontextualtabs-property"></a><span data-ttu-id="69123-104">Propriété Ribbon. ContextualTabs</span><span class="sxs-lookup"><span data-stu-id="69123-104">Ribbon.ContextualTabs property</span></span>

<span data-ttu-id="69123-105">Représente un conteneur pour les onglets contextuels.</span><span class="sxs-lookup"><span data-stu-id="69123-105">Represents a container for contextual tabs.</span></span>

## <a name="usage"></a><span data-ttu-id="69123-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="69123-106">Usage</span></span>

``` syntax
<Ribbon.ContextualTabs>
  child elements
</Ribbon.ContextualTabs>
```

## <a name="attributes"></a><span data-ttu-id="69123-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="69123-107">Attributes</span></span>

<span data-ttu-id="69123-108">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="69123-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="69123-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="69123-109">Child elements</span></span>



| <span data-ttu-id="69123-110">Élément</span><span class="sxs-lookup"><span data-stu-id="69123-110">Element</span></span>                                                       | <span data-ttu-id="69123-111">Description</span><span class="sxs-lookup"><span data-stu-id="69123-111">Description</span></span>                                     |
|---------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="69123-112">**TabGroup**</span><span class="sxs-lookup"><span data-stu-id="69123-112">**TabGroup**</span></span>](windowsribbon-element-tabgroup.md)<br/> | <span data-ttu-id="69123-113">Doit se produire au moins une fois</span><span class="sxs-lookup"><span data-stu-id="69123-113">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="69123-114">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="69123-114">Parent elements</span></span>



| <span data-ttu-id="69123-115">Élément</span><span class="sxs-lookup"><span data-stu-id="69123-115">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="69123-116">**Ruban**</span><span class="sxs-lookup"><span data-stu-id="69123-116">**Ribbon**</span></span>](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="69123-117">Notes</span><span class="sxs-lookup"><span data-stu-id="69123-117">Remarks</span></span>

<span data-ttu-id="69123-118">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="69123-118">Optional.</span></span>

<span data-ttu-id="69123-119">Peut se produire au plus une fois pour chaque [**ruban**](windowsribbon-element-ribbon.md).</span><span class="sxs-lookup"><span data-stu-id="69123-119">May occur at most once for each [**Ribbon**](windowsribbon-element-ribbon.md).</span></span>

<span data-ttu-id="69123-120">Les onglets contextuels sont utiles pour afficher des fonctionnalités qui s’appliquent uniquement à un contexte d’application spécifique, tel qu’un onglet de mise en forme d’image dans un éditeur de texte qui s’affiche uniquement quand une image est mise en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="69123-120">Contextual tabs are useful for displaying functionality that is relevant only to a specific application context, such as an image formatting tab in a text editor that is displayed only when an image is highlighted.</span></span> <span data-ttu-id="69123-121">En général, les onglets contextuels ne sont pas visibles tant qu’un contexte d’application spécifique n’a pas été spécifié et que l’application notifie l’infrastructure du ruban.</span><span class="sxs-lookup"><span data-stu-id="69123-121">Typically, contextual tabs are not visible until a specific application context occurs, and the application notifies the Ribbon framework.</span></span>

<span data-ttu-id="69123-122">Quand ils sont affichés, les onglets contextuels sont codés par couleur pour les différencier des onglets normaux.</span><span class="sxs-lookup"><span data-stu-id="69123-122">When displayed, contextual tabs are color coded to differentiate them from regular tabs.</span></span>

## <a name="examples"></a><span data-ttu-id="69123-123">Exemples</span><span class="sxs-lookup"><span data-stu-id="69123-123">Examples</span></span>

<span data-ttu-id="69123-124">L’exemple suivant illustre le balisage de base pour l’élément **Ribbon. ContextualTabs** .</span><span class="sxs-lookup"><span data-stu-id="69123-124">The following example demonstrates the basic markup for the **Ribbon.ContextualTabs** element.</span></span>

<span data-ttu-id="69123-125">Cette section de code illustre une déclaration de commande [**TabGroup**](windowsribbon-element-tabgroup.md) et deux déclarations de commande d' [**onglet**](windowsribbon-element-tab.md) contextuelles.</span><span class="sxs-lookup"><span data-stu-id="69123-125">This section of code shows a [**TabGroup**](windowsribbon-element-tabgroup.md) Command declaration and two contextual [**Tab**](windowsribbon-element-tab.md) Command declarations.</span></span>


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



<span data-ttu-id="69123-126">Cette section de code illustre la déclaration de contrôle **Ribbon. ContextualTabs** avec un [**TabGroup**](windowsribbon-element-tabgroup.md) et deux contrôles d' [**onglet**](windowsribbon-element-tab.md) contextuels.</span><span class="sxs-lookup"><span data-stu-id="69123-126">This section of code shows the **Ribbon.ContextualTabs** control declaration with a [**TabGroup**](windowsribbon-element-tabgroup.md) and two contextual [**Tab**](windowsribbon-element-tab.md) controls.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="69123-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="69123-127">Requirements</span></span>



| <span data-ttu-id="69123-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="69123-128">Requirement</span></span> | <span data-ttu-id="69123-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="69123-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="69123-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="69123-130">Minimum supported client</span></span><br/> | <span data-ttu-id="69123-131">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="69123-131">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="69123-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="69123-132">Minimum supported server</span></span><br/> | <span data-ttu-id="69123-133">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="69123-133">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="69123-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69123-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69123-135">**Ruban. tabulations**</span><span class="sxs-lookup"><span data-stu-id="69123-135">**Ribbon.Tabs**</span></span>](windowsribbon-element-ribbon-tabs.md)
</dt> </dl>

 

 





