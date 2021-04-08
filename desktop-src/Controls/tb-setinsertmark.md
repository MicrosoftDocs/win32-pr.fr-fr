---
title: Message TB_SETINSERTMARK (commctrl. h)
description: Définit la marque d’insertion actuelle pour la barre d’outils.
ms.assetid: 9a576fca-89cf-4db5-9840-35bfa56af89e
keywords:
- TB_SETINSERTMARK les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_SETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f65ba83d13cbb45f54833725a46de61a5f0444c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102868"
---
# <a name="tb_setinsertmark-message"></a><span data-ttu-id="500a9-104">TO \_ SETINSERTMARK message</span><span class="sxs-lookup"><span data-stu-id="500a9-104">TB\_SETINSERTMARK message</span></span>

<span data-ttu-id="500a9-105">Définit la marque d’insertion actuelle pour la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="500a9-105">Sets the current insertion mark for the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="500a9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="500a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="500a9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="500a9-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="500a9-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="500a9-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="500a9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="500a9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="500a9-110">Pointeur vers une structure [**TBINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) qui contient la marque d’insertion.</span><span class="sxs-lookup"><span data-stu-id="500a9-110">Pointer to a [**TBINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) structure that contains the insertion mark.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="500a9-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="500a9-111">Return value</span></span>

<span data-ttu-id="500a9-112">La valeur de retour de ce message n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="500a9-112">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="500a9-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="500a9-113">Requirements</span></span>



| <span data-ttu-id="500a9-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="500a9-114">Requirement</span></span> | <span data-ttu-id="500a9-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="500a9-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="500a9-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="500a9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="500a9-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="500a9-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="500a9-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="500a9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="500a9-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="500a9-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="500a9-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="500a9-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="500a9-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="500a9-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="500a9-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="500a9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="500a9-123">**TO \_ GETINSERTMARK**</span><span class="sxs-lookup"><span data-stu-id="500a9-123">**TB\_GETINSERTMARK**</span></span>](tb-getinsertmark.md)
</dt> </dl>

 

 





