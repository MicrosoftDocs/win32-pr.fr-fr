---
title: BOUTON. image
description: L’attribut image spécifie ou récupère l’image par défaut du bouton.
ms.assetid: d0d97f14-2c4d-4769-b45c-c6cde7282bea
keywords:
- BUTTON. image lecteur Windows Media
topic_type:
- apiref
api_name:
- BUTTON.image
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d27363383d72110ebe7b3e94187013ab701a6a3c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533191"
---
# <a name="buttonimage"></a><span data-ttu-id="852dc-104">BOUTON. image</span><span class="sxs-lookup"><span data-stu-id="852dc-104">BUTTON.image</span></span>

<span data-ttu-id="852dc-105">L’attribut **image** spécifie ou récupère l’image par défaut du **bouton**.</span><span class="sxs-lookup"><span data-stu-id="852dc-105">The **image** attribute specifies or retrieves the default image of the **BUTTON**.</span></span>

``` syntax
        elementID.image
```

## <a name="possible-values"></a><span data-ttu-id="852dc-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="852dc-106">Possible Values</span></span>

<span data-ttu-id="852dc-107">Cet attribut est une **chaîne** en lecture/écriture contenant le nom du fichier image.</span><span class="sxs-lookup"><span data-stu-id="852dc-107">This attribute is a read/write **String** containing the image file name.</span></span>

## <a name="remarks"></a><span data-ttu-id="852dc-108">Notes</span><span class="sxs-lookup"><span data-stu-id="852dc-108">Remarks</span></span>

<span data-ttu-id="852dc-109">Les formats d’image pris en charge sont BMP, JPG, PNG et GIF (y compris les images GIF animées).</span><span class="sxs-lookup"><span data-stu-id="852dc-109">The supported image formats are BMP, JPG, PNG, and GIF (including animated GIFs).</span></span>

<span data-ttu-id="852dc-110">Si l’image du **bouton** est plus grande que la région définie par les attributs **Width** et **Height** , l’image est rognée.</span><span class="sxs-lookup"><span data-stu-id="852dc-110">If the **BUTTON** image is larger than the region defined by the **width** and **height** attributes, the image will be cropped.</span></span>

<span data-ttu-id="852dc-111">Si l’image n’est pas spécifiée, mais que la **hauteur** et la **largeur** sont, l’image située directement derrière ce contrôle s’affiche.</span><span class="sxs-lookup"><span data-stu-id="852dc-111">If the image is not specified but the **height** and **width** are, then the image directly behind this control is displayed.</span></span> <span data-ttu-id="852dc-112">Cela peut faciliter le dessin de l’image sur la **vue** elle-même, ce qui réduit le nombre de fichiers image distincts nécessaires.</span><span class="sxs-lookup"><span data-stu-id="852dc-112">This can facilitate drawing the image on the **VIEW** itself, reducing the number of separate image files needed.</span></span>

<span data-ttu-id="852dc-113">Si l’image ne peut pas être récupérée, une image par défaut (l’image rouge-x) s’affiche.</span><span class="sxs-lookup"><span data-stu-id="852dc-113">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="852dc-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="852dc-114">Requirements</span></span>



| <span data-ttu-id="852dc-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="852dc-115">Requirement</span></span> | <span data-ttu-id="852dc-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="852dc-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="852dc-117">Version</span><span class="sxs-lookup"><span data-stu-id="852dc-117">Version</span></span><br/> | <span data-ttu-id="852dc-118">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="852dc-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="852dc-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="852dc-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="852dc-120">**BUTTON, élément**</span><span class="sxs-lookup"><span data-stu-id="852dc-120">**BUTTON Element**</span></span>](button-element.md)
</dt> </dl>

 

 





