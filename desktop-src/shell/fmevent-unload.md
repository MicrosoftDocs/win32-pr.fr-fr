---
description: Envoyé à une DLL d’extension lors du déchargement de la DLL par le gestionnaire de fichiers.
title: Message FMEVENT_UNLOAD (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_UNLOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 15ffcd46-602f-4ad0-9c58-0b8056b9cac4
ms.openlocfilehash: 140fbdc79980a2ab6ba9f50b8815429436df0d3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111747"
---
# <a name="fmevent_unload-message"></a><span data-ttu-id="fac99-103">FMEVENT \_ décharger le message</span><span class="sxs-lookup"><span data-stu-id="fac99-103">FMEVENT\_UNLOAD message</span></span>

<span data-ttu-id="fac99-104">Envoyé à une DLL d’extension lors du déchargement de la DLL par le gestionnaire de fichiers.</span><span class="sxs-lookup"><span data-stu-id="fac99-104">Sent to an extension DLL when File Manager is unloading the DLL.</span></span>

## <a name="parameters"></a><span data-ttu-id="fac99-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fac99-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fac99-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fac99-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="fac99-107">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="fac99-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="fac99-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fac99-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="fac99-109">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="fac99-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fac99-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fac99-110">Return value</span></span>

<span data-ttu-id="fac99-111">Une DLL d’extension doit retourner zéro si elle traite ce message.</span><span class="sxs-lookup"><span data-stu-id="fac99-111">An extension DLL should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="fac99-112">Notes</span><span class="sxs-lookup"><span data-stu-id="fac99-112">Remarks</span></span>

<span data-ttu-id="fac99-113">Les valeurs *HWND* et **HMENU** transmises avec les messages [**FMEVENT \_ Load**](fmevent-load.md) et [**FMEVENT \_ INITMENU**](fmevent-initmenu.md) peuvent ne pas être valides au moment de l’envoi de ce message.</span><span class="sxs-lookup"><span data-stu-id="fac99-113">The *hwnd* and **hMenu** values passed with the [**FMEVENT\_LOAD**](fmevent-load.md) and [**FMEVENT\_INITMENU**](fmevent-initmenu.md) messages may not be valid at the time this message is sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="fac99-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="fac99-114">Requirements</span></span>



| <span data-ttu-id="fac99-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fac99-115">Requirement</span></span> | <span data-ttu-id="fac99-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="fac99-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fac99-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fac99-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fac99-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fac99-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="fac99-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fac99-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fac99-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fac99-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="fac99-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="fac99-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="fac99-122"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="fac99-122"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fac99-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fac99-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fac99-124">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="fac99-124">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




