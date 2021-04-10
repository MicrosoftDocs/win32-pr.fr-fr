---
title: Message LVM_SETSELECTEDCOLUMN (commctrl. h)
description: Définit l’index de la colonne sélectionnée.
ms.assetid: 11b0838e-24a7-4c1c-b67d-0912b5a6442a
keywords:
- LVM_SETSELECTEDCOLUMN les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_SETSELECTEDCOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 827c41fabaea722bb2372c6bd3f7c3a54bee92f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844486"
---
# <a name="lvm_setselectedcolumn-message"></a><span data-ttu-id="ce6df-104">\_Message SETSELECTEDCOLUMN LVM</span><span class="sxs-lookup"><span data-stu-id="ce6df-104">LVM\_SETSELECTEDCOLUMN message</span></span>

<span data-ttu-id="ce6df-105">Définit l’index de la colonne sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="ce6df-105">Sets the index of the selected column.</span></span>

## <a name="parameters"></a><span data-ttu-id="ce6df-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ce6df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce6df-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ce6df-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ce6df-108">Valeur de type **int** qui spécifie l’index de colonne.</span><span class="sxs-lookup"><span data-stu-id="ce6df-108">Value of type **int** that specifies the column index.</span></span></dd> <dt>

<span data-ttu-id="ce6df-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ce6df-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ce6df-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="ce6df-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce6df-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ce6df-111">Return value</span></span>

<span data-ttu-id="ce6df-112">La valeur de retour n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="ce6df-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce6df-113">Notes</span><span class="sxs-lookup"><span data-stu-id="ce6df-113">Remarks</span></span>

<span data-ttu-id="ce6df-114">Les index de colonne sont stockés dans un tableau **int** .</span><span class="sxs-lookup"><span data-stu-id="ce6df-114">The column indices are stored in an **int** array.</span></span> <span data-ttu-id="ce6df-115">Consultez le membre **puColumns** de [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema).</span><span class="sxs-lookup"><span data-stu-id="ce6df-115">See the **puColumns** member of [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema).</span></span>

> [!Note]  
> <span data-ttu-id="ce6df-116">Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="ce6df-116">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="ce6df-117">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ce6df-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ce6df-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ce6df-118">Requirements</span></span>



| <span data-ttu-id="ce6df-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ce6df-119">Requirement</span></span> | <span data-ttu-id="ce6df-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="ce6df-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ce6df-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ce6df-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ce6df-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ce6df-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ce6df-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ce6df-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ce6df-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ce6df-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ce6df-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="ce6df-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce6df-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce6df-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





