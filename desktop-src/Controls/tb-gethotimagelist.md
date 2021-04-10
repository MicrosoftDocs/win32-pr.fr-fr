---
title: Message TB_GETHOTIMAGELIST (commctrl. h)
description: Récupère la liste d’images utilisée par un contrôle de barre d’outils pour afficher les boutons actifs.
ms.assetid: 63054449-2768-459c-933c-781d31bdcc15
keywords:
- TB_GETHOTIMAGELIST les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_GETHOTIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e19c1f3989b0d749a9c663d00b5fb7b54d67fc0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104029"
---
# <a name="tb_gethotimagelist-message"></a><span data-ttu-id="89943-104">TO \_ GETHOTIMAGELIST message</span><span class="sxs-lookup"><span data-stu-id="89943-104">TB\_GETHOTIMAGELIST message</span></span>

<span data-ttu-id="89943-105">Récupère la liste d’images utilisée par un contrôle de barre d’outils pour afficher les boutons actifs.</span><span class="sxs-lookup"><span data-stu-id="89943-105">Retrieves the image list that a toolbar control uses to display hot buttons.</span></span>

## <a name="parameters"></a><span data-ttu-id="89943-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="89943-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89943-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="89943-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="89943-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="89943-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="89943-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="89943-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="89943-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="89943-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89943-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="89943-111">Return value</span></span>

<span data-ttu-id="89943-112">Retourne le handle de la liste d’images que le contrôle utilise pour afficher les boutons actifs, ou **null** si aucune liste d’images réactives n’est définie.</span><span class="sxs-lookup"><span data-stu-id="89943-112">Returns the handle to the image list that the control uses to display hot buttons, or **NULL** if no hot image list is set.</span></span>

## <a name="remarks"></a><span data-ttu-id="89943-113">Notes</span><span class="sxs-lookup"><span data-stu-id="89943-113">Remarks</span></span>

<span data-ttu-id="89943-114">Un bouton est actif lorsque le curseur se trouve sur celui-ci.</span><span class="sxs-lookup"><span data-stu-id="89943-114">A button is hot when the cursor is over it.</span></span> <span data-ttu-id="89943-115">Les contrôles ToolBar doivent avoir le style de [**\_ liste**](toolbar-control-and-button-styles.md) [**TBSTYLE \_ plat**](toolbar-control-and-button-styles.md) ou TBSTYLE pour avoir des éléments chauds.</span><span class="sxs-lookup"><span data-stu-id="89943-115">Toolbar controls must have the [**TBSTYLE\_FLAT**](toolbar-control-and-button-styles.md) or [**TBSTYLE\_LIST**](toolbar-control-and-button-styles.md) style to have hot items.</span></span>

## <a name="requirements"></a><span data-ttu-id="89943-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="89943-116">Requirements</span></span>



| <span data-ttu-id="89943-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="89943-117">Requirement</span></span> | <span data-ttu-id="89943-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="89943-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="89943-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="89943-119">Minimum supported client</span></span><br/> | <span data-ttu-id="89943-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="89943-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="89943-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="89943-121">Minimum supported server</span></span><br/> | <span data-ttu-id="89943-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="89943-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="89943-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="89943-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="89943-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="89943-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





