---
title: commande Update
description: La commande de mise à jour repeint le frame actuel dans le contexte de périphérique (DC) spécifié. Les périphériques vidéo numériques reconnaissent cette commande.
ms.assetid: 51a83262-91d5-4852-ad17-bd62c14417b1
keywords:
- commande de mise à jour Windows multimédia
topic_type:
- apiref
api_name:
- update
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cb0fc96d404efd8e2f657985ffa5a8861d3b4f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509365"
---
# <a name="update-command"></a><span data-ttu-id="c3dd8-105">commande Update</span><span class="sxs-lookup"><span data-stu-id="c3dd8-105">update command</span></span>

<span data-ttu-id="c3dd8-106">La commande de mise à jour repeint le frame actuel dans le contexte de périphérique (DC) spécifié.</span><span class="sxs-lookup"><span data-stu-id="c3dd8-106">The update command repaints the current frame into the specified device context (DC).</span></span> <span data-ttu-id="c3dd8-107">Les périphériques vidéo numériques reconnaissent cette commande.</span><span class="sxs-lookup"><span data-stu-id="c3dd8-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="c3dd8-108">Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.</span><span class="sxs-lookup"><span data-stu-id="c3dd8-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("update %s %s %s"), 
  lpszDeviceID, 
  lpszHDC, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="c3dd8-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c3dd8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3dd8-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="c3dd8-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="c3dd8-111">Identificateur d’un appareil MCI.</span><span class="sxs-lookup"><span data-stu-id="c3dd8-111">Identifier of an MCI device.</span></span> <span data-ttu-id="c3dd8-112">Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.</span><span class="sxs-lookup"><span data-stu-id="c3dd8-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="c3dd8-113"><span id="lpszHDC"></span><span id="lpszhdc"></span><span id="LPSZHDC"></span>*lpszHDC*</span><span class="sxs-lookup"><span data-stu-id="c3dd8-113"><span id="lpszHDC"></span><span id="lpszhdc"></span><span id="LPSZHDC"></span>*lpszHDC*</span></span>
</dt> <dd>

<span data-ttu-id="c3dd8-114">Handle d’un DC.</span><span class="sxs-lookup"><span data-stu-id="c3dd8-114">Handle of a DC.</span></span> <span data-ttu-id="c3dd8-115">Le tableau suivant répertorie les types d’appareils qui reconnaissent la commande de **mise à jour** et les indicateurs utilisés par chaque type.</span><span class="sxs-lookup"><span data-stu-id="c3dd8-115">The following table lists device types that recognize the **update** command and the flags used by each type.</span></span>



| <span data-ttu-id="c3dd8-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3dd8-116">Value</span></span>        | <span data-ttu-id="c3dd8-117">Signification</span><span class="sxs-lookup"><span data-stu-id="c3dd8-117">Meaning</span></span>                       | <span data-ttu-id="c3dd8-118">Signification</span><span class="sxs-lookup"><span data-stu-id="c3dd8-118">Meaning</span></span>         |
|--------------|-------------------------------|-----------------|
| <span data-ttu-id="c3dd8-119">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="c3dd8-119">digitalvideo</span></span> | <span data-ttu-id="c3dd8-120">HDC *HDC* HDC *HDC* au *Rect*</span><span class="sxs-lookup"><span data-stu-id="c3dd8-120">hdc *hdc* hdc *hdc* at *rect*</span></span> | <span data-ttu-id="c3dd8-121">peindre HDC *HDC*</span><span class="sxs-lookup"><span data-stu-id="c3dd8-121">paint hdc *hdc*</span></span> |



 

<span data-ttu-id="c3dd8-122">Le tableau suivant répertorie les indicateurs qui peuvent être spécifiés dans le paramètre **lpszHDC** et leurs significations.</span><span class="sxs-lookup"><span data-stu-id="c3dd8-122">The following table lists the flags that can be specified in the **lpszHDC** parameter and their meanings.</span></span>



| <span data-ttu-id="c3dd8-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3dd8-123">Value</span></span>               | <span data-ttu-id="c3dd8-124">Signification</span><span class="sxs-lookup"><span data-stu-id="c3dd8-124">Meaning</span></span>                                                                                                |
|---------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3dd8-125">HDC *HDC*</span><span class="sxs-lookup"><span data-stu-id="c3dd8-125">hdc *hdc*</span></span>           | <span data-ttu-id="c3dd8-126">Spécifie le handle du contrôleur de périphérique à peindre.</span><span class="sxs-lookup"><span data-stu-id="c3dd8-126">Specifies the handle of the DC to paint.</span></span>                                                               |
| <span data-ttu-id="c3dd8-127">HDC *HDC* au *recto*</span><span class="sxs-lookup"><span data-stu-id="c3dd8-127">hdc *hdc* at *rect*</span></span> | <span data-ttu-id="c3dd8-128">Spécifie le rectangle de découpage par rapport au rectangle client.</span><span class="sxs-lookup"><span data-stu-id="c3dd8-128">Specifies the clipping rectangle relative to the client rectangle.</span></span>                                     |
| <span data-ttu-id="c3dd8-129">peindre HDC *HDC*</span><span class="sxs-lookup"><span data-stu-id="c3dd8-129">paint hdc *hdc*</span></span>     | <span data-ttu-id="c3dd8-130">Peint le DC lorsque l’application reçoit un message de [**\_ peinture WM**](/windows/desktop/gdi/wm-paint) destiné à un contrôleur de périphérique.</span><span class="sxs-lookup"><span data-stu-id="c3dd8-130">Paints the DC when the application receives a [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message intended for a DC.</span></span> |



 

<span data-ttu-id="c3dd8-131">Pour spécifier le descripteur du DC, utilisez la chaîne « HDC » suivie d’une représentation ASCII du descripteur.</span><span class="sxs-lookup"><span data-stu-id="c3dd8-131">To specify the handle of the DC, use the string "hdc" followed by an ASCII representation of the handle.</span></span> <span data-ttu-id="c3dd8-132">Le rectangle est spécifié en tant que **x1 Y1 x2 Y2**.</span><span class="sxs-lookup"><span data-stu-id="c3dd8-132">The rectangle is specified as **X1 Y1 X2 Y2**.</span></span> <span data-ttu-id="c3dd8-133">Les coordonnées **x1 Y1** spécifient l’angle supérieur gauche du rectangle, tandis que les coordonnées **x2 Y2** spécifient la largeur et la hauteur.</span><span class="sxs-lookup"><span data-stu-id="c3dd8-133">The coordinates **X1 Y1** specify the upper left corner of the rectangle, and the coordinates **X2 Y2** specify the width and height.</span></span>

</dd> <dt>

<span data-ttu-id="c3dd8-134"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="c3dd8-134"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="c3dd8-135">Peut être « Wait », « Notify », ou les deux.</span><span class="sxs-lookup"><span data-stu-id="c3dd8-135">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="c3dd8-136">Pour les appareils vidéo numériques, vous pouvez également spécifier « test ».</span><span class="sxs-lookup"><span data-stu-id="c3dd8-136">For digital-video devices, "test" can also be specified.</span></span> <span data-ttu-id="c3dd8-137">Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="c3dd8-137">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3dd8-138">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c3dd8-138">Return Value</span></span>

<span data-ttu-id="c3dd8-139">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="c3dd8-139">Returns zero if successful or an error otherwise.</span></span>

## <a name="examples"></a><span data-ttu-id="c3dd8-140">Exemples</span><span class="sxs-lookup"><span data-stu-id="c3dd8-140">Examples</span></span>

<span data-ttu-id="c3dd8-141">La commande suivante met à jour l’intégralité de la fenêtre d’affichage utilisée par l’appareil « Movie ».</span><span class="sxs-lookup"><span data-stu-id="c3dd8-141">The following command updates the entire display window used by the "movie" device.</span></span> <span data-ttu-id="c3dd8-142">Le nombre 203 est un handle vers un contrôleur de périphérique obtenu à partir de la fonction [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) .</span><span class="sxs-lookup"><span data-stu-id="c3dd8-142">The number 203 is a handle to a DC obtained from the [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) function.</span></span>

``` syntax
update movie hdc 203
```

## <a name="requirements"></a><span data-ttu-id="c3dd8-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c3dd8-143">Requirements</span></span>



| <span data-ttu-id="c3dd8-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c3dd8-144">Requirement</span></span> | <span data-ttu-id="c3dd8-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3dd8-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="c3dd8-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3dd8-146">Minimum supported client</span></span><br/> | <span data-ttu-id="c3dd8-147">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c3dd8-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c3dd8-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3dd8-148">Minimum supported server</span></span><br/> | <span data-ttu-id="c3dd8-149">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c3dd8-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="c3dd8-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3dd8-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3dd8-151">MCI</span><span class="sxs-lookup"><span data-stu-id="c3dd8-151">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="c3dd8-152">Chaînes de commande MCI</span><span class="sxs-lookup"><span data-stu-id="c3dd8-152">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

