---
title: EDITBOX. editStyle
description: L’attribut editStyle spécifie ou récupère le style du contrôle zone d’édition.
ms.assetid: 1b3052c4-3087-4d41-af03-d7758680cc3b
keywords:
- EDITBOX. editStyle Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.editStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 229f225dfca0ec00dd4f45a4eb63f6b2503d5df1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525524"
---
# <a name="editboxeditstyle"></a><span data-ttu-id="a8780-104">EDITBOX. editStyle</span><span class="sxs-lookup"><span data-stu-id="a8780-104">EDITBOX.editStyle</span></span>

<span data-ttu-id="a8780-105">L’attribut **editStyle** spécifie ou récupère le style du contrôle zone d’édition.</span><span class="sxs-lookup"><span data-stu-id="a8780-105">The **editStyle** attribute specifies or retrieves the style of the edit box control.</span></span>

``` syntax
        elementID.editStyle
```

## <a name="possible-values"></a><span data-ttu-id="a8780-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="a8780-106">Possible Values</span></span>

<span data-ttu-id="a8780-107">Cet attribut est une **chaîne** en lecture/écriture contenant l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="a8780-107">This attribute is a read/write **String** containing one of the following values.</span></span>



| <span data-ttu-id="a8780-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="a8780-108">Value</span></span>     | <span data-ttu-id="a8780-109">Description</span><span class="sxs-lookup"><span data-stu-id="a8780-109">Description</span></span>                                                                     |
|-----------|---------------------------------------------------------------------------------|
| <span data-ttu-id="a8780-110">normal</span><span class="sxs-lookup"><span data-stu-id="a8780-110">normal</span></span>    | <span data-ttu-id="a8780-111">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="a8780-111">Default.</span></span> <span data-ttu-id="a8780-112">Affiche le texte normal sur une seule ligne.</span><span class="sxs-lookup"><span data-stu-id="a8780-112">Displays normal text on a single line.</span></span>                                 |
| <span data-ttu-id="a8780-113">mot de passe</span><span class="sxs-lookup"><span data-stu-id="a8780-113">password</span></span>  | <span data-ttu-id="a8780-114">Affiche des astérisques ( \* ) à la place du texte.</span><span class="sxs-lookup"><span data-stu-id="a8780-114">Displays asterisks (\*) in place of text.</span></span> <span data-ttu-id="a8780-115">Peut uniquement être spécifié au moment de la conception.</span><span class="sxs-lookup"><span data-stu-id="a8780-115">Can only be specified at design time.</span></span> |
| <span data-ttu-id="a8780-116">majuscules</span><span class="sxs-lookup"><span data-stu-id="a8780-116">uppercase</span></span> | <span data-ttu-id="a8780-117">Affiche le texte en majuscules.</span><span class="sxs-lookup"><span data-stu-id="a8780-117">Displays text as all uppercase.</span></span>                                                 |
| <span data-ttu-id="a8780-118">minuscules</span><span class="sxs-lookup"><span data-stu-id="a8780-118">lowercase</span></span> | <span data-ttu-id="a8780-119">Affiche le texte en minuscules.</span><span class="sxs-lookup"><span data-stu-id="a8780-119">Displays text as all lowercase.</span></span>                                                 |
| <span data-ttu-id="a8780-120">nombre</span><span class="sxs-lookup"><span data-stu-id="a8780-120">number</span></span>    | <span data-ttu-id="a8780-121">Affiche uniquement les nombres.</span><span class="sxs-lookup"><span data-stu-id="a8780-121">Only displays numbers.</span></span>                                                          |
| <span data-ttu-id="a8780-122">lambda</span><span class="sxs-lookup"><span data-stu-id="a8780-122">multiline</span></span> | <span data-ttu-id="a8780-123">Affiche plusieurs lignes de texte.</span><span class="sxs-lookup"><span data-stu-id="a8780-123">Displays multiple lines of text.</span></span> <span data-ttu-id="a8780-124">Peut uniquement être spécifié au moment de la conception.</span><span class="sxs-lookup"><span data-stu-id="a8780-124">Can only be specified at design time.</span></span>          |



 

## <a name="remarks"></a><span data-ttu-id="a8780-125">Notes</span><span class="sxs-lookup"><span data-stu-id="a8780-125">Remarks</span></span>

<span data-ttu-id="a8780-126">Cet attribut peut uniquement être défini sur « mot de passe » ou « multiligne » au moment de la conception.</span><span class="sxs-lookup"><span data-stu-id="a8780-126">This attribute can only be set to "password" or "multiline" at design time.</span></span> <span data-ttu-id="a8780-127">S’il est défini sur « multiligne », la valeur ne peut pas être modifiée au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="a8780-127">If it is set to "multiline", the value cannot be changed at run time.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8780-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a8780-128">Requirements</span></span>



| <span data-ttu-id="a8780-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a8780-129">Requirement</span></span> | <span data-ttu-id="a8780-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="a8780-130">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="a8780-131">Version</span><span class="sxs-lookup"><span data-stu-id="a8780-131">Version</span></span><br/> | <span data-ttu-id="a8780-132">Lecteur Windows Media pour Windows XP ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="a8780-132">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a8780-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8780-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8780-134">**Élément EDITBOX**</span><span class="sxs-lookup"><span data-stu-id="a8780-134">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> </dl>

 

 





