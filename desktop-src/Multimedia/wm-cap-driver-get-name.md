---
title: Message WM_CAP_DRIVER_GET_NAME (VFW. h)
description: Le \_ message WM Cap \_ Driver \_ obtenir \_ le nom renvoie le nom du pilote de capture connecté à la fenêtre de capture. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capDriverGetName.
ms.assetid: 84cecaf1-e0ff-424f-8c10-8bfe5cc2e7ea
keywords:
- Message WM_CAP_DRIVER_GET_NAME Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_GET_NAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 256b5f7913c83ddd278f3f3a05552b3d81070c73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464735"
---
# <a name="wm_cap_driver_get_name-message"></a><span data-ttu-id="641c7-105">\_Message d' \_ extraction du pilote WM Cap \_ \_</span><span class="sxs-lookup"><span data-stu-id="641c7-105">WM\_CAP\_DRIVER\_GET\_NAME message</span></span>

<span data-ttu-id="641c7-106">Le message **WM \_ Cap \_ Driver obtenir le \_ \_ nom** renvoie le nom du pilote de capture connecté à la fenêtre de capture.</span><span class="sxs-lookup"><span data-stu-id="641c7-106">The **WM\_CAP\_DRIVER\_GET\_NAME** message returns the name of the capture driver connected to the capture window.</span></span> <span data-ttu-id="641c7-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capDriverGetName**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetname) .</span><span class="sxs-lookup"><span data-stu-id="641c7-107">You can send this message explicitly or by using the [**capDriverGetName**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetname) macro.</span></span>


```C++
WM_CAP_DRIVER_GET_NAME 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="641c7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="641c7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="641c7-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="641c7-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="641c7-110">Taille, en octets, de la mémoire tampon référencée par **szName**.</span><span class="sxs-lookup"><span data-stu-id="641c7-110">Size, in bytes, of the buffer referenced by **szName**.</span></span>

</dd> <dt>

<span data-ttu-id="641c7-111"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span><span class="sxs-lookup"><span data-stu-id="641c7-111"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="641c7-112">Pointeur vers une mémoire tampon définie par l’application utilisée pour retourner le nom de l’appareil sous la forme d’une chaîne terminée par le caractère null.</span><span class="sxs-lookup"><span data-stu-id="641c7-112">Pointer to an application-defined buffer used to return the device name as a null-terminated string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="641c7-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="641c7-113">Return Value</span></span>

<span data-ttu-id="641c7-114">Retourne la **valeur true** en cas de réussite ou **false** si la fenêtre de capture n’est pas connectée à un pilote de capture.</span><span class="sxs-lookup"><span data-stu-id="641c7-114">Returns **TRUE** if successful or **FALSE** if the capture window is not connected to a capture driver.</span></span>

## <a name="remarks"></a><span data-ttu-id="641c7-115">Notes</span><span class="sxs-lookup"><span data-stu-id="641c7-115">Remarks</span></span>

<span data-ttu-id="641c7-116">Le nom est une chaîne de texte Récupérée à partir de la zone de ressources du pilote.</span><span class="sxs-lookup"><span data-stu-id="641c7-116">The name is a text string retrieved from the driver's resource area.</span></span> <span data-ttu-id="641c7-117">Les applications doivent allouer environ 80 octets pour cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="641c7-117">Applications should allocate approximately 80 bytes for this string.</span></span> <span data-ttu-id="641c7-118">Si le pilote ne contient pas de ressource de nom, le nom de chemin d’accès complet du pilote figurant dans le registre ou dans le fichier SYSTEM.INI est retourné.</span><span class="sxs-lookup"><span data-stu-id="641c7-118">If the driver does not contain a name resource, the full path name of the driver listed in the registry or in the SYSTEM.INI file is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="641c7-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="641c7-119">Requirements</span></span>



| <span data-ttu-id="641c7-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="641c7-120">Requirement</span></span> | <span data-ttu-id="641c7-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="641c7-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="641c7-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="641c7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="641c7-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="641c7-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="641c7-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="641c7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="641c7-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="641c7-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="641c7-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="641c7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="641c7-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="641c7-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="641c7-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="641c7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="641c7-129">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="641c7-129">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="641c7-130">Messages de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="641c7-130">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





