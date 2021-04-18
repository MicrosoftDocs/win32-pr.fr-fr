---
title: TEXT. wordWrap
description: L’attribut wordWrap spécifie ou récupère une valeur indiquant si le retour automatique à la ligne est activé ou désactivé.
ms.assetid: 3bb127d8-42f1-4167-986a-d41690cb5647
keywords:
- TEXT. wordWrap lecteur Windows Media
topic_type:
- apiref
api_name:
- TEXT.wordWrap
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff2b4d030a7e9efdda1bc7503ae3bf8eb5985401
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533430"
---
# <a name="textwordwrap"></a><span data-ttu-id="b964c-104">TEXT. wordWrap</span><span class="sxs-lookup"><span data-stu-id="b964c-104">TEXT.wordWrap</span></span>

<span data-ttu-id="b964c-105">L’attribut **wordWrap** spécifie ou récupère une valeur indiquant si le retour automatique à la ligne est activé ou désactivé.</span><span class="sxs-lookup"><span data-stu-id="b964c-105">The **wordWrap** attribute specifies or retrieves a value indicating whether word wrap is enabled or disabled.</span></span>

``` syntax
        elementID.wordWrap
```

## <a name="possible-values"></a><span data-ttu-id="b964c-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="b964c-106">Possible Values</span></span>

<span data-ttu-id="b964c-107">Cet attribut est une **valeur booléenne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="b964c-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="b964c-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="b964c-108">Value</span></span> | <span data-ttu-id="b964c-109">Description</span><span class="sxs-lookup"><span data-stu-id="b964c-109">Description</span></span>                                                                                       |
|-------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b964c-110">true</span><span class="sxs-lookup"><span data-stu-id="b964c-110">true</span></span>  | <span data-ttu-id="b964c-111">Le retour automatique à la ligne est activé.</span><span class="sxs-lookup"><span data-stu-id="b964c-111">Word wrap is enabled.</span></span>                                                                             |
| <span data-ttu-id="b964c-112">false</span><span class="sxs-lookup"><span data-stu-id="b964c-112">false</span></span> | <span data-ttu-id="b964c-113">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="b964c-113">Default.</span></span> <span data-ttu-id="b964c-114">Le retour automatique à la ligne est désactivé.</span><span class="sxs-lookup"><span data-stu-id="b964c-114">Word wrap is disabled.</span></span> <span data-ttu-id="b964c-115">Si le texte ne tient pas dans le contrôle, le texte est rogné.</span><span class="sxs-lookup"><span data-stu-id="b964c-115">If the text does not fit within the control, the text is cropped.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b964c-116">Notes</span><span class="sxs-lookup"><span data-stu-id="b964c-116">Remarks</span></span>

<span data-ttu-id="b964c-117">Le contrôle Text ne sépare pas les mots.</span><span class="sxs-lookup"><span data-stu-id="b964c-117">The Text control does not split words apart.</span></span> <span data-ttu-id="b964c-118">Si un mot dépasse la largeur du contrôle, le retour automatique à la ligne est utilisé pour déplacer le mot vers la ligne suivante.</span><span class="sxs-lookup"><span data-stu-id="b964c-118">If a word extends beyond the width of the control, word wrap is employed to move the word to the next line.</span></span> <span data-ttu-id="b964c-119">Si un mot unique est plus long que la largeur du contrôle, ce mot est coupé et occupe une seule ligne.</span><span class="sxs-lookup"><span data-stu-id="b964c-119">If a single word is longer than the control width, that word is clipped and occupies a single line.</span></span>

<span data-ttu-id="b964c-120">Si l’attribut **Width** n’est pas spécifié, **wordWrap** est ignorée et le contrôle Text est redimensionné au lieu d’habiller le texte.</span><span class="sxs-lookup"><span data-stu-id="b964c-120">If the **width** attribute is not specified, **wordWrap** is ignored and the Text control will resize rather than wrapping the text.</span></span>

<span data-ttu-id="b964c-121">Si des sauts de ligne sont souhaités dans des emplacements particuliers, ils doivent être spécifiés explicitement dans la **valeur** à l’aide de « &\# 13 ; » ou « \\ r ».</span><span class="sxs-lookup"><span data-stu-id="b964c-121">If line breaks are desired in particular locations, they must be explicitly specified in **value** using "&\#13;" or "\\r".</span></span> <span data-ttu-id="b964c-122">Si la dernière forme est utilisée lors de la spécification directe de la valeur, la chaîne doit être précédée de « JScript : » et la valeur réelle doit être entourée de guillemets simples, comme indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="b964c-122">If the latter form is used when specifying the value directly, the string must be prefixed with "JScript:" and the actual value must be surrounded by single quotes, as shown below.</span></span> <span data-ttu-id="b964c-123">Cela n’est pas nécessaire si la valeur est définie dynamiquement à partir d’un gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="b964c-123">This is not necessary if the value is set dynamically from within an event handler.</span></span>

<span data-ttu-id="b964c-124">Si **wordWrap** a la valeur true et que l' **info-bulle** n’est pas spécifiée, l’info-bulle affiche le texte complet de l’attribut **value** .</span><span class="sxs-lookup"><span data-stu-id="b964c-124">If **wordWrap** is set to true and **toolTip** is not specified, the ToolTip will display the full text of the **value** attribute.</span></span> <span data-ttu-id="b964c-125">Si aucune info-bulle n’est souhaitée, affectez la valeur "" (chaîne vide) à l' **info-bulle** .</span><span class="sxs-lookup"><span data-stu-id="b964c-125">If no ToolTip is desired, set **toolTip** to "" (empty string).</span></span>

## <a name="examples"></a><span data-ttu-id="b964c-126">Exemples</span><span class="sxs-lookup"><span data-stu-id="b964c-126">Examples</span></span>


```C++
<THEME>
  <VIEW>
    <TEXT
      width = "50"
      height = "200"
      wordWrap = "true"
      backgroundColor = "blue"
      foregroundColor = "white"
      value = "This is a test.&#13;&#13;It is only a test."
    />
    <TEXT
      width = "50"
      height = "200"
      left = "100"
      wordWrap = "true"
      backgroundColor = "green"
      foregroundColor = "white"
      value = "JScript:'This is a test.\r\rIt is only a test.'"
    />
  </VIEW>
</THEME>

```



## <a name="requirements"></a><span data-ttu-id="b964c-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b964c-127">Requirements</span></span>



| <span data-ttu-id="b964c-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b964c-128">Requirement</span></span> | <span data-ttu-id="b964c-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="b964c-129">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="b964c-130">Version</span><span class="sxs-lookup"><span data-stu-id="b964c-130">Version</span></span><br/> | <span data-ttu-id="b964c-131">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="b964c-131">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b964c-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b964c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b964c-133">**AmbientAttributes. Width**</span><span class="sxs-lookup"><span data-stu-id="b964c-133">**AmbientAttributes.width**</span></span>](ambientattributes-width.md)
</dt> <dt>

[<span data-ttu-id="b964c-134">**Élément de texte**</span><span class="sxs-lookup"><span data-stu-id="b964c-134">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="b964c-135">**TEXT. toolTip**</span><span class="sxs-lookup"><span data-stu-id="b964c-135">**TEXT.toolTip**</span></span>](text-tooltip.md)
</dt> <dt>

[<span data-ttu-id="b964c-136">**TEXT. Value**</span><span class="sxs-lookup"><span data-stu-id="b964c-136">**TEXT.value**</span></span>](text-value.md)
</dt> </dl>

 

 





