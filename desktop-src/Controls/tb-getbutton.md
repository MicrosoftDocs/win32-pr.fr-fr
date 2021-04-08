---
title: Message TB_GETBUTTON (commctrl. h)
description: Récupère des informations sur le bouton spécifié dans une barre d’outils.
ms.assetid: d90d053c-0daf-4a5a-b7ca-b9b4472c65a3
keywords:
- TB_GETBUTTON les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_GETBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb2080a6c984bb2384f68a1388bd46fe598f5087
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743964"
---
# <a name="tb_getbutton-message"></a><span data-ttu-id="e8963-104">TO \_ GETBUTTON message</span><span class="sxs-lookup"><span data-stu-id="e8963-104">TB\_GETBUTTON message</span></span>

<span data-ttu-id="e8963-105">Récupère des informations sur le bouton spécifié dans une barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="e8963-105">Retrieves information about the specified button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="e8963-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e8963-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8963-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e8963-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e8963-108">Index de base zéro du bouton pour lequel des informations doivent être récupérées.</span><span class="sxs-lookup"><span data-stu-id="e8963-108">Zero-based index of the button for which to retrieve information.</span></span>

</dd> <dt>

<span data-ttu-id="e8963-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e8963-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e8963-110">Pointeur vers la structure [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) qui reçoit les informations sur le bouton.</span><span class="sxs-lookup"><span data-stu-id="e8963-110">Pointer to the [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure that receives the button information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8963-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e8963-111">Return value</span></span>

<span data-ttu-id="e8963-112">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="e8963-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8963-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e8963-113">Requirements</span></span>



| <span data-ttu-id="e8963-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e8963-114">Requirement</span></span> | <span data-ttu-id="e8963-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="e8963-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e8963-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e8963-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e8963-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e8963-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e8963-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e8963-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e8963-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e8963-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e8963-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="e8963-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8963-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8963-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





