---
description: Effectue l’initialisation nécessaire pour permettre à l’application appelante de devenir un récepteur d’affichage Miracast.
ms.assetid: D87B427B-0B7F-44BB-BC34-726FDF87CCCC
title: WFDDisplaySinkStart, fonction (Wfdsink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFDStartDisplaySink
api_type:
- DllExport
api_location:
- wifidisplay.dll
ms.openlocfilehash: 423ca68364fbe7c4beb89ab3b1d9f8e8fdb891be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528156"
---
# <a name="wfddisplaysinkstart-function"></a><span data-ttu-id="c41d1-103">WFDDisplaySinkStart fonction)</span><span class="sxs-lookup"><span data-stu-id="c41d1-103">WFDDisplaySinkStart function</span></span>

<span data-ttu-id="c41d1-104">Effectue l’initialisation nécessaire pour permettre à l’application appelante de devenir un récepteur d’affichage Miracast.</span><span class="sxs-lookup"><span data-stu-id="c41d1-104">Performs the necessary initialization to allow the calling app to become a Miracast display sink.</span></span> <span data-ttu-id="c41d1-105">Votre application doit l’appeler une fois au démarrage.</span><span class="sxs-lookup"><span data-stu-id="c41d1-105">Your app should call this once on startup.</span></span>

## <a name="syntax"></a><span data-ttu-id="c41d1-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c41d1-106">Syntax</span></span>


```C++
DWORD WINAPI WFDStartDisplaySink(
  _In_     USHORT                                 uDeviceCategory,
  _In_     USHORT                                 uSubCategory,
  _In_opt_ PVOID                                  pCallbackContext,
  _In_     WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK *pfnCallback
);
```



## <a name="parameters"></a><span data-ttu-id="c41d1-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c41d1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c41d1-108">*uDeviceCategory* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c41d1-108">*uDeviceCategory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c41d1-109">Catégorie de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c41d1-109">The device category.</span></span>

</dd> <dt>

<span data-ttu-id="c41d1-110">*uSubCategory* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c41d1-110">*uSubCategory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c41d1-111">Sous-catégorie d’appareil.</span><span class="sxs-lookup"><span data-stu-id="c41d1-111">The device subcategory.</span></span>

</dd> <dt>

<span data-ttu-id="c41d1-112">*pCallbackContext* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="c41d1-112">*pCallbackContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c41d1-113">Pointeur de contexte facultatif qui est passé à la fonction de rappel spécifiée dans le paramètre *pfnCallback* .</span><span class="sxs-lookup"><span data-stu-id="c41d1-113">An optional context pointer which is passed to the callback function specified in the *pfnCallback* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="c41d1-114">*pfnCallback* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c41d1-114">*pfnCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c41d1-115">Pointeur vers la fonction de rappel à appeler à chaque fois qu’une notification est envoyée à l’application.</span><span class="sxs-lookup"><span data-stu-id="c41d1-115">A pointer to the callback function to be called whenever there is a notification for the app.</span></span> <span data-ttu-id="c41d1-116">Les notifications qui peuvent être envoyées sont décrites dans le [**rappel de notification du \_ récepteur d’affichage \_ \_ \_ WFD**](wfd-display-sink-notification-callback.md).</span><span class="sxs-lookup"><span data-stu-id="c41d1-116">Notifications that can be sent are described in [**WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK**](wfd-display-sink-notification-callback.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c41d1-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c41d1-117">Return value</span></span>

<span data-ttu-id="c41d1-118">Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.</span><span class="sxs-lookup"><span data-stu-id="c41d1-118">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="c41d1-119">Si la fonction échoue, la valeur de retour peut être l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="c41d1-119">If the function fails, the return value may be one of the following return codes.</span></span>



| <span data-ttu-id="c41d1-120">Code de retour</span><span class="sxs-lookup"><span data-stu-id="c41d1-120">Return code</span></span>                                                                                          | <span data-ttu-id="c41d1-121">Description</span><span class="sxs-lookup"><span data-stu-id="c41d1-121">Description</span></span>                                                    |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="c41d1-122"><dt>**ERREUR \_ non \_ prise en charge**</dt></span><span class="sxs-lookup"><span data-stu-id="c41d1-122"><dt>**ERROR\_NOT\_SUPPORTED**</dt></span></span> </dl> | <span data-ttu-id="c41d1-123">Le récepteur d’affichage n’est pas pris en charge sur ce matériel.</span><span class="sxs-lookup"><span data-stu-id="c41d1-123">The display sink is not supported on this hardware.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c41d1-124">Notes</span><span class="sxs-lookup"><span data-stu-id="c41d1-124">Remarks</span></span>

<span data-ttu-id="c41d1-125">Cette fonction effectue les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="c41d1-125">This function performs the following tasks:</span></span>

-   <span data-ttu-id="c41d1-126">Rend le PC détectable</span><span class="sxs-lookup"><span data-stu-id="c41d1-126">Makes the PC discoverable</span></span>
-   <span data-ttu-id="c41d1-127">Définit les informations de l’appareil P2P pour refléter la catégorie et la sous-catégorie spécifiées</span><span class="sxs-lookup"><span data-stu-id="c41d1-127">Sets the P2P device info to reflect the category and sub category specified</span></span>
-   <span data-ttu-id="c41d1-128">Définit Miracast IEs sur tous les Wi-Fi frames directs avec le type d’appareil en tant que récepteur</span><span class="sxs-lookup"><span data-stu-id="c41d1-128">Sets the Miracast IEs on all Wi-Fi Direct frames with the device type as the sink</span></span>
-   <span data-ttu-id="c41d1-129">Inscrit le rappel spécifié à appeler à chaque fois qu’il existe une connexion entrante.</span><span class="sxs-lookup"><span data-stu-id="c41d1-129">Registers the specified callback to be invoked whenever there is an incoming connection</span></span>

## <a name="requirements"></a><span data-ttu-id="c41d1-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c41d1-130">Requirements</span></span>



| <span data-ttu-id="c41d1-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c41d1-131">Requirement</span></span> | <span data-ttu-id="c41d1-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="c41d1-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="c41d1-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c41d1-133">Minimum supported client</span></span><br/> | <span data-ttu-id="c41d1-134">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c41d1-134">Windows 8.1 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c41d1-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c41d1-135">Minimum supported server</span></span><br/> | <span data-ttu-id="c41d1-136">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c41d1-136">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c41d1-137">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="c41d1-137">End of client support</span></span><br/>    | <span data-ttu-id="c41d1-138">Windows 10</span><span class="sxs-lookup"><span data-stu-id="c41d1-138">Windows 10</span></span><br/>                                                                      |
| <span data-ttu-id="c41d1-139">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="c41d1-139">End of server support</span></span><br/>    | <span data-ttu-id="c41d1-140">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="c41d1-140">Windows Server 2016</span></span><br/>                                                             |
| <span data-ttu-id="c41d1-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="c41d1-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="c41d1-142"><dt>Wfdsink. h</dt></span><span class="sxs-lookup"><span data-stu-id="c41d1-142"><dt>Wfdsink.h</dt></span></span> </dl>       |
| <span data-ttu-id="c41d1-143">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c41d1-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="c41d1-144"><dt>Wifidisplay. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c41d1-144"><dt>Wifidisplay.lib</dt></span></span> </dl> |
| <span data-ttu-id="c41d1-145">DLL</span><span class="sxs-lookup"><span data-stu-id="c41d1-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c41d1-146"><dt>Wifidisplay.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c41d1-146"><dt>Wifidisplay.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c41d1-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c41d1-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c41d1-148">**\_rappel de \_ notification du récepteur d’affichage WFD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c41d1-148">**WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK**</span></span>](wfd-display-sink-notification-callback.md)
</dt> </dl>

 

 




