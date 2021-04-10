---
title: Message RB_GETBANDMARGINS (commctrl. h)
description: Récupère les marges d’une bande.
ms.assetid: 262f4180-53f9-428f-9360-75b762470270
keywords:
- RB_GETBANDMARGINS les contrôles de message Windows
topic_type:
- apiref
api_name:
- RB_GETBANDMARGINS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51ab77c057073d9816d1310b1e8cb39fd374956b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942459"
---
# <a name="rb_getbandmargins-message"></a><span data-ttu-id="7e693-104">\_Message GETBANDMARGINS RB</span><span class="sxs-lookup"><span data-stu-id="7e693-104">RB\_GETBANDMARGINS message</span></span>

<span data-ttu-id="7e693-105">Récupère les marges d’une bande.</span><span class="sxs-lookup"><span data-stu-id="7e693-105">Retrieves the margins of a band.</span></span>

## <a name="parameters"></a><span data-ttu-id="7e693-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7e693-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e693-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7e693-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="7e693-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="7e693-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="7e693-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7e693-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7e693-110">Pointeur vers une structure de [**marges**](/windows/desktop/api/Uxtheme/ns-uxtheme-margins) qui reçoit les marges récupérées.</span><span class="sxs-lookup"><span data-stu-id="7e693-110">Pointer to a [**MARGINS**](/windows/desktop/api/Uxtheme/ns-uxtheme-margins) structure that receives the retrieved margins.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e693-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7e693-111">Return value</span></span>

<span data-ttu-id="7e693-112">La valeur de retour n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="7e693-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e693-113">Notes</span><span class="sxs-lookup"><span data-stu-id="7e693-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7e693-114">Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="7e693-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="7e693-115">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7e693-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7e693-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7e693-116">Requirements</span></span>



| <span data-ttu-id="7e693-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7e693-117">Requirement</span></span> | <span data-ttu-id="7e693-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="7e693-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7e693-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e693-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7e693-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7e693-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7e693-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e693-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7e693-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7e693-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7e693-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="7e693-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e693-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e693-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





