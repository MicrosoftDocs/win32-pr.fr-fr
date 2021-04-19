---
description: 'Le WiaTransferParams est transmis à une application lors d’un transfert de données par le système d’exécution WIA (Windows Image Acquisition) à la méthode IWiaTransferCallback :: TransferCallback.'
ms.assetid: 4f1bbacf-e9fd-4129-ab05-3edaeecfaf43
title: WiaTransferParams, structure (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WiaTransferParams
api_type:
- HeaderDef
api_location:
- Wia.h
ms.openlocfilehash: 4c432cab14e08d89a49234dd7c6de059cc9d72c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516883"
---
# <a name="wiatransferparams-structure"></a><span data-ttu-id="eca3e-103">WiaTransferParams, structure</span><span class="sxs-lookup"><span data-stu-id="eca3e-103">WiaTransferParams structure</span></span>

<span data-ttu-id="eca3e-104">Le **WiaTransferParams** est transmis à une application lors d’un transfert de données par le système d’exécution WIA (Windows Image Acquisition) à la méthode [**IWiaTransferCallback :: TransferCallback**](-wia-iwiatransfercallback-transfercallback.md) .</span><span class="sxs-lookup"><span data-stu-id="eca3e-104">The **WiaTransferParams** is transmitted to an application during a data transfer by the Windows Image Acquisition (WIA) run-time system to the [**IWiaTransferCallback::TransferCallback**](-wia-iwiatransfercallback-transfercallback.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="eca3e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eca3e-105">Syntax</span></span>


```C++
typedef struct _WiaTransferParams {
  LONG    lMessage;
  LONG    lPercentComplete;
  ULONG64 ulTransferredBytes;
  HRESULT hrErrorStatus;
} WiaTransferParams;
```



## <a name="members"></a><span data-ttu-id="eca3e-106">Membres</span><span class="sxs-lookup"><span data-stu-id="eca3e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="eca3e-107">**lMessage**</span><span class="sxs-lookup"><span data-stu-id="eca3e-107">**lMessage**</span></span>
</dt> <dd>

<span data-ttu-id="eca3e-108">Type : **long**</span><span class="sxs-lookup"><span data-stu-id="eca3e-108">Type: **LONG**</span></span>

</dd> <dd>

<span data-ttu-id="eca3e-109">Indique l’état du transfert de données.</span><span class="sxs-lookup"><span data-stu-id="eca3e-109">Indicates the status of the data transfer.</span></span>

<dt>

<span id="WIA_TRANSFER_MSG_STATUS"></span><span id="wia_transfer_msg_status"></span>

<span data-ttu-id="eca3e-110"><span id="WIA_TRANSFER_MSG_STATUS"></span><span id="wia_transfer_msg_status"></span>**\_État du \_ message de transfert WIA \_**</span><span class="sxs-lookup"><span data-stu-id="eca3e-110"><span id="WIA_TRANSFER_MSG_STATUS"></span><span id="wia_transfer_msg_status"></span>**WIA\_TRANSFER\_MSG\_STATUS**</span></span>


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_END_OF_STREAM"></span><span id="wia_transfer_msg_end_of_stream"></span>

<span data-ttu-id="eca3e-111"><span id="WIA_TRANSFER_MSG_END_OF_STREAM"></span><span id="wia_transfer_msg_end_of_stream"></span>**\_ \_ \_ fin \_ du flux de messages de transfert WIA \_**</span><span class="sxs-lookup"><span data-stu-id="eca3e-111"><span id="WIA_TRANSFER_MSG_END_OF_STREAM"></span><span id="wia_transfer_msg_end_of_stream"></span>**WIA\_TRANSFER\_MSG\_END\_OF\_STREAM**</span></span>


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_END_OF_TRANSFER"></span><span id="wia_transfer_msg_end_of_transfer"></span>

<span data-ttu-id="eca3e-112"><span id="WIA_TRANSFER_MSG_END_OF_TRANSFER"></span><span id="wia_transfer_msg_end_of_transfer"></span>**\_ \_ \_ fin \_ du transfert du message \_ WIA Transfer**</span><span class="sxs-lookup"><span data-stu-id="eca3e-112"><span id="WIA_TRANSFER_MSG_END_OF_TRANSFER"></span><span id="wia_transfer_msg_end_of_transfer"></span>**WIA\_TRANSFER\_MSG\_END\_OF\_TRANSFER**</span></span>


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_DEVICE_STATUS"></span><span id="wia_transfer_msg_device_status"></span>

<span data-ttu-id="eca3e-113"><span id="WIA_TRANSFER_MSG_DEVICE_STATUS"></span><span id="wia_transfer_msg_device_status"></span>**État de l’appareil de message de \_ transfert WIA \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="eca3e-113"><span id="WIA_TRANSFER_MSG_DEVICE_STATUS"></span><span id="wia_transfer_msg_device_status"></span>**WIA\_TRANSFER\_MSG\_DEVICE\_STATUS**</span></span>


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_NEW_PAGE"></span><span id="wia_transfer_msg_new_page"></span>

<span data-ttu-id="eca3e-114"><span id="WIA_TRANSFER_MSG_NEW_PAGE"></span><span id="wia_transfer_msg_new_page"></span>**\_ \_ \_ page nouveau message de transfert WIA \_**</span><span class="sxs-lookup"><span data-stu-id="eca3e-114"><span id="WIA_TRANSFER_MSG_NEW_PAGE"></span><span id="wia_transfer_msg_new_page"></span>**WIA\_TRANSFER\_MSG\_NEW\_PAGE**</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="eca3e-115">**lPercentComplete**</span><span class="sxs-lookup"><span data-stu-id="eca3e-115">**lPercentComplete**</span></span>
</dt> <dd>

<span data-ttu-id="eca3e-116">Type : **long**</span><span class="sxs-lookup"><span data-stu-id="eca3e-116">Type: **LONG**</span></span>

</dd> <dd>

<span data-ttu-id="eca3e-117">Indique la progression du transfert de données sous la forme d’un pourcentage.</span><span class="sxs-lookup"><span data-stu-id="eca3e-117">Indicates the progress of the data transfer as a percentage.</span></span>

</dd> <dt>

<span data-ttu-id="eca3e-118">**ulTransferredBytes**</span><span class="sxs-lookup"><span data-stu-id="eca3e-118">**ulTransferredBytes**</span></span>
</dt> <dd>

<span data-ttu-id="eca3e-119">Type : **ULONG64**</span><span class="sxs-lookup"><span data-stu-id="eca3e-119">Type: **ULONG64**</span></span>

</dd> <dd>

<span data-ttu-id="eca3e-120">Indique la quantité de données transférées.</span><span class="sxs-lookup"><span data-stu-id="eca3e-120">Indicates the amount of data transferred.</span></span>

</dd> <dt>

<span data-ttu-id="eca3e-121">**hrErrorStatus**</span><span class="sxs-lookup"><span data-stu-id="eca3e-121">**hrErrorStatus**</span></span>
</dt> <dd>

<span data-ttu-id="eca3e-122">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="eca3e-122">Type: **HRESULT**</span></span>

</dd> <dd>

<span data-ttu-id="eca3e-123">État ou état d’erreur de l’appareil défini par le pilote ; par exemple, « préchauffage ».</span><span class="sxs-lookup"><span data-stu-id="eca3e-123">The status, or error state, of the device set by the driver; for example, "warming up".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eca3e-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eca3e-124">Requirements</span></span>



| <span data-ttu-id="eca3e-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eca3e-125">Requirement</span></span> | <span data-ttu-id="eca3e-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="eca3e-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="eca3e-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eca3e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="eca3e-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eca3e-128">Windows Vista \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="eca3e-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eca3e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="eca3e-130">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eca3e-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="eca3e-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="eca3e-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="eca3e-132"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="eca3e-132"><dt>Wia.h</dt></span></span> </dl> |



 

 




