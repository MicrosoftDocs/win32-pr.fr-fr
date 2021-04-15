---
title: Message PSM_REBOOTSYSTEM (Prsht. h)
description: Indique que le système doit être redémarré pour que les modifications prennent effet. Vous pouvez envoyer le \_ message REBOOTSYSTEM PSM de manière explicite ou à l’aide de la \_ macro PropSheet REBOOTSYSTEM.
ms.assetid: 461fce3c-183a-4b9b-8eab-ed2838d9f866
keywords:
- PSM_REBOOTSYSTEM les contrôles de message Windows
topic_type:
- apiref
api_name:
- PSM_REBOOTSYSTEM
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14f5018dc3845d699561740ccd9cbb0a9c793f15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464870"
---
# <a name="psm_rebootsystem-message"></a><span data-ttu-id="db6c6-105">\_Message PSM REBOOTSYSTEM</span><span class="sxs-lookup"><span data-stu-id="db6c6-105">PSM\_REBOOTSYSTEM message</span></span>

<span data-ttu-id="db6c6-106">Indique que le système doit être redémarré pour que les modifications prennent effet.</span><span class="sxs-lookup"><span data-stu-id="db6c6-106">Indicates the system needs to be restarted for the changes to take effect.</span></span> <span data-ttu-id="db6c6-107">Vous pouvez envoyer le **message \_ REBOOTSYSTEM PSM** de manière explicite ou à l’aide de la macro [**PropSheet \_ REBOOTSYSTEM**](/windows/desktop/api/Prsht/nf-prsht-propsheet_rebootsystem) .</span><span class="sxs-lookup"><span data-stu-id="db6c6-107">You can send the **PSM\_REBOOTSYSTEM** message explicitly or by using the [**PropSheet\_RebootSystem**](/windows/desktop/api/Prsht/nf-prsht-propsheet_rebootsystem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="db6c6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="db6c6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db6c6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="db6c6-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="db6c6-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="db6c6-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="db6c6-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="db6c6-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="db6c6-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="db6c6-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db6c6-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="db6c6-113">Return value</span></span>

<span data-ttu-id="db6c6-114">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="db6c6-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="db6c6-115">Notes</span><span class="sxs-lookup"><span data-stu-id="db6c6-115">Remarks</span></span>

<span data-ttu-id="db6c6-116">Une application doit envoyer ce message uniquement en réponse au message de notification [PSN \_ apply](psn-apply.md) ou [PSN \_ KILLACTIVE](psn-killactive.md) .</span><span class="sxs-lookup"><span data-stu-id="db6c6-116">An application should send this message only in response to the [PSN\_APPLY](psn-apply.md) or [PSN\_KILLACTIVE](psn-killactive.md) notification message.</span></span>

<span data-ttu-id="db6c6-117">Ce message force la fonction [**feuille**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) à retourner la \_ valeur ID PSREBOOTSYSTEM, mais uniquement si l’utilisateur clique sur le bouton **OK** pour fermer la feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="db6c6-117">This message causes the [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) function to return the ID\_PSREBOOTSYSTEM value, but only if the user clicks the **OK** button to close the property sheet.</span></span> <span data-ttu-id="db6c6-118">Il incombe à l’application de redémarrer le système, ce qui peut être fait à l’aide de la fonction [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) .</span><span class="sxs-lookup"><span data-stu-id="db6c6-118">It is the application's responsibility to reboot the system, which can be done by using the [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) function.</span></span>

<span data-ttu-id="db6c6-119">Ce message remplace tous les [**messages \_ RESTARTWINDOWS PSM**](psm-restartwindows.md) qui le précèdent ou le suivent.</span><span class="sxs-lookup"><span data-stu-id="db6c6-119">This message supersedes all [**PSM\_RESTARTWINDOWS**](psm-restartwindows.md) messages that precede or follow it.</span></span>

> [!Note]  
> <span data-ttu-id="db6c6-120">Ce message n’est pas pris en charge lors de l’utilisation du style de l’Assistant Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="db6c6-120">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="db6c6-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="db6c6-121">Requirements</span></span>



| <span data-ttu-id="db6c6-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="db6c6-122">Requirement</span></span> | <span data-ttu-id="db6c6-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="db6c6-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="db6c6-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="db6c6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="db6c6-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="db6c6-125">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="db6c6-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="db6c6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="db6c6-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="db6c6-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="db6c6-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="db6c6-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="db6c6-129"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="db6c6-129"><dt>Prsht.h</dt></span></span> </dl> |



 

