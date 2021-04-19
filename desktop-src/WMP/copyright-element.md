---
title: Élément de COPYRIGHT (msfeeds. h)
description: L’élément COPYRIGHT définit une chaîne de texte spécifiant les informations de copyright pour un élément ASX ou ENTRy.
ms.assetid: 264b92de-b10c-41b9-b219-727879079f15
keywords:
- Élément de COPYRIGHT lecteur Windows Media
topic_type:
- apiref
api_name:
- COPYRIGHT Element
api_location:
- msfeeds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83b757528cfb14a01854346854a342ee9faced65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543240"
---
# <a name="copyright-element"></a><span data-ttu-id="62393-104">Élément de COPYRIGHT</span><span class="sxs-lookup"><span data-stu-id="62393-104">COPYRIGHT Element</span></span>

<span data-ttu-id="62393-105">L’élément **Copyright** définit une chaîne de texte spécifiant les informations de copyright pour un élément **ASX** ou **entry** .</span><span class="sxs-lookup"><span data-stu-id="62393-105">The **COPYRIGHT** element defines a text string specifying the copyright information for an **ASX** or **ENTRY** element.</span></span>

``` syntax
<COPYRIGHT>
    text string
</COPYRIGHT>
```

## <a name="attributes"></a><span data-ttu-id="62393-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="62393-106">Attributes</span></span>

<span data-ttu-id="62393-107">Cet élément n’a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="62393-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="62393-108">Éléments parent/enfant</span><span class="sxs-lookup"><span data-stu-id="62393-108">Parent/Child Elements</span></span>



| <span data-ttu-id="62393-109">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="62393-109">Hierarchy</span></span>       | <span data-ttu-id="62393-110">Éléments</span><span class="sxs-lookup"><span data-stu-id="62393-110">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="62393-111">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="62393-111">Parent elements</span></span> | <span data-ttu-id="62393-112">**ASX**, **entrée**</span><span class="sxs-lookup"><span data-stu-id="62393-112">**ASX**, **ENTRY**</span></span> |
| <span data-ttu-id="62393-113">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="62393-113">Child elements</span></span>  | <span data-ttu-id="62393-114">Aucune</span><span class="sxs-lookup"><span data-stu-id="62393-114">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="62393-115">Notes</span><span class="sxs-lookup"><span data-stu-id="62393-115">Remarks</span></span>

<span data-ttu-id="62393-116">Cet élément définit une chaîne de texte qui spécifie les informations de copyright pour un élément **ASX** ou d' **entrée** .</span><span class="sxs-lookup"><span data-stu-id="62393-116">This element defines a text string that specifies the copyright information for an **ASX** or **ENTRY** element.</span></span>

<span data-ttu-id="62393-117">Lorsque cet élément apparaît dans un élément **ASX** , la chaîne de Copyright s’affiche uniquement comme **Afficher** les informations.</span><span class="sxs-lookup"><span data-stu-id="62393-117">When this element appears within an **ASX** element, the copyright string is displayed only as **Show** information.</span></span> <span data-ttu-id="62393-118">Lorsque cet élément apparaît dans un élément **entry** , le texte est affiché sous forme d’informations de clips.</span><span class="sxs-lookup"><span data-stu-id="62393-118">When this element appears within an **ENTRY** element, the text is displayed as clip information.</span></span> <span data-ttu-id="62393-119">Chaque **ASX** parent et élément d' **entrée** doit contenir au plus un élément de **Copyright** enfant.</span><span class="sxs-lookup"><span data-stu-id="62393-119">Each parent **ASX** and **ENTRY** element should contain at most one child **COPYRIGHT** element.</span></span> <span data-ttu-id="62393-120">Plusieurs éléments de **Copyright** après le premier seront ignorés et ne seront pas affichés.</span><span class="sxs-lookup"><span data-stu-id="62393-120">Multiple **COPYRIGHT** elements after the first will be ignored and will not be displayed.</span></span>

<span data-ttu-id="62393-121">Les caractères des symboles de copyright et de marque déposée (ou) peuvent ne pas s’afficher correctement si le métafichier n’est pas encodé à l’aide du schéma d’encodage UTF-8.</span><span class="sxs-lookup"><span data-stu-id="62393-121">The characters for copyright and trademark registration symbols (   or   ) may not display properly if the metafile is not encoded using the UTF-8 encoding scheme.</span></span> <span data-ttu-id="62393-122">Dans ce cas, pour afficher correctement l’un de ces symboles pour tous les utilisateurs, vous pouvez utiliser les équivalents ASCII (c) et (R) à la place.</span><span class="sxs-lookup"><span data-stu-id="62393-122">In this case, to display either of these symbols properly for all users, you can use the ASCII equivalents (c) and (R) instead.</span></span>

<span data-ttu-id="62393-123">Si le métafichier est encodé à l’aide de UTF-8, les symboles de copyright et de marque s’affichent correctement.</span><span class="sxs-lookup"><span data-stu-id="62393-123">If the metafile is encoded using UTF-8, copyright and trademark symbols will display correctly.</span></span>

## <a name="examples"></a><span data-ttu-id="62393-124">Exemples</span><span class="sxs-lookup"><span data-stu-id="62393-124">Examples</span></span>


```XML
<COPYRIGHT>Copyright (c) 1998, Microsoft Corporation</COPYRIGHT>

```



## <a name="requirements"></a><span data-ttu-id="62393-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="62393-125">Requirements</span></span>



| <span data-ttu-id="62393-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="62393-126">Requirement</span></span> | <span data-ttu-id="62393-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="62393-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="62393-128">Version</span><span class="sxs-lookup"><span data-stu-id="62393-128">Version</span></span><br/> | <span data-ttu-id="62393-129">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="62393-129">Windows Media Player version 7.0 or later</span></span><br/>                                 |
| <span data-ttu-id="62393-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="62393-130">Header</span></span><br/>  | <dl> <span data-ttu-id="62393-131"><dt>Msfeeds. h</dt></span><span class="sxs-lookup"><span data-stu-id="62393-131"><dt>Msfeeds.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62393-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62393-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62393-133">**Ajout de caractères de copyright aux sous-fichiers**</span><span class="sxs-lookup"><span data-stu-id="62393-133">**Adding Copyright Characters to Metafiles**</span></span>](adding-copyright-characters-to-metafiles.md)
</dt> <dt>

[<span data-ttu-id="62393-134">**Informations de référence sur les éléments de métafichier Windows Media**</span><span class="sxs-lookup"><span data-stu-id="62393-134">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="62393-135">**Informations de référence sur les métafichiers Windows Media**</span><span class="sxs-lookup"><span data-stu-id="62393-135">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





