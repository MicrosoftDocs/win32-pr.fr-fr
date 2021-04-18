---
title: Élément ApplicationMenu
description: Représente le menu de l’application. | Élément ApplicationMenu
ms.assetid: 815e0462-ea45-44b1-81bf-f5797b22e920
keywords:
- Ruban des fenêtres d’élément ApplicationMenu
topic_type:
- apiref
api_name:
- ApplicationMenu
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a02193b4c3e61b4b8cf2f129619969f6a82a84ac
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104211526"
---
# <a name="applicationmenu-element"></a><span data-ttu-id="f890e-105">Élément ApplicationMenu</span><span class="sxs-lookup"><span data-stu-id="f890e-105">ApplicationMenu element</span></span>

<span data-ttu-id="f890e-106">Représente le [menu](windowsribbon-controls-applicationmenu.md)de l’application.</span><span class="sxs-lookup"><span data-stu-id="f890e-106">Represents the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>

## <a name="usage"></a><span data-ttu-id="f890e-107">Utilisation</span><span class="sxs-lookup"><span data-stu-id="f890e-107">Usage</span></span>

``` syntax
<ApplicationMenu
  CommandName = "xs:positiveInteger or xs:string"
>
  child elements
</ApplicationMenu>
```

## <a name="attributes"></a><span data-ttu-id="f890e-108">Attributs</span><span class="sxs-lookup"><span data-stu-id="f890e-108">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f890e-109">Attribut</span><span class="sxs-lookup"><span data-stu-id="f890e-109">Attribute</span></span></th>
<th><span data-ttu-id="f890e-110">Type</span><span class="sxs-lookup"><span data-stu-id="f890e-110">Type</span></span></th>
<th><span data-ttu-id="f890e-111">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="f890e-111">Required</span></span></th>
<th><span data-ttu-id="f890e-112">Description</span><span class="sxs-lookup"><span data-stu-id="f890e-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f890e-113"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="f890e-113"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="f890e-114">XS : positiveInteger ou XS : String</span><span class="sxs-lookup"><span data-stu-id="f890e-114">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="f890e-115">Non</span><span class="sxs-lookup"><span data-stu-id="f890e-115">No</span></span><br/></td>
<td><span data-ttu-id="f890e-116">Associe l’élément à une <a href="windowsribbon-element-command.md"><strong>commande</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="f890e-116">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="f890e-117">
<dt><span></span><span></span><strong></strong> (XS : positiveInteger ou XS : String)</span><span class="sxs-lookup"><span data-stu-id="f890e-117">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="f890e-118">Chaîne, valeur entière comprise entre 2 et 59999, inclusive, ou valeur hexadécimale comprise entre 0X2 et 0xea5f inclus.</span><span class="sxs-lookup"><span data-stu-id="f890e-118">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="f890e-119">La valeur doit être unique dans le document XML du ruban.</span><span class="sxs-lookup"><span data-stu-id="f890e-119">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="f890e-120">Longueur maximale : 100 caractères.</span><span class="sxs-lookup"><span data-stu-id="f890e-120">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="f890e-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="f890e-121">Child elements</span></span>



| <span data-ttu-id="f890e-122">Élément</span><span class="sxs-lookup"><span data-stu-id="f890e-122">Element</span></span>                                                                                             | <span data-ttu-id="f890e-123">Description</span><span class="sxs-lookup"><span data-stu-id="f890e-123">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="f890e-124">**ApplicationMenu.RecentItems**</span><span class="sxs-lookup"><span data-stu-id="f890e-124">**ApplicationMenu.RecentItems**</span></span>](windowsribbon-element-applicationmenu-recentitems.md)<br/> | <span data-ttu-id="f890e-125">Peut se produire au plus une fois</span><span class="sxs-lookup"><span data-stu-id="f890e-125">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="f890e-126">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="f890e-126">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                                     | <span data-ttu-id="f890e-127">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="f890e-127">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="f890e-128">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="f890e-128">Parent elements</span></span>



| <span data-ttu-id="f890e-129">Élément</span><span class="sxs-lookup"><span data-stu-id="f890e-129">Element</span></span>                                                                                   |
|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f890e-130">**Ruban. ApplicationMenu**</span><span class="sxs-lookup"><span data-stu-id="f890e-130">**Ribbon.ApplicationMenu**</span></span>](windowsribbon-element-ribbon-applicationmenu.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="f890e-131">Notes</span><span class="sxs-lookup"><span data-stu-id="f890e-131">Remarks</span></span>

<span data-ttu-id="f890e-132">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="f890e-132">Required.</span></span>

<span data-ttu-id="f890e-133">Doit se produire une seule fois pour chaque [**ruban. ApplicationMenu**](windowsribbon-element-ribbon-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="f890e-133">Must occur exactly once for each [**Ribbon.ApplicationMenu**](windowsribbon-element-ribbon-applicationmenu.md).</span></span>

<span data-ttu-id="f890e-134">Les éléments enfants de l’élément **ApplicationMenu** doivent se produire dans l’ordre spécifié :</span><span class="sxs-lookup"><span data-stu-id="f890e-134">The child elements of the **ApplicationMenu** element must occur in the specified order:</span></span>

1.  [<span data-ttu-id="f890e-135">**ApplicationMenu.RecentItems**</span><span class="sxs-lookup"><span data-stu-id="f890e-135">**ApplicationMenu.RecentItems**</span></span>](windowsribbon-element-applicationmenu-recentitems.md)
2.  [<span data-ttu-id="f890e-136">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="f890e-136">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)

## <a name="examples"></a><span data-ttu-id="f890e-137">Exemples</span><span class="sxs-lookup"><span data-stu-id="f890e-137">Examples</span></span>

<span data-ttu-id="f890e-138">L’exemple suivant illustre le balisage de base pour le menu de l' [application](windowsribbon-controls-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="f890e-138">The following example demonstrates the basic markup for the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>

<span data-ttu-id="f890e-139">Cette section de code montre les déclarations de commande **ApplicationMenu** .</span><span class="sxs-lookup"><span data-stu-id="f890e-139">This section of code shows the **ApplicationMenu** Command declarations.</span></span>


```XML
<!-- Command declarations for the Application Menu. -->
<Command Name="cmdFileMenu"
         Symbol="ID_FILE_MENU"
         Id="25000" />
<!-- Command declaration for most recently used items. -->
<Command Name="cmdMRUItems"
         Symbol="ID_FILE_MRUITEMS"
         Id="25050"/>
<!-- Command declarations for Application Menu items. -->
<Command Name="cmdNew"
         Symbol="ID_FILE_NEW"
         Comment="New"
         Id="25001"
         LabelTitle="&amp;New"/>
<Command Name="cmdOpen"
         Symbol="ID_FILE_OPEN"
         Comment="Open"
         Id="25002"
         LabelTitle="&amp;&amp;Open"/>
<Command>
  <Command.Name>cmdSave</Command.Name>
  <Command.Symbol>ID_FILE_SAVE</Command.Symbol>
  <Command.Comment>Save</Command.Comment>
  <Command.Id>25003</Command.Id>
  <Command.LabelTitle>
    <String>
      <String.Content>Label for Save</String.Content>
      <String.Id>59999</String.Id>
      <String.Symbol>strSave</String.Symbol>
    </String>
  </Command.LabelTitle>
  <Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
  <Command.TooltipDescription>Tooltip description for Save Command.</Command.TooltipDescription>
  <Command.Keytip>s1</Command.Keytip>
</Command>
<Command Name="cmdPrint"
         Symbol="ID_FILE_PRINT"
         Comment="Save"
         Id="25004"
         LabelTitle="Print" />
<Command Name="cmdExit"
         Symbol="ID_FILE_EXIT"
         Comment="Exit"
         Id="25005"
         LabelTitle="Exit" />
```



<span data-ttu-id="f890e-140">Cette section de code montre les déclarations de contrôle **ApplicationMenu** .</span><span class="sxs-lookup"><span data-stu-id="f890e-140">This section of code shows the **ApplicationMenu** control declarations.</span></span>


```XML
<!-- Control declarations for Application Menu items. -->
<Ribbon.ApplicationMenu>
  <ApplicationMenu CommandName="cmdFileMenu">
    <!-- Most recently used items collection. -->
    <ApplicationMenu.RecentItems>
      <RecentItems CommandName="cmdMRUItems"/>
    </ApplicationMenu.RecentItems>
    <!-- Menu items collection. -->
    <MenuGroup>
      <Button CommandName="cmdNew" />
      <Button CommandName="cmdOpen" />
      <Button CommandName="cmdSave" />
    </MenuGroup>
    <MenuGroup>
      <Button CommandName="cmdPrint" />
      <Button CommandName="cmdExit" />
    </MenuGroup>
  </ApplicationMenu>
</Ribbon.ApplicationMenu>
```



## <a name="element-information"></a><span data-ttu-id="f890e-141">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="f890e-141">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="f890e-142">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f890e-142">Minimum supported system</span></span><br/> | <span data-ttu-id="f890e-143">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f890e-143">Windows 7</span></span> |
| <span data-ttu-id="f890e-144">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="f890e-144">Can be empty</span></span>                        | <span data-ttu-id="f890e-145">Non</span><span class="sxs-lookup"><span data-stu-id="f890e-145">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="f890e-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f890e-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f890e-147">Contrôle de menu de l’application</span><span class="sxs-lookup"><span data-stu-id="f890e-147">Application Menu control</span></span>](windowsribbon-controls-applicationmenu.md)
</dt> </dl>

 

 





