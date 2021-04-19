---
title: TDN_TIMER le code de notification (commctrl. h)
description: Envoyé par une boîte de dialogue de tâche environ toutes les 200 millisecondes.
ms.assetid: 5a162d97-6912-45bc-8151-1ea56cc459ea
keywords:
- Contrôles Windows de code de notification TDN_TIMER
topic_type:
- apiref
api_name:
- TDN_TIMER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eea7a1604c70c187299c9f2c99abbe934926317
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106518120"
---
# <a name="tdn_timer-notification-code"></a><span data-ttu-id="1c494-104">\_Code de notification du minuteur TDN</span><span class="sxs-lookup"><span data-stu-id="1c494-104">TDN\_TIMER notification code</span></span>

<span data-ttu-id="1c494-105">Envoyé par une boîte de dialogue de tâche environ toutes les 200 millisecondes.</span><span class="sxs-lookup"><span data-stu-id="1c494-105">Sent by a task dialog approximately every 200 milliseconds.</span></span> <span data-ttu-id="1c494-106">Ce code de notification est envoyé lorsque l' \_ indicateur de minuterie de rappel TDF \_ a été défini dans le membre **dwFlags** de la structure [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) qui a été passée à la fonction [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="1c494-106">This notification code is sent when the TDF\_CALLBACK\_TIMER flag has been set in the **dwFlags** member of the [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) structure that was passed to the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) function.</span></span> <span data-ttu-id="1c494-107">Ce code de notification est reçu uniquement par le biais de la fonction de rappel de la boîte de dialogue de tâche, qui peut être inscrite à l’aide de la méthode **TaskDialogIndirect** .</span><span class="sxs-lookup"><span data-stu-id="1c494-107">This notification code is received only through the task dialog callback function, which can be registered using the **TaskDialogIndirect** method.</span></span>


```C++
TDN_TIMER    

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="1c494-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1c494-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c494-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1c494-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1c494-110">**Valeur DWORD** qui spécifie le nombre de millisecondes écoulées depuis la création de la boîte de dialogue ou si le code de notification a retourné la **\_ valeur false**.</span><span class="sxs-lookup"><span data-stu-id="1c494-110">A **DWORD** that specifies the number of milliseconds since the dialog was created or this notification code returned **S\_FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="1c494-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1c494-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1c494-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="1c494-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c494-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1c494-113">Return value</span></span>

<span data-ttu-id="1c494-114">Pour réinitialiser le TickCount, l’application doit retourner **la \_ valeur false**, sinon le TickCount continue à s’incrémenter.</span><span class="sxs-lookup"><span data-stu-id="1c494-114">To reset the tickcount, the application must return **S\_FALSE**, otherwise the tickcount will continue to increment.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c494-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1c494-115">Requirements</span></span>



| <span data-ttu-id="1c494-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1c494-116">Requirement</span></span> | <span data-ttu-id="1c494-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="1c494-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1c494-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1c494-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1c494-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1c494-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1c494-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1c494-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1c494-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1c494-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1c494-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="1c494-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c494-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c494-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





