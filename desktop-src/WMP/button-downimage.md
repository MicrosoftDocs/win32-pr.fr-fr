---
title: BUTTON. downImage
description: L’attribut downImage spécifie ou récupère l’image représentant l’état inactif du bouton.
ms.assetid: 18149668-5be6-4b64-8adf-8904585ff0be
keywords:
- BUTTON. downImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.downImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca7a405a5df20a04ae9d093f2b28ee4c68cab67d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530379"
---
# <a name="buttondownimage"></a><span data-ttu-id="03b2c-104">BUTTON. downImage</span><span class="sxs-lookup"><span data-stu-id="03b2c-104">BUTTON.downImage</span></span>

<span data-ttu-id="03b2c-105">L’attribut **downImage** spécifie ou récupère l’image représentant l’état inactif du **bouton**.</span><span class="sxs-lookup"><span data-stu-id="03b2c-105">The **downImage** attribute specifies or retrieves the image representing the down state of the **BUTTON**.</span></span>

``` syntax
        elementID.downImage
```

## <a name="possible-values"></a><span data-ttu-id="03b2c-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="03b2c-106">Possible Values</span></span>

<span data-ttu-id="03b2c-107">Cet attribut est une **chaîne** en lecture/écriture contenant le nom du fichier image.</span><span class="sxs-lookup"><span data-stu-id="03b2c-107">This attribute is a read/write **String** containing the image file name.</span></span>

## <a name="remarks"></a><span data-ttu-id="03b2c-108">Notes</span><span class="sxs-lookup"><span data-stu-id="03b2c-108">Remarks</span></span>

<span data-ttu-id="03b2c-109">Les formats d’image pris en charge sont BMP, JPG, PNG et GIF.</span><span class="sxs-lookup"><span data-stu-id="03b2c-109">The supported image formats are BMP, JPG, PNG, and GIF.</span></span>

<span data-ttu-id="03b2c-110">L’image par défaut est celle spécifiée dans l’attribut **image** ou sa valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="03b2c-110">The default image is the one specified in the **image** attribute, or its default.</span></span>

<span data-ttu-id="03b2c-111">Si l’image inférieure est plus grande que la région définie dans l’attribut ambiant, l’image descendante est rognée.</span><span class="sxs-lookup"><span data-stu-id="03b2c-111">If the down image is larger than the defined region in the ambient attribute, the down image will be cropped.</span></span>

<span data-ttu-id="03b2c-112">Si l’image ne peut pas être récupérée, une image par défaut (l’image rouge-x) s’affiche.</span><span class="sxs-lookup"><span data-stu-id="03b2c-112">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="03b2c-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="03b2c-113">Requirements</span></span>



| <span data-ttu-id="03b2c-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="03b2c-114">Requirement</span></span> | <span data-ttu-id="03b2c-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="03b2c-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="03b2c-116">Version</span><span class="sxs-lookup"><span data-stu-id="03b2c-116">Version</span></span><br/> | <span data-ttu-id="03b2c-117">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="03b2c-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="03b2c-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03b2c-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03b2c-119">**BUTTON, élément**</span><span class="sxs-lookup"><span data-stu-id="03b2c-119">**BUTTON Element**</span></span>](button-element.md)
</dt> <dt>

[<span data-ttu-id="03b2c-120">**BUTTON. suiv.**</span><span class="sxs-lookup"><span data-stu-id="03b2c-120">**BUTTON.down**</span></span>](button-down.md)
</dt> <dt>

[<span data-ttu-id="03b2c-121">**BOUTON. image**</span><span class="sxs-lookup"><span data-stu-id="03b2c-121">**BUTTON.image**</span></span>](button-image.md)
</dt> </dl>

 

 





