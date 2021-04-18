---
title: BUTTON. disabledImage
description: L’attribut disabledImage spécifie ou récupère l’image qui s’affiche lorsque le bouton est désactivé.
ms.assetid: b5654323-589a-45da-9534-6fa67c3a4c4b
keywords:
- BUTTON. disabledImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.disabledImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eac407f6e7fbdd155f4bcabe98cecc0546f7d97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532914"
---
# <a name="buttondisabledimage"></a><span data-ttu-id="e3c77-104">BUTTON. disabledImage</span><span class="sxs-lookup"><span data-stu-id="e3c77-104">BUTTON.disabledImage</span></span>

<span data-ttu-id="e3c77-105">L’attribut **disabledImage** spécifie ou récupère l’image qui s’affiche lorsque le **bouton** est désactivé.</span><span class="sxs-lookup"><span data-stu-id="e3c77-105">The **disabledImage** attribute specifies or retrieves the image that displays when the **BUTTON** is disabled.</span></span>

``` syntax
        elementID.disabledImage
```

## <a name="possible-values"></a><span data-ttu-id="e3c77-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="e3c77-106">Possible Values</span></span>

<span data-ttu-id="e3c77-107">Cet attribut est une **chaîne** en lecture/écriture contenant le nom du fichier image.</span><span class="sxs-lookup"><span data-stu-id="e3c77-107">This attribute is a read/write **String** containing the image file name.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3c77-108">Notes</span><span class="sxs-lookup"><span data-stu-id="e3c77-108">Remarks</span></span>

<span data-ttu-id="e3c77-109">Les formats d’image pris en charge sont BMP, JPG, PNG et GIF.</span><span class="sxs-lookup"><span data-stu-id="e3c77-109">The supported image formats are BMP, JPG, PNG, and GIF.</span></span>

<span data-ttu-id="e3c77-110">Cette image s’affiche lorsque l’attribut **désactivé** du contrôle a la valeur true.</span><span class="sxs-lookup"><span data-stu-id="e3c77-110">This image will be displayed whenever the **disabled** attribute of the control is set to true.</span></span> <span data-ttu-id="e3c77-111">Si la taille de l’image désactivée est supérieure à celle de la région définie, l’image désactivée est rognée.</span><span class="sxs-lookup"><span data-stu-id="e3c77-111">If the disabled image is larger than the defined region, the disabled image will be cropped.</span></span>

<span data-ttu-id="e3c77-112">Si l’image ne peut pas être récupérée, une image par défaut (l’image rouge-x) s’affiche.</span><span class="sxs-lookup"><span data-stu-id="e3c77-112">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3c77-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e3c77-113">Requirements</span></span>



| <span data-ttu-id="e3c77-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e3c77-114">Requirement</span></span> | <span data-ttu-id="e3c77-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="e3c77-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="e3c77-116">Version</span><span class="sxs-lookup"><span data-stu-id="e3c77-116">Version</span></span><br/> | <span data-ttu-id="e3c77-117">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="e3c77-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e3c77-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3c77-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3c77-119">**BUTTON, élément**</span><span class="sxs-lookup"><span data-stu-id="e3c77-119">**BUTTON Element**</span></span>](button-element.md)
</dt> </dl>

 

 





