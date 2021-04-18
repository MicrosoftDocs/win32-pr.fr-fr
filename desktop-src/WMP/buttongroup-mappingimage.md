---
title: BUTTONGROUP. mappingImage
description: L’attribut mappingImage spécifie ou récupère le nom de l’image représentant le mappage de bouton du BUTTONGROUP.
ms.assetid: bfea52d1-0e7f-4f77-a212-d34e356a4d85
keywords:
- Lecteur Windows Media BUTTONGROUP. mappingImage
topic_type:
- apiref
api_name:
- BUTTONGROUP.mappingImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26e4afc44a00d5ce9b15ee01d4a0dc1aff52c555
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106522818"
---
# <a name="buttongroupmappingimage"></a><span data-ttu-id="7c05d-104">BUTTONGROUP. mappingImage</span><span class="sxs-lookup"><span data-stu-id="7c05d-104">BUTTONGROUP.mappingImage</span></span>

<span data-ttu-id="7c05d-105">L’attribut **mappingImage** spécifie ou récupère le nom de l’image représentant le mappage de bouton du **BUTTONGROUP**.</span><span class="sxs-lookup"><span data-stu-id="7c05d-105">The **mappingImage** attribute specifies or retrieves the name of the image representing the button map of the **BUTTONGROUP**.</span></span>

``` syntax
        elementID.mappingImage
```

## <a name="possible-values"></a><span data-ttu-id="7c05d-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="7c05d-106">Possible Values</span></span>

<span data-ttu-id="7c05d-107">Cet attribut est une **chaîne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="7c05d-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c05d-108">Notes</span><span class="sxs-lookup"><span data-stu-id="7c05d-108">Remarks</span></span>

<span data-ttu-id="7c05d-109">Il s’agit d’un attribut obligatoire qui doit être spécifié.</span><span class="sxs-lookup"><span data-stu-id="7c05d-109">This is a mandatory attribute that must be specified.</span></span>

<span data-ttu-id="7c05d-110">Les dimensions de l’image de mappage doivent être identiques à celles de l' **image** principale.</span><span class="sxs-lookup"><span data-stu-id="7c05d-110">The mapping image should be the same dimensions as the main **image**.</span></span> <span data-ttu-id="7c05d-111">Il s’agit d’une carte des zones cliquables de l’image principale.</span><span class="sxs-lookup"><span data-stu-id="7c05d-111">It is a map of the clickable areas of the main image.</span></span> <span data-ttu-id="7c05d-112">Construisez la carte en remplissant chaque zone interactive avec une couleur différente.</span><span class="sxs-lookup"><span data-stu-id="7c05d-112">Construct the map by filling each clickable area with a different color.</span></span>

<span data-ttu-id="7c05d-113">Quand vous définissez chaque **BUTTONELEMENT**, vous spécifiez sa couleur à partir de la carte à l’aide de l’attribut **mappingColor** .</span><span class="sxs-lookup"><span data-stu-id="7c05d-113">When defining each **BUTTONELEMENT**, designate its color from the map using the **mappingColor** attribute.</span></span> <span data-ttu-id="7c05d-114">Par exemple, si vous avez un graphique de bouton en forme d’arrêt dans l’image principale, vous pouvez créer une carte avec la zone du signe de couleur rouge.</span><span class="sxs-lookup"><span data-stu-id="7c05d-114">For example, if you have a stop-sign-shaped button graphic in the main image, you can create a map with the area of the sign colored red.</span></span> <span data-ttu-id="7c05d-115">L’attribut **BUTTONELEMENT** doit ensuite être spécifié en rouge pour que l’image d’arrêt soit cliquable.</span><span class="sxs-lookup"><span data-stu-id="7c05d-115">The **BUTTONELEMENT** attribute must then be specified as red to make the stop-sign image clickable.</span></span>

<span data-ttu-id="7c05d-116">Les formats d’image pris en charge sont BMP, JPG, PNG et GIF (à l’exclusion des GIF animés).</span><span class="sxs-lookup"><span data-stu-id="7c05d-116">The supported image formats are BMP, JPG, PNG, and GIF (not including animated GIFs).</span></span> <span data-ttu-id="7c05d-117">Étant donné que les JPGs sont perdus et, par conséquent, soumis à une modification de couleur inattendue, ils ne sont pas recommandés pour le mappage d’images.</span><span class="sxs-lookup"><span data-stu-id="7c05d-117">Because JPGs are lossy and therefore subject to unexpected color change, they are not recommended for mapping images.</span></span>

## <a name="examples"></a><span data-ttu-id="7c05d-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="7c05d-118">Examples</span></span>

<span data-ttu-id="7c05d-119">L’illustration suivante est un exemple de **mappingImage** et de l’image visible à laquelle elle correspond.</span><span class="sxs-lookup"><span data-stu-id="7c05d-119">The following illustration is an example of a **mappingImage** and the visible image it corresponds to.</span></span> <span data-ttu-id="7c05d-120">Ces images font partie de l’apparence dans le petit dossier inclus dans le kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="7c05d-120">These images are part of the skin in the Tiny folder included with the SDK.</span></span>

![exemple d’image de mappage](images/absam01m.png)![exemple d’image d’arrière-plan](images/absam01f.png)

<span data-ttu-id="7c05d-123">Consultez *BUTTONELEMENT*. attribut [mappingColor](buttonelement-mappingcolor.md) pour un exemple de code illustrant l’utilisation de cet attribut.</span><span class="sxs-lookup"><span data-stu-id="7c05d-123">See the *BUTTONELEMENT*.[mappingColor](buttonelement-mappingcolor.md) attribute for a code sample illustrating the use of this attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c05d-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7c05d-124">Requirements</span></span>



| <span data-ttu-id="7c05d-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7c05d-125">Requirement</span></span> | <span data-ttu-id="7c05d-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c05d-126">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="7c05d-127">Version</span><span class="sxs-lookup"><span data-stu-id="7c05d-127">Version</span></span><br/> | <span data-ttu-id="7c05d-128">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="7c05d-128">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7c05d-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c05d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c05d-130">**BUTTONELEMENT. mappingColor**</span><span class="sxs-lookup"><span data-stu-id="7c05d-130">**BUTTONELEMENT.mappingColor**</span></span>](buttonelement-mappingcolor.md)
</dt> <dt>

[<span data-ttu-id="7c05d-131">**Élément BUTTONGROUP**</span><span class="sxs-lookup"><span data-stu-id="7c05d-131">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="7c05d-132">**BUTTONGROUP. image**</span><span class="sxs-lookup"><span data-stu-id="7c05d-132">**BUTTONGROUP.image**</span></span>](buttongroup-image.md)
</dt> <dt>

[<span data-ttu-id="7c05d-133">**BUTTONGROUP. transparencyColor**</span><span class="sxs-lookup"><span data-stu-id="7c05d-133">**BUTTONGROUP.transparencyColor**</span></span>](buttongroup-transparencycolor.md)
</dt> </dl>

 

 





