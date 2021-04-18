---
description: Ces indicateurs spécifient le mode de rendu d’une source vidéo si sa taille ne correspond pas aux dimensions de sortie.
ms.assetid: f740b732-ba05-4fda-aafb-ed04bc3efd33
title: Indicateurs de redimensionnement (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RESIZEF_STRETCH
- RESIZEF_CROP
- RESIZEF_PRESERVEASPECTRATIO
- RESIZEF_PRESERVEASPECTRATIO_NOLETTERBOX
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 9e2ef2766f7f54fea4fad16fc26242a8c2ee08db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533395"
---
# <a name="resize-flags"></a><span data-ttu-id="b0d74-103">Indicateurs de redimensionnement</span><span class="sxs-lookup"><span data-stu-id="b0d74-103">Resize Flags</span></span>

<span data-ttu-id="b0d74-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="b0d74-104">\[Deprecated.</span></span> <span data-ttu-id="b0d74-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b0d74-105">This API may be removed from future releases of Windows.\]</span></span>

<span data-ttu-id="b0d74-106">Ces indicateurs spécifient le mode de rendu d’une source vidéo si sa taille ne correspond pas aux dimensions de sortie.</span><span class="sxs-lookup"><span data-stu-id="b0d74-106">These flags specify how a video source is rendered if its size does not match the output dimensions.</span></span>



| <span data-ttu-id="b0d74-107">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="b0d74-107">Constant/value</span></span>                                                                                                                                                                                                                                                                                      | <span data-ttu-id="b0d74-108">Description</span><span class="sxs-lookup"><span data-stu-id="b0d74-108">Description</span></span>                                                                                                                                                                                                                        |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RESIZEF_STRETCH"></span><span id="resizef_stretch"></span><dl> <span data-ttu-id="b0d74-109"><dt>**RESIZEF \_ STRETCH**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b0d74-109"><dt>**RESIZEF\_STRETCH**</dt> <dt>0</dt></span></span> </dl>                                                                          | <span data-ttu-id="b0d74-110">L’image est étirée pour s’ajuster à la taille du cadre cible dans les deux dimensions, sans conserver les proportions.</span><span class="sxs-lookup"><span data-stu-id="b0d74-110">The image is stretched to fit the target frame size in both dimensions, without preserving the aspect ratio.</span></span><br/>                                                                                                            |
| <span id="RESIZEF_CROP"></span><span id="resizef_crop"></span><dl> <span data-ttu-id="b0d74-111"><dt>**RESIZEF \_ ROGNAGE**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b0d74-111"><dt>**RESIZEF\_CROP**</dt> <dt>1</dt></span></span> </dl>                                                                                   | <span data-ttu-id="b0d74-112">L’image n’est pas redimensionnée.</span><span class="sxs-lookup"><span data-stu-id="b0d74-112">The image is not resized.</span></span> <span data-ttu-id="b0d74-113">Si l’image est plus petite que le frame cible, la zone environnante est noire.</span><span class="sxs-lookup"><span data-stu-id="b0d74-113">If the image is smaller than the target frame, the surrounding area is black.</span></span> <span data-ttu-id="b0d74-114">Si l’image est plus grande que le frame cible, l’image est rognée.</span><span class="sxs-lookup"><span data-stu-id="b0d74-114">If the image is larger than the target frame, the image is cropped.</span></span><br/>                                             |
| <span id="RESIZEF_PRESERVEASPECTRATIO"></span><span id="resizef_preserveaspectratio"></span><dl> <span data-ttu-id="b0d74-115"><dt>**RESIZEF \_ PRESERVEASPECTRATIO**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b0d74-115"><dt>**RESIZEF\_PRESERVEASPECTRATIO**</dt> <dt>2</dt></span></span> </dl>                                      | <span data-ttu-id="b0d74-116">L’image est redimensionnée pour s’ajuster au frame cible sur une dimension, tout en conservant les proportions.</span><span class="sxs-lookup"><span data-stu-id="b0d74-116">The image is resized to fit the target frame along one dimension, while preserving the aspect ratio.</span></span> <span data-ttu-id="b0d74-117">Si le rapport entre la largeur et la hauteur dans l’image ne correspond pas au ratio dans le frame cible, elle crée une zone de bandes.</span><span class="sxs-lookup"><span data-stu-id="b0d74-117">If the ratio of width to height in the image does not match the ratio in the target frame, it creates a letterbox.</span></span><br/> |
| <span id="RESIZEF_PRESERVEASPECTRATIO_NOLETTERBOX"></span><span id="resizef_preserveaspectratio_noletterbox"></span><dl> <span data-ttu-id="b0d74-118"><dt>**RESIZEF \_ PRESERVEASPECTRATIO \_ NOLETTERBOX**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="b0d74-118"><dt>**RESIZEF\_PRESERVEASPECTRATIO\_NOLETTERBOX**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="b0d74-119">L’image est redimensionnée pour remplir l’intégralité du frame cible tout en préservant les proportions.</span><span class="sxs-lookup"><span data-stu-id="b0d74-119">The image is resized to fill the entire target frame while preserving the aspect ratio.</span></span> <span data-ttu-id="b0d74-120">Au lieu de créer une bandes, ce mode rogne l’image, sur les côtés ou en haut et en bas.</span><span class="sxs-lookup"><span data-stu-id="b0d74-120">Rather than create a letterbox, this mode crops the image, either along the sides or across the top and bottom.</span></span><br/>                 |



## <a name="remarks"></a><span data-ttu-id="b0d74-121">Notes</span><span class="sxs-lookup"><span data-stu-id="b0d74-121">Remarks</span></span>

<span data-ttu-id="b0d74-122">Les images suivantes montrent les effets de ces indicateurs.</span><span class="sxs-lookup"><span data-stu-id="b0d74-122">The following images show the effects of these flags.</span></span>

![indicateurs de redimensionnement](images/stretch14.png)

## <a name="requirements"></a><span data-ttu-id="b0d74-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b0d74-124">Requirements</span></span>



| <span data-ttu-id="b0d74-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b0d74-125">Requirement</span></span> | <span data-ttu-id="b0d74-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="b0d74-126">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b0d74-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="b0d74-127">Header</span></span><br/> | <dl> <span data-ttu-id="b0d74-128"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0d74-128"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0d74-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b0d74-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0d74-130">**IAMTimelineSrc::GetStretchMode**</span><span class="sxs-lookup"><span data-stu-id="b0d74-130">**IAMTimelineSrc::GetStretchMode**</span></span>](iamtimelinesrc-getstretchmode.md)
</dt> <dt>

[<span data-ttu-id="b0d74-131">**IAMTimelineSrc::SetStretchMode**</span><span class="sxs-lookup"><span data-stu-id="b0d74-131">**IAMTimelineSrc::SetStretchMode**</span></span>](iamtimelinesrc-setstretchmode.md)
</dt> </dl>

 

 




