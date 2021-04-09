---
title: Message TB_GETITEMDROPDOWNRECT (commctrl. h)
description: Obtient le rectangle englobant de la fenêtre déroulante pour un élément de barre d’outils avec une \_ liste déroulante BTNS style.
ms.assetid: 4b59c96b-8d75-44c1-b771-c1d62502a2c2
keywords:
- TB_GETITEMDROPDOWNRECT les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_GETITEMDROPDOWNRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbcbcef725b0ade0bfc776200fa5b191618d2ccb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032483"
---
# <a name="tb_getitemdropdownrect-message"></a><span data-ttu-id="0671a-104">TO \_ GETITEMDROPDOWNRECT message</span><span class="sxs-lookup"><span data-stu-id="0671a-104">TB\_GETITEMDROPDOWNRECT message</span></span>

<span data-ttu-id="0671a-105">Obtient le rectangle englobant de la fenêtre déroulante pour un élément de barre d’outils avec une [**\_ liste déroulante BTNS**](toolbar-control-and-button-styles.md)style.</span><span class="sxs-lookup"><span data-stu-id="0671a-105">Gets the bounding rectangle of the dropdown window for a toolbar item with style [**BTNS\_DROPDOWN**](toolbar-control-and-button-styles.md).</span></span>

## <a name="parameters"></a><span data-ttu-id="0671a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0671a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0671a-107">*wParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0671a-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0671a-108">Index de base zéro de l’élément de contrôle de barre d’outils pour lequel récupérer le rectangle englobant.</span><span class="sxs-lookup"><span data-stu-id="0671a-108">The zero-based index of the toolbar control item for which to retrieve the bounding rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="0671a-109">*lParam* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="0671a-109">*lParam* \[in, out\]</span></span>
</dt> <dd><span data-ttu-id="0671a-110">Pointeur vers une structure <a href="/previous-versions//dd162897(v=vs.85)">**Rect**</a> pour recevoir les informations de rectangle englobant.</span><span class="sxs-lookup"><span data-stu-id="0671a-110">A pointer to a <a href="/previous-versions//dd162897(v=vs.85)">**RECT**</a> structure to receive the bounding rectangle information.</span></span> <span data-ttu-id="0671a-111">L’expéditeur du message est chargé d’allouer cette structure.</span><span class="sxs-lookup"><span data-stu-id="0671a-111">The message sender is responsible for allocating this structure.</span></span> <span data-ttu-id="0671a-112">Les coordonnées retournées dans la structure **Rect** sont exprimées en tant que coordonnées clientes.</span><span class="sxs-lookup"><span data-stu-id="0671a-112">The coordinates returned in the **RECT** structure are expressed as client coordinates.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0671a-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0671a-113">Return value</span></span>

<span data-ttu-id="0671a-114">Retourne toujours une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="0671a-114">Always returns nonzero.</span></span>

## <a name="remarks"></a><span data-ttu-id="0671a-115">Notes</span><span class="sxs-lookup"><span data-stu-id="0671a-115">Remarks</span></span>

<span data-ttu-id="0671a-116">L’élément doit avoir le style de [**\_ liste déroulante BTNS**](toolbar-control-and-button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="0671a-116">The item must have the [**BTNS\_DROPDOWN**](toolbar-control-and-button-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="0671a-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0671a-117">Requirements</span></span>



| <span data-ttu-id="0671a-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0671a-118">Requirement</span></span> | <span data-ttu-id="0671a-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="0671a-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0671a-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0671a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0671a-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0671a-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0671a-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0671a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0671a-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0671a-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0671a-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="0671a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0671a-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0671a-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

