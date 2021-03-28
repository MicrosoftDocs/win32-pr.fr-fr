---
description: Envoyé lorsque l’utilisateur dépose un fichier dans la fenêtre d’une application qui s’est inscrite en tant que destinataire des fichiers supprimés.
ms.assetid: 07dc2df7-4699-4e9c-b1a5-4ce877116268
title: Message WM_DROPFILES (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb8362bfa746eaab519cdfc34d2cdf7757105fb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973106"
---
# <a name="wm_dropfiles-message"></a><span data-ttu-id="528dd-103">\_Message WM DROPFILES</span><span class="sxs-lookup"><span data-stu-id="528dd-103">WM\_DROPFILES message</span></span>

<span data-ttu-id="528dd-104">Envoyé lorsque l’utilisateur dépose un fichier dans la fenêtre d’une application qui s’est inscrite en tant que destinataire des fichiers supprimés.</span><span class="sxs-lookup"><span data-stu-id="528dd-104">Sent when the user drops a file on the window of an application that has registered itself as a recipient of dropped files.</span></span>


```C++
PostMessage(
    (HWND) hWndControl,   // handle to destination control
    (UINT) WM_DROPFILES,  // message ID
    (WPARAM) wParam,      // = (WPARAM) (HDROP) hDrop;
    (LPARAM) lParam       // = 0; not used, must be zero 
);          
```



## <a name="parameters"></a><span data-ttu-id="528dd-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="528dd-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="528dd-106">*hDrop*</span><span class="sxs-lookup"><span data-stu-id="528dd-106">*hDrop*</span></span> 
</dt> <dd>

<span data-ttu-id="528dd-107">Handle vers une structure interne décrivant les fichiers déplacés.</span><span class="sxs-lookup"><span data-stu-id="528dd-107">A handle to an internal structure describing the dropped files.</span></span> <span data-ttu-id="528dd-108">Transmettez ce handle [**DragFinish**](/windows/desktop/api/Shellapi/nf-shellapi-dragfinish), [**DragQueryFile**](/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea)ou [**DragQueryPoint**](/windows/desktop/api/Shellapi/nf-shellapi-dragquerypoint) pour récupérer des informations sur les fichiers déplacés.</span><span class="sxs-lookup"><span data-stu-id="528dd-108">Pass this handle [**DragFinish**](/windows/desktop/api/Shellapi/nf-shellapi-dragfinish), [**DragQueryFile**](/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea), or [**DragQueryPoint**](/windows/desktop/api/Shellapi/nf-shellapi-dragquerypoint) to retrieve information about the dropped files.</span></span>

</dd> <dt>

<span data-ttu-id="528dd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="528dd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="528dd-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="528dd-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="528dd-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="528dd-111">Return value</span></span>

<span data-ttu-id="528dd-112">Une application doit retourner zéro si elle traite ce message.</span><span class="sxs-lookup"><span data-stu-id="528dd-112">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="528dd-113">Notes</span><span class="sxs-lookup"><span data-stu-id="528dd-113">Remarks</span></span>

<span data-ttu-id="528dd-114">Le descripteur HDROP est déclaré dans shellapi. h.</span><span class="sxs-lookup"><span data-stu-id="528dd-114">The HDROP handle is declared in Shellapi.h.</span></span> <span data-ttu-id="528dd-115">Vous devez inclure cet en-tête dans votre build pour utiliser **WM \_ DROPFILES**.</span><span class="sxs-lookup"><span data-stu-id="528dd-115">You must include this header in your build to use **WM\_DROPFILES**.</span></span> <span data-ttu-id="528dd-116">Pour plus d’informations sur l’utilisation de la fonction glisser-déplacer pour transférer des données de Shell, consultez [transfert de données de Shell à l’aide de la fonction glisser-déplacer ou du presse-papiers](dragdrop.md).</span><span class="sxs-lookup"><span data-stu-id="528dd-116">For further discussion of how to use drag-and-drop to transfer Shell data, see [Transferring Shell Data Using Drag-and-Drop or the Clipboard](dragdrop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="528dd-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="528dd-117">Requirements</span></span>



| <span data-ttu-id="528dd-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="528dd-118">Requirement</span></span> | <span data-ttu-id="528dd-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="528dd-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="528dd-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="528dd-120">Minimum supported client</span></span><br/> | <span data-ttu-id="528dd-121">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="528dd-121">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="528dd-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="528dd-122">Minimum supported server</span></span><br/> | <span data-ttu-id="528dd-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="528dd-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="528dd-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="528dd-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="528dd-125"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="528dd-125"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="528dd-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="528dd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="528dd-127">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="528dd-127">**PostMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="528dd-128">**DragAcceptFiles**</span><span class="sxs-lookup"><span data-stu-id="528dd-128">**DragAcceptFiles**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-dragacceptfiles)
</dt> </dl>

 

 
