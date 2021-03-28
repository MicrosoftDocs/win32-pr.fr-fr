---
description: Demande le titre et le texte d’une info-bulle de Chevron pour l’élément spécifié par la structure SMDATA associée.
ms.assetid: 7bce4079-994c-4eb0-ab86-9044701d85a1
title: Message SMC_CHEVRONGETTIP (ShObjIdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 118056627d19990648e81b69aa355f3df99ec286
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973459"
---
# <a name="smc_chevrongettip-message"></a><span data-ttu-id="62eac-103">\_Message SMC CHEVRONGETTIP</span><span class="sxs-lookup"><span data-stu-id="62eac-103">SMC\_CHEVRONGETTIP message</span></span>

<span data-ttu-id="62eac-104">Demande le titre et le texte d’une info-bulle de Chevron pour l’élément spécifié par la structure [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) associée.</span><span class="sxs-lookup"><span data-stu-id="62eac-104">Requests the title and text for a chevron infotip for the item specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_CHEVRONGETTIP 
    wParam = (WPARAM) (LPWSTR) pwszTipTitle;
    lParam = (LPARAM) (LPWSTR) pwszTipText
            
```



## <a name="parameters"></a><span data-ttu-id="62eac-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="62eac-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62eac-106">*pwszTipTitle*</span><span class="sxs-lookup"><span data-stu-id="62eac-106">*pwszTipTitle*</span></span> 
</dt> <dd>

<span data-ttu-id="62eac-107">Pointeur vers une mémoire tampon qui reçoit une chaîne Unicode terminée par le caractère **null** qui contient le titre de l’info-bulle.</span><span class="sxs-lookup"><span data-stu-id="62eac-107">A pointer to a buffer that receives a **NULL**-terminated Unicode string that contains the infotip's title.</span></span> <span data-ttu-id="62eac-108">Cette chaîne ne doit pas dépasser la longueur maximale de \_ caractères de chemin d’accès, y compris le caractère **null** de fin.</span><span class="sxs-lookup"><span data-stu-id="62eac-108">This string must be no longer than MAX\_PATH characters long, including the terminating **NULL** character.</span></span>

</dd> <dt>

<span data-ttu-id="62eac-109">*pwszTipText*</span><span class="sxs-lookup"><span data-stu-id="62eac-109">*pwszTipText*</span></span> 
</dt> <dd>

<span data-ttu-id="62eac-110">Pointeur vers une mémoire tampon qui reçoit une chaîne Unicode terminée par le caractère **null** qui contient le texte de l’info-bulle.</span><span class="sxs-lookup"><span data-stu-id="62eac-110">A pointer to a buffer that receives a **NULL**-terminated Unicode string that contains the infotip's text.</span></span> <span data-ttu-id="62eac-111">Cette chaîne ne doit pas dépasser la longueur maximale de \_ caractères de chemin d’accès, y compris le caractère **null** de fin.</span><span class="sxs-lookup"><span data-stu-id="62eac-111">This string must be no longer than MAX\_PATH characters long, including the terminating **NULL** character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62eac-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="62eac-112">Return value</span></span>

<span data-ttu-id="62eac-113">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="62eac-113">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="62eac-114">Notes</span><span class="sxs-lookup"><span data-stu-id="62eac-114">Remarks</span></span>

<span data-ttu-id="62eac-115">Cette notification est reçue par la méthode [**IShellMenuCallback :: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="62eac-115">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="62eac-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="62eac-116">Requirements</span></span>



| <span data-ttu-id="62eac-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="62eac-117">Requirement</span></span> | <span data-ttu-id="62eac-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="62eac-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="62eac-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="62eac-119">Minimum supported client</span></span><br/> | <span data-ttu-id="62eac-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="62eac-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="62eac-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="62eac-121">Minimum supported server</span></span><br/> | <span data-ttu-id="62eac-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="62eac-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="62eac-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="62eac-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="62eac-124"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="62eac-124"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="62eac-125">MIDL</span><span class="sxs-lookup"><span data-stu-id="62eac-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="62eac-126"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="62eac-126"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




