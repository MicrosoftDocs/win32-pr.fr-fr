---
title: Élément Spinner
description: Représente un contrôle Spinner.
ms.assetid: 6a174ec9-0fde-4171-a363-0e330ac31a8b
keywords:
- Ruban des fenêtres d’élément Spinner
topic_type:
- apiref
api_name:
- Spinner
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d1ec2e074271e125199ddfd4ff8fac7b2af80c33
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444810"
---
# <a name="spinner-element"></a><span data-ttu-id="fc5f5-104">Élément Spinner</span><span class="sxs-lookup"><span data-stu-id="fc5f5-104">Spinner element</span></span>

<span data-ttu-id="fc5f5-105">Représente un contrôle [Spinner](windowsribbon-controls-spinner.md) .</span><span class="sxs-lookup"><span data-stu-id="fc5f5-105">Represents a [Spinner](windowsribbon-controls-spinner.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="fc5f5-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="fc5f5-106">Usage</span></span>

``` syntax
<Spinner
  CommandName = "xs:positiveInteger or xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="fc5f5-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="fc5f5-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fc5f5-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="fc5f5-108">Attribute</span></span></th>
<th><span data-ttu-id="fc5f5-109">Type</span><span class="sxs-lookup"><span data-stu-id="fc5f5-109">Type</span></span></th>
<th><span data-ttu-id="fc5f5-110">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="fc5f5-110">Required</span></span></th>
<th><span data-ttu-id="fc5f5-111">Description</span><span class="sxs-lookup"><span data-stu-id="fc5f5-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fc5f5-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="fc5f5-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="fc5f5-113">XS : positiveInteger ou XS : String</span><span class="sxs-lookup"><span data-stu-id="fc5f5-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="fc5f5-114">Non</span><span class="sxs-lookup"><span data-stu-id="fc5f5-114">No</span></span><br/></td>
<td><span data-ttu-id="fc5f5-115">Associe l’élément à une <a href="windowsribbon-element-command.md"><strong>commande</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="fc5f5-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="fc5f5-116">
<dt><span></span><span></span><strong></strong> (XS : positiveInteger ou XS : String)</span><span class="sxs-lookup"><span data-stu-id="fc5f5-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="fc5f5-117">Chaîne, valeur entière comprise entre 2 et 59999, inclusive, ou valeur hexadécimale comprise entre 0X2 et 0xea5f inclus.</span><span class="sxs-lookup"><span data-stu-id="fc5f5-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="fc5f5-118">La valeur doit être unique dans le document XML du ruban.</span><span class="sxs-lookup"><span data-stu-id="fc5f5-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="fc5f5-119">Longueur maximale : 100 caractères.</span><span class="sxs-lookup"><span data-stu-id="fc5f5-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="fc5f5-120">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="fc5f5-120">Child elements</span></span>

<span data-ttu-id="fc5f5-121">Il n’y a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="fc5f5-121">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="fc5f5-122">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="fc5f5-122">Parent elements</span></span>



| <span data-ttu-id="fc5f5-123">Élément</span><span class="sxs-lookup"><span data-stu-id="fc5f5-123">Element</span></span>                                                                           |
|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="fc5f5-124">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="fc5f5-124">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>             |
| [<span data-ttu-id="fc5f5-125">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="fc5f5-125">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>       |
| [<span data-ttu-id="fc5f5-126">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="fc5f5-126">**Group**</span></span>](windowsribbon-element-group.md)<br/>                           |
| [<span data-ttu-id="fc5f5-127">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="fc5f5-127">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                   |
| [<span data-ttu-id="fc5f5-128">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="fc5f5-128">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="fc5f5-129">Remarques</span><span class="sxs-lookup"><span data-stu-id="fc5f5-129">Remarks</span></span>

<span data-ttu-id="fc5f5-130">facultatif.</span><span class="sxs-lookup"><span data-stu-id="fc5f5-130">Optional.</span></span>

<span data-ttu-id="fc5f5-131">Peut se produire une ou plusieurs fois pour chaque élément [**ControlGroup**](windowsribbon-element-controlgroup.md) ou [**Group**](windowsribbon-element-group.md) .</span><span class="sxs-lookup"><span data-stu-id="fc5f5-131">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md) or [**Group**](windowsribbon-element-group.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="fc5f5-132">Exemples</span><span class="sxs-lookup"><span data-stu-id="fc5f5-132">Examples</span></span>

<span data-ttu-id="fc5f5-133">L’exemple suivant illustre le balisage de base pour le [compteur](windowsribbon-controls-spinner.md).</span><span class="sxs-lookup"><span data-stu-id="fc5f5-133">The following example demonstrates the basic markup for the [Spinner](windowsribbon-controls-spinner.md).</span></span>

<span data-ttu-id="fc5f5-134">Cette section de code montre les déclarations de commande **Spinner** , avec un élément [**Group**](windowsribbon-element-group.md) qui fonctionne comme conteneur parent pour l’élément **Spinner** .</span><span class="sxs-lookup"><span data-stu-id="fc5f5-134">This section of code shows the **Spinner** Command declarations, with a [**Group**](windowsribbon-element-group.md) element that functions as the parent container for the **Spinner** element.</span></span>


```XML
<Command Name="GroupSpinner1" Symbol="IDR_CMD_GROUPSPINNER1" Id="30010">
  <Command.LabelTitle>
    <String Id="210">Resize</String>
  </Command.LabelTitle>
</Command>
<Command Name="Spinner_Size" Symbol="IDR_CMD_SPINNER_RESIZE" Id="30015">
  <Command.LabelTitle>
    <String Id="215">Resize by:</String>
  </Command.LabelTitle>
</Command>
```



<span data-ttu-id="fc5f5-135">Cette section de code montre les déclarations de contrôle **Spinner** .</span><span class="sxs-lookup"><span data-stu-id="fc5f5-135">This section of code shows the **Spinner** control declarations.</span></span>


```XML
<Group CommandName="GroupSpinner1">
  <Spinner CommandName="Spinner_Size" />
</Group>
```



## <a name="element-information"></a><span data-ttu-id="fc5f5-136">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="fc5f5-136">Element information</span></span>

- <span data-ttu-id="fc5f5-137">**Système minimal pris en charge**: Windows 7</span><span class="sxs-lookup"><span data-stu-id="fc5f5-137">**Minimum supported system**: Windows 7</span></span> 
- <span data-ttu-id="fc5f5-138">**Peut être vide**: Oui</span><span class="sxs-lookup"><span data-stu-id="fc5f5-138">**Can be empty**: Yes</span></span>



## <a name="see-also"></a><span data-ttu-id="fc5f5-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fc5f5-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc5f5-140">Spinner, contrôle</span><span class="sxs-lookup"><span data-stu-id="fc5f5-140">Spinner control</span></span>](windowsribbon-controls-spinner.md)
</dt> </dl>

 

 





