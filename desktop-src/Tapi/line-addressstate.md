---
description: Le \_ message ADDRESSSTATE de ligne TAPI est envoyé lorsque l’état d’une adresse est modifié sur une ligne actuellement ouverte par l’application. L’application peut appeler lineGetAddressStatus pour déterminer l’état actuel de l’adresse.
ms.assetid: af211fa1-79f8-49ac-a1d8-b62981f50519
title: Message LINE_ADDRESSSTATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d85b42f6957487ff24706485bd09d1d47880fe9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542300"
---
# <a name="line_addressstate-message"></a><span data-ttu-id="5411a-104">\_Message ADDRESSSTATE de ligne</span><span class="sxs-lookup"><span data-stu-id="5411a-104">LINE\_ADDRESSSTATE message</span></span>

<span data-ttu-id="5411a-105">Le message **\_ ADDRESSSTATE de ligne** TAPI est envoyé lorsque l’état d’une adresse est modifié sur une ligne actuellement ouverte par l’application.</span><span class="sxs-lookup"><span data-stu-id="5411a-105">The TAPI **LINE\_ADDRESSSTATE** message is sent when the status of an address changes on a line that is currently open by the application.</span></span> <span data-ttu-id="5411a-106">L’application peut appeler [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus) pour déterminer l’état actuel de l’adresse.</span><span class="sxs-lookup"><span data-stu-id="5411a-106">The application can invoke [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus) to determine the current status of the address.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="5411a-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5411a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5411a-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="5411a-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="5411a-109">Handle de l’appareil de ligne.</span><span class="sxs-lookup"><span data-stu-id="5411a-109">A handle to the line device.</span></span>

</dd> <dt>

<span data-ttu-id="5411a-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="5411a-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="5411a-111">Instance de rappel fournie lors de l’ouverture de la ligne.</span><span class="sxs-lookup"><span data-stu-id="5411a-111">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="5411a-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="5411a-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="5411a-113">Identificateur d’adresse de l’adresse qui a modifié l’État.</span><span class="sxs-lookup"><span data-stu-id="5411a-113">The address identifier of the address that changed status.</span></span>

</dd> <dt>

<span data-ttu-id="5411a-114">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="5411a-114">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="5411a-115">État de l’adresse qui a changé.</span><span class="sxs-lookup"><span data-stu-id="5411a-115">The address state that changed.</span></span> <span data-ttu-id="5411a-116">Il peut s’agir d’une ou plusieurs des [**\_ constantes LINEADDRESSSTATE**](lineaddressstate--constants.md).</span><span class="sxs-lookup"><span data-stu-id="5411a-116">Can be one or more of the [**LINEADDRESSSTATE\_ constants**](lineaddressstate--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="5411a-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="5411a-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="5411a-118">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="5411a-118">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5411a-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5411a-119">Return value</span></span>

<span data-ttu-id="5411a-120">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="5411a-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5411a-121">Notes</span><span class="sxs-lookup"><span data-stu-id="5411a-121">Remarks</span></span>

<span data-ttu-id="5411a-122">La **ligne \_ ADDRESSSTATE** message est envoyée à toute application qui a ouvert le périphérique de ligne et qui a activé ce message.</span><span class="sxs-lookup"><span data-stu-id="5411a-122">The **LINE\_ADDRESSSTATE** message is sent to any application that has opened the line device and that has enabled this message.</span></span> <span data-ttu-id="5411a-123">L’envoi de ce message pour les différents éléments d’État peut être contrôlé et interrogé à l’aide de [**lineGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linegetstatusmessages) et [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages).</span><span class="sxs-lookup"><span data-stu-id="5411a-123">The sending of this message for the various status items can be controlled and queried using [**lineGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linegetstatusmessages) and [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages).</span></span> <span data-ttu-id="5411a-124">Par défaut, le rapport d’état de l’adresse est désactivé.</span><span class="sxs-lookup"><span data-stu-id="5411a-124">By default, address status reporting is disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="5411a-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5411a-125">Requirements</span></span>



| <span data-ttu-id="5411a-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5411a-126">Requirement</span></span> | <span data-ttu-id="5411a-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="5411a-127">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="5411a-128">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="5411a-128">TAPI version</span></span><br/> | <span data-ttu-id="5411a-129">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="5411a-129">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="5411a-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="5411a-130">Header</span></span><br/>       | <dl> <span data-ttu-id="5411a-131"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="5411a-131"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5411a-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5411a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5411a-133">**LINEADDRESSCAPS**</span><span class="sxs-lookup"><span data-stu-id="5411a-133">**LINEADDRESSCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[<span data-ttu-id="5411a-134">**lineGetAddressCaps**</span><span class="sxs-lookup"><span data-stu-id="5411a-134">**lineGetAddressCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)
</dt> <dt>

[<span data-ttu-id="5411a-135">**lineGetAddressStatus**</span><span class="sxs-lookup"><span data-stu-id="5411a-135">**lineGetAddressStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)
</dt> <dt>

[<span data-ttu-id="5411a-136">**lineGetStatusMessages**</span><span class="sxs-lookup"><span data-stu-id="5411a-136">**lineGetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetstatusmessages)
</dt> <dt>

[<span data-ttu-id="5411a-137">**lineSetStatusMessages**</span><span class="sxs-lookup"><span data-stu-id="5411a-137">**lineSetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages)
</dt> </dl>

 

 




