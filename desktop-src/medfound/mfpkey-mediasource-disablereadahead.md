---
description: Active ou désactive la lecture anticipée dans une source de média.
ms.assetid: b2b8711f-ba63-4fba-bb88-8d254135eb21
title: MFPKEY_MediaSource_DisableReadAhead, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d06fe354431a24e15152268ba0ea6352e535c5e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532637"
---
# <a name="mfpkey_mediasource_disablereadahead-property"></a><span data-ttu-id="97f7b-103">MFPKEY \_ MediaSource \_ DisableReadAhead, propriété</span><span class="sxs-lookup"><span data-stu-id="97f7b-103">MFPKEY\_MediaSource\_DisableReadAhead property</span></span>

<span data-ttu-id="97f7b-104">Active ou désactive la lecture anticipée dans une source de média.</span><span class="sxs-lookup"><span data-stu-id="97f7b-104">Enables or disables read-ahead in a media source.</span></span>



<span data-ttu-id="97f7b-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="97f7b-105">Data type</span></span>

<span data-ttu-id="97f7b-106">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="97f7b-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="97f7b-107">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="97f7b-107">PROPVARIANT member</span></span>

<span data-ttu-id="97f7b-108">**VARIANT \_ booléen**</span><span class="sxs-lookup"><span data-stu-id="97f7b-108">**VARIANT\_BOOL**</span></span>

<span data-ttu-id="97f7b-109">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="97f7b-109">VT\_BOOL</span></span>

<span data-ttu-id="97f7b-110">**boolVal**</span><span class="sxs-lookup"><span data-stu-id="97f7b-110">**boolVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="97f7b-111">Notes</span><span class="sxs-lookup"><span data-stu-id="97f7b-111">Remarks</span></span>

<span data-ttu-id="97f7b-112">Les applications peuvent utiliser cette propriété pour configurer des sources multimédias.</span><span class="sxs-lookup"><span data-stu-id="97f7b-112">Applications can use this property to configure some media sources.</span></span> <span data-ttu-id="97f7b-113">Pour définir la propriété, transmettez un pointeur **IPropertyStore** au programme de résolution source.</span><span class="sxs-lookup"><span data-stu-id="97f7b-113">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="97f7b-114">Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="97f7b-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="97f7b-115">Si la valeur est **\_ true**, la source du média n’est pas lue dans le flux de données d’octets.</span><span class="sxs-lookup"><span data-stu-id="97f7b-115">If the value is **VARIANT\_TRUE**, the media source will not read ahead in the byte stream.</span></span> <span data-ttu-id="97f7b-116">Ce paramètre peut optimiser les performances si vous envisagez de lire une quantité limitée de données à partir de la source du média, par exemple pour obtenir une image miniature d’un fichier vidéo.</span><span class="sxs-lookup"><span data-stu-id="97f7b-116">This setting can optimize performance if you plan to read a limited amount of data from the media source—for example, to get a thumbnail image from a video file.</span></span>

<span data-ttu-id="97f7b-117">Pour une lecture audio/vidéo classique, cette propriété doit avoir la valeur **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="97f7b-117">For typical audio/video playback, this property should be set to **VARIANT\_FALSE**.</span></span> <span data-ttu-id="97f7b-118">La valeur par défaut **est \_ false**.</span><span class="sxs-lookup"><span data-stu-id="97f7b-118">The default value is **VARIANT\_FALSE**.</span></span>

<span data-ttu-id="97f7b-119">Toutes les sources de média ne prennent pas en charge cette propriété.</span><span class="sxs-lookup"><span data-stu-id="97f7b-119">Not every media source supports this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="97f7b-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="97f7b-120">Requirements</span></span>



| <span data-ttu-id="97f7b-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="97f7b-121">Requirement</span></span> | <span data-ttu-id="97f7b-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="97f7b-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="97f7b-123">Client</span><span class="sxs-lookup"><span data-stu-id="97f7b-123">Client</span></span><br/> | <span data-ttu-id="97f7b-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="97f7b-124">Windows 7</span></span><br/>                                                               |
| <span data-ttu-id="97f7b-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="97f7b-125">Header</span></span><br/> | <dl> <span data-ttu-id="97f7b-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="97f7b-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97f7b-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97f7b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97f7b-128">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="97f7b-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




