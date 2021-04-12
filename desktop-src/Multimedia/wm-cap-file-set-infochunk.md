---
title: Message WM_CAP_FILE_SET_INFOCHUNK (VFW. h)
description: Le \_ jeu de fichiers WM Cap définit les \_ \_ \_ jeux de messages INFOCHUNK et efface les segments d’informations.
ms.assetid: 67d11a05-a2b4-45d2-ba66-83a198745303
keywords:
- Message WM_CAP_FILE_SET_INFOCHUNK Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SET_INFOCHUNK
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 067ba00563a5ca511f13b23615fc4542090ba397
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032386"
---
# <a name="wm_cap_file_set_infochunk-message"></a><span data-ttu-id="85e7b-104">\_ \_ \_ Message INFOCHUNK du jeu de fichiers \_ de la casquette WM</span><span class="sxs-lookup"><span data-stu-id="85e7b-104">WM\_CAP\_FILE\_SET\_INFOCHUNK message</span></span>

<span data-ttu-id="85e7b-105">Le **jeu de fichiers WM Cap définit les jeux de messages \_ \_ \_ \_ INFOCHUNK** et efface les segments d’informations.</span><span class="sxs-lookup"><span data-stu-id="85e7b-105">The **WM\_CAP\_FILE\_SET\_INFOCHUNK** message sets and clears information chunks.</span></span> <span data-ttu-id="85e7b-106">Des blocs d’informations peuvent être insérés dans un fichier AVI au cours de la capture pour incorporer des chaînes de texte ou des données personnalisées.</span><span class="sxs-lookup"><span data-stu-id="85e7b-106">Information chunks can be inserted in an AVI file during capture to embed text strings or custom data.</span></span> <span data-ttu-id="85e7b-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capFileSetInfoChunk**](/windows/desktop/api/Vfw/nf-vfw-capfilesetinfochunk) .</span><span class="sxs-lookup"><span data-stu-id="85e7b-107">You can send this message explicitly or by using the [**capFileSetInfoChunk**](/windows/desktop/api/Vfw/nf-vfw-capfilesetinfochunk) macro.</span></span>


```C++
WM_CAP_FILE_SET_INFOCHUNK 
wParam = (WPARAM)0; 
lParam = (LPARAM) (LPCAPINFOCHUNK) (lpInfoChunk); 
```



## <a name="parameters"></a><span data-ttu-id="85e7b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="85e7b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85e7b-109"><span id="lpInfoChunk"></span><span id="lpinfochunk"></span><span id="LPINFOCHUNK"></span>*lpInfoChunk*</span><span class="sxs-lookup"><span data-stu-id="85e7b-109"><span id="lpInfoChunk"></span><span id="lpinfochunk"></span><span id="LPINFOCHUNK"></span>*lpInfoChunk*</span></span>
</dt> <dd>

<span data-ttu-id="85e7b-110">Pointeur vers une structure [**CAPINFOCHUNK**](/windows/win32/api/vfw/ns-vfw-capinfochunk) définissant le segment d’informations à créer ou à supprimer.</span><span class="sxs-lookup"><span data-stu-id="85e7b-110">Pointer to a [**CAPINFOCHUNK**](/windows/win32/api/vfw/ns-vfw-capinfochunk) structure defining the information chunk to be created or deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85e7b-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="85e7b-111">Return Value</span></span>

<span data-ttu-id="85e7b-112">Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="85e7b-112">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="85e7b-113">Si une erreur se produit et qu’une fonction de rappel d’erreur est définie à l’aide du message d' [**\_ erreur WM Cap \_ Set \_ callback \_**](wm-cap-set-callback-error.md) , la fonction de rappel d’erreur est appelée.</span><span class="sxs-lookup"><span data-stu-id="85e7b-113">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="remarks"></a><span data-ttu-id="85e7b-114">Notes</span><span class="sxs-lookup"><span data-stu-id="85e7b-114">Remarks</span></span>

<span data-ttu-id="85e7b-115">Plusieurs segments d’informations inscrits peuvent être ajoutés à un fichier AVI.</span><span class="sxs-lookup"><span data-stu-id="85e7b-115">Multiple registered information chunks can be added to an AVI file.</span></span> <span data-ttu-id="85e7b-116">Une fois qu’un segment d’informations est défini, il continue à être ajouté aux fichiers de capture suivants jusqu’à ce que l’entrée soit effacée ou que toutes les entrées de segment d’information soient effacées.</span><span class="sxs-lookup"><span data-stu-id="85e7b-116">After an information chunk is set, it continues to be added to subsequent capture files until either the entry is cleared or all information chunk entries are cleared.</span></span> <span data-ttu-id="85e7b-117">Pour effacer une entrée unique, spécifiez le segment d’informations dans le membre **fccInfoID** et la **valeur null** dans le membre **lpData** de la structure [**CAPINFOCHUNK**](/windows/win32/api/vfw/ns-vfw-capinfochunk) .</span><span class="sxs-lookup"><span data-stu-id="85e7b-117">To clear a single entry, specify the information chunk in the **fccInfoID** member and **NULL** in the **lpData** member of the [**CAPINFOCHUNK**](/windows/win32/api/vfw/ns-vfw-capinfochunk) structure.</span></span> <span data-ttu-id="85e7b-118">Pour effacer toutes les entrées, spécifiez **null** dans **fccInfoID**.</span><span class="sxs-lookup"><span data-stu-id="85e7b-118">To clear all entries, specify **NULL** in **fccInfoID**.</span></span>

## <a name="requirements"></a><span data-ttu-id="85e7b-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="85e7b-119">Requirements</span></span>



| <span data-ttu-id="85e7b-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="85e7b-120">Requirement</span></span> | <span data-ttu-id="85e7b-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="85e7b-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="85e7b-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="85e7b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="85e7b-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="85e7b-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="85e7b-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="85e7b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="85e7b-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="85e7b-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="85e7b-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="85e7b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="85e7b-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="85e7b-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85e7b-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="85e7b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85e7b-129">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="85e7b-129">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="85e7b-130">Messages de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="85e7b-130">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





