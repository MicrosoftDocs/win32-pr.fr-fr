---
title: Message TB_SETEXTENDEDSTYLE (commctrl. h)
description: Définit les styles étendus pour un contrôle de barre d’outils.
ms.assetid: aec64bc7-74b4-4efc-9864-2c8a9fbd35c2
keywords:
- TB_SETEXTENDEDSTYLE les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9a540aaeff61bd81b649f0509e064a29282f598
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105040"
---
# <a name="tb_setextendedstyle-message"></a><span data-ttu-id="15f42-104">TO \_ SETEXTENDEDSTYLE message</span><span class="sxs-lookup"><span data-stu-id="15f42-104">TB\_SETEXTENDEDSTYLE message</span></span>

<span data-ttu-id="15f42-105">Définit les styles étendus pour un contrôle de barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="15f42-105">Sets the extended styles for a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="15f42-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="15f42-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15f42-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="15f42-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="15f42-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="15f42-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="15f42-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="15f42-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="15f42-110">Valeur spécifiant les nouveaux styles étendus.</span><span class="sxs-lookup"><span data-stu-id="15f42-110">Value specifying the new extended styles.</span></span> <span data-ttu-id="15f42-111">Ce paramètre peut être une combinaison de [styles étendus](toolbar-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="15f42-111">This parameter can be a combination of [extended styles](toolbar-extended-styles.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15f42-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="15f42-112">Return value</span></span>

<span data-ttu-id="15f42-113">Retourne une **valeur DWORD** qui représente les styles étendus précédents.</span><span class="sxs-lookup"><span data-stu-id="15f42-113">Returns a **DWORD** that represents the previous extended styles.</span></span> <span data-ttu-id="15f42-114">Cette valeur peut être une combinaison de [styles étendus](toolbar-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="15f42-114">This value can be a combination of [extended styles](toolbar-extended-styles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="15f42-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="15f42-115">Requirements</span></span>



| <span data-ttu-id="15f42-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="15f42-116">Requirement</span></span> | <span data-ttu-id="15f42-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="15f42-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="15f42-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="15f42-118">Minimum supported client</span></span><br/> | <span data-ttu-id="15f42-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="15f42-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="15f42-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="15f42-120">Minimum supported server</span></span><br/> | <span data-ttu-id="15f42-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="15f42-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="15f42-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="15f42-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="15f42-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="15f42-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15f42-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="15f42-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15f42-125">**TO \_ GETEXTENDEDSTYLE**</span><span class="sxs-lookup"><span data-stu-id="15f42-125">**TB\_GETEXTENDEDSTYLE**</span></span>](tb-getextendedstyle.md)
</dt> </dl>

 

 





