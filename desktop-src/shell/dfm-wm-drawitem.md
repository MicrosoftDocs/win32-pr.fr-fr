---
description: Envoyé à la fenêtre parente d’un contrôle ou d’un menu owner-drawn lorsqu’un aspect visuel du contrôle ou du menu a changé.
ms.assetid: 2515bbab-025f-4f00-8564-a732d68edea3
title: Message DFM_WM_DRAWITEM (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67255fea5c39bebc995e5c53d90378536b12921b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972006"
---
# <a name="dfm_wm_drawitem-message"></a><span data-ttu-id="4ecfe-103">\_Message DFM WM \_ DRAWITEM</span><span class="sxs-lookup"><span data-stu-id="4ecfe-103">DFM\_WM\_DRAWITEM message</span></span>

<span data-ttu-id="4ecfe-104">Envoyé à la fenêtre parente d’un contrôle ou d’un menu owner-drawn lorsqu’un aspect visuel du contrôle ou du menu a changé.</span><span class="sxs-lookup"><span data-stu-id="4ecfe-104">Sent to the parent window of an owner-drawn control or menu when a visual aspect of the control or menu has changed.</span></span>


```C++
DFM_WM_DRAWITEM 

    wParam = (WPARAM);

    lParam = (LPARAM)(LPDRAWITEMSTRUCT) lpDrawItem;

            
```



## <a name="parameters"></a><span data-ttu-id="4ecfe-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4ecfe-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ecfe-106">*wParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4ecfe-106">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ecfe-107">Identificateur du contrôle qui a envoyé le message **DFM \_ WM \_ DRAWITEM** .</span><span class="sxs-lookup"><span data-stu-id="4ecfe-107">The identifier of the control that sent the **DFM\_WM\_DRAWITEM** message.</span></span> <span data-ttu-id="4ecfe-108">Si le message a été envoyé par un menu, ce paramètre est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="4ecfe-108">If the message was sent by a menu, this parameter is zero.</span></span>

</dd> <dt>

<span data-ttu-id="4ecfe-109">*lpDrawItem* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4ecfe-109">*lpDrawItem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ecfe-110">Pointeur vers une structure [**drawitemstruct,**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) contenant des informations sur l’élément à dessiner et le type de dessin requis.</span><span class="sxs-lookup"><span data-stu-id="4ecfe-110">A pointer to a [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure containing information about the item to be drawn and the type of drawing required.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ecfe-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4ecfe-111">Return value</span></span>

<span data-ttu-id="4ecfe-112">Si une application traite ce message, elle doit retourner la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="4ecfe-112">If an application processes this message, it should return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ecfe-113">Notes</span><span class="sxs-lookup"><span data-stu-id="4ecfe-113">Remarks</span></span>

<span data-ttu-id="4ecfe-114">Le membre **itemAction** de la structure [**drawitemstruct,**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) spécifie l’opération de dessin qu’une application doit effectuer.</span><span class="sxs-lookup"><span data-stu-id="4ecfe-114">The **itemAction** member of the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure specifies the drawing operation that an application should perform.</span></span>

<span data-ttu-id="4ecfe-115">Avant de revenir au traitement de ce message, une application doit s’assurer que le contexte de périphérique identifié par le membre **HDC** de la structure [**drawitemstruct,**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) est dans l’État par défaut.</span><span class="sxs-lookup"><span data-stu-id="4ecfe-115">Before returning from processing this message, an application should ensure that the device context identified by the **hDC** member of the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure is in the default state.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ecfe-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="4ecfe-116">Requirements</span></span>



| <span data-ttu-id="4ecfe-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4ecfe-117">Requirement</span></span> | <span data-ttu-id="4ecfe-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="4ecfe-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4ecfe-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4ecfe-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4ecfe-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4ecfe-120">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="4ecfe-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4ecfe-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4ecfe-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4ecfe-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4ecfe-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="4ecfe-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ecfe-124"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ecfe-124"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
