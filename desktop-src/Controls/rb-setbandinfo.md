---
title: Message RB_SETBANDINFO (commctrl. h)
description: Définit les caractéristiques d’une bande existante dans un contrôle rebar.
ms.assetid: 00021c35-612d-4278-b10c-6e9f1f45a543
keywords:
- RB_SETBANDINFO les contrôles de message Windows
topic_type:
- apiref
api_name:
- RB_SETBANDINFO
- RB_SETBANDINFOA
- RB_SETBANDINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92e81377a40f8b6054f5d8cfae16837621b77b61
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466074"
---
# <a name="rb_setbandinfo-message"></a><span data-ttu-id="22063-104">\_Message SETBANDINFO RB</span><span class="sxs-lookup"><span data-stu-id="22063-104">RB\_SETBANDINFO message</span></span>

<span data-ttu-id="22063-105">Définit les caractéristiques d’une bande existante dans un contrôle rebar.</span><span class="sxs-lookup"><span data-stu-id="22063-105">Sets characteristics of an existing band in a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="22063-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="22063-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22063-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="22063-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="22063-108">Index de base zéro de la bande devant recevoir les nouveaux paramètres.</span><span class="sxs-lookup"><span data-stu-id="22063-108">Zero-based index of the band to receive the new settings.</span></span>

</dd> <dt>

<span data-ttu-id="22063-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="22063-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="22063-110">Pointeur vers une structure [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) qui définit la bande à modifier et les nouveaux paramètres.</span><span class="sxs-lookup"><span data-stu-id="22063-110">Pointer to a [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure that defines the band to be modified and the new settings.</span></span> <span data-ttu-id="22063-111">Avant d’envoyer ce message, vous devez définir la structure **sizeof**(REBARBANDINFO) pour le membre **cbSize** de cette structure.</span><span class="sxs-lookup"><span data-stu-id="22063-111">Before sending this message, you must set the **cbSize** member of this structure to the **sizeof**(REBARBANDINFO) structure.</span></span> <span data-ttu-id="22063-112">En outre, vous devez définir le membre **CCH** de la structure **REBARBANDINFO** sur la taille de la mémoire tampon **lpText** lorsque le \_ texte RBBIM est spécifié.</span><span class="sxs-lookup"><span data-stu-id="22063-112">Additionally, you must set the **cch** member of the **REBARBANDINFO** structure to the size of the **lpText** buffer when RBBIM\_TEXT is specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22063-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="22063-113">Return value</span></span>

<span data-ttu-id="22063-114">Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="22063-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="22063-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="22063-115">Requirements</span></span>



| <span data-ttu-id="22063-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="22063-116">Requirement</span></span> | <span data-ttu-id="22063-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="22063-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="22063-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="22063-118">Minimum supported client</span></span><br/> | <span data-ttu-id="22063-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="22063-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="22063-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="22063-120">Minimum supported server</span></span><br/> | <span data-ttu-id="22063-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="22063-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="22063-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="22063-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="22063-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="22063-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="22063-124">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="22063-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="22063-125">**RB \_ SETBANDINFOW** (Unicode) et **RB \_ SETBANDINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="22063-125">**RB\_SETBANDINFOW** (Unicode) and **RB\_SETBANDINFOA** (ANSI)</span></span><br/>             |



 

 





