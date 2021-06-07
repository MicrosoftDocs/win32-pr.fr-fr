---
title: Élément QuickAccessToolbar
description: Représente la barre d’outils accès rapide (QAT), une petite barre d’outils qui affiche des raccourcis vers les commandes du ruban.
ms.assetid: 59aa35c3-a844-46b3-b066-c9a321fb0891
keywords:
- Ruban des fenêtres d’élément QuickAccessToolbar
topic_type:
- apiref
api_name:
- QuickAccessToolbar
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6ae01f620d66298a5f7200d0be947dbfb3750af4
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443300"
---
# <a name="quickaccesstoolbar-element"></a><span data-ttu-id="3aa1b-104">Élément QuickAccessToolbar</span><span class="sxs-lookup"><span data-stu-id="3aa1b-104">QuickAccessToolbar element</span></span>

<span data-ttu-id="3aa1b-105">Représente la [barre d’outils accès rapide (qat)](windowsribbon-controls-quickaccesstoolbar.md), une petite barre d’outils qui affiche des raccourcis vers les commandes du ruban.</span><span class="sxs-lookup"><span data-stu-id="3aa1b-105">Represents the [Quick Access Toolbar (QAT)](windowsribbon-controls-quickaccesstoolbar.md), a small toolbar that displays shortcuts to Ribbon Commands.</span></span>

## <a name="usage"></a><span data-ttu-id="3aa1b-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="3aa1b-106">Usage</span></span>

``` syntax
<QuickAccessToolbar
  CommandName = "xs:positiveInteger or xs:string"
  CustomizeCommandName = "xs:positiveInteger or xs:string">
  child elements
</QuickAccessToolbar>
```

## <a name="attributes"></a><span data-ttu-id="3aa1b-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="3aa1b-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3aa1b-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="3aa1b-108">Attribute</span></span></th>
<th><span data-ttu-id="3aa1b-109">Type</span><span class="sxs-lookup"><span data-stu-id="3aa1b-109">Type</span></span></th>
<th><span data-ttu-id="3aa1b-110">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="3aa1b-110">Required</span></span></th>
<th><span data-ttu-id="3aa1b-111">Description</span><span class="sxs-lookup"><span data-stu-id="3aa1b-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3aa1b-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="3aa1b-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="3aa1b-113">XS : positiveInteger ou XS : String</span><span class="sxs-lookup"><span data-stu-id="3aa1b-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="3aa1b-114">Non</span><span class="sxs-lookup"><span data-stu-id="3aa1b-114">No</span></span><br/></td>
<td><span data-ttu-id="3aa1b-115">Associe l’élément à une <a href="windowsribbon-element-command.md"><strong>commande</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="3aa1b-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="3aa1b-116">
<dt><span></span><span></span><strong></strong> (XS : positiveInteger ou XS : String)</span><span class="sxs-lookup"><span data-stu-id="3aa1b-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="3aa1b-117">Chaîne, valeur entière comprise entre 2 et 59999, inclusive, ou valeur hexadécimale comprise entre 0X2 et 0xea5f inclus.</span><span class="sxs-lookup"><span data-stu-id="3aa1b-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="3aa1b-118">La valeur doit être unique dans le document XML du ruban.</span><span class="sxs-lookup"><span data-stu-id="3aa1b-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="3aa1b-119">Longueur maximale : 100 caractères.</span><span class="sxs-lookup"><span data-stu-id="3aa1b-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3aa1b-120"><strong>CustomizeCommandName</strong></span><span class="sxs-lookup"><span data-stu-id="3aa1b-120"><strong>CustomizeCommandName</strong></span></span><br/></td>
<td><span data-ttu-id="3aa1b-121">XS : positiveInteger ou XS : String</span><span class="sxs-lookup"><span data-stu-id="3aa1b-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="3aa1b-122">Non</span><span class="sxs-lookup"><span data-stu-id="3aa1b-122">No</span></span><br/></td>
<td><span data-ttu-id="3aa1b-123">Insère un élément de commande supplémentaire dans le menu QAT.</span><span class="sxs-lookup"><span data-stu-id="3aa1b-123">Inserts an additional Command item in the QAT menu.</span></span><br/> <br/><span data-ttu-id="3aa1b-124">
<dt><span></span><span></span><strong></strong> (XS : positiveInteger ou XS : String)</span><span class="sxs-lookup"><span data-stu-id="3aa1b-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <img src="images/markup/qat-customizecommandname.png" alt="Screen shot of a QAT menu with the More commands... Command item." /><br/> <span data-ttu-id="3aa1b-125">Chaîne, valeur entière comprise entre 2 et 59999, inclusive, ou valeur hexadécimale comprise entre 0X2 et 0xea5f inclus.</span><span class="sxs-lookup"><span data-stu-id="3aa1b-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="3aa1b-126">La valeur doit être unique dans le document XML du ruban.</span><span class="sxs-lookup"><span data-stu-id="3aa1b-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="3aa1b-127">Longueur maximale : 100 caractères.</span><span class="sxs-lookup"><span data-stu-id="3aa1b-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="3aa1b-128">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="3aa1b-128">Child elements</span></span>



| <span data-ttu-id="3aa1b-129">Élément</span><span class="sxs-lookup"><span data-stu-id="3aa1b-129">Element</span></span>                                                                                                                   | <span data-ttu-id="3aa1b-130">Description</span><span class="sxs-lookup"><span data-stu-id="3aa1b-130">Description</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="3aa1b-131">**QuickAccessToolbar.ApplicationDefaults**</span><span class="sxs-lookup"><span data-stu-id="3aa1b-131">**QuickAccessToolbar.ApplicationDefaults**</span></span>](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)<br/> | <span data-ttu-id="3aa1b-132">Peut se produire au plus une fois</span><span class="sxs-lookup"><span data-stu-id="3aa1b-132">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="3aa1b-133">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="3aa1b-133">Parent elements</span></span>



| <span data-ttu-id="3aa1b-134">Élément</span><span class="sxs-lookup"><span data-stu-id="3aa1b-134">Element</span></span>                                                                                         |
|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3aa1b-135">**Ruban. QuickAccessToolbar**</span><span class="sxs-lookup"><span data-stu-id="3aa1b-135">**Ribbon.QuickAccessToolbar**</span></span>](windowsribbon-element-ribbon-quickaccesstoolbar.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="3aa1b-136">Remarques</span><span class="sxs-lookup"><span data-stu-id="3aa1b-136">Remarks</span></span>

<span data-ttu-id="3aa1b-137">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="3aa1b-137">Required.</span></span>

<span data-ttu-id="3aa1b-138">Doit se produire une seule fois pour chaque [**ruban. QuickAccessToolbar**](windowsribbon-element-ribbon-quickaccesstoolbar.md).</span><span class="sxs-lookup"><span data-stu-id="3aa1b-138">Must occur exactly once for each [**Ribbon.QuickAccessToolbar**](windowsribbon-element-ribbon-quickaccesstoolbar.md).</span></span>

<span data-ttu-id="3aa1b-139">Les éléments du QAT peuvent être ajoutés ou supprimés au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="3aa1b-139">Items in the QAT can be added or removed at run time.</span></span>

<span data-ttu-id="3aa1b-140">Pour garantir la cohérence entre les applications du ruban, il est recommandé que le gestionnaire de commandes *CustomizeCommandName* lance une boîte de dialogue de personnalisation qat.</span><span class="sxs-lookup"><span data-stu-id="3aa1b-140">For consistency across Ribbon applications, it is recommended that the *CustomizeCommandName* Command handler launch a QAT customization dialog.</span></span>

## <a name="examples"></a><span data-ttu-id="3aa1b-141">Exemples</span><span class="sxs-lookup"><span data-stu-id="3aa1b-141">Examples</span></span>

<span data-ttu-id="3aa1b-142">L’exemple suivant illustre le balisage de base pour **QuickAccessToolbar**.</span><span class="sxs-lookup"><span data-stu-id="3aa1b-142">The following example demonstrates the basic markup for the **QuickAccessToolbar**.</span></span>

<span data-ttu-id="3aa1b-143">Cette section de code affiche la déclaration de commande **QuickAccessToolbar** .</span><span class="sxs-lookup"><span data-stu-id="3aa1b-143">This section of code shows the **QuickAccessToolbar** Command declaration.</span></span>


```XML
<Command Name="cmdQAT"
         Symbol="ID_QAT"
         Id="40000"/>
<Command Name="cmdCustomizeQAT"
         Symbol="ID_CUSTOM_QAT"
         Id="40001"/>
```



<span data-ttu-id="3aa1b-144">Cette section de code illustre la déclaration de contrôle **QuickAccessToolbar** .</span><span class="sxs-lookup"><span data-stu-id="3aa1b-144">This section of code shows the **QuickAccessToolbar** control declaration.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="3aa1b-145">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="3aa1b-145">Element information</span></span>

* <span data-ttu-id="3aa1b-146">**Système minimal pris en charge**: Windows 7</span><span class="sxs-lookup"><span data-stu-id="3aa1b-146">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="3aa1b-147">**Peut être vide**: non</span><span class="sxs-lookup"><span data-stu-id="3aa1b-147">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="3aa1b-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3aa1b-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3aa1b-149">Contrôle de barre d’outils accès rapide</span><span class="sxs-lookup"><span data-stu-id="3aa1b-149">Quick Access Toolbar control</span></span>](windowsribbon-controls-quickaccesstoolbar.md)
</dt> </dl>

 

 





