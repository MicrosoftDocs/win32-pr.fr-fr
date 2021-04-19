---
title: Message TTM_GETTEXT (commctrl. h)
description: Récupère les informations qu’un contrôle ToolTip gère à propos d’un outil.
ms.assetid: f2afa706-4209-4761-a981-df3d5b938c88
keywords:
- TTM_GETTEXT les contrôles de message Windows
topic_type:
- apiref
api_name:
- TTM_GETTEXT
- TTM_GETTEXTA
- TTM_GETTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f774671d34f89306593d23481fa917190ae69aaa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513604"
---
# <a name="ttm_gettext-message"></a><span data-ttu-id="940e0-104">\_Message atténuation GETTEXT</span><span class="sxs-lookup"><span data-stu-id="940e0-104">TTM\_GETTEXT message</span></span>

<span data-ttu-id="940e0-105">Récupère les informations qu’un contrôle ToolTip gère à propos d’un outil.</span><span class="sxs-lookup"><span data-stu-id="940e0-105">Retrieves the information a tooltip control maintains about a tool.</span></span>

## <a name="parameters"></a><span data-ttu-id="940e0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="940e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="940e0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="940e0-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="940e0-108">Le nombre de **TCHARs**, y compris le caractère **null** de fin, à copier dans la mémoire tampon vers laquelle pointe **lpszText**.</span><span class="sxs-lookup"><span data-stu-id="940e0-108">The number of **TCHARs**, including the terminating **NULL**, to copy to the buffer pointed to by **lpszText**.</span></span> </dd> <dt>

<span data-ttu-id="940e0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="940e0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="940e0-110">Pointeur vers une structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) .</span><span class="sxs-lookup"><span data-stu-id="940e0-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span> <span data-ttu-id="940e0-111">Définissez le membre **cbSize** de cette structure sur `sizeof(TOOLINFO)` avant d’envoyer ce message.</span><span class="sxs-lookup"><span data-stu-id="940e0-111">Set the **cbSize** member of this structure to `sizeof(TOOLINFO)` before sending this message.</span></span> <span data-ttu-id="940e0-112">Définissez les membres **HWND** et **UID** pour identifier l’outil pour lequel des informations doivent être récupérées.</span><span class="sxs-lookup"><span data-stu-id="940e0-112">Set the **hwnd** and **uId** members to identify the tool for which to retrieve information.</span></span> <span data-ttu-id="940e0-113">Allouez une mémoire tampon de taille spécifiée par *wParam*.</span><span class="sxs-lookup"><span data-stu-id="940e0-113">Allocate a buffer of size specified by *wParam*.</span></span> <span data-ttu-id="940e0-114">Définissez le membre **lpszText** pour qu’il pointe vers la mémoire tampon pour recevoir le texte de l’outil.</span><span class="sxs-lookup"><span data-stu-id="940e0-114">Set the **lpszText** member to point to the buffer to receive the tool text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="940e0-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="940e0-115">Return value</span></span>

<span data-ttu-id="940e0-116">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="940e0-116">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="940e0-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="940e0-117">Requirements</span></span>



| <span data-ttu-id="940e0-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="940e0-118">Requirement</span></span> | <span data-ttu-id="940e0-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="940e0-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="940e0-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="940e0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="940e0-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="940e0-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="940e0-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="940e0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="940e0-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="940e0-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="940e0-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="940e0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="940e0-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="940e0-125"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="940e0-126">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="940e0-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="940e0-127">**Atténuation \_ GETTEXTW** (Unicode) et **atténuation \_ gettexta** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="940e0-127">**TTM\_GETTEXTW** (Unicode) and **TTM\_GETTEXTA** (ANSI)</span></span><br/>                   |



 

 





