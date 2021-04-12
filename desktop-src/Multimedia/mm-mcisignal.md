---
title: Message MM_MCISIGNAL (mmsystem. h)
description: Le \_ message mm MCISIGNAL est envoyé à une fenêtre pour avertir une application qu’un périphérique MCI a atteint une position définie dans une commande de signal précédente ( \_ signal MCI).
ms.assetid: 12512d23-9a89-4e38-9ec5-88845766f4f6
keywords:
- Message MM_MCISIGNAL Windows Multimedia
topic_type:
- apiref
api_name:
- MM_MCISIGNAL
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6d42d4d39f31b82c7461a5bd8d8561b0da1b6bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385020"
---
# <a name="mm_mcisignal-message"></a><span data-ttu-id="1014a-104">MM \_ message MCISIGNAL</span><span class="sxs-lookup"><span data-stu-id="1014a-104">MM\_MCISIGNAL message</span></span>

<span data-ttu-id="1014a-105">Le message **mm \_ MCISIGNAL** est envoyé à une fenêtre pour avertir une application qu’un périphérique MCI a atteint une position définie dans une commande de [**signal**](signal.md) précédente ( [**\_ signal MCI**](mci-signal.md)).</span><span class="sxs-lookup"><span data-stu-id="1014a-105">The **MM\_MCISIGNAL** message is sent to a window to notify an application that an MCI device has reached a position defined in a previous [**signal**](signal.md) ( [**MCI\_SIGNAL**](mci-signal.md)) command.</span></span>


```C++
MM_MCISIGNAL 
wParam = (WPARAM) wID      
lParam = (LONG) lUserParm  
```



## <a name="parameters"></a><span data-ttu-id="1014a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1014a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1014a-107"><span id="wID"></span><span id="wid"></span><span id="WID"></span>*wID*</span><span class="sxs-lookup"><span data-stu-id="1014a-107"><span id="wID"></span><span id="wid"></span><span id="WID"></span>*wID*</span></span>
</dt> <dd>

<span data-ttu-id="1014a-108">Identificateur de l’appareil initialisant le message de signal.</span><span class="sxs-lookup"><span data-stu-id="1014a-108">Identifier of the device initiating the signal message.</span></span>

</dd> <dt>

<span data-ttu-id="1014a-109"><span id="lUserParm"></span><span id="luserparm"></span><span id="LUSERPARM"></span>*lUserParm*</span><span class="sxs-lookup"><span data-stu-id="1014a-109"><span id="lUserParm"></span><span id="luserparm"></span><span id="LUSERPARM"></span>*lUserParm*</span></span>
</dt> <dd>

<span data-ttu-id="1014a-110">Valeur transmise dans le membre **dwUserParm** de la structure de **paramètre de \_ \_ signal \_ MCI DGV** lorsque la commande de **signal** a défini cette fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="1014a-110">Value passed in the **dwUserParm** member of the **MCI\_DGV\_SIGNAL\_PARAMS** structure when the **signal** command has defined this callback function.</span></span> <span data-ttu-id="1014a-111">Il peut également contenir la valeur de position.</span><span class="sxs-lookup"><span data-stu-id="1014a-111">Alternatively, it might contain the position value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1014a-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1014a-112">Requirements</span></span>



| <span data-ttu-id="1014a-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1014a-113">Requirement</span></span> | <span data-ttu-id="1014a-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="1014a-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1014a-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1014a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="1014a-116">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1014a-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1014a-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1014a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="1014a-118">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1014a-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1014a-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="1014a-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="1014a-120"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1014a-120"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1014a-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1014a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1014a-122">MCI</span><span class="sxs-lookup"><span data-stu-id="1014a-122">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="1014a-123">Messages MCI</span><span class="sxs-lookup"><span data-stu-id="1014a-123">MCI Messages</span></span>](mci-messages.md)
</dt> <dt>

[<span data-ttu-id="1014a-124">**témoin**</span><span class="sxs-lookup"><span data-stu-id="1014a-124">**signal**</span></span>](signal.md)
</dt> </dl>

 

 





