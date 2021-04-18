---
title: Message WM_ADSPROP_NOTIFY_PAGEINIT (Adsprop. h)
description: Une Active Directory extension de la feuille de propriétés appelle le ADsPropGetInitInfo pour obtenir des informations sur l’objet d’annuaire auquel s’applique l’extension de la feuille de propriétés.
ms.assetid: 473c5a75-d0d9-4d12-b855-63683e8cdf3f
ms.tgt_platform: multiple
keywords:
- Message de WM_ADSPROP_NOTIFY_PAGEINIT Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_PAGEINIT
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2718ee30cdbecec7c4e0954636aa14c75f13027
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508457"
---
# <a name="wm_adsprop_notify_pageinit-message"></a><span data-ttu-id="755c8-104">\_Message WM ADSPROP \_ Notify \_ PAGEINIT</span><span class="sxs-lookup"><span data-stu-id="755c8-104">WM\_ADSPROP\_NOTIFY\_PAGEINIT message</span></span>

<span data-ttu-id="755c8-105">Une Active Directory extension de la feuille de propriétés appelle le [**ADsPropGetInitInfo**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo) pour obtenir des informations sur l’objet d’annuaire auquel s’applique l’extension de la feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="755c8-105">An Active Directory property sheet extension calls the [**ADsPropGetInitInfo**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo) to obtain data about regarding the directory object that the property sheet extension applies to.</span></span> <span data-ttu-id="755c8-106">La fonction **ADsPropGetInitInfo** envoie le message **WM \_ ADSPROP \_ Notify \_ PAGEINIT** à l’objet de notification pour obtenir ce résultat.</span><span class="sxs-lookup"><span data-stu-id="755c8-106">The **ADsPropGetInitInfo** function sends the **WM\_ADSPROP\_NOTIFY\_PAGEINIT** message to the notification object to achieve this result.</span></span>


```C++
WM_ADSPROP_NOTIFY_PAGEINIT

    WPARAM wParam
    LPARAM pADsPropInitParams
    
```



## <a name="parameters"></a><span data-ttu-id="755c8-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="755c8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="755c8-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="755c8-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="755c8-109">Handle de l’objet de notification.</span><span class="sxs-lookup"><span data-stu-id="755c8-109">Handle of the notification object.</span></span> <span data-ttu-id="755c8-110">Il s’agit du paramètre *hNotifyObject* obtenu par un appel à [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span><span class="sxs-lookup"><span data-stu-id="755c8-110">This is the *hNotifyObject* parameter obtained by a call to [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span></span>

</dd> <dt>

<span data-ttu-id="755c8-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="755c8-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="755c8-112">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="755c8-112">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="755c8-113">*pADsPropInitParams*</span><span class="sxs-lookup"><span data-stu-id="755c8-113">*pADsPropInitParams*</span></span> 
</dt> <dd>

<span data-ttu-id="755c8-114">Pointeur vers une structure [**ADSPROPINITPARAMS**](/windows/desktop/api/Adsprop/ns-adsprop-adspropinitparams) qui reçoit les informations de l’objet d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="755c8-114">Pointer to an [**ADSPROPINITPARAMS**](/windows/desktop/api/Adsprop/ns-adsprop-adspropinitparams) structure that receives the directory object information.</span></span> <span data-ttu-id="755c8-115">Il s’agit du paramètre *pInitParams* passé à [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span><span class="sxs-lookup"><span data-stu-id="755c8-115">This is the *pInitParams* parameter passed to [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="755c8-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="755c8-116">Return value</span></span>

<span data-ttu-id="755c8-117">Ce message n’a pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="755c8-117">This message has no return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="755c8-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="755c8-118">Requirements</span></span>



| <span data-ttu-id="755c8-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="755c8-119">Requirement</span></span> | <span data-ttu-id="755c8-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="755c8-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="755c8-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="755c8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="755c8-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="755c8-122">Windows Vista</span></span><br/>                                                             |
| <span data-ttu-id="755c8-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="755c8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="755c8-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="755c8-124">Windows Server 2008</span></span><br/>                                                       |
| <span data-ttu-id="755c8-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="755c8-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="755c8-126"><dt>Adsprop. h</dt></span><span class="sxs-lookup"><span data-stu-id="755c8-126"><dt>Adsprop.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="755c8-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="755c8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="755c8-128">Messages dans Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="755c8-128">Messages in Active Directory Domain Services</span></span>](messages-in-active-directory-domain-services.md)
</dt> <dt>

[<span data-ttu-id="755c8-129">**ADsPropGetInitInfo**</span><span class="sxs-lookup"><span data-stu-id="755c8-129">**ADsPropGetInitInfo**</span></span>](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo)
</dt> <dt>

[<span data-ttu-id="755c8-130">**ADSPROPINITPARAMS**</span><span class="sxs-lookup"><span data-stu-id="755c8-130">**ADSPROPINITPARAMS**</span></span>](/windows/desktop/api/Adsprop/ns-adsprop-adspropinitparams)
</dt> </dl>

 

 





