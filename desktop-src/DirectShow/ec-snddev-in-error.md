---
description: Une erreur d’appareil s’est produite dans un filtre de capture audio.
ms.assetid: 13f8641b-7881-4f1c-816c-77c140e48ed4
title: EC_SNDDEV_IN_ERROR (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26f9b95055483b1bda812179f1a1bf132d12de7f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534854"
---
# <a name="ec_snddev_in_error"></a><span data-ttu-id="f5bee-103">EC \_ SNDDEV \_ en \_ erreur</span><span class="sxs-lookup"><span data-stu-id="f5bee-103">EC\_SNDDEV\_IN\_ERROR</span></span>

<span data-ttu-id="f5bee-104">Une erreur d’appareil s’est produite dans un filtre de capture audio.</span><span class="sxs-lookup"><span data-stu-id="f5bee-104">A device error has occurred in an audio capture filter.</span></span>

## <a name="parameters"></a><span data-ttu-id="f5bee-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f5bee-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5bee-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="f5bee-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="f5bee-107">Valeur DWORD du type énuméré [**SNDDEV \_ Err**](/previous-versions/windows/desktop/api/audevcod/ne-audevcod-snddev_err) , indiquant comment l’appareil a fait l’objet d’un accès lorsque la défaillance s’est produite.</span><span class="sxs-lookup"><span data-stu-id="f5bee-107">DWORD value from the [**SNDDEV\_ERR**](/previous-versions/windows/desktop/api/audevcod/ne-audevcod-snddev_err) enumerated type, indicating how the device was being accessed when the failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="f5bee-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="f5bee-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="f5bee-109">Valeur DWORD indiquant l’erreur renvoyée par l’appel de périphérique audio.</span><span class="sxs-lookup"><span data-stu-id="f5bee-109">DWORD value indicating the error returned from the sound device call.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="f5bee-110">Action par défaut</span><span class="sxs-lookup"><span data-stu-id="f5bee-110">Default Action</span></span>

<span data-ttu-id="f5bee-111">Aucun</span><span class="sxs-lookup"><span data-stu-id="f5bee-111">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5bee-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f5bee-112">Requirements</span></span>



| <span data-ttu-id="f5bee-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f5bee-113">Requirement</span></span> | <span data-ttu-id="f5bee-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5bee-114">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f5bee-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="f5bee-115">Header</span></span><br/> | <dl> <span data-ttu-id="f5bee-116"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5bee-116"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5bee-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5bee-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5bee-118">Codes de notification d’événement</span><span class="sxs-lookup"><span data-stu-id="f5bee-118">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="f5bee-119">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="f5bee-119">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




