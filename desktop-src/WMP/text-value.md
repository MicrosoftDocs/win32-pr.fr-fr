---
title: TEXT. Value
description: L’attribut value spécifie ou récupère le texte affiché dans le contrôle de texte.
ms.assetid: dbc50be2-ee18-4661-a343-9e906879aba0
keywords:
- TEXT. Value lecteur Windows Media
topic_type:
- apiref
api_name:
- TEXT.value
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d87f688f7afffeb588a37ac13ebff4cdc7cc105
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525451"
---
# <a name="textvalue"></a><span data-ttu-id="be8d8-104">TEXT. Value</span><span class="sxs-lookup"><span data-stu-id="be8d8-104">TEXT.value</span></span>

<span data-ttu-id="be8d8-105">L’attribut **value** spécifie ou récupère le texte affiché dans le contrôle de texte.</span><span class="sxs-lookup"><span data-stu-id="be8d8-105">The **value** attribute specifies or retrieves the text that is displayed in the Text control.</span></span>

``` syntax
        elementID.value
```

## <a name="possible-values"></a><span data-ttu-id="be8d8-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="be8d8-106">Possible Values</span></span>

<span data-ttu-id="be8d8-107">Cet attribut est une **chaîne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="be8d8-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="be8d8-108">Notes</span><span class="sxs-lookup"><span data-stu-id="be8d8-108">Remarks</span></span>

<span data-ttu-id="be8d8-109">Si la largeur du contrôle de texte est insuffisante pour contenir le texte fourni, le texte est rogné et des points de suspension s’affichent pour illustrer le fait.</span><span class="sxs-lookup"><span data-stu-id="be8d8-109">If the width of the Text control is insufficient to contain the text provided, the text is cropped, and an ellipsis is shown to illustrate the fact.</span></span> <span data-ttu-id="be8d8-110">Si l’attribut **ToolTip** n’a pas été défini, le texte complet s’affiche alors sous la forme d’une info-bulle lorsque le curseur pointe sur le contrôle.</span><span class="sxs-lookup"><span data-stu-id="be8d8-110">If the **toolTip** attribute has not been set, the complete text will then appear as a ToolTip when the cursor hovers over the control.</span></span>

<span data-ttu-id="be8d8-111">Si aucune largeur n’est spécifiée, la largeur par défaut du contrôle correspond à la largeur de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="be8d8-111">If a width is not specified, the default width for the control is the width of the string.</span></span>

<span data-ttu-id="be8d8-112">Si la hauteur du contrôle n’est pas spécifiée, la hauteur par défaut est une ligne.</span><span class="sxs-lookup"><span data-stu-id="be8d8-112">If the height of the control is not specified, the default height is one line.</span></span>

<span data-ttu-id="be8d8-113">Si l’attribut **wordWrap** a la valeur true et que la hauteur du contrôle est suffisante pour accueillir une autre ligne de texte, le texte est renvoyé à la ligne suivante.</span><span class="sxs-lookup"><span data-stu-id="be8d8-113">If the **wordWrap** attribute is set to true and the height of the control is enough to accommodate another line of text, the text wraps to a subsequent line.</span></span> <span data-ttu-id="be8d8-114">L’encapsulage se produit uniquement entre les mots.</span><span class="sxs-lookup"><span data-stu-id="be8d8-114">Wrapping only occurs between words.</span></span> <span data-ttu-id="be8d8-115">Les sauts de ligne peuvent également être forcés, comme expliqué sous **wordWrap**.</span><span class="sxs-lookup"><span data-stu-id="be8d8-115">Line breaks may also be forced, as explained under **wordWrap**.</span></span>

## <a name="examples"></a><span data-ttu-id="be8d8-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="be8d8-116">Examples</span></span>

<span data-ttu-id="be8d8-117">L’exemple suivant est un fichier de définition d’apparence complet qui illustre l’utilisation des attributs de l’élément de **texte** .</span><span class="sxs-lookup"><span data-stu-id="be8d8-117">The following sample is a complete skin definition file that illustrates how the attributes of the **TEXT** element are used.</span></span> <span data-ttu-id="be8d8-118">Il se trouve dans le répertoire d’exemples qui a été installé avec le kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="be8d8-118">It can be found in the Samples directory that was installed with the SDK.</span></span>


```C++
<THEME>
  <VIEW
    height = "175"
  >
    <TEXT 
      width = "150"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      disabledForegroundColor = "#CCCCCC"
      justification = "Center"
      value = "Play"
      cursor = "hand"
      enabled = "wmpenabled:player.controls.play"
      onClick = "JScript: player.URL='https://proseware.com/laure.wma';"
    />
    <TEXT
      top = "50"
      width = "150"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      disabledForegroundColor = "#CCCCCC"
      justification = "Center"
      value = "Stop"
      cursor = "hand"
      enabled = "wmpenabled:player.controls.stop"
      onClick = "JScript: player.controls.stop();"
    />
    <TEXT
      top = "100"
      width = "150"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      justification = "Center"
      value = "Close"
      cursor = "hand"
      onClick = "JScript: view.close();"
    />
    <TEXT
      top = "30"
      left = "120"
      width = "200"
      fontSize = "20"
      fontStyle = "Underline"
      justification = "Center"
      value = "Volume"
    />
    <TEXT
      top = "60"
      left = "120"
      width = "200"
      fontSize = "40"
      justification = "Center"
      value = "wmpprop:player.settings.volume"
    />
    <TEXT
      top = "65"
      left = "142"
      width = "40"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      justification = "Center"
      value = "-"
      cursor = "hand"
      toolTip = "decrease volume"
      onClick = "player.settings.volume = player.settings.volume - 5"
    />
    <TEXT
      top = "65"
      left = "260"
      width = "40"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      justification = "Center"
      value = "+"
      cursor = "hand"
      toolTip = "increase volume"
      onClick = "player.settings.volume = player.settings.volume + 5"
    />
    <TEXT
      top = "155"
      width = "300"
      height = "30"
      fontFace = "System"
      backgroundColor = "blue"
      foregroundColor = "white"
      justification = "Center"
      scrolling = "true"
      scrollingAmount = "1"
      scrollingDelay = "50"
      value = "wmpprop:player.status"
    />
  </VIEW>
</THEME>

```



## <a name="requirements"></a><span data-ttu-id="be8d8-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="be8d8-119">Requirements</span></span>



| <span data-ttu-id="be8d8-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="be8d8-120">Requirement</span></span> | <span data-ttu-id="be8d8-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="be8d8-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="be8d8-122">Version</span><span class="sxs-lookup"><span data-stu-id="be8d8-122">Version</span></span><br/> | <span data-ttu-id="be8d8-123">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="be8d8-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="be8d8-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be8d8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be8d8-125">**Élément de texte**</span><span class="sxs-lookup"><span data-stu-id="be8d8-125">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="be8d8-126">**TEXT. toolTip**</span><span class="sxs-lookup"><span data-stu-id="be8d8-126">**TEXT.toolTip**</span></span>](text-tooltip.md)
</dt> <dt>

[<span data-ttu-id="be8d8-127">**TEXT. wordWrap**</span><span class="sxs-lookup"><span data-stu-id="be8d8-127">**TEXT.wordWrap**</span></span>](text-wordwrap.md)
</dt> </dl>

 

 





