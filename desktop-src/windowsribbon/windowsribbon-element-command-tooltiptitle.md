---
title: Command. TooltipTitle, propriété
description: Représente un titre d’info-bulle.
ms.assetid: b06a7a6a-fbdd-464b-b804-e62912d6e176
keywords:
- Ruban Windows de la propriété Command. TooltipTitle
topic_type:
- apiref
api_name:
- Command.TooltipTitle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c60f4ddea77fbf88a15d5d27e90ca5660bc0edb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466575"
---
# <a name="commandtooltiptitle-property"></a><span data-ttu-id="fe3eb-104">Command. TooltipTitle, propriété</span><span class="sxs-lookup"><span data-stu-id="fe3eb-104">Command.TooltipTitle property</span></span>

<span data-ttu-id="fe3eb-105">Représente un titre d’info-bulle.</span><span class="sxs-lookup"><span data-stu-id="fe3eb-105">Represents a tooltip title.</span></span>

## <a name="usage"></a><span data-ttu-id="fe3eb-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="fe3eb-106">Usage</span></span>

``` syntax
<Command.TooltipTitle>
  child elements
</Command.TooltipTitle>
```

## <a name="attributes"></a><span data-ttu-id="fe3eb-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="fe3eb-107">Attributes</span></span>

<span data-ttu-id="fe3eb-108">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="fe3eb-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="fe3eb-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="fe3eb-109">Child elements</span></span>



| <span data-ttu-id="fe3eb-110">Élément</span><span class="sxs-lookup"><span data-stu-id="fe3eb-110">Element</span></span>                                                   | <span data-ttu-id="fe3eb-111">Description</span><span class="sxs-lookup"><span data-stu-id="fe3eb-111">Description</span></span>                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="fe3eb-112">**String**</span><span class="sxs-lookup"><span data-stu-id="fe3eb-112">**String**</span></span>](windowsribbon-element-string.md)<br/> | <span data-ttu-id="fe3eb-113">Peut se produire au plus une fois</span><span class="sxs-lookup"><span data-stu-id="fe3eb-113">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="fe3eb-114">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="fe3eb-114">Parent elements</span></span>



| <span data-ttu-id="fe3eb-115">Élément</span><span class="sxs-lookup"><span data-stu-id="fe3eb-115">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="fe3eb-116">**Commande**</span><span class="sxs-lookup"><span data-stu-id="fe3eb-116">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="fe3eb-117">Notes</span><span class="sxs-lookup"><span data-stu-id="fe3eb-117">Remarks</span></span>

<span data-ttu-id="fe3eb-118">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="fe3eb-118">Optional.</span></span>

<span data-ttu-id="fe3eb-119">Peut se produire au plus une fois pour chaque [**commande**](windowsribbon-element-command.md).</span><span class="sxs-lookup"><span data-stu-id="fe3eb-119">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="fe3eb-120">**Command. TooltipTitle** peut contenir une valeur de type *XS : String* limitée à toute séquence de caractères, y compris les espaces blancs et les sauts de ligne.</span><span class="sxs-lookup"><span data-stu-id="fe3eb-120">**Command.TooltipTitle** can contain a value of type *xs:string* constrained to any sequence of characters, including white space and line-break characters.</span></span>

> [!Note]  
> <span data-ttu-id="fe3eb-121">Utilisez la référence de caractère XML UCS (Universal Character Set) `&#xA;` pour spécifier un saut de ligne.</span><span class="sxs-lookup"><span data-stu-id="fe3eb-121">Use the Universal Character Set (UCS) XML character reference `&#xA;` to specify a line break.</span></span>

 

<span data-ttu-id="fe3eb-122">La longueur maximale est illimitée.</span><span class="sxs-lookup"><span data-stu-id="fe3eb-122">The maximum length is unbounded.</span></span>

<span data-ttu-id="fe3eb-123">Si aucune valeur n’est fournie pour **Command. TooltipTitle**, l’élément enfant [**String**](windowsribbon-element-string.md) est requis.</span><span class="sxs-lookup"><span data-stu-id="fe3eb-123">If no value is supplied for **Command.TooltipTitle**, the [**String**](windowsribbon-element-string.md) child element is required.</span></span>

> [!Note]  
> <span data-ttu-id="fe3eb-124">Si **Command. TooltipTitle** contient à la fois une valeur et un élément enfant de [**chaîne**](windowsribbon-element-string.md) , la **chaîne** est prioritaire.</span><span class="sxs-lookup"><span data-stu-id="fe3eb-124">If **Command.TooltipTitle** contains both a value and a [**String**](windowsribbon-element-string.md) child element, **String** takes precedence.</span></span>

 

<span data-ttu-id="fe3eb-125">**Command. TooltipTitle** prend uniquement en charge l’alignement à gauche.</span><span class="sxs-lookup"><span data-stu-id="fe3eb-125">**Command.TooltipTitle** only supports left alignment.</span></span>

## <a name="examples"></a><span data-ttu-id="fe3eb-126">Exemples</span><span class="sxs-lookup"><span data-stu-id="fe3eb-126">Examples</span></span>

<span data-ttu-id="fe3eb-127">L’exemple suivant illustre le balisage pour un élément [**Command**](windowsribbon-element-command.md) avec une déclaration **Command. TooltipTitle** .</span><span class="sxs-lookup"><span data-stu-id="fe3eb-127">The following example demonstrates the markup for a [**Command**](windowsribbon-element-command.md) element with a **Command.TooltipTitle** declaration.</span></span>


```XML
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
```



## <a name="requirements"></a><span data-ttu-id="fe3eb-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fe3eb-128">Requirements</span></span>



| <span data-ttu-id="fe3eb-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fe3eb-129">Requirement</span></span> | <span data-ttu-id="fe3eb-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="fe3eb-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="fe3eb-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe3eb-131">Minimum supported client</span></span><br/> | <span data-ttu-id="fe3eb-132">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fe3eb-132">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="fe3eb-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe3eb-133">Minimum supported server</span></span><br/> | <span data-ttu-id="fe3eb-134">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fe3eb-134">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fe3eb-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fe3eb-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe3eb-136">IU \_ \_ TooltipTitle</span><span class="sxs-lookup"><span data-stu-id="fe3eb-136">UI\_PKEY\_TooltipTitle</span></span>](windowsribbon-reference-properties-uipkey-tooltiptitle.md)
</dt> </dl>

 

 





