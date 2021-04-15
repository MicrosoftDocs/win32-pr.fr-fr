---
title: Propriété Command.Id
description: Représente un ID unique pour une commande.
ms.assetid: 937ca9d6-6910-4133-9cfa-d7e3f895f876
keywords:
- Ruban Windows de la propriété Command.Id
topic_type:
- apiref
api_name:
- Command.Id
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13e259e5fd74e3037afde3d4c001000b5a17a9bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466590"
---
# <a name="commandid-property"></a><span data-ttu-id="4018b-104">Propriété Command.Id</span><span class="sxs-lookup"><span data-stu-id="4018b-104">Command.Id property</span></span>

<span data-ttu-id="4018b-105">Représente un ID unique pour une commande.</span><span class="sxs-lookup"><span data-stu-id="4018b-105">Represents a unique ID for a Command.</span></span>

## <a name="usage"></a><span data-ttu-id="4018b-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="4018b-106">Usage</span></span>

``` syntax
<Command.Id/>
```

## <a name="attributes"></a><span data-ttu-id="4018b-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="4018b-107">Attributes</span></span>

<span data-ttu-id="4018b-108">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="4018b-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="4018b-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="4018b-109">Child elements</span></span>

<span data-ttu-id="4018b-110">Il n’y a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="4018b-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="4018b-111">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="4018b-111">Parent elements</span></span>



| <span data-ttu-id="4018b-112">Élément</span><span class="sxs-lookup"><span data-stu-id="4018b-112">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="4018b-113">**Commande**</span><span class="sxs-lookup"><span data-stu-id="4018b-113">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="4018b-114">Notes</span><span class="sxs-lookup"><span data-stu-id="4018b-114">Remarks</span></span>

<span data-ttu-id="4018b-115">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="4018b-115">Optional.</span></span>

<span data-ttu-id="4018b-116">Peut se produire au plus une fois pour chaque [**commande**](windowsribbon-element-command.md).</span><span class="sxs-lookup"><span data-stu-id="4018b-116">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="4018b-117">L’ID est associé à une définition de commande dans le fichier d’en-tête du ruban, par exemple `#define cmdSave 25003 /* Save */` .</span><span class="sxs-lookup"><span data-stu-id="4018b-117">The ID is associated with a Command definition in the Ribbon header file, for example, `#define cmdSave 25003 /* Save */`.</span></span>

<span data-ttu-id="4018b-118">Cet élément contient une valeur de l’Union de types *XS : positiveInteger* et *XS : String* , avec une valeur entière comprise entre 2 et 59999, inclusive, ou 0X2 et 0xea5f au format hexadécimal, inclus.</span><span class="sxs-lookup"><span data-stu-id="4018b-118">This element contains a value from the union of types *xs:positiveInteger* and *xs:string* constrained to an integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span>

<span data-ttu-id="4018b-119">La longueur maximale est de 10 caractères, y compris des zéros non significatifs facultatifs.</span><span class="sxs-lookup"><span data-stu-id="4018b-119">The maximum length is 10 characters, including optional leading zeros.</span></span>

## <a name="examples"></a><span data-ttu-id="4018b-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="4018b-120">Examples</span></span>

<span data-ttu-id="4018b-121">L’exemple suivant illustre le balisage pour un élément [**Command**](windowsribbon-element-command.md) avec une déclaration **Command.ID** .</span><span class="sxs-lookup"><span data-stu-id="4018b-121">The following example demonstrates the markup for a [**Command**](windowsribbon-element-command.md) element with a **Command.Id** declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="4018b-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4018b-122">Requirements</span></span>



| <span data-ttu-id="4018b-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4018b-123">Requirement</span></span> | <span data-ttu-id="4018b-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="4018b-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="4018b-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4018b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4018b-126">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4018b-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="4018b-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4018b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4018b-128">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4018b-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





