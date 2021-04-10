---
title: Message PSM_RESTARTWINDOWS (Prsht. h)
description: Indique que Windows doit être redémarré pour que les modifications prennent effet.
ms.assetid: 5bf634ee-7408-45df-adb6-c5b947f6c47b
keywords:
- PSM_RESTARTWINDOWS les contrôles de message Windows
topic_type:
- apiref
api_name:
- PSM_RESTARTWINDOWS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb12126ae0a2b9187a941ccc1aff53186a0cda7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843425"
---
# <a name="psm_restartwindows-message"></a><span data-ttu-id="a28c1-104">\_Message PSM RESTARTWINDOWS</span><span class="sxs-lookup"><span data-stu-id="a28c1-104">PSM\_RESTARTWINDOWS message</span></span>

<span data-ttu-id="a28c1-105">Indique que Windows doit être redémarré pour que les modifications prennent effet.</span><span class="sxs-lookup"><span data-stu-id="a28c1-105">Indicates that Windows needs to be restarted for the changes to take effect.</span></span>

## <a name="parameters"></a><span data-ttu-id="a28c1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a28c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a28c1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a28c1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a28c1-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="a28c1-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a28c1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a28c1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a28c1-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="a28c1-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a28c1-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a28c1-111">Return value</span></span>

<span data-ttu-id="a28c1-112">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="a28c1-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a28c1-113">Notes</span><span class="sxs-lookup"><span data-stu-id="a28c1-113">Remarks</span></span>

<span data-ttu-id="a28c1-114">Une application doit envoyer ce message uniquement en réponse au code de notification [PSN \_ apply](psn-apply.md) ou [PSN \_ KILLACTIVE](psn-killactive.md) .</span><span class="sxs-lookup"><span data-stu-id="a28c1-114">An application should send this message only in response to the [PSN\_APPLY](psn-apply.md) or [PSN\_KILLACTIVE](psn-killactive.md) notification code.</span></span> <span data-ttu-id="a28c1-115">Vous pouvez envoyer le **message \_ RESTARTWINDOWS PSM** de manière explicite ou à l’aide de la macro [**PropSheet \_ RESTARTWINDOWS**](/windows/desktop/api/Prsht/nf-prsht-propsheet_restartwindows) .</span><span class="sxs-lookup"><span data-stu-id="a28c1-115">You can send the **PSM\_RESTARTWINDOWS** message explicitly or by using the [**PropSheet\_RestartWindows**](/windows/desktop/api/Prsht/nf-prsht-propsheet_restartwindows) macro.</span></span>

<span data-ttu-id="a28c1-116">Ce message force la fonction [**feuille**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) à retourner la \_ valeur ID PSRESTARTWINDOWS, mais uniquement si l’utilisateur clique sur le bouton **OK** pour fermer la feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="a28c1-116">This message causes the [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) function to return the ID\_PSRESTARTWINDOWS value, but only if the user clicks the **OK** button to close the property sheet.</span></span> <span data-ttu-id="a28c1-117">L’application est responsable du redémarrage de Windows, ce qui peut être effectué à l’aide de la fonction [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) .</span><span class="sxs-lookup"><span data-stu-id="a28c1-117">It is the application's responsibility to restart Windows, which can be done by using the [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) function.</span></span>

> [!Note]  
> <span data-ttu-id="a28c1-118">Ce message n’est pas pris en charge lors de l’utilisation du style de l’Assistant Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="a28c1-118">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a28c1-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a28c1-119">Requirements</span></span>



| <span data-ttu-id="a28c1-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a28c1-120">Requirement</span></span> | <span data-ttu-id="a28c1-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="a28c1-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a28c1-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a28c1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a28c1-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a28c1-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a28c1-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a28c1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a28c1-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a28c1-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a28c1-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="a28c1-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a28c1-127"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="a28c1-127"><dt>Prsht.h</dt></span></span> </dl> |



 

