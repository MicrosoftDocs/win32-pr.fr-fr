---
description: Spécifie le niveau de volume moyen de contenu audio.
ms.assetid: eabb36ff-300f-4ed1-aca3-9415627ac1a7
title: MFPKEY_WMADRC_AVGREF, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf18c37b00f84cc3ae3fdf1f44b2fbefcc56d9f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521455"
---
# <a name="mfpkey_wmadrc_avgref-property"></a><span data-ttu-id="d366d-103">MFPKEY \_ WMADRC \_ AVGREF, propriété</span><span class="sxs-lookup"><span data-stu-id="d366d-103">MFPKEY\_WMADRC\_AVGREF Property</span></span>

<span data-ttu-id="d366d-104">Spécifie le niveau de volume moyen de contenu audio.</span><span class="sxs-lookup"><span data-stu-id="d366d-104">Specifies the average volume level of audio content.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="d366d-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="d366d-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="d366d-106">\_wszWMADRCAverageReference g</span><span class="sxs-lookup"><span data-stu-id="d366d-106">g\_wszWMADRCAverageReference</span></span>

## <a name="data-type"></a><span data-ttu-id="d366d-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="d366d-107">Data Type</span></span>

<span data-ttu-id="d366d-108">VT \_</span><span class="sxs-lookup"><span data-stu-id="d366d-108">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="d366d-109">Notes</span><span class="sxs-lookup"><span data-stu-id="d366d-109">Remarks</span></span>

<span data-ttu-id="d366d-110">Vous pouvez récupérer cette valeur à partir de l’encodeur une fois le contenu traité.</span><span class="sxs-lookup"><span data-stu-id="d366d-110">You can get this value from the encoder after the content is processed.</span></span> <span data-ttu-id="d366d-111">Cette valeur peut également être définie sur le décodeur à des fins de contrôle de plage dynamique, mais n’a d’effet que si la propriété [MFPKEY \_ WMADEC \_ DRCMODE](mfpkey-wmadec-drcmodeproperty.md) est définie.</span><span class="sxs-lookup"><span data-stu-id="d366d-111">This value can also be set on the decoder for the purpose of dynamic range control, but it will have an effect only if the [MFPKEY\_WMADEC\_DRCMODE](mfpkey-wmadec-drcmodeproperty.md) property is set.</span></span>

<span data-ttu-id="d366d-112">Pour plus d’informations sur le contrôle de plage dynamique, consultez l’article Web [Windows Media Audio fonctionnalités du codec professionnel](/previous-versions/ms867218(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="d366d-112">For more information on dynamic range control see the web article [Windows Media Audio Professional Codec Features](/previous-versions/ms867218(v=msdn.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="d366d-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d366d-113">Requirements</span></span>



| <span data-ttu-id="d366d-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d366d-114">Requirement</span></span> | <span data-ttu-id="d366d-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="d366d-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d366d-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d366d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d366d-117">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d366d-117">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d366d-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d366d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d366d-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d366d-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d366d-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="d366d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d366d-121"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d366d-121"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d366d-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d366d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d366d-123">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d366d-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
