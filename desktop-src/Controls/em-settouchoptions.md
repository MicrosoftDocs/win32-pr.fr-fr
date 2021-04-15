---
title: Message EM_SETTOUCHOPTIONS (RichEdit. h)
description: Définit les options tactiles associées à un contrôle RichEdit.
ms.assetid: C15036D6-B74F-414D-B731-F1587B616644
keywords:
- EM_SETTOUCHOPTIONS les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETTOUCHOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7613679a574955ef726da9fa10e8d919c8fe53b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465702"
---
# <a name="em_settouchoptions-message"></a><span data-ttu-id="777d8-104">\_Message SETTOUCHOPTIONS em</span><span class="sxs-lookup"><span data-stu-id="777d8-104">EM\_SETTOUCHOPTIONS message</span></span>

<span data-ttu-id="777d8-105">Définit les options tactiles associées à un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="777d8-105">Sets the touch options associated with a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="777d8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="777d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="777d8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="777d8-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="777d8-108">Option Touch à définir.</span><span class="sxs-lookup"><span data-stu-id="777d8-108">The touch option to set.</span></span> <span data-ttu-id="777d8-109">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="777d8-109">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="777d8-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="777d8-110">Value</span></span>                                                                                                                                                                        | <span data-ttu-id="777d8-111">Signification</span><span class="sxs-lookup"><span data-stu-id="777d8-111">Meaning</span></span>                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTO_SHOWHANDLES"></span><span id="rto_showhandles"></span><dl> <span data-ttu-id="777d8-112"><dt>**RTO \_ SHOWHANDLES**</dt></span><span class="sxs-lookup"><span data-stu-id="777d8-112"><dt>**RTO\_SHOWHANDLES**</dt></span></span> </dl>          | <span data-ttu-id="777d8-113">Affichez ou masquez les poignées de la pince tactile, en fonction de la valeur de *lParam*.</span><span class="sxs-lookup"><span data-stu-id="777d8-113">Show or hide the touch gripper handles, depending on the value of *lParam*.</span></span><br/>                                                                                                                                                       |
| <span id="RTO_DISABLEHANDLES"></span><span id="rto_disablehandles"></span><dl> <span data-ttu-id="777d8-114"><dt>**RTO \_ DISABLEHANDLES**</dt></span><span class="sxs-lookup"><span data-stu-id="777d8-114"><dt>**RTO\_DISABLEHANDLES**</dt></span></span> </dl> | <span data-ttu-id="777d8-115">Activez ou désactivez les handles de la pince tactile, en fonction de la valeur de *lParam*.</span><span class="sxs-lookup"><span data-stu-id="777d8-115">Enable or disable the touch gripper handles, depending on the value of *lParam*.</span></span> <span data-ttu-id="777d8-116">Lorsque les descripteurs sont désactivés, ils sont masqués s’ils sont visibles et restent masqués jusqu’à ce qu’un message **\_ SETTOUCHOPTIONS em** change leur état.</span><span class="sxs-lookup"><span data-stu-id="777d8-116">When handles are disabled, they are hidden if they are visible and remain hidden until an **EM\_SETTOUCHOPTIONS** message changes their status.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="777d8-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="777d8-117">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="777d8-118">Affectez la valeur **true** pour afficher/activer les poignées de sélection tactile, ou **false** pour masquer/désactiver les poignées de sélection tactile.</span><span class="sxs-lookup"><span data-stu-id="777d8-118">Set to **TRUE** to show/enable the touch selection handles, or **FALSE** to hide/disable the touch selection handles.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="777d8-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="777d8-119">Return value</span></span>

<span data-ttu-id="777d8-120">Ce message retourne la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="777d8-120">This message returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="777d8-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="777d8-121">Requirements</span></span>



| <span data-ttu-id="777d8-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="777d8-122">Requirement</span></span> | <span data-ttu-id="777d8-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="777d8-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="777d8-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="777d8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="777d8-125">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="777d8-125">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="777d8-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="777d8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="777d8-127">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="777d8-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="777d8-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="777d8-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="777d8-129"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="777d8-129"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="777d8-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="777d8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="777d8-131">**\_GETTOUCHOPTIONS em**</span><span class="sxs-lookup"><span data-stu-id="777d8-131">**EM\_GETTOUCHOPTIONS**</span></span>](em-settouchoptions.md)
</dt> </dl>

 

 





