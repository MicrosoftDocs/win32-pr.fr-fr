---
title: Message LVM_GETSELECTEDCOLUMN (commctrl. h)
description: Récupère un entier qui spécifie la colonne sélectionnée.
ms.assetid: 5aba5d96-50fd-439b-9782-fd5d8684b17f
keywords:
- LVM_GETSELECTEDCOLUMN les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETSELECTEDCOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24ffae9a9c7812f025241f5b46f3b1ea61bb88bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317377"
---
# <a name="lvm_getselectedcolumn-message"></a><span data-ttu-id="7148d-104">\_Message GETSELECTEDCOLUMN LVM</span><span class="sxs-lookup"><span data-stu-id="7148d-104">LVM\_GETSELECTEDCOLUMN message</span></span>

<span data-ttu-id="7148d-105">Récupère un entier qui spécifie la colonne sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="7148d-105">Retrieves an integer that specifies the selected column.</span></span>

## <a name="parameters"></a><span data-ttu-id="7148d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7148d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7148d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7148d-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="7148d-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="7148d-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="7148d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7148d-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="7148d-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="7148d-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7148d-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7148d-111">Return value</span></span>

<span data-ttu-id="7148d-112">Retourne un **uint** qui spécifie la colonne sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="7148d-112">Returns an **UINT** that specifies the selected column.</span></span>

## <a name="remarks"></a><span data-ttu-id="7148d-113">Notes</span><span class="sxs-lookup"><span data-stu-id="7148d-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7148d-114">Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="7148d-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="7148d-115">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7148d-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7148d-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7148d-116">Requirements</span></span>



| <span data-ttu-id="7148d-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7148d-117">Requirement</span></span> | <span data-ttu-id="7148d-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="7148d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7148d-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7148d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7148d-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7148d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7148d-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7148d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7148d-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7148d-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7148d-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="7148d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7148d-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7148d-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





