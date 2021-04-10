---
title: Propriété String.Id
description: Représente l’ID unique d’une ressource de type chaîne.
ms.assetid: 393da279-bdf6-4796-a546-1931cbe49113
keywords:
- Ruban Windows de la propriété String.Id
topic_type:
- apiref
api_name:
- String.Id
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c3ab87327ed4f11a901fb8a201e72137ab62c7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105622"
---
# <a name="stringid-property"></a><span data-ttu-id="0e840-104">Propriété String.Id</span><span class="sxs-lookup"><span data-stu-id="0e840-104">String.Id property</span></span>

<span data-ttu-id="0e840-105">Représente l’ID unique d’une ressource de type chaîne.</span><span class="sxs-lookup"><span data-stu-id="0e840-105">Represents the unique ID of a string resource.</span></span>

## <a name="usage"></a><span data-ttu-id="0e840-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="0e840-106">Usage</span></span>

``` syntax
<String.Id/>
```

## <a name="attributes"></a><span data-ttu-id="0e840-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="0e840-107">Attributes</span></span>

<span data-ttu-id="0e840-108">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="0e840-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="0e840-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0e840-109">Child elements</span></span>

<span data-ttu-id="0e840-110">Il n’y a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="0e840-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="0e840-111">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="0e840-111">Parent elements</span></span>



| <span data-ttu-id="0e840-112">Élément</span><span class="sxs-lookup"><span data-stu-id="0e840-112">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="0e840-113">**String**</span><span class="sxs-lookup"><span data-stu-id="0e840-113">**String**</span></span>](windowsribbon-element-string.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="0e840-114">Notes</span><span class="sxs-lookup"><span data-stu-id="0e840-114">Remarks</span></span>

<span data-ttu-id="0e840-115">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="0e840-115">Optional.</span></span>

<span data-ttu-id="0e840-116">Peut se produire au plus une fois pour chaque élément de [**chaîne**](windowsribbon-element-string.md) .</span><span class="sxs-lookup"><span data-stu-id="0e840-116">May occur at most once for each [**String**](windowsribbon-element-string.md) element.</span></span>

<span data-ttu-id="0e840-117">La valeur de **String.ID** doit être unique.</span><span class="sxs-lookup"><span data-stu-id="0e840-117">The value for **String.Id** must be unique.</span></span>

<span data-ttu-id="0e840-118">L’ID est associé à une définition de chaîne dans le fichier d’en-tête du ruban, par exemple `#define strSave 59999` .</span><span class="sxs-lookup"><span data-stu-id="0e840-118">The ID is associated with a string definition in the Ribbon header file, for example, `#define strSave 59999`.</span></span>

<span data-ttu-id="0e840-119">Cet élément contient une valeur de l’Union de types *XS : positiveInteger* et *XS : String*.</span><span class="sxs-lookup"><span data-stu-id="0e840-119">This element contains a value from the union of types *xs:positiveInteger* and *xs:string*.</span></span> <span data-ttu-id="0e840-120">La valeur est restreinte à une valeur entière comprise entre 2 et 59999, inclusive, ou 0X2 et 0xea5f en hexadécimal, inclus.</span><span class="sxs-lookup"><span data-stu-id="0e840-120">The value is constrained to a integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span>

<span data-ttu-id="0e840-121">La longueur maximale est de 10 caractères avec des zéros non significatifs facultatifs.</span><span class="sxs-lookup"><span data-stu-id="0e840-121">The maximum length is 10 characters with optional leading zeros.</span></span>

## <a name="examples"></a><span data-ttu-id="0e840-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="0e840-122">Examples</span></span>

<span data-ttu-id="0e840-123">L’exemple suivant illustre le balisage pour un élément [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) avec une déclaration **String.ID** .</span><span class="sxs-lookup"><span data-stu-id="0e840-123">The following example demonstrates the markup for a [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) element with a **String.Id** declaration.</span></span>


```XML
<Command.LabelTitle>
  <String>
    <String.Content>Label for Save</String.Content>
    <String.Id>59999</String.Id>
    <String.Symbol>strSave</String.Symbol>
  </String>
</Command.LabelTitle>
```



## <a name="requirements"></a><span data-ttu-id="0e840-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e840-124">Requirements</span></span>



| <span data-ttu-id="0e840-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e840-125">Requirement</span></span> | <span data-ttu-id="0e840-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e840-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="0e840-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e840-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0e840-128">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e840-128">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="0e840-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e840-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0e840-130">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e840-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





