---
title: Message WM_CAP_DRIVER_GET_VERSION (VFW. h)
description: Le \_ message WM Cap \_ Driver \_ obtenir \_ la version retourne les informations de version du pilote de capture connecté à une fenêtre de capture. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capDriverGetVersion.
ms.assetid: 762ebe7e-0d09-46ea-ab17-86061f0bd8f9
keywords:
- Message WM_CAP_DRIVER_GET_VERSION Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_GET_VERSION
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ced70f2d0159ef4bbad3f2d7a8027c30b2c71a5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509743"
---
# <a name="wm_cap_driver_get_version-message"></a><span data-ttu-id="d84f8-105">Message de la version du \_ pilote WM Cap \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="d84f8-105">WM\_CAP\_DRIVER\_GET\_VERSION message</span></span>

<span data-ttu-id="d84f8-106">Le message **WM \_ Cap \_ Driver obtenir la \_ \_ version** retourne les informations de version du pilote de capture connecté à une fenêtre de capture.</span><span class="sxs-lookup"><span data-stu-id="d84f8-106">The **WM\_CAP\_DRIVER\_GET\_VERSION** message returns the version information of the capture driver connected to a capture window.</span></span> <span data-ttu-id="d84f8-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capDriverGetVersion**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetversion) .</span><span class="sxs-lookup"><span data-stu-id="d84f8-107">You can send this message explicitly or by using the [**capDriverGetVersion**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetversion) macro.</span></span>


```C++
WM_CAP_DRIVER_GET_VERSION 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szVer); 
```



## <a name="parameters"></a><span data-ttu-id="d84f8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d84f8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d84f8-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="d84f8-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="d84f8-110">Taille, en octets, de la mémoire tampon définie par l’application référencée par **szVer**.</span><span class="sxs-lookup"><span data-stu-id="d84f8-110">Size, in bytes, of the application-defined buffer referenced by **szVer**.</span></span>

</dd> <dt>

<span data-ttu-id="d84f8-111"><span id="szVer"></span><span id="szver"></span><span id="SZVER"></span>*szVer*</span><span class="sxs-lookup"><span data-stu-id="d84f8-111"><span id="szVer"></span><span id="szver"></span><span id="SZVER"></span>*szVer*</span></span>
</dt> <dd>

<span data-ttu-id="d84f8-112">Pointeur vers une mémoire tampon définie par l’application utilisée pour retourner les informations de version sous la forme d’une chaîne terminée par le caractère null.</span><span class="sxs-lookup"><span data-stu-id="d84f8-112">Pointer to an application-defined buffer used to return the version information as a null-terminated string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d84f8-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d84f8-113">Return Value</span></span>

<span data-ttu-id="d84f8-114">Retourne la **valeur true** en cas de réussite ou **false** si la fenêtre de capture n’est pas connectée à un pilote de capture.</span><span class="sxs-lookup"><span data-stu-id="d84f8-114">Returns **TRUE** if successful or **FALSE** if the capture window is not connected to a capture driver.</span></span>

## <a name="remarks"></a><span data-ttu-id="d84f8-115">Notes</span><span class="sxs-lookup"><span data-stu-id="d84f8-115">Remarks</span></span>

<span data-ttu-id="d84f8-116">Les informations de version sont une chaîne de texte Récupérée à partir de la zone de ressources du pilote.</span><span class="sxs-lookup"><span data-stu-id="d84f8-116">The version information is a text string retrieved from the driver's resource area.</span></span> <span data-ttu-id="d84f8-117">Les applications doivent allouer environ 40 octets pour cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="d84f8-117">Applications should allocate approximately 40 bytes for this string.</span></span> <span data-ttu-id="d84f8-118">Si les informations de version ne sont pas disponibles, une chaîne **null** est retournée.</span><span class="sxs-lookup"><span data-stu-id="d84f8-118">If version information is not available, a **NULL** string is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="d84f8-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d84f8-119">Requirements</span></span>



| <span data-ttu-id="d84f8-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d84f8-120">Requirement</span></span> | <span data-ttu-id="d84f8-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="d84f8-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d84f8-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d84f8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d84f8-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d84f8-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d84f8-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d84f8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d84f8-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d84f8-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d84f8-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="d84f8-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d84f8-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="d84f8-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d84f8-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d84f8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d84f8-129">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="d84f8-129">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="d84f8-130">Messages de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="d84f8-130">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





