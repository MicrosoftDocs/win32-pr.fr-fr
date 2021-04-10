---
title: LVN_COLUMNCLICK le code de notification (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle List-View qu’un clic a été effectué sur un en-tête de colonne alors que le contrôle List-View était en mode rapport. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: a6bfbd6c-4778-47a7-92e9-9140d46d89cc
keywords:
- Contrôles Windows de code de notification LVN_COLUMNCLICK
topic_type:
- apiref
api_name:
- LVN_COLUMNCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27cfd75d913c62c89c4cfe305333a934fe172fe2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032422"
---
# <a name="lvn_columnclick-notification-code"></a><span data-ttu-id="66ee4-105">\_Code de notification LVN COLUMNCLICK</span><span class="sxs-lookup"><span data-stu-id="66ee4-105">LVN\_COLUMNCLICK notification code</span></span>

<span data-ttu-id="66ee4-106">Avertit une fenêtre parente d’un contrôle List-View qu’un clic a été effectué sur un en-tête de colonne alors que le contrôle List-View était en mode rapport.</span><span class="sxs-lookup"><span data-stu-id="66ee4-106">Notifies a list-view control's parent window that a column header was clicked while the list-view control was in report mode.</span></span> <span data-ttu-id="66ee4-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="66ee4-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_COLUMNCLICK

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="66ee4-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="66ee4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66ee4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="66ee4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="66ee4-110">Pointeur vers une structure [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) .</span><span class="sxs-lookup"><span data-stu-id="66ee4-110">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure.</span></span> <span data-ttu-id="66ee4-111">Le membre **iItem** est-1 et le membre **iSubItem** identifie la colonne.</span><span class="sxs-lookup"><span data-stu-id="66ee4-111">The **iItem** member is -1, and the **iSubItem** member identifies the column.</span></span> <span data-ttu-id="66ee4-112">Tous les autres membres sont nuls.</span><span class="sxs-lookup"><span data-stu-id="66ee4-112">All other members are zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66ee4-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="66ee4-113">Return value</span></span>

<span data-ttu-id="66ee4-114">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="66ee4-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="66ee4-115">Notes</span><span class="sxs-lookup"><span data-stu-id="66ee4-115">Remarks</span></span>

<span data-ttu-id="66ee4-116">L’utilisation de formats de contrôle d’en-tête tels que HDF \_ case à cocher pour modifier le format des en-têtes de colonnes dans un contrôle List-View entraîne l’envoi par le contrôle du code de notification [ \_ ITEMSTATEICONCLICK HDN](hdn-itemstateiconclick.md) au lieu de LVN \_ COLUMNCLICK lorsqu’un utilisateur clique sur un élément d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="66ee4-116">Using header control formats such as HDF\_CHECKBOX to modify the format of column headers in a list-view control causes the control to send the [HDN\_ITEMSTATEICONCLICK](hdn-itemstateiconclick.md) notification code instead of LVN\_COLUMNCLICK when a header item is clicked.</span></span>

## <a name="requirements"></a><span data-ttu-id="66ee4-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="66ee4-117">Requirements</span></span>



| <span data-ttu-id="66ee4-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="66ee4-118">Requirement</span></span> | <span data-ttu-id="66ee4-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="66ee4-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="66ee4-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66ee4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="66ee4-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="66ee4-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="66ee4-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66ee4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="66ee4-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="66ee4-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="66ee4-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="66ee4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="66ee4-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="66ee4-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





