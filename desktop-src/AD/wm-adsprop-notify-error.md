---
title: Message WM_ADSPROP_NOTIFY_ERROR (Adsprop. h)
description: Le \_ \_ \_ message d’erreur WM ADSPROP Notify ajoute un message d’erreur à la liste des messages d’erreur affichés en appelant la fonction ADsPropShowErrorDialog.
ms.assetid: 7abf1b3d-5abe-42cd-baeb-1bf863c7f04d
ms.tgt_platform: multiple
keywords:
- Message de WM_ADSPROP_NOTIFY_ERROR Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_ERROR
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9cdcb33c5536cfa67ab136daa5aa56d93f1d706
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103792"
---
# <a name="wm_adsprop_notify_error-message"></a><span data-ttu-id="53fd2-104">\_Message d' \_ erreur de notification WM ADSPROP \_</span><span class="sxs-lookup"><span data-stu-id="53fd2-104">WM\_ADSPROP\_NOTIFY\_ERROR message</span></span>

<span data-ttu-id="53fd2-105">Le message d' **\_ \_ \_ erreur WM ADSPROP Notify** ajoute un message d’erreur à la liste des messages d’erreur affichés en appelant la fonction [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) .</span><span class="sxs-lookup"><span data-stu-id="53fd2-105">The **WM\_ADSPROP\_NOTIFY\_ERROR** message adds an error message to a list of error messages that are displayed by calling the [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) function.</span></span>


```C++
WM_ADSPROP_NOTIFY_ERROR

    WPARAM wParam
    LPARAM lParam
    
```



## <a name="parameters"></a><span data-ttu-id="53fd2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="53fd2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53fd2-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="53fd2-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="53fd2-108">Handle de l’objet de notification.</span><span class="sxs-lookup"><span data-stu-id="53fd2-108">Handle of the notification object.</span></span> <span data-ttu-id="53fd2-109">Il s’agit du paramètre *hNotifyObject* obtenu par [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span><span class="sxs-lookup"><span data-stu-id="53fd2-109">This is the *hNotifyObject* parameter obtained by [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span></span>

</dd> <dt>

<span data-ttu-id="53fd2-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="53fd2-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="53fd2-111">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="53fd2-111">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="53fd2-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="53fd2-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="53fd2-113">Pointeur vers une structure [**ADSPROPERROR**](/windows/desktop/api/Adsprop/ns-adsprop-adsproperror) qui contient les données de message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="53fd2-113">Pointer to an [**ADSPROPERROR**](/windows/desktop/api/Adsprop/ns-adsprop-adsproperror) structure that contains error message data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53fd2-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="53fd2-114">Return value</span></span>

<span data-ttu-id="53fd2-115">Ce message n’a pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="53fd2-115">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="53fd2-116">Notes</span><span class="sxs-lookup"><span data-stu-id="53fd2-116">Remarks</span></span>

<span data-ttu-id="53fd2-117">La fonction [**ADsPropSendErrorMessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) est la méthode recommandée pour envoyer ce message.</span><span class="sxs-lookup"><span data-stu-id="53fd2-117">The [**ADsPropSendErrorMessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) function is the preferred method of sending this message.</span></span>

<span data-ttu-id="53fd2-118">Les messages d’erreur ajoutés par le message d' **\_ \_ \_ erreur de notification WM ADSPROP** sont accumulés jusqu’à ce que [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) soit appelé.</span><span class="sxs-lookup"><span data-stu-id="53fd2-118">The error messages added by the **WM\_ADSPROP\_NOTIFY\_ERROR** message are accumulated until [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) is called.</span></span> <span data-ttu-id="53fd2-119">**ADsPropShowErrorDialog** combine et affiche les messages d’erreur accumulés.</span><span class="sxs-lookup"><span data-stu-id="53fd2-119">**ADsPropShowErrorDialog** combines and displays the accumulated error messages.</span></span> <span data-ttu-id="53fd2-120">Quand la boîte de dialogue d’erreur est fermée, les messages d’erreur accumulés sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="53fd2-120">When the error dialog is dismissed, the accumulated error messages are deleted.</span></span>

## <a name="requirements"></a><span data-ttu-id="53fd2-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="53fd2-121">Requirements</span></span>



| <span data-ttu-id="53fd2-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="53fd2-122">Requirement</span></span> | <span data-ttu-id="53fd2-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="53fd2-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="53fd2-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53fd2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="53fd2-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="53fd2-125">Windows Vista</span></span><br/>                                                             |
| <span data-ttu-id="53fd2-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53fd2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="53fd2-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="53fd2-127">Windows Server 2008</span></span><br/>                                                       |
| <span data-ttu-id="53fd2-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="53fd2-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="53fd2-129"><dt>Adsprop. h</dt></span><span class="sxs-lookup"><span data-stu-id="53fd2-129"><dt>Adsprop.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53fd2-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53fd2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53fd2-131">Messages dans Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="53fd2-131">Messages in Active Directory Domain Services</span></span>](messages-in-active-directory-domain-services.md)
</dt> <dt>

[<span data-ttu-id="53fd2-132">**ADSPROPERROR**</span><span class="sxs-lookup"><span data-stu-id="53fd2-132">**ADSPROPERROR**</span></span>](/windows/desktop/api/Adsprop/ns-adsprop-adsproperror)
</dt> <dt>

[<span data-ttu-id="53fd2-133">**ADsPropSendErrorMessage**</span><span class="sxs-lookup"><span data-stu-id="53fd2-133">**ADsPropSendErrorMessage**</span></span>](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage)
</dt> <dt>

[<span data-ttu-id="53fd2-134">**ADsPropShowErrorDialog**</span><span class="sxs-lookup"><span data-stu-id="53fd2-134">**ADsPropShowErrorDialog**</span></span>](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog)
</dt> </dl>

 

 





