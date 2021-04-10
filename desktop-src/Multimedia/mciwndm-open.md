---
title: Message MCIWNDM_OPEN (VFW. h)
description: Le \_ message MCIWNDM Open ouvre un appareil MCI et l’associe à une fenêtre MCIWnd.
ms.assetid: ad1dfe0f-015b-45a9-ab88-cc0bdf0aa057
keywords:
- Message MCIWNDM_OPEN Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_OPEN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2f232ea9076a1e0ff8c105d8c5cf94104e455c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103436"
---
# <a name="mciwndm_open-message"></a><span data-ttu-id="f1e60-104">MCIWNDM \_ ouvrir le message</span><span class="sxs-lookup"><span data-stu-id="f1e60-104">MCIWNDM\_OPEN message</span></span>

<span data-ttu-id="f1e60-105">Le message **MCIWNDM \_ Open** ouvre un appareil MCI et l’associe à une fenêtre MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="f1e60-105">The **MCIWNDM\_OPEN** message opens an MCI device and associates it with an MCIWnd window.</span></span> <span data-ttu-id="f1e60-106">Pour les appareils MCI qui utilisent des fichiers de données, cette macro peut également ouvrir un fichier de données spécifié, nommer un nouveau fichier à créer ou afficher une boîte de dialogue qui permet à l’utilisateur de sélectionner un fichier à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="f1e60-106">For MCI devices that use data files, this macro can also open a specified data file, name a new file to be created, or display a dialog box to let the user select a file to open.</span></span> <span data-ttu-id="f1e60-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) .</span><span class="sxs-lookup"><span data-stu-id="f1e60-107">You can send this message explicitly or by using the [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) macro.</span></span>


```C++
MCIWNDM_OPEN 
wParam = (WPARAM) (UINT) wFlags; 
lParam = (LPARAM) (LPVOID) szFile; 
```



## <a name="parameters"></a><span data-ttu-id="f1e60-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f1e60-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1e60-109"><span id="wFlags"></span><span id="wflags"></span><span id="WFLAGS"></span>*wFlags*</span><span class="sxs-lookup"><span data-stu-id="f1e60-109"><span id="wFlags"></span><span id="wflags"></span><span id="WFLAGS"></span>*wFlags*</span></span>
</dt> <dd>

<span data-ttu-id="f1e60-110">Indicateurs associés à l’appareil ou au fichier à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="f1e60-110">Flags associated with the device or file to open.</span></span> <span data-ttu-id="f1e60-111">Le \_ nouvel indicateur MCIWNDOPENF spécifie qu’un nouveau fichier doit être créé avec le nom spécifié dans **szFile**.</span><span class="sxs-lookup"><span data-stu-id="f1e60-111">The MCIWNDOPENF\_NEW flag specifies a new file is to be created with the name specified in **szFile**.</span></span>

</dd> <dt>

<span data-ttu-id="f1e60-112"><span id="szFile"></span><span id="szfile"></span><span id="SZFILE"></span>*szFile*</span><span class="sxs-lookup"><span data-stu-id="f1e60-112"><span id="szFile"></span><span id="szfile"></span><span id="SZFILE"></span>*szFile*</span></span>
</dt> <dd>

<span data-ttu-id="f1e60-113">Pointeur vers une chaîne se terminant par un caractère null, identifiant le nom de fichier ou le nom du périphérique MCI à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="f1e60-113">Pointer to a null-terminated string identifying the filename or MCI device name to open.</span></span> <span data-ttu-id="f1e60-114">Spécifiez 1 pour que ce paramètre affiche la boîte de dialogue Ouvrir.</span><span class="sxs-lookup"><span data-stu-id="f1e60-114">Specify  1 for this parameter to display the Open dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1e60-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f1e60-115">Return Value</span></span>

<span data-ttu-id="f1e60-116">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="f1e60-116">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1e60-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f1e60-117">Requirements</span></span>



| <span data-ttu-id="f1e60-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f1e60-118">Requirement</span></span> | <span data-ttu-id="f1e60-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1e60-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f1e60-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f1e60-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f1e60-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f1e60-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="f1e60-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f1e60-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f1e60-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f1e60-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f1e60-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="f1e60-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1e60-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1e60-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1e60-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f1e60-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1e60-127">**MCIWndOpen**</span><span class="sxs-lookup"><span data-stu-id="f1e60-127">**MCIWndOpen**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndopen)
</dt> </dl>

 

 





