---
title: AmbientAttributes. alphaBlend
description: L’attribut alphaBlend spécifie ou récupère une valeur pour la fusion alpha d’une vue, d’une sous-vue ou d’un widget d’interface utilisateur.
ms.assetid: a6c47d32-a497-4bfa-8fa3-ef94e267d94b
keywords:
- Lecteur Windows Media AmbientAttributes. alphaBlend
topic_type:
- apiref
api_name:
- AmbientAttributes.alphaBlend
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8c0f0cb9d885f643b39acfbc5148403a5c8b788
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533178"
---
# <a name="ambientattributesalphablend"></a><span data-ttu-id="a88a7-104">AmbientAttributes. alphaBlend</span><span class="sxs-lookup"><span data-stu-id="a88a7-104">AmbientAttributes.alphaBlend</span></span>

<span data-ttu-id="a88a7-105">L’attribut **alphaBlend** spécifie ou récupère une valeur pour la fusion alpha d’une **vue**, d’une sous- **vue** ou d’un widget d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a88a7-105">The **alphaBlend** attribute specifies or retrieves a value for alpha blending any **VIEW**, **SUBVIEW**, or UI widget.</span></span>

``` syntax
        elementID.alphaBlend
```

## <a name="possible-values"></a><span data-ttu-id="a88a7-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="a88a7-106">Possible Values</span></span>

<span data-ttu-id="a88a7-107">Cet attribut est un **nombre** en lecture/écriture (**long**) dont la valeur est comprise entre 0 (aucune opacité) et 255 (opacité complète) et une valeur par défaut de 255.</span><span class="sxs-lookup"><span data-stu-id="a88a7-107">This attribute is a read/write **Number** (**long**) with a value ranging from 0 (no opacity) to 255 (full opacity) and a default value of 255.</span></span>

## <a name="remarks"></a><span data-ttu-id="a88a7-108">Notes</span><span class="sxs-lookup"><span data-stu-id="a88a7-108">Remarks</span></span>

<span data-ttu-id="a88a7-109">Cet attribut permet à un élément d’apparaître comme translucide, en fonction de la quantité d’opacité définie.</span><span class="sxs-lookup"><span data-stu-id="a88a7-109">This attribute allows an element to appear semitransparent, depending on the amount of opacity set.</span></span> <span data-ttu-id="a88a7-110">Moins l’opacité est faible, plus l’élément est transparent.</span><span class="sxs-lookup"><span data-stu-id="a88a7-110">The less opacity, the more transparent the element will appear.</span></span> <span data-ttu-id="a88a7-111">Chaque élément de l’apparence peut avoir une valeur d’opacité distincte, à l’exception des éléments de bouton dans un contrôle **BUTTONGROUP** .</span><span class="sxs-lookup"><span data-stu-id="a88a7-111">Each element in the skin can have a separate opacity value except for button elements in a **BUTTONGROUP** control.</span></span> <span data-ttu-id="a88a7-112">Quand **alphaBlend** est défini dans la **vue**, l’opacité de la totalité de l’apparence est définie.</span><span class="sxs-lookup"><span data-stu-id="a88a7-112">When **alphaBlend** is set in **VIEW**, the opacity of the entire skin will be set.</span></span> <span data-ttu-id="a88a7-113">Alpha Blend ne fonctionne pas pour les contrôles avec fenêtres, y compris les **sélections**, les **effets**, la zone de liste, les **menus contextuels** **, les** **zones** d’édition et les **vidéos** (si l’absence de **fenêtre** est définie sur false).</span><span class="sxs-lookup"><span data-stu-id="a88a7-113">Alpha blend will not work for windowed controls, including **PLAYLIST**, **EFFECTS**, **LISTBOX**, **POPUP**, **EDITBOX**, and **VIDEO** (if **windowless** is set to false).</span></span> <span data-ttu-id="a88a7-114">Quand **alphaBlend** est défini sur **View**, la totalité de la peau devient transparente.</span><span class="sxs-lookup"><span data-stu-id="a88a7-114">When **alphaBlend** is set on **VIEW**, the whole skin becomes transparent.</span></span> <span data-ttu-id="a88a7-115">Les attributs **transparencyColor** utilisés par plusieurs éléments ne sont pas pris en charge par **alphaBlend**.</span><span class="sxs-lookup"><span data-stu-id="a88a7-115">The **transparencyColor** attributes used by several elements are not supported with **alphaBlend**.</span></span>

<span data-ttu-id="a88a7-116">Lorsque vous utilisez **alphaBlend** avec un élément de **texte** pour lequel le **backgroundColor** n’est pas spécifié, une couleur d’arrière-plan noire est utilisée.</span><span class="sxs-lookup"><span data-stu-id="a88a7-116">When you use **alphaBlend** with a **TEXT** element that does not have the **backgroundColor** specified, a background color of black will be used.</span></span> <span data-ttu-id="a88a7-117">Si la couleur de premier plan est également noire (valeur par défaut pour le *texte*).**foregroundColor**), votre texte peut devenir illisible.</span><span class="sxs-lookup"><span data-stu-id="a88a7-117">If the foreground color is also black (which is the default value for *TEXT*.**foregroundColor**), your text may become unreadable.</span></span> <span data-ttu-id="a88a7-118">Pour éviter cela, spécifiez toujours l’attribut **backgroundColor** ou définissez **foregroundColor** sur une couleur autre que Black.</span><span class="sxs-lookup"><span data-stu-id="a88a7-118">To prevent this, always specify the **backgroundColor** attribute, or set **foregroundColor** to a color other than black.</span></span>

> [!Note]  
> <span data-ttu-id="a88a7-119">Cet attribut n’est pas pris en charge dans Windows 98.</span><span class="sxs-lookup"><span data-stu-id="a88a7-119">This attribute is not supported in Windows 98.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a88a7-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a88a7-120">Requirements</span></span>



| <span data-ttu-id="a88a7-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a88a7-121">Requirement</span></span> | <span data-ttu-id="a88a7-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="a88a7-122">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="a88a7-123">Version</span><span class="sxs-lookup"><span data-stu-id="a88a7-123">Version</span></span><br/> | <span data-ttu-id="a88a7-124">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="a88a7-124">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a88a7-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a88a7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a88a7-126">**Attributs ambiants**</span><span class="sxs-lookup"><span data-stu-id="a88a7-126">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="a88a7-127">**AmbientAttributes.alphaBlendTo**</span><span class="sxs-lookup"><span data-stu-id="a88a7-127">**AmbientAttributes.alphaBlendTo**</span></span>](ambientattributes-alphablendto.md)
</dt> <dt>

[<span data-ttu-id="a88a7-128">**Élément de texte**</span><span class="sxs-lookup"><span data-stu-id="a88a7-128">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="a88a7-129">**TEXT. backgroundColor**</span><span class="sxs-lookup"><span data-stu-id="a88a7-129">**TEXT.backgroundColor**</span></span>](text-backgroundcolor.md)
</dt> <dt>

[<span data-ttu-id="a88a7-130">**TEXT. foregroundColor**</span><span class="sxs-lookup"><span data-stu-id="a88a7-130">**TEXT.foregroundColor**</span></span>](text-foregroundcolor.md)
</dt> </dl>

 

 





