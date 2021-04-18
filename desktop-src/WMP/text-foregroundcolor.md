---
title: TEXT. foregroundColor
description: L’attribut foregroundColor spécifie ou récupère la couleur de texte du contrôle de texte.
ms.assetid: 1ddbad93-fbff-4be6-9797-6594b5f09a1e
keywords:
- TEXT. foregroundColor Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.foregroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e452a18a085337e8cbf0ec88567d6a57a0a498a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532969"
---
# <a name="textforegroundcolor"></a><span data-ttu-id="c10d7-104">TEXT. foregroundColor</span><span class="sxs-lookup"><span data-stu-id="c10d7-104">TEXT.foregroundColor</span></span>

<span data-ttu-id="c10d7-105">L’attribut **foregroundColor** spécifie ou récupère la couleur de texte du contrôle de texte.</span><span class="sxs-lookup"><span data-stu-id="c10d7-105">The **foregroundColor** attribute specifies or retrieves the text color for the Text control.</span></span>

``` syntax
        elementID.foregroundColor
```

## <a name="possible-values"></a><span data-ttu-id="c10d7-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="c10d7-106">Possible Values</span></span>

<span data-ttu-id="c10d7-107">Cet attribut est une **chaîne** en lecture/écriture contenant toute valeur de couleur Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="c10d7-107">This attribute is a read/write **String** containing any Microsoft Internet Explorer color value.</span></span> <span data-ttu-id="c10d7-108">La valeur par défaut est « Black ».</span><span class="sxs-lookup"><span data-stu-id="c10d7-108">The default value is "black".</span></span>

<span data-ttu-id="c10d7-109">Pour obtenir un exemple illustrant l’utilisation des attributs de l’élément de **texte** , consultez l’attribut [value](text-value.md) .</span><span class="sxs-lookup"><span data-stu-id="c10d7-109">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

<span data-ttu-id="c10d7-110">Quand vous utilisez **alphaBlend** ou **alphaBlendTo** avec un élément de **texte** pour lequel le **backgroundColor** n’est pas spécifié, une couleur d’arrière-plan noire est utilisée.</span><span class="sxs-lookup"><span data-stu-id="c10d7-110">When you use **alphaBlend** or **alphaBlendTo** with a **TEXT** element that does not have the **backgroundColor** specified, a background color of black will be used.</span></span> <span data-ttu-id="c10d7-111">Si la couleur de premier plan est également noire (valeur par défaut pour l’attribut **foregroundColor** ), votre texte peut devenir illisible.</span><span class="sxs-lookup"><span data-stu-id="c10d7-111">If the foreground color is also black (which is the default value for the **foregroundColor** attribute), your text may become unreadable.</span></span> <span data-ttu-id="c10d7-112">Pour éviter cela, spécifiez toujours l’attribut **backgroundColor** ou définissez **foregroundColor** sur une couleur autre que Black.</span><span class="sxs-lookup"><span data-stu-id="c10d7-112">To prevent this, always specify the **backgroundColor** attribute, or set **foregroundColor** to a color other than black.</span></span>

## <a name="requirements"></a><span data-ttu-id="c10d7-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c10d7-113">Requirements</span></span>



| <span data-ttu-id="c10d7-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c10d7-114">Requirement</span></span> | <span data-ttu-id="c10d7-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="c10d7-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="c10d7-116">Version</span><span class="sxs-lookup"><span data-stu-id="c10d7-116">Version</span></span><br/> | <span data-ttu-id="c10d7-117">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="c10d7-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c10d7-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c10d7-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c10d7-119">**AmbientAttributes. alphaBlend**</span><span class="sxs-lookup"><span data-stu-id="c10d7-119">**AmbientAttributes.alphaBlend**</span></span>](ambientattributes-alphablend.md)
</dt> <dt>

[<span data-ttu-id="c10d7-120">**AmbientAttributes.alphaBlendTo**</span><span class="sxs-lookup"><span data-stu-id="c10d7-120">**AmbientAttributes.alphaBlendTo**</span></span>](ambientattributes-alphablendto.md)
</dt> <dt>

[<span data-ttu-id="c10d7-121">**Référence de couleur**</span><span class="sxs-lookup"><span data-stu-id="c10d7-121">**Color Reference**</span></span>](color-reference.md)
</dt> <dt>

[<span data-ttu-id="c10d7-122">**Élément de texte**</span><span class="sxs-lookup"><span data-stu-id="c10d7-122">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="c10d7-123">**TEXT. backgroundColor**</span><span class="sxs-lookup"><span data-stu-id="c10d7-123">**TEXT.backgroundColor**</span></span>](text-backgroundcolor.md)
</dt> </dl>

 

 





