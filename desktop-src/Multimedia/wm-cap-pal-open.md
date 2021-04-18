---
title: Message WM_CAP_PAL_OPEN (VFW. h)
description: Le \_ message WM Cap \_ PAL \_ Open charge une nouvelle palette à partir d’un fichier de palette et la transmet à un pilote de capture.
ms.assetid: e77b518e-ff03-4622-978f-d9ebaa49c6a4
keywords:
- Message WM_CAP_PAL_OPEN Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_PAL_OPEN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e949bab50294251543c50d72c8d8b169cfc5514
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512362"
---
# <a name="wm_cap_pal_open-message"></a><span data-ttu-id="edcb8-104">Message d’ouverture de WM \_ Cap \_ PAL \_</span><span class="sxs-lookup"><span data-stu-id="edcb8-104">WM\_CAP\_PAL\_OPEN message</span></span>

<span data-ttu-id="edcb8-105">Le message **WM \_ Cap \_ PAL \_ Open** charge une nouvelle palette à partir d’un fichier de palette et la transmet à un pilote de capture.</span><span class="sxs-lookup"><span data-stu-id="edcb8-105">The **WM\_CAP\_PAL\_OPEN** message loads a new palette from a palette file and passes it to a capture driver.</span></span> <span data-ttu-id="edcb8-106">Les fichiers de palette utilisent généralement l’extension de nom de fichier. Adaptation.</span><span class="sxs-lookup"><span data-stu-id="edcb8-106">Palette files typically use the filename extension .PAL.</span></span> <span data-ttu-id="edcb8-107">Un pilote de capture utilise une palette lorsqu’il est requis par le format d’image numérisé spécifié.</span><span class="sxs-lookup"><span data-stu-id="edcb8-107">A capture driver uses a palette when required by the specified digitized image format.</span></span> <span data-ttu-id="edcb8-108">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capPaletteOpen**](/windows/desktop/api/Vfw/nf-vfw-cappaletteopen) .</span><span class="sxs-lookup"><span data-stu-id="edcb8-108">You can send this message explicitly or by using the [**capPaletteOpen**](/windows/desktop/api/Vfw/nf-vfw-cappaletteopen) macro.</span></span>


```C++
WM_CAP_PAL_OPEN 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="edcb8-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="edcb8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edcb8-110"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span><span class="sxs-lookup"><span data-stu-id="edcb8-110"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="edcb8-111">Pointeur vers une chaîne se terminant par null et contenant le nom de fichier de palette.</span><span class="sxs-lookup"><span data-stu-id="edcb8-111">Pointer to a null-terminated string containing the palette filename.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edcb8-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="edcb8-112">Return Value</span></span>

<span data-ttu-id="edcb8-113">Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="edcb8-113">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="edcb8-114">Si une erreur se produit et qu’une fonction de rappel d’erreur est définie à l’aide du message d' [**\_ erreur WM Cap \_ Set \_ callback \_**](wm-cap-set-callback-error.md) , la fonction de rappel d’erreur est appelée.</span><span class="sxs-lookup"><span data-stu-id="edcb8-114">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="edcb8-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="edcb8-115">Requirements</span></span>



| <span data-ttu-id="edcb8-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="edcb8-116">Requirement</span></span> | <span data-ttu-id="edcb8-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="edcb8-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="edcb8-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="edcb8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="edcb8-119">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="edcb8-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="edcb8-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="edcb8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="edcb8-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="edcb8-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="edcb8-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="edcb8-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="edcb8-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="edcb8-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edcb8-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="edcb8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edcb8-125">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="edcb8-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="edcb8-126">Messages de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="edcb8-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





