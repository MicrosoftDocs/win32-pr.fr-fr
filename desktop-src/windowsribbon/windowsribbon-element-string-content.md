---
title: Propriété String. Content
description: Représente le contenu d’une ressource de type chaîne.
ms.assetid: 86f34cdc-1311-4f52-979f-201d71bbb9e9
keywords:
- Propriété String. Content du ruban Windows
topic_type:
- apiref
api_name:
- String.Content
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8912264e4f55568c190212227d2e305f9d676a1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511140"
---
# <a name="stringcontent-property"></a><span data-ttu-id="fd54b-104">Propriété String. Content</span><span class="sxs-lookup"><span data-stu-id="fd54b-104">String.Content property</span></span>

<span data-ttu-id="fd54b-105">Représente le contenu d’une ressource de type chaîne.</span><span class="sxs-lookup"><span data-stu-id="fd54b-105">Represents the content of a string resource.</span></span>

## <a name="usage"></a><span data-ttu-id="fd54b-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="fd54b-106">Usage</span></span>

``` syntax
<String.Content/>
```

## <a name="attributes"></a><span data-ttu-id="fd54b-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="fd54b-107">Attributes</span></span>

<span data-ttu-id="fd54b-108">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="fd54b-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="fd54b-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="fd54b-109">Child elements</span></span>

<span data-ttu-id="fd54b-110">Il n’y a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="fd54b-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="fd54b-111">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="fd54b-111">Parent elements</span></span>



| <span data-ttu-id="fd54b-112">Élément</span><span class="sxs-lookup"><span data-stu-id="fd54b-112">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="fd54b-113">**String**</span><span class="sxs-lookup"><span data-stu-id="fd54b-113">**String**</span></span>](windowsribbon-element-string.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="fd54b-114">Notes</span><span class="sxs-lookup"><span data-stu-id="fd54b-114">Remarks</span></span>

<span data-ttu-id="fd54b-115">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="fd54b-115">Optional.</span></span>

<span data-ttu-id="fd54b-116">Peut se produire au plus une fois pour chaque élément de [**chaîne**](windowsribbon-element-string.md) .</span><span class="sxs-lookup"><span data-stu-id="fd54b-116">May occur at most once for each [**String**](windowsribbon-element-string.md) element.</span></span>

<span data-ttu-id="fd54b-117">Cet élément contient une valeur de type *XS : String*.</span><span class="sxs-lookup"><span data-stu-id="fd54b-117">This element contains a value of type *xs:string*.</span></span> <span data-ttu-id="fd54b-118">La valeur est limitée à une chaîne composée d’une séquence de caractères, y compris des espaces blancs et des sauts de ligne.</span><span class="sxs-lookup"><span data-stu-id="fd54b-118">The value is constrained to a string composed of any sequence of characters, including white space and line-break characters.</span></span>

<span data-ttu-id="fd54b-119">La longueur maximale est illimitée.</span><span class="sxs-lookup"><span data-stu-id="fd54b-119">The maximum length is unbounded.</span></span>

## <a name="examples"></a><span data-ttu-id="fd54b-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="fd54b-120">Examples</span></span>

<span data-ttu-id="fd54b-121">L’exemple suivant illustre le balisage pour un élément [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) avec une déclaration **String. Content** .</span><span class="sxs-lookup"><span data-stu-id="fd54b-121">The following example demonstrates the markup for a [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) element with a **String.Content** declaration.</span></span>


```XML
<Command.LabelTitle>
  <String>
    <String.Content>Label for Save</String.Content>
    <String.Id>59999</String.Id>
    <String.Symbol>strSave</String.Symbol>
  </String>
</Command.LabelTitle>
```



## <a name="requirements"></a><span data-ttu-id="fd54b-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fd54b-122">Requirements</span></span>



| <span data-ttu-id="fd54b-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fd54b-123">Requirement</span></span> | <span data-ttu-id="fd54b-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd54b-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="fd54b-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd54b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="fd54b-126">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fd54b-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="fd54b-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd54b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="fd54b-128">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fd54b-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





