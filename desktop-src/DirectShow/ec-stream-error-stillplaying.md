---
description: Une erreur s’est produite dans un flux, mais le flux est toujours en cours d’exécution.
ms.assetid: ff155c01-22ba-46dd-85b8-05eabf956908
title: EC_STREAM_ERROR_STILLPLAYING (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5db74a9f16a0ca01ce74e6d94df50cc402221aaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535951"
---
# <a name="ec_stream_error_stillplaying"></a><span data-ttu-id="21f5e-103">\_erreur de flux EC \_ \_ STILLPLAYING</span><span class="sxs-lookup"><span data-stu-id="21f5e-103">EC\_STREAM\_ERROR\_STILLPLAYING</span></span>

<span data-ttu-id="21f5e-104">Une erreur s’est produite dans un flux, mais le flux est toujours en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="21f5e-104">An error occurred in a stream, but the stream is still playing.</span></span>

## <a name="parameters"></a><span data-ttu-id="21f5e-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="21f5e-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21f5e-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="21f5e-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="21f5e-107">(**HRESULT**) Code d’échec de l’opération qui a échoué.</span><span class="sxs-lookup"><span data-stu-id="21f5e-107">(**HRESULT**) Failure code of the operation that failed.</span></span>

</dd> <dt>

<span data-ttu-id="21f5e-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="21f5e-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="21f5e-109">(**DWORD**) Code d’erreur mineur.</span><span class="sxs-lookup"><span data-stu-id="21f5e-109">(**DWORD**) Minor error code.</span></span> <span data-ttu-id="21f5e-110">Cette valeur est généralement égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="21f5e-110">This value is usually zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="21f5e-111">Action par défaut</span><span class="sxs-lookup"><span data-stu-id="21f5e-111">Default Action</span></span>

<span data-ttu-id="21f5e-112">Aucun</span><span class="sxs-lookup"><span data-stu-id="21f5e-112">None.</span></span> <span data-ttu-id="21f5e-113">L’application doit décider d’arrêter ou non le graphique.</span><span class="sxs-lookup"><span data-stu-id="21f5e-113">The application must decide whether to stop the graph.</span></span>

## <a name="requirements"></a><span data-ttu-id="21f5e-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="21f5e-114">Requirements</span></span>



| <span data-ttu-id="21f5e-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="21f5e-115">Requirement</span></span> | <span data-ttu-id="21f5e-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="21f5e-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="21f5e-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="21f5e-117">Header</span></span><br/> | <dl> <span data-ttu-id="21f5e-118"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="21f5e-118"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21f5e-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="21f5e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21f5e-120">Codes de notification d’événement</span><span class="sxs-lookup"><span data-stu-id="21f5e-120">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="21f5e-121">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="21f5e-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




