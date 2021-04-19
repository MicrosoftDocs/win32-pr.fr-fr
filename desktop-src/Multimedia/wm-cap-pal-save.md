---
title: Message WM_CAP_PAL_SAVE (VFW. h)
description: Le \_ message WM Cap \_ PAL \_ Save enregistre la palette actuelle dans un fichier palette. Les fichiers de palette utilisent généralement l’extension de nom de fichier. Adaptation. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capPaletteSave.
ms.assetid: b1fa3978-9147-403f-aa08-db1a803aa5ac
keywords:
- Message WM_CAP_PAL_SAVE Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_PAL_SAVE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf5ea36b2eaf50b2555fa849a176d12d0932eed2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509928"
---
# <a name="wm_cap_pal_save-message"></a><span data-ttu-id="722bd-106">\_Message d’enregistrement WM Cap \_ PAL \_</span><span class="sxs-lookup"><span data-stu-id="722bd-106">WM\_CAP\_PAL\_SAVE message</span></span>

<span data-ttu-id="722bd-107">Le message **WM \_ Cap \_ PAL \_ Save** enregistre la palette actuelle dans un fichier palette.</span><span class="sxs-lookup"><span data-stu-id="722bd-107">The **WM\_CAP\_PAL\_SAVE** message saves the current palette to a palette file.</span></span> <span data-ttu-id="722bd-108">Les fichiers de palette utilisent généralement l’extension de nom de fichier. Adaptation.</span><span class="sxs-lookup"><span data-stu-id="722bd-108">Palette files typically use the filename extension .PAL.</span></span> <span data-ttu-id="722bd-109">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capPaletteSave**](/windows/desktop/api/Vfw/nf-vfw-cappalettesave) .</span><span class="sxs-lookup"><span data-stu-id="722bd-109">You can send this message explicitly or by using the [**capPaletteSave**](/windows/desktop/api/Vfw/nf-vfw-cappalettesave) macro.</span></span>


```C++
WM_CAP_PAL_SAVE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="722bd-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="722bd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="722bd-111"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span><span class="sxs-lookup"><span data-stu-id="722bd-111"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="722bd-112">Pointeur vers une chaîne se terminant par null et contenant le nom de fichier de palette.</span><span class="sxs-lookup"><span data-stu-id="722bd-112">Pointer to a null-terminated string containing the palette filename.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="722bd-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="722bd-113">Return Value</span></span>

<span data-ttu-id="722bd-114">Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="722bd-114">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="722bd-115">Si une erreur se produit et qu’une fonction de rappel d’erreur est définie à l’aide du message d' [**\_ erreur WM Cap \_ Set \_ callback \_**](wm-cap-set-callback-error.md) , la fonction de rappel d’erreur est appelée.</span><span class="sxs-lookup"><span data-stu-id="722bd-115">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="722bd-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="722bd-116">Requirements</span></span>



| <span data-ttu-id="722bd-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="722bd-117">Requirement</span></span> | <span data-ttu-id="722bd-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="722bd-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="722bd-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="722bd-119">Minimum supported client</span></span><br/> | <span data-ttu-id="722bd-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="722bd-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="722bd-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="722bd-121">Minimum supported server</span></span><br/> | <span data-ttu-id="722bd-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="722bd-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="722bd-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="722bd-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="722bd-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="722bd-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="722bd-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="722bd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="722bd-126">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="722bd-126">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="722bd-127">Messages de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="722bd-127">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





