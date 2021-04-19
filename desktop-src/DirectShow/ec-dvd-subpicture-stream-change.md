---
description: Signale que le numéro de flux de sous-image actuel a changé pour le titre principal.
ms.assetid: b6da3201-55df-47dc-ad4f-5cd2e78073ee
title: EC_DVD_SUBPICTURE_STREAM_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_SUBPICTURE_STREAM_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: c30ef0b27185b5300ac5cec877ed4e4b38685c12
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545417"
---
# <a name="ec_dvd_subpicture_stream_change"></a><span data-ttu-id="1a964-103">modification du flux de sous- \_ image de DVD EC \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="1a964-103">EC\_DVD\_SUBPICTURE\_STREAM\_CHANGE</span></span>

<span data-ttu-id="1a964-104">Signale que le numéro de flux de sous-image actuel a changé pour le titre principal.</span><span class="sxs-lookup"><span data-stu-id="1a964-104">Signals that the current subpicture stream number changed for the main title.</span></span>

## <a name="parameters"></a><span data-ttu-id="1a964-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1a964-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a964-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="1a964-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="1a964-107">Valeur **DWORD** indiquant le numéro du nouveau flux de sous-image de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1a964-107">**DWORD** value indicating the new user subpicture stream number.</span></span> <span data-ttu-id="1a964-108">Les numéros de flux de sous-image sont compris entre 0 et 31.</span><span class="sxs-lookup"><span data-stu-id="1a964-108">Subpicture stream numbers range from 0 to 31.</span></span> <span data-ttu-id="1a964-109">Stream 0xFFFFFFFF indique qu’aucun flux n’est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="1a964-109">Stream 0xFFFFFFFF indicates that no stream is selected.</span></span>

</dd> <dt>

<span data-ttu-id="1a964-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="1a964-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="1a964-111">Valeur booléenne qui indique l’état activé/désactivé de la sous-image.</span><span class="sxs-lookup"><span data-stu-id="1a964-111">Boolean value that indicates the subpicture's on/off state.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1a964-112">Notes</span><span class="sxs-lookup"><span data-stu-id="1a964-112">Remarks</span></span>

<span data-ttu-id="1a964-113">La sous-image peut changer automatiquement à l’aide d’une commande de navigation créée sur le disque, ainsi que via le contrôle d’application à l’aide de [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2).</span><span class="sxs-lookup"><span data-stu-id="1a964-113">The subpicture can change automatically with a navigation command authored on disc as well as through application control using [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2).</span></span>

<span data-ttu-id="1a964-114">Cet événement est déclenché dans tous les domaines.</span><span class="sxs-lookup"><span data-stu-id="1a964-114">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a964-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1a964-115">Requirements</span></span>



| <span data-ttu-id="1a964-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1a964-116">Requirement</span></span> | <span data-ttu-id="1a964-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="1a964-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a964-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="1a964-118">Header</span></span><br/> | <dl> <span data-ttu-id="1a964-119"><dt>Dvdevcode. h (inclure DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1a964-119"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a964-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a964-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a964-121">Applications DVD</span><span class="sxs-lookup"><span data-stu-id="1a964-121">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="1a964-122">Codes de notification des événements DVD</span><span class="sxs-lookup"><span data-stu-id="1a964-122">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="1a964-123">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="1a964-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




