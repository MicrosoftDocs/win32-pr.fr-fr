---
title: Message RB_PUSHCHEVRON (commctrl. h)
description: Envoyé à un contrôle rebar pour pousser par programme un chevron.
ms.assetid: 00a8ce10-1fb2-488a-a6f9-1814f73f82bd
keywords:
- RB_PUSHCHEVRON les contrôles de message Windows
topic_type:
- apiref
api_name:
- RB_PUSHCHEVRON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e09e558d5574d4fd28cf01e9794657556dda4ae8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508906"
---
# <a name="rb_pushchevron-message"></a><span data-ttu-id="7d0f4-104">\_Message PUSHCHEVRON RB</span><span class="sxs-lookup"><span data-stu-id="7d0f4-104">RB\_PUSHCHEVRON message</span></span>

<span data-ttu-id="7d0f4-105">Envoyé à un contrôle rebar pour pousser par programme un chevron.</span><span class="sxs-lookup"><span data-stu-id="7d0f4-105">Sent to a rebar control to programmatically push a chevron.</span></span>

## <a name="parameters"></a><span data-ttu-id="7d0f4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7d0f4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d0f4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7d0f4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7d0f4-108">Index de base zéro de la bande dont le Chevron doit faire l’objet d’un push.</span><span class="sxs-lookup"><span data-stu-id="7d0f4-108">Zero-based index of the band whose chevron is to be pushed.</span></span>

</dd> <dt>

<span data-ttu-id="7d0f4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7d0f4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7d0f4-110">Valeur 32 bits définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="7d0f4-110">An application defined 32-bit value.</span></span> <span data-ttu-id="7d0f4-111">Elle est repassée à l’application en tant que membre **lParamNM** de la structure [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) qui est passée avec la notification [ \_ CHEVRONPUSHED RBN](rbn-chevronpushed.md) .</span><span class="sxs-lookup"><span data-stu-id="7d0f4-111">It will be passed back to the application as the **lParamNM** member of the [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) structure that is passed with the [RBN\_CHEVRONPUSHED](rbn-chevronpushed.md) notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d0f4-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7d0f4-112">Return value</span></span>

<span data-ttu-id="7d0f4-113">La valeur de retour de ce message n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="7d0f4-113">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d0f4-114">Notes</span><span class="sxs-lookup"><span data-stu-id="7d0f4-114">Remarks</span></span>

<span data-ttu-id="7d0f4-115">Lorsque ce message est envoyé, le contrôle rebar envoie à l’application un code de notification [RBN \_ CHEVRONPUSHED](rbn-chevronpushed.md) , lui invitant à afficher le menu Chevron.</span><span class="sxs-lookup"><span data-stu-id="7d0f4-115">When this message is sent, the rebar control will send the application an [RBN\_CHEVRONPUSHED](rbn-chevronpushed.md) notification code, prompting it to display the chevron menu.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d0f4-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7d0f4-116">Requirements</span></span>



| <span data-ttu-id="7d0f4-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7d0f4-117">Requirement</span></span> | <span data-ttu-id="7d0f4-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="7d0f4-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7d0f4-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7d0f4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7d0f4-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7d0f4-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7d0f4-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7d0f4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7d0f4-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7d0f4-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7d0f4-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="7d0f4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d0f4-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d0f4-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





