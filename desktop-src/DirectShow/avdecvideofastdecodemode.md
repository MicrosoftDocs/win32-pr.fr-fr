---
description: Obtient ou définit la vitesse de décodage vidéo.
ms.assetid: 76F7013D-C172-4D31-93BC-EA3D186EB14C
title: Propriété AVDecVideoFastDecodeMode (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 355c085731befedbcb9245a67870d9d609a92c6f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109678"
---
# <a name="avdecvideofastdecodemode-property"></a><span data-ttu-id="9d5de-103">Propriété AVDecVideoFastDecodeMode</span><span class="sxs-lookup"><span data-stu-id="9d5de-103">AVDecVideoFastDecodeMode property</span></span>

<span data-ttu-id="9d5de-104">Obtient ou définit la vitesse de décodage vidéo.</span><span class="sxs-lookup"><span data-stu-id="9d5de-104">Gets or sets the video decoding speed.</span></span>

## <a name="data-type"></a><span data-ttu-id="9d5de-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="9d5de-105">Data type</span></span>

<span data-ttu-id="9d5de-106">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="9d5de-106">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="9d5de-107">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="9d5de-107">Property GUID</span></span>

<span data-ttu-id="9d5de-108">**CODECAPI \_ AVDecVideoFastDecodeMode**</span><span class="sxs-lookup"><span data-stu-id="9d5de-108">**CODECAPI\_AVDecVideoFastDecodeMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="9d5de-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="9d5de-109">Property value</span></span>

<span data-ttu-id="9d5de-110">La valeur de cette propriété peut être comprise entre 0 et 32, où 0 indique un décodage normal et 32 le mode de décodage le plus rapide.</span><span class="sxs-lookup"><span data-stu-id="9d5de-110">The value of this property can range from 0 to 32, where 0 indicates normal decoding and 32 is the fastest decoding mode.</span></span> <span data-ttu-id="9d5de-111">Le comportement exact dépend de l’implémentation du décodeur.</span><span class="sxs-lookup"><span data-stu-id="9d5de-111">The exact behavior depends on the decoder implementation.</span></span> <span data-ttu-id="9d5de-112">Tous les incréments compris entre 1 et 32 ne sont pas nécessairement définis comme un mode distinct.</span><span class="sxs-lookup"><span data-stu-id="9d5de-112">Not every increment between 1 and 32 necessarily defines is a distinct mode.</span></span>

<span data-ttu-id="9d5de-113">L’énumération [**eAVFastDecodeMode**](/windows/desktop/api/codecapi/ne-codecapi-eavfastdecodemode) contient des modes prédéfinis pour cette propriété.</span><span class="sxs-lookup"><span data-stu-id="9d5de-113">The [**eAVFastDecodeMode**](/windows/desktop/api/codecapi/ne-codecapi-eavfastdecodemode) enumeration contains some predefined modes for this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d5de-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9d5de-114">Requirements</span></span>



| <span data-ttu-id="9d5de-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9d5de-115">Requirement</span></span> | <span data-ttu-id="9d5de-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d5de-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9d5de-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d5de-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9d5de-118">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="9d5de-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="9d5de-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d5de-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9d5de-120">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="9d5de-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="9d5de-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="9d5de-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d5de-122"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d5de-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d5de-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d5de-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d5de-124">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="9d5de-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="9d5de-125">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="9d5de-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




