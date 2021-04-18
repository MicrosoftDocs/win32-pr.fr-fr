---
title: Message LVM_SETINFOTIP (commctrl. h)
description: Définit le texte info-bulle en réponse différée à la \_ notification LVN GETINFOTIP.
ms.assetid: 3dbf6a9a-52ec-4619-9c70-041e75942e20
keywords:
- LVM_SETINFOTIP les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_SETINFOTIP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90827766a6f1218dbbd631ed4eaf6b2989257944
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512776"
---
# <a name="lvm_setinfotip-message"></a><span data-ttu-id="c2e68-104">\_Message SETINFOTIP LVM</span><span class="sxs-lookup"><span data-stu-id="c2e68-104">LVM\_SETINFOTIP message</span></span>

<span data-ttu-id="c2e68-105">Définit le texte info-bulle en réponse différée à la notification [LVN \_ GETINFOTIP](lvn-getinfotip.md) .</span><span class="sxs-lookup"><span data-stu-id="c2e68-105">Sets tooltip text in delayed response to the [LVN\_GETINFOTIP](lvn-getinfotip.md) notification.</span></span>

## <a name="parameters"></a><span data-ttu-id="c2e68-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c2e68-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2e68-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c2e68-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c2e68-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="c2e68-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c2e68-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c2e68-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c2e68-110">Pointeur vers une structure <a href="/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip">LVSETINFOTIP</a> qui contient les informations à définir.</span><span class="sxs-lookup"><span data-stu-id="c2e68-110">Pointer to a <a href="/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip">LVSETINFOTIP</a> structure that contains the information to set.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2e68-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c2e68-111">Return value</span></span>

<span data-ttu-id="c2e68-112">Retourne la **valeur true** si le texte de l’info-bulle est correctement défini, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="c2e68-112">Returns **TRUE** if the tooltip text is set successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2e68-113">Notes</span><span class="sxs-lookup"><span data-stu-id="c2e68-113">Remarks</span></span>

<span data-ttu-id="c2e68-114">Le **message \_ SETINFOTIP LVM** permet à une application de calculer info-bulles en arrière-plan en effectuant les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="c2e68-114">The **LVM\_SETINFOTIP** message lets an application calculate infotips in the background by performing the following steps:</span></span>

1.  <span data-ttu-id="c2e68-115">En réponse à la notification [LVN \_ GETINFOTIP](lvn-getinfotip.md) , définissez le membre **PszText** de la structure [**NMLVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmlvgetinfotipa) sur une chaîne vide et retournez 0.</span><span class="sxs-lookup"><span data-stu-id="c2e68-115">In response to the [LVN\_GETINFOTIP](lvn-getinfotip.md) notification, set the **pszText** member of the [**NMLVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmlvgetinfotipa) structure to an empty string and return 0.</span></span>
2.  <span data-ttu-id="c2e68-116">En arrière-plan, calculez l’info-bulle.</span><span class="sxs-lookup"><span data-stu-id="c2e68-116">In the background, compute the infotip.</span></span>
3.  <span data-ttu-id="c2e68-117">Après le calcul de l’info-bulle, envoyez le message **\_ SETINFOTIP LVM** , en définissant le membre **PszText** de la structure [**LVSETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip) sur l’info-bulle et les membres **iItem** et **iSubItem** sur l’élément et le sous-élément auxquels s’applique l’info-bulle.</span><span class="sxs-lookup"><span data-stu-id="c2e68-117">After computing the infotip, send the **LVM\_SETINFOTIP** message, setting the **pszText** member of the [**LVSETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip) structure to the infotip and the **iItem** and **iSubItem** members to the item and sub-item to which the infotip applies.</span></span>

<span data-ttu-id="c2e68-118">Le texte transmis au message **LVM \_ SETINFOTIP** s’affiche uniquement si l’élément et le sous-élément décrits par la structure [**LVSETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip) sont toujours dans un État qui requiert une info-bulle</span><span class="sxs-lookup"><span data-stu-id="c2e68-118">The text passed to the **LVM\_SETINFOTIP** message appears only if the item and sub-item described by the [**LVSETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip) structure are still in a state that requires an infotip</span></span>

> [!Note]  
> <span data-ttu-id="c2e68-119">Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="c2e68-119">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="c2e68-120">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c2e68-120">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c2e68-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c2e68-121">Requirements</span></span>



| <span data-ttu-id="c2e68-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c2e68-122">Requirement</span></span> | <span data-ttu-id="c2e68-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2e68-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c2e68-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2e68-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c2e68-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c2e68-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c2e68-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2e68-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c2e68-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c2e68-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c2e68-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="c2e68-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2e68-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2e68-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





