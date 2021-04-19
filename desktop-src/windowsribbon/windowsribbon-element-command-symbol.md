---
title: Command. Symbol, propriété
description: Représente le nom d’une commande qui peut être référencée en externe.
ms.assetid: affa5f3f-f641-4bec-9165-6102509cf355
keywords:
- Propriété Command. Symbol, ruban Windows
topic_type:
- apiref
api_name:
- Command.Symbol
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b88dccb71a90feca7348ca9731ca5966b012c9c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510352"
---
# <a name="commandsymbol-property"></a><span data-ttu-id="6d0cb-104">Command. Symbol, propriété</span><span class="sxs-lookup"><span data-stu-id="6d0cb-104">Command.Symbol property</span></span>

<span data-ttu-id="6d0cb-105">Représente le nom d’une [**commande**](windowsribbon-element-command.md) qui peut être référencée en externe.</span><span class="sxs-lookup"><span data-stu-id="6d0cb-105">Represents the name of a [**Command**](windowsribbon-element-command.md) that can be referenced externally.</span></span>

## <a name="usage"></a><span data-ttu-id="6d0cb-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="6d0cb-106">Usage</span></span>

``` syntax
<Command.Symbol/>
```

## <a name="attributes"></a><span data-ttu-id="6d0cb-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="6d0cb-107">Attributes</span></span>

<span data-ttu-id="6d0cb-108">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="6d0cb-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="6d0cb-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="6d0cb-109">Child elements</span></span>

<span data-ttu-id="6d0cb-110">Il n’y a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="6d0cb-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="6d0cb-111">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="6d0cb-111">Parent elements</span></span>



| <span data-ttu-id="6d0cb-112">Élément</span><span class="sxs-lookup"><span data-stu-id="6d0cb-112">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="6d0cb-113">**Commande**</span><span class="sxs-lookup"><span data-stu-id="6d0cb-113">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="6d0cb-114">Notes</span><span class="sxs-lookup"><span data-stu-id="6d0cb-114">Remarks</span></span>

<span data-ttu-id="6d0cb-115">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="6d0cb-115">Optional.</span></span>

<span data-ttu-id="6d0cb-116">Peut se produire au plus une fois pour chaque [**commande**](windowsribbon-element-command.md).</span><span class="sxs-lookup"><span data-stu-id="6d0cb-116">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="6d0cb-117">Le symbole est associé à une définition de commande dans le fichier d’en-tête du ruban, par exemple `#define cmdSave 25003 /* Save */` .</span><span class="sxs-lookup"><span data-stu-id="6d0cb-117">The symbol is associated with a Command definition in the Ribbon header file, for example, `#define cmdSave 25003 /* Save */`.</span></span>

<span data-ttu-id="6d0cb-118">Cet élément contient une valeur de type *XS : String*.</span><span class="sxs-lookup"><span data-stu-id="6d0cb-118">This element contains a value of type *xs:string*.</span></span>

<span data-ttu-id="6d0cb-119">La valeur est conformée en une chaîne qui se compose d’une lettre ou d’un trait de soulignement suivi d’une séquence de lettres, de chiffres et de traits de soulignement.</span><span class="sxs-lookup"><span data-stu-id="6d0cb-119">The value is constrained to a string that consists of a letter or underscore followed by any sequence of letters, digits, and underscores.</span></span>

<span data-ttu-id="6d0cb-120">La longueur maximale est de 100 caractères.</span><span class="sxs-lookup"><span data-stu-id="6d0cb-120">The maximum length is 100 characters.</span></span>

## <a name="examples"></a><span data-ttu-id="6d0cb-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="6d0cb-121">Examples</span></span>

<span data-ttu-id="6d0cb-122">L’exemple suivant illustre le balisage pour un élément [**Command**](windowsribbon-element-command.md) avec une déclaration **Command. Symbol** .</span><span class="sxs-lookup"><span data-stu-id="6d0cb-122">The following example demonstrates the markup for a [**Command**](windowsribbon-element-command.md) element with a **Command.Symbol** declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="6d0cb-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6d0cb-123">Requirements</span></span>



| <span data-ttu-id="6d0cb-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6d0cb-124">Requirement</span></span> | <span data-ttu-id="6d0cb-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="6d0cb-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="6d0cb-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d0cb-126">Minimum supported client</span></span><br/> | <span data-ttu-id="6d0cb-127">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6d0cb-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="6d0cb-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d0cb-128">Minimum supported server</span></span><br/> | <span data-ttu-id="6d0cb-129">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6d0cb-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





