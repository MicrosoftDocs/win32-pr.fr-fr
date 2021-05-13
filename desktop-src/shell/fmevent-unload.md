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
ms.openlocfilehash: 24b5b2a77393178cad545cb63c1524a8d7e92c5c
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843070"
---
# <a name="fmevent_unload-message"></a><span data-ttu-id="3dcc8-103">FMEVENT \_ décharger le message</span><span class="sxs-lookup"><span data-stu-id="3dcc8-103">FMEVENT\_UNLOAD message</span></span>

<span data-ttu-id="3dcc8-104">Envoyé à une DLL d’extension lors du déchargement de la DLL par le gestionnaire de fichiers.</span><span class="sxs-lookup"><span data-stu-id="3dcc8-104">Sent to an extension DLL when File Manager is unloading the DLL.</span></span>

## <a name="parameters"></a><span data-ttu-id="3dcc8-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3dcc8-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3dcc8-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3dcc8-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="3dcc8-107">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="3dcc8-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="3dcc8-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3dcc8-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="3dcc8-109">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="3dcc8-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3dcc8-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3dcc8-110">Return value</span></span>

<span data-ttu-id="3dcc8-111">Une DLL d’extension doit retourner zéro si elle traite ce message.</span><span class="sxs-lookup"><span data-stu-id="3dcc8-111">An extension DLL should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="3dcc8-112">Notes</span><span class="sxs-lookup"><span data-stu-id="3dcc8-112">Remarks</span></span>

<span data-ttu-id="3dcc8-113">Les valeurs *HWND* et **HMENU** transmises avec les messages [**FMEVENT \_ Load**](fmevent-load.md) et [**FMEVENT \_ INITMENU**](fmevent-initmenu.md) peuvent ne pas être valides au moment de l’envoi de ce message.</span><span class="sxs-lookup"><span data-stu-id="3dcc8-113">The *hwnd* and **hMenu** values passed with the [**FMEVENT\_LOAD**](fmevent-load.md) and [**FMEVENT\_INITMENU**](fmevent-initmenu.md) messages may not be valid at the time this message is sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="3dcc8-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3dcc8-114">Requirements</span></span>



| <span data-ttu-id="3dcc8-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3dcc8-115">Requirement</span></span> | <span data-ttu-id="3dcc8-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="3dcc8-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3dcc8-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3dcc8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3dcc8-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3dcc8-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="3dcc8-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3dcc8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3dcc8-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3dcc8-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3dcc8-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="3dcc8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3dcc8-122"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="3dcc8-122"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3dcc8-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3dcc8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dcc8-124">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="3dcc8-124">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




