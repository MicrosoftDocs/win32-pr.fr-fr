---
title: Message HDN_ITEMSTATEICONCLICK (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle header que l’utilisateur a cliqué sur l’icône d’état d’un élément. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: a1969579-3a69-49ff-b06e-4b7450146a92
keywords:
- HDN_ITEMSTATEICONCLICK les contrôles de message Windows
topic_type:
- apiref
api_name:
- HDN_ITEMSTATEICONCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95e5e162b78c829e60494f6e8ff81af3ca97eee4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466938"
---
# <a name="hdn_itemstateiconclick-message"></a><span data-ttu-id="cf9f1-105">\_Message HDN ITEMSTATEICONCLICK</span><span class="sxs-lookup"><span data-stu-id="cf9f1-105">HDN\_ITEMSTATEICONCLICK message</span></span>

<span data-ttu-id="cf9f1-106">Avertit la fenêtre parente d’un contrôle header que l’utilisateur a cliqué sur l’icône d’état d’un élément.</span><span class="sxs-lookup"><span data-stu-id="cf9f1-106">Notifies a header control's parent window that the user clicked an item's state icon.</span></span> <span data-ttu-id="cf9f1-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="cf9f1-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_ITEMSTATEICONCLICK

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="cf9f1-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cf9f1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf9f1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cf9f1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cf9f1-110">Pointeur vers une structure [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) qui contient des informations supplémentaires sur l’icône d’État sur laquelle l’utilisateur a cliqué.</span><span class="sxs-lookup"><span data-stu-id="cf9f1-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains additional information about the state icon that was clicked on.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf9f1-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cf9f1-111">Return value</span></span>

<span data-ttu-id="cf9f1-112">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="cf9f1-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf9f1-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cf9f1-113">Requirements</span></span>



| <span data-ttu-id="cf9f1-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cf9f1-114">Requirement</span></span> | <span data-ttu-id="cf9f1-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="cf9f1-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cf9f1-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cf9f1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="cf9f1-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cf9f1-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cf9f1-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cf9f1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="cf9f1-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cf9f1-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cf9f1-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="cf9f1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf9f1-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf9f1-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





