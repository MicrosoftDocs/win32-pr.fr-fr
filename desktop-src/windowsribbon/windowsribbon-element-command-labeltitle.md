---
title: Command. LabelTitle, propriété
description: Représente le titre d’une étiquette.
ms.assetid: 97378ec3-7988-4e39-9cf5-c382b246c5c9
keywords:
- Ruban Windows de la propriété Command. LabelTitle
topic_type:
- apiref
api_name:
- Command.LabelTitle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed6d6c72ddd60cca63834fdcf21cf8f8b726ad22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509182"
---
# <a name="commandlabeltitle-property"></a><span data-ttu-id="ea539-104">Command. LabelTitle, propriété</span><span class="sxs-lookup"><span data-stu-id="ea539-104">Command.LabelTitle property</span></span>

<span data-ttu-id="ea539-105">Représente le titre d’une étiquette.</span><span class="sxs-lookup"><span data-stu-id="ea539-105">Represents a label title.</span></span>

## <a name="usage"></a><span data-ttu-id="ea539-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="ea539-106">Usage</span></span>

``` syntax
<Command.LabelTitle>
  child elements
</Command.LabelTitle>
```

## <a name="attributes"></a><span data-ttu-id="ea539-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="ea539-107">Attributes</span></span>

<span data-ttu-id="ea539-108">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="ea539-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="ea539-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ea539-109">Child elements</span></span>



| <span data-ttu-id="ea539-110">Élément</span><span class="sxs-lookup"><span data-stu-id="ea539-110">Element</span></span>                                                   | <span data-ttu-id="ea539-111">Description</span><span class="sxs-lookup"><span data-stu-id="ea539-111">Description</span></span>                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="ea539-112">**String**</span><span class="sxs-lookup"><span data-stu-id="ea539-112">**String**</span></span>](windowsribbon-element-string.md)<br/> | <span data-ttu-id="ea539-113">Peut se produire au plus une fois</span><span class="sxs-lookup"><span data-stu-id="ea539-113">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="ea539-114">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="ea539-114">Parent elements</span></span>



| <span data-ttu-id="ea539-115">Élément</span><span class="sxs-lookup"><span data-stu-id="ea539-115">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="ea539-116">**Commande**</span><span class="sxs-lookup"><span data-stu-id="ea539-116">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="ea539-117">Notes</span><span class="sxs-lookup"><span data-stu-id="ea539-117">Remarks</span></span>

<span data-ttu-id="ea539-118">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="ea539-118">Optional.</span></span>

<span data-ttu-id="ea539-119">Peut se produire au plus une fois pour chaque [**commande**](windowsribbon-element-command.md).</span><span class="sxs-lookup"><span data-stu-id="ea539-119">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="ea539-120">**Command. LabelTitle** peut contenir une valeur de type *XS : String* limitée à toute séquence de caractères, y compris les espaces blancs et les sauts de ligne.</span><span class="sxs-lookup"><span data-stu-id="ea539-120">**Command.LabelTitle** can contain a value of type *xs:string* constrained to any sequence of characters, including white space and line-break characters.</span></span>

> [!Note]  
> <span data-ttu-id="ea539-121">Utilisez la référence de caractère XML UCS (Universal Character Set) `&#xA;` pour spécifier un saut de ligne.</span><span class="sxs-lookup"><span data-stu-id="ea539-121">Use the Universal Character Set (UCS) XML character reference `&#xA;` to specify a line break.</span></span>

 

<span data-ttu-id="ea539-122">La longueur maximale est illimitée.</span><span class="sxs-lookup"><span data-stu-id="ea539-122">The maximum length is unbounded.</span></span>

<span data-ttu-id="ea539-123">Si aucune valeur n’est fournie pour **Command. LabelTitle**, l’élément enfant [**String**](windowsribbon-element-string.md) est requis.</span><span class="sxs-lookup"><span data-stu-id="ea539-123">If no value is supplied for **Command.LabelTitle**, the [**String**](windowsribbon-element-string.md) child element is required.</span></span>

> [!Note]  
> <span data-ttu-id="ea539-124">Si **Command. LabelTitle** contient à la fois une valeur et un élément enfant de [**chaîne**](windowsribbon-element-string.md) , la **chaîne** est prioritaire.</span><span class="sxs-lookup"><span data-stu-id="ea539-124">If **Command.LabelTitle** contains both a value and a [**String**](windowsribbon-element-string.md) child element, **String** takes precedence.</span></span>

 

<span data-ttu-id="ea539-125">**Command. LabelTitle** prend uniquement en charge l’alignement à gauche.</span><span class="sxs-lookup"><span data-stu-id="ea539-125">**Command.LabelTitle** only supports left alignment.</span></span>

<span data-ttu-id="ea539-126">Si une commande est exposée à l’aide d’un élément de menu et que la valeur de **Command. LabelTitle** ou de l' [ \_ \_ étiquette de l’interface utilisateur](windowsribbon-reference-properties-uipkey-label.md) contient une lettre précédée d’une esperluette, comme indiqué dans l’exemple suivant, cette lettre est traitée comme une touche d’accès et une touche d’accès rapide pour cette commande par l’infrastructure du ruban.</span><span class="sxs-lookup"><span data-stu-id="ea539-126">If a Command is exposed through a menu item and the value of **Command.LabelTitle** or [UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md) contains a letter preceded by an ampersand, as shown in the following example, this letter is treated as both a keytip and a keyboard accelerator for that Command by the Ribbon framework.</span></span>


```XML
<Command Name="cmdNew"
         Symbol="ID_FILE_NEW"
         Comment="New"
         Id="25001"
         LabelTitle="&amp;New"/>
```



<span data-ttu-id="ea539-127">Pour afficher une esperluette dans une étiquette, échappez la désignation de caractères spéciaux par une double esperluette ( `&&` ), comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="ea539-127">To display an ampersand in a label, escape the special character designation with a double ampersand (`&&`) as shown in the following example.</span></span>


```XML
<Command Name="cmdOpen"
         Symbol="ID_FILE_OPEN"
         Comment="Open"
         Id="25002"
         LabelTitle="&amp;&amp;Open"/>
```



## <a name="examples"></a><span data-ttu-id="ea539-128">Exemples</span><span class="sxs-lookup"><span data-stu-id="ea539-128">Examples</span></span>

<span data-ttu-id="ea539-129">L’exemple suivant illustre le balisage pour un élément [**Command**](windowsribbon-element-command.md) avec une déclaration **Command. LabelTitle** .</span><span class="sxs-lookup"><span data-stu-id="ea539-129">The following example demonstrates the markup for a [**Command**](windowsribbon-element-command.md) element with a **Command.LabelTitle** declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="ea539-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ea539-130">Requirements</span></span>



| <span data-ttu-id="ea539-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ea539-131">Requirement</span></span> | <span data-ttu-id="ea539-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="ea539-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="ea539-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ea539-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ea539-134">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ea539-134">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="ea539-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ea539-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ea539-136">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ea539-136">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ea539-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ea539-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea539-138">\_Étiquette de nom de l’interface utilisateur \_</span><span class="sxs-lookup"><span data-stu-id="ea539-138">UI\_PKEY\_Label</span></span>](windowsribbon-reference-properties-uipkey-label.md)
</dt> </dl>

 

 





