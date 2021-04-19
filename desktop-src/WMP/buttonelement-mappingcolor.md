---
title: BUTTONELEMENT. mappingColor
description: L’attribut mappingColor spécifie ou récupère la clé de couleur qui identifie ce BUTTONELEMENT dans le BUTTONGROUP.
ms.assetid: e7b1663c-3263-41d5-9a69-4cf1dcf0fc1f
keywords:
- Lecteur Windows Media BUTTONELEMENT. mappingColor
topic_type:
- apiref
api_name:
- BUTTONELEMENT.mappingColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7318f01246578fe8ff34118427c95afb7b3bb098
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544418"
---
# <a name="buttonelementmappingcolor"></a><span data-ttu-id="53ef1-104">BUTTONELEMENT. mappingColor</span><span class="sxs-lookup"><span data-stu-id="53ef1-104">BUTTONELEMENT.mappingColor</span></span>

<span data-ttu-id="53ef1-105">L’attribut **mappingColor** spécifie ou récupère la clé de couleur qui identifie ce **BUTTONELEMENT** dans le **BUTTONGROUP**.</span><span class="sxs-lookup"><span data-stu-id="53ef1-105">The **mappingColor** attribute specifies or retrieves the color key that identifies this **BUTTONELEMENT** in the **BUTTONGROUP**.</span></span>

``` syntax
        elementID.mappingColor
```

## <a name="possible-values"></a><span data-ttu-id="53ef1-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="53ef1-106">Possible Values</span></span>

<span data-ttu-id="53ef1-107">Cet attribut est une **chaîne** en lecture/écriture contenant toute valeur de couleur Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="53ef1-107">This attribute is a read/write **String** containing any Microsoft Internet Explorer color value.</span></span> <span data-ttu-id="53ef1-108">Il n'a aucune valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="53ef1-108">It has no default value.</span></span>

## <a name="remarks"></a><span data-ttu-id="53ef1-109">Notes</span><span class="sxs-lookup"><span data-stu-id="53ef1-109">Remarks</span></span>

<span data-ttu-id="53ef1-110">Cet attribut spécifie la couleur de la région dans le groupe de boutons **mappingImage** qui correspond à cet élément de bouton.</span><span class="sxs-lookup"><span data-stu-id="53ef1-110">This attribute specifies the color of the region in the button group **mappingImage** that corresponds to this button element.</span></span> <span data-ttu-id="53ef1-111">Tous les clics sur cette région sont gérés par cet élément bouton.</span><span class="sxs-lookup"><span data-stu-id="53ef1-111">All clicks on this region are handled by this button element.</span></span>

<span data-ttu-id="53ef1-112">Si une couleur non valide est spécifiée, le **BUTTONELEMENT** n’est pas activé.</span><span class="sxs-lookup"><span data-stu-id="53ef1-112">If an invalid color is specified, the **BUTTONELEMENT** is not activated.</span></span>

## <a name="examples"></a><span data-ttu-id="53ef1-113">Exemples</span><span class="sxs-lookup"><span data-stu-id="53ef1-113">Examples</span></span>

<span data-ttu-id="53ef1-114">L’exemple suivant est un fichier de définition d’apparence complet qui illustre l’utilisation de certains des attributs **BUTTONELEMENT** .</span><span class="sxs-lookup"><span data-stu-id="53ef1-114">The following sample is a complete skin definition file that illustrates how some of the **BUTTONELEMENT** attributes are used.</span></span> <span data-ttu-id="53ef1-115">Il se trouve dans le répertoire d’exemples qui a été installé avec le kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="53ef1-115">It can be found in the Samples directory that was installed with the SDK.</span></span>


```
<THEME>
  <VIEW
    backgroundImage = "background.bmp"
    titleBar = "False"
  >
    <PLAYER
      URL = "https://proseware.com/mellow.wma"
    />
    <EFFECTS
      id = "myeffects"
      top = "25"
      left = "88"
      width = "180"
      height = "150"
    />
    <BUTTONGROUP
      mappingImage = "map.bmp"
      hoverImage = "hover.bmp"
    >
      <BUTTONELEMENT
        mappingColor = "#00FF00"
        upToolTip = "Next"
        onClick = "JScript:myeffects.next();"
      />
      <BUTTONELEMENT
        mappingColor = "#FF0000"
        upToolTip = "Previous"
        onClick = "JScript:myeffects.previous();"
      />
    </BUTTONGROUP>
  </VIEW>
</THEME>

```



## <a name="requirements"></a><span data-ttu-id="53ef1-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="53ef1-116">Requirements</span></span>



| <span data-ttu-id="53ef1-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="53ef1-117">Requirement</span></span> | <span data-ttu-id="53ef1-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="53ef1-118">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="53ef1-119">Version</span><span class="sxs-lookup"><span data-stu-id="53ef1-119">Version</span></span><br/> | <span data-ttu-id="53ef1-120">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="53ef1-120">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="53ef1-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53ef1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53ef1-122">**Référence de couleur**</span><span class="sxs-lookup"><span data-stu-id="53ef1-122">**Color Reference**</span></span>](color-reference.md)
</dt> <dt>

[<span data-ttu-id="53ef1-123">**Élément BUTTONELEMENT**</span><span class="sxs-lookup"><span data-stu-id="53ef1-123">**BUTTONELEMENT Element**</span></span>](buttonelement-element.md)
</dt> <dt>

[<span data-ttu-id="53ef1-124">**BUTTONGROUP. mappingImage**</span><span class="sxs-lookup"><span data-stu-id="53ef1-124">**BUTTONGROUP.mappingImage**</span></span>](buttongroup-mappingimage.md)
</dt> </dl>

 

 





