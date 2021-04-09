---
title: Message WM_ADSPROP_NOTIFY_EXIT (Adsprop. h)
description: Une extension de feuille de propriétés Active Directory envoie \_ le \_ \_ message de sortie de notification WM ADSPROP à l’objet de notification lorsque l’objet de notification n’est plus nécessaire.
ms.assetid: b0f58c73-8953-412d-b801-bf34967fe0b4
ms.tgt_platform: multiple
keywords:
- Message de WM_ADSPROP_NOTIFY_EXIT Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_EXIT
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32d74ef4b7dfa525cfb77a6d89499837cbfac8f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942672"
---
# <a name="wm_adsprop_notify_exit-message"></a><span data-ttu-id="d66b7-104">\_Message de \_ sortie de notification WM ADSPROP \_</span><span class="sxs-lookup"><span data-stu-id="d66b7-104">WM\_ADSPROP\_NOTIFY\_EXIT message</span></span>

<span data-ttu-id="d66b7-105">Une extension de feuille de propriétés Active Directory envoie le message de **\_ \_ \_ sortie de notification WM ADSPROP** à l’objet de notification lorsque l’objet de notification n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="d66b7-105">An Active Directory property sheet extension sends the **WM\_ADSPROP\_NOTIFY\_EXIT** message to the notification object when the notification object is no longer required.</span></span>


```C++
WM_ADSPROP_NOTIFY_EXIT

    WPARAM wParam
    LPARAM lParam
    
```



## <a name="parameters"></a><span data-ttu-id="d66b7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d66b7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d66b7-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="d66b7-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="d66b7-108">Handle de l’objet de notification.</span><span class="sxs-lookup"><span data-stu-id="d66b7-108">The handle of the notification object.</span></span> <span data-ttu-id="d66b7-109">Pour obtenir ce handle, appelez [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span><span class="sxs-lookup"><span data-stu-id="d66b7-109">To obtain this handle, call [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span></span>

</dd> <dt>

<span data-ttu-id="d66b7-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d66b7-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d66b7-111">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="d66b7-111">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="d66b7-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d66b7-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d66b7-113">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="d66b7-113">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d66b7-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d66b7-114">Return value</span></span>

<span data-ttu-id="d66b7-115">Ce message n’a pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="d66b7-115">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d66b7-116">Notes</span><span class="sxs-lookup"><span data-stu-id="d66b7-116">Remarks</span></span>

<span data-ttu-id="d66b7-117">L’objet de notification se supprime lui-même en réponse à ce message.</span><span class="sxs-lookup"><span data-stu-id="d66b7-117">The notification object will delete itself in response to this message.</span></span> <span data-ttu-id="d66b7-118">Lorsque ce message a été envoyé, le descripteur d’objet de notification doit être considéré comme non valide.</span><span class="sxs-lookup"><span data-stu-id="d66b7-118">When this message has been sent, the notification object handle should be considered invalid.</span></span>

## <a name="requirements"></a><span data-ttu-id="d66b7-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d66b7-119">Requirements</span></span>



| <span data-ttu-id="d66b7-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d66b7-120">Requirement</span></span> | <span data-ttu-id="d66b7-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="d66b7-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d66b7-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d66b7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d66b7-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d66b7-123">Windows Vista</span></span><br/>                                                             |
| <span data-ttu-id="d66b7-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d66b7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d66b7-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d66b7-125">Windows Server 2008</span></span><br/>                                                       |
| <span data-ttu-id="d66b7-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="d66b7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d66b7-127"><dt>Adsprop. h</dt></span><span class="sxs-lookup"><span data-stu-id="d66b7-127"><dt>Adsprop.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d66b7-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d66b7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d66b7-129">**ADsPropCreateNotifyObj**</span><span class="sxs-lookup"><span data-stu-id="d66b7-129">**ADsPropCreateNotifyObj**</span></span>](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)
</dt> <dt>

[<span data-ttu-id="d66b7-130">Messages dans Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="d66b7-130">Messages in Active Directory Domain Services</span></span>](messages-in-active-directory-domain-services.md)
</dt> </dl>

 

 





