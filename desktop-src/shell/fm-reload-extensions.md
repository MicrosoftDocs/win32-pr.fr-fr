---
description: Envoyé par une extension du gestionnaire de fichiers (ou une autre application) pour faire en sorte que le gestionnaire de fichiers recharge toutes les dll d’extension listées dans la \[ section addons \] du fichier Winfile.ini.
ms.assetid: 5103a986-5f45-4deb-aaae-c6e87cb60051
title: Message FM_RELOAD_EXTENSIONS (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_RELOAD_EXTENSIONS
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.openlocfilehash: 9e82ec9ec638cb70cc7b571ed9e5e76d604cd4da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973230"
---
# <a name="fm_reload_extensions-message"></a><span data-ttu-id="1073f-103">\_Message d’extensions de REchargement FM \_</span><span class="sxs-lookup"><span data-stu-id="1073f-103">FM\_RELOAD\_EXTENSIONS message</span></span>

<span data-ttu-id="1073f-104">Envoyé par une extension du gestionnaire de fichiers (ou une autre application) pour faire en sorte que le gestionnaire de fichiers recharge toutes les dll d’extension listées dans la \[ section addons \] du fichier Winfile.ini.</span><span class="sxs-lookup"><span data-stu-id="1073f-104">Sent by a File Manager extension (or another application) to cause File Manager to reload all extension DLLs listed in the \[AddOns\] section of the Winfile.ini file.</span></span>

## <a name="parameters"></a><span data-ttu-id="1073f-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1073f-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1073f-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1073f-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1073f-107">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="1073f-107">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1073f-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1073f-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1073f-109">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="1073f-109">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1073f-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1073f-110">Return value</span></span>

<span data-ttu-id="1073f-111">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="1073f-111">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1073f-112">Notes</span><span class="sxs-lookup"><span data-stu-id="1073f-112">Remarks</span></span>

<span data-ttu-id="1073f-113">D’autres applications peuvent utiliser la fonction [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) pour envoyer ce message au gestionnaire de fichiers.</span><span class="sxs-lookup"><span data-stu-id="1073f-113">Other applications can use the [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) function to send this message to File Manager.</span></span> <span data-ttu-id="1073f-114">Pour obtenir le handle de fenêtre appropriée du gestionnaire de fichiers, une application peut spécifier « WFS \_ Frame » comme paramètre *lpszClassName* dans un appel à la fonction [**FindWindow**](/windows/win32/api/winuser/nf-winuser-findwindowa) .</span><span class="sxs-lookup"><span data-stu-id="1073f-114">To obtain the appropriate File Manager window handle, an application can specify "WFS\_Frame" as the *lpszClassName* parameter in a call to the [**FindWindow**](/windows/win32/api/winuser/nf-winuser-findwindowa) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="1073f-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1073f-115">Requirements</span></span>



| <span data-ttu-id="1073f-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1073f-116">Requirement</span></span> | <span data-ttu-id="1073f-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="1073f-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1073f-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1073f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1073f-119">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1073f-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="1073f-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1073f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1073f-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1073f-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1073f-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="1073f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1073f-123"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="1073f-123"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1073f-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1073f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1073f-125">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="1073f-125">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 
