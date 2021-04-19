---
title: TEXT. fontSmoothing
description: L’attribut fontSmoothing spécifie ou récupère une valeur indiquant si le lissage des polices est activé.
ms.assetid: bd6f0468-285e-44b3-a5e8-361744c5ce4a
keywords:
- TEXT. fontSmoothing Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.fontSmoothing
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcdf285572b4edda0f514cb3519b6953f9e94677
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532935"
---
# <a name="textfontsmoothing"></a><span data-ttu-id="17523-104">TEXT. fontSmoothing</span><span class="sxs-lookup"><span data-stu-id="17523-104">TEXT.fontSmoothing</span></span>

<span data-ttu-id="17523-105">L’attribut **fontSmoothing** spécifie ou récupère une valeur indiquant si le lissage des polices est activé.</span><span class="sxs-lookup"><span data-stu-id="17523-105">The **fontSmoothing** attribute specifies or retrieves a value indicating whether font smoothing is enabled.</span></span>

``` syntax
        elementID.fontSmoothing
```

## <a name="possible-values"></a><span data-ttu-id="17523-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="17523-106">Possible Values</span></span>

<span data-ttu-id="17523-107">Cet attribut est une **valeur booléenne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="17523-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="17523-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="17523-108">Value</span></span> | <span data-ttu-id="17523-109">Description</span><span class="sxs-lookup"><span data-stu-id="17523-109">Description</span></span>                          |
|-------|--------------------------------------|
| <span data-ttu-id="17523-110">true</span><span class="sxs-lookup"><span data-stu-id="17523-110">true</span></span>  | <span data-ttu-id="17523-111">Le lissage des polices est activé.</span><span class="sxs-lookup"><span data-stu-id="17523-111">Font smoothing is enabled.</span></span>           |
| <span data-ttu-id="17523-112">false</span><span class="sxs-lookup"><span data-stu-id="17523-112">false</span></span> | <span data-ttu-id="17523-113">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="17523-113">Default.</span></span> <span data-ttu-id="17523-114">Le lissage des polices est désactivé.</span><span class="sxs-lookup"><span data-stu-id="17523-114">Font smoothing is disabled.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="17523-115">Notes</span><span class="sxs-lookup"><span data-stu-id="17523-115">Remarks</span></span>

<span data-ttu-id="17523-116">Le lissage des polices utilise la fonctionnalité d’anticrénelage du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="17523-116">Font smoothing uses the anti-aliasing feature of the operating system.</span></span> <span data-ttu-id="17523-117">Si le lissage des polices est activé et que le système d’exploitation prend en charge l’anticrénelage, le lecteur Windows Media tente de lisser le texte.</span><span class="sxs-lookup"><span data-stu-id="17523-117">If font smoothing is enabled and the operating system supports anti-aliasing, Windows Media Player attempts to smooth the text.</span></span> <span data-ttu-id="17523-118">Toutes les polices ne prennent pas en charge l’anticrénelage.</span><span class="sxs-lookup"><span data-stu-id="17523-118">Not all fonts support anti-aliasing.</span></span> <span data-ttu-id="17523-119">Le lecteur Windows Media 10 utilise la méthode d’anticrénelage ClearType de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="17523-119">Windows Media Player 10 uses the Windows XP ClearType anti-aliasing method.</span></span>

-   <span data-ttu-id="17523-120">**Avertissement** Le lissage des polices sur une couleur transparente peut entraîner la fusion de la couleur transparente dans les caractères.</span><span class="sxs-lookup"><span data-stu-id="17523-120">**Warning** Font smoothing over a transparent color may cause the transparent color to blend into the characters.</span></span> <span data-ttu-id="17523-121">Il n’est pas recommandé d’utiliser **fontSmoothing** si le texte s’affiche sur une transparence.</span><span class="sxs-lookup"><span data-stu-id="17523-121">It is not recommended that you use **fontSmoothing** if the text will display over a transparency.</span></span>

<span data-ttu-id="17523-122">Pour obtenir un exemple illustrant l’utilisation des attributs de l’élément de **texte** , consultez l’attribut [value](text-value.md) .</span><span class="sxs-lookup"><span data-stu-id="17523-122">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="17523-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="17523-123">Requirements</span></span>



| <span data-ttu-id="17523-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="17523-124">Requirement</span></span> | <span data-ttu-id="17523-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="17523-125">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="17523-126">Version</span><span class="sxs-lookup"><span data-stu-id="17523-126">Version</span></span><br/> | <span data-ttu-id="17523-127">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="17523-127">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="17523-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17523-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17523-129">**Élément de texte**</span><span class="sxs-lookup"><span data-stu-id="17523-129">**TEXT Element**</span></span>](text-element.md)
</dt> </dl>

 

 





