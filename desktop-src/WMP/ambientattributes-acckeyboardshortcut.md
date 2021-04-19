---
title: AmbientAttributes.accKeyboardShortcut
description: L’attribut accKeyboardShortcut spécifie ou récupère une description de raccourci clavier pour tout élément.
ms.assetid: f97cffc9-4e7c-4226-9e02-0ea7f84b7450
keywords:
- Lecteur Windows Media AmbientAttributes. accKeyboardShortcut
topic_type:
- apiref
api_name:
- AmbientAttributes.accKeyboardShortcut
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67d7259f0b32e3575d902a83b6508383361028d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532217"
---
# <a name="ambientattributesacckeyboardshortcut"></a><span data-ttu-id="134f4-104">AmbientAttributes.accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="134f4-104">AmbientAttributes.accKeyboardShortcut</span></span>

<span data-ttu-id="134f4-105">L’attribut **accKeyboardShortcut** spécifie ou récupère une description de raccourci clavier pour tout élément.</span><span class="sxs-lookup"><span data-stu-id="134f4-105">The **accKeyboardShortcut** attribute specifies or retrieves a keyboard shortcut description for any element.</span></span>

``` syntax
        elementID.accKeyboardShortcut
```

## <a name="possible-values"></a><span data-ttu-id="134f4-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="134f4-106">Possible Values</span></span>

<span data-ttu-id="134f4-107">Cet attribut est une **chaîne** en lecture/écriture dont la valeur par défaut est «» (chaîne vide).</span><span class="sxs-lookup"><span data-stu-id="134f4-107">This attribute is a read/write **String** with a default value of "" (empty string).</span></span> <span data-ttu-id="134f4-108">Pour l’élément **Button** , cet attribut a une valeur par défaut « espace ou entrée ».</span><span class="sxs-lookup"><span data-stu-id="134f4-108">For the **BUTTON** element, this attribute has a default value of "Spacebar or Enter".</span></span> <span data-ttu-id="134f4-109">Pour l’élément **Slider** , la valeur par défaut est « flèche droite/haut pour augmenter, flèche gauche/bas pour diminuer ».</span><span class="sxs-lookup"><span data-stu-id="134f4-109">For the **SLIDER** element, the default value is "Right/Up Arrow to increase, Left/Down Arrow to decrease".</span></span>

## <a name="remarks"></a><span data-ttu-id="134f4-110">Notes</span><span class="sxs-lookup"><span data-stu-id="134f4-110">Remarks</span></span>

<span data-ttu-id="134f4-111">Cet attribut est utilisé à des fins d’accessibilité.</span><span class="sxs-lookup"><span data-stu-id="134f4-111">This attribute is used for accessibility purposes.</span></span> <span data-ttu-id="134f4-112">Il permet d’obtenir une description du raccourci clavier pour tout élément à lire à voix haute par un programme de lecture.</span><span class="sxs-lookup"><span data-stu-id="134f4-112">It allows a description of the keyboard shortcut for any element to be read aloud by a reader program.</span></span> <span data-ttu-id="134f4-113">Cet attribut ne définit pas le raccourci.</span><span class="sxs-lookup"><span data-stu-id="134f4-113">This attribute does not set the shortcut.</span></span> <span data-ttu-id="134f4-114">Le scripteur doit effectuer cette tâche.</span><span class="sxs-lookup"><span data-stu-id="134f4-114">The scripter must do that work.</span></span>

<span data-ttu-id="134f4-115">Cet attribut s’applique également aux éléments de bouton à l’intérieur du contrôle de groupe de boutons.</span><span class="sxs-lookup"><span data-stu-id="134f4-115">This attribute also applies to button elements inside the button group control.</span></span>

## <a name="requirements"></a><span data-ttu-id="134f4-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="134f4-116">Requirements</span></span>



| <span data-ttu-id="134f4-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="134f4-117">Requirement</span></span> | <span data-ttu-id="134f4-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="134f4-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="134f4-119">Version</span><span class="sxs-lookup"><span data-stu-id="134f4-119">Version</span></span><br/> | <span data-ttu-id="134f4-120">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="134f4-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="134f4-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="134f4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="134f4-122">**Attributs ambiants**</span><span class="sxs-lookup"><span data-stu-id="134f4-122">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





