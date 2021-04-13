---
description: Nettoie l’état de la session en cours d’ouverture, ou la session actuellement ouverte.
ms.assetid: 8247AFA9-F471-4CCD-972D-D0C827E86880
title: WFDDisplaySinkCloseSession, fonction (Wfdsink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFDCloseDisplaySinkSession
api_type:
- DllExport
api_location:
- wifidisplay.dll
ms.openlocfilehash: 7697bc7ff1aa42569cf954b3f0b037f66ec67ded
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528161"
---
# <a name="wfddisplaysinkclosesession-function"></a><span data-ttu-id="efb7f-103">WFDDisplaySinkCloseSession fonction)</span><span class="sxs-lookup"><span data-stu-id="efb7f-103">WFDDisplaySinkCloseSession function</span></span>

<span data-ttu-id="efb7f-104">Nettoie l’état de la session en cours d’ouverture, ou la session actuellement ouverte.</span><span class="sxs-lookup"><span data-stu-id="efb7f-104">Cleans up the state for the session being opened, or the currently open session.</span></span>

## <a name="syntax"></a><span data-ttu-id="efb7f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="efb7f-105">Syntax</span></span>


```C++
DWORD WINAPI WFDCloseDisplaySinkSession(
  _In_ HANDLE hSessionHandle
);
```



## <a name="parameters"></a><span data-ttu-id="efb7f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="efb7f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efb7f-107">*hSessionHandle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="efb7f-107">*hSessionHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efb7f-108">Le descripteur reçu via l’appel de [**rappel de notification du \_ récepteur d’affichage \_ \_ \_ WFD**](wfd-display-sink-notification-callback.md) le plus récent qui en comprenait un.</span><span class="sxs-lookup"><span data-stu-id="efb7f-108">The handle received via the most recent [**WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK**](wfd-display-sink-notification-callback.md) invocation that included one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efb7f-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="efb7f-109">Return value</span></span>

<span data-ttu-id="efb7f-110">Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.</span><span class="sxs-lookup"><span data-stu-id="efb7f-110">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

## <a name="remarks"></a><span data-ttu-id="efb7f-111">Notes</span><span class="sxs-lookup"><span data-stu-id="efb7f-111">Remarks</span></span>

<span data-ttu-id="efb7f-112">Votre application peut appeler cette fonction pour mettre fin à la session Miracast pour une raison quelconque.</span><span class="sxs-lookup"><span data-stu-id="efb7f-112">Your app can call this function to terminate the Miracast session for any reason.</span></span> <span data-ttu-id="efb7f-113">Votre application n’est pas obligée de l’appeler quand elle reçoit le type **DisconnectedNotification** dans son rappel.</span><span class="sxs-lookup"><span data-stu-id="efb7f-113">Your app is not required to call it when it receives the **DisconnectedNotification** type in its callback.</span></span>

## <a name="requirements"></a><span data-ttu-id="efb7f-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="efb7f-114">Requirements</span></span>



| <span data-ttu-id="efb7f-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="efb7f-115">Requirement</span></span> | <span data-ttu-id="efb7f-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="efb7f-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="efb7f-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="efb7f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="efb7f-118">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="efb7f-118">Windows 8.1 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="efb7f-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="efb7f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="efb7f-120">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="efb7f-120">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="efb7f-121">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="efb7f-121">End of client support</span></span><br/>    | <span data-ttu-id="efb7f-122">Windows 10</span><span class="sxs-lookup"><span data-stu-id="efb7f-122">Windows 10</span></span><br/>                                                                      |
| <span data-ttu-id="efb7f-123">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="efb7f-123">End of server support</span></span><br/>    | <span data-ttu-id="efb7f-124">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="efb7f-124">Windows Server 2016</span></span><br/>                                                             |
| <span data-ttu-id="efb7f-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="efb7f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="efb7f-126"><dt>Wfdsink. h</dt></span><span class="sxs-lookup"><span data-stu-id="efb7f-126"><dt>Wfdsink.h</dt></span></span> </dl>       |
| <span data-ttu-id="efb7f-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="efb7f-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="efb7f-128"><dt>Wifidisplay. lib</dt></span><span class="sxs-lookup"><span data-stu-id="efb7f-128"><dt>Wifidisplay.lib</dt></span></span> </dl> |
| <span data-ttu-id="efb7f-129">DLL</span><span class="sxs-lookup"><span data-stu-id="efb7f-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="efb7f-130"><dt>Wifidisplay.dll</dt></span><span class="sxs-lookup"><span data-stu-id="efb7f-130"><dt>Wifidisplay.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efb7f-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="efb7f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efb7f-132">**\_rappel de \_ notification du récepteur d’affichage WFD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="efb7f-132">**WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK**</span></span>](wfd-display-sink-notification-callback.md)
</dt> </dl>

 

 




