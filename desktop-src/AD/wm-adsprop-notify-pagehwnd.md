---
title: Message WM_ADSPROP_NOTIFY_PAGEHWND (Adsprop. h)
description: Une extension de feuille de propriétés de service d’annuaire Active Directory appelle ADsPropSetHwnd pour informer l’objet de notification du handle de fenêtre de la page de propriétés.
ms.assetid: eb8bf525-cd7f-44d0-a0f9-43178a29c443
ms.tgt_platform: multiple
keywords:
- Message de WM_ADSPROP_NOTIFY_PAGEHWND Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_PAGEHWND
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d74ef2db993d2a3daf10f69687b8f3525ef80a87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105616"
---
# <a name="wm_adsprop_notify_pagehwnd-message"></a><span data-ttu-id="60ac6-104">\_Message WM ADSPROP \_ Notify \_ PAGEHWND</span><span class="sxs-lookup"><span data-stu-id="60ac6-104">WM\_ADSPROP\_NOTIFY\_PAGEHWND message</span></span>

<span data-ttu-id="60ac6-105">Une extension de feuille de propriétés de service d’annuaire Active Directory appelle [**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd) pour informer l’objet de notification du handle de fenêtre de la page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="60ac6-105">An Active Directory directory service property sheet extension calls the [**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd) to inform the notification object of the property page window handle.</span></span> <span data-ttu-id="60ac6-106">La fonction **ADsPropSetHwnd** envoie le message **WM \_ ADSPROP \_ Notify \_ PAGEHWND** à l’objet de notification, qui informe l’objet de notification du handle de fenêtre de la page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="60ac6-106">The **ADsPropSetHwnd** function sends the **WM\_ADSPROP\_NOTIFY\_PAGEHWND** message to the notification object, which informs the notification object of the property page window handle.</span></span>


```C++
WM_ADSPROP_NOTIFY_PAGEHWND

    WPARAM hPage
    LPARAM ptzTitle
    
```



## <a name="parameters"></a><span data-ttu-id="60ac6-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="60ac6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60ac6-108">*hNotifyObj*</span><span class="sxs-lookup"><span data-stu-id="60ac6-108">*hNotifyObj*</span></span> 
</dt> <dd>

<span data-ttu-id="60ac6-109">Handle de l’objet de notification.</span><span class="sxs-lookup"><span data-stu-id="60ac6-109">The handle of the notification object.</span></span> <span data-ttu-id="60ac6-110">Pour obtenir ce handle, appelez [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span><span class="sxs-lookup"><span data-stu-id="60ac6-110">To obtain this handle, call [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span></span>

</dd> <dt>

<span data-ttu-id="60ac6-111">*hPage*</span><span class="sxs-lookup"><span data-stu-id="60ac6-111">*hPage*</span></span> 
</dt> <dd>

<span data-ttu-id="60ac6-112">Handle de fenêtre de la page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="60ac6-112">A window handle of the property page.</span></span>

</dd> <dt>

<span data-ttu-id="60ac6-113">*ptzTitle*</span><span class="sxs-lookup"><span data-stu-id="60ac6-113">*ptzTitle*</span></span> 
</dt> <dd>

<span data-ttu-id="60ac6-114">Pointeur vers une mémoire tampon **WCHAR** se terminant par un caractère null qui contient le titre de la page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="60ac6-114">Pointer to a NULL-terminated **WCHAR** buffer that contains the title of the property page.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60ac6-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="60ac6-115">Return value</span></span>

<span data-ttu-id="60ac6-116">Ce message n’a pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="60ac6-116">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="60ac6-117">Notes</span><span class="sxs-lookup"><span data-stu-id="60ac6-117">Remarks</span></span>

<span data-ttu-id="60ac6-118">Une Active Directory extension de la feuille de propriétés appelle normalement la fonction [**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd) lors du traitement du message [**WM \_ INITDIALOG**](../dlgbox/wm-initdialog.md) .</span><span class="sxs-lookup"><span data-stu-id="60ac6-118">An Active Directory property sheet extension normally calls the [**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd) function while processing the [**WM\_INITDIALOG**](../dlgbox/wm-initdialog.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="60ac6-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="60ac6-119">Requirements</span></span>



| <span data-ttu-id="60ac6-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="60ac6-120">Requirement</span></span> | <span data-ttu-id="60ac6-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="60ac6-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="60ac6-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="60ac6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="60ac6-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="60ac6-123">Windows Vista</span></span><br/>                                                             |
| <span data-ttu-id="60ac6-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="60ac6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="60ac6-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="60ac6-125">Windows Server 2008</span></span><br/>                                                       |
| <span data-ttu-id="60ac6-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="60ac6-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="60ac6-127"><dt>Adsprop. h</dt></span><span class="sxs-lookup"><span data-stu-id="60ac6-127"><dt>Adsprop.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60ac6-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60ac6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60ac6-129">Messages dans Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="60ac6-129">Messages in Active Directory Domain Services</span></span>](messages-in-active-directory-domain-services.md)
</dt> <dt>

[<span data-ttu-id="60ac6-130">**ADsPropSetHwnd**</span><span class="sxs-lookup"><span data-stu-id="60ac6-130">**ADsPropSetHwnd**</span></span>](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd)
</dt> <dt>

[<span data-ttu-id="60ac6-131">**ADsPropCreateNotifyObj**</span><span class="sxs-lookup"><span data-stu-id="60ac6-131">**ADsPropCreateNotifyObj**</span></span>](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)
</dt> <dt>

[<span data-ttu-id="60ac6-132">**\_INITDIALOG WM**</span><span class="sxs-lookup"><span data-stu-id="60ac6-132">**WM\_INITDIALOG**</span></span>](../dlgbox/wm-initdialog.md)
</dt> </dl>

 

