---
title: Message PSM_GETRESULT (Prsht. h)
description: Utilisé par les feuilles de propriétés non modales pour récupérer les informations retournées aux feuilles de propriétés modales par feuille. Vous pouvez envoyer ce message explicitement ou utiliser la \_ macro PropSheet GetResult.
ms.assetid: e0f609ea-5d7e-4c17-ade1-3c1051c5a5bf
keywords:
- PSM_GETRESULT les contrôles de message Windows
topic_type:
- apiref
api_name:
- PSM_GETRESULT
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d41609f625cbd3938fa78e9a2f91ab70168ecc29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509077"
---
# <a name="psm_getresult-message"></a><span data-ttu-id="884c9-105">\_Message PSM GETRESULT</span><span class="sxs-lookup"><span data-stu-id="884c9-105">PSM\_GETRESULT message</span></span>

<span data-ttu-id="884c9-106">Utilisé par les feuilles de propriétés non modales pour récupérer les informations retournées aux feuilles de propriétés modales par [**feuille**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta).</span><span class="sxs-lookup"><span data-stu-id="884c9-106">Used by modeless property sheets to retrieve the information returned to modal property sheets by [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta).</span></span> <span data-ttu-id="884c9-107">Vous pouvez envoyer ce message explicitement ou utiliser la macro [**PropSheet \_ GetResult**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getresult) .</span><span class="sxs-lookup"><span data-stu-id="884c9-107">You can send this message explicitly or use the [**PropSheet\_GetResult**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getresult) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="884c9-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="884c9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="884c9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="884c9-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="884c9-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="884c9-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="884c9-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="884c9-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="884c9-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="884c9-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="884c9-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="884c9-113">Return value</span></span>

<span data-ttu-id="884c9-114">Retourne une valeur positive en cas de réussite, ou-1 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="884c9-114">Returns a positive value if successful, or -1 otherwise.</span></span> <span data-ttu-id="884c9-115">Les valeurs de retour suivantes ont une signification particulière.</span><span class="sxs-lookup"><span data-stu-id="884c9-115">The following return values have a special meaning.</span></span>



| <span data-ttu-id="884c9-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="884c9-116">Return code</span></span>                                                                                         | <span data-ttu-id="884c9-117">Description</span><span class="sxs-lookup"><span data-stu-id="884c9-117">Description</span></span>                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="884c9-118"><dt>**ID \_ PSREBOOTSYSTEM**</dt></span><span class="sxs-lookup"><span data-stu-id="884c9-118"><dt>**ID\_PSREBOOTSYSTEM**</dt></span></span> </dl>   | <span data-ttu-id="884c9-119">Une page a envoyé un message [**PSM \_ REBOOTSYSTEM**](psm-rebootsystem.md) à la feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="884c9-119">A page sent a [**PSM\_REBOOTSYSTEM**](psm-rebootsystem.md) message to the property sheet.</span></span> <span data-ttu-id="884c9-120">L’ordinateur doit être redémarré pour que les modifications apportées à l’utilisateur prennent effet.</span><span class="sxs-lookup"><span data-stu-id="884c9-120">The computer must be restarted for the user's changes to take effect.</span></span><br/> |
| <dl> <span data-ttu-id="884c9-121"><dt>**ID \_ PSRESTARTWINDOWS**</dt></span><span class="sxs-lookup"><span data-stu-id="884c9-121"><dt>**ID\_PSRESTARTWINDOWS**</dt></span></span> </dl> | <span data-ttu-id="884c9-122">Une page a envoyé un message [**PSM \_ RESTARTWINDOWS**](psm-restartwindows.md) à la feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="884c9-122">A page sent a [**PSM\_RESTARTWINDOWS**](psm-restartwindows.md) message to the property sheet.</span></span> <span data-ttu-id="884c9-123">Vous devez redémarrer Windows pour que les modifications apportées à l’utilisateur prennent effet.</span><span class="sxs-lookup"><span data-stu-id="884c9-123">Windows must be restarted for the user's changes to take effect.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="884c9-124">Notes</span><span class="sxs-lookup"><span data-stu-id="884c9-124">Remarks</span></span>

<span data-ttu-id="884c9-125">Pour récupérer les informations d’erreur étendues, appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="884c9-125">To retrieve extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

<span data-ttu-id="884c9-126">La valeur de retour de ce message est identique à celle que [**feuille**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) retourne pour une feuille de propriétés modale.</span><span class="sxs-lookup"><span data-stu-id="884c9-126">The return value for this message is identical to what [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) returns for a modal property sheet.</span></span>

[<span data-ttu-id="884c9-127">Version 5,80.</span><span class="sxs-lookup"><span data-stu-id="884c9-127">Version 5.80.</span></span>](common-control-versions.md) <span data-ttu-id="884c9-128">La valeur de retour [**feuille**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) transporte des informations différentes pour les feuilles de propriétés modales et non modales.</span><span class="sxs-lookup"><span data-stu-id="884c9-128">The [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) return value carries different information for modal and modeless property sheets.</span></span> <span data-ttu-id="884c9-129">Dans certains cas, les feuilles de propriétés non modales peuvent avoir besoin des informations qu’elles auraient reçues de **feuille** si elles avaient été modales.</span><span class="sxs-lookup"><span data-stu-id="884c9-129">In some cases, modeless property sheets may need the information they would have received from **PropertySheet** if they had been modal.</span></span> <span data-ttu-id="884c9-130">En particulier, il peut être nécessaire de savoir si l’ID \_ PSREBOOTSYSTEM ou l’ID \_ PSRESTARTWINDOWS aurait été retourné.</span><span class="sxs-lookup"><span data-stu-id="884c9-130">In particular, they may need to know whether ID\_PSREBOOTSYSTEM or ID\_PSRESTARTWINDOWS would have been returned.</span></span>

<span data-ttu-id="884c9-131">Pour une feuille de propriétés non modale, votre boucle de messages doit utiliser des [**\_ ISDIALOGMESSAGE PSM**](psm-isdialogmessage.md) pour transmettre des messages à la boîte de dialogue de la feuille de propriétés, et [**PSM \_ GETCURRENTPAGEHWND**](psm-getcurrentpagehwnd.md) pour déterminer quand détruire la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="884c9-131">For a modeless property sheet, your message loop should use [**PSM\_ISDIALOGMESSAGE**](psm-isdialogmessage.md) to pass messages to the property sheet dialog box, and [**PSM\_GETCURRENTPAGEHWND**](psm-getcurrentpagehwnd.md) to determine when to destroy the dialog box.</span></span> <span data-ttu-id="884c9-132">Quand l’utilisateur clique sur le bouton **OK** ou **Annuler** , **PSM \_ GETCURRENTPAGEHWND** retourne la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="884c9-132">When the user clicks the **OK** or **Cancel** button, **PSM\_GETCURRENTPAGEHWND** returns **NULL**.</span></span> <span data-ttu-id="884c9-133">Vous pouvez ensuite récupérer la valeur qu’une feuille de propriétés modale aurait reçue de [**feuille**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) en envoyant un message **PSM \_** .</span><span class="sxs-lookup"><span data-stu-id="884c9-133">You can then retrieve the value that a modal property sheet would have received from [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) by sending a **PSM\_GETRESULT** message.</span></span>

> [!Note]  
> <span data-ttu-id="884c9-134">Ce message n’est pas pris en charge lors de l’utilisation du style de l’Assistant Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="884c9-134">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="884c9-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="884c9-135">Requirements</span></span>



| <span data-ttu-id="884c9-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="884c9-136">Requirement</span></span> | <span data-ttu-id="884c9-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="884c9-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="884c9-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="884c9-138">Minimum supported client</span></span><br/> | <span data-ttu-id="884c9-139">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="884c9-139">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="884c9-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="884c9-140">Minimum supported server</span></span><br/> | <span data-ttu-id="884c9-141">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="884c9-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="884c9-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="884c9-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="884c9-143"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="884c9-143"><dt>Prsht.h</dt></span></span> </dl> |



 

