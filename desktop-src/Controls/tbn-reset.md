---
title: TBN_RESET le code de notification (commctrl. h)
description: Avertit la fenêtre parente de la barre d’outils que l’utilisateur a réinitialisé le contenu de la boîte de dialogue Personnaliser la barre d’outils. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 55efba85-b453-48b9-83df-76820249e7a8
keywords:
- Contrôles Windows de code de notification TBN_RESET
topic_type:
- apiref
api_name:
- TBN_RESET
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 117ee2a50445ffe4dd8cd23d952fde7836bcf023
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033201"
---
# <a name="tbn_reset-notification-code"></a><span data-ttu-id="d7bb0-105">\_Code de notification de réinitialisation TBN</span><span class="sxs-lookup"><span data-stu-id="d7bb0-105">TBN\_RESET notification code</span></span>

<span data-ttu-id="d7bb0-106">Avertit la fenêtre parente de la barre d’outils que l’utilisateur a réinitialisé le contenu de la boîte de dialogue Personnaliser la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="d7bb0-106">Notifies the toolbar's parent window that the user has reset the content of the Customize Toolbar dialog box.</span></span> <span data-ttu-id="d7bb0-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d7bb0-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_RESET 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="d7bb0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d7bb0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7bb0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d7bb0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d7bb0-110">Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations sur le code de notification.</span><span class="sxs-lookup"><span data-stu-id="d7bb0-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7bb0-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d7bb0-111">Return value</span></span>

<span data-ttu-id="d7bb0-112">Return TBNRF \_ ENDCUSTOMIZE pour fermer la boîte de dialogue Personnaliser la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="d7bb0-112">Return TBNRF\_ENDCUSTOMIZE to close the Customize Toolbar dialog box.</span></span> <span data-ttu-id="d7bb0-113">Toutes les autres valeurs de retour sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="d7bb0-113">All other return values are ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7bb0-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d7bb0-114">Requirements</span></span>



| <span data-ttu-id="d7bb0-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d7bb0-115">Requirement</span></span> | <span data-ttu-id="d7bb0-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7bb0-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d7bb0-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7bb0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d7bb0-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d7bb0-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d7bb0-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7bb0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d7bb0-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d7bb0-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d7bb0-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="d7bb0-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7bb0-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7bb0-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





