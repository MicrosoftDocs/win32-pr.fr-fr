---
title: Message BM_SETDONTCLICK (winuser. h)
description: Définit un indicateur sur une case d’option qui contrôle la génération de \_ messages sur lesquels un clic a été effectué lorsque le bouton reçoit le focus.
ms.assetid: 91d98bce-abea-4afc-a995-0f426ba7a518
keywords:
- BM_SETDONTCLICK les contrôles de message Windows
topic_type:
- apiref
api_name:
- BM_SETDONTCLICK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8596ec679ff07b87b3433d5b5a7805698f56f84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513583"
---
# <a name="bm_setdontclick-message"></a><span data-ttu-id="87c5b-104">\_Message SETDONTCLICK BM</span><span class="sxs-lookup"><span data-stu-id="87c5b-104">BM\_SETDONTCLICK message</span></span>

<span data-ttu-id="87c5b-105">Définit un indicateur sur une case d’option qui contrôle la génération de messages [ \_ sur lesquels un clic a été effectué](bn-clicked.md) lorsque le bouton reçoit le focus.</span><span class="sxs-lookup"><span data-stu-id="87c5b-105">Sets a flag on a radio button that controls the generation of [BN\_CLICKED](bn-clicked.md) messages when the button receives focus.</span></span>

## <a name="parameters"></a><span data-ttu-id="87c5b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87c5b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87c5b-107">*wParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="87c5b-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87c5b-108">Valeur **booléenne** qui spécifie l’État.</span><span class="sxs-lookup"><span data-stu-id="87c5b-108">A **BOOL** that specifies the state.</span></span> <span data-ttu-id="87c5b-109">**True** pour définir l’indicateur, sinon **false**.</span><span class="sxs-lookup"><span data-stu-id="87c5b-109">**TRUE** to set the flag, otherwise **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="87c5b-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="87c5b-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="87c5b-111">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="87c5b-111">Not used.</span></span> <span data-ttu-id="87c5b-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="87c5b-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87c5b-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="87c5b-113">Return value</span></span>

<span data-ttu-id="87c5b-114">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="87c5b-114">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="87c5b-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="87c5b-115">Requirements</span></span>



| <span data-ttu-id="87c5b-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="87c5b-116">Requirement</span></span> | <span data-ttu-id="87c5b-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="87c5b-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87c5b-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87c5b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="87c5b-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="87c5b-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="87c5b-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87c5b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="87c5b-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="87c5b-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="87c5b-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="87c5b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="87c5b-123"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="87c5b-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 





