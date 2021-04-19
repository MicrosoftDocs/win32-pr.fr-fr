---
description: Spécifie si l’application requiert des performances d’encodage en temps réel.
ms.assetid: 7e98a9f4-113b-45d0-ae55-7dc3f2af099e
title: Propriété AVEncCommonRealTime (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a03e51da1a088603273da3d083573e5921edf7a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106514097"
---
# <a name="avenccommonrealtime-property"></a><span data-ttu-id="a2148-103">Propriété AVEncCommonRealTime</span><span class="sxs-lookup"><span data-stu-id="a2148-103">AVEncCommonRealTime property</span></span>

<span data-ttu-id="a2148-104">Spécifie si l’application requiert des performances d’encodage en temps réel.</span><span class="sxs-lookup"><span data-stu-id="a2148-104">Specifies whether the application requires real-time encoding performance.</span></span>

<span data-ttu-id="a2148-105">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="a2148-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="a2148-106">Type de données</span><span class="sxs-lookup"><span data-stu-id="a2148-106">Data type</span></span>

<span data-ttu-id="a2148-107">**Variante \_ BOOL** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="a2148-107">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="a2148-108">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="a2148-108">Property GUID</span></span>

<span data-ttu-id="a2148-109">**CODECAPI \_ AVEncCommonRealTime**</span><span class="sxs-lookup"><span data-stu-id="a2148-109">**CODECAPI\_AVEncCommonRealTime**</span></span>

## <a name="remarks"></a><span data-ttu-id="a2148-110">Notes</span><span class="sxs-lookup"><span data-stu-id="a2148-110">Remarks</span></span>

<span data-ttu-id="a2148-111">Pour spécifier que l’encodage doit être exécuté en temps réel, affectez à cette propriété la **\_ valeur variant true**.</span><span class="sxs-lookup"><span data-stu-id="a2148-111">To specify that encoding must be performed in real time, set this property to **VARIANT\_TRUE**.</span></span> <span data-ttu-id="a2148-112">Les codecs peuvent également retourner cette propriété en tant que fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="a2148-112">Codecs can also return this property as a capability.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2148-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a2148-113">Requirements</span></span>



| <span data-ttu-id="a2148-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a2148-114">Requirement</span></span> | <span data-ttu-id="a2148-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="a2148-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a2148-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a2148-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a2148-117">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="a2148-117">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="a2148-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a2148-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a2148-119">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="a2148-119">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="a2148-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="a2148-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2148-121"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2148-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2148-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a2148-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2148-123">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="a2148-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="a2148-124">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="a2148-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




