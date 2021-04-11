---
title: Message IPM_GETADDRESS (commctrl. h)
description: Obtient les valeurs d’adresse pour les quatre champs dans le contrôle d’adresse IP.
ms.assetid: 4fe68d45-7d7f-46da-a110-65f899b3c393
keywords:
- IPM_GETADDRESS les contrôles de message Windows
topic_type:
- apiref
api_name:
- IPM_GETADDRESS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 426e9c76712701b2f4e108679133be23eb700687
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942384"
---
# <a name="ipm_getaddress-message"></a><span data-ttu-id="f632c-104">\_Message de message de message IPM</span><span class="sxs-lookup"><span data-stu-id="f632c-104">IPM\_GETADDRESS message</span></span>

<span data-ttu-id="f632c-105">Obtient les valeurs d’adresse pour les quatre champs dans le contrôle d’adresse IP.</span><span class="sxs-lookup"><span data-stu-id="f632c-105">Gets the address values for all four fields in the IP address control.</span></span>

## <a name="parameters"></a><span data-ttu-id="f632c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f632c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f632c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f632c-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f632c-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="f632c-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f632c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f632c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f632c-110">Pointeur vers une valeur **DWORD** qui reçoit l’adresse.</span><span class="sxs-lookup"><span data-stu-id="f632c-110">A pointer to a **DWORD** value that receives the address.</span></span> <span data-ttu-id="f632c-111">La valeur du champ 3 sera comprise entre bits 0 et 7.</span><span class="sxs-lookup"><span data-stu-id="f632c-111">The field 3 value will be contained in bits 0 through 7.</span></span> <span data-ttu-id="f632c-112">La valeur du champ 2 sera contenue dans les bits 8 à 15.</span><span class="sxs-lookup"><span data-stu-id="f632c-112">The field 2 value will be contained in bits 8 through 15.</span></span> <span data-ttu-id="f632c-113">La valeur du champ 1 est comprise entre les bits 16 et 23.</span><span class="sxs-lookup"><span data-stu-id="f632c-113">The field 1 value will be contained in bits 16 through 23.</span></span> <span data-ttu-id="f632c-114">La valeur du champ 0 sera contenue dans les bits de 24 à 31.</span><span class="sxs-lookup"><span data-stu-id="f632c-114">The field 0 value will be contained in bits 24 through 31.</span></span> <span data-ttu-id="f632c-115">Les [**premières \_**](/windows/desktop/api/Commctrl/nf-commctrl-first_ipaddress)macros IPAddress, [**second \_**](/windows/desktop/api/Commctrl/nf-commctrl-second_ipaddress)IPAddress, [**troisième \_ IPAddress**](/windows/desktop/api/Commctrl/nf-commctrl-third_ipaddress)et quatrième sont également utilisables pour extraire les informations d’adresse. [**\_**](/windows/desktop/api/Commctrl/nf-commctrl-fourth_ipaddress)</span><span class="sxs-lookup"><span data-stu-id="f632c-115">The [**FIRST\_IPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-first_ipaddress), [**SECOND\_IPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-second_ipaddress), [**THIRD\_IPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-third_ipaddress), and [**FOURTH\_IPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-fourth_ipaddress) macros can also be used to extract the address information.</span></span> <span data-ttu-id="f632c-116">La valeur zéro est renvoyée en tant qu’adresse pour tous les champs vides.</span><span class="sxs-lookup"><span data-stu-id="f632c-116">Zero will be returned as the address for any blank fields.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f632c-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f632c-117">Return value</span></span>

<span data-ttu-id="f632c-118">Retourne le nombre de champs non vides.</span><span class="sxs-lookup"><span data-stu-id="f632c-118">Returns the number of nonblank fields.</span></span>

## <a name="requirements"></a><span data-ttu-id="f632c-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f632c-119">Requirements</span></span>



| <span data-ttu-id="f632c-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f632c-120">Requirement</span></span> | <span data-ttu-id="f632c-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="f632c-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f632c-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f632c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f632c-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f632c-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f632c-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f632c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f632c-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f632c-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f632c-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="f632c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f632c-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f632c-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





