---
title: Message WM_RENDERFORMAT (winuser. h)
description: Envoyé au propriétaire du presse-papiers s’il a retardé le rendu d’un format de presse-papiers spécifique et si une application a demandé des données dans ce format.
ms.assetid: 81638109-4c5e-4b4c-b2db-4208b6ee83cc
keywords:
- WM_RENDERFORMAT l’échange de données de message
topic_type:
- apiref
api_name:
- WM_RENDERFORMAT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab9d0e8539dc666c7a791a24c9ba7ac772c3c2c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317261"
---
# <a name="wm_renderformat-message"></a><span data-ttu-id="cb518-104">\_Message WM RENDERFORMAT</span><span class="sxs-lookup"><span data-stu-id="cb518-104">WM\_RENDERFORMAT message</span></span>

<span data-ttu-id="cb518-105">Envoyé au propriétaire du presse-papiers s’il a retardé le rendu d’un format de presse-papiers spécifique et si une application a demandé des données dans ce format.</span><span class="sxs-lookup"><span data-stu-id="cb518-105">Sent to the clipboard owner if it has delayed rendering a specific clipboard format and if an application has requested data in that format.</span></span> <span data-ttu-id="cb518-106">Le propriétaire du presse-papiers doit restituer les données dans le format spécifié et les placer dans le presse-papiers en appelant la fonction [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) .</span><span class="sxs-lookup"><span data-stu-id="cb518-106">The clipboard owner must render data in the specified format and place it on the clipboard by calling the [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) function.</span></span>


```C++
#define WM_RENDERFORMAT                 0x0305
```



## <a name="parameters"></a><span data-ttu-id="cb518-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cb518-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb518-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cb518-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cb518-109">[Format du presse-papiers](standard-clipboard-formats.md) à restituer.</span><span class="sxs-lookup"><span data-stu-id="cb518-109">The [clipboard format](standard-clipboard-formats.md) to be rendered.</span></span>

</dd> <dt>

<span data-ttu-id="cb518-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cb518-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cb518-111">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="cb518-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb518-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cb518-112">Return value</span></span>

<span data-ttu-id="cb518-113">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="cb518-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb518-114">Notes</span><span class="sxs-lookup"><span data-stu-id="cb518-114">Remarks</span></span>

<span data-ttu-id="cb518-115">Lors de la réponse à un message **WM \_ RENDERFORMAT** , le propriétaire du presse-papiers ne doit pas ouvrir le presse-papiers avant d’appeler [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata).</span><span class="sxs-lookup"><span data-stu-id="cb518-115">When responding to a **WM\_RENDERFORMAT** message, the clipboard owner must not open the clipboard before calling [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata).</span></span> <span data-ttu-id="cb518-116">Il n’est pas nécessaire d’ouvrir le presse-papiers avant de placer des données en réponse à **WM \_ RENDERFORMAT**, et toute tentative d’ouvrir le presse-papiers échoue parce que le presse-papiers est actuellement maintenu ouvert par l’application qui a demandé le rendu du format.</span><span class="sxs-lookup"><span data-stu-id="cb518-116">Opening the clipboard is not necessary before placing data in response to **WM\_RENDERFORMAT**, and any attempt to open the clipboard will fail because the clipboard is currently being held open by the application that requested the format to be rendered.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb518-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cb518-117">Requirements</span></span>



| <span data-ttu-id="cb518-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cb518-118">Requirement</span></span> | <span data-ttu-id="cb518-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb518-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb518-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb518-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cb518-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cb518-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="cb518-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb518-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cb518-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cb518-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cb518-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="cb518-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb518-125"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cb518-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb518-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cb518-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="cb518-127">**Référence**</span><span class="sxs-lookup"><span data-stu-id="cb518-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cb518-128">**SetClipboardData**</span><span class="sxs-lookup"><span data-stu-id="cb518-128">**SetClipboardData**</span></span>](/windows/win32/api/winuser/nf-winuser-setclipboarddata)
</dt> <dt>

[<span data-ttu-id="cb518-129">**\_RENDERALLFORMATS WM**</span><span class="sxs-lookup"><span data-stu-id="cb518-129">**WM\_RENDERALLFORMATS**</span></span>](wm-renderallformats.md)
</dt> <dt>

<span data-ttu-id="cb518-130">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="cb518-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="cb518-131">Presse-papiers</span><span class="sxs-lookup"><span data-stu-id="cb518-131">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 

 





