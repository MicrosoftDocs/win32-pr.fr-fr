---
title: Message TB_GETEXTENDEDSTYLE (commctrl. h)
description: Récupère les styles étendus pour un contrôle ToolBar.
ms.assetid: d9e31a8e-5e5a-4d2d-bc3b-65ac40e8592f
keywords:
- TB_GETEXTENDEDSTYLE les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_GETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f80bc4f4ad45e5c1c75366e0890f3fd76ec1fa74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741212"
---
# <a name="tb_getextendedstyle-message"></a><span data-ttu-id="8d507-104">TO \_ GETEXTENDEDSTYLE message</span><span class="sxs-lookup"><span data-stu-id="8d507-104">TB\_GETEXTENDEDSTYLE message</span></span>

<span data-ttu-id="8d507-105">Récupère les styles étendus pour un contrôle ToolBar.</span><span class="sxs-lookup"><span data-stu-id="8d507-105">Retrieves the extended styles for a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="8d507-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8d507-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d507-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8d507-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="8d507-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="8d507-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="8d507-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8d507-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="8d507-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="8d507-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d507-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8d507-111">Return value</span></span>

<span data-ttu-id="8d507-112">Retourne une **valeur DWORD** qui représente les styles en cours d’utilisation pour le contrôle ToolBar.</span><span class="sxs-lookup"><span data-stu-id="8d507-112">Returns a **DWORD** that represents the styles currently in use for the toolbar control.</span></span> <span data-ttu-id="8d507-113">Cette valeur peut être une combinaison de [styles étendus](toolbar-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="8d507-113">This value can be a combination of [extended styles](toolbar-extended-styles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8d507-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8d507-114">Requirements</span></span>



| <span data-ttu-id="8d507-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8d507-115">Requirement</span></span> | <span data-ttu-id="8d507-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="8d507-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8d507-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d507-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8d507-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8d507-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8d507-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d507-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8d507-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8d507-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8d507-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="8d507-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d507-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d507-122"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d507-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d507-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d507-124">**TO \_ SETEXTENDEDSTYLE**</span><span class="sxs-lookup"><span data-stu-id="8d507-124">**TB\_SETEXTENDEDSTYLE**</span></span>](tb-setextendedstyle.md)
</dt> </dl>

 

 





