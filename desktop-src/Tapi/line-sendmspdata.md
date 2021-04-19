---
description: Le message SENDMSPDATA de la ligne TSPI \_ est envoyé lorsque le fournisseur de services de téléphonie (TSP) souhaite transmettre des informations au fournisseur de services multimédia (MSP).
ms.assetid: 982f40b3-7758-493c-9d04-6480e3c9e86d
title: Message LINE_SENDMSPDATA (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce46664be0bc7f312af8b45cc5e06e13a7d91488
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525200"
---
# <a name="line_sendmspdata-message"></a><span data-ttu-id="1bf87-103">\_Message SENDMSPDATA de ligne</span><span class="sxs-lookup"><span data-stu-id="1bf87-103">LINE\_SENDMSPDATA message</span></span>

<span data-ttu-id="1bf87-104">Le message **\_ SENDMSPDATA** de la ligne TSPI est envoyé lorsque le fournisseur de services de téléphonie (TSP) souhaite transmettre des informations au fournisseur de services multimédia (MSP).</span><span class="sxs-lookup"><span data-stu-id="1bf87-104">The TSPI **LINE\_SENDMSPDATA** message is sent when the telephony service provider (TSP) wants to pass information to the media service provider (MSP).</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="1bf87-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1bf87-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1bf87-106">*htLine*</span><span class="sxs-lookup"><span data-stu-id="1bf87-106">*htLine*</span></span> 
</dt> <dd>

<span data-ttu-id="1bf87-107">Handle TAPI pour la ligne.</span><span class="sxs-lookup"><span data-stu-id="1bf87-107">The TAPI handle for the line.</span></span>

</dd> <dt>

<span data-ttu-id="1bf87-108">*htCall*</span><span class="sxs-lookup"><span data-stu-id="1bf87-108">*htCall*</span></span> 
</dt> <dd>

<span data-ttu-id="1bf87-109">Handle TAPI pour l’appel.</span><span class="sxs-lookup"><span data-stu-id="1bf87-109">The TAPI handle for the call.</span></span>

</dd> <dt>

<span data-ttu-id="1bf87-110">*dwMsg*</span><span class="sxs-lookup"><span data-stu-id="1bf87-110">*dwMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="1bf87-111">La ligne de valeur \_ SENDMSPDATA.</span><span class="sxs-lookup"><span data-stu-id="1bf87-111">The value LINE\_SENDMSPDATA.</span></span>

</dd> <dt>

<span data-ttu-id="1bf87-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="1bf87-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="1bf87-113">Identifie le MSP qui doit recevoir le message.</span><span class="sxs-lookup"><span data-stu-id="1bf87-113">Identifies the MSP that should receive the message.</span></span> <span data-ttu-id="1bf87-114">Si la valeur est 0, le message est envoyé à tous les MSP.</span><span class="sxs-lookup"><span data-stu-id="1bf87-114">If 0, the message will be sent to all MSPs.</span></span> <span data-ttu-id="1bf87-115">Il s’agit du handle qui est passé à la fonction [**TSPI \_ LineCreateMSPInstance**](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance) .</span><span class="sxs-lookup"><span data-stu-id="1bf87-115">This is the handle that is passed to the [**TSPI\_LineCreateMSPInstance**](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance) function.</span></span>

</dd> <dt>

<span data-ttu-id="1bf87-116">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="1bf87-116">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="1bf87-117">Mémoire tampon à transmettre au MSP.</span><span class="sxs-lookup"><span data-stu-id="1bf87-117">The buffer to pass to the MSP.</span></span> <span data-ttu-id="1bf87-118">La mémoire tampon n’est pas interprétée par TAPI.</span><span class="sxs-lookup"><span data-stu-id="1bf87-118">The buffer is not interpreted by TAPI.</span></span>

</dd> <dt>

<span data-ttu-id="1bf87-119">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="1bf87-119">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="1bf87-120">Taille, en octets, de la mémoire tampon dans *dwParam2*.</span><span class="sxs-lookup"><span data-stu-id="1bf87-120">The size, in bytes, of the buffer in *dwParam2*.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1bf87-121">Notes</span><span class="sxs-lookup"><span data-stu-id="1bf87-121">Remarks</span></span>

<span data-ttu-id="1bf87-122">Le fournisseur de services doit négocier une version TAPI 3,0 ou ultérieure pour que ce message fonctionne.</span><span class="sxs-lookup"><span data-stu-id="1bf87-122">The service provider must negotiate a TAPI version 3.0 or later for this message to operate.</span></span>

## <a name="requirements"></a><span data-ttu-id="1bf87-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1bf87-123">Requirements</span></span>



| <span data-ttu-id="1bf87-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1bf87-124">Requirement</span></span> | <span data-ttu-id="1bf87-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="1bf87-125">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="1bf87-126">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="1bf87-126">TAPI version</span></span><br/> | <span data-ttu-id="1bf87-127">Nécessite TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="1bf87-127">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="1bf87-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="1bf87-128">Header</span></span><br/>       | <dl> <span data-ttu-id="1bf87-129"><dt>TSPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="1bf87-129"><dt>Tspi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1bf87-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1bf87-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bf87-131">À propos du fournisseur de services multimédia (MSP)</span><span class="sxs-lookup"><span data-stu-id="1bf87-131">About The Media Service Provider (MSP)</span></span>](./about-the-media-service-provider-msp-.md)
</dt> <dt>

[<span data-ttu-id="1bf87-132">**TSPI \_ lineMSPIdentify**</span><span class="sxs-lookup"><span data-stu-id="1bf87-132">**TSPI\_lineMSPIdentify**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linemspidentify)
</dt> <dt>

[<span data-ttu-id="1bf87-133">**TSPI \_ LineCreateMSPInstance**</span><span class="sxs-lookup"><span data-stu-id="1bf87-133">**TSPI\_LineCreateMSPInstance**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance)
</dt> <dt>

[<span data-ttu-id="1bf87-134">**TSPI \_ lineCloseMSPInstance**</span><span class="sxs-lookup"><span data-stu-id="1bf87-134">**TSPI\_lineCloseMSPInstance**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineclosemspinstance)
</dt> <dt>

[<span data-ttu-id="1bf87-135">**TSPI \_ lineRecieveMSPData**</span><span class="sxs-lookup"><span data-stu-id="1bf87-135">**TSPI\_lineRecieveMSPData**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata)
</dt> <dt>

[<span data-ttu-id="1bf87-136">**LINEDEVCAPS**</span><span class="sxs-lookup"><span data-stu-id="1bf87-136">**LINEDEVCAPS**</span></span>](/windows/win32/api/tapi/ns-tapi-linedevcaps)
</dt> </dl>

 

