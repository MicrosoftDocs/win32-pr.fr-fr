---
title: Message WM_CAP_FILE_SAVEAS (VFW. h)
description: Le \_ message WM Cap \_ file \_ SaveAs copie le contenu du fichier de capture dans un autre fichier. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capFileSaveAs.
ms.assetid: fab37bee-3160-4ebc-b58f-46021ed49b55
keywords:
- Message WM_CAP_FILE_SAVEAS Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SAVEAS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aca099fefab7ca0f4ef391b1b65e89938a947a01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384259"
---
# <a name="wm_cap_file_saveas-message"></a><span data-ttu-id="1ea16-105">\_Message de \_ fichier \_ SaveAs de l’embout de fichier WM</span><span class="sxs-lookup"><span data-stu-id="1ea16-105">WM\_CAP\_FILE\_SAVEAS message</span></span>

<span data-ttu-id="1ea16-106">Le message **WM \_ Cap \_ file \_ SaveAs** copie le contenu du fichier de capture dans un autre fichier.</span><span class="sxs-lookup"><span data-stu-id="1ea16-106">The **WM\_CAP\_FILE\_SAVEAS** message copies the contents of the capture file to another file.</span></span> <span data-ttu-id="1ea16-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capFileSaveAs**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) .</span><span class="sxs-lookup"><span data-stu-id="1ea16-107">You can send this message explicitly or by using the [**capFileSaveAs**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) macro.</span></span>


```C++
WM_CAP_FILE_SAVEAS 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="1ea16-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1ea16-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ea16-109"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span><span class="sxs-lookup"><span data-stu-id="1ea16-109"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="1ea16-110">Pointeur vers la chaîne terminée par le caractère null qui contient le nom du fichier de destination utilisé pour copier le fichier.</span><span class="sxs-lookup"><span data-stu-id="1ea16-110">Pointer to the null-terminated string that contains the name of the destination file used to copy the file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ea16-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1ea16-111">Return Value</span></span>

<span data-ttu-id="1ea16-112">Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="1ea16-112">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="1ea16-113">Si une erreur se produit et qu’une fonction de rappel d’erreur est définie à l’aide du message d' [**\_ erreur WM Cap \_ Set \_ callback \_**](wm-cap-set-callback-error.md) , la fonction de rappel d’erreur est appelée.</span><span class="sxs-lookup"><span data-stu-id="1ea16-113">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ea16-114">Notes</span><span class="sxs-lookup"><span data-stu-id="1ea16-114">Remarks</span></span>

<span data-ttu-id="1ea16-115">Ce message ne modifie pas le nom ou le contenu du fichier de capture actuel.</span><span class="sxs-lookup"><span data-stu-id="1ea16-115">This message does not change the name or contents of the current capture file.</span></span>

<span data-ttu-id="1ea16-116">Si l’opération de copie échoue en raison d’une erreur de disque plein, le fichier de destination est automatiquement supprimé.</span><span class="sxs-lookup"><span data-stu-id="1ea16-116">If the copy operation is unsuccessful due to a disk full error, the destination file is automatically deleted.</span></span>

<span data-ttu-id="1ea16-117">En règle générale, un fichier de capture est préalloué pour le plus grand segment de capture attendu et seule une partie de celui-ci peut être utilisée pour capturer des données.</span><span class="sxs-lookup"><span data-stu-id="1ea16-117">Typically, a capture file is preallocated for the largest capture segment anticipated and only a portion of it might be used to capture data.</span></span> <span data-ttu-id="1ea16-118">Ce message copie uniquement la partie du fichier contenant les données de capture.</span><span class="sxs-lookup"><span data-stu-id="1ea16-118">This message copies only the portion of the file containing the capture data.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ea16-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1ea16-119">Requirements</span></span>



| <span data-ttu-id="1ea16-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1ea16-120">Requirement</span></span> | <span data-ttu-id="1ea16-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="1ea16-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="1ea16-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1ea16-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1ea16-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1ea16-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="1ea16-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1ea16-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1ea16-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1ea16-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="1ea16-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="1ea16-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ea16-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ea16-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ea16-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ea16-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ea16-129">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="1ea16-129">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="1ea16-130">Messages de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="1ea16-130">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





