---
title: Message TB_SETHOTIMAGELIST (commctrl. h)
description: Définit la liste d’images que le contrôle ToolBar utilisera pour afficher les boutons actifs.
ms.assetid: 3c29cdde-bd57-4194-984f-220dbf963733
keywords:
- TB_SETHOTIMAGELIST les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_SETHOTIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9a84c3420eaf64710ac1f8764db20d2cfc88b7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942536"
---
# <a name="tb_sethotimagelist-message"></a><span data-ttu-id="488d3-104">TO \_ SETHOTIMAGELIST message</span><span class="sxs-lookup"><span data-stu-id="488d3-104">TB\_SETHOTIMAGELIST message</span></span>

<span data-ttu-id="488d3-105">Définit la liste d’images que le contrôle ToolBar utilisera pour afficher les boutons actifs.</span><span class="sxs-lookup"><span data-stu-id="488d3-105">Sets the image list that the toolbar control will use to display hot buttons.</span></span>

## <a name="parameters"></a><span data-ttu-id="488d3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="488d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="488d3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="488d3-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="488d3-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="488d3-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="488d3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="488d3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="488d3-110">Handle de la liste d’images qui sera définie.</span><span class="sxs-lookup"><span data-stu-id="488d3-110">Handle to the image list that will be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="488d3-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="488d3-111">Return value</span></span>

<span data-ttu-id="488d3-112">Retourne le handle de la liste d’images utilisée précédemment pour afficher les boutons actifs, ou **null** si aucune liste d’images n’a été définie précédemment.</span><span class="sxs-lookup"><span data-stu-id="488d3-112">Returns the handle to the image list previously used to display hot buttons, or **NULL** if no image list was previously set.</span></span>

## <a name="remarks"></a><span data-ttu-id="488d3-113">Notes</span><span class="sxs-lookup"><span data-stu-id="488d3-113">Remarks</span></span>

<span data-ttu-id="488d3-114">Un bouton est actif lorsque le curseur se trouve sur celui-ci.</span><span class="sxs-lookup"><span data-stu-id="488d3-114">A button is hot when the cursor is over it.</span></span> <span data-ttu-id="488d3-115">Les contrôles ToolBar doivent avoir le style de [**\_ liste**](toolbar-control-and-button-styles.md) [**TBSTYLE \_ plat**](toolbar-control-and-button-styles.md) ou TBSTYLE pour avoir des éléments chauds.</span><span class="sxs-lookup"><span data-stu-id="488d3-115">Toolbar controls must have the [**TBSTYLE\_FLAT**](toolbar-control-and-button-styles.md) or [**TBSTYLE\_LIST**](toolbar-control-and-button-styles.md) style to have hot items.</span></span>

## <a name="requirements"></a><span data-ttu-id="488d3-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="488d3-116">Requirements</span></span>



| <span data-ttu-id="488d3-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="488d3-117">Requirement</span></span> | <span data-ttu-id="488d3-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="488d3-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="488d3-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="488d3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="488d3-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="488d3-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="488d3-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="488d3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="488d3-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="488d3-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="488d3-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="488d3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="488d3-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="488d3-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





