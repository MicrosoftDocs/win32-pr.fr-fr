---
title: Command. Comment, propriété
description: Représente un commentaire, ou annotation, pour une commande.
ms.assetid: 4ac5c7d4-9627-4703-bd3c-594d9497ba24
keywords:
- Commande. Comment, propriété du ruban Windows
topic_type:
- apiref
api_name:
- Command.Comment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f7df2131234623dd30fc90339634a932eca5bd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385119"
---
# <a name="commandcomment-property"></a><span data-ttu-id="0cf06-104">Command. Comment, propriété</span><span class="sxs-lookup"><span data-stu-id="0cf06-104">Command.Comment property</span></span>

<span data-ttu-id="0cf06-105">Représente un commentaire, ou annotation, pour une commande.</span><span class="sxs-lookup"><span data-stu-id="0cf06-105">Represents a comment, or annotation, for a Command.</span></span>

## <a name="usage"></a><span data-ttu-id="0cf06-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="0cf06-106">Usage</span></span>

``` syntax
<Command.Comment/>
```

## <a name="attributes"></a><span data-ttu-id="0cf06-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="0cf06-107">Attributes</span></span>

<span data-ttu-id="0cf06-108">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="0cf06-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="0cf06-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0cf06-109">Child elements</span></span>

<span data-ttu-id="0cf06-110">Il n’y a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="0cf06-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="0cf06-111">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="0cf06-111">Parent elements</span></span>



| <span data-ttu-id="0cf06-112">Élément</span><span class="sxs-lookup"><span data-stu-id="0cf06-112">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="0cf06-113">**Commande**</span><span class="sxs-lookup"><span data-stu-id="0cf06-113">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="0cf06-114">Notes</span><span class="sxs-lookup"><span data-stu-id="0cf06-114">Remarks</span></span>

<span data-ttu-id="0cf06-115">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="0cf06-115">Optional.</span></span>

<span data-ttu-id="0cf06-116">Peut se produire au plus une fois pour chaque [**commande**](windowsribbon-element-command.md).</span><span class="sxs-lookup"><span data-stu-id="0cf06-116">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="0cf06-117">Le commentaire est associé à une définition de commande dans le fichier d’en-tête du ruban, par exemple `#define cmdSave 25003 /* Save */` .</span><span class="sxs-lookup"><span data-stu-id="0cf06-117">The comment is associated with a Command definition in the Ribbon header file, for example, `#define cmdSave 25003 /* Save */`.</span></span>

<span data-ttu-id="0cf06-118">Cet élément contient une valeur de type *XS : String*.</span><span class="sxs-lookup"><span data-stu-id="0cf06-118">This element contains a value of type *xs:string*.</span></span>

<span data-ttu-id="0cf06-119">La longueur maximale est de 250 caractères.</span><span class="sxs-lookup"><span data-stu-id="0cf06-119">The maximum length is 250 characters.</span></span>

## <a name="examples"></a><span data-ttu-id="0cf06-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="0cf06-120">Examples</span></span>

<span data-ttu-id="0cf06-121">L’exemple suivant illustre le balisage pour un élément [**Command**](windowsribbon-element-command.md) avec une déclaration **Command. Comment** .</span><span class="sxs-lookup"><span data-stu-id="0cf06-121">The following example demonstrates the markup for a [**Command**](windowsribbon-element-command.md) element with a **Command.Comment** declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="0cf06-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0cf06-122">Requirements</span></span>



| <span data-ttu-id="0cf06-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0cf06-123">Requirement</span></span> | <span data-ttu-id="0cf06-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="0cf06-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="0cf06-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0cf06-125">Minimum supported client</span></span><br/> | <span data-ttu-id="0cf06-126">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0cf06-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="0cf06-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0cf06-127">Minimum supported server</span></span><br/> | <span data-ttu-id="0cf06-128">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0cf06-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





