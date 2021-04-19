---
title: Élément HelpButton
description: Représente le contrôle de bouton d’aide.
ms.assetid: 24c709da-539e-4ea0-bd3e-d3fbd72dfb97
keywords:
- Ruban des fenêtres d’élément HelpButton
topic_type:
- apiref
api_name:
- HelpButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5be084ff6fc92d4eac4bbaffb3c507142f91eba8
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2020
ms.locfileid: "106511270"
---
# <a name="helpbutton-element"></a><span data-ttu-id="7afe0-104">Élément HelpButton</span><span class="sxs-lookup"><span data-stu-id="7afe0-104">HelpButton element</span></span>

<span data-ttu-id="7afe0-105">Représente le contrôle de [bouton d’aide](windowsribbon-controls-helpbutton.md) .</span><span class="sxs-lookup"><span data-stu-id="7afe0-105">Represents the [Help Button](windowsribbon-controls-helpbutton.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="7afe0-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="7afe0-106">Usage</span></span>

``` syntax
<HelpButton
  CommandName = "xs:positiveInteger or xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="7afe0-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="7afe0-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7afe0-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="7afe0-108">Attribute</span></span></th>
<th><span data-ttu-id="7afe0-109">Type</span><span class="sxs-lookup"><span data-stu-id="7afe0-109">Type</span></span></th>
<th><span data-ttu-id="7afe0-110">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="7afe0-110">Required</span></span></th>
<th><span data-ttu-id="7afe0-111">Description</span><span class="sxs-lookup"><span data-stu-id="7afe0-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7afe0-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="7afe0-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="7afe0-113">XS : positiveInteger ou XS : String</span><span class="sxs-lookup"><span data-stu-id="7afe0-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="7afe0-114">Non</span><span class="sxs-lookup"><span data-stu-id="7afe0-114">No</span></span><br/></td>
<td><span data-ttu-id="7afe0-115">Associe l’élément à une <a href="windowsribbon-element-command.md"><strong>commande</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="7afe0-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="7afe0-116">
<dt><span></span><span></span><strong></strong> (XS : positiveInteger ou XS : String)</span><span class="sxs-lookup"><span data-stu-id="7afe0-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="7afe0-117">Chaîne, valeur entière comprise entre 2 et 59999, inclusive, ou valeur hexadécimale comprise entre 0X2 et 0xea5f inclus.</span><span class="sxs-lookup"><span data-stu-id="7afe0-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="7afe0-118">La valeur doit être unique dans le document XML du ruban.</span><span class="sxs-lookup"><span data-stu-id="7afe0-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="7afe0-119">Longueur maximale : 100 caractères.</span><span class="sxs-lookup"><span data-stu-id="7afe0-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="7afe0-120">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="7afe0-120">Child elements</span></span>

<span data-ttu-id="7afe0-121">Il n’y a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="7afe0-121">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="7afe0-122">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="7afe0-122">Parent elements</span></span>



| <span data-ttu-id="7afe0-123">Élément</span><span class="sxs-lookup"><span data-stu-id="7afe0-123">Element</span></span>                                                                         |
|---------------------------------------------------------------------------------|
| [<span data-ttu-id="7afe0-124">**Ruban. HelpButton**</span><span class="sxs-lookup"><span data-stu-id="7afe0-124">**Ribbon.HelpButton**</span></span>](windowsribbon-element-ribbon-helpbutton.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="7afe0-125">Notes</span><span class="sxs-lookup"><span data-stu-id="7afe0-125">Remarks</span></span>

<span data-ttu-id="7afe0-126">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="7afe0-126">Optional.</span></span>

<span data-ttu-id="7afe0-127">Peut se produire au plus une fois pour chaque [**ruban. HelpButton**](windowsribbon-element-ribbon-helpbutton.md).</span><span class="sxs-lookup"><span data-stu-id="7afe0-127">May occur at most once for each [**Ribbon.HelpButton**](windowsribbon-element-ribbon-helpbutton.md).</span></span>

<span data-ttu-id="7afe0-128">Ouvre une boîte de dialogue d’aide sur l’application lorsque vous cliquez dessus.</span><span class="sxs-lookup"><span data-stu-id="7afe0-128">Launches an application help dialog box when clicked.</span></span>

## <a name="examples"></a><span data-ttu-id="7afe0-129">Exemples</span><span class="sxs-lookup"><span data-stu-id="7afe0-129">Examples</span></span>

<span data-ttu-id="7afe0-130">L’exemple suivant illustre le balisage de base requis pour implémenter un contrôle de [bouton d’aide](windowsribbon-controls-helpbutton.md) du ruban.</span><span class="sxs-lookup"><span data-stu-id="7afe0-130">The following example demonstrates the basic markup that is required to implement a Ribbon [Help Button](windowsribbon-controls-helpbutton.md) control.</span></span>

<span data-ttu-id="7afe0-131">Cette section de code affiche la déclaration de commande **HelpButton** .</span><span class="sxs-lookup"><span data-stu-id="7afe0-131">This section of code shows the **HelpButton** Command declaration.</span></span>


```XML
<Command Name="cmdHelp"
         Symbol="IDR_CMD_HELP">      
</Command>
```



<span data-ttu-id="7afe0-132">Cette section de code illustre la déclaration de contrôle **HelpButton** .</span><span class="sxs-lookup"><span data-stu-id="7afe0-132">This section of code shows the **HelpButton** control declaration.</span></span>


```XML
<Ribbon.HelpButton>
  <HelpButton CommandName="cmdHelp"/>
</Ribbon.HelpButton>
```



## <a name="element-information"></a><span data-ttu-id="7afe0-133">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="7afe0-133">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="7afe0-134">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7afe0-134">Minimum supported system</span></span><br/> | <span data-ttu-id="7afe0-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7afe0-135">Windows 7</span></span> |
| <span data-ttu-id="7afe0-136">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="7afe0-136">Can be empty</span></span>                        | <span data-ttu-id="7afe0-137">Oui</span><span class="sxs-lookup"><span data-stu-id="7afe0-137">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="7afe0-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7afe0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7afe0-139">Contrôle de bouton d’aide</span><span class="sxs-lookup"><span data-stu-id="7afe0-139">Help Button control</span></span>](windowsribbon-controls-helpbutton.md)
</dt> </dl>

 

 





