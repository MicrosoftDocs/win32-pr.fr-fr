---
title: Message TTM_GETTOOLINFO (commctrl. h)
description: Récupère les informations qu’un contrôle ToolTip gère à propos d’un outil.
ms.assetid: b94d3b78-2437-4c60-ba46-b3f57cf9c876
keywords:
- TTM_GETTOOLINFO les contrôles de message Windows
topic_type:
- apiref
api_name:
- TTM_GETTOOLINFO
- TTM_GETTOOLINFOA
- TTM_GETTOOLINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc0de37b97be3bec495c8777b2ddd1cc6fc1bd42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103732"
---
# <a name="ttm_gettoolinfo-message"></a><span data-ttu-id="89fea-104">\_Message atténuation GETTOOLINFO</span><span class="sxs-lookup"><span data-stu-id="89fea-104">TTM\_GETTOOLINFO message</span></span>

<span data-ttu-id="89fea-105">Récupère les informations qu’un contrôle ToolTip gère à propos d’un outil.</span><span class="sxs-lookup"><span data-stu-id="89fea-105">Retrieves the information that a tooltip control maintains about a tool.</span></span>

## <a name="parameters"></a><span data-ttu-id="89fea-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="89fea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89fea-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="89fea-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="89fea-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="89fea-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="89fea-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="89fea-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="89fea-110">Pointeur vers une structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) .</span><span class="sxs-lookup"><span data-stu-id="89fea-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span> <span data-ttu-id="89fea-111">Lors de l’envoi du message, les membres **HWND** et **UID** identifient un outil et le membre **cbSize** doit spécifier la taille de la structure.</span><span class="sxs-lookup"><span data-stu-id="89fea-111">When sending the message, the **hwnd** and **uId** members identify a tool, and the **cbSize** member must specify the size of the structure.</span></span> <span data-ttu-id="89fea-112">Lorsque vous utilisez ce message pour récupérer le texte d’info-bulle, assurez-vous que le membre **lpszText** de la structure **TOOLINFO** pointe vers une mémoire tampon de taille adquate valide</span><span class="sxs-lookup"><span data-stu-id="89fea-112">When using this message to retrieve the tooltip text, ensure that the **lpszText** member of the **TOOLINFO** structure points to a valid buffer of adquate size</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89fea-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="89fea-113">Return value</span></span>

<span data-ttu-id="89fea-114">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="89fea-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="89fea-115">Notes</span><span class="sxs-lookup"><span data-stu-id="89fea-115">Remarks</span></span>

<span data-ttu-id="89fea-116">Si le contrôle ToolTip comprend l’outil, la structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) reçoit des informations sur l’outil.</span><span class="sxs-lookup"><span data-stu-id="89fea-116">If the tooltip control includes the tool, the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure receives information about the tool.</span></span>

## <a name="examples"></a><span data-ttu-id="89fea-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="89fea-117">Examples</span></span>

<span data-ttu-id="89fea-118">L’exemple suivant repositionne un contrôle ToolTip.</span><span class="sxs-lookup"><span data-stu-id="89fea-118">The following example repositions a tooltip control.</span></span>


```C++
HRESULT MyToolTipClass::OffsetTooltip(int xOffset, int yOffset)  
{  
    HRESULT hr = S_OK;   
    DWORD   dwError = 0;  
  
    if (NULL != m_hWndToolTip)  
    {  
        TOOLINFO ti = {0};  
  
        ti.cbSize = sizeof(TOOLINFO);  
        ti.hwnd   = m_hWndToolTipOwner;  
  
        // Get the current tooltip definition.          
        if( SendMessage(m_hWndToolTip, TTM_GETTOOLINFO, 0, (LPARAM)&ti))  
        {  
            // Offset the tooltip rectangle as specified.              
            OffsetRect(&ti.rect, xOffset, yOffset);  
  
            // Apply the new rectangle to the tooltip.
            SendMessage(m_hWndToolTip, TTM_NEWTOOLRECT, 0, (LPARAM)&ti);  
        }  
        else  
        {  
            dwError = GetLastError();  
            hr = HRESULT_FROM_WIN32(dwError);  
            MyErrorHandler(hr);
       }  
    }  
    return hr;  
}  
```



## <a name="requirements"></a><span data-ttu-id="89fea-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="89fea-119">Requirements</span></span>



| <span data-ttu-id="89fea-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="89fea-120">Requirement</span></span> | <span data-ttu-id="89fea-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="89fea-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="89fea-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="89fea-122">Minimum supported client</span></span><br/> | <span data-ttu-id="89fea-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="89fea-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="89fea-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="89fea-124">Minimum supported server</span></span><br/> | <span data-ttu-id="89fea-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="89fea-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="89fea-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="89fea-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="89fea-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="89fea-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="89fea-128">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="89fea-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="89fea-129">**Atténuation \_ GETTOOLINFOW** (Unicode) et **atténuation \_ GETTOOLINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="89fea-129">**TTM\_GETTOOLINFOW** (Unicode) and **TTM\_GETTOOLINFOA** (ANSI)</span></span><br/>           |



 

 





