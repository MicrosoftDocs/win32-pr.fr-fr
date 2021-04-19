---
title: Message WM_ADSPROP_NOTIFY_APPLY (Adsprop. h)
description: Une extension de feuille de propriétés de service de Active Directory Directory envoie le \_ \_ \_ message de notification d’application ADSPROP WM à l’objet de notification si la page de propriétés PSN \_ apply Handler a été établie.
ms.assetid: 3536054b-83ee-4cfa-ab54-c0af3a46289e
ms.tgt_platform: multiple
keywords:
- Message de WM_ADSPROP_NOTIFY_APPLY Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_APPLY
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0ccd5bb95e3f092634d54ba0534e81ded6701bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106543632"
---
# <a name="wm_adsprop_notify_apply-message"></a><span data-ttu-id="df806-104">\_Message d' \_ application de notification WM ADSPROP \_</span><span class="sxs-lookup"><span data-stu-id="df806-104">WM\_ADSPROP\_NOTIFY\_APPLY message</span></span>

<span data-ttu-id="df806-105">Une extension de feuille de propriétés de service de Active Directory Directory envoie le message de notification d' **\_ \_ \_ application ADSPROP WM** à l’objet de notification si la page de propriétés PSN \_ apply Handler a été établie.</span><span class="sxs-lookup"><span data-stu-id="df806-105">An Active Directory directory service property sheet extension sends the **WM\_ADSPROP\_NOTIFY\_APPLY** message to the notification object if the property page PSN\_APPLY handler succeeds.</span></span>


```C++
WM_ADSPROP_NOTIFY_APPLY

    WPARAM wParam
    LPARAM lParam
    
```



## <a name="parameters"></a><span data-ttu-id="df806-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="df806-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df806-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="df806-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="df806-108">Handle de l’objet de notification.</span><span class="sxs-lookup"><span data-stu-id="df806-108">The handle of the notification object.</span></span> <span data-ttu-id="df806-109">Pour obtenir ce handle, appelez [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span><span class="sxs-lookup"><span data-stu-id="df806-109">To obtain this handle, call [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span></span>

</dd> <dt>

<span data-ttu-id="df806-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="df806-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="df806-111">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="df806-111">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="df806-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="df806-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="df806-113">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="df806-113">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df806-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="df806-114">Return value</span></span>

<span data-ttu-id="df806-115">Ce message n’a pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="df806-115">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="df806-116">Notes</span><span class="sxs-lookup"><span data-stu-id="df806-116">Remarks</span></span>

<span data-ttu-id="df806-117">Lorsque vous ajoutez des pages au composant logiciel enfichable MMC Active Directory Manager, Active Directory feuilles de propriétés MMC créent les objets de notification par un appel à la fonction [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj) , puis passe le handle d’objet de notification à chaque page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="df806-117">When adding pages to the Active Directory Manager MMC snap-in, Active Directory MMC property sheets create the notification objects by a call to the [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj) function, and then passes the notification object handle to each property page.</span></span>

## <a name="requirements"></a><span data-ttu-id="df806-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="df806-118">Requirements</span></span>



| <span data-ttu-id="df806-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="df806-119">Requirement</span></span> | <span data-ttu-id="df806-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="df806-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="df806-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df806-121">Minimum supported client</span></span><br/> | <span data-ttu-id="df806-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="df806-122">Windows Vista</span></span><br/>                                                             |
| <span data-ttu-id="df806-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df806-123">Minimum supported server</span></span><br/> | <span data-ttu-id="df806-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="df806-124">Windows Server 2008</span></span><br/>                                                       |
| <span data-ttu-id="df806-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="df806-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="df806-126"><dt>Adsprop. h</dt></span><span class="sxs-lookup"><span data-stu-id="df806-126"><dt>Adsprop.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df806-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df806-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df806-128">**ADsPropCreateNotifyObj**</span><span class="sxs-lookup"><span data-stu-id="df806-128">**ADsPropCreateNotifyObj**</span></span>](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)
</dt> <dt>

[<span data-ttu-id="df806-129">Messages dans Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="df806-129">Messages in Active Directory Domain Services</span></span>](messages-in-active-directory-domain-services.md)
</dt> </dl>

 

 





