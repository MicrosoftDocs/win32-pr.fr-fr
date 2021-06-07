---
title: Élément TabGroup
description: Représente un ensemble contextuel de contrôles onglet.
ms.assetid: f131efe1-b8c4-416e-997a-5e2d3bcc03ea
keywords:
- Ruban des fenêtres d’élément TabGroup
topic_type:
- apiref
api_name:
- TabGroup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a4c18db72d6b0161842bfde9d5a836d14189c6a
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444060"
---
# <a name="tabgroup-element"></a><span data-ttu-id="ec0f3-104">Élément TabGroup</span><span class="sxs-lookup"><span data-stu-id="ec0f3-104">TabGroup element</span></span>

<span data-ttu-id="ec0f3-105">Représente un ensemble contextuel de contrôles [onglet](windowsribbon-controls-tabgroup.md) .</span><span class="sxs-lookup"><span data-stu-id="ec0f3-105">Represents a contextual set of [Tab](windowsribbon-controls-tabgroup.md) controls.</span></span>

## <a name="usage"></a><span data-ttu-id="ec0f3-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="ec0f3-106">Usage</span></span>

``` syntax
<TabGroup
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</TabGroup>
```

## <a name="attributes"></a><span data-ttu-id="ec0f3-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="ec0f3-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ec0f3-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="ec0f3-108">Attribute</span></span></th>
<th><span data-ttu-id="ec0f3-109">Type</span><span class="sxs-lookup"><span data-stu-id="ec0f3-109">Type</span></span></th>
<th><span data-ttu-id="ec0f3-110">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="ec0f3-110">Required</span></span></th>
<th><span data-ttu-id="ec0f3-111">Description</span><span class="sxs-lookup"><span data-stu-id="ec0f3-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ec0f3-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="ec0f3-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="ec0f3-113">XS : positiveInteger ou XS : String</span><span class="sxs-lookup"><span data-stu-id="ec0f3-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="ec0f3-114">Non</span><span class="sxs-lookup"><span data-stu-id="ec0f3-114">No</span></span><br/></td>
<td><span data-ttu-id="ec0f3-115">Associe l’élément à une <a href="windowsribbon-element-command.md"><strong>commande</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="ec0f3-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="ec0f3-116">
<dt><span></span><span></span><strong></strong> (XS : positiveInteger ou XS : String)</span><span class="sxs-lookup"><span data-stu-id="ec0f3-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="ec0f3-117">Chaîne, valeur entière comprise entre 2 et 59999, inclusive, ou valeur hexadécimale comprise entre 0X2 et 0xea5f inclus.</span><span class="sxs-lookup"><span data-stu-id="ec0f3-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="ec0f3-118">La valeur doit être unique dans le document XML du ruban.</span><span class="sxs-lookup"><span data-stu-id="ec0f3-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="ec0f3-119">Longueur maximale : 100 caractères.</span><span class="sxs-lookup"><span data-stu-id="ec0f3-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="ec0f3-120">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ec0f3-120">Child elements</span></span>



| <span data-ttu-id="ec0f3-121">Élément</span><span class="sxs-lookup"><span data-stu-id="ec0f3-121">Element</span></span>                                             | <span data-ttu-id="ec0f3-122">Description</span><span class="sxs-lookup"><span data-stu-id="ec0f3-122">Description</span></span>                                     |
|-----------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="ec0f3-123">**/**</span><span class="sxs-lookup"><span data-stu-id="ec0f3-123">**Tab**</span></span>](windowsribbon-element-tab.md)<br/> | <span data-ttu-id="ec0f3-124">Doit se produire au moins une fois</span><span class="sxs-lookup"><span data-stu-id="ec0f3-124">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="ec0f3-125">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="ec0f3-125">Parent elements</span></span>



| <span data-ttu-id="ec0f3-126">Élément</span><span class="sxs-lookup"><span data-stu-id="ec0f3-126">Element</span></span>                                                                                 |
|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="ec0f3-127">**Ruban. ContextualTabs**</span><span class="sxs-lookup"><span data-stu-id="ec0f3-127">**Ribbon.ContextualTabs**</span></span>](windowsribbon-element-ribbon-contextualtabs.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="ec0f3-128">Remarques</span><span class="sxs-lookup"><span data-stu-id="ec0f3-128">Remarks</span></span>

<span data-ttu-id="ec0f3-129">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="ec0f3-129">Required.</span></span>

<span data-ttu-id="ec0f3-130">Doit se produire au moins une fois pour chaque élément [**Ribbon. ContextualTabs**](windowsribbon-element-ribbon-contextualtabs.md) .</span><span class="sxs-lookup"><span data-stu-id="ec0f3-130">Must occur at least once for each [**Ribbon.ContextualTabs**](windowsribbon-element-ribbon-contextualtabs.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="ec0f3-131">Exemples</span><span class="sxs-lookup"><span data-stu-id="ec0f3-131">Examples</span></span>

<span data-ttu-id="ec0f3-132">L’exemple suivant illustre le balisage de base pour l’élément **TabGroup** .</span><span class="sxs-lookup"><span data-stu-id="ec0f3-132">The following example demonstrates the basic markup for the **TabGroup** element.</span></span>

<span data-ttu-id="ec0f3-133">Cette section de code illustre une déclaration de commande **TabGroup** avec deux onglets contextuels.</span><span class="sxs-lookup"><span data-stu-id="ec0f3-133">This section of code shows a **TabGroup** Command declaration with two contextual tabs.</span></span>


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



<span data-ttu-id="ec0f3-134">Cette section de code montre les déclarations de contrôle **TabGroup** correspondantes.</span><span class="sxs-lookup"><span data-stu-id="ec0f3-134">This section of code shows corresponding **TabGroup** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="ec0f3-135">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="ec0f3-135">Element information</span></span>

- <span data-ttu-id="ec0f3-136">**Système minimal pris en charge**: Windows 7</span><span class="sxs-lookup"><span data-stu-id="ec0f3-136">**Minimum supported system**: Windows 7</span></span> 
- <span data-ttu-id="ec0f3-137">**Peut être vide**: non</span><span class="sxs-lookup"><span data-stu-id="ec0f3-137">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="ec0f3-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec0f3-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec0f3-139">Contrôle de groupe d’onglets</span><span class="sxs-lookup"><span data-stu-id="ec0f3-139">Tab Group control</span></span>](windowsribbon-controls-tabgroup.md)
</dt> <dt>

[<span data-ttu-id="ec0f3-140">Contrôle Tab</span><span class="sxs-lookup"><span data-stu-id="ec0f3-140">Tab control</span></span>](windowsribbon-controls-tab.md)
</dt> </dl>

 

 





