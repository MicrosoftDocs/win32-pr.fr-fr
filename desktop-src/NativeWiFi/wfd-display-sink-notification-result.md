---
description: Décrit le résultat que vous pouvez éventuellement définir après le traitement d’un récepteur d’affichage notification par dans la \_ fonction de rappel de notification du récepteur d’affichage WFD \_ \_ \_ .
ms.assetid: 6ED04294-2ED9-455B-9274-8C3DB06D4B21
title: Structure WFD_DISPLAY_SINK_NOTIFICATION_RESULT (Wfdsink. h)
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
ms.openlocfilehash: dc23416d4d13284862aea652dd71909e71879afc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534760"
---
# <a name="wfd_display_sink_notification_result-structure"></a><span data-ttu-id="c5268-103">Structure du résultat de la notification du récepteur d' \_ affichage WFD \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="c5268-103">WFD\_DISPLAY\_SINK\_NOTIFICATION\_RESULT structure</span></span>

<span data-ttu-id="c5268-104">La structure du résultat de la **\_ notification du récepteur d’affichage \_ \_ \_ WFD** décrit le résultat que vous pouvez éventuellement définir après le traitement d’un récepteur d’affichage notification par dans la fonction de [**rappel de notification du \_ récepteur d’affichage \_ \_ \_ WFD**](wfd-display-sink-notification-callback.md) .</span><span class="sxs-lookup"><span data-stu-id="c5268-104">The **WFD\_DISPLAY\_SINK\_NOTIFICATION\_RESULT** structure describes the result that you can optionally set after processing a display sink notfication in the [**WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK**](wfd-display-sink-notification-callback.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5268-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c5268-105">Syntax</span></span>


```C++
typedef struct _WFD_DISPLAY_SINK_NOTIFICATION {
  WFD_DISPLAY_SINK_OBJECT_HEADER     Header;
  WFD_DISPLAY_SINK_NOTIFICATION_TYPE type;
  union {
    struct {
      DOT11_WPS_CONFIG_METHOD ConfigMethod;
      UINT32                  uPassKeyLength;
      WCHAR                   Passkey[WFD_SINK_WPS_INFO_MAX_PASSKEY_LENGTH];
    } ProvisioningData;
    struct {
      PWSTR strProfile;
    } ReconnectData;
  };
} WFD_DISPLAY_SINK_NOTIFICATION, *PWFD_DISPLAY_SINK_NOTIFICATION;
```



## <a name="members"></a><span data-ttu-id="c5268-106">Membres</span><span class="sxs-lookup"><span data-stu-id="c5268-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c5268-107">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="c5268-107">**Header**</span></span>
</dt> <dd>

<span data-ttu-id="c5268-108">[**\_ \_ \_ \_ En-tête d’objet récepteur WFD**](wfd-display-sink-object-header.md) qui décrit les données incluses dans le résultat de la notification.</span><span class="sxs-lookup"><span data-stu-id="c5268-108">A [**WFD\_DISPLAY\_SINK\_OBJECT\_HEADER**](wfd-display-sink-object-header.md) that describes the data included in the notification result.</span></span>

</dd> <dt>

<span data-ttu-id="c5268-109">**type**</span><span class="sxs-lookup"><span data-stu-id="c5268-109">**type**</span></span>
</dt> <dd>

<span data-ttu-id="c5268-110">Valeur [**du \_ \_ type de \_ notification \_ du récepteur d’affichage WFD**](wfd-display-sink-notification-type.md) qui indique le type du résultat de la notification.</span><span class="sxs-lookup"><span data-stu-id="c5268-110">A [**WFD\_DISPLAY\_SINK\_NOTIFICATION\_TYPE**](wfd-display-sink-notification-type.md) value that indicates the type of the notification result.</span></span> <span data-ttu-id="c5268-111">Ce paramètre détermine également les informations à utiliser dans l’Union ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="c5268-111">This parameter also determines which Info to use in the union below.</span></span>

</dd> <dt>

<span data-ttu-id="c5268-112">**ProvisioningData**</span><span class="sxs-lookup"><span data-stu-id="c5268-112">**ProvisioningData**</span></span>
</dt> <dd>

<span data-ttu-id="c5268-113">Informations sur le résultat d’une demande d’approvisionnement.</span><span class="sxs-lookup"><span data-stu-id="c5268-113">Info about the result of a provisioning request.</span></span> <span data-ttu-id="c5268-114">Utilisez cette valeur si le *type* a la valeur **ProvisioningRequestNotification**.</span><span class="sxs-lookup"><span data-stu-id="c5268-114">Use this if *type* has the value **ProvisioningRequestNotification**.</span></span>

<dl> <dt>

<span data-ttu-id="c5268-115">**ConfigMethod**</span><span class="sxs-lookup"><span data-stu-id="c5268-115">**ConfigMethod**</span></span>
</dt> <dd>

<span data-ttu-id="c5268-116">Méthode pour l’indication de l’interface utilisateur pour l’acceptation interactive.</span><span class="sxs-lookup"><span data-stu-id="c5268-116">The method for showing UI for interactive acceptance.</span></span>

</dd> <dt>

<span data-ttu-id="c5268-117">**uPassKeyLength**</span><span class="sxs-lookup"><span data-stu-id="c5268-117">**uPassKeyLength**</span></span>
</dt> <dd>

<span data-ttu-id="c5268-118">Nombre de caractères larges dans la *clé de clé*, sans compter les terminateurs null.</span><span class="sxs-lookup"><span data-stu-id="c5268-118">The number of wide characters in *Passkey*, not counting any NULL-terminator.</span></span>

</dd> <dt>

<span data-ttu-id="c5268-119">**Partout**</span><span class="sxs-lookup"><span data-stu-id="c5268-119">**Passkey**</span></span>
</dt> <dd>

<span data-ttu-id="c5268-120">Contient la clé de passe sous la forme d’un tableau de caractères larges.</span><span class="sxs-lookup"><span data-stu-id="c5268-120">Contains the pass key as an array of wide characters.</span></span> <span data-ttu-id="c5268-121">\_ \_ \_ \_ \_ La longueur maximale de la clé de clé du récepteur WFD \_ est définie sur la valeur (8).</span><span class="sxs-lookup"><span data-stu-id="c5268-121">WFD\_SINK\_WPS\_INFO\_MAX\_PASSKEY\_LENGTH is defined as the value (8).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="c5268-122">**ReconnectData**</span><span class="sxs-lookup"><span data-stu-id="c5268-122">**ReconnectData**</span></span>
</dt> <dd>

<span data-ttu-id="c5268-123">Informations sur le résultat d’une demande de reconnexion.</span><span class="sxs-lookup"><span data-stu-id="c5268-123">Info about the result of a reconnect request.</span></span> <span data-ttu-id="c5268-124">Utilisez cette valeur si le *type* a la valeur **ReconnectRequestNotification**.</span><span class="sxs-lookup"><span data-stu-id="c5268-124">Use this if *type* has the value **ReconnectRequestNotification**.</span></span>

<dl> <dt>

<span data-ttu-id="c5268-125">**strProfile**</span><span class="sxs-lookup"><span data-stu-id="c5268-125">**strProfile**</span></span>
</dt> <dd>

<span data-ttu-id="c5268-126">Pointeur vers une chaîne se terminant par NULL et décrivant le profil.</span><span class="sxs-lookup"><span data-stu-id="c5268-126">A pointer to a NULL-terminated string describing the profile.</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c5268-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c5268-127">Requirements</span></span>



| <span data-ttu-id="c5268-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c5268-128">Requirement</span></span> | <span data-ttu-id="c5268-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5268-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c5268-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c5268-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c5268-131">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c5268-131">Windows 8.1 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c5268-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c5268-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c5268-133">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c5268-133">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c5268-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="c5268-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5268-135"><dt>Wfdsink. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5268-135"><dt>Wfdsink.h</dt></span></span> </dl> |



 

 




