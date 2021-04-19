---
description: Spécifie si la table MFT REMUX vidéo H. 264 doit marquer I images comme point de nettoyage pour améliorer la capacité de recherche. Cela risque d’endommager les recherches dans des fichiers MP4 finaux non conformes.
ms.assetid: BB521E13-40A4-4643-B071-76B8CBC62074
title: Attribut MFT_REMUX_MARK_I_PICTURE_AS_CLEAN_POINT (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26c9fe8398507f6d7af5d0e4bf45a36a4454f220
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531867"
---
# <a name="mft_remux_mark_i_picture_as_clean_point-attribute"></a><span data-ttu-id="20924-104">\_ \_ Image de la marque REMUX MFT \_ \_ \_ comme \_ point de nettoyage \_</span><span class="sxs-lookup"><span data-stu-id="20924-104">MFT\_REMUX\_MARK\_I\_PICTURE\_AS\_CLEAN\_POINT attribute</span></span>

<span data-ttu-id="20924-105">Spécifie si la table MFT REMUX vidéo H. 264 doit marquer I images comme point de nettoyage pour améliorer la capacité de recherche.</span><span class="sxs-lookup"><span data-stu-id="20924-105">Specifies whether the H.264 video remux MFT should mark I pictures as clean point for better seek-ability.</span></span> <span data-ttu-id="20924-106">Cela risque d’endommager les recherches dans des fichiers MP4 finaux non conformes.</span><span class="sxs-lookup"><span data-stu-id="20924-106">This has the potential for corruptions on seeks in non-conforming final MP4 files.</span></span>

## <a name="data-type"></a><span data-ttu-id="20924-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="20924-107">Data type</span></span>

<span data-ttu-id="20924-108">**Bool** stocké comme **UInt32**</span><span class="sxs-lookup"><span data-stu-id="20924-108">**Bool** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="20924-109">Notes</span><span class="sxs-lookup"><span data-stu-id="20924-109">Remarks</span></span>

<span data-ttu-id="20924-110">L’image de point de nettoyage doit être compressée pour les images par définition.</span><span class="sxs-lookup"><span data-stu-id="20924-110">Clean point picture should be compressed IDR pictures by definition.</span></span>

<span data-ttu-id="20924-111">Cela n’est pas recommandé pour l’enregistrement ou la remuxing des fichiers MP4, sauf si un tel exercice consiste à produire des fichiers Pseudo-MP4 intermédiaires pour la modification vidéo.</span><span class="sxs-lookup"><span data-stu-id="20924-111">This is not recommended for recording or remuxing MP4 files, unless such an exercise is to produce some intermediate pseudo MP4 files for video editing.</span></span>

## <a name="requirements"></a><span data-ttu-id="20924-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="20924-112">Requirements</span></span>



| <span data-ttu-id="20924-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="20924-113">Requirement</span></span> | <span data-ttu-id="20924-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="20924-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="20924-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="20924-115">Minimum supported client</span></span><br/> | <span data-ttu-id="20924-116">\[Applications Windows 8.1 Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="20924-116">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="20924-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="20924-117">Minimum supported server</span></span><br/> | <span data-ttu-id="20924-118">Applications Windows Server 2012 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="20924-118">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                             |
| <span data-ttu-id="20924-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="20924-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="20924-120"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="20924-120"><dt>Mftransform.h</dt></span></span> </dl>   |
| <span data-ttu-id="20924-121">MIDL</span><span class="sxs-lookup"><span data-stu-id="20924-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="20924-122"><dt>Mftransform. idl</dt></span><span class="sxs-lookup"><span data-stu-id="20924-122"><dt>Mftransform.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20924-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20924-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20924-124">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="20924-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




