---
description: Les constantes d’intention d’image spécifient le type de données que l’image doit représenter.
ms.assetid: 171228d9-a619-49aa-964e-f72a7f294a9d
title: Constantes d’intention d’image (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_INTENT_IMAGE_TYPE_COLOR
- WIA_INTENT_IMAGE_TYPE_GRAYSCALE
- WIA_INTENT_IMAGE_TYPE_TEXT
- WIA_INTENT_MINIMIZE_SIZE
- WIA_INTENT_MAXIMIZE_QUALITY
- WIA_INTENT_BEST_PREVIEW
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: f35c1f7436c8cc5110215a6ccf0383960ec3fb87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951339"
---
# <a name="image-intent-constants"></a><span data-ttu-id="02e35-103">Constantes d’intention d’image</span><span class="sxs-lookup"><span data-stu-id="02e35-103">Image Intent Constants</span></span>

<span data-ttu-id="02e35-104">Les constantes d’intention d’image spécifient le type de données que l’image doit représenter.</span><span class="sxs-lookup"><span data-stu-id="02e35-104">Image intent constants specify what type of data the image is meant to represent.</span></span> <span data-ttu-id="02e35-105">La propriété de scanneur de l' [**\_ \_ \_ intention d’IPS d’WIA**](-wia-wiaitempropscanneritem.md) utilise ces indicateurs.</span><span class="sxs-lookup"><span data-stu-id="02e35-105">The [**WIA\_IPS\_CUR\_INTENT**](-wia-wiaitempropscanneritem.md) scanner property uses these flags.</span></span> <span data-ttu-id="02e35-106">Pour fournir une intention, associez un indicateur de type d’image prévu à un indicateur de taille/qualité prévu à l’aide de l’opérateur OR.</span><span class="sxs-lookup"><span data-stu-id="02e35-106">To provide an intent, combine an intended image type flag with an intended size/quality flag by using the OR operator.</span></span> <span data-ttu-id="02e35-107">\_L’intention WIA \_ None ne doit pas être combinée avec d’autres indicateurs.</span><span class="sxs-lookup"><span data-stu-id="02e35-107">WIA\_INTENT\_NONE should not be combined with any other flags.</span></span> <span data-ttu-id="02e35-108">Notez qu’une image ne peut pas être à la fois des nuances de gris et des couleurs.</span><span class="sxs-lookup"><span data-stu-id="02e35-108">Note that an image cannot be both grayscale and color.</span></span>

<span data-ttu-id="02e35-109">Les éléments suivants sont des constantes d’intention d’image valides :</span><span class="sxs-lookup"><span data-stu-id="02e35-109">The following are valid image intent constants:</span></span>



| <span data-ttu-id="02e35-110">Indicateurs de type d’image prévu</span><span class="sxs-lookup"><span data-stu-id="02e35-110">Intended image type flags</span></span>           | <span data-ttu-id="02e35-111">Description</span><span class="sxs-lookup"><span data-stu-id="02e35-111">Description</span></span>                                  |
|-------------------------------------|----------------------------------------------|
| <span data-ttu-id="02e35-112">\_intention WIA \_ aucune</span><span class="sxs-lookup"><span data-stu-id="02e35-112">WIA\_INTENT\_NONE</span></span>                   | <span data-ttu-id="02e35-113">Valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="02e35-113">Default value.</span></span> <span data-ttu-id="02e35-114">Ne pas définir de propriétés.</span><span class="sxs-lookup"><span data-stu-id="02e35-114">Do not preset any properties.</span></span> |
| <span data-ttu-id="02e35-115">\_couleur du \_ type d’image d’intention WIA \_ \_</span><span class="sxs-lookup"><span data-stu-id="02e35-115">WIA\_INTENT\_IMAGE\_TYPE\_COLOR</span></span>     | <span data-ttu-id="02e35-116">Propriétés prédéfinies pour le contenu des couleurs.</span><span class="sxs-lookup"><span data-stu-id="02e35-116">Preset properties for color content.</span></span>         |
| <span data-ttu-id="02e35-117">\_type d’image d’intention WIA nuances de \_ \_ \_ gris</span><span class="sxs-lookup"><span data-stu-id="02e35-117">WIA\_INTENT\_IMAGE\_TYPE\_GRAYSCALE</span></span> | <span data-ttu-id="02e35-118">Propriétés prédéfinies pour le contenu en nuances de gris.</span><span class="sxs-lookup"><span data-stu-id="02e35-118">Preset properties for grayscale content.</span></span>     |
| <span data-ttu-id="02e35-119">\_texte du \_ type d’image d’intention WIA \_ \_</span><span class="sxs-lookup"><span data-stu-id="02e35-119">WIA\_INTENT\_IMAGE\_TYPE\_TEXT</span></span>      | <span data-ttu-id="02e35-120">Propriétés prédéfinies pour le contenu de texte.</span><span class="sxs-lookup"><span data-stu-id="02e35-120">Preset properties for text content.</span></span>          |
| <span data-ttu-id="02e35-121">\_masque de \_ type d’image d’intention WIA \_ \_</span><span class="sxs-lookup"><span data-stu-id="02e35-121">WIA\_INTENT\_IMAGE\_TYPE\_MASK</span></span>      | <span data-ttu-id="02e35-122">Masque pour tous les indicateurs de type d’image.</span><span class="sxs-lookup"><span data-stu-id="02e35-122">Mask for all of the image type flags.</span></span>        |



 



| <span data-ttu-id="02e35-123">Indicateurs de qualité/taille d’image prévus</span><span class="sxs-lookup"><span data-stu-id="02e35-123">Intended image size/quality flags</span></span> | <span data-ttu-id="02e35-124">Description</span><span class="sxs-lookup"><span data-stu-id="02e35-124">Description</span></span>                                  |
|-----------------------------------|----------------------------------------------|
| <span data-ttu-id="02e35-125">\_ \_ taille limite de l’intention WIA \_</span><span class="sxs-lookup"><span data-stu-id="02e35-125">WIA\_INTENT\_MINIMIZE\_SIZE</span></span>       | <span data-ttu-id="02e35-126">Propriétés prédéfinies pour réduire la taille de l’image.</span><span class="sxs-lookup"><span data-stu-id="02e35-126">Preset properties to minimize image size.</span></span>    |
| <span data-ttu-id="02e35-127">optimiser la qualité de l' \_ intention WIA \_ \_</span><span class="sxs-lookup"><span data-stu-id="02e35-127">WIA\_INTENT\_MAXIMIZE\_QUALITY</span></span>    | <span data-ttu-id="02e35-128">Propriétés prédéfinies pour optimiser la qualité de l’image.</span><span class="sxs-lookup"><span data-stu-id="02e35-128">Preset properties to maximize image quality.</span></span> |
| <span data-ttu-id="02e35-129">\_masque de \_ taille d’intention WIA \_</span><span class="sxs-lookup"><span data-stu-id="02e35-129">WIA\_INTENT\_SIZE\_MASK</span></span>           | <span data-ttu-id="02e35-130">Masque pour tous les indicateurs de taille/qualité.</span><span class="sxs-lookup"><span data-stu-id="02e35-130">Mask for all of the size/quality flags.</span></span>      |
| <span data-ttu-id="02e35-131">meilleure version préliminaire de l' \_ intention WIA \_ \_</span><span class="sxs-lookup"><span data-stu-id="02e35-131">WIA\_INTENT\_BEST\_PREVIEW</span></span>        | <span data-ttu-id="02e35-132">Spécifie la meilleure qualité d’aperçu.</span><span class="sxs-lookup"><span data-stu-id="02e35-132">Specifies the best quality preview.</span></span>          |



 

<span data-ttu-id="02e35-133">La liste suivante affiche le nom de constante C/C++ suivi du nom correspondant entre parenthèses utilisé dans les scripts.</span><span class="sxs-lookup"><span data-stu-id="02e35-133">The following list shows the C/C++ constant name followed by the corresponding name in parentheses that is used in scripting.</span></span> <span data-ttu-id="02e35-134">Les noms de script proviennent du type énuméré WiaIntent.</span><span class="sxs-lookup"><span data-stu-id="02e35-134">The script names are from the WiaIntent enumerated type.</span></span> <span data-ttu-id="02e35-135">Notez que toutes les constantes ne sont pas disponibles par le biais d’un script.</span><span class="sxs-lookup"><span data-stu-id="02e35-135">Note that not all constants are available through script.</span></span>



| <span data-ttu-id="02e35-136">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="02e35-136">Constant/value</span></span>                                                                                                                                                                                                                                                                         | <span data-ttu-id="02e35-137">Description</span><span class="sxs-lookup"><span data-stu-id="02e35-137">Description</span></span>                                             |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------|
| <span id="WIA_INTENT_IMAGE_TYPE_COLOR"></span><span id="wia_intent_image_type_color"></span><dl> <span data-ttu-id="02e35-138"><dt>**WIA \_ TYPE d’image d’intention \_ \_ \_ couleur**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="02e35-138"><dt>**WIA\_INTENT\_IMAGE\_TYPE\_COLOR**</dt> <dt>0x00000001</dt></span></span> </dl>             | <span data-ttu-id="02e35-139">Propriétés prédéfinies pour le contenu des couleurs.</span><span class="sxs-lookup"><span data-stu-id="02e35-139">Preset properties for color content.</span></span><br/>         |
| <span id="WIA_INTENT_IMAGE_TYPE_GRAYSCALE"></span><span id="wia_intent_image_type_grayscale"></span><dl> <span data-ttu-id="02e35-140"><dt>**WIA \_ TYPE d’image d’intention \_ \_ nuances de \_ gris**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="02e35-140"><dt>**WIA\_INTENT\_IMAGE\_TYPE\_GRAYSCALE**</dt> <dt>0x00000002</dt></span></span> </dl> | <span data-ttu-id="02e35-141">Propriétés prédéfinies pour le contenu en nuances de gris.</span><span class="sxs-lookup"><span data-stu-id="02e35-141">Preset properties for grayscale content.</span></span><br/>     |
| <span id="WIA_INTENT_IMAGE_TYPE_TEXT"></span><span id="wia_intent_image_type_text"></span><dl> <span data-ttu-id="02e35-142"><dt>**WIA \_ TYPE d’image d’intention \_ \_ \_ texte**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="02e35-142"><dt>**WIA\_INTENT\_IMAGE\_TYPE\_TEXT**</dt> <dt>0x00000004</dt></span></span> </dl>                | <span data-ttu-id="02e35-143">Propriétés prédéfinies pour le contenu de texte.</span><span class="sxs-lookup"><span data-stu-id="02e35-143">Preset properties for text content.</span></span><br/>          |
| <span id="WIA_INTENT_MINIMIZE_SIZE"></span><span id="wia_intent_minimize_size"></span><dl> <span data-ttu-id="02e35-144"><dt>**WIA \_ \_Limiter la \_ taille**</dt> des <dt>0x00010000</dt></span><span class="sxs-lookup"><span data-stu-id="02e35-144"><dt>**WIA\_INTENT\_MINIMIZE\_SIZE**</dt> <dt>0x00010000</dt></span></span> </dl>                       | <span data-ttu-id="02e35-145">Propriétés prédéfinies pour réduire la taille de l’image.</span><span class="sxs-lookup"><span data-stu-id="02e35-145">Preset properties to minimize image size.</span></span><br/>    |
| <span id="WIA_INTENT_MAXIMIZE_QUALITY"></span><span id="wia_intent_maximize_quality"></span><dl> <span data-ttu-id="02e35-146"><dt>**WIA \_ \_Optimiser la \_ qualité**</dt> <dt>0x00020000</dt></span><span class="sxs-lookup"><span data-stu-id="02e35-146"><dt>**WIA\_INTENT\_MAXIMIZE\_QUALITY**</dt> <dt>0x00020000</dt></span></span> </dl>              | <span data-ttu-id="02e35-147">Propriétés prédéfinies pour optimiser la qualité de l’image.</span><span class="sxs-lookup"><span data-stu-id="02e35-147">Preset properties to maximize image quality.</span></span><br/> |
| <span id="WIA_INTENT_BEST_PREVIEW"></span><span id="wia_intent_best_preview"></span><dl> <span data-ttu-id="02e35-148"><dt>**WIA \_ INTENTION de la \_ meilleure version \_ préliminaire**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="02e35-148"><dt>**WIA\_INTENT\_BEST\_PREVIEW**</dt> <dt>0x00040000</dt></span></span> </dl>                          | <span data-ttu-id="02e35-149">Spécifie la meilleure qualité d’aperçu.</span><span class="sxs-lookup"><span data-stu-id="02e35-149">Specifies the best quality preview.</span></span><br/>          |



## <a name="requirements"></a><span data-ttu-id="02e35-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="02e35-150">Requirements</span></span>



| <span data-ttu-id="02e35-151">Condition requise</span><span class="sxs-lookup"><span data-stu-id="02e35-151">Requirement</span></span> | <span data-ttu-id="02e35-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="02e35-152">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="02e35-153">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="02e35-153">Minimum supported client</span></span><br/> | <span data-ttu-id="02e35-154">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="02e35-154">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="02e35-155">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="02e35-155">Minimum supported server</span></span><br/> | <span data-ttu-id="02e35-156">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="02e35-156">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="02e35-157">En-tête</span><span class="sxs-lookup"><span data-stu-id="02e35-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="02e35-158"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="02e35-158"><dt>Wiadef.h</dt></span></span> </dl> |



 

 




