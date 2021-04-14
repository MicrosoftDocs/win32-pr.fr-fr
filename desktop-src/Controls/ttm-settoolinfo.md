---
title: Message TTM_SETTOOLINFO (commctrl. h)
description: Définit les informations gérées par un contrôle ToolTip pour un outil.
ms.assetid: ba18f651-2e52-46e2-871b-c1760e94ab59
keywords:
- TTM_SETTOOLINFO les contrôles de message Windows
topic_type:
- apiref
api_name:
- TTM_SETTOOLINFO
- TTM_SETTOOLINFOA
- TTM_SETTOOLINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 327dd853e3304f8233b95c947a890c4f49298cc7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466798"
---
# <a name="ttm_settoolinfo-message"></a><span data-ttu-id="56835-104">\_Message atténuation SETTOOLINFO</span><span class="sxs-lookup"><span data-stu-id="56835-104">TTM\_SETTOOLINFO message</span></span>

<span data-ttu-id="56835-105">Définit les informations gérées par un contrôle ToolTip pour un outil.</span><span class="sxs-lookup"><span data-stu-id="56835-105">Sets the information that a tooltip control maintains for a tool.</span></span>

## <a name="parameters"></a><span data-ttu-id="56835-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="56835-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56835-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="56835-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="56835-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="56835-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="56835-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="56835-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="56835-110">Pointeur vers une structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) qui spécifie les informations à définir.</span><span class="sxs-lookup"><span data-stu-id="56835-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure that specifies the information to set.</span></span> <span data-ttu-id="56835-111">Le membre **cbSize** de cette structure doit être défini avant l’envoi de ce message.</span><span class="sxs-lookup"><span data-stu-id="56835-111">The **cbSize** member of this structure must be set before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56835-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="56835-112">Return value</span></span>

<span data-ttu-id="56835-113">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="56835-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="56835-114">Notes</span><span class="sxs-lookup"><span data-stu-id="56835-114">Remarks</span></span>

<span data-ttu-id="56835-115">Certaines propriétés internes d’un outil sont établies lorsque l’outil est créé et ne sont pas recalculées lorsqu’un message **atténuation \_ SETTOOLINFO** est envoyé.</span><span class="sxs-lookup"><span data-stu-id="56835-115">Some internal properties of a tool are established when the tool is created, and are not recomputed when a **TTM\_SETTOOLINFO** message is sent.</span></span> <span data-ttu-id="56835-116">Si vous affectez simplement des valeurs à une structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) et que vous la transmettez au contrôle ToolTip avec un message **atténuation \_ SETTOOLINFO** , ces propriétés peuvent être perdues.</span><span class="sxs-lookup"><span data-stu-id="56835-116">If you simply assign values to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure and pass it to the tooltip control with a **TTM\_SETTOOLINFO** message, these properties may be lost.</span></span> <span data-ttu-id="56835-117">Au lieu de cela, votre application doit d’abord demander la structure **TOOLINFO** actuelle de l’outil en envoyant le contrôle ToolTip à un message [**atténuation \_ GETTOOLINFO**](ttm-gettoolinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="56835-117">Instead, your application should first request the tool's current **TOOLINFO** structure by sending the tooltip control a [**TTM\_GETTOOLINFO**](ttm-gettoolinfo.md) message.</span></span> <span data-ttu-id="56835-118">Modifiez ensuite les membres de cette structure en fonction des besoins et repassez-la au contrôle ToolTip avec **atténuation \_ SETTOOLINFO**.</span><span class="sxs-lookup"><span data-stu-id="56835-118">Then, modify the members of this structure as needed and pass it back to the tooltip control with **TTM\_SETTOOLINFO**.</span></span>

<span data-ttu-id="56835-119">Lors de l’appel de **atténuation \_ SETTOOLINFO**, la chaîne vers laquelle pointe le membre **LpszText** de la structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) ne doit pas dépasser 80 **TCHARs** , y compris le caractère **null** de fin.</span><span class="sxs-lookup"><span data-stu-id="56835-119">When calling **TTM\_SETTOOLINFO**, the string pointed to by the **lpszText** member of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure must not exceed 80 **TCHARs** in length, including the terminating **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="56835-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="56835-120">Requirements</span></span>



| <span data-ttu-id="56835-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="56835-121">Requirement</span></span> | <span data-ttu-id="56835-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="56835-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="56835-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="56835-123">Minimum supported client</span></span><br/> | <span data-ttu-id="56835-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="56835-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="56835-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="56835-125">Minimum supported server</span></span><br/> | <span data-ttu-id="56835-126">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="56835-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="56835-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="56835-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="56835-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="56835-128"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="56835-129">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="56835-129">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="56835-130">**Atténuation \_ SETTOOLINFOW** (Unicode) et **atténuation \_ SETTOOLINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="56835-130">**TTM\_SETTOOLINFOW** (Unicode) and **TTM\_SETTOOLINFOA** (ANSI)</span></span><br/>           |



 

 





