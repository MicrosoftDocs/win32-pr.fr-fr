---
title: Message IPM_SETADDRESS (commctrl. h)
description: Définit les valeurs d’adresse pour les quatre champs dans le contrôle d’adresse IP.
ms.assetid: 52e72437-3558-4789-844f-5ab5b0b7967c
keywords:
- IPM_SETADDRESS les contrôles de message Windows
topic_type:
- apiref
api_name:
- IPM_SETADDRESS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8e8e4fa69791f93094d24f990ad62207cad33dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104464"
---
# <a name="ipm_setaddress-message"></a><span data-ttu-id="413b4-104">\_Message SETADDRESS IPM</span><span class="sxs-lookup"><span data-stu-id="413b4-104">IPM\_SETADDRESS message</span></span>

<span data-ttu-id="413b4-105">Définit les valeurs d’adresse pour les quatre champs dans le contrôle d’adresse IP.</span><span class="sxs-lookup"><span data-stu-id="413b4-105">Sets the address values for all four fields in the IP address control.</span></span>

## <a name="parameters"></a><span data-ttu-id="413b4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="413b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="413b4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="413b4-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="413b4-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="413b4-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="413b4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="413b4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="413b4-110">Valeur **DWORD** qui contient la nouvelle adresse.</span><span class="sxs-lookup"><span data-stu-id="413b4-110">A **DWORD** value that contains the new address.</span></span> <span data-ttu-id="413b4-111">La valeur du champ 3 est comprise entre bits 0 et 7.</span><span class="sxs-lookup"><span data-stu-id="413b4-111">The field 3 value is contained in bits 0 through 7.</span></span> <span data-ttu-id="413b4-112">La valeur du champ 2 est comprise entre bits 8 et 15.</span><span class="sxs-lookup"><span data-stu-id="413b4-112">The field 2 value is contained in bits 8 through 15.</span></span> <span data-ttu-id="413b4-113">La valeur du champ 1 est comprise entre les bits 16 et 23.</span><span class="sxs-lookup"><span data-stu-id="413b4-113">The field 1 value is contained in bits 16 through 23.</span></span> <span data-ttu-id="413b4-114">La valeur du champ 0 est comprise entre bits 24 et 31.</span><span class="sxs-lookup"><span data-stu-id="413b4-114">The field 0 value is contained in bits 24 through 31.</span></span> <span data-ttu-id="413b4-115">La macro [**MAKEIPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-makeipaddress) peut également être utilisée pour créer les informations d’adresse.</span><span class="sxs-lookup"><span data-stu-id="413b4-115">The [**MAKEIPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-makeipaddress) macro can also be used to create the address information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="413b4-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="413b4-116">Return value</span></span>

<span data-ttu-id="413b4-117">La valeur de retour n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="413b4-117">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="413b4-118">Notes</span><span class="sxs-lookup"><span data-stu-id="413b4-118">Remarks</span></span>

<span data-ttu-id="413b4-119">Ce message ne génère pas de notification [**IPN \_ FIELDCHANGED**](ipn-fieldchanged.md) .</span><span class="sxs-lookup"><span data-stu-id="413b4-119">This message does not generate an [**IPN\_FIELDCHANGED**](ipn-fieldchanged.md) notification.</span></span>

## <a name="requirements"></a><span data-ttu-id="413b4-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="413b4-120">Requirements</span></span>



| <span data-ttu-id="413b4-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="413b4-121">Requirement</span></span> | <span data-ttu-id="413b4-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="413b4-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="413b4-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="413b4-123">Minimum supported client</span></span><br/> | <span data-ttu-id="413b4-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="413b4-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="413b4-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="413b4-125">Minimum supported server</span></span><br/> | <span data-ttu-id="413b4-126">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="413b4-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="413b4-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="413b4-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="413b4-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="413b4-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





