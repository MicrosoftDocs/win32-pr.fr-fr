---
title: Message SB_SETBKCOLOR (commctrl. h)
description: Définit la couleur d’arrière-plan dans une barre d’État.
ms.assetid: 49bcd816-e3e2-45f4-8845-ef67789b8a01
keywords:
- SB_SETBKCOLOR les contrôles de message Windows
topic_type:
- apiref
api_name:
- SB_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc08687c6d228074bc3e4dd7c8442a1c1e35a835
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385064"
---
# <a name="sb_setbkcolor-message"></a><span data-ttu-id="92e33-104">\_Message SB SETBKCOLOR</span><span class="sxs-lookup"><span data-stu-id="92e33-104">SB\_SETBKCOLOR message</span></span>

<span data-ttu-id="92e33-105">Définit la couleur d’arrière-plan dans une barre d’État.</span><span class="sxs-lookup"><span data-stu-id="92e33-105">Sets the background color in a status bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="92e33-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="92e33-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92e33-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="92e33-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="92e33-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="92e33-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="92e33-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="92e33-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="92e33-110">Valeur [**COLORREF**](/windows/desktop/gdi/colorref) qui spécifie la nouvelle couleur d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="92e33-110">[**COLORREF**](/windows/desktop/gdi/colorref) value that specifies the new background color.</span></span> <span data-ttu-id="92e33-111">Spécifiez la \_ valeur CLR par défaut pour faire en sorte que la barre d’État utilise sa couleur d’arrière-plan par défaut.</span><span class="sxs-lookup"><span data-stu-id="92e33-111">Specify the CLR\_DEFAULT value to cause the status bar to use its default background color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92e33-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="92e33-112">Return value</span></span>

<span data-ttu-id="92e33-113">Retourne la couleur d’arrière-plan précédente ou la \_ valeur CLR par défaut si la couleur d’arrière-plan est la couleur par défaut.</span><span class="sxs-lookup"><span data-stu-id="92e33-113">Returns the previous background color, or CLR\_DEFAULT if the background color is the default color.</span></span>

## <a name="requirements"></a><span data-ttu-id="92e33-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="92e33-114">Requirements</span></span>



| <span data-ttu-id="92e33-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="92e33-115">Requirement</span></span> | <span data-ttu-id="92e33-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="92e33-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="92e33-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="92e33-117">Minimum supported client</span></span><br/> | <span data-ttu-id="92e33-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="92e33-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="92e33-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="92e33-119">Minimum supported server</span></span><br/> | <span data-ttu-id="92e33-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="92e33-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="92e33-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="92e33-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="92e33-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="92e33-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

