---
title: Message TB_MAPACCELERATOR (commctrl. h)
description: Détermine l’ID du bouton qui correspond au caractère d’accélérateur spécifié.
ms.assetid: 724b593d-39af-4301-b721-0332844677b1
keywords:
- TB_MAPACCELERATOR les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_MAPACCELERATOR
- TB_MAPACCELERATORA
- TB_MAPACCELERATORW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 029584d9e1614a3a135da5ebd3f4f446795fd9ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742660"
---
# <a name="tb_mapaccelerator-message"></a><span data-ttu-id="f52e0-104">TO \_ MAPACCELERATOR message</span><span class="sxs-lookup"><span data-stu-id="f52e0-104">TB\_MAPACCELERATOR message</span></span>

<span data-ttu-id="f52e0-105">Détermine l’ID du bouton qui correspond au caractère d’accélérateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="f52e0-105">Determines the ID of the button that corresponds to the specified accelerator character.</span></span>

## <a name="parameters"></a><span data-ttu-id="f52e0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f52e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f52e0-107">*wParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f52e0-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f52e0-108">Caractère d’accélérateur.</span><span class="sxs-lookup"><span data-stu-id="f52e0-108">The accelerator character.</span></span>

</dd> <dt>

<span data-ttu-id="f52e0-109">*lParam* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f52e0-109">*lParam* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f52e0-110">Pointeur vers un **uint**.</span><span class="sxs-lookup"><span data-stu-id="f52e0-110">Pointer to a **UINT**.</span></span> <span data-ttu-id="f52e0-111">En cas de retour, en cas de réussite, ce paramètre contiendra l’ID du bouton avec *wParam* comme caractère d’accélérateur.</span><span class="sxs-lookup"><span data-stu-id="f52e0-111">On return, if successful, this parameter will hold the id of the button that has *wParam* as its accelerator character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f52e0-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f52e0-112">Return value</span></span>

<span data-ttu-id="f52e0-113">Retourne une valeur différente de zéro si l’un des boutons a *wParam* comme caractère d’accélérateur, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="f52e0-113">Returns a nonzero value if one of the buttons has *wParam* as its accelerator character, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="f52e0-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f52e0-114">Requirements</span></span>



| <span data-ttu-id="f52e0-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f52e0-115">Requirement</span></span> | <span data-ttu-id="f52e0-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="f52e0-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f52e0-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f52e0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f52e0-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f52e0-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f52e0-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f52e0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f52e0-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f52e0-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f52e0-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="f52e0-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f52e0-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f52e0-122"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="f52e0-123">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="f52e0-123">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f52e0-124">**To \_ MAPACCELERATORW** (Unicode) et **to \_ MAPACCELERATORA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f52e0-124">**TB\_MAPACCELERATORW** (Unicode) and **TB\_MAPACCELERATORA** (ANSI)</span></span><br/>       |



 

 





