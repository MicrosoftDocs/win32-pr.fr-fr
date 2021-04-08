---
title: Message TB_SETLISTGAP (commctrl. h)
description: Définit la distance entre les boutons de la barre d’outils dans une barre d’outils spécifique.
ms.assetid: ca8ba6e4-cf70-41ca-ac61-cd13671d4010
keywords:
- TB_SETLISTGAP les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_SETLISTGAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 224a709b7beefcfdf49ea7838f905977487aca8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843053"
---
# <a name="tb_setlistgap-message"></a><span data-ttu-id="b6b02-104">TO \_ SETLISTGAP message</span><span class="sxs-lookup"><span data-stu-id="b6b02-104">TB\_SETLISTGAP message</span></span>

<span data-ttu-id="b6b02-105">Définit la distance entre les boutons de la barre d’outils dans une barre d’outils spécifique.</span><span class="sxs-lookup"><span data-stu-id="b6b02-105">Sets the distance between the toolbar buttons on a specific toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="b6b02-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b6b02-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6b02-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b6b02-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b6b02-108">Intervalle, en pixels, entre les boutons de la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="b6b02-108">The gap, in pixels, between buttons on the toolbar.</span></span>

</dd> <dt>

<span data-ttu-id="b6b02-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b6b02-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b6b02-110">Ignoré.</span><span class="sxs-lookup"><span data-stu-id="b6b02-110">Ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6b02-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b6b02-111">Return value</span></span>

<span data-ttu-id="b6b02-112">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="b6b02-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6b02-113">Notes</span><span class="sxs-lookup"><span data-stu-id="b6b02-113">Remarks</span></span>

<span data-ttu-id="b6b02-114">L’intervalle entre les boutons s’applique uniquement à la fenêtre de contrôle de barre d’outils qui reçoit ce message.</span><span class="sxs-lookup"><span data-stu-id="b6b02-114">The gap between buttons only applies to the toolbar control window that receives this message.</span></span> <span data-ttu-id="b6b02-115">La réception de ce message déclenche une redessine de la barre d’outils, si la barre d’outils est actuellement visible.</span><span class="sxs-lookup"><span data-stu-id="b6b02-115">Receipt of this message triggers a repaint of the toolbar, if the toolbar is currently visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6b02-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b6b02-116">Requirements</span></span>



| <span data-ttu-id="b6b02-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b6b02-117">Requirement</span></span> | <span data-ttu-id="b6b02-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="b6b02-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b6b02-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b6b02-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b6b02-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b6b02-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b6b02-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b6b02-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b6b02-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b6b02-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b6b02-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="b6b02-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6b02-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6b02-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





