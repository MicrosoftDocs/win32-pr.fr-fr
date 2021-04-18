---
description: Définit la fonction de rappel&\# 8212 ; que vous implémentez dans votre application&\# 8212 ; qui a été spécifié pour la fonction WFDStartDisplaySink.
ms.assetid: 0D4C00FD-4ED6-4F0F-BB72-0A1FCC05DB37
title: WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK fonction de rappel (Wfdsink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK
api_type:
- UserDefined
api_location:
- wfdsink.h
ms.openlocfilehash: c576f88a5b7f97484647c4c06f44522a5c3c379f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529162"
---
# <a name="wfd_display_sink_notification_callback-callback-function"></a><span data-ttu-id="fd345-103">\_Fonction de \_ rappel de rappel de \_ notification du récepteur d’affichage WFD \_</span><span class="sxs-lookup"><span data-stu-id="fd345-103">WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK callback function</span></span>

<span data-ttu-id="fd345-104">La fonction de **rappel de notification du \_ récepteur d’affichage \_ \_ \_ WFD** définit la fonction de rappel, que vous implémentez dans votre application, qui a été spécifiée pour la fonction [**WFDStartDisplaySink**](wfdstartdisplaysink.md) .</span><span class="sxs-lookup"><span data-stu-id="fd345-104">The **WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK** function defines the callback function—which you implement in your app—that was specified to the [**WFDStartDisplaySink**](wfdstartdisplaysink.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd345-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fd345-105">Syntax</span></span>


```C++
DWORD CALLBACK WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK(
  _In_opt_          PVOID                                 pvContext,
  _In_        const PWFD_DISPLAY_SINK_NOTIFICATION        pNotification,
  _Inout_opt_       PWFD_DISPLAY_SINK_NOTIFICATION_RESULT pNotificationResult
);
```



## <a name="parameters"></a><span data-ttu-id="fd345-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fd345-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd345-107">*pvContext* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="fd345-107">*pvContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fd345-108">Pointeur de contexte facultatif passé à la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="fd345-108">An optional context pointer passed to the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="fd345-109">*pNotification* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fd345-109">*pNotification* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd345-110">Pointeur vers un struct contenant les données relatives à la notification du récepteur d’affichage.</span><span class="sxs-lookup"><span data-stu-id="fd345-110">A pointer to a struct containing data about the display sink notification.</span></span>

</dd> <dt>

<span data-ttu-id="fd345-111">*pNotificationResult* \[ in, out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="fd345-111">*pNotificationResult* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fd345-112">Pointeur vers un struct contenant les données que votre application peut éventuellement définir pour indiquer le résultat du traitement de la notification du récepteur d’affichage.</span><span class="sxs-lookup"><span data-stu-id="fd345-112">A pointer to a struct containing data that your app can optionally set to indicate the result of processing the display sink notification.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fd345-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fd345-113">Requirements</span></span>



| <span data-ttu-id="fd345-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fd345-114">Requirement</span></span> | <span data-ttu-id="fd345-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd345-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fd345-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd345-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fd345-117">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fd345-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="fd345-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd345-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fd345-119">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fd345-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="fd345-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="fd345-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd345-121"><dt>Wfdsink. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd345-121"><dt>Wfdsink.h</dt></span></span> </dl> |



 

 




