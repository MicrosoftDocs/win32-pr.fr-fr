---
title: Message RB_MAXIMIZEBAND (commctrl. h)
description: Redimensionne une bande dans un contrôle rebar en sa taille idéale ou la plus grande taille.
ms.assetid: 79fff6d0-01f2-4308-b916-38dc06dad894
keywords:
- RB_MAXIMIZEBAND les contrôles de message Windows
topic_type:
- apiref
api_name:
- RB_MAXIMIZEBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 708a8fae7c0dd8e72eea8e5acefe43ab50054592
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843925"
---
# <a name="rb_maximizeband-message"></a><span data-ttu-id="4042e-104">\_Message MAXIMIZEBAND RB</span><span class="sxs-lookup"><span data-stu-id="4042e-104">RB\_MAXIMIZEBAND message</span></span>

<span data-ttu-id="4042e-105">Redimensionne une bande dans un contrôle rebar en sa taille idéale ou la plus grande taille.</span><span class="sxs-lookup"><span data-stu-id="4042e-105">Resizes a band in a rebar control to either its ideal or largest size.</span></span>

## <a name="parameters"></a><span data-ttu-id="4042e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4042e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4042e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4042e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4042e-108">Index de base zéro de la bande à agrandir.</span><span class="sxs-lookup"><span data-stu-id="4042e-108">Zero-based index of the band to be maximized.</span></span>

</dd> <dt>

<span data-ttu-id="4042e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4042e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4042e-110">Indique si la largeur idéale de la bande doit être utilisée lorsque la bande est agrandie.</span><span class="sxs-lookup"><span data-stu-id="4042e-110">Indicates if the ideal width of the band should be used when the band is maximized.</span></span> <span data-ttu-id="4042e-111">Si cette valeur est différente de zéro, la largeur idéale sera utilisée.</span><span class="sxs-lookup"><span data-stu-id="4042e-111">If this value is nonzero, the ideal width will be used.</span></span> <span data-ttu-id="4042e-112">Si cette valeur est égale à zéro, la bande sera aussi grande que possible.</span><span class="sxs-lookup"><span data-stu-id="4042e-112">If this value is zero, the band will be made as large as possible.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4042e-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4042e-113">Return value</span></span>

<span data-ttu-id="4042e-114">La valeur de retour n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="4042e-114">The return value is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="4042e-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4042e-115">Requirements</span></span>



| <span data-ttu-id="4042e-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4042e-116">Requirement</span></span> | <span data-ttu-id="4042e-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="4042e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4042e-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4042e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4042e-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4042e-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4042e-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4042e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4042e-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4042e-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4042e-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="4042e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4042e-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4042e-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4042e-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4042e-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="4042e-125">**Référence**</span><span class="sxs-lookup"><span data-stu-id="4042e-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4042e-126">**\_SETBANDINFO RB**</span><span class="sxs-lookup"><span data-stu-id="4042e-126">**RB\_SETBANDINFO**</span></span>](rb-setbandinfo.md)
</dt> </dl>

 

 





