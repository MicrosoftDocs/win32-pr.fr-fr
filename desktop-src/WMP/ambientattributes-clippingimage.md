---
title: AmbientAttributes.clippingImage
description: L’attribut clippingImage spécifie ou récupère la zone dans laquelle détourer le contrôle.
ms.assetid: e4b51d31-f9c7-4398-983d-95867a2cab45
keywords:
- Lecteur Windows Media AmbientAttributes. clippingImage
topic_type:
- apiref
api_name:
- AmbientAttributes.clippingImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e05e05ca9c7c3efdf842ffd4297da6f9fee035d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533312"
---
# <a name="ambientattributesclippingimage"></a><span data-ttu-id="91928-104">AmbientAttributes.clippingImage</span><span class="sxs-lookup"><span data-stu-id="91928-104">AmbientAttributes.clippingImage</span></span>

<span data-ttu-id="91928-105">L’attribut **clippingImage** spécifie ou récupère la zone dans laquelle détourer le contrôle.</span><span class="sxs-lookup"><span data-stu-id="91928-105">The **clippingImage** attribute specifies or retrieves the region to clip the control to.</span></span>

``` syntax
        elementID.clippingImage
```

## <a name="possible-values"></a><span data-ttu-id="91928-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="91928-106">Possible Values</span></span>

<span data-ttu-id="91928-107">Cet attribut est une **chaîne** en lecture/écriture indiquant le nom du fichier image.</span><span class="sxs-lookup"><span data-stu-id="91928-107">This attribute is a read/write **String** indicating the image file name.</span></span> <span data-ttu-id="91928-108">Il n'a aucune valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="91928-108">It has no default value.</span></span>

## <a name="remarks"></a><span data-ttu-id="91928-109">Notes</span><span class="sxs-lookup"><span data-stu-id="91928-109">Remarks</span></span>

<span data-ttu-id="91928-110">L’attribut **clippingImage** prend en charge les fichiers PNG, jpg, BMP et GIF (à l’exclusion des fichiers GIF animés).</span><span class="sxs-lookup"><span data-stu-id="91928-110">The **clippingImage** attribute supports PNG, JPG, BMP, and GIF files (not including animated GIFs).</span></span> <span data-ttu-id="91928-111">Étant donné que les JPGs sont perdus et, par conséquent, soumis à une modification de couleur inattendue, ils ne sont pas recommandés pour les images de découpage.</span><span class="sxs-lookup"><span data-stu-id="91928-111">Because JPGs are lossy and therefore subject to unexpected color change, they are not recommended for clipping images.</span></span>

<span data-ttu-id="91928-112">Cet attribut est utile lorsque vous souhaitez afficher uniquement une partie de l’image de contrôle, et non l’intégralité de la zone rectangulaire.</span><span class="sxs-lookup"><span data-stu-id="91928-112">This attribute is useful when you want to display only a part of the control image and not the entire rectangular area.</span></span> <span data-ttu-id="91928-113">L’attribut **clippingColor** indique les régions de l’image de découpage qui correspondent à des portions transparentes et non intercliquables du contrôle.</span><span class="sxs-lookup"><span data-stu-id="91928-113">The **clippingColor** attribute indicates the regions of the clipping image that correspond to transparent, non-clickable portions of the control.</span></span> <span data-ttu-id="91928-114">Le contrôle peut donc être de n’importe quelle forme.</span><span class="sxs-lookup"><span data-stu-id="91928-114">The control can therefore be of any shape.</span></span> <span data-ttu-id="91928-115">Pour de meilleurs résultats, l’image de découpage doit être de la même taille que l’image de contrôle.</span><span class="sxs-lookup"><span data-stu-id="91928-115">For best results, the clipping image should be the same size as the control image.</span></span>

<span data-ttu-id="91928-116">L’attribut **clippingImage** n’est pas pris en charge par les éléments **playlist**, **View** et **subview** .</span><span class="sxs-lookup"><span data-stu-id="91928-116">The **clippingImage** attribute is not supported by the **PLAYLIST**, **VIEW**, and **SUBVIEW** elements.</span></span> <span data-ttu-id="91928-117">Une image de découpage ne fonctionne pas avec l’élément **vidéo** si la *vidéo* est. **sans fenêtre** est défini sur false, ni avec l’élément **Effects** si *Effects*. **Windowed** a la valeur true.</span><span class="sxs-lookup"><span data-stu-id="91928-117">A clipping image will not work with the **VIDEO** element if *VIDEO*.**windowless** is set to false, nor with the **EFFECTS** element if *EFFECTS*.**windowed** is set to true.</span></span>

<span data-ttu-id="91928-118">Étant donné que l’utilisation d’images de découpage impose une baisse des performances, elles ne doivent pas être utilisées lorsque l’efficacité est un problème.</span><span class="sxs-lookup"><span data-stu-id="91928-118">Because the use of clipping images imposes a performance penalty, they should not be used when efficiency is an issue.</span></span>

## <a name="examples"></a><span data-ttu-id="91928-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="91928-119">Examples</span></span>

<span data-ttu-id="91928-120">Consultez l’attribut [BUTTONELEMENT. mappingColor](buttonelement-mappingcolor.md) pour obtenir un exemple illustrant l’utilisation de cet attribut.</span><span class="sxs-lookup"><span data-stu-id="91928-120">See the [BUTTONELEMENT.mappingColor](buttonelement-mappingcolor.md) attribute for a sample illustrating the use of this attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="91928-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="91928-121">Requirements</span></span>



| <span data-ttu-id="91928-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="91928-122">Requirement</span></span> | <span data-ttu-id="91928-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="91928-123">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="91928-124">Version</span><span class="sxs-lookup"><span data-stu-id="91928-124">Version</span></span><br/> | <span data-ttu-id="91928-125">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="91928-125">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="91928-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91928-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91928-127">**Attributs ambiants**</span><span class="sxs-lookup"><span data-stu-id="91928-127">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="91928-128">**AmbientAttributes.clippingColor**</span><span class="sxs-lookup"><span data-stu-id="91928-128">**AmbientAttributes.clippingColor**</span></span>](ambientattributes-clippingcolor.md)
</dt> </dl>

 

 





