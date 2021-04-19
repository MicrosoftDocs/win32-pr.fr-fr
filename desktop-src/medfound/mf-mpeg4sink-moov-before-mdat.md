---
description: Indique que Moov sera écrit avant la boîte de MDAT dans le fichier généré.
ms.assetid: 97B68B0A-8266-4FCF-8CD9-35890E1AC774
title: Attribut MF_MPEG4SINK_MOOV_BEFORE_MDAT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b5d345dc027c457ceb6123ce3854fff4b74f987
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524272"
---
# <a name="mf_mpeg4sink_moov_before_mdat-attribute"></a><span data-ttu-id="4095a-103">MF \_ MPEG4SINK \_ Moov \_ avant \_ attribut MDAT</span><span class="sxs-lookup"><span data-stu-id="4095a-103">MF\_MPEG4SINK\_MOOV\_BEFORE\_MDAT attribute</span></span>

<span data-ttu-id="4095a-104">Indique que « Moov » sera écrit avant la zone « MDAT » dans le fichier généré.</span><span class="sxs-lookup"><span data-stu-id="4095a-104">Indicates that 'moov' will be written before 'mdat' box in the generated file.</span></span>

## <a name="data-type"></a><span data-ttu-id="4095a-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="4095a-105">Data type</span></span>

<span data-ttu-id="4095a-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="4095a-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="4095a-107">Notes</span><span class="sxs-lookup"><span data-stu-id="4095a-107">Remarks</span></span>

<span data-ttu-id="4095a-108">Le comportement par défaut du récepteur multimédia MPEG4 consiste à écrire « Moov » après la zone « MDAT ».</span><span class="sxs-lookup"><span data-stu-id="4095a-108">The default behavior of the mpeg4 media sink is to write 'moov' after 'mdat' box.</span></span> <span data-ttu-id="4095a-109">La définition de cet attribut fait que le fichier généré écrit « Moov » avant la zone « MDAT ».</span><span class="sxs-lookup"><span data-stu-id="4095a-109">Setting this attribute causes the generated file to write 'moov' before 'mdat' box.</span></span>

<span data-ttu-id="4095a-110">Pour que le récepteur MPEG4 utilise cet attribut, le flux d’octets transmis ne doit pas être lent ou distant pour.</span><span class="sxs-lookup"><span data-stu-id="4095a-110">In order for the mpeg4 sink to use this attribute, the byte stream passed in must not be slow seek or remote for .</span></span>

<span data-ttu-id="4095a-111">Cette fonctionnalité implique une copie de fichier supplémentaire/remuxing.</span><span class="sxs-lookup"><span data-stu-id="4095a-111">This feature involves an additional file copying/remuxing.</span></span>

## <a name="requirements"></a><span data-ttu-id="4095a-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4095a-112">Requirements</span></span>



| <span data-ttu-id="4095a-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4095a-113">Requirement</span></span> | <span data-ttu-id="4095a-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="4095a-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4095a-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4095a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="4095a-116">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="4095a-116">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="4095a-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4095a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="4095a-118">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="4095a-118">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="4095a-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="4095a-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="4095a-120"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4095a-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4095a-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4095a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4095a-122">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4095a-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4095a-123">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="4095a-123">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




