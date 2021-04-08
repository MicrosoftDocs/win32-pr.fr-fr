---
title: Message MCIWNDM_SENDSTRING (VFW. h)
description: Le \_ message MCIWNDM SENDSTRING envoie une commande MCI sous forme de chaîne à l’appareil associé à la fenêtre MCIWnd. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndSendString.
ms.assetid: 0e999a0e-588d-4f06-a1bc-fd3f245d8980
keywords:
- Message MCIWNDM_SENDSTRING Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_SENDSTRING
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d36a034a3459803b1652bafed4eb389866add211
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742485"
---
# <a name="mciwndm_sendstring-message"></a><span data-ttu-id="d00f8-105">\_Message MCIWNDM SENDSTRING</span><span class="sxs-lookup"><span data-stu-id="d00f8-105">MCIWNDM\_SENDSTRING message</span></span>

<span data-ttu-id="d00f8-106">Le message **MCIWNDM \_ SENDSTRING** envoie une commande MCI sous forme de chaîne à l’appareil associé à la fenêtre MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="d00f8-106">The **MCIWNDM\_SENDSTRING** message sends an MCI command in string form to the device associated with the MCIWnd window.</span></span> <span data-ttu-id="d00f8-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) .</span><span class="sxs-lookup"><span data-stu-id="d00f8-107">You can send this message explicitly or by using the [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) macro.</span></span>


```C++
MCIWNDM_SENDSTRING 
wParam = 0; 
lParam = (LPARAM) (LPSTR) sz; 
```



## <a name="parameters"></a><span data-ttu-id="d00f8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d00f8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d00f8-109"><span id="sz"></span><span id="SZ"></span>*SZ*</span><span class="sxs-lookup"><span data-stu-id="d00f8-109"><span id="sz"></span><span id="SZ"></span>*sz*</span></span>
</dt> <dd>

<span data-ttu-id="d00f8-110">Commande de chaîne à envoyer à l’appareil MCI.</span><span class="sxs-lookup"><span data-stu-id="d00f8-110">String command to send to the MCI device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d00f8-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d00f8-111">Return Value</span></span>

<span data-ttu-id="d00f8-112">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="d00f8-112">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d00f8-113">Notes</span><span class="sxs-lookup"><span data-stu-id="d00f8-113">Remarks</span></span>

<span data-ttu-id="d00f8-114">Le gestionnaire de messages pour **MCIWNDM \_ SENDSTRING** ajoute un alias d’appareil à la commande MCI que vous envoyez à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d00f8-114">The message handler for **MCIWNDM\_SENDSTRING** appends a device alias to the MCI command you send to the device.</span></span> <span data-ttu-id="d00f8-115">Par conséquent, vous ne devez pas utiliser d’alias dans une commande MCI que vous émettez avec **MCIWNDM \_ SENDSTRING**.</span><span class="sxs-lookup"><span data-stu-id="d00f8-115">Therefore, you should not use any alias in an MCI command that you issue with **MCIWNDM\_SENDSTRING**.</span></span>

<span data-ttu-id="d00f8-116">Pour obtenir la chaîne de retour, qui contient le résultat de la commande, envoyez le message [**MCIWNDM \_ RETURNSTRING**](mciwndm-returnstring.md) .</span><span class="sxs-lookup"><span data-stu-id="d00f8-116">To get the return string, which contains the result of the command, send the [**MCIWNDM\_RETURNSTRING**](mciwndm-returnstring.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="d00f8-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d00f8-117">Requirements</span></span>



| <span data-ttu-id="d00f8-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d00f8-118">Requirement</span></span> | <span data-ttu-id="d00f8-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="d00f8-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d00f8-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d00f8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d00f8-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d00f8-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d00f8-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d00f8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d00f8-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d00f8-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d00f8-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="d00f8-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d00f8-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="d00f8-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d00f8-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d00f8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d00f8-127">**MCIWndSendString**</span><span class="sxs-lookup"><span data-stu-id="d00f8-127">**MCIWndSendString**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring)
</dt> <dt>

[<span data-ttu-id="d00f8-128">Chaînes de commande multimédia</span><span class="sxs-lookup"><span data-stu-id="d00f8-128">Multimedia Command Strings</span></span>](multimedia-command-strings.md)
</dt> </dl>

 

 





