---
description: Une opération a été abandonnée en raison d’une erreur.
ms.assetid: de7b5222-3a29-40cc-af1a-2672bd68b7c9
title: EC_ERRORABORTEX (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8465825b93207059e5f2ea5f054deb7c3fd5619f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545948"
---
# <a name="ec_errorabortex"></a><span data-ttu-id="a8bef-103">\_ERRORABORTEX EC</span><span class="sxs-lookup"><span data-stu-id="a8bef-103">EC\_ERRORABORTEX</span></span>

<span data-ttu-id="a8bef-104">Une opération a été abandonnée en raison d’une erreur.</span><span class="sxs-lookup"><span data-stu-id="a8bef-104">An operation was aborted because of an error.</span></span>

## <a name="parameters"></a><span data-ttu-id="a8bef-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a8bef-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8bef-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="a8bef-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="a8bef-107">**(HRESULT)** Code d’échec de l’opération qui a échoué.</span><span class="sxs-lookup"><span data-stu-id="a8bef-107">**(HRESULT)** Failure code of the operation that failed.</span></span>

</dd> <dt>

<span data-ttu-id="a8bef-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="a8bef-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="a8bef-109">**(BSTR)** Chaîne qui contient des informations supplémentaires sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="a8bef-109">**(BSTR)** String that contains additional error information.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="a8bef-110">Action par défaut</span><span class="sxs-lookup"><span data-stu-id="a8bef-110">Default Action</span></span>

<span data-ttu-id="a8bef-111">Aucun.</span><span class="sxs-lookup"><span data-stu-id="a8bef-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8bef-112">Notes</span><span class="sxs-lookup"><span data-stu-id="a8bef-112">Remarks</span></span>

<span data-ttu-id="a8bef-113">Le filtre de [source Windows Media](windows-media-source-filter.md) hérité envoie cet événement.</span><span class="sxs-lookup"><span data-stu-id="a8bef-113">The legacy [Windows Media Source](windows-media-source-filter.md) filter sends this event.</span></span> <span data-ttu-id="a8bef-114">Les nouveaux filtres ne doivent pas envoyer cet événement.</span><span class="sxs-lookup"><span data-stu-id="a8bef-114">New filters should not send this event.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8bef-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a8bef-115">Requirements</span></span>



| <span data-ttu-id="a8bef-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a8bef-116">Requirement</span></span> | <span data-ttu-id="a8bef-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="a8bef-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a8bef-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="a8bef-118">Header</span></span><br/> | <dl> <span data-ttu-id="a8bef-119"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8bef-119"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8bef-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8bef-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8bef-121">Codes de notification d’événement</span><span class="sxs-lookup"><span data-stu-id="a8bef-121">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="a8bef-122">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="a8bef-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




