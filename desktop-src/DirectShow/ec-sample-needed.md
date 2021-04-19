---
description: Demande un nouvel exemple d’entrée à partir du filtre de convertisseur vidéo amélioré (EVR).
ms.assetid: f1bf32ba-ecb7-435f-aefc-f60fdd355620
title: EC_SAMPLE_NEEDED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da73d02604e128fdf94edb8f84d1526cfcdb586e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520373"
---
# <a name="ec_sample_needed"></a><span data-ttu-id="9e954-103">\_exemple EC \_ requis</span><span class="sxs-lookup"><span data-stu-id="9e954-103">EC\_SAMPLE\_NEEDED</span></span>

<span data-ttu-id="9e954-104">Demande un nouvel exemple d’entrée à partir du filtre de [**convertisseur vidéo amélioré**](enhanced-video-renderer-filter.md) (EVR).</span><span class="sxs-lookup"><span data-stu-id="9e954-104">Requests a new input sample from the [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR) filter.</span></span>

## <a name="parameters"></a><span data-ttu-id="9e954-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9e954-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e954-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="9e954-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="9e954-107">Identificateur du flux d’entrée qui a besoin d’une nouvelle entrée.</span><span class="sxs-lookup"><span data-stu-id="9e954-107">Identifier of the input stream that needs new input.</span></span>

</dd> <dt>

<span data-ttu-id="9e954-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="9e954-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="9e954-109">Zéro.</span><span class="sxs-lookup"><span data-stu-id="9e954-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="9e954-110">Action par défaut</span><span class="sxs-lookup"><span data-stu-id="9e954-110">Default Action</span></span>

<span data-ttu-id="9e954-111">Aucun.</span><span class="sxs-lookup"><span data-stu-id="9e954-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e954-112">Notes</span><span class="sxs-lookup"><span data-stu-id="9e954-112">Remarks</span></span>

<span data-ttu-id="9e954-113">Le mélangeur pour le filtre EVR envoie ce message lorsqu’il a besoin d’un nouvel exemple d’entrée.</span><span class="sxs-lookup"><span data-stu-id="9e954-113">The mixer for the EVR filter sends this message when it needs a new input sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e954-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9e954-114">Requirements</span></span>



| <span data-ttu-id="9e954-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9e954-115">Requirement</span></span> | <span data-ttu-id="9e954-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e954-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9e954-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="9e954-117">Header</span></span><br/> | <dl> <span data-ttu-id="9e954-118"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e954-118"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e954-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e954-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e954-120">Codes de notification d’événement</span><span class="sxs-lookup"><span data-stu-id="9e954-120">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> </dl>

 

 




