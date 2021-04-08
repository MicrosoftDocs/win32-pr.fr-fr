---
title: String. Symbol, propriété
description: Représente le nom d’une ressource de type chaîne.
ms.assetid: 7c1d0197-2c9b-4f42-afba-73fd1c366deb
keywords:
- Propriété String. Symbol, ruban Windows
topic_type:
- apiref
api_name:
- String.Symbol
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7bf7d30ddd8677b1c5ff0a5e55d4b9c119795ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843173"
---
# <a name="stringsymbol-property"></a><span data-ttu-id="8feac-104">String. Symbol, propriété</span><span class="sxs-lookup"><span data-stu-id="8feac-104">String.Symbol property</span></span>

<span data-ttu-id="8feac-105">Représente le nom d’une ressource de type chaîne.</span><span class="sxs-lookup"><span data-stu-id="8feac-105">Represents the name of a string resource.</span></span>

## <a name="usage"></a><span data-ttu-id="8feac-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="8feac-106">Usage</span></span>

``` syntax
<String.Symbol/>
```

## <a name="attributes"></a><span data-ttu-id="8feac-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="8feac-107">Attributes</span></span>

<span data-ttu-id="8feac-108">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="8feac-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="8feac-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="8feac-109">Child elements</span></span>

<span data-ttu-id="8feac-110">Il n’y a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="8feac-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="8feac-111">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="8feac-111">Parent elements</span></span>



| <span data-ttu-id="8feac-112">Élément</span><span class="sxs-lookup"><span data-stu-id="8feac-112">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="8feac-113">**String**</span><span class="sxs-lookup"><span data-stu-id="8feac-113">**String**</span></span>](windowsribbon-element-string.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="8feac-114">Notes</span><span class="sxs-lookup"><span data-stu-id="8feac-114">Remarks</span></span>

<span data-ttu-id="8feac-115">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="8feac-115">Optional.</span></span>

<span data-ttu-id="8feac-116">Peut se produire au plus une fois pour chaque élément de [**chaîne**](windowsribbon-element-string.md) .</span><span class="sxs-lookup"><span data-stu-id="8feac-116">May occur at most once for each [**String**](windowsribbon-element-string.md) element.</span></span>

<span data-ttu-id="8feac-117">Le symbole est associé à une définition de chaîne dans le fichier d’en-tête du ruban, par exemple `#define strSave 59999` .</span><span class="sxs-lookup"><span data-stu-id="8feac-117">The symbol is associated with a string definition in the Ribbon header file, for example, `#define strSave 59999`.</span></span>

<span data-ttu-id="8feac-118">Cet élément contient une valeur de type *XS : String*.</span><span class="sxs-lookup"><span data-stu-id="8feac-118">This element contains a value of type *xs:string*.</span></span> <span data-ttu-id="8feac-119">La valeur est conformée en une chaîne composée d’une lettre ou d’un trait de soulignement suivi d’une séquence de lettres, de chiffres ou de traits de soulignement.</span><span class="sxs-lookup"><span data-stu-id="8feac-119">The value is constrained to a string composed of a letter or underscore followed by any sequence of letters, digits, or underscores.</span></span>

<span data-ttu-id="8feac-120">La longueur maximale est de 100 caractères.</span><span class="sxs-lookup"><span data-stu-id="8feac-120">The maximum length is 100 characters.</span></span>

## <a name="examples"></a><span data-ttu-id="8feac-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="8feac-121">Examples</span></span>

<span data-ttu-id="8feac-122">L’exemple suivant illustre le balisage pour un élément [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) avec une déclaration **String. Symbol** .</span><span class="sxs-lookup"><span data-stu-id="8feac-122">The following example demonstrates the markup for a [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) element with a **String.Symbol** declaration.</span></span>


```XML
<Command.LabelTitle>
  <String>
    <String.Content>Label for Save</String.Content>
    <String.Id>59999</String.Id>
    <String.Symbol>strSave</String.Symbol>
  </String>
</Command.LabelTitle>
```



## <a name="requirements"></a><span data-ttu-id="8feac-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8feac-123">Requirements</span></span>



| <span data-ttu-id="8feac-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8feac-124">Requirement</span></span> | <span data-ttu-id="8feac-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="8feac-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="8feac-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8feac-126">Minimum supported client</span></span><br/> | <span data-ttu-id="8feac-127">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8feac-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="8feac-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8feac-128">Minimum supported server</span></span><br/> | <span data-ttu-id="8feac-129">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8feac-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





