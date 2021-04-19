---
description: Définit le type de la notification transmise à la \_ fonction de rappel de notification du récepteur d’affichage WFD \_ \_ \_ .
ms.assetid: C0AFF80E-A4D2-4FF1-B111-D628AF8755A8
title: Énumération WFD_DISPLAY_SINK_NOTIFICATION_TYPE (Wfdsink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFD_DISPLAY_SINK_NOTIFICATION_TYPE
api_type:
- HeaderDef
api_location:
- wfdsink.h
ms.openlocfilehash: 25361b0f3529da0293f373117c7bf655635de852
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544835"
---
# <a name="wfd_display_sink_notification_type-enumeration"></a><span data-ttu-id="57ed7-103">\_ \_ \_ Énumération des types de notification du récepteur d’affichage WFD \_</span><span class="sxs-lookup"><span data-stu-id="57ed7-103">WFD\_DISPLAY\_SINK\_NOTIFICATION\_TYPE enumeration</span></span>

<span data-ttu-id="57ed7-104">Le type d’énumération du **type de notification du \_ récepteur d’affichage \_ \_ \_ WFD** définit le type de la notification transmise à la fonction de [**rappel de notification du \_ récepteur d’affichage \_ \_ \_ WFD**](wfd-display-sink-notification-callback.md) .</span><span class="sxs-lookup"><span data-stu-id="57ed7-104">The **WFD\_DISPLAY\_SINK\_NOTIFICATION\_TYPE** enumerated type defines the type of the notification passed to the [**WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK**](wfd-display-sink-notification-callback.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="57ed7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="57ed7-105">Syntax</span></span>


```C++
typedef enum _WFD_DISPLAY_SINK_NOTIFICATION_TYPE { 
  ProvisioningRequestNotification,
  ReconnectRequestNotification,
  ConnectedNotification,
  DisconnectedNotification
} WFD_DISPLAY_SINK_NOTIFICATION_TYPE, *PWFD_DISPLAY_SINK_NOTIFICATION_TYPE;
```



## <a name="constants"></a><span data-ttu-id="57ed7-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="57ed7-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="57ed7-107"><span id="ProvisioningRequestNotification"></span><span id="provisioningrequestnotification"></span><span id="PROVISIONINGREQUESTNOTIFICATION"></span>**ProvisioningRequestNotification**</span><span class="sxs-lookup"><span data-stu-id="57ed7-107"><span id="ProvisioningRequestNotification"></span><span id="provisioningrequestnotification"></span><span id="PROVISIONINGREQUESTNOTIFICATION"></span>**ProvisioningRequestNotification**</span></span>
</dt> <dd>

<span data-ttu-id="57ed7-108">La notification est une demande d’approvisionnement.</span><span class="sxs-lookup"><span data-stu-id="57ed7-108">The notification is a provisioning request.</span></span>

</dd> <dt>

<span data-ttu-id="57ed7-109"><span id="ReconnectRequestNotification"></span><span id="reconnectrequestnotification"></span><span id="RECONNECTREQUESTNOTIFICATION"></span>**ReconnectRequestNotification**</span><span class="sxs-lookup"><span data-stu-id="57ed7-109"><span id="ReconnectRequestNotification"></span><span id="reconnectrequestnotification"></span><span id="RECONNECTREQUESTNOTIFICATION"></span>**ReconnectRequestNotification**</span></span>
</dt> <dd>

<span data-ttu-id="57ed7-110">La notification est une demande de reconnexion.</span><span class="sxs-lookup"><span data-stu-id="57ed7-110">The notification is a reconnect request.</span></span>

</dd> <dt>

<span data-ttu-id="57ed7-111"><span id="ConnectedNotification"></span><span id="connectednotification"></span><span id="CONNECTEDNOTIFICATION"></span>**ConnectedNotification**</span><span class="sxs-lookup"><span data-stu-id="57ed7-111"><span id="ConnectedNotification"></span><span id="connectednotification"></span><span id="CONNECTEDNOTIFICATION"></span>**ConnectedNotification**</span></span>
</dt> <dd>

<span data-ttu-id="57ed7-112">La notification est une notification connectée.</span><span class="sxs-lookup"><span data-stu-id="57ed7-112">The notification is a connected notification.</span></span>

</dd> <dt>

<span data-ttu-id="57ed7-113"><span id="DisconnectedNotification"></span><span id="disconnectednotification"></span><span id="DISCONNECTEDNOTIFICATION"></span>**DisconnectedNotification**</span><span class="sxs-lookup"><span data-stu-id="57ed7-113"><span id="DisconnectedNotification"></span><span id="disconnectednotification"></span><span id="DISCONNECTEDNOTIFICATION"></span>**DisconnectedNotification**</span></span>
</dt> <dd>

<span data-ttu-id="57ed7-114">La notification est une notification déconnectée.</span><span class="sxs-lookup"><span data-stu-id="57ed7-114">The notification is a disconnected notification.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="57ed7-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="57ed7-115">Requirements</span></span>



| <span data-ttu-id="57ed7-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="57ed7-116">Requirement</span></span> | <span data-ttu-id="57ed7-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="57ed7-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="57ed7-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="57ed7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="57ed7-119">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="57ed7-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="57ed7-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="57ed7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="57ed7-121">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="57ed7-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="57ed7-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="57ed7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="57ed7-123"><dt>Wfdsink. h</dt></span><span class="sxs-lookup"><span data-stu-id="57ed7-123"><dt>Wfdsink.h</dt></span></span> </dl> |



 

 




