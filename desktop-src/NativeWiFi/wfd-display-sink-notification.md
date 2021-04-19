---
description: Décrit la notification transmise à la \_ fonction de rappel de notification du récepteur d’affichage WFD \_ \_ \_ .
ms.assetid: 1CB91DD9-5B58-4FE0-B7B0-E6189760511A
title: Structure WFD_DISPLAY_SINK_NOTIFICATION (Wfdsink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFD_DISPLAY_SINK_NOTIFICATION
api_type:
- HeaderDef
api_location:
- wfdsink.h
ms.openlocfilehash: d4c2a15bbe6ef0df62fc0d607c97ecb3a2b54ec6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517063"
---
# <a name="wfd_display_sink_notification-structure"></a><span data-ttu-id="ca374-103">\_Structure de \_ notification du récepteur d’affichage WFD \_</span><span class="sxs-lookup"><span data-stu-id="ca374-103">WFD\_DISPLAY\_SINK\_NOTIFICATION structure</span></span>

<span data-ttu-id="ca374-104">La structure de **\_ notification du \_ récepteur \_ d’affichage WFD** décrit la notification transmise à la fonction de rappel de notification du [**récepteur d' \_ affichage \_ \_ \_ WFD**](wfd-display-sink-notification-callback.md) .</span><span class="sxs-lookup"><span data-stu-id="ca374-104">The **WFD\_DISPLAY\_SINK\_NOTIFICATION** structure describes the notification passed to the [**WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK**](wfd-display-sink-notification-callback.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca374-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ca374-105">Syntax</span></span>


```C++
typedef struct _WFD_DISPLAY_SINK_NOTIFICATION {
  WFD_DISPLAY_SINK_OBJECT_HEADER     Header;
  WFD_DISPLAY_SINK_NOTIFICATION_TYPE type;
  WCHAR                              strRemoteDeviceName[WFD_SINK_MAX_DEVICE_NAME_LENGTH + 1];
  DOT11_MAC_ADDRESS                  RemoteDeviceAddress;
  union {
    struct {
      HANDLE                  hSessionHandle;
      DOT11_WPS_CONFIG_METHOD PossibleConfigMethods;
    } ProvisioningRequestInfo;
    struct {
      DOT11_WFD_GROUP_ID GroupID;
    } ReconnectRequestInfo;
    struct {
      HANDLE             hSessionHandle;
      GUID               guidSessionInterface;
      DOT11_WFD_GROUP_ID GroupID;
      PWSTR              strProfile;
      SOCKADDR_STORAGE   LocalAddress;
      SOCKADDR_STORAGE   RemoteAddress;
      USHORT             uRTSPPort;
    } ConnectedInfo;
  };
} WFD_DISPLAY_SINK_NOTIFICATION, *PWFD_DISPLAY_SINK_NOTIFICATION;
```



## <a name="members"></a><span data-ttu-id="ca374-106">Membres</span><span class="sxs-lookup"><span data-stu-id="ca374-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ca374-107">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="ca374-107">**Header**</span></span>
</dt> <dd>

<span data-ttu-id="ca374-108">[**\_ \_ \_ \_ En-tête d’objet récepteur WFD**](wfd-display-sink-object-header.md) qui décrit les données incluses dans la notification.</span><span class="sxs-lookup"><span data-stu-id="ca374-108">A [**WFD\_DISPLAY\_SINK\_OBJECT\_HEADER**](wfd-display-sink-object-header.md) that describes the data included in the notification.</span></span>

</dd> <dt>

<span data-ttu-id="ca374-109">**type**</span><span class="sxs-lookup"><span data-stu-id="ca374-109">**type**</span></span>
</dt> <dd>

<span data-ttu-id="ca374-110">Valeur [**du \_ \_ type de \_ notification \_ du récepteur d’affichage WFD**](wfd-display-sink-notification-type.md) qui indique le type de la notification.</span><span class="sxs-lookup"><span data-stu-id="ca374-110">A [**WFD\_DISPLAY\_SINK\_NOTIFICATION\_TYPE**](wfd-display-sink-notification-type.md) value that indicates the type of the notification.</span></span> <span data-ttu-id="ca374-111">Ce paramètre détermine également les informations à utiliser dans l’Union ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="ca374-111">This parameter also determines which Info to use in the union below.</span></span>

</dd> <dt>

<span data-ttu-id="ca374-112">**strRemoteDeviceName**</span><span class="sxs-lookup"><span data-stu-id="ca374-112">**strRemoteDeviceName**</span></span>
</dt> <dd>

<span data-ttu-id="ca374-113">Contient une chaîne se terminant par un caractère NULL qui contient le nom de l’appareil distant.</span><span class="sxs-lookup"><span data-stu-id="ca374-113">Contains a NULL-terminated string containing the name of the remote device.</span></span> <span data-ttu-id="ca374-114">\_ \_ \_ \_ La longueur maximale du nom d’appareil du récepteur WFD \_ est définie en tant que valeur (32).</span><span class="sxs-lookup"><span data-stu-id="ca374-114">WFD\_SINK\_MAX\_DEVICE\_NAME\_LENGTH is defined as the value (32).</span></span>

</dd> <dt>

<span data-ttu-id="ca374-115">**RemoteDeviceAddress**</span><span class="sxs-lookup"><span data-stu-id="ca374-115">**RemoteDeviceAddress**</span></span>
</dt> <dd>

<span data-ttu-id="ca374-116">[**\_ \_ Adresse Mac DOT11**](dot11-mac-address-type.md) qui contient le BSSID du périphérique distant.</span><span class="sxs-lookup"><span data-stu-id="ca374-116">A [**DOT11\_MAC\_ADDRESS**](dot11-mac-address-type.md) that contains the BSSID of the remote device.</span></span>

</dd> <dt>

<span data-ttu-id="ca374-117">**ProvisioningRequestInfo**</span><span class="sxs-lookup"><span data-stu-id="ca374-117">**ProvisioningRequestInfo**</span></span>
</dt> <dd>

<span data-ttu-id="ca374-118">Informations sur une demande d’approvisionnement.</span><span class="sxs-lookup"><span data-stu-id="ca374-118">Info about a provisioning request.</span></span> <span data-ttu-id="ca374-119">Utilisez cette valeur si le *type* a la valeur **ProvisioningRequestNotification**.</span><span class="sxs-lookup"><span data-stu-id="ca374-119">Use this if *type* has the value **ProvisioningRequestNotification**.</span></span>

<dl> <dt>

<span data-ttu-id="ca374-120">**hSessionHandle**</span><span class="sxs-lookup"><span data-stu-id="ca374-120">**hSessionHandle**</span></span>
</dt> <dd>

<span data-ttu-id="ca374-121">Handle de session.</span><span class="sxs-lookup"><span data-stu-id="ca374-121">The session handle.</span></span>

</dd> <dt>

<span data-ttu-id="ca374-122">**PossibleConfigMethods**</span><span class="sxs-lookup"><span data-stu-id="ca374-122">**PossibleConfigMethods**</span></span>
</dt> <dd>

<span data-ttu-id="ca374-123">Méthodes possibles pour l’indication de l’interface utilisateur pour l’acceptation interactive.</span><span class="sxs-lookup"><span data-stu-id="ca374-123">Possible methods for showing UI for interactive acceptance.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="ca374-124">**ReconnectRequestInfo**</span><span class="sxs-lookup"><span data-stu-id="ca374-124">**ReconnectRequestInfo**</span></span>
</dt> <dd>

<span data-ttu-id="ca374-125">Informations sur une demande de reconnexion.</span><span class="sxs-lookup"><span data-stu-id="ca374-125">Info about a reconnect request.</span></span> <span data-ttu-id="ca374-126">Utilisez cette valeur si le *type* a la valeur **ReconnectRequestNotification**.</span><span class="sxs-lookup"><span data-stu-id="ca374-126">Use this if *type* has the value **ReconnectRequestNotification**.</span></span>

<dl> <dt>

<span data-ttu-id="ca374-127">**GroupID**</span><span class="sxs-lookup"><span data-stu-id="ca374-127">**GroupID**</span></span>
</dt> <dd>

<span data-ttu-id="ca374-128">ID de groupe.</span><span class="sxs-lookup"><span data-stu-id="ca374-128">The group id.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="ca374-129">**ConnectedInfo**</span><span class="sxs-lookup"><span data-stu-id="ca374-129">**ConnectedInfo**</span></span>
</dt> <dd>

<span data-ttu-id="ca374-130">Informations sur une notification connectée.</span><span class="sxs-lookup"><span data-stu-id="ca374-130">Info about a connected notification.</span></span> <span data-ttu-id="ca374-131">Utilisez cette valeur si le *type* a la valeur **ConnectedNotification**.</span><span class="sxs-lookup"><span data-stu-id="ca374-131">Use this if *type* has the value **ConnectedNotification**.</span></span>

<dl> <dt>

<span data-ttu-id="ca374-132">**hSessionHandle**</span><span class="sxs-lookup"><span data-stu-id="ca374-132">**hSessionHandle**</span></span>
</dt> <dd>

<span data-ttu-id="ca374-133">Handle de session.</span><span class="sxs-lookup"><span data-stu-id="ca374-133">The session handle.</span></span>

</dd> <dt>

<span data-ttu-id="ca374-134">**guidSessionInterface**</span><span class="sxs-lookup"><span data-stu-id="ca374-134">**guidSessionInterface**</span></span>
</dt> <dd>

<span data-ttu-id="ca374-135">GUID indiquant l’interface de la session.</span><span class="sxs-lookup"><span data-stu-id="ca374-135">A GUID indicating the session interface.</span></span>

</dd> <dt>

<span data-ttu-id="ca374-136">**GroupID**</span><span class="sxs-lookup"><span data-stu-id="ca374-136">**GroupID**</span></span>
</dt> <dd>

<span data-ttu-id="ca374-137">ID de groupe.</span><span class="sxs-lookup"><span data-stu-id="ca374-137">The group id.</span></span>

</dd> <dt>

<span data-ttu-id="ca374-138">**strProfile**</span><span class="sxs-lookup"><span data-stu-id="ca374-138">**strProfile**</span></span>
</dt> <dd>

<span data-ttu-id="ca374-139">Pointeur vers une chaîne se terminant par NULL et décrivant le profil.</span><span class="sxs-lookup"><span data-stu-id="ca374-139">A pointer to a NULL-terminated string describing the profile.</span></span>

</dd> <dt>

<span data-ttu-id="ca374-140">**LocalAddress**</span><span class="sxs-lookup"><span data-stu-id="ca374-140">**LocalAddress**</span></span>
</dt> <dd>

<span data-ttu-id="ca374-141">Adresse locale.</span><span class="sxs-lookup"><span data-stu-id="ca374-141">The local address.</span></span>

</dd> <dt>

<span data-ttu-id="ca374-142">**RemoteAddress**</span><span class="sxs-lookup"><span data-stu-id="ca374-142">**RemoteAddress**</span></span>
</dt> <dd>

<span data-ttu-id="ca374-143">Adresse distante.</span><span class="sxs-lookup"><span data-stu-id="ca374-143">The remote address.</span></span>

</dd> <dt>

<span data-ttu-id="ca374-144">**uRTSPPort**</span><span class="sxs-lookup"><span data-stu-id="ca374-144">**uRTSPPort**</span></span>
</dt> <dd>

<span data-ttu-id="ca374-145">Port RTSP.</span><span class="sxs-lookup"><span data-stu-id="ca374-145">The RTSP port.</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ca374-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ca374-146">Requirements</span></span>



| <span data-ttu-id="ca374-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ca374-147">Requirement</span></span> | <span data-ttu-id="ca374-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="ca374-148">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ca374-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca374-149">Minimum supported client</span></span><br/> | <span data-ttu-id="ca374-150">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ca374-150">Windows 8.1 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ca374-151">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca374-151">Minimum supported server</span></span><br/> | <span data-ttu-id="ca374-152">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ca374-152">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ca374-153">En-tête</span><span class="sxs-lookup"><span data-stu-id="ca374-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca374-154"><dt>Wfdsink. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca374-154"><dt>Wfdsink.h</dt></span></span> </dl> |



 

 




